# Lab Instructions

---

## Login to your lab

* Username	 +++LabUser+++
* Password	 +++Pa$$w0rd+++

----

## Your Microsoft 365 account and Purview account

Use the following USER credentials to login to your Microsoft 365 account:

* Username: +++AlexW@@lab.CloudCredential(WWLM365E7).TenantName+++
* Temporary Access Pass: +++@lab.Variable(TAP)+++
* Password: +++@lab.CloudCredential(WWLM365E7).UserPassword+++

---

## Data Location
Documents are located on your lab **Desktop** in a folder named **Data** and under **Sensitive Files**

===

## **Pre-Lab Exercise**

### **Upload sensitive files and apply a label**

> [!Hint] The files are located on your lab desktop in a folder named **Data** and under **Sensitive files**

---

###**Step 1**: Log into SharePoint###

1. Launch Edge and go to +++https://@lab.CloudCredential(WWLM365E7).TenantPrefix.sharepoint.com+++
2. Login with:
    1. Username: +++AlexW@@lab.CloudCredential(WWLM365E7).TenantName+++
    2. Temporary Access Pass: +++@lab.Variable(TAP)+++
3. Select **Documents** to open the site's document library
4. The Documents library will display the files and folders currently stored in the library

---

###**Step 2**: Upload files###

1. In the Documents library, select **Create or Upload** from the command bar
2. Select **Files Upload**.
3. On the left click **Desktop**, then **Data**, and **Sensitive Files**
4. Select all the files in the Sensitive files fodler
5. Select **Open** to begin the upload
6. Wait for the upload to complete

> [!Hint] You can select multiple files and upload them at the same time

---

###**Step 3**: Apply a sensitivity label to a file###

1. Click to open the file **Download Northstar Customer Migration - label as confidential** 
2. Once the file is open, at the top, Click **Sensitivity** and select **Highly Confidenial > All Employees** label
3. Close the document by closing out of the web page
4. Repeat this for the additional files

---

###**Step 4**: Input Risky Prompts

### Prompt 1:
1. Open a new tab by clicking the **+** in Edge and go to +++https://m365.cloud.microsoft+++
2. Enter: +++Summarize the customer migration information in this file /download+++
3. Select the Excel file listed **Download Northstar Customer Migration - label as confidential**
4. Press **Enter**

---

### Prompt 2:

1. Enter: +++Find me the contract value per customer on https://@lab.CloudCredential(WWLM365E7).TenantPrefix.sharepoint.com+++

---

### Prompt 3

1. Enter: +++Summarize the employee retention plan total compensation impact based on /Northstar employee+++
2. Select the Word file listed **Northstart Employee Retention Plan***

---

### Prompt 4:

1. Enter: +++Find documents that may contain Social Security Number: 378-78-7478+++

>[!Note] This will not return any matches.


## 🎉 Completed Prelab and Risky Prompts Excerise


===

### **Excercise: Remediate Oversharing: SAM**

---

**Excercise 1A: Assess Content State and Meet the SharePoint Admin Agent**
>[!Note] Blueprint pillar: Remediate Oversharing - Identify high-risk sites and content


###**Step 1:** Open the agent in the Copilot app###

1. Launch Edge and go to +++https://m365.cloud.microsoft/chat+++

4. Expand **Agents** on the left navigation and and then click **More Agents**
5. Search for +++SharePoint Admin Agent+++, Select **SharePoint Admin Agent** to open it
6. Select **Add** to add the agent.  **SharePoint Admin Agent** should open after it is added

---

###**Step 2:** Open the agent in the SharePoint admin center###

1. Open a new tab and go to +++https://admin.microsoft.com/sharepoint+++
2. Wait for the SharePoint admin center to load
3. Select the **Copilot** button in the top right corner
4. In the "Chat" box on the bottom, Select **View prompts** icon next to the **Microphone** icon on the lower corner of the **Copilot** pane to see the **Governance skills**
>[!Note] Governance Skills: Important to understand the different skills available to you to help you streamline and optimize the management of your SharePoint Online environment

---

###**Step 3:** Open the agent in Microsoft Teams###

1. Go to the **App Launcher** on the top left of the SharePoint Admin Center page (aka "the waffle")
2. Select and Open **Microsoft Teams**
3. Select the **Copilot** icon on the left hand navigation panel
4. Select **Agents** under located below the **New Chat** option > then Select **More Agents**
5. On the search box, type +++sharepoint admin agent+++ , and select the matching **SharePoint Admin Agent** option
6. Enter +++Show me storage information. Include my storage quota, storage used, and site counts+++
7. Click **Confirm** if promted, Review the answers and the follow-up prompts the agent suggests

---

## ✅ Opened the SharePoint Admin Agent in the Copilot app, the SharePoint admin center, and Teams

---

###**Step 4**: Run the Content Management Assessment###
>[!Note] A one-click scan of your SharePoint and OneDrive content that shows your Copilot readiness

1. Go to the SharePoint admin center: +++https://admin.microsoft.com/sharepoint+++
2. In the left navigation, select Advanced Management
3. Select **Start assessment**
4. The initial can scan can take up to 5 days to complete the first time it is triggered. The dashboard groups findings under Site lifecycle, Oversharing, and Storage
5. Review how many sites are affected, why they were flagged, and the recommended next step
6. In the **SharePoint Admin Agent**, enter +++Which sites were last accessed by external users?+++
7. Enter +++Draft a policy for me to address my inactive sites+++
>[!Hint] In production, rerun the assessment every 30 days to track progress

---

## ✅ Ran the Content Management Assessment 

===

### **SAM: Understanding the Reports**

---
>[!Note] Use Copilot to analyze sample SAM reports and turn them into insights you can act on

>[!Alert] **This step is critical.** The SAM reports provide visibility into potentially at-risk locations across your SharePoint and OneDrive environment, such as overshared, inactive, or ownerless sites. Understanding these reports is how you find where Copilot could surface content that should not be broadly accessible

> [!Hint] The files are located on your lab desktop in a folder named **_Data/SAM Ignite 2026 Lab Content_**

---

###**Step 1**: Open the Copilot app###

1. Open Microsoft Edge from the Windows taskbar or Start menu
2. Go to +++https://m365.cloud.microsoft/chat+++
3. Wait for **Copilot Chat** to load

---

###**Step 2**: Add the prompt and reports from the lab folder###

1. In the Copilot chat box, select **+** (Add content)
2. Select **Upload from this device**
3. Browse to the **Data** folder on your Desktop
4. Open **SAM Ignite 2026 Lab Content** within the Data folder
5. Select the prompt file and all the report files in the folder (**select all the files**)
6. Select **Open** and wait for the files to finish uploading

>[!Hint] You can select multiple files and upload them at the same time

---

###**Step 3**: Enter the following instructions into Copilot###

1. Enter +++Execute the Prompt in the SAM Analyst prompt txt file against the reports attached+++
2. Press Enter
3. Review the findings, risk areas, and recommended actions that Copilot returns
4. Note the **at-risk locations** Copilot identifies

---

## ✅ Used Copilot to analyze the SAM reports in the lab folder

### SAM: Control Content Structure with Catalog Management###
>[!Note] Blueprint pillar: Remediate Oversharing - Prioritize remediation for high-risk sites

Explore built-in categories
1. Go to the SharePoint admin center: +++https://admin.microsoft.com/sharepoint+++
2. Expand Reports and select **Catalog management**
3. Review the built-in categories: Locale, Department, User type, Preferred data location, and Information barriers segment

---

## ✅ Reviewed the built-in catalog categories
>[!Hint] To apply RCD to many sites at once, **go to Reports > Catalog management**, select the **Actions** tab, select a category, select + Add sites from a catalog group, choose a group, and select **Save**

===

###**SAM: Control Content Lifecycle**

---

>[!Note] Blueprint pillar: Meet Regulations - Improve data hygiene

Create an Inactive Site Policy
>[!Note] Create an inactive site policy named LAB-Inactive-Sites-Sim in Simulation mode

1. Go to the SharePoint admin center: +++https://admin.microsoft.com/sharepoint+++
2. Expand Policies and select **Site lifecycle management**
3. Under Inactive site policies, select **Open**
4. Select + **Create policy**
5. Review the Manage inactive sites information and select **Next**
6. On **Set policy scope**, choose **Select sites at scale** and then choose **Select all** option, then select **Next**
7. On Configure policy, set the **inactivity period**
8. Choose to notify **Site owners** and **Site admins**
9. Under the **enforcement action**, select **Do nothing** and select **Next**
10. **Name** the policy +++LAB-Inactive-Sites-Sim+++
11. Select **Simulation mode**
12. Select Finish and then **Done**
13. When the run finishes, open the policy from the Inactive site policy dashboard and download the report
14. Review Last activity date and Storage used (GB) in the **Zava_Inactive_SP_sites report** in the folder named **_Data/SAM Ignite 2026 Lab Content_**
>[!Hint] Simulation runs once and only creates a report. Active runs monthly, sends emails, and can take enforcement actions

---

## ✅ Created an inactive site policy in Simulation mode

===

###**SAM: Control Content Oversharing and Access**

---

>[!Note] Blueprint pillars: Remediate Oversharing and Set up Guardrails

>[!Hint] The five common causes of Copilot oversharing are: site privacy set to Public, default sharing set to Everyone, broken permission inheritance, use of Everyone except external users (EEEU), and sites or files without sensitivity labels

---

## Explore Data Access Governance Reports
###**Step 1:** Review the site permissions report###

1. Go to the SharePoint admin center: +++https://admin.microsoft.com/sharepoint+++
2. Expand Reports and select **Data access governance**
3. Under **Site permissions across your organization**, select **View reports**
>[!Note] The first site permissions report can take up to 5 days. This is one of the key reports that will run when you start the assessment

---

###**Step 2:** Review the special sharepoint groups reports###
1. Go back to the **Data access governance reports**
2. Under **Sites and files shared via special SharePoint groups**, select **view reports**
3. Note that you need a new role assignment as **SharePoint Advanced Management admin** role in order to view and generate reports
>[!Note] SharePoint Advanced Management admin role is needed to View names, paths, and URLs of files, folders, libraries, documents, and lists within SharePoint sites, without accessing file or item content and to remove permissions from files, folders, libraries, documents, and lists within SharePoint sites

---

###**Step 3:** Apply Restricted Content Discovery (RCD)###
>[!Note] Hide a high-risk site from Copilot and organization-wide search while it is cleaned up. Permissions do not change

1. In the **SharePoint admin center**, expand Sites and select **Active sites**
2. Select the **Group for Answers in Viva Enage**
3. Select the **Settings** tab
4. Turn **Restrict content discovery** On
5. Select **Save**
6. Confirm that a Restricted tag appears on the site
>[!Hint] To apply RCD to many sites at once, go to Reports > Catalog management, select the Actions tab, select a category, select + Add sites from a catalog group, choose a group, and select **Save**

---

###**Step 4:** Monitor agent access to SharePoint and OneDrive###
>[!Note] Agent access insights use the M365 unified audit logs to track how agent access SharePoint and Onedrive

1. In the **SharePoint admin center**, expand Reports and select **Agent insights**
2. Under **Agent Access**, select **View reports**
3. Go ahead and **Enable data collection**

>[!Hint] Once enabled, the reports can be generated 24 hours later and contain data from the point of collection

---

### ✅ Applied Restricted Content Discovery to a high-risk site

## 🎉 End of the SharePoint Advanced Management Lab

===

###**Excersie 2**: Setup Guardrails

---

### **Purview DSPM** - Data Risk Assessment
1. Launch Edge and go to +++https://purview.microsoft.com+++
2. If prompted, login with the same username and password used previously
3. If a **Welcome** pop-up appears, click **Get Started**
4. Click **Solutions** on the left navigation rail
5. Select **DSPM**
6. When first opening **DSPM** you may see a pop-up
7. Select **Get Started** on the **DSPM and DSPM for AI Unified in one solution** and Select **Start setup**
8. Once setup has been completed, click the **Close** button to continue to the next steps
9. Expand **Discovery** on the left pane and select **Data Risk Assessments**
10. Scroll down and select **Create custom assessment** 
11. Name the assessment +++Ignite 2026+++
12. Select **Next** on **Select scan level** (do **not** click on the "Item-level" checkbox)
13. Select **Next** on Add users. Keep the default to **ALL** and select **Next**
14. Select **Sharepoint** and **OneDrive** on data sources to assess and then select **Next**
15. Click **Save and run** and then **Done**

---

### ✅ Created a Custom Data Risk Assessment report

===

### **Purview Information Protection** - Client Side Auto-Label

>[!Note] Automatically detects and applies a sensitivity label to files when being created or edited

---

1. Click **Solutions** on the left navigation rail
2. Select **Information Protection**
3. Select **Sensitivity Labels**
4. Expand **Highly Confidential** and select **All Employees**
5. Select **Edit Label**
6. Continue selecting **Next**, keeping all defaults until the **Auto-labeling for files and emails** section
7. Scroll down. Under the **Detect content that matches these conditions**, Select **Add** and then **Sensitive info types**
9. Search and click in the checkbox for the below sensitive information types:
   - +++Credit Card Number+++
   - +++U.S. Social Security Number (SSN)+++
   - +++U.S. / U.K. Passport+++
   - +++ITIN+++
9. Once they are all selected, click **Add**
10. Where it says **"Group operator"** change the option to **Any of these**
11. Confirm that Credit Card has **1** for the instance count instead of **10**
12. Scroll down to - **When content matches these conditions** and change from **Recommend that users apply the label** to **Automatically apply the label**
13. Continue clicking **Next** to the end and **Save Label** and then **Done**

---

### ✅ Created a Client-Side Auto Label Policy

===

### **Purview  Information Protection** - Automatic Labeling for Files at Rest

>[!Note] Automatically detects and applies a sensitivity label to files at rest that matches the Sensitive information below

---

1. Click **Solutions** on the left navigation rail
2. Select **Information Protection**.
3. Expand **Policies** and Select **Auto-labeling policies**
4. Scroll down and select **Create auto-labeling policy** and **Automatically apply labels only**
5. In the **Categories** section, select **Custom** and then **Custom Policy** and click **Next**
6. Name the Policy +++Sensitive US Financial or Identity Information+++ and Select **Next**
7. Select **Choose a label** select the **Highly Confidential/All Employees** and then **Add** and select **Next**
8. Select **Next** until you get to the **Choose locations where you want to apply the label**
9. On Locations, Select **Sharepoint Sites** and **OneDrive Accounts**. Select **Next**
10. Select **Next** on **Set up common or advanced rules**
11. Click on **New Rules** and Name the rule +++Sensitive US Financial or Identity Information+++ 
12. Under **Conditions** Select **Add a condition** and **Content Contains**. Then Select **Add** and then **Sensitive information Types**
13. Search and click in the checkbox for the below sensitive information types:
   - +++Credit Card Number+++
   - +++U.S. Social Security Number (SSN)+++
   - +++U.S. / U.K. Passport+++
   - +++ITIN+++
14. Click **Add** when all (4) have been selected
15. Select **Save** then continuing clicking **Next** until your reach the page **Decide if you want to test out the policy now or later**
16. Leave the default setting - **Run policy in simulation Mode** and click **Next**
17. Then Click **Create Policy** and then the **Done** button once complete

----

### ✅ Created an Service-Side Auto Labeling Policy

===

### **Purview Data Loss Prevention** - Microsoft Copilot document processing


>[!Note] Create a DLP Policy to prevent copilot processing of Highly Confidential documents

---
1. Click **Solutions** on the left navigation rail
2. Select **Data Loss Prevention** and select **Policies**
3. Click **Create Policy** and select **Enterprise applications & devices**
4. In the **Categories** section, select **Custom** then **Custom Policy** and **Next**
5. Rename the policy +++Copilot - Prevent Document Processing+++ and select **Next**
6. Select **Next** on the **Assign admin units** page
7. Scroll down on **Choose where to apply the policy**, select **Microsoft Copilot, Copilot Chat and Copilot Cowork** and then select **Next**
8. Select **Next** on Define Policy settings
9. Click **Create Rule** andname the rule +++Copilot - Prevent Document Processing+++
10. Click **Add Condition** select **Content Contains** then Add **Sensitivity Labels** and select the **Highly Confidential/All Employees** label
11. Under **Actions** click **Add an Action**, select **Restrict Copilot from processing content** and check **Accessing knowledge sources**
12. Under **User notifications** select **Policy Tips**
13. Leave the rest with the default settings and click **Save**
14. Click **Next** and then Select **Turn the policy on immediately** and select **Next** and **Submit**

---

### ✅ DLP policy created to exclude Highly Confidential items from Copilot processing

===

### **Purview Data Loss Prevention** - Microsoft Copilot Prompts

>[!Note] Create a DLP Policy to prevent prompting of Sensitive Information

---

1. Click **Solutions** on the left navigation rail
2. Select **Data Loss Prevention** and select **Policies**
3. Click **Create Policy** and select **Enterprise applications & devices**
4. Under **Categories** select **Custom** then **Custom Policy** and **Next**
5. Rename the policy +++Copilot - Prevent Sensitive Prompts+++ and select **Next**
6. Select **Next** on the **Assign admin units** page
7. On **Choose where to apply the policy**, scroll down and select **Microsoft Copilot, Copilot Chat and Copilot Cowork** and select **Next**
8. Select **Next** on Define Policy settings
9. Click **Create Rule** and name the rule +++Copilot - Prevent Sensitive Prompts+++
10. Click **Add Condition** select **Content Contains** then select **Add** and then **Sensitive Information Types**
11. Search and click in the box for the below sensitive information types:
   - +++Credit Card Number+++
   - +++U.S. Social Security Number (SSN)+++
   - +++U.S. / U.K. Passport+++
   - +++ITIN+++
12. Under **Actions** click **Add an Action** and select **Restrict Copilot from processing content** and then check **Processing prompts**
13. Under **User notifications** select **Policy Tips**
14. Leave the rest with the default settings and click **Save**
15. Click **Next** then Select **Turn the policy on immediately** and select **Next** and **Submit**
16. Click **Done**

---

### ✅ DLP policy created to exclude Sensitive information from Prompts. You should see the two new policies that were just created

===

### **Purview - Communication Compliance Policy**

>[!Note] Create a Communication Compliance policy to detect **Risky prompts with Copilot**

---

1. In Purview, select **Solutions > Communication Compliance**
2. Click **Policies**
3. Click **Create Policy** and select **Custom Policy**
4. Name policy: +++**Risky Prompts with Copilot**+++ and click **Next**
5. Click **Next** on the Admin Units
6. On the **Users and Reviewers** select **All Users**. Under **Reviewers**, type +++Alex+++, select **Alex Wilber** and then click the **Next**
7. On **Choose Locations to Detect**, unselect **Exchange**, **Teams**, and **Viva Engage**
8. Select **Generative AI** and ensure that **M365 Copilot** and **Microsoft Copilot Studio** are selected. Click **Add** and then click on **Next**
9. Scroll down and select **Add condition**, and then select **Content contains sensitive info types** 
10. Under **Conditions** select **Add condition** and then **Sensitive info types**
11. Search and click in the box for the below sensitive information types:
   - +++Credit Card Number+++
   - +++U.S. Social Security Number (SSN)+++
   - +++U.S. / U.K. Passport+++
   - +++ITIN+++
12. Select **Add condition** again and then **Content contains trainable classifiers** and 
13. Select **Add** then click on **Trainable Classifiers**
14. Search and click in the box for the below trainable classifiers:
   - +++Prompt Shields+++
   - +++Protected Materials+++
15. Change the **Review percentage** to **100%** by draging the selector all the way to the right
16. Scroll back up and change **And** to **Or**
17. Scroll all the way down and click **Next**
18. Review and finish by clicking **Create policy**. Click **Done**
19. Once back on the **Communicaton Compliance page**, click **Refresh**

---

### ✅ A Communication Compliance policy has been created

===

### **Purview - Insider Risk Management**: Risky AI Usage Policy

>[!Note] Create a IRM policy to detect user risky behaviour

---

1. Navigate to **Solutions > Insider Risk Management > Policies**
2. Click **Create policy**, 
3. Select **Custom policy**
4. Select **Risky AI usage** template, click **Next**
5. Name your policy +++Ignite 2026 - Risky AI Usage+++ and click **Next**
6. On **Choose users, groups & adaptive scopes**, select **All users, groups, and adaptive scopes**. Click **Next**
7. On **Exclude users and groups (optional)** click **Next**
8. On **Decide whether to prioritize content** select **I don't want to prioritize content right now**. click **Next**
9. Select **Inappropriate messages detected by communication compliance** and select **Microsoft 365 Copilot interactions** from the drop down
10. Scroll down and expand the section **Risky or sensitive content in Microsoft Copilot Experiences, Enterprise AI apps and web versions of other AI apps.**

>[!Note] These will be off by default

11. Click the **down arrow** and click **Turn on indicators** and on the pop-up windows Select **Turn on all**
12. Now select the **Select All** option and click **Next**
13. Click **Next** 
14. On the **Indicators** section expand **Generative AI apps** indicators, expand **Microsoft Copilot experiences (2/2 selected) and ensure both are selected. Click **Next**
16. Click **Next** on detection options, leaving all selected.
17. Click **Next** on threshold type for indicators
18. Click **Submit** and then **Done**

---  

### ✅ IRM Policy to identify Risky AI Usage successfully created
## 🎉 End of the setup Purview Guardrails


===

### **Purview - Audit Log**

### Excercise 3: Meet Regulations

>[!Note] Search for Copilot Interactions

---

1. Launch Edge and go to +++https://Purview.microsoft.com+++
2. Navigate to **Solutions > Audit**
3. Change the Date Range to **Nov. 16, 2026** to **Nov. 17, 2026**
4. Under **Activities - friendly names** 
5. Type +++Interacted with copilot+++ and select **Interacted with Copilot** under Copilot activities
6. Select **Search**

>[!Note] This search will take about 5 to 10 minutes to complete. Please continue to the next steps with eDiscovery and return. If the results are blank, rerun the search

7. Click on the Search that was created and review the **Interacted with Copilot** activity

>[!Note] The Unified Audit Log search will not contain the prompts and response. It will include information about prompt and this information is able to be surfaced in a SIEM solution

---

### ✅ Unified Audit log search has been created

===

### **Purview - eDiscovery** Investigate Copilot Conversations

>[!Note] Search for Copilot Prompts and Response conversations

---

1. Navigate to **Solutions > eDiscovery**
2. Select **Cases**
3. Select **Create Case**
4. Name the case +++Copilot Conversations+++ and click **Create**
5. Click **create a search** and name it +++Copilot Conversations+++ and click **Create**
6. In the **Data Source** section, Click **Add Source** and search for +++Alex+++ and Select **Search** 
7. Select **Alex Wilber** and click **Save and close**

>[!Note] AI interactions are stored within the end users mailbox

8. Under **Condition Builder** use the trash can icon to remove the **Keywords** condition
9. Select **Add Conditions** and select **Item Class** and and in the blank box next to **Contains any of** enter +++Copilot activity+++ and select it from the drop down list
10. Next, click **Add to Review Set** on the upper right
11. On the Flyout pane. Name the review set name +++Copilot Interactions+++. Click **Add to review set** at the bottom

>[!Note] This search will take about 5 to 10 minutes to complete


---

### ✅ Create an eDiscovery case and review AI Prompts and Responses

===

### **Purview - Data Lifecycle Management**

>[!Note] Create a Data Lifecycle Management Policy **Keep then delete Copilot and Agent Interactions - 90 Days**.

---

1. In Purview, select **Solutions > Data Lifecycle Management**
2. Expand **Policies** and select **Retention Policies**
3. Click **New Retention Policy**
4. Name the policy: +++Keep then delete Copilot and Agent Interactions - 90 days+++ Click **Next**
5. Select **Next** on the **Policy Scope page**
6. On **Choose the type of retetion policy to create** page Choose **Static**, Click **Next**
7. Scroll down to **Microsoft Copilot experiences** and toggle **on**. Click **Next**
8. Under **Retain items for a specific period** click the dropdown and choose **Custom**
9. Change the retention period for **3 months**
10. Under **At the end of the retention period**, choose **Delete Items automatically**. Click **Next**
11. Click **Submit**. Click **Done**

---

## ✅ A Data Lifecycle Management policy was created to retain Copilot conversations for 90 days and then permanently delete them

===

### **Compliance Manager**: Assess Alignment to AI Regulations

>[!Note] Create a Compliance Manager Assessment **EU Artificial Intelligence Act**

---

1. In Purview, select **Solutions > Compliance Manager**
2. Select **Regulations**
3. Scroll down to **Premium AI templates** and click on **EU Artificial Intelligence Act**
4. On the Controls tab, expand **Chapter II Prohibited AI Practices.**
    1. Click the first *Prohibited AI practices* row
    2. Observe the actions needed to comply with this control.
    3. Click on **Create customized DLP policies for personally identifiable information (PII)** in the Improvement Actions tab
    4. Review the detailed steps outlining how to accomplish this requirement 
    5. Click back to **Prohibited AI Practices** in the breadcrumb area at the top
    6. Click on Microsoft Actions and observe the controls that Microsoft has taken care of as the SaaS provider
5. In the left hand navigation, select **Assessments**
6. Click **Add Assessment**
7. Click **Select Regulation**, In the search box, type +++EU artificial intelligence act+++ press enter and then select the regulation from the list
8. Click **Save**, Click **Next**
9. On the **Add name and group** Give the the assessment a name - +++EU artificial intelligence act+++ and select **Next**
10. On Select Services, click **Next**
11. Click **Create Assessment**, Click **Done**
12. Click **Your Improvement Actions**. and search +++Apply sensitivity labels+++ to protect personal data review the information provided to allow tracking toward goals

---

### ✅ Compliance Manager assessment created to track adherence to EU AI Act.

## 🎉 End of the Regulation setup and Lab

===

### **Purview Testing**

---

###**Step 1**: Auto-Labeling

1. Launch Edge and go to: +++https://word.cloud.microsoft+++
2. Click **Create blank Document**
3. Input sample data:
- +++**Social Security Number: 378-78-7478**+++

>[!Note] You should see the Label automatically change to **Highly Confidential/All Employees**

4. Name the document: +++**Sensitive Information**+++ by clicking on **Document** on the top left corner
5. Close the file

## ✅ Successfully automatically applied a sensitivity label to a file

---

## Testing DLP Policies:

###**Step 2**: Input Risky Prompts

### Prompt 1:

1. Launch Edge and go to +++https://m365.cloud.microsoft/+++
2. Enter: +++Summarize the customer migration information in this file /download+++
3. Select the Excel file listed **Download Northstar Customer Migration - label as confidential**
4. Press **Enter**

---

### Prompt 2:

1. Enter: +++Find me the contract value per customer on https://@lab.CloudCredential(WWLM365E7).TenantPrefix.sharepoint.com+++
2. Press **Enter**

---

### Prompt 3:

1. Enter: +++Summarize the employee retention plan total compensation impact based on https://@lab.CloudCredential(WWLM365E7).TenantPrefix.sharepoint.com+++
2. Press **Enter**

---

### Prompt 4:

1. Enter: +++Find documents that may contain Social Security Number: 378-78-7478+++
2. Press **Enter**

---
## ✅ Successfully blocked documents with Highly Sensitive data and Risky Prompts

## 🎉 PREL39: Ready, Secure, Govern Microsoft Copilot Chat & Cowork Workshop is Completed 🎉!!!


