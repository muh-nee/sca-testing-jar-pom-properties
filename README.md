# sca-testing-jar-pom-properties

Test repository for Datadog SCA JAR pom.properties scanning.

Contains JARs with embedded `pom.properties` metadata for testing the JAR extractor, including known vulnerable versions.

## JARs

| File | groupId | artifactId | version | CVEs |
|------|---------|------------|---------|------|
| `libs/log4j-core-2.14.1.jar` | org.apache.logging.log4j | log4j-core | 2.14.1 | CVE-2021-44228 (Log4Shell) |
| `libs/commons-collections-3.2.1.jar` | commons-collections | commons-collections | 3.2.1 | CVE-2015-6420 |
| `libs/jackson-databind-2.9.10.jar` | com.fasterxml.jackson.core | jackson-databind | 2.9.10 | CVE-2019-14379, CVE-2019-14540 |
| `libs/guava-31.1-jre.jar` | com.google.guava | guava | 31.1-jre | — |
| `libs/myapp-1.0.0.jar` | com.example | myapp | 1.0.0 | — |

## JARs with declared but missing dependencies

| File | Declared dependencies (not included) |
|------|---------------------------------------|
| `libs/guava-31.1-jre.jar` | failureaccess:1.0.1, listenablefuture, jsr305, checker-qual, error_prone_annotations, j2objc-annotations |
| `libs/myapp-1.0.0.jar` | jackson-databind:2.9.10, commons-lang3:3.12.0 |
