# What is FHIR Fix?

FHIR Fix is a utility for fixing and manipulation of data in a FHIR Store. Use Cases include:

**1. Data Fixing**

It may be that data has been mapped and loaded into a FHIR Store, for example such as the Interweave Connect FHIR Store. If mapping errors subsequently come to light then FHIR Fix can be used to manipulate the data and make corrections to data that has previously been loaded

**2. Retention Management**

There may be a requirement to implement retention policies which remove data from view after a certain period of time. FHIR Fix can also be configured to apply these selective "soft deletes" on a scheduled basis.

*Internally FHIR Fix uses the same technologies (node.js, docker) as Interweave Connect and so is a natural companion which can be installed alongside. However this is in no way a pre-requisite, and FHIR Fix can also be used as a stand-alone utility which can connect to **any** FHIR compliant endpoint.*

# Key Features

The overall goal is to provide a framework for creating data-fix jobs - providing a rigorous and consistent implementation of all "boilerplate" aspects so that Data Providers can focus on configuring only the specifics of the actaul desired updates. This includes:

 - Provides flexible options for data-fix "jobs" to be defined and scheduled
 - Jobs can be for either update or deletion
 - Job definition includes selection criteria (FHIR Query) to select the relevant records
 - Easy-to-write code "plugins" can be used to add any other custom logic - for example more complex selection critieria, field manipulations, etc
 - Keeps an audit trail and resource versions
 - Keeps logs, including recording any errors
 - Includes options for throttling

# Getting Started

[01 - Installation](/docs/install-guide.md)

[02 - User Guide](/docs/user-guide.md)

[03 - Retention Management](/docs/retention-mgt.md)
