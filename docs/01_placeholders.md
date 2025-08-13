# Placeholder Text
Documentation frequently uses **placeholder text** to show where you need to enter something specific to *your* system. These are not meant to be copied literally, instead existing to notify you not to do that. If you treat placeholders as fixed text, or don't read the documentation close enough to notice when a placeholder is being used, commands will often fail or behave in unexpected ways. 

Here are some common examples of placeholders:

* `<your-username>`

* `[path/to/your/file]`

* `example.com`

* `my-project`

* `REPLACE_ME`

An important thing to pay attention to regarding placeholder text is the surrounding punctuation. Placeholders are often surrounded by square, curly, or angle brackets (`[]`, `{}`, `<>`) to make the part you need to replace more noticeable. You're **not** supposed to include the brackets when you enter your own value.

## How to Recognize a Placeholder

If you're unsure whether something is a placeholder:

* Ask: "Is this value likely to change depending on who's using it or where it's run?"

* Is it generic, vague, or labeled as "your-", "my-", or "example-"?

* Is it in a context where you'd normally enter personal/system specific info (e.g. usernames, file paths, URLs, keys)?

Sometime the docs won't use any special punctuation at all, just words like `myproject`, `your_site`, or `localhost`. Be alert for these even if they *look* like real values.

>### Exercise 1
>Take a look at this [Docker SSH tutorial](https://det-lab.github.io/docker-lesson/03_docker-ssh/) and see if you can find all of the lines which use placeholder text.
>
><details>
><summary>Solution</summary>
><p>
>
>```bash
>mkdir example-ssh-container
>cd example-ssh-container
>```
>
>```bash
>RUN mkdir /var/run/sshd && echo 'root:<your-new-password>' | chpasswd
>```
>
>```bash
>docker build -t example-ssh-container .
>```
>
>```bash
>docker run -d -p 2222:22 --name ssh-container example-ssh-container
>```
></p>
></details>

>### Exercise 2
>Now let's take a look at this [SSH key generation guide](https://docs.gitlab.com/user/ssh/#generate-an-ssh-key-pair). Try and find all of the lines between the sections **Generate an SSH key pair** and **Add an SSH key to your GitLab account** which contain placeholder text.
>
><details>
><summary>Solution</summary>
><p>
>
>```shell
>ssh-keygen -t ed25519 -C "<comment>"
>```
>
>```shell
>ssh-keygen -t rsa -b 2048 -C "<comment>"
>```
>
>```shell
>ssh-add <directory to private SSH key>
>```
>
>```shell
># GitLab.com
>Host gitlab.com
>  PreferredAuthentications publickey
>  IdentityFile ~/.ssh/gitlab_com_rsa
>
># Private GitLab instance
>Host gitlab.company.com
>  PreferredAuthentications publickey
>  IdentityFile ~/.ssh/example_com_rsa
>```
>
>**gitlab_com_rsa**, **gitlab.company.com**, and **example_com_rsa** are all placeholder text. In this case, the placeholder text is not set off with any kind of brackets which can make it particularly hard to notice.
>
></p>
></details>

>### Exercise 3
>Try and find all the placeholder text from this guide for [Getting Started - First-Time Git Setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).
>
><details>
><summary>Solution</summary>
><p>
>
>```bash
>[path]/etc/gitconfig
>```
>
>```bash
>$ git config --global user.name "John Doe"
>$ git config --global user.email johndoe@example.com
>```
>
>```bash
>$ git config --global init.defaultBranch main
>```
>
>```bash
>$ git config --list
>user.name=John Doe
>user.email=johndoe@example.com
>```
>
></p>
></details>

## Best Practices

* Scan the entire command before copying it. Identify which parts might need replacing.

* Don't include the punctuation unless the doc says to (or if the brackets are required syntax in that language).

* Check multiple examples. Sometimes a later example clarifies what an earlier placeholder meant.

* When in doubt, try it with a safe value and see how the system responds.

---

Now that you’re comfortable identifying and understanding placeholders, it’s time to explore how to move forward confidently with the next steps when working through documentation. [Click here to continue to the next section](02_follow_steps.md) where we will go over best practices for following steps.