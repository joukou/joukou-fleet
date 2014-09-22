Joukou Fleet Units
==================
[![Apache 2.0](http://img.shields.io/badge/License-Apache%202.0-brightgreen.svg)](#license) [![Stories in Ready](https://badge.waffle.io/joukou/joukou-fleet.png?label=ready&title=Ready)](http://waffle.io/joukou/joukou-fleet) [![IRC](http://img.shields.io/badge/IRC-%23joukou-blue.svg)](http://webchat.freenode.net/?channels=joukou)

![](http://media.giphy.com/media/123EKEzenhM2dy/giphy.gif)

Fleet units for [Joukou](https://joukou.com) intended for use with
[CoreOS](https://coreos.com).

This does not include Fleet units for Joukou Circles, as those are managed by
the [Conductor](https://github.com/joukou/joukou-conductor) which interacts
directly with the Fleet HTTP API.

## Usage

Units are written as [template unit files](https://github.com/coreos/fleet/blob/master/Documentation/unit-files-and-scheduling.md#template-unit-files).

Example of starting 3 instances of the cAdvisor unit:

```
$ fleetctl submit cadvisor\@.service
$ fleetctl start cadvisor\@{1,2,3}.service
```

There is a convenience script to deploy the entire fleet to a cluster of N hosts:

```
$ ./bin/deploy 3
```

Likewise to destroy the entire fleet:

```
$ ./bin/destroy 3
```

## License

Copyright &copy; 2014 Joukou Ltd.

Joukou Fleet Units is under the Apache 2.0 license. See the
[LICENSE](LICENSE) file for details.

[![Analytics](https://ga-beacon.appspot.com/UA-41911221-2/joukou-fleet/readme)](https://github.com/igrigorik/ga-beacon)
