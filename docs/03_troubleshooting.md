# When Something Doesn't Work: Troubleshooting with Documentation
Even if you follow the documentation closely, it is still possible to run into errors. This doesn't necessarily mean that the documentation is inadequate or that you made a mistake, but figuring out what went wrong in these situations means approaching the error systematically.

Documentation can be treated much like a map: retrace your steps, look for landmarks you missed, and read carefully for assumptions or conditions that might not have applied to you.

## Revisit the Instructions
When things go wrong, go back to the beginning of the documentation and ask:

* **Did I really complete each step?** Look for things that didn't give feedback; maybe they failed silently.

* **Was I in the right environment?** For example, in the correct folder, using the correct version of Python, etc.

* **Did I skip any prerequisites, notes, or special instructions?** Check for things like *"if you're on macOS...", "requires admin privileges,"* or *"restart your shell after installing..."*

Reading documentation thoroughly often means re-reading it. Especially with long installation or setup processes, going back to the very beginning can often reveal what's missing.

## Identify an Error
If an error message appears, the best option isn't always to just copy and paste it into a search engine. Instead, sometimes try:

* Reading the full error message. It can often include the filename, line number, or command that failed.

* Look at what the command was doing.

* Compare your input to the example. Did you replace placeholders correctly? Were any arguments left out?

Sometimes the error isn't in the line that failed, but instead a result of a previous step having left things in an incorrect state. 

## Look for Context in the Documentation
Good documentation often includes sections for:

* Common errors or known issues

* Platform specific notes

* Version compatibility warnings

* Optional steps that become required in certain cases

For example, the `conda` package manager has multiple steps for installing packages and configuring environments. If a package fails to install, it can often be because the channel wasn't added or the environment wasn't activated. Both are steps that look optional until something breaks.

If the documentation includes a **troubleshooting** or **FAQ** section, go there immediately. They're written precisely for moments like this.

## Gather Evidence and Context Before Seeking Help
If you've checked the documentation and you're still stuck, it's time to look elsewhere. To do that efficiently:

* Search with context. Include tool names and versions when searching for errors.

Instead of `ModuleNotFoundError`, try `pandas ModuleNotFoundError Python 3.11 virtualenv`

* Be ready to explain what you've tried. If you post on a forum or ask a mentor, include the commands you ran, the error you got, and the part of the documentation you were following. 

## Best Practices
* Reread the documentation with fresh eyes when something fails.

* Trust that most errors are solvable with careful review and patience.

* Reach out to a human mentor if at all possible. 

---

With troubleshooting strategies in hand, it’s helpful to take a step back and familiarize yourself with the overall structure of good documentation to better navigate and utilize it. [Click here to continue to the next section](04_basic_structure.md) where we will go over some standard components of technical documentation.