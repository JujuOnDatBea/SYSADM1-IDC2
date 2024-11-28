+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| f955829a85c2423d823a94db86c70ec4 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: TALUSIG, NIKOS A.          | DATE PERFORMED:        |          |
|                                  | 09/12/24               |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Managing Services in Linux

# Requirement: 

-   A virtual machine running Linux

![](vertopal_f955829a85c2423d823a94db86c70ec4/media/image2.png){width="4.135416666666667in"
height="1.8020833333333333in"}

Complete this lab as follows:

1.  Use the service --status-all command to list all active and inactive
    services.

List down active and inactive services in the table below. Provide five
(5) services for each column.

  -----------------------------------------------------------------------
  **Active**                             **Inactive**
  -------------------------------------- --------------------------------
  Apport                                 Bluetooth

  Cups                                   Cryptdisks

  Dbus                                   Anacron

  Gdm3                                   Plymouth

  kmod                                   rsync
  -----------------------------------------------------------------------

SS:

![](vertopal_f955829a85c2423d823a94db86c70ec4/media/image3.png){width="4.896516841644795in"
height="5.511185476815398in"}

2.  Start the Bluetooth service using the systemctl command.

Ex. sudo systemctl start httpd

![](vertopal_f955829a85c2423d823a94db86c70ec4/media/image4.png){width="4.359946412948381in"
height="1.1875in"}

3.  Check the status of the Bluetooth service. What is its status?
    **It's status is still inactive after the command**

SS:

![](vertopal_f955829a85c2423d823a94db86c70ec4/media/image5.png){width="6.011255468066492in"
height="1.8127526246719161in"}

4.  Check the status of the cups services. Since when was it running?

SS:
![](vertopal_f955829a85c2423d823a94db86c70ec4/media/image6.png){width="7.027083333333334in"
height="3.4006944444444445in"}

..

5.  Stop cups services.

6.  Verify if the service was stopped.

![](vertopal_f955829a85c2423d823a94db86c70ec4/media/image7.png){width="3.920304024496938in"
height="2.1090748031496065in"}

7.  Restart the cups services

8.  Verify if the service was restarted.

![](vertopal_f955829a85c2423d823a94db86c70ec4/media/image8.png){width="5.115297462817148in"
height="2.708711723534558in"}
