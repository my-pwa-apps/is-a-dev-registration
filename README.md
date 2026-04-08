# is-a-dev-registration

This repository is created for registering a custom subdomain via is-a.dev for outbound email. The goal is to enable the use of a real sending domain for the Resend service to reach external customers, partners, and users.

## Steps to Register a Custom Domain
1. **Fork the Repository**: Fork the is-a-dev/register repository.
2. **Create Domain Registration JSON**: Prepare the following JSON file:
   ```json
   {
       "owner": {
           "username": "your-github",
           "email": "your@email.com"
       },
       "record": {
           "CNAME": "paperclip-ai.pages.dev"
       }
   }
   ```
3. **Submit Pull Request**: Add the JSON file to the repository and submit a Pull Request.
4. **Configure Resend**: Once the PR is approved, log into the Resend dashboard to add the new domain. Verify any required DNS records.
5. **Update Application Code**: Ensure that the `from` address in your application code (e.g., `worker/src/tools/comms.ts`) is updated to use the new domain.

## Additional Notes
- Alternative free options for domain registration include js.org and eu.org if is-a.dev is not suitable.