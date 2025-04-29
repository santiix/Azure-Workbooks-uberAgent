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

## 📚 Included Workbooks

### **Logon and Session Analysis**
- **Logon Diagnosis**
- **Single User Session Details**
- **Single Machine Details**

### **Application Insights**
- **App UI Unresponsive**
- **Application Network Communications**
- **Application Inventory**
- **Application Performance**
- **Application Usage**

### **System Health Monitoring**
- **Machine Performance**
- **Machine Network Performance**

### **Process and Input Delay Analysis**
- **Process Startup**
- **Process Statistics**

### **User Statistics**
- **User Statistics Overview**

---

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
> - "/subscriptions/<Azure-Subscription-ID>/resourceGroups/<Resource-Group-Name>/providers/Microsoft.OperationalInsights/workspaces/<LogAnalytics-Workspace-Name>"

4. Adjust any parameters (like `TimeRange`, `Machine`, or `User`) in the workbook views.
5. Start analyzing and customizing the dashboards as needed!

> **Requirements:**
> - Azure Subscription with Monitor and Log Analytics enabled.
   > - Microsoft.OperationalInsight and Microsoft.Insight required:Enable under your Azure Subscription under Resource Providers:
> - ![image](https://github.com/user-attachments/assets/12e36a07-0c4b-4f40-8f56-4c270c7b48c1)


> - uberAgent configured to send logs to Azure Monitor (Log Analytics Workspace).
> - uberAgent Installation Guide
https://docs.citrix.com/en-us/uberagent/7-3-1/installation/backend/configuring-microsoft-azure-oms-log-analytics.html

## 🤝 Contributions

Contributions are welcome! Feel free to open a Pull Request if you:
- Have new workbook templates to add.
- Optimize or fix existing queries.
- Add documentation or usage examples.

Suggestions, ideas, and improvements are always appreciated!

## 🤝 Special Thanks:

🤝 - Amir Trujillo for finding my first bugs and gettin them resolved on the spot!
🤝 - Vivek KR for sharing some of the original workbooks to get me started.
---

## 📬 Contact

If you have questions, feedback, or just want to connect, feel free to open an Issue or submit a Pull Request!

Let's make it easier for everyone to unlock their uberAgent data using Azure Monitor! 🚀

---

**Built out of necessity to simplify visibility for environments where Splunk licensing is cost-prohibitive.** 🎯

Licensed under GPL-3.0
