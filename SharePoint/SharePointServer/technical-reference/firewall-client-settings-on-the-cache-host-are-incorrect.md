---
title: "Firewall client settings on the cache host are incorrect (SharePoint Server)"
ms.author: stevhord
author: bentoncity
manager: pamgreen
ms.date: 8/29/2017
ms.audience: ITPro
ms.topic: troubleshooting
ms.prod: sharepoint-server-itpro
localization_priority: Normal
ms.collection:
- IT_Sharepoint_Server
- IT_Sharepoint_Server_Top
ms.assetid: f8dcfd5c-aaec-46cd-b25e-94e14bf98c7d
description: "Summary: Learn how to resolve the SharePoint Health Analyzer ruleFirewall client settings on the cache host are incorrect, in SharePoint Server 2016 and SharePoint 2013."
---

# Firewall client settings on the cache host are incorrect (SharePoint Server)

 **Summary:** Learn how to resolve the SharePoint Health Analyzer rule "Firewall client settings on the cache host are incorrect", in SharePoint Server 2016 and SharePoint 2013. 
  
 **Rule Name:** Firewall client settings on the cache host are incorrect. 
  
 **Summary:** Firewall rule settings for App fabric caching are disabled. 
  
 **Cause:** Firewall rule settings for App fabric caching are disabled. 
  
 **Resolution: Enable the firewall rules for the AppFabric Caching service.**
  
1. Verify that the user account that is performing this procedure is a member of the Administrators group on the local computer.
    
2. On **Server Manager**, click **Tools**, and then select **Windows Firewall with Advanced Security**.
    
3. In the **Windows Firewall with Advanced Security** console tree, click **Inbound Rules**.
    
4. In the **Inbound Rules** list, right-click **AppFabric Caching Service (TCP-In)**, and then select **Enable Rule**.
    
5. In the **Windows Firewall with Advanced Security** console tree, click **Outbound Rules**.
    
6. In the **Outbound Rules** list, right-click **AppFabric Caching Service (TCP-Out)** and then select **Enable Rule**.
    
By default, the **Repair Automatically** option is enabled for this rule. You can restore the default setting for this rule by doing the following: 
  
1. On the the SharePoint Central Administration website, click **Monitoring**.
    
2. On the Monitoring page, in the **Health Analyzer** section, click **Review rule definitions**.
    
3. On the Health Analyzer Rule Definitions - All Rules page, in the **Category: Configuration** section, click the name of the rule. 
    
4. On the **Health Analyzer Rule Definitions** page, click **Edit Item**.
    
5. Select the **Repair Automatically** check box, and then click **Save**.
    
