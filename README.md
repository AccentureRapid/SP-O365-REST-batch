# Using the $batch query option against the SharePoint REST APIs #

### Summary ###
This sample shows how combine multiple OData operations against the SharePoint REST/OData service into a single HTTP Request/Response. The sample uses HTML, C#, and the managed code OData library in [Microsoft.Data.Odata](http://msdn.microsoft.com/en-us/office/microsoft.data.odata(v=vs.90)).

### Applies to ###
-  SharePoint Online and the Files and Folders subset of the Office 365 REST APIs

### Prerequisites ###
Not required, but recommended: Install [Fiddler](http://www.telerik.com/fiddler).

### Solution ###
Solution | Author(s)
---------|----------
SPO-REST-Batch | Ricky Kirkham (**Microsoft**)

### Version history ###
Version  | Date | Comments
---------| -----| --------
1.0  | December 18th 2014 | Initial release

### Disclaimer ###
**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**


----------

# Overview #
The purpose of this sample is to show how to use the $batch query option, as defined by the OData 3.0/4.0 standard can be used with SharePoint Online's REST APIs and the Files and Folders APIs of Office 365.

As of the initial release of this sample, Microsoft's support for $batch is not compliant with the OData 3.0/4.0 standard in one respect: The REST service does not support "all or nothing" transaction protection for the operations that are included in a ChangeSet, which is a set of operations that make changes on the OData source. (Purely "read" operations; that is, operations that use the GET verb, are outside of ChangeSets although they can be included in the operations of a batch request.

# To use this sample #

12. Open the .sln file for the sample in **Visual Studio**.
13. In Solution Explorer, highlight the SharePoint app project and replace the **Site URL** property with the URL of your SharePoint developer site.
14. Turn on Fiddler if you have it installed.

You can now run the sample with F5. The first time you do, you are prompted to trust the app. The default page of the web application then opens. There are three different batch jobs you can try. They use lists that are present on every Developer Site out-of-the-box: The User list, the Composed Looks list, and the List of Lists on the website.






