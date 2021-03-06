---
layout: post
title: "Viewing your world through security-colored DevOps glasses"
date: 2021-01-19
comments: true
author: Rackspace Onica Team
published: true
authorIsRacker: true
categories:
    - DevOps
    - Security
metaTitle: "Viewing your world through security-colored DevOps glasses"
metaDescription: "In a utopian world, the security team works alongside operations, developers and business
owners, who collaborate, share goals, code, and use the same tools. Such organizations embed security throughout the
value supply chain. Complying with minimal regulations or certifications required by governments and customers, and
creating a wide window of exposure should be the goal for any first-class technology organization."
ogTitle: "Viewing your world through security-colored DevOps glasses"
ogDescription: "In a utopian world, the security team works alongside operations, developers and business
owners, who collaborate, share goals, code, and use the same tools. Such organizations embed security throughout the
value supply chain. Complying with minimal regulations or certifications required by governments and customers, and
creating a wide window of exposure should be the goal for any first-class technology organization."
slug: "viewing-your-world-through-security-colored-devops-glasses"
canonical: https://onica.com/blog/devops/viewing-world-security-coloured-devops-glasses/
---

*Originally published in Oct 2017, at Onica.com/blog*

Complying with minimal regulations or certifications required by governments or customers and creating
a wide window of exposure should be the goal for any first-class technology organization. 

<!--more-->

### Is security embedded throughout the value supply chain of your organization?

In a utopian world, the security team works alongside operations, developers and business owners, who collaborate,
share goals, code, and use the same tools. Such organizations embed security throughout the value supply chain,
including the following aspects:

- Service design, including threat modeling.
- User stories that include security acceptance criteria.
- Security engineers who promote changes.
- Security policies and standards translated into code.
- Developers and operations who interact with the security services by using APIs.
- Security teams who constantly create test frameworks to streamline the delivery pipeline.
- Security engineers who create safe code to handle untrusted input.
- Security events that are collected, aggregated, and correlated, leveraging data science capabilities to make informed decisions.

This utopian organization is very difficult to grasp because security is considered an afterthought, where risk assessments
take place annually, coupled with penetration testing. The goal is to comply with the minimal regulations or certifications
required by governments and customers, creating a wide window of exposure and only covering a small portion of the services.

For Agile teams, traditional security represents a waterfall model. This is the opposite of Agile, where the security
organization’s responsibility is to define policies and standards that are almost impossible to translate into the Agile
processes.  For this reason, security usually ends up applying at the perimeter, mostly focused on the infrastructure
(such as firewalls, IDS/IPS, WAF, or SIEM) but very far from the applications or services.

This model is far from optimal. One of the biggest problems of the security field is that failure to provide an adequate
level of protection can cause huge damage to organizations and their customers. In the worst cases, these lead to massive
loss of trust and headlines in the news such as:

- [Equifax officially has no excuse](https://www.wired.com/story/equifax-breach-no-excuse/)
- [Health Insurer Anthem is hacked, exposing Millions of patients data](https://www.wired.com/2015/02/breach-health-insurer-exposes-sensitive-data-millions-patients/)
- [Every single Yahoo account was hacked – 3 billion in all](https://money.cnn.com/2017/10/03/technology/business/yahoo-breach-3-billion-accounts/index.html)

Having the right level of security is hard to achieve, and budget constraints don’t make it any easier. With Agile
development and DevOps movements increasing the rate of change, the gap between the security team's desired state
and actual state increases. However, security teams can be part of this DevOps cultural movement, helping developers
and operations to deliver incremental, efficient, and secure features to customers.

DevOps is a cultural mindset where the operations department works alongside developers, sharing goals and tools,
collaborating, and embracing change. DevOps promotes incremental changes, creating a value supply chain process that
allows you to introduce changes rapidly while providing confidence. Adding security to this cultural mindset is a must
for the modern and agile organization that know it must integrate security into its current teams and processes.

Adding security to the DevOps movement&mdash;DevSecOps, or Rugged Software&mdash;allows development, operation, and
security teams to work together, with wide communication channels. Understanding that security is everyone’s goal, they
can then embrace change with a security mindset and look for new and Agile methods to solve security problems.

### How can you organize your teams?

You should embed security into the development and operation processes. For this reason, every Agile team should
have a security engineer. An engineer who understands development and security, supporting the team with security
coding practices, translating the security policies and standards into code, and creating a feedback loop from the
Agile team to the security organization can improve those policies and standards.

This security engineer can be part of multiple Agile teams, participating in application design discussions, sprint planning,
review and retrospective meetings, and specific stand-ups depending on the user stories that are part of the sprint. The risk
associated with these user stories could help define the level of participation of the security engineer. Some user stories
implement functionalities with medium or high risk, such as the following ones:

- data moving across trust boundaries
- user-submitted input
- elevation of privileges
- storing or retrieving personally-identifiable information, protected health information, or credit card data

These stories might require more participation, either providing guidance on the security controls to be implemented
or creating security tests to evaluate the effectiveness of the implemented security controls.

This approach increases the security awareness and security coding standards of the team while gradually instilling a security
mindset in the members of the Agile team. Also, just as operations must be a part of the Agile team&mdash;describing and
implementing the Infrastructure-As-Code&mdash;the security operations team should be a part, implementing the security
controls at the infrastructure level as code by using the same tools as the operations team. These tools include implementing
configuration management, defining container images, and writing network security policies as code (Ansible or API-driven).
You might also have security checklists that translate into code by the security teams, working together with operations.
You can add security infrastructure tests to provide confidence over the security controls.

### Integrate security with the Agile processes

I an Agile software development lifecycle, an iterative process using the [Microsoft Security SDLC](https://www.microsoft.com/en-us/securityengineering/sdl/) and scrum, you can integrate security as follows:

- **Requirements gathering:** Include security requirements as part of non-functional requirements.

- **System design:** Use [threat modeling](https://owasp.org/www-community/Application_Threat_Modeling) to identify,
  quantify, and address the security risk associated with an application.

#### Implementation

Consider the following agile principles when implementing security:

- **Backlog grooming:** Review and update the threat model, define security acceptance criteria for user stories, and define
  security tests as part of user stories.
- **Sprint planning:** Explain security acceptance criteria to the team before committing to the user stories to implement
  during the sprint.
- **Sprint:** Perform security-static analysis of the code, implement security tests including fuzzing or dynamic analysis
  based on the application domain, vulnerability dependency check (check vulnerabilities in libraries and other dependencies,
  as well as the use of approved or trusted dependencies). You can implement these tasks as part of the CI/CD.
- **Sprint review:** Share results of security tests and controls that you implemented.
- **Sprint retrospective:** Use collected data and team self-evaluation to improve the process.

#### Production

After your project goes into production, peform the following tasks:

- Perform continuous dynamic analysis tests on the production platform to identify security gaps.
- Collect and correlate events, aggregating data from multiples sources, providing greater visibility, and allowing informed decisions.
- Develop and improve an Incident Response Plan.

Having an updated threat model of the application is very important. This enables the team to apply the right security
controls to mitigate the identified security threats. Implementing TLS and Deep Packet Inspection firewalls won’t protect
the application from SQL injection attacks. Only input validation, applying whitelisting or input sanitization coupled with
SQL prepared statements, can provide an adequate level of protection.

As the code moves through the different stages of the CI/CD pipeline, security controls can test the security of the changes.
Checking for known vulnerabilities in the application’s dependencies can help with tools like the
[OWASP Dependency-Check Project](https://owasp.org/www-project-dependency-check/). Also, having a list of tested and approved
dependencies that are constantly updated and enforced in the CI/CD helps to mitigate
[typo-squatting attacks](https://www.csoonline.com/article/3214624/malicious-code-in-the-node-js-npm-registry-shakes-open-source-trust-model.html)
that inject malicious packages into known registries with names very similar to existing packages.

Vulnerability scanning tools can test security in the CI/CD. It’s important to have an updated vulnerability database with
alerting capabilities to notify the team if the database failed to update. These tools can also add the current database release
date to the testing report.

Security policy enforcement and reporting is a must for highly regulated companies. Requirements like strong authentication,
use of multi-factor authentication (MFA), and data encryption at rest and in transit can work together with the operations team.
The use of cloud platforms also helps to simplify this process, where policies translate directly into code.

Cloud platforms like AWS&reg; enable you to achieve MFA enforcement and reporting by using IAM policies coupled with the AWS
Config&reg; service, which use rules to trigger alarms or specific actions in response to changes to the configuration. For
example, EC2&reg; instance tags and specific AWS Config rules can help with data classification values (public, private, secret,
and so on) based on the processed or stored data. You can check the existence of this tag, and validate that you encrypt volumes
where the data classification value is equal or greater than **secret**. Using the same concept, AWS Config rules can check the
use of TLS v1.1 or v1.2 as the only available policies in the load balancers or check S3 bucket permissions to prevent public access.

Adding a Blue/Red team approach to the preceding process improves the security of the services and the organization as a whole.
Having a team continuously challenging the security controls and attempting different attack vectors to gain access to the resources
fits well with the Agile mindset.

#### Conclusion

Security must be a part of all of the organization’s processes to be effective. Leaving security as an afterthought leads to higher
security risks, while enforcing security policies and standards without teaming-up with the rest of the organization creates more
friction and insecure services. Security must embrace the DevOps mindset to keep up with the rapid pace of change and continuously
add value to the customers. While no one solution or recipe can fit all organizations, applying Agile values and practices is a good
starting point.

<a class="cta red" id="cta" href="https://www.rackspace.com/security">Learn more about our Security services.</a>

Use the Feedback tab to make any comments or ask questions. You can also click
**Sales Chat** to [chat now](https://www.rackspace.com/) and start the conversation.
