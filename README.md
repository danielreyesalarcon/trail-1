$ cd C:/Users/user/my_project
$ git init
$ git add LICENSE
$ git commit -m 'Initial project version'
$ git clone https://github.com/libgit2/libgit2 mylibgit
s git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean
$ echo 'My Project' > README
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)
  
    README
  
 nothing added to commit but untracked files present (use "git add" to track)
$ git add README  
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
  
  new file:  README
  
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout --<file>..." to discard changes in working directory)
  
   modified:  CONTRIBUTING.md
$ git add CONTRIBUTING.md
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
  
  new file:  README
  modified:  CONTRIBUTING.md
$ vim CONTRIBUTING.md
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
  
  new file: README
  modified: CONTRIBUTING.md
  
Changes not staged to commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)
  
  modified:  CONTRIBUTING.md
$ git add CONTRIBUTING.md
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
  
  new file:  README
  modified:  CONTRIBUTING.md 
  
$ git status -s
  M README
MM Rakefile
A lib/git.rb
M lib/simplegit.rb
?? LICENSE.txt  
$ cat .gitignore
*.[oa]
*~
# ignore all .a files
*.a
  
# but do track lib.a, even though you're ignoring .a files above
!lib.a
  
# only ignore the TODO file in the current directory, not subdir/TODO
/TODO
  
# ignore all files in any directory named build
  
# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt
  
# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf  
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
  
  modified:  README
  
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)
  
  modified:  CONTRIBUTING.md
$ git diff
diff --git a/CONTRIBUTING.md b/CONTRIBUTING.md
index 8ebb991..643e24f 100644
--- a/CONTRIBUTING.md
+++ b/CONTRIBUTING.md
@@ -65,7 +65,8 @@ branch directly, things can get messy.
 I am learning to make changes on this system
-merged in.
+merged in. Split changes into comprehensive chuncks if I have lots of code on me
+longer than dozen lines.  
$ git diff --staged
diff --git a/README b/README
new file mode 100644
index 0000000..03902a1
--- /dev/null
+++ b/README
@@ -0,0 +1 @@
+My Project  
