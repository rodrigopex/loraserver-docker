# Docker Images for [LoRa Server](https://github.com/brocaar/loraserver) and [LoRa App Server](https://github.com/brocaar/lora-app-server)

LoRa Server - open source LoRaWAN network-server created by [Orne Brocaar](http://www.brocaar.com/).

Supported versions:

 * v1.1.0

   * LoRa Server: 0.19.1
   * LoRa App Server: 0.10.1

 * v1.0.0
   
   * LoRa Server: 0.16.1
   * LoRa App Server: 0.7.2

## Deploy

1. Clone the repository:

    ```
    git clone https://github.com/ceratop/loraserver-docker.git

    git checkout v1.1.0
    ```
1. Change the default configuration and generate certificates _(optional)_:

    Change the following envars in `docker-compose.yml`:
     
     * `POSTGRES_PASSWORD`
     * `LORASERVER_DB_PASSWORD`
     * `LORAAPPSERVER_DB_PASSWORD`
     * `NET_ID`
     * `BAND`
     * `JWT_SECRET`
   
   Generate the certificates and put them in `lora-app-server/certs` folder by replacing `default.crt` and `default.key` files.
   
1. All set! Run:

   ```
   docker-compose up -d
   ```
   
   and go to `https://<host>`.
   
## License

MIT License.
