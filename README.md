# is-a-dev Registration

This repository contains the necessary files for registering a custom subdomain via is-a.dev for outbound email using Resend.

## Steps to Register a Domain
1. **Fork the Repository**: Fork the repository at [is-a-dev/register](https://github.com/is-a-dev/register).
2. **Create Domain Configuration**: The domain configuration file is located at `domains/paperclip.json`. It contains the following:
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
3. **Submit PR**: After forking and making changes, submit a Pull Request to the original repository.
4. **Verify DNS**: Once approved, add the domain in the Resend dashboard at [resend.com/domains](https://resend.com/domains) and verify the DNS settings.
5. **Update Configuration**: Update the `CORS_ORIGIN` and `WORKER_URL` in `wrangler.toml` if the domain changes.
6. **Update Email Sending Code**: Ensure the `from` address in `worker/src/tools/comms.ts` is updated to use the new domain.

## Note
Ensure all steps are followed carefully to avoid issues with email sending capabilities.