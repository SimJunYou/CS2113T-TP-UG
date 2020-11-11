<span style="font-size:150%'">ra.VI User Guide</span>

Welcome to the ra.VI User Guide! Choose a section from the table of contents on the left, or simply start reading from the introduction. This User Guide will give you step-by-step instructions to start your journey in planning out your NUS life.

# Introduction

Repository Assistant with a Versatile Interface (ra.VI) is a desktop app for managing tasks, deadlines, and timetable, optimized for use via a Command Line Interface (CLI). If you can type fast, ra.VI can manage your tasks and timetable faster than traditional GUI apps.

This user guide aims to provide you with a clear documentation of ra.VI's features. In addition, the quick start guide provides an start-to-end setup process to begin tracking your tasks, modules, and lessons with ra.VI.

## Product Overview

ra.VI is targeted at you - the NUS freshman. As a freshman, there are many documents and new procedures that you must get familiar with. This may be daunting for you but ra.VI will provide you with the assistance you need.
By helping you keep track of your tasks and deadlines, you will be able to keep on top of deadlines.
Moreover, the timetable feature helps you to schedule your lessons, allowing you to be more prepared for lessons.
Adding on, ra.VI also allows you to keep track of your CAP, so that you can keep tabs on how well you are doing, motivating you towards that elusive CAP 5.0.

## Keywords

**Command-Line Interface**

The Command-Line Interface (or CLI for short) is a type of user interface which lets a user control a computer program like ra.VI. Instead of the Graphical User Interface (GUI) with buttons and menus like you are probably used to, the CLI is entirely text-based. This makes it less intuitive but far faster to use, especially if you are a fast typer!

**Tasks**

A task refers to something that you would like to get done. This refers to reading a book or doing an assignment. Tasks can be created with or without a deadline.

**Deadline**

A deadline refers to a date and time associated with a task. This is in the format: DAY-MONTH-YEAR TIME_24H, e.g. `23-12-2020 1400` or `1-2-2000 0800` <br>

**Modules**

A module refers to a module taken under NUS. Entered modules will be checked against the list of NUS modules taken from [NUSMods](https://nusmods.com/timetable/sem-1). <br>

**Module Code**

A module code refers to the **official** module code of the module you are trying to refer to. As with modules, ra.VI will be taking reference from [NUSMods](https://nusmods.com/timetable/sem-1). <br>

**CAP**

CAP refers to Cumulative Average Point, which is the [grading system used by NUS](http://www.nus.edu.sg/registrar/academic-information-policies/graduate/modular-system). The CAP will be calculated based on your modules and the grades you have assigned to them. <br>

**Done**

Any task can be marked as “done”. This will signify completion of the task so that you can get an easy view of any remaining tasks. <br>

**Timetable**

The timetable holds all the lessons you take. It allows you to add lessons for modules you are taking. <br>

**NUS Week Number**

NUS’s semesters last for 6 weeks, followed by Recess Week, then another 6 weeks, and finally Reading Week for a total of 14 weeks. When you first use ra.VI, you will be asked to tell ra.VI the current NUS week number. After setting the timetable up the first time, you do not need to go through the set up again.<br>

**Day**

Some commands have a `day` field for you to specify a certain day. Here are the accepted values:\
`MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY`, `SUNDAY`

```warning
This format must be followed exactly! Fully spelled out in uppercase. `Monday`, `Mon`, `monday` are examples of what will **not** work. If you want to specify Monday, only `MONDAY` will work.
```

**Lesson Type**

Some commands have a `lesson_type` field for you to specify a certain type of lesson. Here are the accepted values:\

`TUTORIAL`, `LECTURE`, `SEMINAR`, `LAB`, `RECITATION`, `SESSION`

```warning
Similar to the `day` field, this format must be followed exactly! It has to be fully spelled out as shown here, and entirely in uppercase.
```

**Repeat**

`repeat` is a field to specify how often lessons should repeat.
* `0` - Does not repeat.
* `1` - Repeats every week.
* `2` - Repeats every **even** week.
* `3` - Repeats every **odd** week.

**Time**

Some commands require you to enter a time. The `time` field requires the hours and minutes of the time you want to specify, in the [24H format](https://en.wikipedia.org/wiki/24-hour_clock). For example, 9AM would be `0900` and 2:15PM would be `1415`.

**Deadline**

Some commands require you to enter a date and time for a deadline. The date portion should have the day, month, and year written in numbers and separated with dashes. For example, 30 December 2020 would be `30-12-2020`. The time portion is the same as described in the **Time** explanation above. A full deadline of “15 February 2021 3:30AM” would be `15-02-2021 0330`.

**Undo**

Some commands edit your tasks, modules, and lessons. All commands that edit your information can be undone! Here’s a list:
* Adding / deleting / editing tasks
* Completing tasks
* Adding / deleting / editing modules
* Adding / deleting / editing lessons to / from the timetable
* Resetting the timetable
* Grading a module

## ra.VI’s Interface

![Interface with arrows and labels]()

ra.VI is a CLI application, which means you control it entirely with text commands. ra.VI will “talk” to you with lines of text, as indicated in the diagram.

# Quick Start

1. Ensure that you have Java 11 or above installed.
2. Download the latest version of `ra.VI` from [here](https://github.com/AY2021S1-CS2113T-T09-2/tp/releases/tag/v2.1).
3. Copy the file to the folder you want to use as the home folder for `ra.VI`.
![Jar file in folder]()
4. Use your terminal of choice (like Command Prompt or Powershell on Windows, or Terminal on macOS) in the folder from step 3 and enter `java -jar ravi.jar`.
![Console with start jar command]()
5. ra.VI will be launched, and you will be greeted with the welcome screen! Enter the current NUS week number as prompted.
![Welcome screen]()
6. Type the command in the command box and press the Enter key to execute it.
  1. For example, typing `help` and pressing the Enter key will show you the help message, with a list of all of ra.VI’s commands.
7. Refer to the Features below for details of each command, or refer to the command summary for a quick look at all possible commands.

# Features

## Tasks

Tasks are the one of the main features of ra.VI. Every modern student has tasks to do, and ra.VI helps you to manage your to-do list. This section will show you all you need to know about managing your tasks with ra.VI.

### Adding a task
You can add a task into ra.VI to keep you on top of your tasks.

**Format:**
`add -t <task_name> [-by <deadline>]`

**Example Usage:**
Let’s say you have a task `read chapter 1`.
To add a task into ra.VI:
1. Type `add -t`, followed by your task name, `read chapter 1`.
2. The full command would be `add -t read chapter 1`.
3. Then, simply press the Enter key to execute it.

Now, let’s say you have to add a deadline `30-12-2020 1800` (i.e. 30th of December 2020, 6pm).
1. You can add this optional deadline to the task by adding `-by`, followed by the deadline for your task, but don’t forget to press enter to execute!
2. The full command would be `add -t read chapter 1 -by 30-12-2020 1800`.

**Outcome:**
ra.VI will display the message saying that your task has been added successfully! What you would expect to see is shown below.

```note
After you add your task, you may want to check if it is there. You will learn how to view your tasks using the `list -t` command later on!
```

|Example Commands|Expected Output|
|--------------|--------------|
|`add -t read chapter 1`|![Add Task]()|
|`add -t read chapter 1 -by 30-12-2020 1800`|![Add Task W Deadline]()|
|`add -t read chapter 1 -by 30-12-2020 800`|![Add Task W Wrong Deadline]()|

#### Listing all tasks
You have a whole list of tasks now, but you need a way to view them. ra.VI can help with that.

**Format:**
`list -t`

**Example Usage:**
To view your task list:
1. Type `list -t`
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display the list of tasks and their indexes.

```tip
You will need the task indexes for `del`, `edit`, and `done` commands!
```

|Example Commands|Expected Output|
|--------------|--------------|
|`list -t`|With one task in your list: ![List Task]()|

### Deleting a task
If your teacher cancels that last minute assignment, ra.VI can help remove a task from your task list.

**Format:**
`del -t <task_index>`

**Example Usage:**
Let’s say you have a task `read chapter 1` of index 1 (seen from your `list -t` command), and you would like to remove it from your list.
To delete a task from ra.VI:
1. Type `del -t`, followed by the task index of the task you want to delete., `1`. The full command would be `del -t 1`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display the message saying that your task has been deleted successfully!

```note
After you delete your task, you may want to check if it is there. You will be able to view your tasks using the `list` command earlier!
```

|Example Commands|Expected Output|
|--------------|--------------|
|`del -t 1`|![Delete Task]()|
|`del -t 0`|![Delete Task wrong index]()|

### Marking a task as done
Already completed your assignments and cleaned the dishes? You can mark your tasks as completed with ra.VI.

**Format:**
`done <task_index>`

**Example Usage:**
Let’s say you have a task `return book` of index 1 (seen from your `list -t` command), and you have completed it.
To mark a task as done:
1. Type `done`, followed by the task index of the task you want to delete, `1`. The full command would be `done 1`.
2. Then, simply press the Enter key to execute it.

|Example Commands|Expected Output|
|--------------|--------------|
|`done 1`|![Done Task]()|
|`done 0`|![Delete Task wrong index]()|

**Outcome:**
ra.VI will display the message saying that your task has been marked done! Your task will now be marked with a tick.

### Editing a task description
Put `CS2113 homework` instead of `CS2113 homework`? You can edit the task descriptions of existing tasks.

**Format:**
`edit -t <task_index> <task_description>`

**Example Usage:**
Let’s say you have a task `Team project` of index 1 (seen from your `list -t` command), and you have completed it.
To edit a task’s description:
1. Type `edit -t`, followed by the task index of the task you want to edit, `1`, and the new task description, `Individual project`. The full command would be `edit -t 1 individual project`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display the message saying that your task has been edited successfully! Your task will now be marked with a tick.

```tip
You can find the index of the tasks by using `list -t`.
```

|Example Commands|Context|Expected Output|
|--------------|----------|--------------|
|`edit -t 1 individual project`|You have a task `individual project` at index 1 in the list|![Edit Task]()|

### Viewing task summary `summary`
To view all of your tasks

**Format:**
`summary`

**Example Usage:**
To view your task summary:
1. Type `summary`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display a neat summary of all your tasks, grouped into three categories.

## Modules

Modules are the one of the main features of ra.VI. Every NUS student takes modules, and ra.VI helps you to manage all of your modules. This section will show you all you need to know about managing your modules with ra.VI.

### Adding a module
You can add a module that you are currently taking into ra.VI.

**Format:**
`add -m <module_code>`

**Example Usage:**
Let’s say you are taking the module CS1010 Programming Methodology.

To add a module into ra.VI:
1. Type `add -m`, followed by your module, `CS1010`.
2. The full command would be `add -m CS1010`.
3. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display the message saying that your module has been added successfully! What you would expect to see is shown below.

```note
After you add your module, you may want to check if it is there. You will learn how to view your modules using the `list` command later on!
```

```warning
You will only be able to add modules that are offered at NUS.
```

|Example Commands|Expected Output|
|--------------|--------------|
|`add -m CS1010`|![Add CS1010]()|
|`add -m CS2113T`|![Add CS2113T]()|
|`add -m CS`|![Add CS]()|

### Listing all modules
You have a whole list of modules now, but you need a way to view them. ra.VI can help with that.

**Format:**
`list -m`

**Example Usage:**
To view your module list:
1. Type `list -m`
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display the list of modules with their modular credits and attained grades, which we will talk about in our `grade` command later on!

```note
You will usually use this only to check the status of the modules and their respective modular credits and grades.
```

|Example Commands|Expected Output|
|--------------|--------------|
|`list -m`|With CS1010 in your list: ![List CS1010]()|

### Deleting a module
If you have accidentally added a module, you can either choose to use the `undo` command (which we will be going through later) or the `del` command.

**Format:**
`del -m <module_code>`

**Example Usage:**
Let’s say you have a module `CS1010` in your list (seen from your `list -m` command), and you would like to remove it from your list.
To delete a module from ra.VI:
1. Type `del -m`, followed by the module code of the module you want to delete, `CS1010`. The full command would be `del -m CS1010`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display the message saying that your module has been deleted successfully!

```tip
After you delete your module, you may want to check if it is there. You will be able to view your modules using the `list` command earlier!
```

|Example Commands|Context|Expected Output|
|--------------|----------|--------------|
|`del -m CS1010`|CS1010 is a module in your module list|![Delete CS1010 Success]()|
|`del -m CS2113T`|CS2113T is not in your module list|![Delete CS2113T Failure]()|

### Editing a module
Put `CS2113` instead of `CS2101`? You can edit the module code of specific modules in your module list.

**Format:**
`edit -m <module_code> <new_module_code>`

**Example Usage:**
Let’s say you have a module `CS2113` in your module list (seen from your `list -t` command).

To edit a module:
1. Type `edit -m`, followed by the module code you want to edit, `CS2113`, and the new module code, `CS2101`. The full command would be `edit -m CS2113 CS2101`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display the message saying that your module has been edited successfully!

```tip
You can check your module list by using `list -m` to check if the module has been edited.
```

|Example Commands|Context|Expected Output|
|--------------|----------|--------------|
|`edit -m CS2113 CS2101`|You have `CS2113` in your module list|![Edit Module]()|
|`edit -m CG2271 CS2101`|You do not have `CG2271` in your module list|![Edit Missing Module]()|

### Grade an existing module
Assign a grade and its relevant module credits to a module in the Scheduler.

**Format:**
 `grade <module Code> <module credit> <grade>`

**Example Usage.**
Let’s say it is the end of the semester and results are out.
You may assign the achieved grade and its relevant module credits to the module in your personalised module list by executing the `grade` command.

```note
* ra.VI will accept both _lowercase_ and _uppercase_. ie `A+` or `a+`. <br>
* Relevant module information,such as the number of module credits for the relevant module, can be found at [NUSMods](https://nusmods.com/modules) <br>
```

To assign a grade and module credits to the module:
1. Type `grade` into the command box, followed by the module code of the module to be graded.
2. Subsequently, type in the respective module credits and the grade achieved for that module.
3. The full command would be `grade CS2101 4 A+`
4. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display the message saying that your module has been successfully graded!

```warning
* Please ensure that the grade assigned is compliant to the [NUS grade schematic](http://www.nus.edu.sg/registrar/academic-information-policies/non-graduating/modular-system)  
* The module to be graded must first **exist** in the list of modules, to be assigned a grade.
```

|Example Commands|Context|Expected Output|
|--------------|----------|--------------|
|`grade CS2101 4 A+`|CS2101 has been successfully graded|![Grade CS2101 Success]()|
|`grade ACC1002 4 C+`|ACC1002 is not in your module list|![Grade ACC1002 Failure]()|

## Calculate your current CAP
Curious to know your current CAP before,during or after the semester?
You may have the flexibility of calculating your current cap anytime.

**Format:**
`cap`

**Example Usage:**
With all of the relevant modules in the module list graded, you may calculate your current CAP by executing the `grade` command.

```note
Please ensure the relevant modules in the module list have been graded, for ra.VI to calculate the CAP accurately.
However, **not** **all** **modules** need to be graded for CAP to be calculated.
```

To calculate your current cap:
1. Simply type in the command `cap`
2. The full command would be `cap`.
3. Then simply press the Enter key to execute it.

**Outcome:**
ra.VI will display the current calculated CAP to you.

|Example Commands|Context|Expected Output|
|--------------|----------|--------------|
|`cap`|CAP calculated successfully|![CAP calculated Success]()|


## Undo
Deleted a task when you didn’t mean to? You can undo your previous action.

**Format:**
`undo`

**Example Usage:**
Let’s say you have accidentally deleted an important task.
To undo an action:
1. Type `undo`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display the message saying that your last action has been undone!

## Timetable
Every NUS student has lessons to take, whether they are lectures, labs or tutorials, just to name a few. These lessons are usually at regular intervals throughout the semester. ra.VI will help you arrange your lessons into a timetable, allowing you to view all of your lessons in one place.

### Adding a lesson
Every student has lessons. Too many lessons, even. Let ra.VI help you keep track of them all with this command.

**Format:**
`timetable -add <module_code> <day> <start_time> <end_time> <lesson_type> <repeat>`

```tip
These fields
* <module_code>: Module code must be added to the module list. See your module list with `list -m`.
* <day>: Please refer to [keywords]().
* <start_time>: Must be in 24h format, e.g. 1100.
* <end_time>: Must be in 24h format, e.g. 1300, and be after <start time>.
* <lesson_type>: Please refer to [keywords]().
* <repeat>: Please refer to [keywords]().
```

**Example Usage:**
Let’s say you have a LECTURE for CS2101 at 8AM to 10AM, every TUESDAY, and you would like to add it to your timetable.
To add a lesson to your timetable:
1. Type `timetable -add`, followed by the lesson’s details, `CS2101 TUESDAY 0800 1000 LECTURE 2`. For example, `timetable -add CS2101 TUESDAY 0800 1000 LECTURE 2`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display a message saying that your lesson has been added!

|Example Commands|Context|Expected Output|
|--------------|----------|--------------|
|`timetable -add CS2101 TUESDAY 0800 1000 LECTURE 2`|CS2101 is a module in your module list|![Timetable add CS2101 Success]()|
|`timetable -add CS1010 WEDNESDAY 1200 1400 LECTURE 2`|CS1010 is not in your module list|![Timetable add CS1010 Failure]()|
|`timetable -add CS2113T TUESDAY 0800 1000 LECTURE 2`|Overlapping lesson times|![Timetable add Overlap Failure]()|
|`timetable -add CS1010 THURSDAY LECTURE 2`|Missing parameters|![Timetable add Missing Parameters Failure]()|

### Viewing your timetable
Now that you have your lessons in your timetable, you can view them too!

**Format:**
`timetable -day` or `timetable -week`

**Example Usage:**
To view your day’s timetable:
1. Type `timetable -day`.
2. Then, simply press the Enter key to execute it.

To view the current week’s timetable:
1. Type `timetable -week`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display your timetable, containing the lessons and their indexes, for the day or week!

|Example Commands|Context|Expected Output|
|--------------|----------|--------------|
|`timetable -day`|View day’s timetable|![Timetable view day]()|
|`timetable -week`|View week’s timetable|![Timetable view week]()|

### Deleting a lesson

Made a mistake adding the wrong entry to your timetable? Delete the entry by executing the `timetable -del` command.

**Format:**
`timetable -del <day> <lesson_index>`

**Example Usage:**
Let’s say that you have a lesson on TUESDAY, with the index of `1`.
To remove a lesson from your timetable:
1. Type `timetable -del`, followed by the lesson’s details, `TUESDAY 1`. The whole command would be `timetable -del TUESDAY 1`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display a message saying that your lesson has been deleted.

```tip
You will need the lesson indexes for `timetable -del`! Use `timetable -day` or `timetable -week` to see the lesson’s index.
```

|Example Commands|Context|Expected Output|
|--------------|----------|--------------|
|`timetable -del MONDAY 1`|Lesson on Monday with an index of 1|![Timetable Del Success]()|
|`timetable -del FRIDAY 3`|No lessons on Friday with an index of 3|![Timetable Del Failure]()|

### Filtering lessons in your timetable

Let’s say that you have a cluttered timetable and would only like to view your `CG2271` lessons. You would use the `timetable -filter` command.

**Format:**
`timetable -filter <module> <day> <start time> <end time> <lesson type>`

**Example Usage:**
Let’s say that you want to see all your CG2271 lectures this week on Monday between 10AM and 1PM. To filter out these lessons from your timetable:
1. Type `timetable -filter`, followed by the lesson’s details, `CG2271 MONDAY 1000 1300 LECTURE`. The whole command would be `timetable -filter CG2271 MONDAY 1000 1300 LECTURE`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display a message saying that your lesson has been deleted.

```tip
If you want to skip using certain criteria, you can use a dash (`-`) in the place of that field! For example, if you only want to filter all lessons on Monday, you could do `timetable -filter - MONDAY - - -`, only filling in the `<day>` field and using `-` to ignore the other fields. **Any combination of fields is possible!**
```

|Example Commands|Context|Expected Output|
|--------------|----------|--------------|
|`timetable -del MONDAY 1`|Lesson on Monday with an index of 1|![Timetable Del Success]()|
|`timetable -del FRIDAY 3`|No lessons on Friday with an index of 3|![Timetable Del Failure]()|

### Resetting your timetable
As you move to the next semester, you can continue to use ra.VI. In fact, we would appreciate it if you could use ra.VI all the way until your graduation!

**Format:**
`timetable -reset`

**Example Usage:**
Let’s say that it is the start of a new semester and you would like to start with a new timetable.

To reset your timetable:
1. Type `timetable -reset`
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI will display a message saying that your timetable has been reset.

```warning
Once you reset your timetable and exit ra.VI, there is no going back! You can only undo your timetable reset before you exit ra.VI, so do make sure that you truly want to reset your timetable and that you will not lose any valuable information.
```

|Example Commands|Expected Output|
|--------------|--------------|
|`timetable -reset`|![Reset the timetable]()|

## Exit
Done using ra.VI? You can save your data and safely exit ra.VI.

**Format:**
`bye`

**Example Usage:**
To exit ra.VI:
1. Type `bye`.
2. Then, simply press the Enter key to execute it.

**Outcome:**
ra.VI saves all data and exits.

|Example Commands|Expected Output|
|--------------|--------------|
|`bye`|![bye success]()|

# FAQ

**Q**: Can I use ra.VI on operating system other than Windows?\
**A**: Yes. ra.VI is compatible with Windows, macOS and Linux.

**Q**: Can I use ra.VI throughout my time in NUS?\
**A**: Yes! In fact, we strongly encourage using ra.VI for your time at NUS. ra.VI is robust enough to handle the trials of time.

**Q**: How do I transfer my data to another computer?\
**A**: Zip the folder where you have installed ra.VI on and transfer the zip file to the other computer. Unzip the folder on the new computer, and you are good to go!

**Q**: Can I edit the files created by ra.VI?\
**A**: It is not advised to edit the files created by ra.VI with any other software.

**Q**: Can I force close ra.VI?\
**A**: It is not advised to force close ra.VI. If you decide to do so, the changes made during that current session may get corrupted. To close ra.VI, please enter `bye`.

---

# Command Summary

| Function | Command |
|--------|---------------------------------------|
| Add a task | `add -t <task_name> [-by <deadline>]`|
| Delete a task | `del -t <task_index>` |
| Edit a task | `edit -t <task_index> <task_name> [-by <deadline>]` |
| Mark task as done | `done <task_index>` |
| List all tasks | `list -t` |
| View task summary | `summary` |
| Add a module | `add -m <module_code>` |
| Delete a module | `del -m <module_code>` |
| Edit a module | `edit -m <module_code> <new_module_code>` |
| List all modules | `list -m` |
| Grade and allocated MCs to a module | `grade <module_code> <grade>` |
| Calculate cap | `cap` |
| Add lesson to timetable | `timetable -add <module_code> <day> <start_time> <end_time> <lesson_type> <repeat>` |
| Delete lesson from timetable | `timetable -del <day> <lesson_index>` |   
| View day's timetable | `timetable -day` |
| View week's timetable | `timetable -week` |
| Filter timetable | `timetable -filter <module> <day> <start time> <end time> <lesson type>` |
| Reset timetable | `timetable -reset` |
| Undo previous action | `undo` |
| Get list of commands | `help` |
| Get detailed help message for each command | `help <command_word>` |
| Exit ra.VI | `bye` |

---

# v3.0 Graphical User Interface

## Change Directory Command `cd`
Traverse to the target directory.

**Note:** <br>
All the modules and tasks are treated as directories, like the folders in the Window OS.
To create a task related to Module CS2101, the user need to go into the Directory CS2101, to create the task.
Format: `cd <module code>` <br>
        `cd ..` <br>

Example of usage: <br>
* `cd CS2101` <br>
* `cd ..` <br>

Example of output:
* `CS2101` <br>
* `Root` <br>

## 6.2 General Add `add`
The generic way to add a module or a task to the system.

**Note:** <br>
There are two types of add commands in the system: add a module and add a task.
The general add command combines and simplifies the above two command.
The ra.VI system could parse the general add command to different add commands according to the user current directory level.
Format: `add <module code or task description>` <br>
Example of usage: <br>
* `add CS2101` <br>
* `add read a book` <br>

Example of output:
* Module has been added <br>
* Task has been added <br>

## 6.3 Undo `undo`
Recover the data from the previous "Data-changed" operations.

**Note:** <br>
"Data-changed" operations refer to Add, Edit, Delete operations only.

Example of usage:
1. `add -m CS2113T`
2. `undo`

Example of output:
* Undo Successfully <br>

## 6.4 Week Command  `week`
A window will pop out and the task number on the each day of the upcoming week will be listed.

Example of usage:
* `week`

## 6.5 Directory Command  `dir`
A window will pop out and all module with related tasks will be listed.

Example of usage:
* `dir`
