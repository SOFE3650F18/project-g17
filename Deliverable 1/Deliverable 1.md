### Use Cases

| Use Case                                                     | Requirements     | Description                                                  |
| ------------------------------------------------------------ | ---------------- | ------------------------------------------------------------ |
| UC-1: Retrieve and display course information (including history and grades) | 1-6, 9-10, 26    | Provide / stores / represents static and dynamic course information, provides history of a course, provide student course attendance and grades per semester |
| UC-2: Modify enrolled courses and exams                      | 11-12            | Allow students to subscribe/unsubscribe to courses and exams |
| UC-3: Access course-wide messaging and notification system   | 7, 16, 24        | Provides an inter-course messaging system, which also notifies students of upcoming events in course |
| UC-4: Access group and file sharing system                   | 8, 13-20, 24     | Inter-course team system in which students can: retrieve contact information, share files, and search for files within the course |
| UC-5: Login and user settings                                | 21-23, 25        | Allows students to edit personal information and user settings (password), reset their password, and customize notifications |
| UC-6: Create / recreate courses                              | 48-50            | Allow lecturers to create and recreate courses               |
| UC-7: Modify course details                                  | 51-52, 59-65, 68 | Register course TAs, prepare lecture schedule, set course registration requirements, manage static and dynamic course information |
| UC-8: Course mail system                                     | 56-58            | Allow lecturers to send mail to all students or a subset of students, allow for mail templates. |
| UC-9: Course interaction system                              | 66-67, 69        | View personal information of students in their courses, plan meetings with individual students, and post news messages relating to course |
| UC-10: Add content and grades to course                      | 53-55, 70-82     | Upload and manage course materials (I.e. lecture notes), set visibility of lecture notes, and allows for the management of inter-course teams. Upload and manage grades and grade weighting, as well as check grade statistics for other courses |
| UC-11: Create and manage backups                             | 88-89            | Allow system maintainers to create, manage, and restore backups of the system |
| UC-12: Set size restrictions for courses                     | 90-91            | Set restrictions of the number and size of files per course, and set total storage limit per course. |
| UC-13: Manage course and course involvement                  | 97-106, 118      | Allow administrators to manage courses (create/delete), set course registration requirements, set principle lecturers, and override registration requirements for students. |
| UC-14: View / manage all participant information             | 107-109          | View information related to all participants within a course, and set lecturer information. |
| UC-15: Generate statistics and surveys                       | 110-117          | Calculate multiple different grade statistics per course / department, and evaluate courses with web-surveys. |
| UC-16: (Automatically) Synchronize with secondary university systems | 119-120          | Disallow modification of information used and maintained by secondary university systems, and synchronize this system with secondary systems. |

### Use Case Diagram
![alt text](https://raw.githubusercontent.com/SOFE3650F18/project-g17/master/Deliverable%201/Use%20Case%20Diagram.png)

### Quality Attribute Scenarios

| ID   | Quality Attribute                | Scenario                                                     | Associated Use Case |
| ---- | -------------------------------- | ------------------------------------------------------------ | ------------------- |
| QA-1 | Availability                     | Sceduelded and unscedueled downtime should be no more than 4 hours per month, during low-intensity hours | All                 |
| QA-2 | Security, Privacy                | All data kept private to relevant users, data visibility and modifibilty up to discretion of user / lecturers / administrators | All                 |
| QA-3 | User Friendliness, Accessibility | Bilingual support, UI elements self-descriptive, all content easiliy accessable (3 clicks maximum), accessible by diabled users | All                 |
| QA-4 | Interoperability                 | Provides an export for common calendar formats, and should integrate with other (secondary) university systems | UC-16               |
| QA-5 | Extensibility                    | All administation to make exceptions is regards to course requirements and limits | UC-13               |
| QA-6 | Maintainability, Fault-tolerance | System allows for creation of backups, and the ability for partial or full restoration of backups | UC-11               |

### Constraints

| ID    | Constraint                                                   |
| ----- | ------------------------------------------------------------ |
| CON-1 | System should be secure, protect users privacy.              |
| CON-2 | Accessed through the user's browser                   |
| CON-3 | User friendly, bilingual support, single login, 3 clicks maximum to reach all content. Navigable by disabled (blind) users |
| CON-4 | High interoperability, allow for multiple formats for importing / exporting data. |
| CON-5 | System easily expanded, scalable, and testable, along with compatible with other university systems. |

### Architectural Concerns

| ID    | Concern                                |
| ----- | -------------------------------------- |
| CRN-1 | Establish overall system structure     |
| CRN-2 | Leverage of team's knowldege           |
| CRN-3 | Allocation of work to development team |
