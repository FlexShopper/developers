## MARKETPLACE
Our Marketplace has three (3) parts to the integration: send FlexShopper your product feed, receive orders from FlexShopper, and handle cancelations or returns.  Please review the steps below and read our documentation.

> View our [Marketplace Integration Docs Here](https://github.com/FlexShopper/docs/blob/master/assets/Marketplace.pdf) & our full [API Documentation](assets/SharedV2EndpointDocumentation.pdf)

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
4. EDI integration 
    - Ask us about our EDI integration support `integration @ flexshopper.com`
 5. API Integration
 	- Ask us about our API integration support `integration @ flexshopper.com`


**RECEIVE ORDERS** <br/>
FlexShopper will send you order confirmations and expect shipping confirmations in return.  Once we have a shipment confirmation, we will process payment to you.

1. FlexShopper sends order file
	- Format: email, csv, or json
	- Post: email address, *our* ftp, or _your_ api
	- [Email example](https://github.com/FlexShopper/docs/blob/master/assets/email-order.txt)
	- [CSV example](https://github.com/FlexShopper/docs/blob/master/assets/example-order-submission.csv)
2. Merchant sends shipping confirmation
	- Full documentation for confirmations can be found under the 'Transaction Item Shipment Confirmations' header on our [API Documentation Page](file:///Users/Savage/Desktop/apollo/docs/assets/SharedV2EndpointDocumentation.pdf)
	- Format: email, csv, or xml/json
	- Post: `neworders @ flexshopper.com`, *our* ftp, or _our_ api
	- [Email example](https://github.com/FlexShopper/docs/blob/master/assets/email-shipping.txt)
	- [CSV example](https://github.com/FlexShopper/docs/blob/master/assets/example-shipment-tracking-file.csv)
	- EDI Integration upon request. Please send an email to `integration @ flexshopper.com`
3. Shipping Date Estimation
	- Some merchants can provide estimated dates of delivery without tracking numbers. Please reference the 'Transaction Item Delivery Date' header on our [API Documentation Page](file:///Users/Savage/Desktop/apollo/docs/assets/SharedV2EndpointDocumentation.pdf)
4. FlexShopper pays Merchant
	- Set payment terms
	- Send voided check for wire transfer
	- FlexShopper is exempt from taxes in all 50 states
		- Email `integration @ flexshopper.com` for our tax exempt certificates


**CANCEL ORDERS** <br/>
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
3. Customer requests a refund/credit
	- For a breakdown of the credit procedure please reference the 'Transaction Item Credits' header on our [API Documentation](/Users/Savage/Desktop/apollo/docs/assets/SharedV2EndpointDocumentation.pdf)
4. EDI Integration
	- EDI integration allows for cancellation of orders. Please send an email to `integration @ flexshopper.com` for more information. 

**RETURN ORDERS**
1. Customer contacts FlexShopper to return a product
	- A return occurs when a customer contacts FlexShopper to coordinate the return of a good to a vendor/store. Please reference the 'Transaction Item Returns' header on our [API Documentation](file:///Users/Savage/Desktop/apollo/docs/assets/SharedV2EndpointDocumentation.pdf)
