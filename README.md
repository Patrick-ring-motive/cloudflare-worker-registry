# cloudflare-worker-registry 🚀
# cloudflare-worker-registry
Registry for overflow cloudflare workers

My primary cloudflare account has hit the limit of 100 workers per free account.
This project serves as a remote registry to dynamically load worker code individually.
The `hostMap` serves as a direct map for host to dynamically loaded worker file.
`hostMatch` serves as an alternative to us regex to map a host to a worker file.
# cloudflare-worker-registry 🚀

`cloudflare-worker-registry` is a remote registry system designed to bypass Cloudflare's 100-worker limit on free accounts by dynamically loading worker code.

## How it Works

When a Cloudflare account reaches its limit, this registry allows you to host worker code externally and load it dynamically based on the incoming request's host.

### Registry Configuration

The system uses `registry.json` to manage the mapping between hosts and their corresponding worker scripts.

- **`hostMap`**: A direct mapping of specific hostnames to worker file paths.
- **`hostMatch`**: An alternative mapping that uses regular expressions to match hosts to worker files.

## Project Structure

- **`switchboard/`**: Contains the core logic for routing and loading workers.
- **`registry.json`**: The central configuration file for host-to-worker mappings.

## Setup

1. Configure your host mappings in `registry.json`.
2. Deploy the switchboard logic to your primary Cloudflare account.
3. The switchboard will intercept requests and dynamically fetch the appropriate worker code from the registry.

