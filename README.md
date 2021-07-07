# Mango

How to run the final project -
1.	Change connection string in appsettings and run migrations for the following project (6 database will be created)
•	Mango.CouponAPI
•	Mango.Services.Email
•	Mango.Services.Identity
•	Mango.Services.OrderAPI
•	Mango.Services.ProductAPI
•	Mango.Services.ShoppingCartAPI
2.	Search term to change service bus connection string (do ctrl+shift+f and replace, should be 4 places) - sb://mangorestaurant
3.	Create the following queues and topics/subscriptions in Azure Service bus.
•	Queue - checkoutqueue
•	Topic 1 - checkoutmessagetopic
o	Subscription (Topic 1) - mangoOrderSubscription (subscription)
•	Topic 2 - orderpaymentprocesstopic
o	Subscription (Topic 2) - mangoPayment
•	Topic 3 - orderupdatepaymentresulttopic 
o	Subscription (Topic 3) - emailSubscription
o	Subscription (Topic 3) - mangoOrderSubscription
