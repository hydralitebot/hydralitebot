# Bitwarden Org Vault Documentation

## Instance Information

* **Instance Domain**: <https://vault.madebythepins.tk>
* **Hosting Service and Type**: Divio - PaaS (migrating to Railway soon, probably before second week of August)
* **From address**: <bitwardenrs@mail.madebythepins.tk> (may be changed to <vaultwarden@mail.madebythepins.tk> in the future
* **Issue Tracker**: Soon

**Notes, will be updated**:

* Export and import your data anytime. The vault org is all yours once you're an Org Owner/Admin.
* The Pins Team doesn't share your data to third parties, since the data is encrypted. Because Bitwarden is Zero Knowledge password manager, we cannot help you recover
your account in case yu lose access to it.
* Some features that requires HIBP API key isn't available in this Vaultwarden instance, particularly Exposed Passwords and Data Breach Report. If you have spare keys,
contact Andrei Jiroh so he can use it. Thank you for your help.

## Setup / Initial Steps

* Create an account at <https://vault.madebythepins.tk> and verify your account from the address specified above.
* Go to your account settings and copy your fingerprint pharse (for example, Andrei Jiroh's fingerprint pharse is `rambling-reroute-stunner-overhand-bullfight`).
Send that, along with your account email address to Andrei Jiroh over Discord so he can invite you to that org with permissions (maintainers has Owner/Admin role,
while regular developers with push access should have User role instead).
* Accept the org invite from email. After accepting, you can optinally remove Andrei Jiroh from the org or give him lower permissions, but if you REALLY trust him,
the Admin/Manager role across all collections should be fine.

## Using Bitwarden's Official Clients

Since Vaultwarden is Rust reimplemention of Bitwarden Self-hosted Server, which is resource-intenstive for an Raspberry Pi to run, it's compartible to the official
Bitwarden clients, as long as things don't break.

After installing one of their clients, [configure your client](https://bitwarden.com/help/article/change-client-environment/) to point into our Vaultwarden instance
before logging in. You can sign in after configuring your client.
