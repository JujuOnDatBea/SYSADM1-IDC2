+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 5f3798d5a7c540eeae411d25a06e7e1a |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: TALUSIG, NIKOS A.          | DATE PERFORMED:        | /50      |
|                                  | 10/10/24               |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 10/10/24               |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Setting Up Webserver

# Requirement: 

-   A virtual machine running Linux and Windows OS

    Task Instructions:

1.  Install IIS by adding it as a role, select necessary features,
    include monitoring tools

    ![](vertopal_5f3798d5a7c540eeae411d25a06e7e1a/media/image2.png){width="3.1566907261592303in"
    height="2.802474846894138in"}

2.  Create a website by opening IIS Manager

    -   Right-click on the server's name and select Internet Information
        Services Manager.

    -   Right-click on Sites and select Add Website.

    -   Enter a name, description, physical path (where your website
        files will reside), IP address, port, and host name.

        ![](vertopal_5f3798d5a7c540eeae411d25a06e7e1a/media/image3.png){width="4.681615266841645in"
        height="4.491176727909012in"}

3.  Configure the Website:

    -   Right-click on your website and select Edit.

    -   Set the Default Document to the name of your main HTML file
        \>default.html

        ![](vertopal_5f3798d5a7c540eeae411d25a06e7e1a/media/image4.png){width="3.708850612423447in"
        height="1.6252263779527558in"}

    -   Configure other settings as needed (e.g., SSL certificates,
        authentication)

        ![](vertopal_5f3798d5a7c540eeae411d25a06e7e1a/media/image5.png){width="4.552718722659668in"
        height="2.239896106736658in"}

        ![](vertopal_5f3798d5a7c540eeae411d25a06e7e1a/media/image6.png){width="5.130370734908136in"
        height="1.55751312335958in"}

4.  Create a Web Page:

    -   Create an HTML file in the physical path you specified.

        ![](vertopal_5f3798d5a7c540eeae411d25a06e7e1a/media/image7.png){width="3.652083333333333in"
        height="1.52377624671916in"}

    -   Save it as default.html or your preferred name.

        ![](vertopal_5f3798d5a7c540eeae411d25a06e7e1a/media/image8.png){width="5.89208552055993in"
        height="1.9453969816272967in"}

        ![](vertopal_5f3798d5a7c540eeae411d25a06e7e1a/media/image9.png){width="5.302444225721785in"
        height="1.79001312335958in"}

5.  Test the Web Server:

    -   Open a web browser and enter the URL of your website (e.g.,
        http://localhost).

    -   You should see your web page displayed.

        ![](vertopal_5f3798d5a7c540eeae411d25a06e7e1a/media/image10.png){width="4.1047397200349955in"
        height="3.0108366141732286in"}

        ![](vertopal_5f3798d5a7c540eeae411d25a06e7e1a/media/image11.png){width="4.083903105861768in"
        height="3.0108366141732286in"}

        Grading Rubric

  ------------------------------------------------------------------------------
  **Criteria**      **Points**   **Description**
  ----------------- ------------ -----------------------------------------------
  Web Server        15           Correctly installs IIS or another web server on
  Installation                   the virtual machine.

  Website           15           Successfully configures the website with the
  Configuration                  correct physical path, IP address, port, and
                                 default document.

  Successful Access 15           Successfully accesses the web page from the
                                 client computer using the correct URL.

  Troubleshooting   15           Demonstrates ability to troubleshoot common
                                 issues, such as network connectivity problems
                                 or configuration errors.

  Documentation     10           Provides clear and concise documentation of the
                                 installation, configuration, and testing
                                 process.

  Total             /70          
  ------------------------------------------------------------------------------
