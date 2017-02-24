# Coding Cheat Sheet
## Markdown
In order to display C# in the second-level header, you will need to close the header with a # in addition to the # from C#. A space between the last two # is needed.

These will NOT work

```
## C##
## C#
```

This will work

```
## C# #
```

## Git

```
git clone url
git add foo
git status
git log
git add '*.txt'
git remote add origin https://github.com/tingzhi/foo.git
git push -u origin master
git push 
git pull
git pull origin master
git diff HEAD
git diff --staged
git reset octofamily/octodog.txt  // unstaging octodog.txt
git checkout -- octocat.txt 
// undo changes to octocat.txt to the state of last commit
git branch clean_up
git checkout clean_up //switch to clean_up branch
git rm '*.txt'
git checkout master
git merge clean_up // making sure you are on master branch
git branch -d clean_up
git push
```
Commands that I need to double check.

```
git add -u
git commit -au "foo"
```

## C# #
### Code Snippet
- prop: create property
- cw: Console.WriteLine()
- ctor: create constructor


### Important Concepts
- CLR: Common Language Runtime
- FCL: Framework Class Library

### Questions
- How to quickly move cursor around in VS2015 editor?

### Syntax
```
switch(foo)
{
	case "A":
		break;
	case "B":
		break;
	default:
		break;
}
```