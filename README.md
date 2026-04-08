# is-a-dev Registration

This repository is dedicated to registering a custom subdomain via the [is-a.dev](https://is-a.dev) service for use as an outbound email sender domain.

## Steps to Register a Custom Domain

1. **Fork the Repository**: Start by forking this repository.
2. **Prepare Domain Registration**: Create a JSON file to register the domain. The example JSON is provided in `domains/paperclip.json`.
3. **Submit a Pull Request**: Once the JSON file is ready, submit a pull request to the original [is-a.dev/register](https://github.com/is-a-dev/register) repository.
4. **Add Domain in Resend**: After the PR is approved, go to the Resend dashboard and add the new domain.
5. **Verify DNS Records**: Ensure that the necessary DNS records are set up correctly.
6. **Update Codebase**: Update the 'from' address in the `worker/src/tools/comms.ts` file to reflect the new domain.

## Example Domain Registration JSON
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