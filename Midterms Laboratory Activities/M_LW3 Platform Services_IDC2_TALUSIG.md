+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 4277d020dc9d40528667cec065884077 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: TALUSIG, NIKOS A.          | DATE PERFORMED:        | /50      |
|                                  | 10/17/24               |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 10/17/24               |          |
+----------------------------------+------------------------+----------+

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

![](vertopal_4277d020dc9d40528667cec065884077/media/image2.png){width="1.7398261154855643in"
height="1.1251574803149607in"}

*Its major categories are application, security, setup, system, and
forwarded events.*

**Part 2: Filtering and Analyzing IIS Events**

1.  Apply filter to the windows log categories to display errors for the
    past 12 hours.

[Error filter for all categories:]{.underline}

![](vertopal_4277d020dc9d40528667cec065884077/media/image3.png){width="5.729966097987751in"
height="2.3649136045494314in"}

[Result:]{.underline}

![](vertopal_4277d020dc9d40528667cec065884077/media/image4.png){width="7.027083333333334in"
height="3.7152777777777777in"}

![](vertopal_4277d020dc9d40528667cec065884077/media/image5.png){width="7.027083333333334in"
height="3.0166666666666666in"}

![](vertopal_4277d020dc9d40528667cec065884077/media/image6.png){width="7.027083333333334in"
height="0.17847222222222223in"}

[\
]{.underline}*10 errors and 23 warnings identified, with 5 errors and 2
warnings found for the application category while 5 errors and 21
warnings found for the system category.*

2.  **Identify Critical Events** or recurring events.

3.  **Analyze the Events**:

    -   For each critical or recurring event, **record the following
        details**:

        -   **Event ID**

        -   **Source**

        -   **Timestamp**

        -   **Description**

+----+----------+-----------+----------+---------+-------------------+
| *  | **       | **First   | **Last   | **No.   | **Description**   |
| *E | Source** | Occ       | Occu     | of      |                   |
| ve |          | urrence** | rrence** | Occurr  |                   |
| nt |          |           |          | ences** |                   |
| ID |          |           |          |         |                   |
| ** |          |           |          |         |                   |
+====+==========+===========+==========+=========+===================+
| 10 | DNS      | 10/17/24  | 10/17/24 | 10      | DNS resolution    |
| 14 | Client   | 8:14:31   |          |         | issue             |
|    | Events   | am        | 8:35:19  |         |                   |
|    |          |           | am       |         |                   |
+----+----------+-----------+----------+---------+-------------------+
| 34 | disk     | 10/17/24  | 10/17/24 | 6       | Driver disabling  |
|    |          |           |          |         | write cache       |
|    |          | 8:32:11   | 8:33:02  |         |                   |
|    |          | am        | am       |         |                   |
+----+----------+-----------+----------+---------+-------------------+
| 1  | Windows  | 10/17/24  | 10/17/24 | 2       | WinRM service not |
| 01 | Remote   |           |          |         | listening for     |
| 49 | Manager  | 8:16:06   | 8:32:45  |         | management        |
|    |          | am        | am       |         | requests          |
+----+----------+-----------+----------+---------+-------------------+

**Part 3: Troubleshooting and Solution Development**

1.  Review the logs and check for recurring errors.

> *The 3 recurring errors I found were event IDs 1014, 34, and 10149.*

2.  Is there a specific time or pattern to these errors?

> *There is no specific time or pattern for event ID 1014 as for event
> ID 34, it seems to happen twice before recurring again. For event ID
> 10149, it only happened twice so I could not conclude any time or
> pattern for it.*

3.  Draft a Troubleshooting Report:

    -   Based on the events found, create a short report with the
        following sections:

**Report Structure**

**1.** Overview

*During the review of the Event Viewer logs from a Windows Server 2012
machine running in a VirtualBox environment, I found that no critical
errors occurred in the past 12 hours. However, there were a total of 33
events logged under the Warning and Error event levels.*

2\. Key Findings

-   List the critical events you found. Example:

    -   ***Event ID 34**: Occurred 6 times between 8:32 am and 8:33 am.
        Disk write cache disabled.*

    -   ***Event ID 1014**: Occurred 10 times between 8:14 am and 8:35
        am. DNS resolution issues.*

    -   ***Event ID 10149**: Occurred 2 times between 8:16 am and 8:32
        am. WinRM service no listening for management requests.*

**3.** Root Causes and Solutions

> *Event ID 34 is likely related to driver related issues, updating the
> drivers should fix the problem. Event ID 1014 is likely related to
> misconfigurations on the DNS server and naming. Rechecking these
> configurations and making sure the right configurations are set should
> be able to take care of this event.*

**Part 4: Reflection Questions**

1.  What are the most common causes of a **503 Service Unavailable**
    error?

2.  How would you **monitor login attempts** to detect potential
    security threats?

3.  Why is **monitoring logs** in Event Viewer important for
    administrators?

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
