rfc
===

This is the Flux RFC project.

We collect specifications for APIs, file formats, wire protocols, and
processes.

Active RFC Documents
--------------------

#### [1/C4.1 - Collective Code Construction Contract](spec_1.rst)

The Collective Code Construction Contract (C4.1) is an evolution of
the github.com Fork + Pull Model, aimed at providing an optimal
collaboration model for free software projects.

#### [2/Flux Licensing and Collaboration Guidelines](spec_2.rst)

The Flux framework is a family of projects used to build
site-customized resource management systems for High Performance
Computing (HPC) data centers. This document specifies licensing and
collaboration guidelines for Flux projects.

#### [3/CMB1 - Flux Comms Message Broker Protocol](spec_3.rst)

This specification describes the format of communications message
broker messages, Version 1, also referred to as CMB1.

#### [4/Flux Resource Model](spec_4.rst)

The Flux Resource Model describes the conceptual model used for
resources within the Flux framework.

#### [5/Flux Comms Modules](spec_5.rst)

This specification describes the broker extension modules used to
implement Flux services.

#### [6/Flux Remote Procedure Call Protocol](spec_6.rst)

This specification describes how Flux Remote Procedure Call (RPC) is
built on top of CMB1 request and response messages.

#### [7/Flux Coding Style Guide](spec_7.rst)

This specification presents the recommended standards when
contributing C code to the Flux code base.

#### [8/Flux Task and Program Execution Services](spec_8.rst)

A core service of Flux is to launch, monitor, and handle I/O for
distributed sets of tasks in order to execute a parallel workload. A
Flux workload can include further instances of Flux, to arbitrary
recursive depth. The goal of this RFC is to specify in detail the
services required to execute a Flux workload.

#### [9/Distributed Communication and Synchronization Best Practices](spec_9.rst)

Establishes best practices, preferred patterns and anti-patterns for
distributed services in the flux framework.

#### [10/Content Storage](spec_10.rst)

This specification describes the Flux content storage service and
the messages used to access it.

#### [11/Key Value Store Tree Object Format v1](spec_11.rst)

The Flux Key Value Store (KVS) implements hierarchical key
namespaces layered atop the content storage service described in
RFC 10. Namespaces are organized as hash trees of content-addressed
tree objects and values. This specification defines the version 1
format of key value store tree objects.

#### [12/Flux Security Architecture](spec_12.rst)

This document describes the mechanisms used to secure Flux instances
against unauthorized access and prevent privilege escalation and
other attacks, while ensuring programs run with appropriate user
credentials and are contained within their set of allocated
resources.

#### [13/Simple Process Manager Interface v1](spec_13.rst)

The MPI process manager interface (PMI) version 1 is a de-facto
standard API and wire protocol for communication between MPI
runtimes and resource managers. It was added to the MPICH2 MPI-2
reference implementation in late 2001, and has since been widely
implemented, but was not officially standardized by the MPI Forum
and has been only lightly documented. This RFC is an attempt to
document PMI-1 to guide developers of resource managers that must
support current and legacy MPI implementations.

#### [14/Canonical Job Specification](spec_14.rst)

A domain specific language based on YAML is defined to express the
resource requirements and other attributes of one or more programs
submitted to a Flux instance for execution. This RFC describes the
canonical form of the jobspec language, which represents a request
to run exactly one program.

#### [15/Independent Minister of Privilege for Flux: The Security IMP](spec_15.rst)

This specification describes Flux Security IMP, a privileged service
used by multi-user Flux instances to launch, monitor, and control
processes running as users other than the instance owner.

#### [16/KVS Job Schema](spec_16.rst)

This specification describes the format of data stored in the KVS
for Flux jobs.

#### [18/KVS Event Log Format](spec_18.rst)

A log format is defined that can be used to log job state
transitions and other date-stamped events.

#### [19/Flux Locally Unique ID (FLUID)](spec_19.rst)

This specification describes a scheme for a distributed,
uncoordinated *flux locally unique ID* service that generates 64 bit
k-ordered, unique identifiers that are a combination of timestamp
since some epoch, generator id, and sequence number. The scheme is
used to generate Flux job IDs.

#### [20/Resource Set Specification](spec_20.rst)

This specification defines the version 1 format of the resource-set
representation or *R* in short.

#### [21/Job States and Events](spec_21.rst)

This specification describes Flux job states and the events that
trigger job state transitions.

#### [22/Idset String Representation](spec_22.rst)

This specification describes a compact form for expressing a set of
non-negative, integer ids.

#### [23/Flux Standard Duration](spec_23.rst)

This specification describes a standard form for time duration.

#### [24/Flux Job Standard I/O Version 1](spec_24.rst)

This specification describes the format used to represent standard
I/O streams in the Flux KVS.

#### [25/Job Specification Version 1](spec_25.rst)

Version 1 of the domain specific job specification language
canonically defined in RFC14.

#### [27/Job Specification Version 2](spec_27.rst)

Version 2 of the domain specific job specification language
canonically defined in RFC14.

Change Process
--------------

The change process is [C4.1](spec_1.rst) with
a few modifications:

-   A specification is created and modified by pull requests according
    to C4.1.
-   Each specification has an editor who publishes the RFC to (website
    TBD) as needed.
-   Each specification has a status on that website: Raw, Draft, Stable,
    Legacy, Retired, Deleted.
-   Non-cosmetic changes are allowed only on Raw and Draft
    specifications.
