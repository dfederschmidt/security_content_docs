---
title: "AD LDAP Account Locking"
last_modified_at: 2023-05-08
toc: true
toc_label: ""
tags:
  - Investigation
  - Splunk SOAR
  - AD LDAP API
---

[Try in Splunk SOAR](https://www.splunk.com/en_us/software/splunk-security-orchestration-and-automation.html){: .btn .btn--success}

#### Description

Accepts user, to be disabled using Microsoft AD LDAP connector. This playbook produces a normalized observables output for each user and device.

- **Type**: Investigation
- **Product**: Splunk SOAR
- **Apps**: [AD LDAP API](https://splunkbase.splunk.com/apps/#/search/AD LDAP API/product/soar)
- **Last Updated**: 2023-05-08
- **Author**: Teoderick Contreras, Splunk
- **ID**: e6f96caf-610c-4ced-aa2c-ba9b19b89e1f

#### Associated Detections


#### How To Implement
This input playbook requires the Microsoft AD LDAP connector to be configured. It is designed to work in conjunction with the Dynamic Attribute Lookup playbook or other playbooks in the same style.


#### [Explore Playbook](https://splunk.github.io/soar-playbook-viewer/?playbook=https://raw.githubusercontent.com/phantomcyber/playbooks/latest/AD_LDAP_Account_Locking.json){: .btn .btn--info}

[![explore](https://raw.githubusercontent.com/splunk/security_content/develop/playbooks/AD_LDAP_Account_Locking.png){:height="500px" width="500px"}](https://splunk.github.io/soar-playbook-viewer/?playbook=https://raw.githubusercontent.com/phantomcyber/playbooks/latest/AD_LDAP_Account_Locking.json)

#### Required field


#### Reference



[*source*](https://github.com/splunk/security_content/tree/develop/playbooks/AD_LDAP_Account_Locking.yml) \| *version*: **1**