<h1 style="text-align:center;">
BITCOIN: Local realisation: Private to public, Elliptic curve,signature, verification, Asymmetric cryptography using BTC EC... 
</h1>

# Introduction <a class="title_class" id="title_1"></a>

### Why this project ?  <a class="title_class" id="title_2"></a>

In this project we will make our version of BTC protocol using only common libraries such NumPy, Hashlib.
<br> 
This project is for education prepose, please don't use it for real bitcoin transaction. 
* We will start by presenting the elliptic curve and its operations: addition, doubling, multiplication scalar / points.
* We will develop some functions to convert a private key to public key and to BTC address.
* We will developpe also functions for signature and verification.
* In the end, we will introduce the ECDH key agreement protocol and use it in AES secure cryptography/communication

<div style="text-align: center;">
    <img src="BTC_EC.PNG" style="width: 50%;text-align: center;">
</div>

# Table of contents
 * [Introduction](#title_1)
     * [Why this project ? ](#title_2)
 * [Table of contents](#title_3)
 * [Elliptic curve cryptography of the BTC Secp256K1](#title_4)
     * [General libraries](#title_5)
     * [General case $y^2=x^3+a x^2+b$](#title_6)
   * [Bitcoin elliptic curve $y^2=x^3+7$](#title_7)
     * [Bitcoin elliptic curve: Add 2 points and Doubling a point: Illustration](#title_8)
     * [Bitcoin elliptic curve: Add 2 points and Doubling a point: for integers](#title_9)
     * [Secp256K1 Parameters](#title_10)
     * [Point additions (P+Q), point double (2P) for integers](#title_11)
     * [Scalar and point multiplication (k.P) for integers](#title_12)
   * [Private key to Public key](#title_13)
     * [Test private to public key using local vs ecdsa library](#title_14)
 * [Pubilc key to BTC add](#title_15)
   * [Compressed <=> Uncompressed public key convertion](#title_16)
   * [Base 58](#title_17)
   * [Public key to BTC address](#title_18)
 * [BTC signature and verification](#title_19)
     * [Signature](#title_20)
     * [Verification](#title_21)
     * [Test the siganture and verification](#title_22)
 * [Elliptic-curve Diffie–Hellman (ECDH) ](#title_23)
     * [Generate the common key](#title_24)
     * [AES communication using the common key](#title_25)
 * [Sources](#title_26)
