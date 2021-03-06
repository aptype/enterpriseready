+++
date = "2016-11-20T00:00:00Z"
title = "Deployment Models"
type = "breakdown"
company = "Deployment Models"
+++

The evolution of enterprise software has changed the landscape for how applications are adopted and deployed. Below are the most common methods for delivering applications to customers.

## Multi-tenant (vendor managed)
Most SaaS applications today are built to be deployed as a multi-tenant application that is managed and operated by the application vendor. This deployment model was [pioneered by Salesforce](https://developer.salesforce.com/page/Multi_Tenant_Architecture) as “on-demand” and has led to the modern software landscape we’re familiar with today. The low barrier to adoption of this model has supported freemium and trial opportunities through which most customers initially experience the product. As a result this the method that creates “bottom up” adoption of applications (and is the reason that applications like GitHub, Slack, Dropbox were able to penetrate the enterprise). In larger organizations where an application has not been approved but is still given access to sensitive company data, this "bottom up adoption" is often called “shadow IT”. There is an entire product category around stopping shadow IT called [Cloud Access Security Brokers](http://www.gartner.com/it-glossary/cloud-access-security-brokers-casbs/) or “CASBs”. As enterprises discover shadow IT, they can either block access or try to negotiate a license that will meet its needs.

## Single-tenant (vendor managed)
Occasionally, large customers will prefer to have a dedicated instance of an application that is managed by the vendor. This can be similar to having an extra deployment environment (ie dev, staging, prod) as it is managed with the same tools. Some IaaS services are not compatible with true single tenant deployments as the backing services are multi-tenant in themselves.

## Private cloud (buyer managed)
Over the last seven years, enterprises have started to move away from physical data centers and the outsource the effort of racking & stacking servers to the IaaS providers (namely AWS, GCE & Azure). Often times they’ll start to move enterprise workloads over to cloud providers and setup a private network that those servers access. As they do so, the tooling that is available in those cloud platforms, which is often leveraged by SaaS companies in their multi-tenant deployments (ie RDS, S3, SNS, Lambda), are also available for use by the SaaS vendor for enterprise private cloud installations. This means that SaaS vendor can reach a certain portion of the enterprise market by making private instances available in whatever cloud provider they use for their multi-tenant deployments.

## On-prem datacenter (buyer managed)
The largest enterprise buyers (banks, governments, healthcare orgs, telcos) often have some infrastructure that they’d like to continue to utilize. To reach these customers (as well as enterprises looking to deploy into a private cloud on a IaaS), SaaS providers will need a fully portable version of their application that can be deployed and managed anywhere.

We cover the product features that SaaS vendors should consider when building a version of their application that can be managed as a private instance by their enterprise customers in our overview of [enterprise deployment models](/features/deployment-options).
