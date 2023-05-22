# Step 4
$ ssh cs15lsp23fa@ieng6.ucsd.edu // *connects to server*\
`<input password here>` // *I can't set up a trusted connection so this step may be exclusive to me :P*\
![Image](Step4.png)

# Step 5
$ git clone https://github.com/TheColb/lab7.git // *clones the repository to your active directory*\
// *inputting the command "ls" here is good to ensure that it was cloned correctly*\
![Image](Step5.png)

# Step 6
$ cd lab7 // *move to a terminal location within the lab7 file for conviencence*\
$ sh test.sh // *runs the default shell test (This should fail)*\
![Image](Step6.png)

# Step 7
$ vim ListExamples.java // *opens VIM*\
// *in vim I will specify when to click `<enter>`*\
:44 `<enter>` // *go to line 44*\
w `<left arrow>` // *move forward a word, and go back one character*\
i `<backspace>` 2 `<esc>` // *enter insert mode, and replace the 1 with a 2*\
:wq `<enter>`// *save and quit vim*
![Image](Step7.png)

# Step 8
$ sh test.sh // *runs the test again (it should work this time!)*\
![Image](Step8.png)

# Step 9
$ git add . // *Adds all modified and new files to the staging area.*\
$ git remote set-url origin git@github.com:TheColb/lab7.git // *Changes the remote URL to the specified GitHub repository.*\
// *shoutout ChatGPT for generating that command when I gave it my problem!*\
$ git commit -m "Changed index1 to index2" // *Creates a commit with the given message*\
$ git push // *Uploads local commits to the configured remote repository*\
![Image](Step9.png) \
All done! Your changes should now be in your GitHub repository!
