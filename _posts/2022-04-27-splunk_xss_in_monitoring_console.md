---
title: "Splunk XSS in Monitoring Console"
excerpt: "Drive-by Compromise"
categories:
  - Application
last_modified_at: 2022-04-27
toc: true
toc_label: ""
tags:
  - Drive-by Compromise
  - Initial Access
  - Splunk Enterprise
  - Splunk Enterprise Security
  - Splunk Cloud
  - CVE-2022-27183
---



[Try in Splunk Security Cloud](https://www.splunk.com/en_us/cyber-security.html){: .btn .btn--success}

#### Description

On May 3rd, 2022, Splunk published a security advisory for a reflective Cross-Site Scripting (XSS) vulnerability stemming from the lack of input validation in the Distributed Monitoring Console app. This detection will alert on attempted exploitation in patched versions of Splunk as well as actual exploitation in unpatched version of Splunk.

- **Type**: TTP
- **Product**: Splunk Enterprise, Splunk Enterprise Security, Splunk Cloud
- **Datamodel**: 
- **Last Updated**: 2022-04-27
- **Author**: Lou Stella, Splunk
- **ID**: b11accac-6fa3-4103-8a1a-7210f1a67087


#### [ATT&CK](https://attack.mitre.org/)

| ID          | Technique   | Tactic         |
| ----------- | ----------- |--------------- |
| [T1189](https://attack.mitre.org/techniques/T1189/) | Drive-by Compromise | Initial Access |

#### Search

```
 `splunkd_web` method="GET" uri_query="description=%3C*" 
| table _time host status clientip user uri 
| `splunk_xss_in_monitoring_console_filter`
```

#### Associated Analytic Story
* [Splunk Vulnerabilities](/stories/splunk_vulnerabilities)


#### How To Implement
This detection does not require you to ingest any new data. The detection does require the ability to search the _internal index. This detection will find attempted exploitation of CVE-2022-27183.

#### Required field
* method
* uri_query
* status
* clientip
* user
* uri


#### Kill Chain Phase
* Exploitation


#### Known False Positives
Use of the monitoring console where the less-than sign (&lt;) is the first character in the description field.


#### RBA

| Risk Score  | Impact      | Confidence   | Message      |
| ----------- | ----------- |--------------|--------------|
| 40.0 | 50 | 80 | A potential XSS attempt has been detected from $user$ |



#### CVE

| ID          | Summary | [CVSS](https://nvd.nist.gov/vuln-metrics/cvss) |
| ----------- | ----------- | -------------- |
| [CVE-2022-27183](https://nvd.nist.gov/vuln/detail/CVE-2022-27183) | The Monitoring Console app configured in Distributed mode allows for a Reflected XSS in a query parameter in Splunk Enterprise versions before 8.1.4. The Monitoring Console app is a bundled app included in Splunk Enterprise, not for download on SplunkBase, and not installed on Splunk Cloud Platform instances. Note that the Cloud Monitoring Console is not impacted. | 4.3 |



#### Reference

* [https://www.splunk.com/en_us/product-security/announcements/svd-2022-0505.html](https://www.splunk.com/en_us/product-security/announcements/svd-2022-0505.html)



#### Test Dataset
Replay any dataset to Splunk Enterprise by using our [`replay.py`](https://github.com/splunk/attack_data#using-replaypy) tool or the [UI](https://github.com/splunk/attack_data#using-ui).
Alternatively you can replay a dataset into a [Splunk Attack Range](https://github.com/splunk/attack_range#replay-dumps-into-attack-range-splunk-server)

* [https://media.githubusercontent.com/media/splunk/attack_data/master/datasets/attack_techniques/T1189/xss/splunk_web_access.log](https://media.githubusercontent.com/media/splunk/attack_data/master/datasets/attack_techniques/T1189/xss/splunk_web_access.log)



[*source*](https://github.com/splunk/security_content/tree/develop/detections/application/splunk_xss_in_monitoring_console.yml) \| *version*: **1**