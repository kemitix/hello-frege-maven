# Hello Frege

A Hello Frege (World) example Maven project

This is a demo project showing how to simply develop in [Frege](http://frege-lang.org), while using Maven as your build tool. It uses the `onejar-maven-plugin` to produce an executable uber-jar.

```haskell
module HelloFrege where

greeting :: String
greeting = "Hello Frege"

main :: IO ()
main = println greeting
```

## Source

Create your source files in `src/main/frege/`.

## Compile

Compile to create the Java source files from your Frege sources and them compile them into `.class` files. These java files are created in `target/generated-sources`.

> `mvn compile`

## Run

Compile and run using maven:

> `mvn compile exec:exec`

## Package

Create the executable uber-jar with:

> `mvn package`

The resulting jar file is created in `target/${project.name}-${project.version}.run.${project.packaging`. e.g. `target/hello-frege-1.0-SNAPSHOT.run.jar`

## Run

Execute the jar:

> `java -jar target/hello-frege-1.0-SNAPSHOT.run.jar`

> Hello Frege

# TODO

* Run QuickCheck tests
