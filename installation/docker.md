# Fluent Bit Docker Images

Fluent Bit container image is also available on Docker Hub ready for production usage. The following table describe the tags are available on [fluent/fluent-bit](https://hub.docker.com/r/fluent/fluent-bit/) repository:

| Tag(s)       | Description                                                                        |
|--------------|------------------------------------------------------------------------------------|
| 0.12, latest | Latest release of 0.12 stable series                                               |
| 0.12.8       | Container image of Fluent Bit [v0.12.8](http://fluentbit.io/announcements/v0.12.8) |
| 0.12.7       | Container image of Fluent Bit [v0.12.7](http://fluentbit.io/announcements/v0.12.7) |
| 0.12.6       | Container image of Fluent Bit [v0.12.6](http://fluentbit.io/announcements/v0.12.6) |
| 0.12.5       | Container image of Fluent Bit [v0.12.5](http://fluentbit.io/announcements/v0.12.5) |
| 0.12.4       | Container image of Fluent Bit [v0.12.4](http://fluentbit.io/announcements/v0.12.4) |
| 0.12.3       | Container image of Fluent Bit [v0.12.3](http://fluentbit.io/announcements/v0.12.3) |
| 0.12.2       | Container image of Fluent Bit [v0.12.2](http://fluentbit.io/announcements/v0.12.2) |
| 0.12.1       | Container image of Fluent Bit [v0.12.1](http://fluentbit.io/announcements/v0.12.1) |
| 0.12.0       | Container image of Fluent Bit [v0.12.0](http://fluentbit.io/announcements/v0.12.0) |

It's strongly suggested that you always use the latest image of Fluent Bit.

## Getting Started

Download the last stable image from 0.12 series:

```
$ docker pull fluent/fluent-bit:0.12
```

Once the image is in place, now run the following (useless) test which makes Fluent Bit meassure CPU usage by the container:

```
$ docker run -ti fluent/fluent-bit:0.12 /fluent-bit/bin/fluent-bit -i cpu -o stdout -f 1
```

That command will let Fluent Bit meassure CPU usage every second and flush the results to the standard output, e.g:


```
Fluent-Bit v0.12.8
Copyright (C) Treasure Data

[2017/11/07 14:29:02] [ info] [engine] started
[0] cpu.0: [1504290543.000487750, {"cpu_p"=>0.750000, "user_p"=>0.250000, "system_p"=>0.500000, "cpu0.p_cpu"=>0.000000, "cpu0.p_user"=>0.000000, "cpu0.p_system"=>0.000000, "cpu1.p_cpu"=>1.000000, "cpu1.p_user"=>0.000000, "cpu1.p_system"=>1.000000, "cpu2.p_cpu"=>1.000000, "cpu2.p_user"=>1.000000, "cpu2.p_system"=>0.000000, "cpu3.p_cpu"=>0.000000, "cpu3.p_user"=>0.000000, "cpu3.p_system"=>0.000000}]
```
