# PROG6212-P1
## CI/CD Build Status
Successful green build implemented with GitHub Actions:

![Green Build](green-build.png)

DESCRIPTION OF THE TWO ROLES
 Contract Monthly Claim System (CMCS) - PROG6212 Part 1

 Brief Description of the System
The Contract Monthly Claim System (CMCS) is a WPF application built in C# that digitizes the monthly claim process for Independent Contractor lecturers. The system allows lecturers to submit claims for hours worked, upload supporting documents, and track their claim status, while Programme Coordinators can review and manage those claims. This replaces the manual, paper-based process with a more efficient and transparent solution.

User Roles
The system has two main user roles:

1. Lecturer (Independent Contractor)**
- Submits monthly claims by entering hours worked and hourly rate.
- Uploads supporting documents (e.g., timesheets).
- Views the status of submitted claims: Pending, Approved, or Rejected.

2. Programme Coordinator / Academic Manager**
- Views all claims submitted by lecturers.
- Verifies supporting documents and claim details.
- Approves or rejects claims and can view reports.

 CI/CD Build Status
This project uses GitHub Actions for continuous integration. The build workflow automatically builds the solution on every push to ensure code integrity.

![Green Build](green-build.png)

 Technologies Used
- C# / .NET 8.0
- WPF
- GitHub Actions
