# **This is my Week 7 Lab Report, by Christophian Austin Sulaiman**

**For this Week Part 1, I will be choosing the first option:**

## In DocSearchServer.java, change the name of the start parameter of getFiles, and all of its uses, to instead be called base.

We can do this in under 30 key presses by doing these individual key-presses (using vim shortcuts):

I will be explaining what each shortcut does.

(Sequence of key presses based on the comment on my previous submission without explanation yet)

1. `Vim DocSearchServer.java`

2. `<Enter>`

3. `/start`

4. `<Enter>`

5. `ce`

6. `I`

7. `"base"`

8. `<esc>`

9. `n`

10. `ce`

11. `I`

12. `"base"`

13. `<esc>`

14. `n`

15. `ce`

16. `I`

17. `"base"`

18. `<esc>`

19. `:wq`

20. `<Enter>`

This is a total of 20 key presses, using the vim shorcuts!

(Changes made based on feedback, seperated the key presses with the explanation, key presses on top and explanation at the bottom)

So firstly, we will use vim to edit DocSearchServer.java, by typing "vim DocSearchServer.java" (this will automatically make you in vim normal mode), and then just `<enter>` to execute the command. Next, by typing '/start' we are searching through the file for the word "start", and we `<enter>` to start the search. Your cursor will automatically be on the first "start" that is in the file. Then we type 'ce', which deletes the word your editing cursor is at (which in this case will be "start"), this only works in normal mode. Then we press 'i' to enter to Insert mode again in the vim. Then type 'base' to replace the 'start' we just deleted. After that, press the `<esc>` key to go back to Normal Mode in vim, and press the key 'n' to cycle through the next "start". Repeat the steps 5-9 until all the "start"s we want to replace has been replaced with "base", and then `<esc>` key to go back to normal mode. Lastly to exit and save from the vim mode, type ':wq' and `<Enter>`.



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