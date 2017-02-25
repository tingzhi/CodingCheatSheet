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
- Access modifier: Private, Public, Internal, Protected.
- Internal: only accessible inside the same project. This is the default setting for classes.

### Naming Conventions
- Project name: Grades
- Unit test project name: Grades.Tests
- For private filed: _grades
- For public field: Grades
- For common variables: hoursOfSleep
- For method name: AddGrade

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
Enumeration

```
public enum PayrollType
{
	Contractor = 1,
	Salaried,
	Executive,
	Hourly
}

if(employee.Role == PayrollType.Hourly)
{
	// ...
}
```

How to compare two strings

```
string name1 = "Scott";
string name2 = "scott";

bool areEqual = name1.Equals(name2, StringComparison.CurrentCulture);
```

Immutable

```
private static void Immutable()
        {
            string name = " Scott ";
            name = name.Trim();
            Console.WriteLine(name);

            DateTime date = new DateTime(2014, 12, 3);
            date = date.AddHours(1);
            Console.WriteLine(date);
        }
```

Array Syntax

```
private static void Arrays()
        {
            float[] grades;  // List<float> _grades
            grades = new float[3];

            AddGrades(grades);

            foreach(float grade in grades)
            {
                Console.WriteLine(grade);
            }
        }

        private static void AddGrades(float[] grades)
        {
            grades[0] = 91f;
            grades[1] = 98f;
            grades[2] = 86f;
        }
```

Compare Arry with List

```
float[] grades // This is an array
grades.Length

List<float> grades // This is a list
grades.Count
```

### Important Tips
- Write class as default. Write struct with caution. 99% of the time, you will use class instead of struct.
