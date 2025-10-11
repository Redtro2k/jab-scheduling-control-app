# 🧭 Job Scheduling Control App
The **Job Scheduling Control App** is a centralized system designed to efficiently manage, monitor, and coordinate job assignments across teams or departments. It provides an organized, visual way to schedule, track, and control tasks, ensuring that all jobs are executed on time and according to priority. Built with a focus on automation and real-time updates, the app allows administrators to create, assign, and adjust job schedules dynamically — while giving users a clear overview of workloads, progress, and upcoming tasks. Integration with broadcasting tools and calendar views (like FullCalendar) provides a seamless and interactive experience for managing operations.

## ✨ Key Features
- 📅 **Interactive Calendar View** – Visualize job schedules and timelines in an intuitive drag-and-drop calendar.
- ⚙️ **Job Management – Create**, update, and assign jobs or tasks to specific users or departments.
- 🔔 **Real-Time Notifications** – Receive instant updates for job changes, completions, or delays (via Pusher or WebSockets).
- 🗂️ **Process Control Board** – Monitor job status (Pending, Ongoing, Completed) in a Kanban-style dashboard.
- 🧾 **Reporting & History Logs** – Track job performance and maintain a record of completed tasks.
- 👥 **User Roles & Permissions** – Secure and role-based access control for admins, managers, and staff.

## 🧱 Tech Stack
- **Backend**: Laravel 12 + Filament 4 Admin
- **Frontend**: Livewire + Alpine.js + TailwindCSS
- **Real-Time**: Pusher
- **Database**: MySQL

#### System Process
|  #  | Process                                 | Assigned To | Group           |
| :-: | --------------------------------------- | ----------- | --------------- |
|  1  | Ready for Estimation                    | Joma        | Estimation      |
|  2  | Awaiting LOA                            | Joma        | Estimation      |
|  3  | Approved LOA                            | Joma        | Approval        |
|  4  | Waiting Parts (Outside Unit)            | Fhey        | Preparation     |
|  5  | Parts Available / For Unit In           | Fhey        | Preparation     |
|  6  | Unit In – Input Lead Time               | Fhey        | Job Started     |
|  7  | Job Stoppage (Re-inspection)            | Joma        | Rework          |
|  8  | Waiting Additional Parts                | Joma        | Rework          |
|  9  | For Additional Labor                    | Joma        | Rework          |
|  10 | Q.C Passed                              | Kaith       | Quality Control |
|  11 | Parts Price Discrepancy                 | Kaith       | QC / Billing    |
|  12 | Billing                                 | Kaith       | Billing         |
|  13 | For Invoice Sending (Outside Insurance) | Joma        | Billing         |
|  14 | Waiting for Release                     | Kaith       | Finalization    |
|  15 | Released                                | Joma        | Completed       |

## Roles
| Member    | Primary Responsibilities                                          | Suggested Role                       |
| :-------- | :---------------------------------------------------------------- | :----------------------------------- |
| **Joma**  | Estimation, LOA approval, rework management, release coordination | **Service Advisor / Job Controller** |
| **Fhey**  | Parts handling, unit intake, job lead time tracking               | **Parts & Scheduling Coordinator**   |
| **Kaith** | Quality control, billing, and release confirmation                | **QC & Billing Officer**             |
