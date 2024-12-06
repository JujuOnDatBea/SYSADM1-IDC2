![image](https://github.com/user-attachments/assets/4d638f03-44f3-478b-98aa-b52f9d7a12c9)


# SYSADM1 -- Kerberos Lab Activity: A step-by-step Guide

**Objective:**

Set up a basic Kerberos authentication system to understand how Kerberos
manages secure logins through ticket-based access.

**Setup Requirements:**

-   Two VMs in Oracle VM, both running a Linux distribution like Ubuntu
    or CentOS.

-   VM1: Kerberos Server

-   VM2: Kerberos Client

**Step 1: Initial Setup and Package Installation**

1.  **Update Packages on Both VMs:**

    -   Open a terminal on each VM and run:

> bash
> sudo apt update && sudo apt upgrade --y

![image](https://github.com/user-attachments/assets/45086b5d-cba8-4179-ba05-dd2758c3722c)


2.  **Install Kerberos Server Packages on VM1 (Kerberos Server):**

    -   In VM1, install the Kerberos Key Distribution Center (KDC) and
        admin server:

> bash
> sudo apt install krb5-kdc krb5-admin-server --y

![image](https://github.com/user-attachments/assets/1986e1cd-a375-4af8-815e-33f6bc5bd91d)


3.  **Install Kerberos Client Package on VM2 (Kerberos Client):**

    -   In VM2, install the Kerberos client software:

> bash
> sudo apt install krb5-user --y

![image](https://github.com/user-attachments/assets/bb9c8b3b-e884-4019-98a6-50ffbd3d6c05)


-   During installation, when prompted, enter the Kerberos realm you
    plan to set up, e.g., MYLAB.LOCAL.

**Step 2: Configure the Kerberos Server (VM1)**

1.  **Edit the Kerberos Configuration File:**

    -   Open /etc/krb5.conf for editing:

> bash
> sudo nano /etc/krb5.conf

-   Set the realm as MYLAB.LOCAL. You should also specify the KDC and
    admin server as VM1's hostname or IP address:

> ini
> [libdefaults]
>     default_realm = MYLAB.LOCAL
> [realms]
>    MYLAB.LOCAL = {
>        kdc = <VM1_IP_or_hostname>
>        admin_server = <VM1_IP_or_hostname>
>    }

![image](https://github.com/user-attachments/assets/4f6f7bf9-0d00-4703-a28e-c57b3d9a5913)


-   Save and close the file (Ctrl+X, then Y, and Enter to confirm).

2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

> bash
> sudo krb5_newrealm

-   You will be prompted to set a password for the Kerberos database.

![image](https://github.com/user-attachments/assets/8a950812-f204-4ff3-9c86-24447bc60804)


3.  **Start and Enable the Kerberos Services:**

    -   Start the KDC and admin server, and ensure they start
        automatically on boot:
      
> bash
> sudo systemctl start krb5-kdc
> sudo systemctl start krb5-admin-server
> sudo systemctl enable krb5-kdc
> sudo systemctl enable krb5-admin-server

![image](https://github.com/user-attachments/assets/fbe16339-23a3-4c7d-808a-752c06c23f88)


**Step 3: Set Up a Kerberos User Principal**

1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        realm:

> bash
> sudo kadmin.local -q "addprinc testuser@MYLAB.LOCAL"

-   Set a password for testuser.

![image](https://github.com/user-attachments/assets/d8db3720-7493-4b62-ab9f-db172bc54a81)


2.  **Verify the User Principal:**

    -   To confirm the principal is created, list all principals:

> bash
> sudo kadmin.local -q "listprincs"

![image](https://github.com/user-attachments/assets/0364c96d-0c93-4fc9-a139-37e1021123bf)


**Step 4: Configure the Kerberos Client (VM2)**

1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

> bash
> sudo nano /etc/krb5.conf

![image](https://github.com/user-attachments/assets/e5675ecc-99ac-49ce-bfc2-cfd0552d74c8)


-   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    server on VM1. The configuration should match what you set on VM1.

**Step 5: Test Kerberos Authentication**

1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

> bash
> kinit <testuser@MYLAB.LOCAL>

![image](https://github.com/user-attachments/assets/16d2849e-b1e9-488f-a64e-c5c2789ec3ab)


-   Enter the password you set for testuser.

2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        tickets:

> bash
> klist

![image](https://github.com/user-attachments/assets/6f82ddc8-9a82-4083-8704-4cb75e3d1ad2)


-   You should see details about the ticket, such as the principal and
    expiration time, confirming successful Kerberos authentication.
