# Azure Workbooks for uberAgent: Unlocking Insights Without Splunk

Welcome to the Azure Workbooks for uberAgent project!

This repository contains a curated set of **Azure Monitor Workbooks** designed specifically for **uberAgent** users who want deep operational insights **without requiring Splunk**.

---

## 🚀 Project Purpose

This project was created by diving deep into Azure Monitor and KQL (Kusto Query Language) to answer practical questions with real data — without a formal data analyst background.

> **If you know how to ask the right question, the data already has the answer.**

The goal is to help others:
- Explore uberAgent data directly through Azure Monitor.
- Learn how tables can be joined, queried, and visualized.
- Build operational dashboards that are easy to extend.

---
## 🛠️ Install & Requirements:
> - Azure Subscription with Monitor and Log Analytics enabled.
   > - Microsoft.OperationalInsight and Microsoft.Insight required:Enable under your Azure Subscription under Resource Providers:

![image](https://github.com/user-attachments/assets/12e36a07-0c4b-4f40-8f56-4c270c7b48c1)


**uberAgent Installation Guide**
https://docs.citrix.com/en-us/uberagent/7-3-1/installation/backend/configuring-microsoft-azure-oms-log-analytics.html
- Install uberAgent on a Test Machine (Server With Apps or VDI)
- Run uberAgent_7.3.1_x64.msi
- Enable Chrome extension for browser data: https://chromewebstore.google.com/detail/uberagent/jghgedlkcoafeakcaepncnlanjkbinpb?hl=en


**Configure uberAgent to send logs to Azure Monitor (Log Analytics Workspace)**
- Copy & Paste the contents of **C:\Program Files\vast limits\uberAgent\Config Templates** to **C:\ProgramData\vastlimits\uberAgent\Configuration**
- Rename **uberAgent.conf** to **uberAgent.bak**
- Rename **uberAgent-data-volume-optimized.conf** to **uberAgent.conf**
Data volume optimized control the flow of data to not overwhelm the system as you get started.
- Edit **uberAgent.conf** file and enter your Receiver details:
  
>[Receiver]
> - Name= (Match Workspace Log name)
> - Type= OMSLogAnalytics
> - Protocol= HTTP
> - Servers= https://WORKSPACE-LOG-ID.ods.opinsights.azure.com
> - RESTToken= WORKSPACE-LOG-PRVATE-TOKEN

- Enable Windows Event Forwarding: uberAgent-ESA-eventlog-windows.conf : Uncomment Option to use.
- Restart uberAgent service after saving changes


## 📚 Included Workbooks

### **All Tables - Index**
![image](https://github.com/user-attachments/assets/3721a84e-1463-4e72-ac20-e8531497ddba)

### **Logon and Session Analysis**
- **Logon Diagnosis**
- **Logon Analysis**
- **Single User Session Details**
- **Single Machine Details**
![image](https://github.com/user-attachments/assets/5f83ae6e-f54f-450e-a863-71fcb0a06cf0)

### **Application Insights**
- **App UI Unresponsive**
- **Application Network Communications**

![image](https://github.com/user-attachments/assets/3cd66596-23d6-4307-b34a-ff9a65f1702a)

- **Application Inventory**
- **Application Performance**
- **Application Usage**
- **Application Usage Extended**
![image](https://github.com/user-attachments/assets/6e480137-37cc-4c45-ad8c-0c443518bbfe)


### **System Health Monitoring**
- **Machine Performance**
- **Machine Network Performance**
- **SMB Share Details**
- **Session Health**
![image](https://github.com/user-attachments/assets/b9c36797-d8ce-405d-865d-44e32b9bb557)
  
### **Process and Input Delay Analysis**
- **Process Startup**
- **Process Statistics**
![image](https://github.com/user-attachments/assets/47ce0275-c867-457f-b813-9ff29c530885)

### **User Statistics**
- **User Statistics Overview**
![image](https://github.com/user-attachments/assets/a4eb4c85-c735-4acc-ac11-b468cd2235b8)

### **Event ID's**
- **Event ID Diagnostic**
![image](https://github.com/user-attachments/assets/9778cc30-2708-47b4-a0b6-6adda8267656)

- ### **Web Browsing Domains & Events**
- **Chrome Browsing Details**
- Install the uberAgent Chrome Extension to collect data: https://chromewebstore.google.com/detail/uberagent/jghgedlkcoafeakcaepncnlanjkbinpb?hl=en
![image](https://github.com/user-attachments/assets/714517bc-ac55-4631-9ea1-a2be69e069e2)

- ### **ESA Security Events**
- **DNS Risk Example Charts**
![image](https://github.com/user-attachments/assets/48c80dda-d89a-4e5d-bd09-4459bb22b42f)
  

## 📈 Focus Areas

- Deep Logon Performance Troubleshooting
- Process Startup and Input Delay Timeline Analysis
- Session Health and Resource Usage
- Application Launch and Network Behavior Analysis
- System-Wide CPU, Memory, Disk, and Network Health Monitoring
- User-Based Session and Application Statistics

---

## 🛠️ How to Use

1. Import the JSON files directly into Azure Monitor Workbooks, under the Advanced Editor Option:
    > - ![{BADCE5E9-BF5E-4F7F-857E-76A5A8F71FA9}](https://github.com/user-attachments/assets/929b9523-bda2-41a1-8b4d-8412d36f0150)

2. Connect to your Log Analytics Workspace where uberAgent is sending data.
3. Enter your Azure Subscription and Resource Group Name & LogAnalytics Workspace Name in the configuration section of the files:
> - `/subscriptions/<Azure-Subscription-ID>/resourceGroups/<Resource-Group-Name>/providers/Microsoft.OperationalInsights/workspaces/<LogAnalytics-Workspace-Name>`

4. Adjust any parameters (like `TimeRange`, `Machine`, or `User`) in the workbook views.
5. Start analyzing and customizing the dashboards as needed!


## 🤝 Contributions

Contributions are welcome! Feel free to open a Pull Request if you:
- Have new workbook templates to add.
- Optimize or fix existing queries.
- Add documentation or usage examples.

Suggestions, ideas, and improvements are always appreciated!

## 🤝 Special Thanks:

- 🤝 **Amir Trujillo** – for finding my first bugs and getting them resolved on the spot!
- 🤝 **Vivek KR** – for sharing some of the original workbooks to get me started.
---

## 📬 Contact

If you have questions, feedback, or just want to connect, feel free to open an Issue or submit a Pull Request!

Let's make it easier for everyone to unlock their uberAgent data using Azure Monitor! 🚀

---

**Built out of necessity to simplify visibility for environments where Splunk licensing is cost-prohibitive.** 🎯

Licensed under GPL-3.0
