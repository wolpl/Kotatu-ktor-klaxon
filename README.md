# Kotatu-ktor-klaxon
[![](https://jitpack.io/v/wolpl/Kotatu-ktor-klaxon.svg)](https://jitpack.io/#wolpl/Kotatu-ktor-klaxon)  
Kotatu-ktor-klaxon is library to use klaxon for JsonParser in Ktor.
Version 0.1.5 requires Kotlin 1.3.21 and ktor version 1.1.3.

# install
```groovy
repositories {		
	maven { url 'https://jitpack.io' }
}

dependencies {
	compile 'com.github.wolpl:Kotatu-ktor-klaxon:0.1.5'
}

```

# How to use
## Use default Klaxon Converter
```kotlin
fun Application.main() {
    install(ContentNegotiation) {
        klaxon()
    }
}
```
## Use Custom Converter
```kotlin
fun Application.main() {
    install(ContentNegotiation) {
        klaxon {
            converter(YourCustomConverter())
        }
    }
}
```
