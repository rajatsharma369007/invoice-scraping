# Invoice Scraping using Robot Process Automation

This repository contains robot process automation workflow for automating the manual task of downloading the PDF invoices from a certain group of emails and then storing the important information into  a more strucured format. It takes a lot of time and attention to complete the whole process but automating this would take only seconds to complete with less prone to error.

![alt-txt](https://github.com/rajatsharma369007/invoice-scraping/blob/main/doc/images/image1.jpg)

### Automation contains 7 key steps

1) Read the Emails with given subjectline
2) Download the attached invoices
3) Analyze selectors on get the attributes and their ability to be robust, stable and dynamic with relevant tags to extract structured data from the invoice
4) Port the scraped data to an excel sheet
5) Uploads the data to UiPath Orchestrator queue
6) Sends an Email with an attached excel

### Workflow in Operation

- [Fetch_Save_Attachment.xaml](https://github.com/rajatsharma369007/invoice-scraping/blob/main/workflow/Fetch_Save_Attachment.xaml) : Automates the task of download the PDF invoices from Emails with a specific subjectline.
- [Scraping_Automation.xaml](https://github.com/rajatsharma369007/invoice-scraping/blob/main/workflow/Scaping_Automation.xaml) : Automate the task of reading each PDF file and invokes some other workflow.
  - [Scrap_PDF_Data.xaml](https://github.com/rajatsharma369007/invoice-scraping/blob/main/workflow/Scrap_PDF_Data.xaml) : Scraps the useful information from the PDF using defined selectors and create an excel to store the data in structured format.
    - [Orchestrator_Queue.xaml](https://github.com/rajatsharma369007/invoice-scraping/blob/main/workflow/Orchestrator_Queue.xaml) : Sends the information to UiPath Orchestrator Queue
  - [Send_Excel_Mail.xaml](https://github.com/rajatsharma369007/invoice-scraping/blob/main/workflow/Send_Excel_Mail.xaml) : Sends an Email with an attached excel having structured data.
 
### Screenshots

##### Received Emails with PDF invoices
<img src="https://github.com/rajatsharma369007/invoice-scraping/blob/main/doc/images/image4.jpg" width="500px"/>

##### A sample of PDF invoice 
<img src="https://github.com/rajatsharma369007/invoice-scraping/blob/main/doc/images/image2.jpg" width="500px"/>

##### A sample of structured invoice
<img src="https://github.com/rajatsharma369007/invoice-scraping/blob/main/doc/images/image3.jpg" width="500px"/>

##### Orchestrator Queue
<img src="https://github.com/rajatsharma369007/invoice-scraping/blob/main/doc/images/image6.png" width="500px"/>
    
##### Sent Emails with attached excel
<img src="https://github.com/rajatsharma369007/invoice-scraping/blob/main/doc/images/image5.png" width="500px"/>


### License

Licensed under the [MIT License](./LICENSE.md) @ Udacity


### Issues/Bugs

Please open issues on github to report bugs or make feature requests

### Contribution

If you are interested in improving the code, please open an issue first to describe the task you are planning to do. For small fixes (a few lines of change) feel free to open pull requests directly.
