NOTE: This is part of practice at Capital One's Tech Summit 2026 GIT Workshop

Git Code-Along
For this part of the day, we're all going to follow the process of creating repositories, committing to them, and reverting changes.

Create a Repository
Open the terminal.
Create a new folder by entering: mkdir git-practice2
Move into that folder by entering: cd git-practice2
Make this a git repository by entering: git init
Create a file named README.md by entering: touch README.md
Open the README file in a text editor, and describe the poet William Wordsworth. Kidding! Introduce this repository as a collection of poetry by editing the README.md file to have a title line.
Back in the command line, verify that there are changes ready to be committed by entering: git status
Stage your changes by entering: git add README.md
Run git status to verify that README.md has been added to the staging area.
Commit these changes by entering git commit -m "Add initial README file"
Run git status to verify that there are no more staged changes.
Create another file named cloud.md
Commit Changes
Edit cloud.md to contain the following text:
I wandered lonely as a cloud
That floats on high o'er vales and hills,
When all at once I saw a crowd,
A host, of golden daffodils;
Beside the lake, beneath the trees,
Fluttering and dancing in the breeze.
Stage and commit your changes.
Append the following to the end of cloud.md:
Continuous as the stars that shine
And twinkle on the milky way,
They stretched in never-ending lip
Along the margin of a bay:
Ten thousand saw I at a glance,
Tossing their heads in sprightly dance.
Stage and commit your changes.
Fix a typo: change "never-ending lip" to "never-ending line"
Stage and commit your changes.
View Changes
Verify that these changes were tracked by git by entering: git log
Copy the hash for the very first thing you committed (which will be at the bottom of the log) to the clipboard. The hash will be different for every person and every commit, but will look something like 13c988d4f15e06bcdd0b0af290086a3079cdadb0
View the differences between the last commit and the first commit by entering: git diff HEAD <<hash>> replacing <<hash>> with the hash value.
Practice Branching and Merging
Create and switch to a feature branch by entering git checkout -b formattingFeature.
In this branch, cut up the blocks of text in cloud.md into four blocks of 3 lines:
I wandered lonely as a cloud
That floats on high o'er vales and hills,
When all at once I saw a crowd,

A host, of golden daffodils;
Beside the lake, beneath the trees,
Fluttering and dancing in the breeze.

Continuous as the stars that shine
And twinkle on the milky way,
They stretched in never-ending line

Along the margin of a bay:
Ten thousand saw I at a glance,
Tossing their heads in sprightly dance.
Stage and commit these changes by entering git add cloud.md followed by git commit -m "formatting cloud.md"

Move back to the main branch and merge your feature branch into the main branch by entering git checkout main followed by git merge formattingFeature.
