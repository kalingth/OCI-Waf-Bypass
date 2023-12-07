# OCI Waf Bypass

## Abstract

One day, after my session expired, I was redirected to the login screen. Upon trying to log in, I was redirected to a legacy login console page.

At this login screen, the page required my credentials once again. After inputting them, I was successfully logged into the legacy console page.

Something caught my attention: No MFA method was requested during the login process!

To prove that this is indeed a bug, I used another browser in incognito mode. I followed the default login flow process, and I successfully bypassed the MFA verification for my account by accessing the legacy console URL.

Moreover, within that legacy console, I was able to manipulate my MFA configurations and change my password without encountering any issues.

## About

This repository will be focused on publishing more information about a vulnerability that can be exploited to gain access to your Oracle Cloud Infrastructure, based on a weak MFA enforcement policy created by Oracle. I reported it to Oracle, but they informed me that it is a known issue that only affects some accounts under certain circumstances. Nevertheless, one of the impacted accounts is mine, and it could potentially have an impact on your account as well. By the way, you can find more information about this issue tracking in the **[Disclaimer](#disclaimer)** section.

### Disclaimer

All of the information provided here was previously authorized by Oracle and can be seen [here](DISCLAIMER.md).

### Write Up

All of the information on how an attacker can use that vulnerability to access your account can be seen [here](WRITEUP.md).

### Hotfix

The hotfix provided by Oracle to ensure that your account is secure can be viewed [here](HOTFIX.md)

## Conclusion

A cracker can use stolen passwords to access Oracle Cloud Infrastructure accounts, bypassing the MFA enforced by Oracle itself.
So, I recommend you to check your OCI configurations, and if your account is vulnerable, apply the hotfix described in the **[Hotfix](#hotfix)** section.

---

## References

https://docs.oracle.com/en-us/iaas/Content/Security/Reference/iam_security_topic-iam_mfa_identity_domains_signon_policy.htm
https://docs.oracle.com/en-us/iaas/Content/Security/Reference/iam_security_topic-iam_mfa_with_identity_domains.htm
https://docs.public.oneportal.content.oci.oraclecloud.com/en-us/iaas/Content/Security/Reference/dashboards-security.htm
https://docs.public.oneportal.content.oci.oraclecloud.com/en-us/iaas/Content/Security/Reference/iam_security.htm?Highlight=permission%20to%20inspect%20user%20groups 
