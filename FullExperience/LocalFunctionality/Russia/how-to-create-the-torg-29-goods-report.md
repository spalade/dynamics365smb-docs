---
title: "How to: Create the TORG-29 Goods Report"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "TORG reports, creating"
ms.assetid: 792c1f9d-0fda-4f2d-84b6-ffd3795e7b21
caps.latest.revision: 2
ms.author: "edupont"
translation.priority.ht: 
  - "ru-ru"
---
# How to: Create the TORG-29 Goods Report
The TORG\-29 report shows the item documents that you can use to submit for receipts and shipments for a location.  
  
 When you run the report for a location, the **\($ T\_14\_12400 Last Goods Report No. $\)** and **\($ T\_14\_12401 Last Goods Report Date $\)** fields in the **\($ N\_5703 Location Card $\)** window are updated to ensure consistent reporting.  
  
### To create the TORG\-29 report  
  
1.  In the **Search** box, enter **Item Report TORG\-29**, and then choose the related link.  
  
2.  On the **Options** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ R\_14919\_F\_1\_1210028 Location Code $\)**|Specifies the location that the report is for.|  
    |**\($ R\_14919\_F\_1\_1210003 Report No. $\)**|Specifies the number of times that the report has printed based on the value of the **\($ T\_14\_12400 Last Goods Report No. $\)** field in the **\($ N\_5703 Location Card $\)** window.|  
    |**\($ R\_14919\_F\_1\_1210005 Responsible Employee $\)**|Specifies the employee who is responsible for the validity of the data in the report.|  
    |**\($ R\_14919\_F\_1\_1210000 Report Acceptor $\)**|Specifies the employee who is responsible for accepting the report.|  
    |**\($ R\_14919\_F\_1\_1210002 Report Date $\)**|Specifies the date of the report.|  
    |**\($ R\_14919\_F\_1\_1210008 Start Date $\)**|Specifies the start date for the report.|  
    |**\($ R\_14919\_F\_1\_1210010 End Date $\)**|Specifies the start date for the report.|  
    |**\($ R\_14919\_F\_1\_1210012 Operation Type $\)**|Optionally, specifies the type of operation. This information will be included in the report.|  
    |**\($ R\_14919\_F\_1\_1210015 Attaches No. $\)**|Specifies the number of attachments to the report.|  
    |**\($ R\_14919\_F\_1\_1210017 Receipt Detailing $\)**|Specifies what the detailed information for each entry is based on.<br /><br /> If you select **Document**, amounts are totaled for each document. If you select **Item**, the amount and quantity are totaled for each item. If you select **Operation**, the amount and quantity are included in a single transaction.|  
    |**\($ R\_14919\_F\_1\_1210018 Shipment Detailing $\)**|Specifies what the detailed information for each entry is based on.<br /><br /> If you select **Total Amount**, the report summarizes amounts in a single line. If you select **Document**, amounts are totaled for each document. If you select **Item**, the amount and quantity are totaled for each item. If you select **Operation**, the amount and quantity are included in a single transaction.|  
    |**\($ R\_14919\_F\_1\_1210021 Amount Type $\)**|Specifies what the amounts are based on, cost or sales price.<br /><br /> If you set this field to **Sales Price**, the **\($ R\_14919\_F\_1\_1210030 Sales Type $\)**, **\($ R\_14919\_F\_1\_1210032 Show Cost Amount for Receipts $\)**, and **\($ R\_14919\_F\_1\_1210033 Show Cost Amounts for Shipment $\)** fields become available.|  
    |**\($ R\_14919\_F\_1\_1210030 Sales Type $\)**|Specifies the type of price list.<br /><br /> If you select **Customer Price List**  or **Campaign**, you can select the price list in the **\($ R\_14919\_F\_1\_1210035 Sales Code $\)** field. If you select **All Customers**, a unified price list is used.|  
    |**\($ R\_14919\_F\_1\_1210035 Sales Code $\)**|Specifies the price list. Depending on the selection in the **\($ R\_14919\_F\_1\_1210030 Sales Type $\)** field, you can specify either a customer price group or a campaign number.|  
    |**\($ R\_14919\_F\_1\_1210032 Show Cost Amount for Receipts $\)**|Specifies if each receipt line must be divided into two lines. If selected, the first line for a receipt represents item cost, and the second line represents the sales margin.|  
    |**\($ R\_14919\_F\_1\_1210033 Show Cost Amounts for Shipment $\)**|Specifies if each shipment line must be divided into two lines. If selected, the first line for a receipt represents the item cost, and the second line represents the sales margin.|  
  
3.  Choose the **Print** button.  
  
## See Also  
 [Inventory Setup](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Russia/inventory-setup.md)   
 [\($ R\_14919 Item Report TORG\-29 $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Russia/-$-r_14919-item-report-torg-29-$-.md)   
 [\($ B\_14918 Items Receipt Act TORG\-1 $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Russia/-$-b_14918-items-receipt-act-torg-1-$-.md)   
 [\($ B\_14925 Receipt Deviations TORG\-2 $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Russia/-$-b_14925-receipt-deviations-torg-2-$-.md)   
 [\($ R\_14976 Transfer Order TORG\-13 $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Russia/-$-r_14976-transfer-order-torg-13-$-.md)