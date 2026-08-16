# Changelog

All notable changes to this repository will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## Unreleased

### Upgrade Notes

### Known Issues

### Added

Added Sonarqube scanner

### Changed

- **Performance**: Disabled Nagle's algorithm (`TCP_NODELAY = 1`) on accepted sockets for lower latency.
- **Performance**: Passed `buffer_size` (now defaults to `65536`) to `SO_RCVBUF` and `SO_SNDBUF`.
- **Performance**: Changed subscription initialization to use `raw=True` for zero-copy receipt of ROS 2 messages.
- **Performance**: Updated TCP send path to support zero-copy routing of raw bytes (avoiding re-serialization).

### Deprecated

### Removed

### Fixed

- **Performance/Bug**: Replaced busy-waiting with a 100% CPU usage loop in `service.py` with an event-driven `threading.Event` mechanism.
- **Performance**: Fixed an unnecessary buffer allocation copy in `client.py`'s `recvall` by returning the `bytearray` directly.
- **Cleanup**: Removed a meaningless return value in the subscriber callback.

## [0.7.0] - 2022-02-01

### Added

Added Sonarqube scanner

Send information during hand shaking for ros and package version checks

Send service response as one queue item


## [0.6.0] - 2021-09-30

Add the [Close Stale Issues](https://github.com/marketplace/actions/close-stale-issues) action

### Upgrade Notes

### Known Issues

### Added

Support for queue_size and latch for publishers. (https://github.com/Unity-Technologies/ROS-TCP-Endpoint/issues/82)

### Changed

### Deprecated

### Removed

### Fixed

## [0.5.0] - 2021-07-15

### Upgrade Notes

Upgrade the ROS communication to support ROS2 with Unity

### Known Issues

### Added

### Changed

### Deprecated

### Removed

### Fixed

## [0.4.0] - 2021-05-27

Note: the logs only reflects the changes from version 0.3.0

### Upgrade Notes

RosConnection 2.0: maintain a single constant connection from Unity to the Endpoint. This is more efficient than opening one connection per message, and it eliminates a whole bunch of user issues caused by ROS being unable to connect to Unity due to firewalls, proxies, etc.

### Known Issues

### Added

Add a link to the Robotics forum, and add a config.yml to add a link in the Github Issues page

Add linter, unit tests, and test coverage reporting

### Changed

Improving the performance of the read_message in client.py, This is done by receiving the entire message all at once instead of reading 1024 byte chunks and stitching them together as you go.

### Deprecated

### Removed

Remove outdated handshake references

### Fixed
