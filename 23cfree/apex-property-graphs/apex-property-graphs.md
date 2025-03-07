# Bank Transfers Graph Example with SQL/PGQ in 23c

## Introduction

In this lab you will query the newly create graph (that is, `bank_graph`) in PGQL paragraphs.

Estimated Time: 30 minutes.

Watch the video below for a quick walk through of the lab.

<!-- update video link. Previous iteration: [](youtube:XnE1yw2k5IU) -->

### Objectives
Learn how to:
- Use APEX and PGQL to query, analyze, and visualize a graph.

### Prerequisites
This lab assumes:
- The graph user exists
- You have logged into APEX
- The graph bank_graph exists

*See Lab \_\_ for instructions to complete these prerequisites.*

### Tables are
| Name | Null? | Type |
| ------- |:--------:| --------------:|
| ACCT_ID | NOT NULL | NUMBER|
| NAME |  | VARCHAR2(4000) |
| BALANCE |  | NUMBER |
{: title="ACCOUNTS"}

| Name | Null? | Type |
| ------- |:--------:| --------------:|
| TXN_ID | NOT NULL | NUMBER|
| SRC\_ACCT\_ID |  | NUMBER |
| DST\_ACCT\_ID |  | NUMBER |
| DESCRIPTION |  | VARCHAR2(4000) |
| AMOUNT |  | NUMBER |
{: title="TRANSFERS"}

## Task 1 : Import APEX app to visualize queries

1. Open Activities -> Google Chrome

    ![Open Google Chrome](images/activities-chrome.png)


2. Go to this URL and wait for the screen to load.
    ```
    <copy>
    http://localhost:8080/ords/apex_admin
    </copy>
    ```

    ![URL login screen](images/admin-services.png)


3. Login as ADMIN with your password.

    ![Login using credentials](images/login-details.png)

4. You can see the welcome screen for APEX now. 

    ![Welcome screen after login](images/welcome-to-apex.png)

5. Click create workspace

    ![workspace welcome screen](images/workspace-name.png)

6. Name the workspace 'graph' and click Next

    ![enter graph for the workspace](images/graph-next.png)

7. Set reuse existing schema to Yes. Click the menu icon next to schema name and select HOL23C. Set your schema password to whatever but write it down. Leave the default for space quota.

    ![Schema information input changes](images/schema-info.png)

8. Admin username: admin, password: Welcome123#, email: your email.

    ![admin password email input](images/admin-password-email.png)

9. Review the output then click Create workspace.

    ![Create workspace](images/create-workspace.png)

10. Success! Now click done.

    ![completetion screen](images/done.png)


## Task 2 : Import app

1. In the upper right corner, click the admin icon then click sign out.
    ![sign out from admin](images/logout.png)


2.  Log back in as the admin info you just created along with the workspace name as graph.
    ![log back in](images/log-back-in.png)


3. Change password
    ![password change](images/change-password.png)


4. App Builder -> Import

    ![Import from app builder](images/app-builder-import.png)

5. Click to add a file to open for import. Go to Home -> example -> graph -> f106.sql and open that file. Leave the defaults and click next.

    ![Import f106 sql file](images/f106-import.png)

6. Click next.
    
7.  Leave all defaults, except check Reuse app 106 from file under Install Application and click Install Application. 

    ![Install the application](images/install-application.png)

8.  Click run application

    ![Run the application](images/run-application.png)



9.  Login

    ![Log back in](images/login-final.png)


10. Click property graph queries with pgq box
    ![Property graph queries selection](images/property-graph-queries.png)
    
11. Scroll through output.
    ![Final scroll through the output](images/scroll-through.png)

12. You have now completed this lab.