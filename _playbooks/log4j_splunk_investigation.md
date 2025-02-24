---
title: "Log4j Splunk Investigation"
last_modified_at: 2021-12-14
toc: true
toc_label: ""
tags:
  - Investigation
  - Splunk SOAR
  - Splunk
---

[Try in Splunk SOAR](https://www.splunk.com/en_us/software/splunk-security-orchestration-and-automation.html){: .btn .btn--success}

#### Description

Published in response to CVE-2021-44228, this playbook utilizes data already in your Splunk environment to help investigate and remediate impacts caused by this vulnerability in your environment.

- **Type**: Investigation
- **Product**: Splunk SOAR
- **Apps**: [Splunk](https://splunkbase.splunk.com/apps/#/search/Splunk/product/soar)
- **Last Updated**: 2021-12-14
- **Author**: Lou Stella, Splunk
- **ID**: fc0adc66-ff2b-48b0-9a6f-63da6783fd63

#### Associated Detections


#### How To Implement
This playbook presumes you have Enterprise Security and have configured Assets &amp; Identities, as well as the Endpoint.Processes datamodel


#### [Explore Playbook](https://splunk.github.io/soar-playbook-viewer/?playbook=https://raw.githubusercontent.com/phantomcyber/playbooks/latest/internal_host_splunk_investigate_log4j.json){: .btn .btn--info}

[![explore](https://raw.githubusercontent.com/splunk/security_content/develop/playbooks/internal_host_splunk_investigate_log4j.png){:height="500px" width="500px"}](https://splunk.github.io/soar-playbook-viewer/?playbook=https://raw.githubusercontent.com/phantomcyber/playbooks/latest/internal_host_splunk_investigate_log4j.json)

#### Required field
* hostName
* destinationAddress


#### Reference

* [https://www.splunk.com/en_us/blog/security/log-jammin-log4j-2-rce.html](https://www.splunk.com/en_us/blog/security/log-jammin-log4j-2-rce.html)




[*source*](https://github.com/splunk/security_content/tree/develop/playbooks/internal_host_splunk_investigate_log4j.yml) \| *version*: **1**