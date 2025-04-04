# Spring Boot Replicate Client 🚧

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
![version](https://img.shields.io/badge/version-1.0.0-purple)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=nilsw13_Spring-Boot-Replicate&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=nilsw13_Spring-Boot-Replicate)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=nilsw13_Spring-Boot-Replicate&metric=coverage&cachebuster=123)](https://sonarcloud.io/summary/new_code?id=nilsw13_Spring-Boot-Replicate)

**🚧 Work in Progress 🚧**  
A Spring Boot client for interacting with the [Replicate API](https://replicate.com/). Inspired by the [Laravel Replicate PHP Client](https://github.com/halilcosdu/laravel-replicate), this library is currently under development and will soon provide a convenient way to manage and interact with Replicate services in Java.

---


## Coming Soon! 🚀

A comprehensive Spring Boot client for interacting with the [Replicate API](https://replicate.com/). This library provides a convenient way to manage and interact with Replicate services in Java.
This library is currently in active development. Stay tuned for the first release.


## Features

- 🏃‍♂️ **Run Models**: Execute predictions with any model available on Replicate
- 🤖 **Model Management**: Create, list, update, and delete models
- 🔄 **Versions**: Get information about model versions and their capabilities
- 📊 **Deployments**: Create and manage model deployments for production use
- 🎓 **Training**: Fine-tune models with your own data
- 📚 **Collections**: Browse curated model collections
- 🔒 **Authentication**: Built-in token authentication support
- 🪝 **Webhooks**: Configure webhooks for event notifications

## Installation

Add the dependency to your `pom.xml` if you're using Maven:

```xml
<dependency>
    <groupId>io.github.nilsw13</groupId>
    <artifactId>spring-boot-replicate</artifactId>
    <version>1.0.0</version>
</dependency>
```

## ⚡ Quick Start
- 1 **Configure your Replicate API token in application.properties otherwise you won't be able to use the library this is very important**
```properties
    replicate.api-token=your_replicate_api_token_here
```
- 2 **Usage Examples**
```java

@RestController
public class DemoController {
    private final Replicate replicate;

    public DemoController(Replicate replicate) {
        this.replicate = replicate;
    }

    @GetMapping("/models")
    public ModelList listModels() {
        return replicate.models().list();
    }

    @GetMapping("/account")
    public Account get() {
        return replicate.account().get();
    }
}

```










