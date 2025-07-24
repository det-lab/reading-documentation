# Follow Every Step
One of the most common sources of frustration when working through technical documentation is skipping a step, intentionally or not. Many commands and configuration instructions rely on prior steps being completed exactly as written. A missing flag, a misread instruction, or a skipped environment setup can cause errors that are difficult to trace back to their cause.

When you're following documentation, be sure to **read each step in full before acting**. Don't just copy and paste blocks of code without understanding the context or prerequisites.

Sometimes, a step looks trivial or like something you've done before, but includes a small variation that makes it essential. For example, when installing the Windows Subsystem for Linux (WSL), the instructions include the line:

> "Run Powershell as Administrator"

If you skip that and open a normal Powershell window, several of the next steps will silently fail or produce errors, and it may not be obvious that the problem was your permissions when you go to troubleshoot them. The documentation assumes you followed *every* step, so if you didn't, the help it provides may no longer apply. 

This kind of detail - how a program is run, which directory you're in, whether a file has been downloaded yet - is often where beginner mistakes happen. Always check for:

* Role or permissions requirements (e.g., "run as root", or "use an admin shell")

* Environment setup (e.g., "ensure Python 3.10+ is installed")

* Context switches (e.g., "now open a Linux terminal" after installing WSL)

Skipping a step doesn't always cause an immediate error. Sometimes it causes a later step to break in a way that can be hard to diagnose. Even worse, if you're working on something with many interdependent steps, you might spend hours debugging something that's actually caused by a skipped or altered instruction from the very beginning.