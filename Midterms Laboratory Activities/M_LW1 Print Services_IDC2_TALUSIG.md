![image](https://github.com/user-attachments/assets/3135c8dc-223c-4a1a-8d13-0203db88f578)

# SYSADM1 -- Monitoring Print Services in Windows Server 2019

# Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

![image](https://github.com/user-attachments/assets/4ab3db85-c251-41d8-89be-7a9e3a08a5ea)


2.  Connect one client to the recently created domain

![image](https://github.com/user-attachments/assets/a9478e83-946b-4662-b09a-aac3a38d69f6)

3.  Install Print Services Role:

![image](https://github.com/user-attachments/assets/ddb3ec4e-9e33-43b5-84a8-1b14dc15a8f7)


4.  Search the internet for any printer installer and convert it to iso

![image](https://github.com/user-attachments/assets/2db73d4c-4f0e-4ca1-b47c-23bbbf300829)


5.  Install and deploy it as network printer

![image](https://github.com/user-attachments/assets/acd6d440-4a3c-49a3-a14c-07a732b1efac)

![image](https://github.com/user-attachments/assets/2c44777c-7a1a-4b10-8019-e35d99d04898)


Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in
Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        Windows \> PrintService.

    -   Review logs for print jobs, errors, and warnings.

![image](https://github.com/user-attachments/assets/8bf8a5e7-b1a3-48bd-88ab-bb5de45c7637)


2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

    -   In the left pane, expand Data Collector Sets \> System.

    -   Right-click System Performance and select Start.

    -   Monitor performance metrics related to print services.

![image](https://github.com/user-attachments/assets/4740d6c6-432c-4619-9294-42cdbffffe01)

> ***Graph goes up every time the printer is used, indicating processor use.

3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

![image](https://github.com/user-attachments/assets/b4b7f859-9e5a-4021-9e8d-2cd0f5728f21)

> ***Printer currently not in use however ready to use.

Part 3: Exploring Third-Party Monitoring Tools

1.  Research at least two third-party print monitoring tools

    -   Consider factors such as features, pricing, and compatibility
        with Windows Server 2019.

![image](https://github.com/user-attachments/assets/04dcf55a-d83a-487a-8065-325599b9cc6e)


References:
PaperCut MF - System requirements \| PaperCut*. (n.d.).
https://www.papercut.com/products/mf/system-requirements/

Pttrns. (2023, September 1). Top 10 Best Print Management Software
Solutions - PTTRns. *Pttrns*.
https://www.pttrns.com/best-print-management-software-solutions/

Willoughby, B. (n.d.). *A guide to the best print management software*.
https://www.gflesch.com/blog/best-print-management-software

2.  Install and Configure:

    -   Choose one of the tools to install in your environment.

![image](https://github.com/user-attachments/assets/0899c0b6-493d-45af-9fd6-33092db0ba1c)


-   Follow the installation instructions provided by the tool\'s
    documentation.

-   Configure it to monitor your print services.

![image](https://github.com/user-attachments/assets/bfb11839-1d9f-4038-9d20-411c2aed3bac)


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
