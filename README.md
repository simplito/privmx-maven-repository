# Privmx Maven Repository

This is public Github Maven Repository for Java libraries to simplify working with Privmx Endpoint C++ library inside Java Virtual Machines. Go to the [Privmx Platform Docs](https://docs.privmx.cloud/java) to read more about these libraries.

## Libraries

### Privmx Endpoint Java

PrivMX Endpoint Java is a minimal wrapper library declaring native functions in Java using JNI.

This library implements models, exception catching and the following modules:
1. `CryptoApi` - cryptographic methods used to encrypt/decrypt and sign your data or generate keys to work with Privmx Bridge;
2. `CoreApi` - methods to connect with Privmx Bridge and listening for events;
3. `ThreadApi` - methods for managing Threads and sending/reading messages;
4. `StoreApi` - methods for managing Stores and sending/reading files.


### Privmx Endpoint Java Extra

PrivMX Endpoint Java Extra is an extension of `Privmx Endpoint Java`. It's extended with additional logic that makes using our libraries simpler and less error-prone.

This library implements:

1. Enums and static fields to reduce errors while using the methods.
2. [`PrivmxEndpointWrapper`](https://docs.privmx.cloud/java/api-reference/privmx-endpoint-java-extra/classes/privmx-endpoint-wrapper) for managing connection and event loop.
3. [`PrivmxEndpointContainer`](https://docs.privmx.cloud/java/api-reference/privmx-endpoint-java-extra/classes/privmx-endpoint-container) for managing global session.
4. Classes to simplify reading/writing to files using byte arrays and InputStream/OutputStream.

### Privmx Endpoint Java Android

PrivMX Endpoint Java Android is an extension of `Privmx Endpoint Java Extra` with logic for Android.

This library implements:

1. [`PrivmxEndpointService`](https://docs.privmx.cloud/java/api-reference/privmx-endpoint-java-android/classes/privmx-endpoint-service) - Android Service that manages [`PrivmxEndpointContainer`](https://docs.privmx.cloud/java/api-reference/privmx-endpoint-java-extra/classes/privmx-endpoint-container) and handles app lifecycle changes.
2. [`PrivmxEndpointBaseActivity`](https://docs.privmx.cloud/java/api-reference/privmx-endpoint-java-android/classes/privmx-endpoint-base-activity) - Android Activity that configures and binds to [`PrivmxEndpointService`](https://docs.privmx.cloud/java/api-reference/privmx-endpoint-java-android/classes/privmx-endpoint-service)
    

## Gradle Plugins

### Privmx Endpoint Install Native

Privmx Endpoint Install Native is a gradle plugin that automates the process of downloading and installing native libraries into your project.
