# ra.VI User Guide

Welcome to the ra.VI User Guide! Choose a section from the table of contents on the left, or simply start reading from the introduction. This User Guide will give you step-by-step instructions to start your journey in planning out your NUS life.

## Introduction

Repository Assistant with a Versatile Interface (ra.VI) is a desktop app for managing tasks, deadlines, and timetable, optimized for use via a Command Line Interface (CLI). If you can type fast, ra.VI can manage your tasks and timetable faster than traditional GUI apps.

This user guide aims to provide you with a clear documentation of ra.VI's features. In addition, the quick start guide provides an end-to-end setup process to begin tracking your tasks and timetable with ra.VI.

### Product Overview

ra.VI is targeted at you - the NUS freshman. As a freshman, there are many documents and new procedures that you must get familiar with. This may be daunting for you but ra.VI will provide you with the assistance you need.
By helping you keep track of your tasks and deadlines, you will be able to keep on top of deadlines.
Moreover, the timetable feature helps you to schedule your lessons, allowing you to be more prepared for lessons.
Adding on, ra.VI also allows you to keep track of your CAP, so that you can keep tabs on how well you are doing, motivating you towards that elusive CAP 5.0.

### Keywords

**Tasks**

A task refers to something that you would like to get done. This refers to reading a book or doing an assignment. Tasks can be created with or without a deadline. <br>

**Deadline**

A deadline refers to a date and time associated with a task. This is in the format: DAY-MONTH-YEAR TIME_24H, e.g. `23-12-2020 1400` or `1-2-2000 0800` <br>

**Modules**

A module refers to a module taken under NUS. Entered modules will be checked against the list of NUS modules. <br>

**CAP**

CAP refers to Cumulative Average Point, which is the grading system used by NUS. CAP will be calculated based on your modules. <br>

**Done**

A task can be marked as done. This will signify completion of the task so that you can get an easy view of any remaining tasks. <br>

**Timetable**

The timetable is specific to you. It allows you to add lessons to your timetable with respect to the modules that you are taking. After setting the timetable up the first time, you do not need to go through the set up again. <br>

**Day**

Values for `<day>`:\
`MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY`, `SUNDAY`

**Lesson Type**

Values for `<lesson type>`:\
`TUTORIAL`, `LECTURE`, `SEMINAR`, `LAB`, `RECITATION`, `SESSION`

**Time**

Format of `<time>`:\
Must be in the 24h format e.g. `0900`, `1415`

**Undo**

Commands that can be undone:
* Add / Delete tasks
* Done tasks
* Add / Delete modules
* Add / Delete lessons to / from the timetable
* Reset the timetable
* Edit tasks / modules
* Grade a module

## Quick Start

1. Ensure that you have Java 11 or above installed.
2. Download the latest version of `ra.VI` from [here](https://github.com/AY2021S1-CS2113T-T09-2/tp/releases/tag/v2.1).
3. Copy the file to the folder you want to use as the home folder for `ra.VI`.
4. Open a command prompt in the folder from step 3 and enter `java -jar ravi.jar`.
5. Enter the current NUS week number as prompted.
5. Type the command in the command box and press Enter to execute it. e.g. typing help and pressing Enter will show the help message.
Some example commands you can try:
* `add -t`: Add a task
* `list -t`: List all tasks
* `bye`: Exit the program
6. Refer to the Features below for details of each command, or refer to the command summary for a quick look at all possible commands.

## Features

### Tasks

Tasks are the one of the main features of ra.VI. Every modern student has tasks to do, and ra.VI helps you to manage your to-do list. This section will show you all you need to know about managing your tasks with ra.VI.

#### Adding a task: `add -t [-by]`

**Format:**
`add -t <task_name> [-by <deadline>]`

**Example Usage:**
Let’s say you have a task `read chapter 1`.
To add a task into ra.VI:
1. Type `add -t`, followed by your task name, `read chapter 1`. The full command would be `add -t read chapter 1`.
2. Then, simply press Enter to execute it.
3. You may also add an optional deadline to the task by adding `-by`, followed by the deadline for your task, but don’t forget to also press enter to execute!
	1. For example, if you wanted to give your task `read chapter 1` a deadline `30-12-2020 1800` (i.e. 30th of December 2020, 6pm), the full command would be `add -t read chapter 1 -by 30-12-2020 1800`.

**Outcome:**
ra.VI will display the message saying that your task has been added successfully!

```note
After you add your task, you may want to check if it’s there. You will learn how to view your tasks using the `list` command later on!
```

|Example Commands|Expected Output|
|--------------|--------------|
|`add -t read chapter 1`|![Add Task](https://github.com/AY2021S1-CS2113T-T09-2/tp/blob/master/docs/diagrams/MainSequenceDiagramLoopSd.png?raw=true)|
|`add -t read chapter 1 -by 30-12-2020 1800`|![Add Task W Deadline](https://github.com/AY2021S1-CS2113T-T09-2/tp/blob/master/docs/diagrams/MainSequenceDiagramLoopSd.png?raw=true)|


#### Deleting a task: `del -t`
You can remove a task from ra.VI by using the following format.\
Format: `del -t <task_index>`

#### Editing a task description: `edit -t <task_index> <task_description>`

#### Listing all tasks `list -t`

#### Viewing task summary `summary`


### Modules

### Undo

### Summary

### Timetable

### Exit

## FAQ

:question:**Q**: Can I use ra.VI on operating system other than Windows?\
:a:**A**: Yes. ra.VI is compatible with Windows, macOS and Linux.

:question:**Q**: Can I use ra.VI throughout my time in NUS?\
:a:**A**: Yes! In fact, we strongly encourage using ra.VI for your time at NUS. ra.VI is robust enough to handle the trials of time.

:question:**Q**: How do I transfer my data to another computer?\
:a:**A**: Zip the folder where you have installed ra.VI on and transfer the zip file to the other computer. Unzip the folder on the new computer, and you are good to go!

:question:**Q**: Can I edit the files created by ra.VI?\
:a:**A**: It is not advised to edit the files created by ra.VI with any other software.

:question:**Q**: Can I force close ra.VI?\
:a:**A**: It is not advised to force close ra.VI. If you decide to do so, the changes made during that current session may get corrupted. To close ra.VI, please enter `bye`.

---

## Command Summary

| Function | Command |
|--------|---------------------------------------|
| Add a task | `add -t <task_name> [-by <deadline>]`|
| Add a module | `add -m <module_code>` |
| Delete a task | `del -t <task_index>` |
| Delete a module | `del -m <module_code>` |
| Edit a task | `edit -t <task_index> <task_name>` |
| Edit a module | `edit -m <module_code> <new_module_code>` |
| Mark task as Done | `done <task_index>` |
| Grade and allocated MCs to a module | `grade <module_code> <grade>` |
| Calculate cap | `cap <total mc taken> <current cap>` |
| Undo previous action | `undo` |
| Add lesson to timetable | `timetable -add <module> <day> <start time> <end time> <lesson type> <repeat>` |
| Delete lesson from timetable | `timetable -del <day> <lesson index>` |   
| List all tasks | `list -t` |
| List all modules | `list -m` |
| View task summary | `summary` |
| View day's timetable | `timetable -day` |
| View week's timetable | `timetable -week` |
| Filter timetable | `timetable -filter <module> <day> <start time> <end time> <lesson type>` |
| Reset timetable | `timetable -reset` |
| Get list of commands | `help` |
| Get detailed help message for each command | `help <command_word>` |
| Exit ra.VI | `bye` |

---

## v3.0 Graphical User Interface

### Change Directory Command `cd`
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

### 6.2 General Add `add`
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

### 6.3 Undo `undo`
Recover the data from the previous "Data-changed" operations.

**Note:** <br>
"Data-changed" operations refer to Add, Edit, Delete operations only.

Example of usage:
1. `add -m CS2113T`
2. `undo`

Example of output:
* Undo Successfully <br>

### 6.4 Week Command  `week`
A window will pop out and the task number on the each day of the upcoming week will be listed.

Example of usage:
* `week`

### 6.5 Directory Command  `dir`
A window will pop out and all module with related tasks will be listed.

Example of usage:
* `dir`
