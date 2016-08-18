---
title: Rancher API - amazonec2Config
layout: rancher-api-default
version: v1.2
lang: en
---

## Amazonec2Config

The configuration to launch an EC2 instance in Amazon Web Services using [machine]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/machine). Rancher is calling `docker-machine`, so any available options in `docker-machine` for specific drivers are exposed in Rancher. The default fields from `docker-machine` are not listed in the Rancher API, and they can be found in the `docker-machine` documentation. The notes on which fields are **required** are from the `docker-machine` documentation.

### Resource Fields

Field | Type | Create | Update | Default | Notes
---|---|---|---|---|---
accessKey | string | Optional | - | - | 
ami | string | Optional | - | - | 
deviceName | string | Optional | - | /dev/sda1 | 
iamInstanceProfile | string | Optional | - | - | 
instanceType | string | Optional | - | t2.micro | 
monitoring | boolean | Optional | - | - | 
privateAddressOnly | boolean | Optional | - | - | 
region | string | Optional | - | us-east-1 | The region to use when launching the host
requestSpotInstance | boolean | Optional | - | - | 
rootSize | string | Optional | - | 16 | 
secretKey | string | Optional | - | - | 
securityGroup | string | Optional | - | docker-machine | 
sessionToken | string | Optional | - | - | 
spotPrice | string | Optional | - | 0.50 | 
sshKeypath | string | Optional | - | - | 
sshUser | string | Optional | - | ubuntu | The ssh username to use to ssh into the host
subnetId | string | Optional | - | - | 
tags | string | Optional | - | - | 
useEbsOptimizedInstance | boolean | Optional | - | - | 
usePrivateAddress | boolean | Optional | - | - | 
volumeType | string | Optional | - | gp2 | 
vpcId | string | Optional | - | - | 
zone | string | Optional | - | a | 

<br>
Please read more about the [common resource fields]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/common/). These fields are read only and applicable to almost every resource. We have segregated them from the list above.

### Operations
{::options parse_block_html="true" /}
<a id="create"></a>
<div class="action"><span class="header">Create<span class="headerright">POST:  <code>/v1/amazonec2Configs</code></span></span>
<div class="action-contents">
{% highlight json %}
{
	"accessKey": "",
	"ami": "",
	"deviceName": "/dev/sda1",
	"iamInstanceProfile": "",
	"instanceType": "t2.micro",
	"monitoring": true,
	"privateAddressOnly": true,
	"region": "us-east-1",
	"requestSpotInstance": true,
	"rootSize": "16",
	"secretKey": "",
	"securityGroup": "docker-machine",
	"sessionToken": "",
	"spotPrice": "0.50",
	"sshKeypath": "",
	"sshUser": "ubuntu",
	"subnetId": "",
	"tags": "",
	"useEbsOptimizedInstance": true,
	"usePrivateAddress": true,
	"volumeType": "gp2",
	"vpcId": "",
	"zone": "a"
}
{% endhighlight %}
</div>
</div>
