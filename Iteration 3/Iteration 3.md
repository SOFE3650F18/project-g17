# Iteration 3: Addressing Quality Attribute Scenario Driver (QA2)

In this iteration we want to refine previously created structures to address the remaining drivers. Tactics, Deployment patterns and Architectural patterns will be used.

The driver for this iteration will be QA-2 security:   All data kept private to relevant users, data visibility and modifiability up to discretion of user / lecturers / administrators.



#### Step 2: Establish Iteration Goal by Selecting Drivers

The driver for this iteration will be QA-2 security:   All data kept private to relevant users, data visibility and modifiability up to discretion of user / lecturers / administrators.

The remaining QA scenarios and remaining drivers will also be considered, as this will be the final iteration and we want to address the remaining drivers.

#### Step 3: Choose one or more elements of the System to Refine

The elements being refined are the application server and the database server.

#### Step 4: Choose One or More Design Concepts that Satisfy the Selected Drivers

| Design Decisions and Location                                | Rationale and Assumptions                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Introduce the security tactic to resist attacks This can be done by using the Spring Security framework to manage authorization and authentication | The rationale behind this decision is that it supports the driver QA-2. This spring security framework can be implemented as part of the application server and database server. It allows for the managing of authorization and authentication. Alternatives considered include: Ad hoc code which was discarded because it would take a lot more resources to develop an authentication system from scratch as opposed to implementing a frame work. |
| Use the interoperability tactic                              | The discover service tactic can be used to address CON-3. It is used to search for locations on the service. |



#### Step 5: Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces

| Design Decisions and Locations                              | Rationale                                                    |
| ----------------------------------------------------------- | ------------------------------------------------------------ |
| The Spring security framework is added as a component       | this addresses QA-2. It will allow for authentication and authorization of the users attempting to access data. |
| A discover service component is added in the services layer | When a user is making a request they can use the discover service to search for services. Allowing them to reach content within 3 clicks. |
|                                                             |                                                              |



#### Step 6: Sketch Views and Record Design Decisions 



The Spring Security framework is added as a component. There is a Security Manager Module that connects to the Presentation layer, business layer and Data Access layer. This prevents access to data of unauthorized users as they must be authenticated by the Security Manager before gaining access to the data. 



![alt text](https://github.com/SOFE3650F18/project-g17/blob/master/Iteration%203/Class%20Diagram1.jpg)

The Sequence diagram below shows the sequence of interactions that take place when the user uses the DiscoverService element to search for a file or directory. The rationale behind including this element was that it is a way of addressing the QA-3 and CON-3 that requires a three click maximum when a user wants to reach any content. 

The alternative would be to either have a link to most major directories on all pages or another form of navigation that would provide easy access to directories. Implementing this would require restructuring of existing components so we decided against it. 

![alt text](https://github.com/SOFE3650F18/project-g17/blob/master/Iteration%203/discoverservice.jpg)



#### 

| Element          | Responsibility                                               |
| ---------------- | ------------------------------------------------------------ |
| Security Manager | The security manager module is implemented using Spring Security. It handles authentication of users and keeps data private to relevant users. |
| Discover Service | This module allows users to locate a service by searching a known directory. |
|                  |                                                              |

#### 



#### Step 7: Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose

| Not Addressed | Partially Addressed | Completely Addressed | Design Decisions Made During the Iteration                   |
| ------------- | ------------------- | -------------------- | ------------------------------------------------------------ |
|               |                     | QA-2                 | Security Manager module implemented                          |
|               |                     | QA-3                 | Discover service tactic implemtented                         |
|               | QA-4                |                      | The use case related to this QA has been identified.         |
|               |                     | CON-1                | Security Manager module implemented                          |
|               | CON-3               |                      | No relevant decisions made                                   |
|               | CON-4               |                      | No relevant decisions made |
|               | CON-5               |                      | No relevant decisions made  |
