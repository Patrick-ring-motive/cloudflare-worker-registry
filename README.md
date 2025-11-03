# cloudflare-worker-registry
Registry for overflow cloudflare workers

My primary cloudflare account has hit the limit of 100 workers per free account.
This project serves as a remote registry to dynamically load worker code individually.
The `hostMap` serves as a direct map for host to dynamically loaded worker file.
`hostMatch` serves as an alternative to us regex to map a host to a worker file.
