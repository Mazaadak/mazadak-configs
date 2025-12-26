# Mazadak Configs
## Overview
- The Mazadak Configs repository contains centralized configuration files for all microservices in the Mazadak platform.

- These configuration files are consumed by the [Config Server](https://github.com/Mazaadak/config-server), which provides environment-specific settings to services at runtime using Spring Cloud Config.

- This repository is the single source of truth for application properties, database connections, Kafka topics, and other service configurations across the platform.

## Configuration Files
- Each service's configuration file should be named `{spring.application.name}-{profile}.yml` for it to be loaded, not having the `{profile}` part will register it with the default profile.

## Usage
The Config Server automatically pulls these configuration files from this repository. Services retrieve their configuration from the Config Server at startup using:
```
http://config-server:18071/{service-name}/{profile}
```

## For Further Information
Refer to [Config Server Documentation](https://github.com/Mazaadak/.github/wiki/Config-Server).
