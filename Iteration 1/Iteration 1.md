# Iteration 1: Establishing an overall System Structure

#### Step 2: Establish Iteration Goal by Selecting Drivers

This section is driven mostly by CRN-1, however all drivers from step 1 are relevant. 

#### Step 3: Choose one or more elements of the System to Refine

Since it is a greenfield development, the element being refined is the entire CMS system.

![alt text](https://raw.githubusercontent.com/SOFE3650F18/project-g17/master/Iteration%201/Context%20Diagram%20for%20CMS%20System.png "Context diagram for CMS system")

#### Step 4: Choose One or More Design Concepts that Satisfy the Selected Drivers

| Design Decisions and Location                                | Rationale                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Logically structure the client part of the system using a web application reference architecture | This architecture is based in a web browser and communicated with the server using HTTP (CON-2).  Most of the application and data is stored on the server (QA-2, CON-1). |
| Logically structure the server part of the system using a service application reference architecture | This design architecture does not require any sort of UI. The presentation layer only contains a message interface, allowing for simple transfer of data between the server and the user. Also allows for data transfer from other services (UC-16). |
| Physically structure the application using the three-tier pattern | The three layers will support the system. The presentation layer can contain modules responsible for user interaction (CON-3). The data layer contains modules that handle data stored either locally or remotely (CON-4). |
| Build the interface of the client application using the Angular JS framework | Separates presentation logic from business logic. Provides a clean, single page framework, limiting the 'distance' to any information (QA-3, CON-3). |

#### Step 5: Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces

| Design Decision and Location                                 | Rationale                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Create module to access secondary university systems in data layer of service application reference architecture. | The reference architecture is adapted to access secondary university systems. Plays a critical role in QA-4 and UC-16. |

#### Step 6: Sketch Views and Record Design Decisions 

![](https://raw.githubusercontent.com/SOFE3650F18/project-g17/master/Iteration%201/Modular%20View.png)

| Element                  | Responsibility                                               |
| ------------------------ | ------------------------------------------------------------ |
| *Presentation CS*        | Contains modules controlling user interaction and use cases  |
| UI Module                | Render UI and receive user inputs                            |
| UI Process Module        | Controls flow of UI (use cases)                              |
| *Business Logic CS*      | Contains modules controlling client side business logic operations |
| Business Module CS       | Implement business operations or expose business operations from server |
| Business Entities CS     | Make up domain model                                         |
| *Data CS*                | Contains modules that communicate with server                |
| Communication Module     | Consume services by application on server                    |
| *Cross-Cutting CS / SS*  | Contains multi-layer modules                                 |
| *Services SS*            | Contains modules that expose services for clients            |
| Service Interface        | Module that expose services for clients                      |
| *Business Logic SS*      | Contains modules that perform business logic operations for server side |
| Business Module SS       | Implement business operations                                |
| Business Entities SS     | Entities that make up domain model                           |
| *Data SS*                | Contains modules that are responsible for data and server communication |
| DB Access Module         | Responsible for data from main database, shields application from unnecessary details |
| Secondary Service Module | Responsible for data import/export for exterior university systems |

![](https://raw.githubusercontent.com/SOFE3650F18/project-g17/master/Iteration%201/Deployment%20Diagram.png)



| Element            | Responsibility                         |
| ------------------ | -------------------------------------- |
| User Workstation   | Hosts client side logic                |
| Application Server | Serves web pages, server side logic    |
| Database Server    | Hosts system database                  |
| Secondary Systems  | The set of external university systems |

| Relationship                           | Description                                                |
| -------------------------------------- | ---------------------------------------------------------- |
| Between app server and database server | Communication done using ODBC (Open Database Connectivity) |



#### Step 7: Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose

| Not Addressed | Partially Addressed | Completely Addressed | Design Decisions Made During the Iteration                   |
| ------------- | ------------------ | -------------------- | ------------------------------------------------------------ |
| UC-1          |                    |                      | N/A                                                          |
| UC-3          |                    |                      | N/A                                                          |
| UC-4          |                    |                      | N/A                                                          |
| UC-7          |                    |                      | N/A                                                          |
| UC-10         |                    |                      | N/A                                                          |
|               | UC-16              |                      | Server structure to handle secondary system information was decided |
|               | QA-2               |                      | Use of web application architecture to increase system security |
|               | QA-3               |                      | Use of Angular JS to limit number of clicks to any content   |
| QA-4          |                    |                      | N/A                                                          |
| CON-1         |                    |                      | N/A                                                          |
|               |                    | CON-2                | Decision on front end reference architecture, web application reference architecture |
|               | CON-3              |                      | Use of Angular JS to limit number of clicks to any content, and decision on three-layer style |
| CON-4         |                    |                      | N/A                                                          |
| CON-5         |                    |                      | N/A                                                          |
|               | CRN-1              |                      | Set overall design specifications                            |
|               |                    | CRN-2                | Used team's knowledge and strengths to choose suitable architectures and design styles |
| CRN-3         |                    |                      | N/A                                                          |

