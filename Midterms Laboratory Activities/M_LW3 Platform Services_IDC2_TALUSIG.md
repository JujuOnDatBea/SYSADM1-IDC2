![image](https://github.com/user-attachments/assets/ae81ab12-b6ab-43d1-b58a-482710f8e040)


# SYSADM1 -- Platform Services

# Requirement: 

-   A virtual machine running Windows Server

    **Objective/s:**

    To analyze IIS logs in the Event Viewer to identify critical web
    service metrics, understand common error codes, and learn how to
    monitor the health of web applications.

**Instructions**

**Part 1: Opening Event Viewer and Loading Logs**

1.  Access the event viewer in the server.

2.  From the event viewer, explore the windows log and list down its
    major categories:

![image](https://github.com/user-attachments/assets/de4a9a50-eeb5-4546-8d9b-251144f71ecd)


Its major categories are application, security, setup, system, and
forwarded events.

**Part 2: Filtering and Analyzing IIS Events**

1.  Apply filter to the windows log categories to display errors for the
    past 12 hours.

Error filter for all categories:

![image](https://github.com/user-attachments/assets/491cd291-4b22-452f-8fb8-a02205c91c7f)


Result:

![image](https://github.com/user-attachments/assets/2eae3716-bf23-47f2-b54a-607762dc7f1b)
![image](https://github.com/user-attachments/assets/325ae3c9-e172-4fc5-a91f-6b366a4f62f6)
![image](https://github.com/user-attachments/assets/c537b86a-2b77-46c9-991a-cc424932495f)


10 errors and 23 warnings identified, with 5 errors and 2 warnings found for the application category while 5 errors and 21 warnings found for the system category.

2.  **Identify Critical Events** or recurring events.

3.  **Analyze the Events**:

    -   For each critical or recurring event, **record the following
        details**:

        -   **Event ID**

        -   **Source**

        -   **Timestamp**

        -   **Description**

![image](https://github.com/user-attachments/assets/cd80d0ce-5e50-4d0a-9818-f53234183751)


**Part 3: Troubleshooting and Solution Development**

1.  Review the logs and check for recurring errors.

> The 3 recurring errors I found were event IDs 1014, 34, and 10149.

2.  Is there a specific time or pattern to these errors?

> There is no specific time or pattern for event ID 1014 as for event ID 34, it seems to happen twice before recurring again. For event ID 10149, it only happened twice so I could not conclude any time or pattern for it.

3.  Draft a Troubleshooting Report:

    -   Based on the events found, create a short report with the
        following sections:

**Report Structure**

**1.** Overview

During the review of the Event Viewer logs from a Windows Server 2012 machine running in a VirtualBox environment, I found that no critical errors occurred in the past 12 hours. However, there were a total of 33 events logged under the Warning and Error event levels.

2\. Key Findings

-   List the critical events you found. Example:

    -   Event ID 34: Occurred 6 times between 8:32 am and 8:33 am Disk write cache disabled.

    -   Event ID 1014: Occurred 10 times between 8:14 am and 8:35 am DNS resolution issues.

    -   Event ID 10149: Occurred 2 times between 8:16 am and 8:32 am WinRM service no listening for management requests.

**3.** Root Causes and Solutions

> Event ID 34 is likely related to driver related issues, updating the drivers should fix the problem. Event ID 1014 is likely related to misconfigurations on the DNS server and naming. Rechecking these configurations and making sure the right configurations are set should be able to take care of this event.

**Part 4: Reflection Questions**

1.  What are the most common causes of a **503 Service Unavailable**
    error?
>   The most common causes of a 503 Service Unavailable error include server overload, scheduled maintenance, misconfigured server settings, resource limits being exceeded, or network connectivity issues between servers. These errors typically indicate that the server cannot handle the request temporarily.

2.  How would you **monitor login attempts** to detect potential
    security threats?
>   To monitor login attempts for potential security threats, administrators can enable logging of successful and failed login events in the system logs, analyze patterns using monitoring tools, and set alerts for suspicious activity such as repeated failed attempts or logins from unusual locations. Automated tools like SIEM solutions can provide real-time insights and notifications.

3.  Why is **monitoring logs** in Event Viewer important for
    administrators?
>   Monitoring logs in Event Viewer is critical for administrators because it helps identify and troubleshoot system errors, security breaches, and performance issues. Logs provide detailed records of events, enabling proactive maintenance and quick response to threats or malfunctions.

Grading Rubric

  ---------------------------------------------------------------------------------------------------------------------------------------
  **Criteria**        **Excellent**     **Good**          **Needs                           **Poor**                         **Points**
                                                          Improvement**                                                      
  ------------------- ----------------- ----------------- --------------- ----------------- ------------- ------------------ ------------
  **Log Analysis**    Identifies all    Identifies most   Identifies some                   Fails to                         /10
                      key events (503,  key events with   events, but                       identify key                     
                      404, 500, etc.)   minor errors in   with incomplete                   events or                        
                      with accurate     details.          or incorrect                      provides                         
                      event details.                      details.                          incorrect                        
                                                                                            details.                         

  **Troubleshooting   Proposes logical, Solutions are     Solutions are                     Solutions are                    /10
  Solutions**         effective         mostly correct    somewhat vague                    unclear or                       
                      solutions to all  but miss some key or incomplete.                    incorrect.                       
                      identified        points.                                                                              
                      issues.                                                                                                

  **Report Structure  Well-organized    Report is mostly  Report is                         Report is                        /10
  & Clarity**         report with all   organized with    disorganized or                   unclear or                       
                      sections clearly  minor formatting  missing                           incomplete.                      
                      completed.        issues.           sections.                                                          

  **Recommendations   Provides          Recommendations                   Recommendations                 Fails to provide   /10
  for Monitoring**    thoughtful,       are relevant but                  are vague or                    relevant           
                      proactive         lack depth.                       incomplete.                     recommendations.   
                      recommendations                                                                                        
                      to prevent future                                                                                      
                      issues.                                                                                                

  **Participation &   Actively engaged  Participated but                  Minimal                         Did not            /10
  Effort**            in the activity,  required some                     participation,                  participate        
                      followed          guidance.                         needed                          meaningfully.      
                      instructions                                        significant help.                                  
                      thoroughly.                                                                                            

  **Score**                                                                                                                  **/50**
  ---------------------------------------------------------------------------------------------------------------------------------------
