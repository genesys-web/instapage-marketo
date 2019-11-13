# instapage-marketo

## Scripts

| Scripts        | Description              |
| -------------- | ------------------------ |
| https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js | Added to initialize jQuery as Marketo needs this |
| https://genbin.genesys.com/marketo/instapage/mkt_basecode.min.js | Customized Base Marketo script for Genesys |
| https://genbin.genesys.com/marketo/instapage/RequestForm.js | Main form script required for the request functions |
| https://risk.clearbit.com/v1/risk.js | Creabit Risk Script |

## Object Variables

| Variables        | Values           | Description              |
| ---------------- | ---------------- | ------------------------ |
| lang | en,en-gb,en-sg,fr-fr,de-de... | This should contain the site language defaulted to "en" when empty. |
| form_id | ex. 1234 | 4 numbers that maps back to marketo to load any specific form |
| cid_id | ex. x1v3b2m2n4x7 | Salesforce ID that maps back to Salesforce for tracking |
| cms_hold | "web","HOT","RG" | "web" as default, "HOT" for hot lead, "RG" for Registered |
| action | "page", "inline" | "Page" sends the user to a new URL after submit, "Inline" manipulates the current page to hide the form and show the thank you content |
| url | url of the thank you page | Requirements: action = "page" |
| target | ID or Class of the Targeted DIV. ex. ".thankyou" or "#thankyou" | Requirements: action = "inline" |
| button | ex. "Download" | define the button text on the form |
| ar_status | default, dynamic | Defines how the autoresponder is configured |
| clearbit | "yes", "no" | define if you want to use clearbit in the form |

## Added Variables

| Variables        | Values           | Description              |
| ---------------- | ---------------- | ------------------------ |
| pagepath | window path | stores the current page window path |


## Multi Page Routing

**mkt_obj** this single variable contains the form attributes of the single page. By manipulating this variable before the **_RequestForm()_** function is called.


## Change logs

### Version 1.0.0
* Initialize readme
* Known Issues:
    * Clearbit forms not altering the forms
