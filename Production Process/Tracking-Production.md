# Individual Production

Keeping track of one's production as a developer can be challenging.
There are several phases of the production process as well as multiple duties required of a developer.
It would be logical to assume that all that is required of a software developer is to solve the problems then write the code.
Unfortunately, there is a bit more required. The individual developer also plays a major part in maintaining the
coherency of any given project. That means keeping track of what needs to be done along with what has already been done.
And don't forget, no developer knows everything. There is also research time that must be accounted for.
Add to that production deadlines and you can see there is quite a bit of administration that goes along with development.

Any company engaged in software development has procedures and protocols for overcoming the challenges of
tracking production. The material presented here are the practices and procedures developed for K and R Software.
Other companies handle these issues a little differently.
Even so, you will find they are similar to other industry organizations.

## The Ticket System

Software projects are broken down into individual tasks. These tasks are then assigned to individual developers
to be completed. The means by which this is done is by the use of tickets. Tickets are very much like workorders.
They give the assignee information about what needs to be done, how long it should take, and a point value awarded
upon its completion. Here at K and R Software we use an application for this purpose called Redmine.

### Ticket Procedure

1. Log into Redmine
2. Navigate to the assigned project
3. Look through the tickets listed for the project.
4. Select the ticket you wish to take on (incomplete).

## Time

Time is a primary measure of production for most jobs. An employee punches a time clock and is then paid for the
time he is actually there. This has only limited workability in a development environment. This industry is largely
based on completing applications for clients.
The longer the application is not working in the hands of the client, the greater the costs to the company.
Time is certainly a factor, but getting the work done with excellent quality and reasonable speed is very much
senior to time spent in the development process.

It is understood that there are always unforseen circumstances that arise in the course of the development process.
A task that is estimated to take 2 hours can end up taking 4 hours or more. Usually, this is because there was
some other bug not known at the time the ticket was written.
When such situations arise it is perfectly acceptable to simply let someone know. Tickets are not carved in stone.
They can be changed based on changing circumstances.
A short conversation can usually handle any time related discrepancies.

## Points

Some tickets require a lot of time and effort. Some tickets are easy to complete. The completion of *all* tickets is
essential to the timely completion of the project. It can happen that one dev worked all week on a single ticket
because that's what it took to get the job done. In the same week, another dev completed 20 tickets, all of
which were relatively simple tasks. This creates an unreal picture of individual production. It is true that every
task listed in a ticket is required to be completed. But it is also true that not all tickets are created equally.
In order to account for this, tickets are given a point value. Tickets that have high estimates for time will also carry
a higher point value. The time estimate is based on the difficulty of the task. The point value rises in
direct proportion to the time estimate.

## Administration

Administration is the process of directing actions, recording actions, and analyzing what actions have been done and
what actions have not been done. The purpose of administration is to assist production personnel in the completion
of products. Ideally, there would exist a sharp demarcation between production personnel and administrative
personnel. Production people would focus only on the actual production tasks required to complete the project. Adminstrative
personnel would focus on the reports and other records required to keep track of production and the lines of communication
both inside and outside of the organization.

Just to keep it simple, the two sheres of activity would break down like this: Dev's solve the problems regarding the
project, and then write the code. Administrative personnel record what has
been done, schedule when things are going to happen, financial matters, employee issues, communication both
internally and externally, etc. As stated above, this is the *ideal* situation. Unfortunately, the real world
rarely presents us with ideal situations.

Developer's, in addition to their duties as developers, are also required to engage in some amount of administration.
This is required in order to keep track of the progress of a project. When several developers are engaged on a
single project, coordination of their individual activities is essential. Otherwise, chaos ensues and nobody knows what
anyone else is doing or why. To stave off this confusion, proper administration is important. But what does that
mean, exactly? What specific adminstrative tasks are required? Let's go over a few of them.

A lot of the administration required of the developer involves recording what has been done and when it was done. (Incomplete)

## The Production Cycle

In an effort to make clear what exactly is expected of a developer in the course of any given day, a cycle
of production has been created. This is merely a guide, as it is understood that circumstances
evolve and change. Still, it is helpful to know what one is supposed to be doing when asked
to get something done. Here is the cycle:

* Fire up your machine.
* Log into the project management system.

    * The system we use at K and R Software is called Redmine

* Start your timer

    * The time recorded at this point is considered Admin time. This is separate from
    Development time. It is helpful to have a recording of both.

* Determine your next task.

    * Tasks are prioritized by calendar date.
    * Select your next task with the above in mind.
    * Also, select a task that you feel you can get done in the course of your day.
    * If you find that there are several tasks that are all needed by a certain date, pick
    the ones you can get done the fastest.
    * If in doubt, pick the task you have good certainty you can do.
    * You are not on your own. You have a team there. So, determining your task will also be modified
    by the agreements made at your daily meeting.

* Open a terminal on your machine

    * Navigate to your project folder.
    * Clone the repository, if needed.
    * Pull in any changes from the repository to ensure everything is up to date.

* Create a new feature branch.

    * Feature branches are created off of a Development branch, not the Master branch.

* Stop your timer

    * This concludes your administrative time.
    * You are now ready to start writing your code.

* Start You Development Timer.
* Write out your requirements.

    * The task description is a brief statement of what is needed to be done.
    * It is necessary to now write out the specific requirements of what needs to be done to fulfill the task description.

* Begin writing your tests for the requirements

    * Your tests should all fail initially because you haven't written any code yet.
    * You then write the code that satisfies the requirements of your tests. They should now all pass.
    If not, make whatever changes are needed and test again.
    * When your code works (All test are passed), go back and refactor the code to make it readable.
    * Then run the code through your linters. These ensure your code is written per the standards of the language in use.

* Commit your changes.
* Create a Pull Request

    * If your PR is accepted, your are done.
    * Stop your timer.
    * If your PR is rejected, fix it and resubmit.
    * Only after your PR has been accepted would you then stop your timer for that task.

* Begin the cycle again at step #1.

That is a brief description of the cycle of production. There absolutley will be exceptions to the above steps.
Things change all the time. However, the above description serves a reference point for you to help guide your day.
