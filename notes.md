# HTTP observations (Lab 4, Task 1)

| Question | My answer |
|----------|-----------|
| Request method for index.html |GET|
| Status code with Disable cache ticked | 200 |
| Status code on a normal reload | 304 |
| Status code for /nothing-here.html | 404 |
| Value of the Content-Type response header | text/html; charset=utf-8  |
| Remote Address (IP and port) | 127.0.0.1:5500 |
| Protocol in the address bar (http or https) | http |

## Why is this address http and not https?

Localhost traffic stays entirely inside your own computer and never travels across the public internet where it could be intercepted. Because of this isolation, there is no risk of network eavesdropping, making the encryption and security certificates of HTTPS unnecessary for basic local development.
