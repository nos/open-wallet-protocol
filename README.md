# Open Wallet Protocol

**NOTE: Not yet standardized!**

## Introduction

The [Open Wallet protocol](https://openwalletprotocol.org) enables any web page to add cryptocurrency addresses which other software can interact with.

Open Wallet protocol follows the same semantics as the Open Graph protocol, to make the experience of adding meta properties containing cryptocurrency wallets feel familiar.

## Basic Metadata

To add wallet addresses into your web page, you need to add basic metadata to
your page. We've based the initial version of the protocol on
<a href="http://en.wikipedia.org/wiki/RDFa">RDFa</a> which means that you'll place
additional <code>&lt;meta&gt;</code> tags in the <code>&lt;head&gt;</code> of your web page. The 
meta tag for a cryptocurrency wallet is:

<p> <code>&lt;meta name="wallet:{ticker}" content="{address}" /&gt;</code> </p>

<p>The <i><code>name</code></i> attribute should contain the representation of the wallet’s primary belonging cryptocurrency ticker in lowercase. For example “btc” for Bitcoin and “eth” for Ethereum.</p>

<p>The <i><code>content</code></i> attribute should contain the wallet’s full public address.</p>

<p>As an example, the following is the Open Wallet markup for the Genesis Bitcoin Address:</p>

```html
<html>
<head>
<title>My Web App</title>
<meta name="wallet:btc" content="1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa" />
...
</head>
...
</html>
```
