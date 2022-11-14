# **This is my Week 7 Lab Report, by Christophian Austin Sulaiman**

**For this Week Part 1, I will be choosing the first option:**

## In DocSearchServer.java, change the name of the start parameter of getFiles, and all of its uses, to instead be called base.

We can do this in under 30 key presses by doing these individual key-presses (using vim shortcuts):

I will be explaining what each shortcut does.

`Vim DocSearchServer.java` (For this, we will be entering the normal mode for the vim of DocSearchServer.java)
`<Enter>`
`/start` (This command is used to search through the file DocSearchServer for any "start" in it)
`<Enter>`
`ce` (This command is used to delete the word your editing cursor is at (which in this case will be "start"))
`I (insert)` (This is to enter insert mode in VIM)
`Type “base”` (Here we are just typing the replacement word)
`<esc>` (esc to go back to normal mode)
`n` (n is to cycle through the word "start" again, from top to bottom)
`ce`
`Insert(I)`
`Type “base”`
`<esc>`
`n`
`ce`
`Insert(I)`
`Type “base”`
`<esc>`
`:wq` (this is to save and exit the vim file)
`<Enter>`

This is 19 total key presses, which is reduced significantly using some useful vim shortcuts.



# ***Part 2***

Editing using Visual Studio Code: 1 minute 34 seconds


Editing remotely with SSH: 30 seconds

Which of these two styles would you prefer using if you had to work on a program that you were running remotely, and why?

-I would definitely prefer working on remote server/SSH since it will be a lot faster. Using vim shortcuts can reduce time spent editing a code by half which is
a lot especially when working on larger codes.

What about the project or task might factor into your decision one way or another? (If nothing would affect your decision, say so and why!)

-Since I am using a windows device, I couldn't enter bash without being in a remote server. Therefore if I want to use bash to run any files it would be a lot more time consuming if I use
Visual Studio Code, since I could use bash in remote server. Plus, even if the project was a large code, I would utilize shortcuts in vim to delete words, find words, etc, using commands
like "/word" and n. For shorter codes/projects, there would be no downfall to using vim instead of VSC.