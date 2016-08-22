Contargo Types
===============

This is a library aimed at providing a collection of re-usable Contargo objects.

## Getting started

Using the `contargo-types` as a library in your project, means simply including
it as a Maven dependency:

```xml
<dependency>
    <groupId>net.contargo</groupId>
    <artifactId>contargo-types</artifactId>
    <version>LATEST</version>
</dependency>
```

## Usage

### Container number

```java
ContainerNumber containerNumber = ContainerNumber.forValue(string);
```

The built container number instance provides various information, such as the
validity on `isValid()` or the formatted value on `toString()`.

### License plate

```java
// Create with default country Germany
LicensePlate licensePlate = LicensePlate.forValue(string);
// Create with dedicated country
LicensePlate licensePlateWithCountry = LicensePlate.forValue(string).withCountry(SupportedLicensePlateCountry.NETHERLANDS);
```

The built license plate instance provides various information depending on the
bound country, such as the validity on `isValid()` or the formatted value on
`toString()`.

To find out which countries are supported, take a look at the
`SupportedLicensePlateCountry` enum.

## Development

This is a pretty straight-forward Java-project, use `mvn` to build, test and
deploy.

Happy hacking!
