# Nexmo-SMS-module
This is a module for Mendix which uses the Nexmo SMS service for sending text messages

# Dependencies 
Made in modeler 5.16.1, but the java and Jar file should be compatible with all versions of Mendix
Dependancy on the nexmo-sdk.jar that is included in the package, but otherwise can be downloaded from the nexmo website
Installation
Just call the java action for sending a message. The module itself can be deleted once you have moved the java-action to a logic place in your existing application

# Configuration

1. Go to https://dashboard.nexmo.com/sign-up to sign up

2. Activate account and log in

3. At the top right you see a tab API settings. Click on edit to see all the info you need to set this module up (your API Key and API secret). A screenshot of the page is included in the screenshots with this widget

4. If you are using a test account you need to add to which mobile numbers sms messages are allouwed to be sent. This is done on API settings page with the Test Phone Numbers fields.

5. In the Java action use these keys for sending your sms message

6. Make sure you format your mobile number correctly, with the country code and without spaces or plus signs.  The mobile number should be in international format, and one recipient per request. Ex: to=447525856424 or to=00447525856424 when sending to UK.

# Use

The Java action has the following inputs:
+ API Key : the key you can find in your nexmo account
+ API Secret: the secret you can find in your nexmo account
+ FromText: The name of the message sender
+ PhoneNr: The phone number in international format
+ Text: The message that has to be sent

# Pricing

Pricing per message in NL is €0.0490 and for UK: €0.0290
With registering Nexmo you recieve €2 euros to test with. Payment is easy with paypal or creditcard.
For more infomation go to https://www.nexmo.com/pricing/

# Limitations
Messages have a maximum length of 3200 characters in UTF-8 and URL encoded value. Ex: "Déjà vu" content would be "D%c3%a9j%c3%a0+vu"

As a general rule in SMS the maximum length for sender string is:
 + 11 characters maximum length for Alphanumeric Originators
 + 15 digits maximum length for Numeric Originators

# Known bugs 

None
