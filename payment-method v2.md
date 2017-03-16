## PAYMENT METHOD
The FlexShopper payment method can be used on your website to capitalize on **_New_** customers.  We finance your customers shopping and pay you 100% of the retail price with no fees.  Read our documentation below to get started.

> View our [Payment Method Integration Docs Here](/Users/Savage/Desktop/apollo/docs/assets/FPayPaymentMethodDocumentationv2 (1).pdf)

##### 4 Easy Steps
1. Review our [Payment Processor Documentation](/Users/Savage/Desktop/apollo/docs/assets/FPayPaymentMethodDocumentationv2 (1).pdf) & [Shared API Endpoint Documentation](/Users/Savage/Desktop/apollo/docs/assets/SharedV2EndpointDocumentation.pdf)
2. Receive credentials
	- Retailer ID:
	- Retailer Token:
3. Integrate & test
	- Obtain a user test account from `integration @ flexshopper.com`
4. Implement marketing best practices
	- Use our [Go To Market Guide](https://github.com/FlexShopper/docs/blob/master/assets/Go-To-Market-Guide.pdf)

**Payment Processor 5 Pillars of Success**<br>
	- The payment processor integration is comprised of four major parts: The "Hidden Payment Form", "Handshake", "Shipping confirmation", and "Shared Services."
1. Payment Button
	- 
2. GET/Transactions "Handshake"
	- This is a required endpoint used by the merchant consuming the payment processor to confirm the status of the transaction. Please reference the 'Transaction Status Endpoint (Final Handshake)' header on our [Shared API Endpoint Documentation](file:///Users/Savage/Desktop/apollo/docs/assets/SharedV2EndpointDocumentation.pdf)
3. Shipping Confirmation
	- This is a required endpoint used by the merchant to identify the date the item or items were delivered. Please reference the 'Transaction Item Shipment Confirmations' header on our [Shared API Endpoint Documentation](file:///Users/Savage/Desktop/apollo/docs/assets/SharedV2EndpointDocumentation.pdf)
4. Fulfillment Communication<br>
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>Merchant sends shipping confirmation</b>
	- Full documentation for confirmations can be found under the 'Transaction Item Shipment Confirmations' header on our [API Documentation Page](file:///Users/Savage/Desktop/apollo/docs/assets/SharedV2EndpointDocumentation.pdf)
	- Format: email, csv, or xml/json
	- Post: `neworders @ flexshopper.com`, *our* ftp, or _our_ api
	- [Email example](https://github.com/FlexShopper/docs/blob/master/assets/email-shipping.txt)
	- [CSV example](https://github.com/FlexShopper/docs/blob/master/assets/example-shipment-tracking-file.csv)
	<br>
	<br>
<b>Shipping Date Estimation</b>
	- Some merchants can provide estimated dates of delivery without tracking numbers. Please reference the 'Transaction Item Delivery Date' header on our [API Documentation Page](file:///Users/Savage/Desktop/apollo/docs/assets/SharedV2EndpointDocumentation.pdf)
	<br>
	<br>
<b>FlexShopper pays Merchant</b>
	- Set payment terms
	- Send voided check for wire transfer
	- FlexShopper is exempt from taxes in all 50 states
5. Shared Services 
	- Shared Services is a combination of <i>Order Change</i>, <i>Ship Date Estimation</i>, <i>Cancellations</i>, <i>Returns</i>, and <i>Refunds/Credits</i>. All information on Shared
   Services can be found on our [Shared API Engpoint Documentation](file:///Users/Savage/Desktop/apollo/docs/assets/SharedV2EndpointDocumentation.pdf)