# FAQ

### How does the extension work?

Privacy Pass is a browser extension written in JavaScript using the Chrome extension developer kit. This includes making use of the webRequest, webNavigation, cookie and tab frameworks. Privacy Pass can use triggers in HTTP responses (such as presence of headers) or via presence of HTML tags to initiate the signing and redemption procedures.

### Which cryptographic library is used?

Privacy Pass uses the [Stanford JavaScript Cryptography Library](https://github.com/bitwiseshiftleft/sjcl) (SJCL) for performing cryptographic operations. For elliptic-curve operations, Privacy Pass uses the NIST P-256 curve.

### Is the protocol provably secure?

In the near future, we hope to publish a paper detailing the security goals that we hope for our protocol to achieve. With these goals we also present proofs of security that assume the hardness of standard cryptographic assumptions such as the discrete log problem.

### What does Privacy Pass change about my browser experience?

Privacy Pass only stores data relating the tokens that are used creating 'passes'. Privacy Pass may also make changes to outgoing requests if a situation is deemed to instantiate either the signing or redemption phase of our protocol.

### What overheads do I incur from using Privacy Pass?

In preliminary tests on consumer hardware, our extension takes ~1.1 seconds to generate blinded tokens to be signed by the server and ~1.9 seconds to parse the signed tokens and verify the DLEQ proof. Creating a pass that can be used to redeem signed tokens takes <40ms.

### Who currently supports Privacy Pass?

Privacy Pass is currently supported by Cloudflare to help reduce the number of CAPTCHAs that need to be solved by honest users. The privacy-preserving aspect of Privacy Pass means that users can redeem tokens instead of solving more CAPTCHAs without compromising their anonymity.

### I want to contribute to Privacy Pass, what should I do?

Feel free to open a pull request on our GitHub [repository](https://github.com/privacypass/challenge-bypass-extension). This also applies to our [server implementation](https://github.com/privacypass/challenge-bypass-server).

### I want to support Privacy Pass, what should I do?

Great! the [server](https://github.com/privacypass/challenge-bypass-server) that we have written is open-sourced under the BSD-3 license. You can use this implementation or one of your own creation to construct a compatible server for the Privacy Pass extension. If the extension needs to be adapted to include support for your new server then get in contact with the Privacy Pass team or submit a PR yourself, as above.  

### I have found a bug in the protocol and/or implementation, what should I do?

Feel free to contact any member of the Privacy Pass team and they should be able to help. Otherwise open a PR as above, or create an issue in the GitHub issue tracker.