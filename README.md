 YOUTUBE VIDEO PRESENTATION
 https://.yout.be/h7Qx_X4Tcl8

  System Description
This system is an Event Management and Enrolment Platform. It allows students/athletes to browse events, enrol for events based on categories, and view their results. The backend is built with ASP.NET Core Web API and SQL Server (.SQLEXPRESS), with a planned front-end and API for Part 2.

 User Roles (2 Roles)

Role 1: Student / Athlete
- Can register and login.
- Can view all events and categories.
- Can enrol themselves for an event (if space available).
- Can view their own enrolments and cancel enrolment.
- Can view their own results and event leaderboards.
- **Cannot** create, edit or delete events.

Role 2: Admin / Organizer
- Has all Student permissions.
- Can create, update and delete Events.
- Can create and manage Categories.
- Can view all users and all enrolments for any event.
- Can capture, update and publish Results for enrolled students.
- Responsible for managing the system.

 CI/CD Screenshot
![CI/CD Green Build](docs/green-build.png)
*The build passes in GitHub Actions showing successful build and tests.*

 YouTube Video Link
https://youtu.be/YOUR_LINK_HERE
Video demonstrates database setup, executing SQL script, and shows "Commands completed successfully" in SSMS.
