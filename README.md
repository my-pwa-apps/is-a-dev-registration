# is-a-dev-registration

This repository is intended for registering a custom subdomain with is-a.dev for the purpose of outbound email using Resend.

## Steps to Register Custom Subdomain
1. Fork the [is-a-dev/register](https://github.com/is-a-dev/register) repository.
2. Create the following JSON file:
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
3. Submit a Pull Request with your JSON file.
4. Once the PR is approved, add the domain in the Resend dashboard at [resend.com/domains](https://resend.com/domains) and verify DNS settings.
5. Update the `CORS_ORIGIN` and `WORKER_URL` in the `wrangler.toml` file if the domain changes.
6. After the domain is live, update the `from` address in `worker/src/tools/comms.ts` to use the new domain.