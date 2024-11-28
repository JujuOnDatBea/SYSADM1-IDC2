+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| d150a29a21df403b964188ecaf35f0b3 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: TALUSIG, NIKOS A.          | DATE PERFORMED:        |          |
|                                  | 08/29/24               |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 08/29/24               |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Managing Services in Windows

# Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

# Instructions:  {#instructions .list-paragraph}

1.  Open the Start menu and search for \"Services\"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

+-------+----------------+-------------------------------------------+---+
| **Sta | **Name of      | **Screenshot**                            |   |
| tus** | Service**      |                                           |   |
+=======+================+===========================================+===+
| Start | Remote Access  | ![](vertop                                |   |
|       | Connection     | al_d150a29a21df403b964188ecaf35f0b3/media |   |
|       | Manager        | /image2.png){width="3.6463418635170606in" |   |
|       |                | height="0.541742125984252in"}             |   |
|       |                |                                           |   |
|       |                | ![](vert                                  |   |
|       |                | opal_d150a29a21df403b964188ecaf35f0b3/med |   |
|       |                | ia/image3.png){width="3.06292760279965in" |   |
|       |                | height="0.1875262467191601in"}            |   |
+-------+----------------+-------------------------------------------+---+
| Stop  | Windows Update | ![](verto                                 |   |
|       |                | pal_d150a29a21df403b964188ecaf35f0b3/medi |   |
|       |                | a/image4.png){width="3.854704724409449in" |   |
|       |                | height="0.45839676290463693in"}           |   |
|       |                |                                           |   |
|       |                | ![](vertop                                |   |
|       |                | al_d150a29a21df403b964188ecaf35f0b3/media |   |
|       |                | /image5.png){width="1.5210454943132108in" |   |
|       |                | height="0.2500349956255468in"}            |   |
+-------+----------------+-------------------------------------------+---+
| Re    | DNS Client     | ![](verto                                 |   |
| start |                | pal_d150a29a21df403b964188ecaf35f0b3/medi |   |
|       |                | a/image6.png){width="3.938050087489064in" |   |
|       |                | height="0.9793033683289589in"}            |   |
|       |                |                                           |   |
|       |                | ![](vertop                                |   |
|       |                | al_d150a29a21df403b964188ecaf35f0b3/media |   |
|       |                | /image7.png){width="3.9172134733158357in" |   |
|       |                | height="1.7398261154855643in"}            |   |
|       |                |                                           |   |
|       |                | ![](verto                                 |   |
|       |                | pal_d150a29a21df403b964188ecaf35f0b3/medi |   |
|       |                | a/image8.png){width="3.938050087489064in" |   |
|       |                | height="1.7294083552055992in"}            |   |
+-------+----------------+-------------------------------------------+---+
| Pause | Telephony      | ![](vertop                                |   |
|       |                | al_d150a29a21df403b964188ecaf35f0b3/media |   |
|       |                | /image9.png){width="3.8130325896762907in" |   |
|       |                | height="0.5938331146106737in"}            |   |
|       |                |                                           |   |
|       |                | ![](vertopa                               |   |
|       |                | l_d150a29a21df403b964188ecaf35f0b3/media/ |   |
|       |                | image10.png){width="3.6255063429571304in" |   |
|       |                | height="0.16668963254593175in"}           |   |
+-------+----------------+-------------------------------------------+---+

4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:
>
> ![](vertopal_d150a29a21df403b964188ecaf35f0b3/media/image11.png){width="3.2370122484689414in"
> height="3.6286504811898515in"}
> ![](vertopal_d150a29a21df403b964188ecaf35f0b3/media/image12.png){width="4.188083989501313in"
> height="4.7194083552056in"}
>
> ![](vertopal_d150a29a21df403b964188ecaf35f0b3/media/image13.png){width="3.841803368328959in"
> height="4.308920603674541in"}![](vertopal_d150a29a21df403b964188ecaf35f0b3/media/image14.png){width="4.188083989501313in"
> height="4.7194083552056in"}![](vertopal_d150a29a21df403b964188ecaf35f0b3/media/image15.png){width="4.208920603674541in"
> height="4.781917104111986in"}

5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![](vertopal_d150a29a21df403b964188ecaf35f0b3/media/image16.png){width="4.808325678040245in"
> height="2.0055664916885387in"}

7.  Save the batch file in Z:\\lastname_timer.bat

8.  Use the sc command to add timer.bat service in the command line
    interface.

> *sc create BatchTimerService binPath= \"path_to_your_batch_file.bat\"
> start= auto*
>
> *net start BatchTimerService*
>
> **Replace path_to_your_batch_file.bat with the actual path to your
> batch file.**
>
> ![](vertopal_d150a29a21df403b964188ecaf35f0b3/media/image17.png){width="7.027083333333334in"
> height="2.9166666666666665in"}

9.  Verify that BatchTimerService has been added to the services.

> **SS:**
> ![](vertopal_d150a29a21df403b964188ecaf35f0b3/media/image18.png){width="7.027083333333334in"
> height="1.2666666666666666in"}

10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
>
> ![](vertopal_d150a29a21df403b964188ecaf35f0b3/media/image19.png){width="5.413603455818023in"
> height="3.1166152668416447in"}

**Rubric**

  ---------------------------------------------------------------------------------------
  **Criteria**      **Excellent       **Good (7)**    **Needs          **Unsatisfactory
                    (10)**                            Improvement      (1)**
                                                      (3)**            
  ----------------- ----------------- --------------- ---------------- ------------------
  Understanding of  Demonstrates a    Shows a solid   Has a basic      Shows little or no
  Services          deep              understanding   understanding of understanding of
                    understanding of  of services,    services, but    services.
                    the concept of    but may lack    may struggle     
                    services, their   some depth in   with specific    
                    roles, and their  specific areas. concepts.        
                    importance in                                      
                    Windows.                                           

  Service           Successfully      Demonstrates    Can perform      Struggles to
  Management Skills starts, stops,    proficiency in  basic service    perform even basic
                    restarts, and     managing        management       service management
                    configures        services, but   tasks, but may   tasks.
                    services using    may encounter   need assistance  
                    the Services app. minor           or guidance.     
                                      difficulties.                    

  Custom Service    Successfully      Can create a    Has limited      Cannot create a
  Creation          creates and       custom service, experience with  custom service.
                    manages a custom  but may         creating custom  
                    service using the encounter minor services.        
                    appropriate tools difficulties or                  
                    and techniques.   require                          
                                      assistance.                      

  Problem-Solving   Demonstrates      Can effectively May require      Struggles to
                    strong            troubleshoot    assistance to    troubleshoot and
                    problem-solving   and resolve     troubleshoot     resolve issues.
                    skills when       most issues     some issues.     
                    encountering      related to                       
                    challenges or     service                          
                    errors.           management.                      

  Documentation and Provides clear    Documents the   Provides basic   Does not provide
  Reporting         and concise       lab activities  documentation,   any documentation
                    documentation of  adequately, but but may be       or reporting.
                    the lab           may lack some   disorganized or  
                    activities,       detail or       incomplete.      
                    including         clarity.                         
                    relevant                                           
                    screenshots and                                    
                    observations.                                      

  **Score:**        **/50**                                            
  ---------------------------------------------------------------------------------------
