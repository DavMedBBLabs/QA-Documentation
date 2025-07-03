
**Description**

**As** a user of the Riwi Talent system,

**I want** automatic emails to be sent

**when** a developer is marked as “Preselected” 

**so** that the developer, the client and the internal RIWI teams (Product, Life Skills, Technical and Commercial) receive the information immediately **and** in a traceable way.

  

**User Role**

Internal user  

  

**User flow**

1. Select a group of developers to add to a process  
    
2. Confirm selection of developers in process

---

1. User intent (Macro) 
   
	1. SCENARIO 1: Successful notification on preselection GIVEN that the user has “Process Manager” permissions AND there is an active developer with status “available” or “in process”. WHEN he confirms the action “Mark as Pre-Selected”. THEN the system sends an email to the Pre-selected Developer, Partner Company and internal Riwi Teams (Product, Life Skills, Technical, Commercial) And a green toast with the text “Notification sent successfully” is displayed.  
    

2. Full functional flow (Intermediate)  
	1. SCENARIO 2: Base flow of pre-selection WHEREAS the confirmation modal is visible WHEN the user clicks on “Add”. THEN the system updates the developer's status to “Pre-Selected”. AND triggers the mailing defined in scenario 1.  
    
	2. SCENARIO 3: User cancels preselection  WHEREAS the confirmation modal is visible WHEN the user selects “Cancel”.  THEN the system closes the modal AND DOES NOT change the status or send mails.