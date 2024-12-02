+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 477b2109c15a4e7787eb02505d423f98 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: TALUSIG, NIKOS A.          | DATE PERFORMED:        | /50      |
|                                  | 09/26/24               |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 09/26/24               |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Monitoring Print Services in Windows Server 2019

# Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image2.png){width="1.9794433508311462in"
> height="1.4897911198600176in"}

2.  Connect one client to the recently created domain

> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image3.png){width="2.5732753718285215in"
> height="1.5210454943132108in"}

3.  Install Print Services Role:

> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image4.png){width="3.6234241032370953in"
> height="1.4886297025371829in"}

4.  Search the internet for any printer installer and convert it to iso

> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image5.png){width="6.323799212598425in"
> height="0.3125437445319335in"}

5.  Install and deploy it as network printer

> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image6.png){width="4.813171478565179in"
> height="1.7710804899387576in"}
>
> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image7.png){width="2.698292869641295in"
> height="1.7294083552055992in"}

Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in
Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        Windows \> PrintService.

    -   Review logs for print jobs, errors, and warnings.

> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image8.png){width="5.823729221347332in"
> height="1.2085017497812773in"}

2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

    -   In the left pane, expand Data Collector Sets \> System.

    -   Right-click System Performance and select Start.

    -   Monitor performance metrics related to print services.

> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image9.png){width="3.175310586176728in"
> height="1.8567366579177602in"}
>
> ***[Graph goes up every time the printer is used, indicating processor
> use.]{.underline}***

3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image10.png){width="6.598837489063867in"
> height="0.6338648293963255in"}
>
> ***[Printer currently not in use however ready to use.]{.underline}***

Part 3: Exploring Third-Party Monitoring Tools

1.  Research at least two third-party print monitoring tools

    -   Consider factors such as features, pricing, and compatibility
        with Windows Server 2019.

+-----------+--------------------------+-------------------------------+
|           | PaperCut                 | UniFlow                       |
+===========+==========================+===============================+
| Features  | -   Supports mobile      | -   Supports mobile devices.  |
|           |     devices              |                               |
|           |                          | -   Offers over 50            |
|           | -   Administrators can   |     > customizable reports    |
|           |     set rules to control |     > for detailed analysis.  |
|           |     and reduce printing  |                               |
|           |     costs.               | -   Wide range compatibility  |
|           |                          |     > of printers and         |
|           | -   Provides insights    |     > multifunction devices.  |
|           |     into print usage and |                               |
|           |     cost savings.        | -   Print job and retrieval   |
|           |                          |     > from any printer in the |
|           | -   Sensitive documents  |     > network.                |
|           |     are only printed     |                               |
|           |     when user is present |                               |
+-----------+--------------------------+-------------------------------+
| Pricing   | -   Commercial business  | -   Free.                     |
|           |     and educational      |                               |
|           |     pricing ranges from  |                               |
|           |     \$0-\$1385 depending |                               |
|           |     on number of users.  |                               |
|           |                          |                               |
|           | -   Professional clients |                               |
|           |     range from           |                               |
|           |     \$692-\$1712         |                               |
|           |     depending on number  |                               |
|           |     of users.            |                               |
+-----------+--------------------------+-------------------------------+
| Comp      | -   Cross-platform,      | -   Designed to work with     |
| atibility |     supports several     |     various printer brands    |
|           |     major OS such as     |     and works well with       |
|           |     macOS and Linux.     |     Windows Server 2019       |
|           |     Compatible with      |     environments.             |
|           |     Windows Server 2019  |                               |
|           |     as well.             |                               |
+-----------+--------------------------+-------------------------------+

*References:\
PaperCut MF - System requirements \| PaperCut*. (n.d.).
https://www.papercut.com/products/mf/system-requirements/

Pttrns. (2023, September 1). Top 10 Best Print Management Software
Solutions - PTTRns. *Pttrns*.
https://www.pttrns.com/best-print-management-software-solutions/

Willoughby, B. (n.d.). *A guide to the best print management software*.
https://www.gflesch.com/blog/best-print-management-software

2.  Install and Configure:

    -   Choose one of the tools to install in your environment.

> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image11.png){width="6.372341426071741in"
> height="2.602716535433071in"}

-   Follow the installation instructions provided by the tool\'s
    documentation.

-   Configure it to monitor your print services.

> ![](vertopal_477b2109c15a4e7787eb02505d423f98/media/image12.png){width="6.315321522309711in"
> height="1.4448042432195976in"}

3.  Test and Report Findings:

    -   Generate a report or dashboard from the tool.

    -   Analyze the collected data (e.g., print volume, errors, user
        activity).

Rubric

  --------------------------------------------------------------------------------------------------------------
  **Criteria**   **1                  **2 (Needs       **3                **4        **5             **Score**
                 (Unsatisfactory)**   Improvement)**   (Satisfactory)**   (Good)**   (Excellent)**   
  -------------- -------------------- ---------------- ------------------ ---------- --------------- -----------

  --------------------------------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 1: Setting Up Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Domain         No domain Domain     Domain      Domain       Domain           
  Installation**   created   created    created     configured   configured and   
                             with       correctly   well         documented       
                             errors                              thoroughly       
  ---------------- --------- ---------- ----------- ------------ ---------------- --

  ----------------------------------------------------------------------------------

  --------------------------------------------------------------------------------
  **Client       Client not  Connection   Client      Client      Client        
  Connection**   connected   attempt      connected   connected   connected and 
                             failed       but with    correctly   documented    
                                          issues                  well          
  -------------- ----------- ------------ ----------- ----------- ------------- --

  --------------------------------------------------------------------------------

  ------------------------------------------------------------------------------------
  **Print Services Role not    Role        Role        Role         Role installed, 
  Role             installed   installed   installed   installed    configured, and 
  Installation**               with issues correctly   and          documented      
                                                       configured   thoroughly      
  ---------------- ----------- ----------- ----------- ------------ --------------- --

  ------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Printer      No          Installer    Installer   Installer   Installer      
  Installer      installer   conversion   converted   converted   converted,     
  Conversion**   found       attempted    but not     and used    used, and      
                             but failed   used                    documented     
                                                                  well           
  -------------- ----------- ------------ ----------- ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Network      Printer    Deployment   Printer      Printer     Printer        
  Printer        not        failed       deployed but deployed    deployed,      
  Deployment**   deployed                not          correctly   tested, and    
                                         functional               documented     
                                                                  well           
  -------------- ---------- ------------ ------------ ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 2: Monitoring Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ------------------------------------------------------------------------------
  **Event   Event     Opened but  Logs reviewed Logs        Logs reviewed     
  Viewer    Viewer    no logs     but           reviewed    with thorough     
  Usage**   not       reviewed    superficial   with some   analysis and      
            opened                              analysis    documentation     
  --------- --------- ----------- ------------- ----------- ----------------- --

  ------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Performance   Performance   Opened but  Metrics     Metrics     Metrics       
  Monitor Usage** Monitor not   no metrics  monitored   monitored   monitored,    
                  opened        monitored   but not     with some   analyzed, and 
                                            analyzed    analysis    documented    
                                                                    thoroughly    
  --------------- ------------- ----------- ----------- ----------- ------------- --

  ----------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Print       Console   Opened but      Active jobs     Active    Active jobs   
  Management    not       functionality   viewed          jobs      viewed and    
  Console       opened    not used        superficially   viewed    documented    
  Usage**                                                 with some thoroughly    
                                                          detail                  
  ------------- --------- --------------- --------------- --------- ------------- --

  ----------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 3: Exploring Third-Party Tools**                                        
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Research   No tools     Research     Research on Research on  Research on    
  on Tools**   researched   incomplete   one tool    two tools    two tools,     
                                         completed   with some    detailed       
                                                     analysis     analysis, and  
                                                                  comparison     
  ------------ ------------ ------------ ----------- ------------ -------------- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------
  **Installation    Tool not    Installation   Tool         Tool         Tool           
  and               installed   failed         installed    installed    installed,     
  Configuration**                              but not      and          configured,    
                                               configured   configured   and documented 
                                                            with issues  thoroughly     
  ----------------- ----------- -------------- ------------ ------------ -------------- --

  ----------------------------------------------------------------------------------------

  -------------------------------------------------------------------------------
  **Reporting   No report   Report   Report      Report      Comprehensive     
  Findings**    generated   lacks    generated   generated   report with       
                            detail   but lacks   with some   thorough analysis 
                                     analysis    analysis    and documentation 
  ------------- ----------- -------- ----------- ----------- ----------------- --

  -------------------------------------------------------------------------------
