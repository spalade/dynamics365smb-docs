---
title: "How to: Create a Configuration Package"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "RapidStart Services, creating configuration packages"
ms.assetid: f14b31f2-92d5-462f-9b8f-7213ed156bf6
caps.latest.revision: 14
ms.author: "solsen"
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
# How to: Create a Configuration Package
When you configure a new company, table relations are recognized and processed. Data is imported and applied in the correct order. Dimension tables are also imported if they are included in the configuration package.  
  
 To help your customer use the configuration package, you may want to add a questionnaire or a set of questionnaires to the package. The questionnaire can help the customer in understanding the various setup options. Typically, questionnaires are created for the major setup tables within [!INCLUDE[navnow](../ApplicationDesign/includes/navnow_md.md)], when a customer may require additional guidance about how to select an appropriate setting. For more information, see [How to: Create Configuration Questionnaires](../SetupAndAdministration/how-to-create-configuration-questionnaires.md).  
  
 Make sure that you are on the [!INCLUDE[rim](../Roles/includes/rim_md.md)] Role Center page for the baseline company. To change your Role Center home page, see [How to: Change Role Centers](../GettingStarted/how-to-change-role-centers.md). Choose the RapidStart Profile ID.  
  
> [!IMPORTANT]  
>  When exporting and importing configuration packages between two company databases, the databases should have the same schema to ensure that all data is transferred successfully. This means that the databases should have the same table and field structure, in which the tables have the same primary keys and fields have the same IDs and data types.  
>   
>  You can import a configuration package that has been exported from a database that has a different schema than that target database. However, any tables or fields in the configuration package that are missing in the target database will not be imported. Tables with different primary keys and fields with different data types will also not successfully import. For example, if the configuration pack includes table **50000 Customer** that has primary key **Code20** and the database to which you import the pack includes table **50000 Customer Bank Account** that has the primary key **Code20 \+ Code 20**, data will not be imported.  
  
### To create a configuration package  
  
1.  In the **Search** box, enter **Configuration Packages**, and then choose the related link.  
  
2.  On the **Home** tab, in the **New** group, choose **New**.  
  
3.  On the **General** FastTab, fill in the fields as appropriate.  
  
     [!INCLUDE[bp_fieldhelp]()]  
  
4.  To exclude the configuration questionnaires, configuration templates, and configuration worksheet tables from the package, select the **Exclude Configuration Tables** check box. Otherwise, these tables will be added to the list of package tables automatically when you export the package.  
  
5.  On the **Actions** tab, in the **Functions** group, choose **Get Tables**. The **\($ B\_8616 Get Package Tables $\)** batch job window opens.  
  
     Choose the **Select Tables** field. The **Config. Selection** window opens.  
  
6.  On the **Home** tab, in the **Process** group, choose **Select All** to add all tables to the package, or select the **Selected** check box for each table in the list that you want to add.  
  
7.  Choose the **OK** button. The count of tables that you have selected is indicated in the **Select Tables** field. Specify additional options, and then choose the **OK** button. [!INCLUDE[navnow](../ApplicationDesign/includes/navnow_md.md)] tables are added to the lines of the **Config. Package** card.  
  
    > [!NOTE]  
    >  You can also do this in the configuration worksheet. Select the tables you want to include in the package, and on the **Actions** tab, in the **Functions** group, choose **Assign Package**.  
  
8.  To select the fields you want to include from a table, select the table, and on the **Lines** toolbar, on the **Table** menu, choose **Fields**. Specify which fields are included in the package. By default, all fields are included.  
  
     To select just the fields you want to include, on the **Home** tab, in the **Process** group, choose **Clear Included**. To add all fields, choose **Set Included**.  
  
     To specify that the field data should not be validated, clear the **Validate Field** check box for the field.  
  
9. Determine whether you have introduced potential errors. This can occur when you do not include tables that your configuration relies on. On the **Actions** tab, on the **Functions** group, choose **Validate Package**.  
  
10. Choose the **OK** button.  
  
 After you have refined the list of fields to include from a table, you can check your results in Excel.  
  
### To filter and review your dataset  
  
1.  To filter to a certain set of records to include in the package, on the **Lines** toolbar, on the **Table** menu, choose **Filters**. Specify the appropriate filter values.  
  
     [!INCLUDE[bp_fieldhelp]()]  
  
2.  On the package card, on the **Lines** toolbar, on the **Excel** menu, choose **Export to Excel**.  
  
     Confirm the messages that enable the export of data to Excel. The named .xlsx file opens. Review the records that have been exported.  
  
     Close Excel.  
  
 For certain tables, such a table that will contain master data, you can specify a template to apply to the data. The template can include the required fields that you want to apply to all master data and that you never want to vary. For example, you can create a template that can be used with customer data. The template can contain all the required fields, which then enables consistent import of standardized information. Information that cannot be standardized, such as customer name, is then treated when you do an import of customer data.  
  
### To include a template for application to a table  
  
1.  In the package card, select a table, and then choose the **Data Template** field.  
  
     A list of templates is displayed that are based on the table.  
  
2.  Select a template, and then choose the **OK** button.  
  
 After the package is complete, use the procedure that follows to save the package to a file. You can then give the package to a customer or partner to use.  
  
### To save and export a configuration package  
  
-   On the **Actions** tab, in the **Package** group, choose **Export Package**.  
  
     The package is created in a .rapidstart file, which delivers the package contents in a compressed format. Configuration questionnaires, configuration templates, and the configuration worksheet are added to the package automatically unless you specifically decide to exclude them.  
  
     You can save the file with a name that is meaningful to you, but you cannot change the extension of the file. It must be .rapidstart.  
  
 After you have created a package that meets most of your needs, you can use it as a basis for creating similar packages. This can speed implementation time and enhances the repeatability aspect of [!INCLUDE[rim](../Roles/includes/rim_md.md)].  
  
### To copy a configuration package  
  
1.  In the **Search** box, enter **Configuration Packages**, and then choose the related link.  
  
2.  Select a package from the list, and on the **Actions** tab, in the **Functions** group, choose **Copy Package**.  
  
3.  In the **New Package Code** field, enter a code for the new package.  
  
4.  Select the **Copy Data** check box if you also want to copy database data from the existing package.  
  
5.  Choose the **OK** button.  
  
## See Also  
 [How to: Assign a Configuration Package](../SetupAndAdministration/how-to-assign-a-configuration-package.md)   
 [\($ B\_8615 Copy Package $\)](../Topic/\($%20B_8615%20Copy%20Package%20$\).md)   
 [\($ B\_8616 Get Package Tables $\)](../Topic/\($%20B_8616%20Get%20Package%20Tables%20$\).md)   
 [How to: Manage Company Configuration in a Worksheet](../SetupAndAdministration/how-to-manage-company-configuration-in-a-worksheet.md)   
 [How to: Import Configuration Packages](../SetupAndAdministration/how-to-import-configuration-packages.md)