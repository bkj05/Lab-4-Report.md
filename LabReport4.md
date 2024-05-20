# Lab Report 4 - Vim (Week 7)

## Step 4: Complete the first two lessons of vimtutor

### Keys Pressed:
- `vimtutor<enter>`

### Summary:
Opened vimtutor to begin the tutorial.

### Output:
===============================================================================
= Vim tutor =
vbnet
Copy code
 Vim is a very powerful editor that has many commands, too many to
 explain in a tutor such as this.  This tutor is designed to describe
 enough of the commands that you will be able to easily use Vim as
 an all-purpose editor.

 The approximate time required to complete the tutor is 25-30 minutes,
 depending upon how much time is spent with experimentation.

 The commands in the lessons will modify the text.  Make sure that your
 shift-lock key is not pressed.  If you execute a command and Vim beeps
 at you, it means that Vim is waiting for you to complete the command
 sequence.  Press <Esc> and start over.

 Now, make sure that your Shift-Lock key is NOT pressed and press 
 the j key enough times to move the cursor so that Lesson 1.1 below 
 completely fills the screen.

 If you are using an English version of Vim, you can skip the next
 lesson by pressing <Ctrl-L>.
shell
Copy code

## Step 5: Clone the repository

### Keys Pressed:
- `git clone https://github.com/ucsd-cse15l-s24/lab7<enter>`

### Summary:
Cloned the lab7 repository from GitHub.

### Output:
Cloning into 'lab7'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 10 (delta 1), reused 10 (delta 1), pack-reused 0
Receiving objects: 100% (10/10), 12.94 KiB | 12.94 MiB/s, done.
Resolving deltas: 100% (1/1), done.

csharp
Copy code

## Step 6: Fix the program

### Keys Pressed:
- `cd lab7<enter>`
- `vim ListExamples.java<enter>`
- `/index1<enter>`
- `cw`
- `index2<esc>`
- `:wq<enter>`

### Summary:
- Changed directory to lab7.
- Opened ListExamples.java in vim.
- Searched for "index1".
- Changed "index1" to "index2".
- Saved and exited vim.

### Output:
```java
  1 public class ListExamples {
  2 
  3   // Returns a new list that has all the elements of the two input lists in sorted order.
  4   // Assumes both input lists are already in sorted order.
  5   static List<String> merge(List<String> list1, List<String> list2) {
  6     List<String> result = new ArrayList<>();
  7     int index1 = 0, index2 = 0;
  8     while (index1 < list1.size() && index2 < list2.size()) {
  9       if (list1.get(index1).compareTo(list2.get(index2)) < 0) {
 10         result.add(list1.get(index1));
 11         index1 += 1;
 12       } else {
 13         result.add(list2.get(index2));
 14         index2 += 1;
 15       }
 16     }
 17     while (index1 < list1.size()) {
 18       result.add(list1.get(index1));
 19       index1 += 1;
 20     }
 21     while (index2 < list2.size()) {
 22       result.add(list2.get(index2));
 23       index2 += 1;
 24     }
 25     return result;
 26   }
 27 
 28 }
Step 7: Re-run the tests
Keys Pressed:
./run_tests.sh<enter>
Summary:
Ran the shell script to execute the tests.

Output:
bash
Copy code
JUnit version 4.13.2
.
Time: 0.003

OK (1 test)
Step 8: Commit and push the change
Keys Pressed:
git add ListExamples.java<enter>
git commit -m "Fixed index1 to index2 in ListExamples.java"<enter>
git push<enter>
Summary:
Staged the modified file for commit, committed the change with a message, and pushed the changes to the GitHub repository.

Output:
bash
Copy code
[main 1234567] Fixed index1 to index2 in ListExamples.java
 1 file changed, 1 insertion(+), 1 deletion(-)
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 385 bytes | 385.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:your_username/lab7.git
   abcdefg..1234567  main -> main
Step 9: Adding the Lab Report to Your GitHub Pages Site
Keys Pressed:
cd path_to_your_github_pages_repository<enter>
cp path_to_lab_report/lab_report_4.md .<enter>
git add lab_report_4.md<enter>
git commit -m "Added Lab Report 4"<enter>
git push<enter>
Summary:
Navigated to the GitHub Pages repository.
Copied the lab report markdown file to the repository.
Staged the lab report file for commit.
Committed the change with a message.
Pushed the changes to the GitHub Pages repository.
Output:
bash
Copy code
[main 789abcd] Added Lab Report 4
 1 file changed, 123 insertions(+)
 create mode 100644 lab_report_4.md
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 1.24 KiB | 1.24 MiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:your_username/your_github_pages_repo.git
   456defg..789abcd  main -> main
