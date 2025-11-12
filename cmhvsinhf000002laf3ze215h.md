---
title: "How to connect to ANF using PowerShell"
datePublished: Wed Nov 12 2025 09:21:00 GMT+0000 (Coordinated Universal Time)
cuid: cmhvsinhf000002laf3ze215h
slug: how-to-connect-to-anf-using-powershell
tags: azure, anf

---

## What is Azure NetApp Files?

Azure NetApp Files, popularly known as ANF, is a high-performance file storage offered by Microsoft Azure. If an enterprise or a user has a NAS workload, and/or are familiar with NetApp, then ANF can be a good fit.

ANF provides flexibility in selecting the capacity and performance service levels, catering a variety of performance sensitive workloads. It has a holistic Data Protection and Security Management features, ensuring the safety of data.

More information can be found here: [What is Azure NetApp Files | Microsoft Learn](https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-introduction)

### Important considerations before we connect ANF using PowerShell

1. Enable ANF in subscription:
    
    [https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-register](https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-register)
    
2. Check ANF availability by region
    
    [Azure Product by Region | Microsoft Azure](https://azure.microsoft.com/en-us/explore/global-infrastructure/products-by-region/?products=netapp)
    
3. Check and unlock Resource limits:
    
    [Resource limits for Azure NetApp Files | Microsoft Learn](https://learn.microsoft.com/en-us/azure/azure-netapp-files/azure-netapp-files-resource-limits)
    

## Steps

1. Install Az.NetAppFiles Module
    
    ***Install-Module -Name Az.NetAppFiles***
    
    (Link for documentation and other cmdlet: [Az.NetAppFiles Module | Microsoft Learn](https://learn.microsoft.com/en-us/powershell/module/az.netappfiles/?view=azps-14.5.0))
    
2. Connect to Azure Account
    
    ***Connect-AzAccount***
    
3. Get a list of all the Azure subscriptions
    
    ***Get-AzSubscription***
    
4. Connect to specific subscription using SubscriptionId from Step 3
    
    ***Set-AzContext -Subscription -Subscription &lt;SubscriptionId&gt;***
    
5. Get a list of resource groups to identify resource group where ANF resources exists
    
    ***Get-AzResourceGroup***
    
    (If the command doesn’t work, then install Az.Resources module using Install-Module Az.Resources)
    
6. Display ANF account details
    
    ***Get-AzNetAppFilesAccount -ResourceGroupName &lt;resourceGroup&gt;***
    
7. Display capacity pool details
    
    ***Get-AzNetAppFilesPool -ResourceGroupName &lt;resourceGroup&gt; -AccountName &lt;anfAccountName&gt;***
    
8. Display the volume details
    
    ***Get-AzNetAppFilesVolume -ResourceGroupName &lt;resourceGroup&gt; -AccountName &lt;anfAccountName&gt; -PoolName &lt;poolname&gt;***
    

### References:

1. If you want to retrieve details of snapshots in a csv, checkout my GitHub : [Azure\_NetApp\_Files\_Retrieve\_Snapshots\_Details\_Using\_PowerShell/ANF\_PS\_Snapshots.ps at main · greyknight28/Azure\_NetApp\_Files\_Retrieve\_Snapshots\_Details\_Using\_PowerShell](https://github.com/greyknight28/Azure_NetApp_Files_Retrieve_Snapshots_Details_Using_PowerShell/blob/main/ANF_PS_Snapshots.ps)
    
2. More articles on ANF: [Automate Azure NetApp Files with PowerShell – anfcommunity](https://anfcommunity.com/2020/09/11/automate-azure-netapp-files-with-powershell/)
    
3. More GitHUB IaC: [anthonymashford (Anthony Mashford)](https://github.com/anthonymashford)
    
4. ANF Blogs: [AzureTechLab](https://www.azuretechlab.com/)
    
5. [NetApp: A](https://www.azuretechlab.com/)[zure NetApp Files | Ne](https://github.com/anthonymashford)[tApp](https://www.netapp.com/azure/azure-netapp-files/)
    
6. Microsoft: [Azure NetApp Files | Microsoft Azure](https://azure.microsoft.com/en-us/products/netapp/?msockid=04eeb3532df06d160b99a5df2c336c93)