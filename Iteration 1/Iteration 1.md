# Iteration 1: Establishing an overall System Structure

#### Step 2: Establish Iteration Goal by Selecting Drivers

This section is driven mostly by CRN-1, however all drivers from step 1 are relevant. 

#### Step 3: Choose one or more elements of the System to Refine

Since it is a greenfield development, the element being refined is the entire CMS system.

![alt text](https://raw.githubusercontent.com/SOFE3650F18/project-g17/master/Iteration%201/Context%20Diagram%20for%20CMS%20System.png "Context diagram for CMS system")

#### Step 4: Choose One or More Design Concepts that Satisfy the Selected Drivers

| Design Decisions and Location                                | Rationale                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Use the Web Applications reference architecture to structure the client part of the system | The three layers will support the system. The presentation layer can contain modules responsible for user interaction(CON-5). The data layer contains modules that handle data stored either locally or remotely (CON-6). |
| three-tier distributed deployment                            | Allows flexibility in regards to components residing in different tiers. Allows scalability as more tiers can be added. Adds security with firewalls between layers and security policies may be added to tiers.  Database can be stored in a layer separate from the application. |
|                                                              |                                                              |

#### Step 5: Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces

#### Step 6: Sketch Views and Record Design Decisions 

#### Step 7: Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose
