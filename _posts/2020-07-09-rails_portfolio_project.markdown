---
layout: post
title:      "Rails Portfolio Project"
date:       2020-07-09 14:33:00 +0000
permalink:  rails_portfolio_project
---



**Overview**

My Rails portfolio project is a Classroom Manager app. The user group is teachers.

Who is your User?
Teachers of high school students

What is their pain point?
Teachers need a clear place to manage all schedules, students, assignments, and submissions.

How do they use our solution to overcome this problem?
This app gives teachers a view into all of their classes, students, and assignments. It also calculates students grade averages and their availability for classes.

**Challenges**

Join tables!

Deciding what was a join table and what was not, was tricky. By the end of the project I got the hang of it. I think one of the funky things about join tables is they dont always clearly mimic a real world object the way that traditional models do. For example, I have a `Teacher` `Subject` and `Student` model. These are pretty straightforward. 

However, a student has many classes throughout the day, and teachers need to know information about the student that is relavent to that subject. For exmaple, a student has an overall GPA, but they also have a grade average for just that subject. The join table is `SubjectStudent`, which `belongs to :subject` and `belongs_to :student`. There's a bit of abstraction here which can be hard to wrap your head around at first.

**Scopes**

Towards the end of my project, I did some refactoring to clean it up. One thing I did was turn methods into scopes.

Scopes are custom queries that you define inside your Rails models with the scope method. 

For example, `Assignment` has these scopes:

```
scope :current, -> { where('due_date >= ?', Date.today)}
scope :past_due, -> { where('due_date < ?', Date.today)}
scope :due_today, -> { where('due_date = ?', DateTime.current.beginning_of_day)}
```

These were previously methods which ultimeatly gave the same result, but in a more verbose way. IN this case, i previosuly had these methods related to assignment due dates on `Subject` and I would query the assignment association. It worked, but it seemed off, so after some Googling, I realized scopes were what I wanted. Scopes result in much cleaner code because of their syntax.


All in all this was a great experience. I streched my limits beyond just simple CRUD and implemented logic around availbility for teachers and students, and calculating grade averages. [View the full project here!](https://github.com/sheilacodonnell/education-manager-app)



