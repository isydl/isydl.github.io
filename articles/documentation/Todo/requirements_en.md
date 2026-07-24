- 参考 [中文版](/articles/documentation/Todo/requirements_cn.md)

# Todo App - Requirements Document

## 1. Overview

Todo is a personal task management tool that enables users to plan, track, and organize daily tasks efficiently. Users can create custom lists (e.g., Work, Study, Personal) to categorize tasks by context, and use the "My Day" feature to focus on what matters most each day.

## 2. User Roles

- Single user: the individual using the application on their device.

## 3. Functional Requirements

### 3.1 List Management

#### 3.1.1 Create a List

- Users can create multiple task lists (e.g., Work, Study, Life) to organize tasks by context.
- A default list named "Tasks" is provided by the system and cannot be deleted.

#### 3.1.2 Edit or Delete a List

- Users can rename an existing list.
- Users can delete a list. When a list is deleted, all tasks within it are also removed (requires confirmation).

### 3.2 Task Management

#### 3.2.1 Create a Task

- Users can create a task by clicking the "Add" button on a list page and entering a title.
- Each task contains the following fields: ID (auto-incremented), title, associated list, creation timestamp, due date (optional), reminder time (optional), note (optional), priority level (optional), and completion status.

#### 3.2.2 View the Task List

- All tasks within a list are displayed on the list page.
- Tasks are sorted in reverse chronological order by creation time (newest first).
- Completed tasks are visually distinguished with a strikethrough.

#### 3.2.3 Edit a Task

- Users can click on a task to navigate to the edit page, where they can update its title, due date, reminder time, note, priority, and other fields.

#### 3.2.4 Delete a Task

- Users can delete any task. This action is permanent and cannot be reversed.

#### 3.2.5 Mark as Complete / Incomplete

- Users can toggle a task's completion status by clicking the checkbox next to it.
- Completed tasks can be reverted to incomplete at any time.

### 3.3 My Day

#### 3.3.1 Daily Focus View

- "My Day" is a smart list designed to help users focus on their most important tasks for the current day.
- The current date is displayed at the top of the page.

#### 3.3.2 Add a Task to My Day

- Users can add a task from any list to My Day.
- Users can also create a new task directly within My Day; such tasks will also appear in the default task list.

#### 3.3.3 Smart Suggestions

- Clicking the suggestion icon triggers the system to automatically recommend: overdue tasks, tasks due today, and incomplete tasks from yesterday.
- Users can add all suggested tasks to My Day with a single click.

#### 3.3.4 Remove a Task from My Day

- Completed tasks are automatically removed from My Day.
- Users can also manually remove tasks from My Day. This action does not affect the original task in its list.

### 3.4 Subtasks (Steps)

- Users can break down complex tasks into smaller, more manageable steps by adding subtasks.
- Subtasks can be independently toggled between complete and incomplete.

### 3.5 Reminders and Due Dates

- **Due date**: Users can set a deadline for a task.
- **Reminder**: Users can set a reminder time for a task.
- **Recurring tasks**: Users can configure tasks to repeat automatically on a daily, weekly, or monthly basis.

### 3.6 Notes

- Users can attach notes to tasks for additional context or reference.

### 3.7 Priority and Tags

- **Priority**: Users can star important tasks to distinguish them from others.
- **Tags**: Users can add hashtags (e.g., `#work`) to tasks for easier searching and grouping.

### 3.8 Filter and Search

- Users can filter the task list by All, Active, or Completed status.
- Users can search for tasks by title using keywords.

### 3.9 Statistics

- The system displays total, completed, and active task counts.
- The number of active tasks in My Day is also shown.

## 4. Non-Functional Requirements

- **Data persistence**: All task data is stored in the browser's localStorage and persists across page reloads.
- **Responsive design**: The interface adapts to both desktop and mobile screen sizes.
- **Offline support**: The application works without an internet connection.
- **Zero dependencies**: Built with vanilla HTML, CSS, and JavaScript.

---

# Todo App - Requirements Documentation

## 1. Overview

Todo is a ~~persional~~ personal ~~todo list~~ task management tool ~~which can help user design, trace and manage task effictive.~~ that ~~helps~~ enables users to plan, track, and ~~manage~~ organize daily tasks efficiently. Users can ~~categorize and organize task by creating different task list~~ create custom lists (e.g., Work, Study, Personal) to categorize tasks by context, and ~~focus on the most important item by My Day feature~~ use the "My Day" feature to focus on what matters most each day.

## 2. Roles

- ~~Only one role: The person who used this device.~~ Single user: the individual using the application on their device.

## 3. Functional Requirements

### 3.1 ~~list management~~ List Management

#### 3.1.1 ~~create list~~ Create a List

- ~~user~~ Users can create ~~different type of lists such as work, study, life etc~~ multiple task lists (e.g., Work, Study, Life) to ~~categorize and organize different senece tasks~~ organize tasks by context.
- ~~system~~ A default list named "~~'Task'~~ Tasks" is ~~create~~ provided by the system and ~~can't~~ cannot be deleted.

#### ~~3.2.2~~ 3.1.2 ~~modify and delete list~~ Edit or Delete a List

- ~~user~~ Users can rename ~~list~~ an existing list.
- ~~user~~ Users can delete ~~list~~ a list. When a list is deleted, ~~all subtask in this could be deleted together(need double comfirm)~~ all tasks within it are also removed (requires confirmation).

### 3.2 ~~task management~~ Task Management

#### 3.2.1 ~~create task~~ Create a Task

- ~~User~~ Users can create ~~task~~ a task by clicking the ~~'Add'~~ "Add" button ~~at~~ on ~~the~~ a list page and ~~then typing~~ entering ~~the~~ a task ~~name~~ title.
- Each task ~~includes: id (auto increment), title, list, create time, due date, reminder time, remark, priority level, complete satatus.~~ contains the following fields: ID (auto-incremented), title, associated list, creation timestamp, due date (optional), reminder time (optional), note (optional), priority level (optional), and completion status.

#### 3.2.2 ~~view task list~~ View the Task List

- ~~show~~ All tasks ~~blew list~~ within a list are displayed on the list page.
- ~~task~~ Tasks are ~~sorted by create time lastly~~ sorted in reverse chronological order by creation time (newest first).
- ~~show crossed out style on completed task.~~ Completed tasks are visually distinguished with a strikethrough.

#### 3.2.3 ~~modify task~~ Edit a Task

- ~~Click task forward to modify page which can modify name, due date,reminder time,remark,priority level and more information.~~ Users can click on a task to navigate to the edit page, where they can update its title, due date, reminder time, note, priority, and other fields.

#### 3.2.4 ~~delete task~~ Delete a Task

- ~~each~~ Users can delete ~~task~~ any task. ~~but can't reback.~~ This action is permanent and cannot be reversed.

#### 3.2.5 ~~mark as complete or active status~~ Mark as Complete / Incomplete

- ~~click~~ Users can toggle a task's completion status by clicking the checkbox ~~on the front~~ next to it.
- ~~you can set task to it's origin status at any time for any completed task.~~ Completed tasks can be reverted to incomplete at any time.

### 3.3 My Day

#### 3.3.1 ~~Daily focus~~ Daily Focus View

- ~~My day~~ "My Day" is a smart list ~~to help people focus on the most important task in a day~~ designed to help users focus on their most important tasks for the current day.
- ~~show~~ The current date is displayed at the top of the page.

#### 3.3.2 Add task to My Day

- ~~User~~ Users can ~~choose one task record in task list to My Day~~ add a task from any list to My Day.
- ~~User also can create a new task at My Day while this record appear in defult task list.~~ Users can also create a new task directly within My Day; such tasks will also appear in the default task list.

#### 3.3.3 ~~recommended features~~ Smart Suggestions

- ~~click the suggestion button, system will auto push: incompleted task without time, today's end tasks,yesterday imcomplete task.~~ Clicking the suggestion icon triggers the system to automatically recommend: overdue tasks, tasks due today, and incomplete tasks from yesterday.
- ~~User can add all the suggestion tasks into My Day by one click.~~ Users can add all suggested tasks to My Day with a single click.

#### 3.3.4 ~~remove task from My Day~~ Remove a Task from My Day

- ~~auto remove completed task from My Day~~ Completed tasks are automatically removed from My Day.
- ~~User can remove task from My Day manualy(this doesn't affect the origin task in task list.)~~ Users can also manually remove tasks from My Day. This action does not affect the original task in its list.

### 3.4 ~~subtasks (step)~~ Subtasks (Steps)

- ~~user~~ Users can ~~add subtasks to break down complex task into smaller steps.~~ break down complex tasks into smaller, more manageable steps by adding subtasks.
- ~~subtasks support independent completed or active operation.~~ Subtasks can be independently toggled between complete and incomplete.

### 3.5 ~~reminder and due date~~ Reminders and Due Dates

- ~~due date: user can set due date for task.~~ **Due date**: Users can set a deadline for a task.
- ~~reminder time: user can set reminder time for task.~~ **Reminder**: Users can set a reminder time for a task.
- ~~recurring task: user can set auto repeat by day, week, month.~~ **Recurring tasks**: Users can configure tasks to repeat automatically on a daily, weekly, or monthly basis.

### 3.6 ~~notes~~ Notes

- ~~user can add notes for task to record additional information.~~ Users can attach notes to tasks for additional context or reference.

### 3.7 ~~priority level and tag~~ Priority and Tags

- ~~priority: user can mark task as star to distinguish priorities.~~ **Priority**: Users can star important tasks to distinguish them from others.
- ~~user can use #tag to add tags for tasks, in order to eazy to search and group.~~ **Tags**: Users can add hashtags (e.g., `#work`) to tasks for easier searching and grouping.

### 3.8 ~~filter and search~~ Filter and Search

- ~~user can filter task list by all,active,completed status.~~ Users can filter the task list by All, Active, or Completed status.
- ~~user can search task title by keywords.~~ Users can search for tasks by title using keywords.

### 3.9 ~~statistics~~ Statistics

- ~~view total, completed, and active task counts.~~ The system displays total, completed, and active task counts.
- ~~view the active count in My Day~~ The number of active tasks in My Day is also shown.

## 4. ~~non-functional requirements~~ Non-Functional Requirements

- ~~data save: storage data in localstorage and persists after page refresh.~~ **Data persistence**: All task data is stored in the browser's localStorage and persists across page reloads.
- ~~responsive design: adapts to both desktop and mobile screens.~~ **Responsive design**: The interface adapts to both desktop and mobile screen sizes.
- ~~available offline: no network connceted required.~~ **Offline support**: The application works without an internet connection.
- ~~0-dependence: pure native html + css + Javascripte.~~ **Zero dependencies**: Built with vanilla HTML, CSS, and JavaScript.
