<img align="left" width="80" height="80" src="./src/assets/main_icon.png" alt="Moonshine Icon">

# Moonshine
Moonshine's alpha is available for testing on [iOS](https://testflight.apple.com/join/yTLqj9Xn) & [Android](https://play.google.com/store/apps/details?id=com.kisswallet)

<p style="align-items: center">
  <img src="./src/assets/screenshots/send_transaction.png" width="33%" alt="Send Transaction" />
  <img src="./src/assets/screenshots/main.png" width="33%" alt="Main"/> 
  <img src="./src/assets/screenshots/receive_transaction.png" width="33%" alt="Receive Transaction" />
</p>

> Moonshine is a homebrewed, open-source, non-custodial, Bitcoin/Litecoin Electrum wallet for iOS & Android.

CAUTION: **Caution:**
This app is still heavily in development. Please use at your own risk.

Built with React Native, Moonshine utilizes Electrum's JSON-RPC methods to interact with the Bitcoin/Litecoin network.

Moonshine's intended use is as a hot wallet.
Meaning, your keys are only as safe as the device you install this wallet on.
As with any hot wallet, please ensure that you keep only a small, responsible amount of Bitcoin/Litecoin on it at any given time.

If you are looking for secure cold storage solutions please consider purchasing a [Trezor](https://wallet.trezor.io) or a [Ledger](https://www.ledger.com/)

### Installation
1. First and foremost, we need to generate the Lndmobile.aar & Lndmobile.framework files.
    - Option 1 - Generate them locally:
        - To generate these files, please follow the instructions detailed in the README of Lightning Lab's Lightning App [here.](https://github.com/lightninglabs/lightning-app/tree/master/mobile)
    - Option 2 - Download pre-generated files:
        - If you do not wish to generate these files locally you can download them [here](https://github.com/coreyphillips/moonshine/releases/tag/v0.2.0-2) instead. However, I highly recommend you opt for option 1.
2. Clone Moonshine and Install Dependencies:
   ```
    git clone https://github.com/coreyphillips/moonshine
    cd moonshine
    yarn install
    ```
3. Add the Lndmobile.aar & Lndmobile.framework files to the project:
    - Add the Lndmobile.aar file to `moonshine/android/Lndmobile`
    - Add the Lndmobile.framework file to `moonshine/ios/lightning`

4. Start the project:
    - iOS: `react-native run-ios`
    - Android: `react-native run-android`
### Feature Roadmap
* Complete:
    * Bitcoin/Litecoin Mainnet & Testnet supported
    * Bech32 support
    * Multiple wallet support
    * Electrum
        * Support for both random and custom peers
    * Encrypted storage
    * Biometric + Pin authentication
    * Custom fee selection
    * Import mnemonic phrases via manual entry or scanning
    * RBF functionality
    * Add BIP39 Passphrase functionality
    * Add support for Segwit-compatible & legacy addresses in settings
    * Allow users to select the key derivation path in settings
    * Support individual private key sweeping
    * *Partially Complete (0.1.1)* - Add support for UTXO blacklisting - Blacklist functionality can be accessed via the Transaction Detail view for now.
        * This allows users to blacklist any utxo that they do not wish to include in their list of available utxo's when sending transactions. Blacklisting a utxo excludes it's amount from the wallet's total balance.
    * Ability to Sign & Verify Messages
    * Support BitID for passwordless authentication

* In Progress:
    * Add a UTXO selector to create custom transactions
        * This will allow users to select from a list of available utxo's to include in their transaction.
    * Add support for additional fiat currencies in the settings

For a complete, up-to-date list of in-progress features please refer to Moonshine's [issue page.](https://github.com/coreyphillips/moonshine/issues)
If you do not see a feature that you want feel free to create a new issue requesting it or reach out at support@ferrymanfin.com and let me know.

### Contributing

1. Fork it (<https://github.com/coreyphillips/moonshine>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

### Altcoin Support
Please be aware and take note that my primary focus is on expanding the core functionality of this wallet and not on adding altcoins. However, for those wishing to add a specific altcoin for personal use, I have created the following guide so that you may fork off in a proper fashion:
[Altcoin Implementation Guide](https://gist.github.com/coreyphillips/91de5d15964797054988522664cc3150)
 
 If you have any questions regarding this guide I'm always happy to help so don't hesitate to reach out.

### Support

Supported Derivation Paths: m/0' | 44' | 49' | 84' /0'/0'

Again, if you have any questions, feature requests, etc., please feel free to create an issue on [Github](https://github.com/coreyphillips/moonshine/issues), reach out to me on [Twitter](https://twitter.com/coreylphillips) or send an email to corey@ferrymanfin.com.

### Donate

I built this app to learn and have fun. I never intend to monetize or turn a profit on this app so if you found it useful, cool or interesting please consider donating:

 - **Bitcoin:** bc1qm6knmtrk5jfyt57rwkm8j74kxskxyrl504tlc9
 - **Bitcoin Testnet:** tb1qxvg88t7a498yfdxgs4rjaz3r75dyr64h5r5wd7
 - **Litecoin:** ltc1qrctkm565xale82pjt6nsxsyvvmln2qz8dpf6q9
 - **Litecoin Testnet:** tltc1qxvg88t7a498yfdxgs4rjaz3r75dyr64hdtksah

### Meta

Corey Phillips – [@coreylphillips](https://twitter.com/coreylphillips)

Distributed under the MIT license. See ``LICENSE`` for more information.

[https://github.com/coreyphillips/moonshine](https://github.com/coreyphillips/moonshine)

### License [MIT](https://github.com/coreyphillips/moonshine/blob/master/LICENSE)

### Acknowledgments
* Giant shoutout to the authors and contributors of the following projects along with everyone who has taken the time to provide feedback and help me through this process of learning and development. You are all awesome:
    * [bitcoinjs-lib](https://github.com/bitcoinjs/bitcoinjs-lib)
        * For providing a powerful library with detailed documentation capable of handling all of the necessary client-side, Bitcoin-related heavy-lifting.
    * [Electrum](https://electrum.org)
        * For providing a simple and flexible way to interact with the Bitcoin network.
    * [Lightning-App](https://github.com/lightninglabs/lightning-app)
        * For providing the initial inspiration for the main UI of this app and for providing a wonderful guide/example of how to implement Lightning via Neutrino.
