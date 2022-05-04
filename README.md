# SMPP client

[![Build](https://github.com/telenordigital/sms-smpp/actions/workflows/build.yml/badge.svg)](https://github.com/telenordigital/sms-smpp/actions/workflows/build.yml)

A smpp client library implementing SMPP specification from https://smpp.org.

Uses Netty I/0 asynchronous framework. Requires Java 16.

## Features

- Supports SMS MT, delivery receipts and SMS MO
- Modern and simple implementation with limited third-party dependencies
- Performant and reliable, used by Telenor Digital in production services since 2021

## Usage

At first, you need to create an instance
of [SmppConnectionConfig](src/main/java/com/telenordigital/sms/smpp/config/SmppConnectionConfig.java)
type with necessary configuration parameters. Afterwards, you create an instance
of [SmppConnectionGroup](src/main/java/com/telenordigital/sms/smpp/SmppConnectionGroup.java)
passing the config instance and the handlers for delivery receipts and SMS MO messages as
constructor parameters

See the [complete example](src/test/java/com/telenordigital/sms/smpp/SmppConnectionTester.java) for
more details.

## License

Code licensed under the Apache License 2.0.
See [LICENSE file](https://github.com/telenordigital/sms-smpp/blob/master/LICENSE) for terms.
