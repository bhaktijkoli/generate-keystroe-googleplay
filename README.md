# generate-keystroe-googleplay

1. Follow the instructions in the [Android Studio Help Center](https://developer.android.com/studio/publish/app-signing#generate-key) to generate a new key. It must be different from any previous keys. Alternatively, you can use the following command line to generate a new key:

``keytool -genkeypair -alias upload -keyalg RSA -keysize 2048 -validity 9125 -keystore keystore.jks``

This key must be a 2048 bit RSA key and have 25-year validity.

2. Export the certificate for that key to PEM format:

``keytool -export -rfc -alias upload -file upload_certificate.pem -keystore keystore.jks`` 

3. Upload the PEM file to google play console
