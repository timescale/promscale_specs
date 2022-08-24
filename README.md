# Formal specifications for [Promscale](http://github.com/timescale/promscale) components

This is a nursery repo where we can play around with TLA+ specifications. 
It's likely we move out specifications once they are ready and commit them 
together with the feature they model.

### Running TLC headless

To run the TLC model checker over SSH (supposedly on a beefy AWS instance) one could use a command similar to the following (mind the paths, the number of cores and memory available):

```bash
java -XX:+UseParallelGC -Xmx119g -jar ./toolbox/tla2tools.jar -workers 64 -config ./promscale_specs/cache.cfg ./promscale_specs/cache.tla 2>&1 | tee tlc.log
```

See also: https://www.learntla.com/topics/cli.html