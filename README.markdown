About
=====

JS-AES is a JavaScript implementation of the Advanced Encryption Standard using Counter Mode.

The best way to understand the aes.js source code is to follow along with a FIPS 197, which you can download from 
http://csrc.nist.gov/publications/fips/fips197/fips-197.pdf

Usage
=====

After you include the aes.js file into your page, you can interact with it in the following manner:

Create two new crypto objects

    var aSide = new AES.Crypto(AES.generateKey());
    var bSide = new AES.Crypto(aSide.key);

Sync the two cryptos

    bSide.setCounter(aSide.getCounter());

Encryption

    var cipherText = aSide.encrypt("the quick brown fox jumped over the lazy dog");

Decryption

    var plainText = bSide.decrypt(cipherText);

Compare

    plainText == "the quick brown fox jumped over the lazy dog";

Feedback
========

If you have any questions, comments or just want to talk shop about crypto, feel free to reach me 
through my website at http://www.robertsosinski.com.
