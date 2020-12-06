# Example beam + Go + Flink

## Install system software

1. Follow [official Docker instructions](https://docs.docker.com/engine/install/ubuntu/) for to install docker.

2. Follow the "Portable (Java/Python/Go)"
   [instructions](https://beam.apache.org/documentation/runners/flink/) on the
   beam website.


## Run the example

In one terminal:

```shell
docker run --net=host apache/beam_flink1.10_job_server:latest
```

In another terminal:

```shell
go run cmd/beamgo_pipeline/beamgo_pipeline.go --runner flink --endpoint localhost:8099 --output /tmp/output-flink.txt  --environment_type LOOPBACK
```
