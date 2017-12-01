A simple example of using `docker-compose` with the Akamai ESI Test Server. A barebones NodeJS server
returns raw ESI, which is processed by the ESI Test Server.

Set the usual CLI arguments via the `ETS_CLI_ARGS` environment variable instead.

Using this example:
* `docker-compose up -d`
* `curl -H 'Host: nodejs.test' "http://localhost:8080?value=foo"`
* `docker-compose up -d`

The value of the query string parameter `value` will be echoed back.