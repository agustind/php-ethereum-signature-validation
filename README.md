## PHP library to validate Ethereum signatures

If you want to authenticate a user via an Ethereum wallet from PHP, or restrict certain server-side functionalities to only allowed wallets,
you can request for a signed message on the frontend using a library like Ethers.js or Web3.js and pass the wallet address and signature as parameters
to the server. This library will validate if the signature is valid and was indeed created by the specified wallet address.
## Usage

```php
<?php

use Agustind\Ethsignature;
$signature = new Ethsignature();

// from the frontend, via Ethers.js or Web3.js, the wallet 0x123456789 signs the message 'hello world' and generates the signature 'xxxxyyyyzzzz'
$is_valid = $signature->verify('hello world', 'xxxxyyyyzzzz', '0x123456789');
// true

```




[![Ethereum](https://user-images.githubusercontent.com/725986/61891022-0d0c7f00-af09-11e9-829f-096c039bbbfa.png) 0x8cA54b378C177db1cfde63231f9eA32fa7943036][Ethereum]

[Ethereum]: https://etherscan.io/address/0x8cA54b378C177db1cfde63231f9eA32fa7943036 "Donate with Ethereum"
