# Jmeter Csv Dataset Config

## Introduction

This plugin provides additional feature over the JMeter's default **CSV data set config element**. This also provides additional parameterization feature.

This will enable **LoadRunner** users, the privilege of having similar parameter advantage in **Apache JMeter**

## Preview

![CSV Dataset Config](https://yuyanqing.cn/oss/image-bed/col/jmeter/jmeter-csv-dataset-config.png)

## Required Components

1. Apache JMeter components
2. Apache JMeter core

## Jmeter Target

* Jmeter version 5.1.1 or above
* Java 8 or above

## Installation Instructions

* Download the source code from the GitHub.
* Just do a mvn clean install (M2 is required)
* Jar will be generated under the target directory (di-extended-csv-xx.jar).
* Copy the Jar to \<Jmeter Installed Directory\>/lib/ext/

## What's new ?

* Improved new GUI
* Added feature to create new file
* Added feature to edit csv file with default text editor
* Fixed quoted data issue
* Fixed relative path issue
* Support for large csv (Moved out of In-memory read)

## Options

✨ This version eliminates remembering the below combination table ✨

This allows reading of CSV data as follows

* Select Row (Sequential | Random | Unique)
* Update Value (Each Iteration | Once)
* When Out of Values (Continue Cyclic | Continue with last Value | Abort Thread)

The below table is the combinations allowed while using this plugin

| Select Row | Update value   | Out of Values            | Allocate Block Size |
|------------|----------------|--------------------------|---------------------|
| Sequential | Each Iteration | Continue Cyclic          | NA                  |
| Sequential | Each Iteration | Abort Thread             | NA                  |
| Sequential | Each Iteration | Continue with Last value | NA                  |
| Sequential | Once           | NA                       | NA                  |
| Random     | Each Iteration | NA                       | NA                  |
| Random     | Once           | NA                       | NA                  |
| Unique     | Each Iteration | Continue with Last Value | Enabled             |
| Unique     | Each Iteration | Continue Cyclic          | Enabled             |
| Unique     | Each Iteration | Abort Thread             | Enabled             |
| Unique     | Once           | NA                       | NA                  |

## Future Release in pipeline

* Visualizing csv data in data table
* Simulate Parameter window

## References

* CSV data set config
