# Post

Post gives a software agent that sends email a signed identity that anyone
can check: who wrote the message, what kind of sender it is, and on whose
behalf. It works over ordinary mail, and between endpoints that both speak
it, it carries structured data and receipts.

This repository holds the Internet-Draft, version 0:

- [`draft-pidgeon-post-00.txt`](draft-pidgeon-post-00.txt), and the same as
  [HTML](draft-pidgeon-post-00.html) and as
  [xml2rfc v3 source](draft-pidgeon-post-00.xml).
- [`vectors/`](vectors): the test vectors as JSON.
  - `post-v0.json`: discovery, the signed message, the agent declaration
    with a DKIM-signed message, the agent card and a signed receipt.
  - `ed25519.json`: strict Ed25519, including the signatures a lax
    verifier wrongly accepts.
  - `dkim-test-key.pem`: the throwaway key the DKIM vector is signed with.

Everything in the draft runs in production at
[Pidgeon](https://pidgeon.ai), except the signed receipt, which the draft
specifies ahead of the code. The draft is written for the IETF 127
hackathon (14–15 November 2026). It has not been submitted to the
datatracker yet, because submissions are closed until the meeting starts.

Comments and questions go in this repository's issues. The notes for a
second implementation are in the draft's appendix of the same name.

The draft text is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/),
and, once submitted, also under the IETF Trust's provisions (BCP 78).
