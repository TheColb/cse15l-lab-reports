$ ssh cs15lsp23fa@ieng6.ucsd.edu
<input password>
git clone https://github.com/TheColb/lab7.git
cd lab7
sh test.sh
vim ListExamples.java
:44 <enter> w <left arrow> i <backspace> 2 <esc> :wq
sh test.sh
git add .
git remote set-url origin git@github.com:TheColb/lab7.git
git commit -m "Changed index1 to index2"
git push
