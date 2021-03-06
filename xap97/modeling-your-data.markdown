---
layout: post
title:  Modeling your Data
categories: XAP97
parent: programmers-guide.html
weight: 30
---


{% summary %}Modeling your objects that are used to interact with the space {% endsummary %}

# Space Object ID
When a new object is inserted into the space, it embeds a unique ID - called the UID. The UID can be [generated explicitly](./space-object-id-operations.html) by the client using a unique value generated by the application business logic or using a sequencer running within the space.


# Annotation Support

The XAP API supports [class](./pojo-class-annotations.html) and [field-level](./pojo-attribute-annotations.html) decorations with POJOs. These can be specified via annotations on the space class source itself or external xml file accompanied with the class byte code files located within the jar/war. You can define common behavior for all class instances, and specific behavior for class fields.

# Storage Types
To reduce the memory footprint of the objects stored in space, different storage types can be defined for individual properties of a space class.
Object properties can be assigned a [storage type](./storage-types---controlling-serialization.html) decoration which determines how it is serialized and stored in the space.

# Partition Routing
A partitioned space provides the ability to perform space operations against multiple spaces from a single proxy transparently. The primary goal of the partitioned space is to provide unlimited In-Memory space storage size and group objects into the same partition to speed up performance. The initial intention is to write data into the partitioned space, and route query operations based on the template data.
In order to accomplish that, a [routing property](./routing-in-partitioned-spaces.html) can be defined on the entry type.


{%children%}