# Step 4
![step 4 screenshot](https://user-images.githubusercontent.com/83570191/221434259-f8290981-34eb-463b-8f2a-b86334736158.png)

I typed `ssh cs15lwi23ask@ieng6.ucsd.edu<enter>`. This logs me in to the my remote account on ieng6. 


# Step 5 
![step 5 screenshot](https://user-images.githubusercontent.com/83570191/221434361-b4d6ed04-fa07-48da-82ae-75c31e6c2b0d.png)

I typed `git clone <ctrl^v><enter>` after copying my forked lab7 repository https link. This results in the lab7 repository being cloned to the home directory of my remote computer. To note, when I push the changes later, I use the ssh link to my repository, so copying the https link now is not an issue.

# Step 6
![step 6 screenshot](https://user-images.githubusercontent.com/83570191/221434961-76a39168-dd77-4995-aa28-6c8786765c98.png)

I typed `cd l<tab><enter>`. This autocompletes to `cd lab7/<enter>`, and changes the working directory to be the lab7 one. After that I did `ctrl^v<enter>` to paste the javac command, after copying it from the cse15l week 3 website, which compiles all the java files in the directory. I then did `<ctrl^v> ListExamplesTests<enter>` to run the tests, which resulted in the output of 2 tests run, 1 test failed.

# Step 7
![step 7 screenshot](https://user-images.githubusercontent.com/83570191/221435643-7234f087-04f9-4ebc-9abd-431198e05d58.png)


I typed `nano L<tab>.java<enter>`. This autocompletes to `nano ListExamples.java<enter>`, and opens up an interface in the command line to allow me to edit the file. I then held down the `<down>` key to scroll down, equivalent to 42 presses of the `<down>` key. I then pressed `<right>` 12 times, then pressed `<backspace>`, then I typed the number 2. This allowed me to edit the program and fix the bug. I then did `<ctrl^o><enter>` to save my changes, then `<ctrl^x><enter>` to close the nano interface.

# Step 8
![step 8 screenshot](https://user-images.githubusercontent.com/83570191/221435751-cbbf33a2-7b2e-467b-bf21-0dae2d005962.png)

I typed `<up><up><up><enter>` to get the javac command from earlier to compile all the java files, then `<up><up><up><enter>` to get the java command to run the tester. 

# Step 9
![git add screenshot](https://user-images.githubusercontent.com/83570191/221435984-5970a34f-b410-43d2-aa43-9589ab7e35e4.png)
![git commit and push screenshot](https://user-images.githubusercontent.com/83570191/221436028-a86e6575-c98d-4d13-8e2d-90137ec3b91b.png)

I typed `git add L<tab>.java<enter>`, which autocomplete to `git add ListExamples.java<enter>`, to add the file which now has been changed to the staging area. I then typed `git commit L<tab>.java -m "Bug fixed"<enter>`, which gets autocompleted to `git commit ListExamples.java -m "Bug fixed"<enter>`, which saves the changes to the loacl repository. I then type `git push <ctrl^v><enter>` after copying my ssh link to my repository, to push the changes from the local repository to the remote repository.




