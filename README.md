# docker-ip2tor

Thanks to [LounèsKMT](https://github.com/louneskmt) for this repository.

If you want to connect to your Umbrel Bitcoin Core node through RPC and Tor:

- Clone this repository
- Edit the config file under `ip2tor/config.yml`
  - Change the address value with your _Bitcoin Core RPC Host url (.onion)_
- `$ docker-compose up`
- Make request to your local port: `127.0.0.1:8332` with your Bitcoin Core RPC user and password.
  - Eg.: `curl --data-binary '{"jsonrpc":"1.0","id":"curltext","method":"getblockchaininfo","params":[]}' -H 'content-type:text/plain;' http://<user>:<password>=@127.0.0.1:8332/`

