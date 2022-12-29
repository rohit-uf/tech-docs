# Authentication

1. Firebase provides `providerData` for a user. It contains name, email, phone number etc. 
2. Firebase ID Token is required in each authenticated requests. So custom properties should not be set in Custom Claims. [Ref](https://stackoverflow.com/questions/37415863/firebase-setting-additional-user-properties)
