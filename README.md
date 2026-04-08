# Custom Domain Registration for Outbound Email

This repository is dedicated to registering a custom subdomain via is-a.dev for enabling outbound email functionality using Resend. Follow the steps below to complete the registration process.

## Steps to Register a Custom Domain
1. **Fork the Repository**: Go to [is-a-dev/register](https://github.com/is-a-dev/register) and fork the repository.
2. **Create Domain JSON**: Create a JSON file in the `domains` folder named `paperclip.json` with the following content:
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
3. **Submit a Pull Request**: After adding the JSON file, submit a Pull Request to the original repository and wait for it to be merged.
4. **Add Domain in Resend**: Once the domain is approved, go to the Resend dashboard (resend.com/domains) and add the domain.
5. **Verify DNS**: Copy the DNS TXT/MX records provided by Resend and add them to the is-a.dev zone (or wherever DNS is managed).
6. **Update Configuration**: If the domain changes, update the `CORS_ORIGIN` and `WORKER_URL` in `wrangler.toml`.
7. **Update Email Sending Code**: After the domain is live, update the `from` address in `worker/src/tools/comms.ts` to use the new domain.

## Conclusion
Following these steps will ensure that the custom domain is successfully registered and configured for outbound emails.