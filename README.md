# EnumMapping

This module allows you to convert a string to an enumeration value. It contains an entity EnumMap that has attributes for all enums that you want to convert. Additionally, a JavaAction ConvertStringToEnum is used to convert a string to the corresponding enumeration attribute in the EnumMap entity.

### Typical usage scenario
A string to enum conversion typically is needed on im- and export actions, e.g. excel, webservice, web api, etc.

### Features and limitations
* The string will be matched to the enum key or the localized enum value. The localization from the current user is used.
* The JavaAction will throw an error (MendixRuntimeException) if the string value cannot be converted to the enum value (i.e. the string value does not match any of the enum keys or values)

# Dependencies
* Mendix 5.21.1

# Installation

### Prerequisities

### Installation steps
* download and import the EnumMapping module in your project

# Getting Started

### configuration / how to use
* Add your enumerations as attributes to the EnumMap entity. Name the attribute the same as the enumeration for clarity (e.g. if your enumeration is named TestEnum, name the attribute also TestEnum)
* In your microflow(s), call the JavaAction ConvertStringToEnum to convert a string to an enum value. This returns an instance of EnumMap where the attribute of the requested enumeration is filled with the converted enum value.
* Make sure to use proper (custom) error handling on the action/ flow.
* Use the attribute from EnumMap as enum value in your microflow.

# Remarks

# Known bugs

# Links 

# License
Licensed under the Apache license.

# Developers notes
* `git clone https://github.com/ehuitema/EnumMapping`

# Version history
