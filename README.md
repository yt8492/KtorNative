# How to build & native build

```
./gradlew shadowJar
```

```
native-image --no-server \
-jar build/libs/KtorNative-0.0.1-all.jar \
-H:ReflectionConfigurationFiles=reflect.json \
--initialize-at-run-time=io.netty.handler.ssl.ReferenceCountedOpenSslContext,io.netty.handler.ssl.JdkNpnApplicationProtocolNegotiator \
--allow-incomplete-classpath \
-H:+TraceClassInitialization
```
