# Use Case & Detection Engineering Framework 🛡️

[![Version](https://img.shields.io/badge/Version-2.0-blue.svg)](https://github.com/your-repo/your-project/releases)
[![Last Updated](https://img.shields.io/badge/Last%20Updated-November%2023%2C%202024-green.svg)](https://github.com/your-repo/your-project/commits/main)
[![Authors](https://img.shields.io/badge/Authors-Kunal%20Hatode%2C%20Frank%20Hassenrueck%2C%20Matrix%20Chau-orange.svg)](https://github.com/your-repo/your-project/graphs/contributors)
[![License](https://img.shields.io/badge/License-Unspecified-lightgrey.svg)](https://github.com/your-repo/your-project/blob/main/LICENSE) ---

## 📖 Table of Contents

* [About this Use Case & Detection Engineering Framework](#about-this-use-case--detection-engineering-framework)
    * [History](#history)
    * [Review](#review)
* [Introduction](#introduction) 🚀
    * [Preface](#preface)
    * [Audience](#audience)
    * [Scope](#scope)
* [Use Case & Detection Engineering Framework](#use-case--detection-engineering-framework-1)
    * [Overview](#overview)
    * [Why adopt a Use Case & Detection Engineering Framework?](#why-adopt-a-use-case--detection-engineering-framework)
    * [Principles of the Use Case & Detection Engineering Framework](#principles-of-the-use-case--detection-engineering-framework)
    * [What does the Use Case Framework consist of?](#what-does-the-use-case-framework-consist-of)
    * [Challenges of Creating & Managing Use Cases 🚧](#challenges-of-creating--managing-use-cases-)
* [Drivers for Use Cases](#drivers-for-use-cases)
    * [Risk, Threats and Compliance 📊](#risk-threats-and-compliance-)
    * [Aligning to Business Context](#aligning-to-business-context)
    * [Risk Drivers](#risk-drivers)
        * [Types of Risk Drivers](#types-of-risk-drivers)
    * [Threat Drivers](#threat-drivers)
        * [Types of Threat Drivers](#types-of-threat-drivers)
    * [Compliance Drivers](#compliance-drivers)
        * [Types of Compliance Drivers](#types-of-compliance-drivers)
* [Use Case and Detection Engineering Lifecycle 🔄](#use-case-and-detection-engineering-lifecycle-)
    * [Planning Phase 🗓️](#planning-phase-%EF%B8%8F)
        * [Contextual Feasibility Analysis](#contextual-feasibility-analysis)
    * [Development Phase 🛠️](#development-phase-%EF%B8%8F)
        * [Technical Feasibility Analysis](#technical-feasibility-analysis)
        * [Technical Analysis](#technical-analysis)
        * [Identifying the data Sources](#identifying-the-data-sources)
        * [Identify if attack indicators are fully available](#identify-if-attack-indicators-are-fully-available)
        * [Change Architecture or onboard needed information](#change-architecture-or-onboard-needed-information)
        * [Check if all needed data is available](#check-if-all-needed-data-is-available)
        * [Data Requirements](#data-requirements)
        * [Build the Correlation Rule Logic](#build-the-correlation-rule-logic)
        * [Create the Alert](#create-the-alert)
        * [Handling Exceptions](#handling-exceptions)
    * [Delivery Phase 🚚](#delivery-phase-%EF%B8%8F)
        * [Handover to Security Monitoring Team](#handover-to-security-monitoring-team)
        * [Rule Activation](#rule-activation)
        * [Metrics and Monitoring Rule Behavior](#metrics-and-monitoring-rule-behavior)
        * [SOAR Playbook and Runbook Design](#soar-playbook-and-runbook-design)
        * [Key Roles and Stakeholders](#key-roles-and-stakeholders)
    * [Improvement Phase 📈](#improvement-phase-%EF%B8%8F)
        * [Decommissioning](#decommissioning)
    * [Use Case Cataloguing](#use-case-cataloguing)
        * [Category and Naming Convention](#category-and-naming-convention)
        * [Rule Quality Rating](#rule-quality-rating)
        * [Rule Release Benchmark](#rule-release-benchmark)
        * [Rule Documentation](#rule-documentation)
        * [Use Case Roadmap](#use-case-roadmap)
* [Best Practices](#best-practices) ✨
    * [Proactive Security Measures](#proactive-security-measures)
    * [Support Risk Management Process](#support-risk-management-process)
    * [Have the UCF audited or reviewed](#have-the-ucf-audited-or-reviewed)
* [Sources & References used 📚](#sources--references-used-)

---

# Use Case & Detection Engineering Framework 🛡️

November 23, 2024

Version 2.0

---

# About this Use Case & Detection Engineering Framework

| Author           | Kunal Hatode, Frank Hassenrueck, Matrix Chau |
| :--------------- | :------------------------------------------- |
| Change Authority | Customer Experience, Cisco                   |

## History

| Version No. | Issue Date | Status   | Reason for Change   |
| :---------- | :--------- | :------- | :------------------ |
| 0.1         | 13/04/2021 | Draft    | First Draft         |
| 1.0         | 14/04/2021 | Release  | First Release       |
| 1.1         | 25/04/2021 | Revision | Minor amendments    |
| 1.2         | 15/06/2021 | Revision | Minor amendments    |
| 1.3         | 24/08/2021 | Draft    | Overhaul amendments |
| 1.4         | 07/09/2021 | Released | Minor amendments    |
| 1.5         | 14/04/2022 | Released | Minor amendments    |
| 2.0         | 06/06/2023 | Revision | Major amendments    |

## Review

| Reviewer’s Details | Version No. | Date       |
| :----------------- | :---------- | :--------- |
| Kunal Hatode       | 1.0         | 13/04/2021 |
| Kunal Hatode       | 1.5         | 13/04/2022 |
| Kunal Hatode       | 2.0         | 06/06/2023 |

---

# Introduction 🚀

## Preface

In today's ever-evolving digital landscape, organizations face a multitude of sophisticated and persistent cyber threats that can compromise their sensitive data, disrupt operations, and damage their reputation. To effectively combat these threats, a robust **Use Case and Detection Engineering Framework** is essential. This comprehensive guide aims to provide security professionals, incident responders, and IT teams with a holistic understanding of the key principles, strategies, and best practices involved in building and maintaining an effective security monitoring and incident response program.

The journey begins by establishing a strong foundation in the **Planning Phase**, where organizations define their security objectives, assess risks, and identify the scope of their security monitoring program. This phase emphasizes the importance of collaboration between stakeholders, ensuring alignment with business objectives, and selecting appropriate tools and technologies to support the monitoring efforts.

The guide then delves into the **Development Phase**, where security use cases and detection rules are developed, tested, and fine-tuned. It highlights the significance of conducting thorough technical analysis, considering business cases, and involving stakeholders throughout the development process. The authors stress the need for well-defined and well-designed playbooks, as well as the prerequisites for successful automation implementation, including suitable tools, data integration, process readiness, and organizational preparedness.

The **Delivery Phase** focuses on the handover of use cases to the security monitoring team, rule activation, and the crucial aspect of monitoring rule behavior and metrics. It stresses the need for vigilant monitoring of false positives and false negatives, ensuring the use cases are delivering the desired outcomes and providing insights to drive business decisions. Cataloging the use cases and rules is explored in-depth in the guide's chapters, as a crucial aspect of maintaining an organized and efficient security monitoring program. The authors emphasize the importance of clear and comprehensive catalogs, offering guidance on creating effective use case quality ratings and release benchmarks. The inclusion of mapping the use cases to the MITRE ATT&CK framework adds an additional layer of insight and enables organizations to identify and prioritize security gaps.

The **Improvement Phase** focuses on the continuous enhancement of the use cases and rules in response to technical bugs, deficiencies in output, and the need for periodic review. The guide emphasizes the importance of conducting regular reviews, proactive attack simulations, and acceptance testing to ensure the effectiveness and relevance of the security monitoring program. It also outlines the process of decommissioning use cases that are no longer required, highlighting the need for proper offloading and communication with stakeholders.

Throughout the guide, key roles and stakeholders are identified, providing a clear understanding of the responsibilities and contributions of various teams involved in security monitoring and incident response. This holistic approach ensures effective collaboration and efficient handling of security incidents.

It is important to note that this guide is a comprehensive framework, encompassing a wide range of concepts, methodologies, and best practices. It serves as a valuable resource for organizations seeking to establish or enhance their security monitoring and incident response capabilities. By following the principles and recommendations outlined in this guide, organizations can build a resilient and proactive security posture, mitigating risks and responding effectively to emerging threats.

## Audience

This document is intended for security managers, SOC managers, SOC analysts, Detection Engineers and professionals within the SOC, that are responsible for focusing on the design, capability and maturity of use case development and security monitoring. We hope that this guide will serve as a valuable reference and practical companion for security professionals, incident responders, and IT teams as they navigate the challenging landscape of security monitoring and incident response.

## Scope

This deliverable is a Use Case Framework to address the detection of cyber threats & attack tactics techniques and procedures appropriate to the SOC. The objective of building a Use Case Framework is to better protect the organization’s valuable assets by designing and developing detection use cases using a holistic approach that connects Risk, Threat & compliance requirements.

Following the guidelines and recommendations in this document does not guarantee a secure environment, or that all security incidents will be prevented. Absolute security is impossible to achieve on any open network. However, security risks can be reduced by establishing a good security policy together with sound administration practices; monitoring and responding to security incidents; testing and evaluating security; and improving, securing and managing security weaknesses on an on-going basis. Cisco does not recommend deploying security technologies without associated security policies.

---

# Use Case & Detection Engineering Framework

## Overview

In the context of cybersecurity, a use case describes a potential security threat or incident and defines the steps, actions, or behaviors that indicate the presence of that threat. It helps in identifying, monitoring, and detecting security incidents or suspicious activities within an organization's network or systems.

Detection engineering, on the other hand, refers to the process of designing and developing effective methods and techniques to identify and respond to security threats and incidents. It involves creating and implementing detection rules, logic, search strings, or detection signatures that enable security monitoring systems to identify and generate alerts for suspicious activities or potential security breaches. Detection engineering also encompasses the development of response playbooks, which provide predefined steps and actions to be taken in response to specific security events or incidents.

The use case and detection engineering framework combines these two concepts to create a structured approach for developing, managing, and improving security monitoring capabilities. This framework emphasizes the importance of proactive identification, monitoring, and response to security threats. It involves several phases, including planning, development, delivery, and improvement. A Use Case & Detection Engineering Framework is a fundamental base of what operating strategies guide the SOC to be able to develop use cases that are in line with the business, the organizational structure, the strategic planning and operational systems. Where possible the framework has been built in an agnostic manner, but at the same time have allowances within the framework to ensure that any development of the use cases takes in account the organisation’s operating environment and operating requirements.

The framework per se does not dictate the step by step process of developing use cases but provides guidance on how to develop use cases in a holistic and consistent manner to drive a sustainable approach to use case & detection lifecycle management. The objective of building a Use Case & Detection Engineering Framework is to better protect the organization’s valuable assets by designing and developing detection use cases that connects Risk, Threat & compliance requirements to the reaction and response made by the organisation during a cyber attack or incident.

## Why adopt a Use Case & Detection Engineering Framework?

Essentially, use cases describe manifestations of threats from a high level (the modus operandi of the cyber criminals) to the lowest level (concrete security events in the infrastructure such as exploits, failed logins, etc.). Use cases also describe follow-up actions (incident response) and are tied with business drivers to show how security monitoring reduces risk in the organization. Within the complexity of the security architecture, framework can provide structure and overview.

Such frameworks enable control over the development of the use cases and provide insight into identify how well an organization can defend against cyber threats. The use case framework should allow the SOC:

-   To ensure stakeholder objectives are met uniformly
-   To capture gaps and challenges early on during the creation of use cases
-   To have a holistic “frame of reference” where detection use cases can be categorized into.
-   To engineer detection capabilities in a consistent & methodological manner
-   To quickly see where use cases are lacking and need more attention.
-   To facilitate a phased approach of expanding new use cases based on a large variety of inputs and priorities in the form of Use Case Roadmap.

## Principles of the Use Case & Detection Engineering Framework

-   The creation of use cases should be driven by the organisation's business requirements
-   The use cases must align with the business's risk appetite over any form of asset
-   The use case framework should provide structured control over the compliance requirements of the organisation
-   The creation of use cases must follow a systematic process to eliminate or reduce errors
-   The use case framework should create a foundation for the ability to assess the state of visibility and detection capability
-   The use case framework must reduce the ad hoc detection of threats for the organisation
-   The use case framework should eliminate redundant & duplicate methods of managing use cases
-   The management of the use cases must articulate the state of the use cases at any given point of time

## What does the Use Case Framework consist of?

-   The fundamentals of how business risk, threats and compliance requirements drive the Use Case & Detection Engineering Framework.
-   A practical Use Case & Detection Engineering lifecycle management process
-   A practical guide to develop correlation and detection rules in SIEM from the use cases
-   A suggested guide to maintain use cases and SIEM Rules in catalogue format
-   A series of templates, processes and conventions that support the framework.

## Challenges of Creating & Managing Use Cases 🚧

-   **Out-of-the-box use cases are split-up while covering same scope**
    Most out-of-the-box use cases are split up from each other based on their rule content package which can be put (after some analysis of the detection logic) under the same "use case" as they have the same detection scope.

-   **No naming conventions or pre-determined directory structure**
    Most SIEM out-of-the-box (and later custom added rules) do not have an overarching naming convention over all rules.

-   **Most use case approaches have an Attack-centric or quantitative detection bias**
    Most SIEM Vendors have attempted to organize use cases in a Use Case Framework that primarily focuses on a single limited threat model (kill chain or ATT&CK Framework) this misses critical categories like Self-monitoring, localized anomaly detection (that is not attack centric) and distinctions between quantitative threat modelling and qualitative threat modelling. This as a result will create a attack-centric and quantitative threat detection bias.

-   **Use Cases are hard to align with a SOAR playbooks platform without a framework**
    Most vendors fail to accommodate the emergence of SOAR technologies that are trying to connect automated or semi-automated playbooks to SIEM use cases. Without a proper organized rule set according to some form of framework mapping use cases to playbooks becomes increasingly challenging.

-   **SIEM Vendor Taxonomy overly complex or not generalizable**
    Many SIEM vendors have attempted to standardize detection through taxonomy of detection categories, but these categories are generally limited only to the SIEM vendor itself and hard to generalize to other detection technologies of other vendors like IDS, IPS, UBA and others.
