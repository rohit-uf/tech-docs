# Keycloak

## Documentation: [https://www.keycloak.org/](https://www.keycloak.org/)

## Configuration 

### Database: [DB](https://www.keycloak.org/server/db#_configuring_a_database)

### Server: [Server](https://www.keycloak.org/server/configuration)

- Edit configuration file in `conf/keycloak.conf`
- Can give path to custom configuration file with `-cf` flag

Sample Configuration File

```sh
  # Basic settings for running in production. Change accordingly before deploying the server.

  # Database

  # The database vendor.
  db=mysql
  db-url-host=localhost
  db-username=wordpress
  db-password=pwdfWP123

  # The full database JDBC URL. If not provided, a default URL is set based on the selected database vendor.
  #db-url=jdbc:postgresql://localhost/keycloak

  # Observability

  # If the server should expose healthcheck endpoints.
  #health-enabled=true

  # If the server should expose metrics endpoints.
  #metrics-enabled=true

  # HTTP

  # The file path to a server certificate or certificate chain in PEM format.
  #https-certificate-file=${kc.home.dir}conf/server.crt.pem

  # The file path to a private key in PEM format.
  #https-certificate-key-file=${kc.home.dir}conf/server.key.pem

  # The proxy address forwarding mode if the server is behind a reverse proxy.
  proxy=edge

  # Do not attach route to cookies and rely on the session affinity capabilities from reverse proxy
  #spi-sticky-session-encoder-infinispan-should-attach-route=false

  # Hostname for the Keycloak server.
  hostname=localhost
  hostname-port=8080
  hostname-strict-https=false
```

## Service Provider Interface | SPI

- [How to implement](https://www.keycloak.org/docs/latest/server_development/index.html#_providers)

### User Storage SPI
- [Tutorial](https://www.youtube.com/watch?v=1UklqPPjcRY)
- [JAVA Implementation](https://www.youtube.com/watch?v=1UklqPPjcRY&list=PLNn3plN7ZiaowUvKzKiJjYfWpp86u98iY)
