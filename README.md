# task 1
```sh
$ git init
# Initialized empty Git repository in /home/timur/BaltaevTimur/workspace/lab_02/.git/
```

```sh
$ git remote add origin https://github.com/BaltaevTimur/lab_02.git
$ alias edit=nano
$ edit hello_world.cpp
```
### hello_world.cpp
```sh
#include <iostream>
using namespace std;

int main()
{
  cout << "Hello world!";
  return 0;
}
```
```sh
$ git add hello_world.cpp
$ git commit -m"added hello_world.cpp"
# [main (root-commit) b01a693] added hello_world.cpp
# 1 file changed, 10 insertions(+)
# create mode 100644 hello_world.cpp
```
### adding new branch
```sh
$ git branch master
$ git switch master
$ git push origin master
# Enumerating objects: 3, done.
# Counting objects: 100% (3/3), done.
# Compressing objects: 100% (2/2), done.
# Writing objects: 100% (3/3), 318 bytes | 318.00 KiB/s, done.
# Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
# remote: 
# remote: Create a pull request for 'master' on GitHub by visiting:
# remote:      https://github.com/BaltaevTimur/lab_02/pull/new/master
# remote: 
# To https://github.com/BaltaevTimur/lab_02.git
#  * [new branch]      master -> master
```
### editting hello_world.cpp
```sh
$ edit hello_world.cpp
$ git commit -m"editing hello_world.cpp"
# [master 209fb86] editing hello_world.cpp
# 1 file changed, 4 insertions(+), 3 deletions(-)
$ git push origin master
# Enumerating objects: 5, done.
# Counting objects: 100% (5/5), done.
# Compressing objects: 100% (2/2), done.
# Writing objects: 100% (3/3), 373 bytes | 373.00 KiB/s, done.
# Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
# To https://github.com/BaltaevTimur/lab_02.git
#    b01a693..209fb86  master -> master
```
 - hello_world.cpp
```sh
#include <iostream>
#include <string>
using namespace std;

int main()
{
string name;
cin >> name;
cout << "Hello world from " << name;
return 0;
}
```
 - файл не надо добавлять повторно, так как он уже есть и нужно закоммитить изменения файла
### $ git log
```sh
commit 209fb86a16851241b2a3140bf0b30a1445d80f20 (HEAD -> master, origin/master)
Author: BaltaevTimur <timur.baltaev.2005@gmail.com>
Date:   Mon Mar 11 09:35:25 2024 +0300

    editing hello_world.cpp

commit b01a6933d5755a89c8e33ebefd1277a4abedee79 (main)
Author: BaltaevTimur <timur.baltaev.2005@gmail.com>
Date:   Mon Mar 11 08:44:50 2024 +0300

    added hello_world.cpp
```
# tast 2

```sh
$ git branch patch1
$ git switch patch1
# Switched to branch 'patch1'
$ edit hello_world.cpp
```

 - hello_world.cpp

```sh
#include <iostream>
#include <string>


int main()
{
std::string name;
std::cin >> name;
std::cout << "Hello world from " << name;
return 0;
}
```

```sh
$ git commit -m"editting hello_world.cpp"
# [patch1 c020edc] editting hello_world.cpp
#  1 file changed, 4 insertions(+), 4 deletions(-)
$ git push origin patch1
# Enumerating objects: 5, done.
# Counting objects: 100% (5/5), done.
# Compressing objects: 100% (2/2), done.
# Writing objects: 100% (3/3), 368 bytes | 368.00 KiB/s, done.
# Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
# remote: 
# remote: Create a pull request for 'patch1' on GitHub by visiting:
# remote:      https://github.com/BaltaevTimur/lab_02/pull/new/patch1
# remote: 
# To https://github.com/BaltaevTimur/lab_02.git
#  * [new branch]      patch1 -> patch1
$ git rebase master
# Current branch patch1 is up to date.
$ git switch master
# Switched to branch 'master'
$ git merge patch1
# Updating 209fb86..c020edc
# Fast-forward
#  hello_world.cpp | 8 ++++----
#  1 file changed, 4 insertions(+), 4 deletions(-)
$ git branch -d patch1
# Deleted branch patch1 (was c020edc).
```
# task 3
```sh
$ git branch patch2
$ git switch patch2
# Switched to branch 'patch2'
```



