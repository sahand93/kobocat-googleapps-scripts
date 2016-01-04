The Update_Spreadsheet working example uses token authentication to access the kobocat API v1 allowing users to update all data from within Google Spreadsheets. The script can be run through the added menu item. 

## Known Issues:
1. This script assumes all headers are in the first row. This script does not work on blank worksheets because it compares the headers from the sheet to the information received from kobocat
1. At the moment, the entire sheet is replaced. A Future improvement would be to run through the '_id' column of the sheet, compare it to the kobocat server and only download the instances that are missing. 
1. Blank fields from the kobocat server are tagged as 'Undefined' 


## Installation:
1. Export your (blank) dataset as an XLS file
1. Navigate to Google Drive, upload the XLS file, then click Open in Google Sheets to edit it
1. Click 'Tools>Script Editor...'. If you are presented with a welcome screen, click Blank Project.
1. Delete any code in the script editor and paste in the code from [this file](Update_Spreadsheet) into the editor.
1. Click the menu item Run>OnOpen.
1.  Select the menu item File > Save all. Name your new script "Update from KoBoToolbox" and click OK.
1. Complete the authorization and run the function again
1. A new menu item will appear called 'Update from kobocat'


## Setup:
1. In a separate browser window, navigate to https://kc.kobotoolbox.org/YOURUSERNAME/api-token
1. Highlight and copy the token using Ctrl-C
1. Click 'Update from kobocat>Setup'
1. Paste your token code and click Submit
1. Click 'OK' to the popup
1. Select your kobocat form which updates this sheet
1. Click 'Submit' and 'OK' to the popup


## Running the Script:
1. Click Update from kobocat>Import Data' to update the entire spreadsheet
