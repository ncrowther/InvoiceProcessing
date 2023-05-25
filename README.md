# Invoice Processing Project

This project provides a complete invoice processing solution for small to medium size enterprises.

## Creating Outlook email folders

Create a free Outlook account (IBM Outlook does not work)

In Outlook, create failed and processed invoices folders:
 
 <p align="center"><img width=15% height=15% src="images/outlookfolders.jpg"></p>

## Configuring Outlook in RPA Control Center

Login to the RPA control center. 

Configure the following script parameters:

```
outlookUser - set to your free outlook email address created above
adminUser - set to the email address of the person who will be administering the bot (to start with, this will be you)
invoiceBasePath - set to the base path of this project (the InvoiceProcessing-RPA folder in this project)
```

 <p align="center"><img width=50% height=50% src="images/scriptParams.jpg"></p>

Go to Connections 

Create a new Microsoft Exchange IMAP connection that connects to your Outlook email.   

 <p align="center"><img width=25% height=25% src="images/ImapConnection.jpg"></p>

  <p align="center"><img width=50% height=50% src="images/ImapConnectionName.jpg"></p>

## The RPA Bot

Open RPA studio and import the artefacts in folder ```InvoiceProcessing```

Open ```invoiceBot.wal```. Change line so that it points to the outlook connection you created.

##  Adding new invoices

Edit determineInvoiceType.wal to add new invoice rules
The bot will automaticall create a new template for this invoice
Edit the template script to complete OCR

##  Running API endpoint 


## Running the bot

Move invoices as attachment emails to the Outlook inbox
To process invoices, run ```InvoiceBot.wal```

## Outlook Error diagnosis:
```
[USER DIR]\AppData\Local\IBM Robotic Process Automation\imap.log
```


