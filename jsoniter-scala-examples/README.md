# Jsoniter Scala Examples

## How to build uber jar and run it with JVM

```sh
sbt clean +assembly

time java -jar target/scala-2.11/jsoniter-scala-examples-assembly-0.1.0-SNAPSHOT.jar
time java -jar target/scala-2.12/jsoniter-scala-examples-assembly-0.1.0-SNAPSHOT.jar
time java -jar target/scala-2.13/jsoniter-scala-examples-assembly-0.1.0-SNAPSHOT.jar
```

## How to build with a native image and run binaries

```sh
/usr/lib/jvm/graalvm-ce-java8/bin/gu install native-image

/usr/lib/jvm/graalvm-ce-java8/bin/native-image --no-server --no-fallback --allow-incomplete-classpath --initialize-at-build-time -jar target/scala-2.13/jsoniter-scala-examples-assembly-0.1.0-SNAPSHOT.jar

time ./jsoniter-scala-examples-assembly-0.1.0-SNAPSHOT
```