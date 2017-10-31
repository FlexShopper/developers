## PAYMENT METHOD
The FlexShopper payment method can be used on your website to capitalize on **_New_** customers.  We finance your customers shopping and pay you 100% of the retail price with no fees.  Read our documentation below to get started.

> View our [Payment Method Integration Docs Here](assets/FPayPaymentMethodDocumentationv2(1).pdf)

##### 4 Easy Steps
1. Review our [Payment Processor Documentation](assets/FPayPaymentMethodDocumentationv2(1).pdf) & [Shared API Endpoint Documentation](assets/SharedV2EndpointDocumentationV1.0.6.pdf)
2. Receive credentials
	- Retailer ID:
	- Retailer Token:
3. Integrate & test
	- Obtain a user test account from `integration @ flexshopper.com`
4. Implement marketing best practices
	- Use our [Go To Market Guide](assets/Go-To-Market-Guide.pdf)

**Payment Processor 5 Pillars of Success**
	- The payment processor integration is comprised of four major parts: The "Hidden Payment Form", "Handshake", "Shipping confirmation", and "Shared Services."

1. Payment Button
	- The payment button integrates with the vendor's website and allows customers to purchase products using the payment button without leaving the vendors website. More information can be found on our [Payment Method Documentation](assets/FPayPaymentMethodDocumentationv2(1).pdf)

2. GET/Transactions "Handshake"
	- This is a required endpoint used by the merchant consuming the payment processor to confirm the status of the transaction. Please reference the 'Transaction Status Endpoint (Final Handshake)' header on our [Shared API Endpoint Documentation](assets/SharedV2EndpointDocumentationV1.0.6.pdf)

3. Shipping Confirmation
	- This is a required endpoint used by the merchant to identify the date the item or items were delivered. Please reference the 'Transaction Item Shipment Confirmations' header on our [Shared API Endpoint Documentation](assets/SharedV2EndpointDocumentationV1.0.6.pdf)

4. Fulfillment Communication
   
   **Merchant sends shipping confirmation**
	- Full documentation for confirmations can be found under the 'Transaction Item Shipment Confirmations' header on our [API Documentation Page](assets/SharedV2EndpointDocumentationV1.0.6.pdf)
	- Format: email, csv, or xml/json
	- Post: `neworders @ flexshopper.com`, *our* ftp, or _our_ api
	- [Email example](assets/email-shipping.txt)
	- [CSV example](assets/example-shipment-tracking-file.csv)
	
	
**Shipping Date Estimation**
	- Some merchants can provide estimated dates of delivery without tracking numbers. Please reference the 'Transaction Item Delivery Date' header on our [API Documentation Page](assets/SharedV2EndpointDocumentationV1.0.6.pdf)
	
	
**FlexShopper pays Merchant**
	- Set payment terms
	- Send voided check for wire transfer
	- FlexShopper is exempt from taxes in all 50 states
5. Shared Services 
	- Shared Services is a combination of _Order Change_, _Ship Date Estimation_, _Cancellations_, _Returns_, and _Refunds/Credits_. All information on Shared
   Services can be found on our [Shared API Engpoint Documentation](assets/SharedV2EndpointDocumentationV1.0.6.pdf)
