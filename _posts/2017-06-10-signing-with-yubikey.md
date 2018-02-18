I want to sign my releases with my Yubikey on my MBP.

brew install opensc yubico-piv-tool

https://developers.yubico.com/PIV/Guides/Android_code_signing.html

https://geoffreymetais.github.io/code/key-signing/

Make a cfg file in dotfiles

// Updated 6/30/2017

1. Manually signed builds via Android Studio.
2. Found how to sign release builds via Gradle
3. Figured out how to Google Play App Signing
  a. Encrypt and upload signing key to Google
  b. Create an upload key and share cert with Google
4. Now release builds are built and signed by ./gradlew assembleRelease


Currently out of scope
* The above work to use the Yubikey to sign seems unnecessary without another machine to work on.  Eventually!
* Upload release builds to Google via Gradle