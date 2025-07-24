# Placeholder Text
Documentation frequently uses **placeholder text** to show where you need to enter something specific to *your* system. These are not meant to be copied literally, instead existing to notify you not to do that. If you treat placeholders as fixed text, or don't read the documentation close enough to notice when a placeholder is being used, commands will often fail or behave in unexpected ways. 

Here are some common examples of placeholders:

* `<your-username>`

* `[path/to/your/file]`

* `example.com`

* `my-project`

* `REPLACE_ME`

An important thing to pay attention to regarding placeholder text is the surrounding punctuation. Placeholders are often surrounded by square, curly, or angle brackets (`[]`, `{}`, `<>`) to make the part you need to replace more noticeable. You're usually **not** supposed to include the brackets when you enter your own value.

## How to Recognize a Placeholder

If you're unsure whether something is a placeholder:

* Ask: "Is this value likely to change depending on who's using it or where it's run?"

* Is it generic, vague, or labeled as "your-", "my-", or "example-"?

* Is it in a context where you'd normally enter personal/system specific info (e.g. usernames, file paths, URLs, keys)?

Sometime the docs won't use any special punctuation at all, just words like `myproject`, `your_site`, or `localhost`. Be alert for these even if they *look* like real values.

## Best Practices

* Scan the entire command before copying it. Identify which parts might need replacing.

* Don't include the punctuation unless the doc says to (or if the brackets are required syntax in that language).

* Check multiple examples. Sometimes a later example clarifies what an earlier placeholder meant.

* When in doubt, try it with a safe value and see how the system responds.