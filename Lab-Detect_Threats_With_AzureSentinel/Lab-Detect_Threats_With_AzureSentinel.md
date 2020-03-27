# Detect threats with Azure Sentinel

## Table of Contents

[Overview](#overview)

[Pre-Requisites](#pre-requisites)

[Exercise 1: Creating Azure Sentinel workspace](#exercise-1-creating-azure-sentinel-workspace)

[Exercise 2: Detect threats out-of-the-box](#exercise-2-detect-threats-out-of-the-box)

[Exercise 3: Visualize and monitor your data](#exercise-3-visualize-and-monitor-your-data)

[Exercise 4: Investigate incidents with Azure Sentinel](#exercise-4-investigate-incidents-with-azure-sentinel)

[Exercise 5: Set up automated threat responses in Azure Sentinel](#exercise-5-set-up-automated-threat-responses-in-azure-sentinel)

## Overview

This lab presents use cases to get started using Azure Sentinel. See and stop threats before they cause harm, with SIEM reinvented for a modern world.

### Scenario and Objective

After completing this lab, you will be able to:

* Create Azure Sentinel workspace

* Detect threats out-of-the-box

* Visualize and monitor your data

* Investigate incidents with Azure Sentinel

* Set up automated threat responses in Azure Sentinel

## Pre-Requisites

* Azure Portal

## Exercise 1: Creating Azure Sentinel workspace

1. Using the Chrome browser, Login to Azure Portal with the below details:

 * **Azure login_ID:** `{{azure-login-id}}` <br>

 * **Azure login_Password:** `{{azure-login-password}}`

![alt text](https://qloudableassets.blob.core.windows.net/microsoft-learning/Az103/Lab4%20-%20Configure%20Azure%20DNS/portal1.png?st=2019-09-05T09%3A42%3A02Z&se=2022-09-06T09%3A42%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=igNCmxkgy8jEIHJZ6PyjEF9C7%2F%2BIhh1f4y6NOSGhtXM%3D)

![alt text](https://qloudableassets.blob.core.windows.net/microsoft-learning/Az103/Lab4%20-%20Configure%20Azure%20DNS/portal2.png?st=2019-09-05T09%3A42%3A23Z&se=2022-09-06T09%3A42%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=ZZUZvHB8wU%2B4qcb5%2FEgwvsWym5BZwrxY0ra%2B8RRjfcg%3D)

![alt text](https://qloudableassets.blob.core.windows.net/microsoft-learning/Az103/Lab4%20-%20Configure%20Azure%20DNS/portal3.png?st=2019-09-05T09%3A42%3A40Z&se=2022-09-06T09%3A42%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=wFt6UDhop3gbP%2BwBKG2NA%2FD3u22gYcMYduh8uPmXVZ4%3D)

![alt text](https://qloudableassets.blob.core.windows.net/microsoft-learning/Az103/Lab4%20-%20Configure%20Azure%20DNS/portal4.png?st=2019-09-05T09%3A42%3A55Z&se=2022-09-06T09%3A42%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=gq%2F0iEKqyyV%2F%2FkE%2Fm4OcKfQ4hBKHYowLNbrIUVdSqak%3D)

2. Choose **+Create a resource**, then search for Azure Sentinel in search box and Select **Azure Sentinel**.

![alt text](https://qloudableassets.blob.core.windows.net/azure-sentinel/Images/1.PNG?st=2020-03-27T08%3A30%3A39Z&se=2023-03-28T08%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=fXFmtQnh1zR1OuRkdCKkLEmrA8WaC0VJbHV0pf697Mg%3D)

![alt text](https://qloudableassets.blob.core.windows.net/azure-sentinel/Images/2.png?st=2020-03-27T08%3A30%3A39Z&se=2023-03-28T08%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=fXFmtQnh1zR1OuRkdCKkLEmrA8WaC0VJbHV0pf697Mg%3D)

3. Click on **Create**.

![alt text](https://qloudableassets.blob.core.windows.net/azure-sentinel/Images/3.PNG?st=2020-03-27T08%3A30%3A39Z&se=2023-03-28T08%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=fXFmtQnh1zR1OuRkdCKkLEmrA8WaC0VJbHV0pf697Mg%3D)

4. Click on **+ Add**.

![alt text](https://qloudableassets.blob.core.windows.net/azure-sentinel/Images/4.PNG?st=2020-03-27T08%3A30%3A39Z&se=2023-03-28T08%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=fXFmtQnh1zR1OuRkdCKkLEmrA8WaC0VJbHV0pf697Mg%3D)

5. Then click on **Create a new workspace**.

![alt text](https://qloudableassets.blob.core.windows.net/azure-sentinel/Images/5.PNG?st=2020-03-27T08%3A30%3A39Z&se=2023-03-28T08%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=fXFmtQnh1zR1OuRkdCKkLEmrA8WaC0VJbHV0pf697Mg%3D)

6. Fill in all the fields with required data on the form for creating the Azure Sentinel workspace.

* **Subscription:** Select as default from the dropdown <br>
* **Resource Group:** `{{resource-group-name}}` <br>
* **Name:** The name of the Workspace must be globally unique <br>
* **Region:** `{{location}}`

7. Click on **Review + Create** button at the bottom.

![alt text](https://qloudableassets.blob.core.windows.net/azure-sentinel/Images/6.PNG?st=2020-03-27T08%3A30%3A39Z&se=2023-03-28T08%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=fXFmtQnh1zR1OuRkdCKkLEmrA8WaC0VJbHV0pf697Mg%3D)

8. Click on **Create**. The process takes few minutes, wait for the deployment to complete.

![alt text](https://qloudableassets.blob.core.windows.net/azure-sentinel/Images/7.PNG?st=2020-03-27T08%3A30%3A39Z&se=2023-03-28T08%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=fXFmtQnh1zR1OuRkdCKkLEmrA8WaC0VJbHV0pf697Mg%3D)

9. After successful deployment, you can see the Deployment succeeded message under Notifications.

![alt text](https://qloudableassets.blob.core.windows.net/azure-sentinel/Images/8.PNG?st=2020-03-27T08%3A30%3A39Z&se=2023-03-28T08%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=fXFmtQnh1zR1OuRkdCKkLEmrA8WaC0VJbHV0pf697Mg%3D)

### Add Azure sentinel to the workspace

After successful creation of Azure sentinal workspace, select that created workspace and click on **Add Azure Sentinel**.

![alt text](https://qloudableassets.blob.core.windows.net/azure-sentinel/Images/9.PNG?st=2020-03-27T08%3A30%3A39Z&se=2023-03-28T08%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=fXFmtQnh1zR1OuRkdCKkLEmrA8WaC0VJbHV0pf697Mg%3D)

![alt text](https://qloudableassets.blob.core.windows.net/azure-sentinel/Images/10.PNG?st=2020-03-27T08%3A30%3A39Z&se=2023-03-28T08%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=fXFmtQnh1zR1OuRkdCKkLEmrA8WaC0VJbHV0pf697Mg%3D)

## Exercise 2: Detect threats out-of-the-box

## Exercise 3: Visualize and monitor your data

## Exercise 4: Investigate incidents with Azure Sentinel

## Exercise 5: Set up automated threat responses in Azure Sentinel
