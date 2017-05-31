---
title: "How to: Move Items in Advanced Warehousing"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "operations, moving items between"
  - "movements, ad hoc"
  - "worksheets, moving items"
ms.assetid: e16b182b-bcb0-4b95-b839-4c147e6ae551
caps.latest.revision: 6
ms.author: "sgroespe"
manager: "terryaus"
translation.priority.ht: 
  - "da-dk"
  - "de-at"
  - "de-ch"
  - "de-de"
  - "en-au"
  - "en-ca"
  - "en-gb"
  - "en-in"
  - "en-nz"
  - "es-es"
  - "es-mx"
  - "fi-fi"
  - "fr-be"
  - "fr-ca"
  - "fr-ch"
  - "fr-fr"
  - "is-is"
  - "it-ch"
  - "it-it"
  - "nb-no"
  - "nl-be"
  - "nl-nl"
  - "ru-ru"
  - "sv-se"
---
# How to: Move Items in Advanced Warehousing
In advanced warehouse configurations, that is, locations with directed put\-away and pick, warehouse movements between bins are performed by a senior employee preparing warehouse movements in the movement worksheet and then creating the warehouse movements for warehouse employees to perform.  
  
#### To move items with the warehouse movement worksheet  
  
1.  In the **Search** box, enter **\($ N\_7351 Movement Worksheet $\)**, and then choose the related link.  
  
2.  Enter the warehouse movement information on the worksheet lines as appropriate.  
  
3.  On the **Actions** tab, in the **Functions** group, there are two functions that can assist in automatically filling in the lines. The first is the **Calculate Bin Replenishment** function. This function uses the bin rankings to suggest replenishment for high\-ranking bins from low\-ranking bins. The second is the **Get Bin Content** function, which fills in the worksheet lines with the entire bin contents of the bin or bins you specify.  
  
4.  On the **Actions** tab, in the **Functions** group, choose **Create Movement** to create a warehouse movement document which can then be registered when the warehouse movement is completed.  
  
#### To register the warehouse movement  
  
1.  In the **Search** box, enter **Movements**, and then choose the related link.  
  
2.  Open the warehouse movement that you want to process.  
  
3.  On lines of action type **Place**, specify where, which, and when to move the item in question by editing the **Zone Code**, **Bin Code**, **Qty. to Handle**, or **Due Date** fields.  
  
     If your warehouse has been set up so the bin codes follow the physical structure of the warehouse, you can take quantities of several items from successive bulk bins and then place them in forward picking bins, which also might be close to one another.  
  
4.  On lines of action type **Take**, specify in the **Qty. to Handle** field a part quantity of the bin content that you want to move. All other fields on lines of action type **Take** are read\-only.  
  
5.  To move all suggested quantities as specified in the **Quantity** field, on the **Actions** tab, in the **Functions** group, choose **Autofill Qty. to Handle**.  
  
6.  To print the movement document, on the **Actions** tab, in the **General** group, choose  **Print.**  
  
7.  On the **Actions** tab, in the **Registering** group, choose **Register**.  
  
> [!NOTE]  
>  If the location uses directed put\-away and pick, then you cannot manually move items in or out of bins of bin type RECEIVE, because items in such bins must be registered as being put away before they are part of available inventory.  
  
## See Also  
 [\($ T\_7326\_21 Qty. to Handle $\)](../Topic/\($%20T_7326_21%20Qty.%20to%20Handle%20$\).md)   
 [\($ N\_7315 Warehouse Movement $\)](../Topic/\($%20N_7315%20Warehouse%20Movement%20$\).md)   
 [How to: Plan Warehouse Movements in Worksheets](../WarehouseActivities/how-to-plan-warehouse-movements-in-worksheets.md)   
 [How to: Move Items Ad Hoc in Basic Warehousing](../WarehouseActivities/how-to-move-items-ad-hoc-in-basic-warehousing.md)