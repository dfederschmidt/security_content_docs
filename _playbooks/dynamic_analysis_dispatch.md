---
title: "Dynamic Analysis Dispatch"
last_modified_at: 2023-03-30
toc: true
toc_label: ""
tags:
  - Investigation
  - Splunk SOAR
  - CrowdStrike OAuth API
  - urlscan.io
  - VirusTotal_v3
  - SAA
---

[Try in Splunk SOAR](https://www.splunk.com/en_us/software/splunk-security-orchestration-and-automation.html){: .btn .btn--success}

#### Description

Automatically dispatches input playbooks with the &#39;sandbox&#39; tag. This will produce a merge report and indicator tag for each inputs.

- **Type**: Investigation
- **Product**: Splunk SOAR
- **Apps**: [CrowdStrike OAuth API](https://splunkbase.splunk.com/apps/#/search/CrowdStrike OAuth API/product/soar), [urlscan.io](https://splunkbase.splunk.com/apps/#/search/urlscan.io/product/soar), [VirusTotal_v3](https://splunkbase.splunk.com/apps/#/search/VirusTotal_v3/product/soar), [SAA](https://splunkbase.splunk.com/apps/#/search/SAA/product/soar)
- **Last Updated**: 2023-03-30
- **Author**: Teoderick Contreras, Splunk
- **ID**: a15da934-1f59-4672-b98c-ec1bbfd80885

#### Associated Detections


#### How To Implement
This automatic playbook requires &#34;sandbox&#34; tag be present on each input playbook you want to launch.


#### [Explore Playbook](https://splunk.github.io/soar-playbook-viewer/?playbook=https://raw.githubusercontent.com/phantomcyber/playbooks/latest/Dynamic_Analysis_Dispatch.json){: .btn .btn--info}

[![explore](https://raw.githubusercontent.com/splunk/security_content/develop/playbooks/Dynamic_Analysis_Dispatch.png){:height="500px" width="500px"}](https://splunk.github.io/soar-playbook-viewer/?playbook=https://raw.githubusercontent.com/phantomcyber/playbooks/latest/Dynamic_Analysis_Dispatch.json)

#### Required field


#### Reference



[*source*](https://github.com/splunk/security_content/tree/develop/playbooks/Dynamic_Analysis_Dispatch.yml) \| *version*: **1**