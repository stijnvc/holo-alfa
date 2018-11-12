---
layout: post
title: Digital signature
categories: [blog, nodejs]
tags: [node, nodejs, crypto, signature]
---

In this post i'll give a simple example of how you can sign (digitally) with builtin crypto (node.js) module.

Digital signature is a mathematical process that tries to ensure the contents of message has not been changed after creation.

This process involve signing the document (message) using some private key and hash function.

The result of the process + public key constructs the Digital signature.

If someone would like to confront the message has not been altered, a validation process involving the
original message and the Digital signature can check this.

Ok, it's time to see some code:
In this tutorial we would use openssl for creating private/public key pair

Let's grab some public/private key pair:

{% highlight shell%}
openssl genrsa -out rsa_1024_private.pem 1024
openssl rsa -pubout -in rsa_1024_private.pem -out rsa_1024_public.pem
{% endhighlight %}

We created a private/public key pair named **rsa_1024_private.pem** and **rsa_1024_public.pem**

Signing a message using the private key:

{% highlight js%}
const crypto = require('crypto')
...
function sign(message) {
    const sign = crypto.createSign('sha384')
    sign.update(message)
    return sign.sign(privateKey, 'hex')
}
{% endhighlight %}
Where:
 - **privateKey** is the key we created earlier
 - i choose **sha384** as the hash algorithm, you can find an array of supported algrithm
    if you run 'crypto.getHashes()'

Now let's try to validate the signature using the public key:

{% highlight js%}
function validate(message, signature) {
    const verify = crypto.createVerify('sha384')
    verify.update(message)
    return verify.verify(publicKey, signature, 'hex')
}
{% endhighlight %}
Where:
 - **publicKey** is the key we created earlier
 - validate returns boolean (true if the signature is valid)



You can find the full code [here](https://github.com/adibiton/digitial-signature-service)
