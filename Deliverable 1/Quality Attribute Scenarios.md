**UC-1 Display course information:**
​	Source: Any user
​	Stimulus: Request for data
​	Environment: During normal operations
​	Response: Returns the requested information to the user
​	Response measure: Response time per item requested

**UC-2 Modify enrolled courses and exams:**
​	Source: Student
​	Stimulus: Request to modify data
​	Environment: During normal operations
​	Response: Allows user to modify internal course / exam files based on userID
​	Response measure:  Response time per item modified 

**UC-3 Access messaging and notification system:**
​	Source: Student
​	Stimulus: Request for data
​	Environment: During normal operations
​	Response:  Returns the requested information to the user
​	Response measure: Response time per item requested 

**UC-4 Access group and file sharing system:**
​	Source: Student
​	Stimulus: Request to view system
​	Environment: During normal operations
​	Response: Allows access to information and files based on userID
​	Response measure: Data transfer rate

**UC-5 Manage account settings:**
​	Source: Student
​	Stimulus: Request to change values
​	Environment: During normal operations
​	Response: Allows users to modify personal settings
​	Response measure: Success rate of variables changed

**UC-6 Create / recreate course:**
​	Source: Lecturer 
​	Stimulus: Request to modify courses
​	Environment: During normal operations
​	Response: Creates requested course
​	Response measure:  Response time per item modified 

**UC-7 Course mail system:**
​	Source: Lecturer 
​	Stimulus: Request to access mail server
​	Environment: During normal operations
​	Response: Sends message to entire course or specific participants
​	Response measure: Delay in messages being sent / recieved

**UC-8 Modify course details:**
​	Source: Lecturer 
​	Stimulus: Request to modify course
​	Environment: During normal operations
​	Response: Allows user to modify participant settings
​	Response measure:  Response time per item modified

**UC-9 Course interaction system:**
​	Source: Lecturer 
​	Stimulus: Request to notify particiapants
​	Environment: During normal operations
​	Response: Allows users to interact with specific participants outside of mail system
​	Response measure: System response time for interactions

**UC-10 Add content and grades:**
​	Source: Lecturer 
​	Stimulus: Request to modify course values
​	Environment: During normal operations
​	Response: Adds requested content to course
​	Response measure: Latency in grade updating

**UC-11 Create / manage backups:**
​	Source: Maintainer / Administrator
​	Stimulus: Request to backup OR request to instantiate a backup
​	Environment: During normal operations
​	Response: Backs up system OR restores system to backup
​	Response measure: Data loss in backup process

**UC-12 Set course content size restrictions:**
​	Source: Maintainer / Administrator
​	Stimulus: Request to modify course
​	Environment: During normal operations
​	Response: Changes course variables
​	Response measure:  Response time per item modified

**UC-13 View / manage participant information:**
​	Source: Administrator
​	Stimulus: Request to view participants
​	Environment: During normal operations
​	Response: View information about participants in specific course
​	Response measure: Response time per item requested 

**UC-14 Manage courses:**
​	Source: Administrator
​	Stimulus: Request to modify courses
​	Environment: During normal operations
​	Response: Modifies requested courses
​	Response measure:  Response time per item modified

**UC-15 Generate statistics and surveys:**
​	Source: Administrator
​	Stimulus: Request for statistics
​	Environment: During normal operations
​	Response: Generates requested statistic OR sends survey to participants
​	Response measure: Latency in statistic generation

**UC-16 (Automatically) Synchronize with secondary system:**
​	Source: Administrator
​	Stimulus: Set timer OR request to synchronize systems
​	Environment: During normal operations
​	Response: Synchronize needed files with outside systems
​	Response measure: Time to sync files
