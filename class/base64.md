# About

Base64 encoding is a way of representing binary data using text (Specifically an ASCII string). You can read more about it [here](https://en.wikipedia.org/wiki/Base64).
This class requires the permission `base64` in order to use. Despite requiring a permission, access to base64 methods is not dangerous.
Some APIs require you to encode strings with Base64.

As base64 can represent binary, this means you can represent most things using it.
However there are a few gotchas you should be aware of:

1. Binary data's size in memory is significantly increased by encoding it in memory. Usually about [1.37 times](https://en.wikipedia.org/wiki/Base64#MIME) the original size.

2. You should not represent any unapproved image or other graphic to the user. Images on our platform pass through our automated filting process so that we can ensure copyright and content compliance.
