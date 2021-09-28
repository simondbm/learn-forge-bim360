### Development Build

Callback URL
http://localhost:3000/api/forge/oauth/callback

### Find the Hub ID for the BIM 360 Account

curl -X GET -H "Authorization: Bearer nFRJxzCD8OOUr7hzBwbr06D76zAT" "https://developer.api.autodesk.com/project/v1/hubs"

hub id b.b399ba13-cc73-4fa0-b960-5793e94622cf

### Find the Project ID

curl -X GET -H "Authorization: Bearer nFRJxzCD8OOUr7hzBwbr06D76zAT" "https://developer.api.autodesk.com/project/v1/hubs/b.b399ba13-cc73-4fa0-b960-5793e94622cf/projects"

project id b.58613a2e-1727-45e0-8cd5-ba185fa07930

### Find the Folder ID

curl -X GET -H "Authorization: Bearer nFRJxzCD8OOUr7hzBwbr06D76zAT"
"https://developer.api.autodesk.com/project/v1/hubs/b.b399ba13-cc73-4fa0-b960-5793e94622cf/projects/b.58613a2e-1727-45e0-8cd5-ba185fa07930/topFolders"

#### Find the folder (data.attributes.name); in this example, the Project Files folder, and note the folder ID (data.id) - urn:adsk.wipprod:fs.folder:co.BJU3PTc4Sd2CmXM492XUiA

folder id urn:adsk.wipprod:fs.folder:co.Wt4A3bmHReCk8Q7LGMuKQw

### Find the Nested Folder ID

curl -X GET -H "Authorization: Bearer nFRJxzCD8OOUr7hzBwbr06D76zAT"
"https://developer.api.autodesk.com/data/v1/projects/b.58613a2e-1727-45e0-8cd5-ba185fa07930/folders/urn:adsk.wipprod:fs.folder:co.Wt4A3bmHReCk8Q7LGMuKQw/contents"
