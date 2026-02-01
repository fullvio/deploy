# Connect a container to Gluetun

There are various ways to connect a container to Gluetun.


## Container in the same docker-compose.yml

Add `network_mode: "service:gluetun"` to your second container so that it uses the `gluetun` network stack.

There is no need for `depends_on`.

## External container to Gluetun

Add `--network=container:gluetun` when launching the container, provided Gluetun is already running.

## Container in another docker-compose.yml

Add `network_mode: "container:gluetun"` to your *docker-compose.yml*, provided Gluetun is already running.
