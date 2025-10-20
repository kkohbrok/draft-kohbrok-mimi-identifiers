---
title: "MIMI Identifiers"
category: info

docname: draft-kohbrok-mimi-identifiers-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: "Applications and Real-Time"
workgroup: "More Instant Messaging Interoperability"
keyword:
 - identity
venue:
  group: "More Instant Messaging Interoperability"
  type: "Working Group"
  mail: "mimi@ietf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/mimi/"
  github: "kkohbrok/draft-kohbrok-mimi-identifiers"
  latest: "https://kkohbrok.github.io/draft-kohbrok-mimi-identifiers/draft-kohbrok-mimi-identifiers.html"

author:
 -
    fullname: "Konrad Kohbrok"
    organization: "Phoenix R&D"
    email: "konrad@ratchet.ing"
 -
    fullname: "Raphael Robert"
    organization: "Phoenix R&D"
    email: "ietf@raphaelrobert.com"

normative:

informative:

...

--- abstract

TODO Abstract


--- middle

# Introduction

- MIMI currently doesn't make assumptions about names beyond the URI format introduced in {{!I-D.draft-ietf-mimi-protocol}}
- Different messaging applications use different schemes
- MIMI should be able to support at least the most widely used ones

# Identifier types

## Identifiers for connection establishment

- Globally unique
- User-facing
- Often chosen by user
- Multiple identifiers per user possible
- User can add/delete identifiers dynamically
- Examples:
  - Phone numbers
  - Signal-style usernames
  - Matrix-style usernames
  - Administrative identifiers

## Administrative identifiers

- Globally unique
- Generally not user-facing
- Generally not chosen-facing
- Can be provider-generated
- Server might not be able to link admin to connection establishment identifiers
- Immutable
- Examples
  - UUIDs
  - Matrix-style usernames

## Display names (decorative identifiers)

- Not globally unique
- Not necessarily visible to provider
- User-facing
- User-chosen

# Proposal for MIMI

## Connection establishment

- Multiple options for connection establishment identifiers
  - Phone numbers (draft WIP)
  - Usernames (user chosen names, potentially with format restrictions)
- No requirement for providers to be able to link connection establishment
  identifiers with administrative identifiers
- Ephemeral identifiers should be allowed

## Administrative identifiers

- Should be unique within domain of provider
- Should be immutable
- No other requirement w.r.t. format, i.e. both Matrix-style and UUIDs allowed
- No requirement for user-readability
- These are used for authentication and are included in MLS credentials

## Display names

- No strict requirement for hub/provider to have access to display names, may be
  subject to policy

# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
