#Add-PnPPublishingPage
Adds a publishing page
##Syntax
```powershell
Add-PnPPublishingPage [-Title <String>]
                      -PageName <String>
                      -FolderPath <String>
                      -PageTemplateName <String>
                      [-Publish [<SwitchParameter>]]
                      [-Web <WebPipeBind>]
```


##Parameters
Parameter|Type|Required|Description
---------|----|--------|-----------
|FolderPath|String|True|The site relative folder path of the page to be added|
|PageName|String|True|The name of the page to be added as an aspx file|
|PageTemplateName|String|True|The name of the page layout you want to use. Specify without the .aspx extension. So 'ArticleLeft' or 'BlankWebPartPage'|
|Publish|SwitchParameter|False|Publishes the page. Also Approves it if moderation is enabled on the Pages library.|
|Title|String|False|The title of the page|
|Web|WebPipeBind|False|The web to apply the command to. Omit this parameter to use the current web.|
##Examples

###Example 1
```powershell
PS:> Add-PnPPublishingPage -PageName 'OurNewPage' -Title 'Our new page' -PageTemplateName 'ArticleLeft'
```
Creates a new page based on the pagelayout 'ArticleLeft'

###Example 2
```powershell
PS:> Add-PnPPublishingPage -PageName 'OurNewPage' -Title 'Our new page' -PageTemplateName 'ArticleLeft' -Folder '/Pages/folder'
```
Creates a new page based on the pagelayout 'ArticleLeft' with a site relative folder path
