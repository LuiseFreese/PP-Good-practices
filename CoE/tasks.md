# tasks

1. Check that the CoE toolkit is installed
   - ✅ Ensure all components (Power BI dashboard, apps, flows) are installed
   - ✅ Verify that the correct permissions have been granted to admins and users
   - ✅ Test the Power BI reports to ensure data is populating
   - Reference: [Power Platform CoE Installation Guide](https://docs.microsoft.com/power-platform/guidance/coe/setup)

2. Get familiar with the Power Platform admin center
   - ✅ Explore the admin center and identify key areas: Environments, Data Policies, Security Roles, Capacity
   - ✅ Learn how to navigate between the different sections for Power Apps, Power Automate, and Dataverse
   - ✅ Review documentation for any specific admin settings you are unfamiliar with
   - Reference: [Power Platform Admin Center](https://docs.microsoft.com/power-platform/admin/admin-documentation)

3. Create an environment strategy
   - ✅ Identify the environments needed (Development, Building, Testing, Production)
   - ✅ Decide how many environments are appropriate based on the size and complexity of your organization
   - ✅ Establish policies for environment lifecycle management (e.g., who can create environments, naming conventions)
   - Reference: [Environment Strategy for Power Platform](https://docs.microsoft.com/power-platform/admin/environments-overview)

4. Set up Data Loss Prevention (DLP) policies
   - ✅ Define which connectors are allowed and restricted in each environment (consider environments with sensitive data first)
   - ✅ Group environments into DLP policy zones: Business, Non-business, and Blocked
   - ✅ Review default connectors and limit external sharing or data exposure where necessary
   - Reference: [DLP Policy Overview](https://docs.microsoft.com/power-platform/admin/wp-data-loss-prevention)


5. Prioritize high-impact DLP rules
   - ✅ Focus on production environments first, ensuring that critical data is protected
   - ✅ Loosen DLP rules for development and test environments if needed but monitor usage
   - ✅ Review and adjust policies regularly based on changes in business needs
   - Reference:

6. Assign roles in environments
   - ✅ Ensure admins have full access to manage environments, apps, and flows.
   - ✅ Assign limited roles to makers and users (e.g., “Environment Maker,” “App Opener”)
   - Reference:

7. Set up alerts for new apps and flows
   - ✅ Create a Power Automate flow to alert admins when new apps or flows are created
   - ✅ Review newly created apps and flows to ensure compliance with policies.
   - ✅ Set thresholds for alerting (e.g., trigger for apps using premium connectors)
   - Reference: [Monitor New Apps and Flows with CoE](https://docs.microsoft.com/power-platform/guidance/coe/core-components)

8. Track premium connectors
   - ✅ Use the CoE to monitor who is using premium connectors and where.
   - ✅ Set up notifications for apps using premium connectors without licenses.
   - ✅ Regularly review and audit the use of premium connectors to ensure proper cost management
   - Reference: [Manage Premium Connectors](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq)

9. Review current environments
   - ✅ Go through all existing environments and assess their purpose
   - ✅ Remove or archive inactive or unnecessary environments
   - ✅ Ensure that each environment has an assigned owner
   - Reference: [Manage Environments](https://docs.microsoft.com/power-platform/admin/environments-administration)

10. Tag environments properly

- ✅ Apply appropriate tags to each environment (e.g., `Development`, `Production`,`Sandbox`)
- ✅ Use consistent naming conventions for easy identification
- ✅ Regularly review and update environment tags to reflect changes in usage
- Reference:

11. Monitor the Power Apps and Power Automate usage

- ✅ Use CoE dashboards to review app and flow usage data
- ✅ Identify and retire unused or redundant apps/flows
- ✅ Focus on optimizing apps with high usage for better performance and efficiency
- Reference:

12. Track who owns what apps and flows

- ✅ Review ownership for all apps and flows
- ✅ Assign new owners for orphaned resources (e.g., if someone has left the company)
- ✅ Ensure each critical app/flow has a primary and backup owner
- Reference:

13. Enforce secure sharing practices

- ✅ Review the sharing settings for apps and flows
- ✅ Remove unnecessary users or groups from sensitive apps/flows
- ✅ Implement role-based sharing policies to restrict access where needed
- Reference:

14. Monitor environment capacity

- ✅ Use the CoE to track storage and capacity usage in each environment
- ✅ Remove unused resources to free up capacity
- ✅ Adjust environment settings to optimize performance based on capacity needs
- Reference: [Capacity Management in Power Platform](https://docs.microsoft.com/power-platform/admin/capacity-storage)

15. Review Power Platform licenses

- ✅ Audit licenses to ensure they are being used efficiently
- ✅ Reassign or remove licenses that are underutilized
- ✅ Monitor users of premium features to ensure license compliance
- Reference: [Power Platform Licensing Guide](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq)

16. Run a security audit using CoE

- ✅ Use the security features in CoE to audit permissions and access
- ✅ Identify any security risks or gaps in roles and permissions
- ✅ Share audit results with the team and recommend changes
- Reference: [Security and CoE Toolkit](https://docs.microsoft.com/power-platform/guidance/coe/core-components)

17. Document your policies

- ✅ Write up DLP, environment, and security policies
- ✅ Store the documentation in a central place where all admins can access it
- ✅ Regularly review and update the documentation as policies evolve
- Reference:

18. Set up a backup policy for critical apps and flows

- ✅ Identify business-critical apps and flows
- ✅ Set up automated backup processes
- ✅ Educate app makers about the importance of building in redundancy
- Reference:
