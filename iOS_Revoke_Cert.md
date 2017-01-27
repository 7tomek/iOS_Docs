# iOS Revoke Cert

***
If the computer who requested the distribution certificate is available (or there is a backup of the distribution assets somewhere)

* From the computer where the distribution asset was generated, open Xcode.
* Click on Window, Organizer.
* Expand the Teams section.
* Select your team, select the certificate of "iOS Distribution" type, click Export and follow the instructions.
* Save the exported file and go to your computer.
* Repeat steps 1-3.
* Click Import and select the file you exported before.

If the computer where the distribution profile was created is not accessible anymore (and there is not a backup)

***
You have to revoke the certificate and create a new one.
You may need to ask your team admin or agent to give you some privileges in order to generate distribution certificates. Once you have enough privileges, follow these steps (accurate as of 15-May-2013):

* Go to this webpage: https://developer.apple.com/devcenter/ios/index.action
* Click on "Member Center" and enter your iOS developer credentials.
* Click on "Certificates, Identifiers & Profiles".
* Click on "Certificates" under the "iOS Apps" section.
* Expand the Certificates section on the left, select Distribution, and click on your distribution certificate.
* Click Revoke and follow the instructions.
* Click on the plus sign to add a new certificate.
* Select "App Store and Ad Hoc" option, and click Continue.
* Follow the steps printed in the webpage. That involves opening the Keychain application on your Mac and generate a Certificate Signing Request from there. Click Continue.
* Upload the .csr file and click Continue.

A certificate is generated for distribution. Download it and double click it to integrate it in your keychain.
Reopen Xcode and check your project configuration to see if you can now select an "iPhone Distribution" certificate (i.e. it's not grayed out).
