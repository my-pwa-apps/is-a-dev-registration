# Custom Domain Registration for Outbound Email

## Overview
This repository contains the necessary JSON configuration for registering a custom subdomain via is-a.dev, enabling outbound email functionality through Resend.

## Steps to Register Domain
1. **Fork the Repository**: Fork the repository from [is-a-dev/register](https://github.com/is-a-dev/register).
2. **Create JSON Configuration**: The configuration file `domains/paperclip.json` has already been created. Ensure it contains the correct owner details and CNAME record.
3. **Submit Pull Request**: Submit a PR with the changes to the main repository.
4. **Verify Domain in Resend**: Once the domain is approved, add it to the Resend dashboard and verify the DNS settings.
5. **Update Application Code**: Ensure the `from` address is updated in the application to use the new domain.

## Additional Notes
For any issues or further assistance, please refer to the [is-a.dev documentation](https://docs.is-a.dev/) or contact support.