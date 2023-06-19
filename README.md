# Shaded Netty for gRPC in Apache RocketMQ

[![License][license-image]][license-url]
[![build][build-image]][build-url]
[![Maven Central][maven-image]][maven-url]

## Introduction

This project aims to provide shaded Netty packages that are not included in grpc-java client,
allowing for the utilization of additional features in gRPC services within [Apache RocketMQ](https://rocketmq.apache.org/).

## Requirements

- Java 1.8 or later

## Getting Started

Add the following dependency to your project. Remember to replace `ROCKETMQ-GRPC-NETTY-VERSION` with
the [latest release](https://search.maven.org/search?q=g:io.github.aliyunmq%20AND%20a:rocketmq-logging).

```xml
<dependencies>
    <dependency>
        <groupId>io.github.aliyunmq</groupId>
        <artifactId>rocketmq-grpc-netty-codec-haproxy</artifactId>
        <version>ROCKETMQ-GRPC-NETTY-VERSION</version>
    </dependency>
</dependencies>
```

## Manual Release

Set the password in your `settings.xml` for repositories: `sonatype-nexus-snapshots-aliyunmq`
and `sonatype-nexus-staging-aliyunmq`, then execute the command below:

```bash
mvn clean deploy -Prelease
```

Sign in [nexus repository manager](https://s01.oss.sonatype.org/#stagingRepositories) and check the artifact, then determine whether to release it.

## License

[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html) Copyright (C) Apache Software Foundation

[license-image]: https://img.shields.io/badge/license-Apache%202-4EB1BA.svg
[license-url]: https://www.apache.org/licenses/LICENSE-2.0.html
[build-image]: https://github.com/aliyunmq/rocketmq-logging/actions/workflows/build.yml/badge.svg
[build-url]: https://github.com/aliyunmq/rocketmq-logging/actions/workflows/build.yml
[maven-image]: https://maven-badges.herokuapp.com/maven-central/io.github.aliyunmq/rocketmq-logging/badge.svg
[maven-url]: https://maven-badges.herokuapp.com/maven-central/io.github.aliyunmq/rocketmq-logging