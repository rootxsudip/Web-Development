# What can't in-browser JavaScript do?

1. Read / Write from computer hard disk.
2. You open an evil website and in another tab, you open FB now the evil website makes an ajax request to the FB website for getting its content(your private things) but the browser could not allow it because of the SOP(Same Origin Policy)
    - **Same Origin Policy** → The same-origin policy is a critical security mechanism that restricts how a document or script loaded from one origin can interact with a resource from another origin. It helps isolate potentially malicious documents, reducing possible attack vectors.

**Summary:** Your website can access permitted resources but can't access other websites because of the same-origin policy.