## Httpbeat as container

This is a distributable container bounded with the HTTPBeat. The beat is mainly
from this [Repo](https://github.com/christiangalsterer/httpbeat).

The entrypoint of the container is `./httpbeat -c ./beats/http.yml` with no configuration as to
load a configuration file in order to allow you to bind-mount a volume in the
`/opt/beats` directory and start with
```
./httpbeats -c ./beats/XXXX.yaml
```

Also you can set some environment variables in order to control the output of
the Elastic cluster.

```
ES_HOST (default localhost)
ES_PORT (default 9200)
CONSOLE (to output to stdout also, default true)
```
