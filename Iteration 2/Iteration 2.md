# Iteration 2: Identifying Structures to Support Primary Functionality

#### Step 2: Establish Iteration Goal by Selecting Drivers

The primary use cases for the system in iteration 2 are: UC-1, UC-3, UC-4, UC-7, and UC-10.

#### Step 3: Choose one or more elements of the System to Refine

The elements being refined are the modules described in Modular View diagram from iteration 1.

#### Step 4: Choose One or More Design Concepts that Satisfy the Selected Drivers

| Design Decisions and Location                                | Rationale and Assumptions                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Create a domain model for the application                    | A domain model is necessary for proper decomposition of the system. |
| Identify domain objects that map to functional requirements  | Every functional element of the application (Each use case) needs to have it's own building block / domain object. |
| Decompose domain objects into general and specialized components | A domain object is a complete set of functionality. We want to breakdown there into smaller elements called components (referred to as modules previously). |
| Use RESTful API  to connect to and query an ASP.NET based database | AngularJS (framework used to build the interface) also has built in functionality to connect with databases. This functionality was determined to be the best option as it works well with the interface, and reduces the number of different external frameworks being used. <br>ASP.NET server was chosen since AngularJS has native functionality with this web server. It is also open source, allowing us to keep the total cost down.</br> |

#### Step 5: Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces

| Design Decisions and Location                                | Rationale                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Create only an initial domain model                          | Entities that are in the primary use cases are to be identified and modeled. An initial domain model is created. |
| Map system use cases to domain objects                       | Domain objects are identified for all use case drivers.      |
| Decompose domain objects in each layer to find layer specific modules | Used to identified all modules that support all functionalities for the system. |

#### Step 6: Sketch Views and Record Design Decisions 

##### The initial domain model for the system:

![](https://raw.githubusercontent.com/SOFE3650F18/project-g17/master/Iteration%202/Initial%20Domain%20Model.png)

##### The domain objects associated with the use case model:

![](https://raw.githubusercontent.com/SOFE3650F18/project-g17/master/Iteration%202/Domain%20Object%20from%20Use%20Cases.png)

##### Modular view with modules that support primary use cases:

![](https://raw.githubusercontent.com/SOFE3650F18/project-g17/master/Iteration%202/Modular%20View%20from%20Primary%20Use%20Cases.png)

| Element                   | Responsibility                                               |
| ------------------------- | ------------------------------------------------------------ |
| CourseInformationView     | Displays course information.                                 |
| CourseManagementView      | Displays course information management view. Data related to course information is modifiable through here. When data is updated, updates both local data for CourseInformationView, as well as the data in the database. |
| CourseMessageView         | Displays messages related to the course.                     |
| CourseFileView            | Displays files related to the course                         |
| CourseInfoController      | Provides and receives information related to the course itself (Basic course information, course messages). |
| FileController            | Provides and receives file information.                      |
| RequestManager            | Responsible for communication with server side logic         |
| RequestService            | Receives requests from clients                               |
| TopologyController        | Contains business layer logic related to topographical information of server. |
| DomainEntities            | Contains entities from domain model of the server.           |
| SecondarySystemController | Contains logic related to data storage and retrieval from secondary systems. |
| SecondarySyncController   | Contains logic related to ensuring the main system and secondary systems remain in sync. |
| ContentDataMapper         | Responsible for CRUD operations related to all content for the direct CMS. |
| SecondarySystemMapper     | Responsible for CRUD operations related to the external secondary systems. |
| SecondarySystemConnector  | Responsible for communication with secondary systems. It abstracts operations such that it can connect with any number of different secondary systems. |

##### UC-1: Sequence Diagram

##### UC-3: Sequence Diagram

##### UC-4: Sequence Diagram

##### UC-7: Sequence Diagram

##### UC-10: Sequence Diagram

##### UC-16: Sequence Diagram

#### Step 7: Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose

| Not Addressed | Partially Addressed | Completely Addressed | Design Decisions Made During the Iteration                   |
| ------------- | ------------------- | -------------------- | ------------------------------------------------------------ |
|               |                     | UC-1                 | Modules in both layers and interfaces for this case have been identified. |
|               |                     | UC-3                 | Modules in both layers and interfaces for this case have been identified. |
|               |                     | UC-4                 | Modules in both layers and interfaces for this case have been identified. |
|               |                     | UC-7                 | Modules in both layers and interfaces for this case have been identified. |
|               |                     | UC-10                | Modules in both layers and interfaces for this case have been identified. |
|               |                     | UC-16                | Modules in both layers and interfaces for this case have been identified. |
|               | QA-2                |                      | No relevant decisions made                                   |
|               | QA-3                |                      | No relevant decisions made                                   |
|               | QA-4                |                      | The use case related to this QA has been identified.         |
|               | CON-1               |                      | No relevant decisions made                                   |
|               |                     | CON-2                | N/A                                                          |
|               | CON-3               |                      | No relevant decisions made                                   |
|               | CON-4               |                      | The data abstraction module for secondary systems has been identified. |
|               | CON-5               |                      | The data abstraction module for secondary systems has been identified. |
|               |                     | CRN-1                | N/A                                                          |
|               |                     | CRN-2                | N/A                                                          |
|               |                     | CRN-3                | Work has been allocated to development team                  |