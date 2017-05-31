---
title: "Design Details: Handling Projected Negative Inventory"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "inventory, projected negative"
ms.assetid: dbbe4950-fcae-456b-a7e2-03875e540b4d
caps.latest.revision: 8
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
# Design Details: Handling Projected Negative Inventory
The reorder point expresses the anticipated demand during the lead time of the item. When the reorder point is passed, it is time to order more. But the projected inventory must be large enough to cover the demand until the new order is received. Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.  
  
 Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative. The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply. The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple. Instead, it will reflect the exact deficiency.  
  
 The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.  
  
 In the following illustration, supply D represents an emergency order to adjust for negative inventory.  
  
 ![](../ApplicationDesign/media/nav_app_supply_planning_2_negative_inventory.png "NAV\_APP\_supply\_planning\_2\_negative\_inventory")  
  
1.  Supply **A**, initial projected inventory, is below reorder point.  
  
2.  A new forward\-scheduled supply is created \(**C**\).  
  
     \(Quantity \= Maximum Inventory – Projected Inventory Level\)  
  
3.  Supply **A** is closed by demand **B**, which is not fully covered.  
  
     \(Demand **B** could try to schedule Supply C in but that will not happen according to the time\-bucket concept.\)  
  
4.  New supply \(**D**\) is created to cover the remaining quantity on Demand **B**.  
  
5.  Demand **B** is closed \(creating a reminder to the projected inventory\).  
  
6.  The new supply **D** is closed.  
  
7.  Projected Inventory is checked; reorder point has not been crossed.  
  
8.  Supply **C** is closed \(no more demand exists\).  
  
9. Final check: No outstanding inventory level reminders exist.  
  
> [!NOTE]  
>  Step 4 reflects how the system reacts in versions earlier than [!INCLUDE[nav2009sp1](../ApplicationDesign/includes/nav2009sp1_md.md)].  
  
 This concludes the description of central principles relating to inventory planning based on reordering policies. The following section describes the characteristics of the four supported reordering policies.  
  
## See Also  
 [Design Details: Reordering Policies](../ApplicationDesign/design-details-reordering-policies.md)   
 [Design Details: Planning Parameters](../ApplicationDesign/design-details-planning-parameters.md)   
 [Design Details: Handling Reordering Policies](../ApplicationDesign/design-details-handling-reordering-policies.md)   
 [Design Details: Supply Planning](../ApplicationDesign/design-details-supply-planning.md)