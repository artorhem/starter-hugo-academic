---
title: Trusted Capsules
summary: ARM TrustZone backed data privacy on remote devices
tags:
- Security
- Trusted Execution Environments
- Trusted Computing
date: "2018-05-25T00:00:00"

# Optional external URL for project (replaces project detail page).
external_link: ""

links:
url_code: ''
url_pdf: 'uploads/tc_cybersec.pdf'
url_slides: ''
url_video: ''
---
Security of data is tightly coupled to its access policy. However, in practice, a data owner has control of his data's access policies only as far as the boundaries of his own systems. In this paper, we introduce graduated access control, which provides mobile, programmable, and dynamically-resolving policies for access control that extends a data owner's policies across system boundaries. We realize this through a novel data-centric abstraction called trusted capsules and its associated system, the trusted data monitor. 

A trusted capsule couples data and policy into a single mobile unit. A capsule is backwards-compatible and is indistinguishable from a regular file to applications. In coordination with the trusted data monitor a capsule provides data integrity and confidentiality on remote devices, strong authentication to a trusted capsule service, and supports nuanced and dynamic access control decisions on remote systems. We implemented our data monitor using ARM TrustZone. 

We show that graduated access control can express novel and useful real world policies, such as revocation, remote monitoring, and risk-adaptable disclosure. We illustrate trusted capsules for different file formats, including JPEG, FODT, and PDF. We also show compatibility with unmodified applications, such as LibreOffice Writer, Evince, and VLC.
