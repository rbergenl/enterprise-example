

The team is responsible for providing access to the Tools.

The team is responsible for providing company policies, guidelines, reference architectures, examples and best practices.

The team is responsible for providing the Pipeline Library to be used by teams who need CI/CD.
The [enterprise-pipeline-library](https://github.com/rbergenl/enterprise-pipeline-library) has been moved to its own repository so it can be loaded by a Jenkins pipeline.


# Email team onboarding to AWS
Beste collega’s,

Autorisatie ligt binnen het AD en kan beheerd worden met de standaard aanvraag verzoeken via service now: https://[organization].service-now.com/ (service catalogue/security/active directory)
De owner van onderstaande groepen in service now (Product Owner van team) de verzoeken goed te keuren, graag zelf even het verzoek inschieten via de link hierboven.
 
AD groepen – die toegang verlenen:
Production:
AWS_ORGANIZATION_TEAM_P_Reader
AWS_ORGANIZATION_TEAM_P_Admin
 
Staging:
AWS_ORGANIZATION_TEAM_S_Reader
AWS_ORGANIZATION_TEAM_S_Admin
 
Onderstaande de artifacts nodig in combinatie met de aangesloten PDF om in te loggen
 
ADFS/Opstap Link: https://idpv3.organization.nl/adfs/ls/IdpInitiatedSignOn.aspx?loginToRp=urn:amazon:webservices
 
Switchrole values:
Production:
AWSOrganizationTeamPReader
AWSOrganizationTeamPAdmin
 
Account ID: 1234567890
Account Alias: team-p
 
Staging:
AWSOrganizationTeamSAdmin
AWSOrganizationTeamSReader
 
Account ID: 0123456789
Account Alias: team-s
 
Als er vragen en of opmerkingen zijn dan horen we het graag.

En ik sluit deze mail nog even af met de een overzicht van de aansluit voorwaarden die we hebben geformuleerd:
https://digitaal.sharepoint.com/teams/cloud/std/SitePages/Requirements-aan-applicaties-in-de-Cloud.aspx

# Checklist before go live
- Test "migration" and rollback in acceptance as if it was production
    - What is the go live moment for the AWS setup. As in what points traffic to AWS instead of on-premise?
    - What would determine if a rollback is required?
        - How quickly can this be determined?
        - How quickly can this be executed?
    - Is it possible to do a partial migration (eg 10% of traffic and increase over time)
- Plan for production "migration"
    - What one action triggers the swap to AWS?
    - What time will the swapover be done? When is lowest traffic level?
    - Who will pull the trigger and what backup will be available?
    - Do DNS records need changing? If so, TTL will need to be reduced beforehand to ensure quick propagation
    - What would determine if a rollback is required?
        - How quickly can this be determined?
        - How quickly can this be executed?
    - Is it possible to do a partial migration (eg 10% of traffic and increase over time)
    - All APIs at once? or staggered?
- Change request submitted (shouldn't be done under predefined change as it's probably not low-risk)
- Get baseline for current performance:
    - Response time
    - Error rate etc
    - Availability
    - Good to have this data to compare to performance in AWS
- Add a testing phase after deployment is successful - maybe not necessary as long as ALB health checks are comprehensive.
- Security signoff?
- Update CMDB?
- Monitoring - What is your SLA for in the cloud? I can help define SLIs and SLOs?
- Alerting definitely needs some focus.
- Loadtesting based on expected load will be really valuable for testing scale-up and down and performance. Ideally it would not only test peak load, but realistic load, so peaks, troughs and sudden changes in load to see how the auto-scaling
- On-call - ensure there are clear escalation pathways for incidents
