## MARKETPLACE
Our Marketplace has three (3) parts to the integration: send FlexShopper your product feed, receive orders from FlexShopper, and handle cancelations or returns.  Please review the steps below and read our documentation.

> View our [Marketplace Integration Docs Here](https://github.com/FlexShopper/docs/blob/master/assets/Marketplace.pdf)

**SEND YOUR PRODUCTS** <br/>
After a Merchant prepares their product feed, they can send it to FlexShopper through our FTP Server.  We support both SFTP and FTP.  Once you have received credentials and whitelisted your server, please refer to our FTP Instructions.

1. Merchant prepares feed.  
	- National distribution feed
	- Zip code restricted feed
		- Include a separate list of zip codes
	- [Feed example](https://github.com/FlexShopper/docs/blob/master/assets/example-feed.csv)
2. Merchant sets shipping price
  	- Options: flat price or submit with feed
3. Merchant sends feed via s/ftp
	- FlexShopper provides s/ftp credentials
	- Merchant provides ip for FlexShopper to whitelist


**RECEIVE ORDERS** <br/>
FlexShopper will send you order confirmations and expect shipping confirmations in return.  Once we have a shipment confirmation, we will process payment to you.

1. FlexShopper sends order file
	- Format: email, csv, or json
	- Post: email address, *our* ftp, or _your_ api
	- [Email example](https://github.com/FlexShopper/docs/blob/master/assets/email-order.txt)
	- [CSV example](https://github.com/FlexShopper/docs/blob/master/assets/example-order-submission.csv)
2. Merchant sends shipping confirmation
	- Format: email, csv, or xml/json
	- Post: `neworders @ flexshopper.com`, *our* ftp, or _our_ api
	- [Email example](https://github.com/FlexShopper/docs/blob/master/assets/email-shipping.txt)
	- [CSV example](https://github.com/FlexShopper/docs/blob/master/assets/example-shipment-tracking-file.csv)
3. FlexShopper pays Merchant
	- Set payment terms
	- Send voided check for wire transfer
	- FlexShopper is exempt from taxes in all 50 states
		- Email `development @ flexshopper.com` for our tax exempt certificates


**CANCEL/ RETURN ORDERS** <br/>
Cancellations and returns typically occur through one of two scenarios.  Either the Customer contacts FlexShopper to cancel the order and we contact our Vendor, or the Vendor can not fulfill the order and we contact the Customer.

1. FlexShopper sends cancellation request
	- Format: call, email, csv, or json
	- Post: customer service #, email address, *our* ftp, or _your_ api
	- [CSV example](https://github.com/FlexShopper/docs/blob/master/assets/example-order-change.csv)
2. Merchant sends cancellation request
	- Format: call, email, csv, or json
	- Post: **(855) 353-9289**, `neworders @ flexshopper.com`, *our* ftp, or _our_ api
	- FlexShopper Customer Service notifies customer of cancellation
	- [CSV example](https://github.com/FlexShopper/docs/blob/master/assets/example-order-change.csv)
