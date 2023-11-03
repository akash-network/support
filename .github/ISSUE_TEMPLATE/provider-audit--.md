---
name: "[Provider Audit] Template"
about: This is for Akash users interested in having their providers audited by Akash
title: "[Provider Audit] Template"
labels: Provider Audit
assignees: andy108369

---

# Audit Steps:

- ***Title the issue: " [Provider Audit]: Provider Address" (e.g. "[Provider Audit]: provider.europlots.com")***
  
- Make sure your provider has community provider attributes:

```
  Example:
  $ provider-services query provider get akash1<REDACTED> -o text
  ...
  attributes:
  ...
  - key: host
  value: akash
  - key: tier
  value: community

```

[Ref documentation:[https://docs.akash.network/providers/akash-audited-attributes#standard-attributes](https://docs.akash.network/providers/akash-audited-attributes#standard-attributes).
- Make sure your provider *.ingress resolves to your provider IP (ideally worker node IP)
```
host <anything>.ingress.<yourdomain>
```

Example:
```
$ host anything.ingress.akash.pro
anything.ingress.akash.pro is an alias for nodes.akash.pro.
nodes.akash.pro has address 65.108.6.185
```

- More info on what DNS records should look like are available in the [Akash Documentation here](https://docs.akash.network/providers/build-a-cloud-provider/akash-cloud-provider-build-with-helm-charts/step-5-domain-name-review).
- Please make sure your Akash provider doesn't block these ports
- If you are using a firewall, please follow this doc:
https://docs.akash.network/providers/build-a-cloud-provider/akash-cloud-provider-build-with-helm-charts/step-9-firewall-rule-review
- If you are behind NAT, then you need to make sure these ports are open between your provider worker nodes and the internet.

- Wait for response via comments. If no issues during provider Audit, process will be complete, provider should start bidding on leases, and Audit ticket will be closed.
- If there are issues during the provider Audit, debug those issues, and Audit will be complete.
- Audit Issue will be closed by core team member.


## Leave contact information (optional)
1. Name
2. Discord handle or Telegram handle
3. Contact email address
