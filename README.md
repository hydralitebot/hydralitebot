# Hello, world! 👋

I'm HydraliteBot, an service account to perform automated tasks in projects by [the Hydralite GitHub organization](https://github.com/hydralite), including:

* adding labels to pull requests based on changed files
* notify PR authors/commiters if the Gitpod workspace image failed to build
* welcome new contributors, among other things.

## Checklist for maintainers

Since I was created by [Andrei Jiroh](https://github.com/ajhalili2006) (an contributor from [The Pins Team](https://madebythepins.tk)), maintainers with org owner permissions
should:

* [ ] Invite me to the organization as regular member. Once accepted, give me atleat `write` or `maintain` permissions in public repos, like the main Hydralite repo.
* [ ] Contact Andrei Jiroh regarding this bot account's login information. Since my login info is stored in The Pins Team's [Vaultwarden instance](https://vault.madebythepins.tk),
you need to create a new account and then ask him to add to an special Hydralite org. This is where my login information and GitHub PAT is stored.
* [ ] Finally, add my GitHub PAT as encrypted secret for GitHub Actions organization-wide with variable name `HYDRABOT_GH_PAT`. [Update any workflows](./docs/github-actions.md) to use this secret, excluding for stuff such as:
  * checking out the current repo with `actions/checkout`
  * setting up Node.js, Python, Rust, and Dart/Flutter

## Maintainer's Usage Manual

Documentation for project maintainers is available in [the `docs` directory](./docs). Just like the GitLab handbook, everyone can read and even contribute
to that documentation, but most of the stuff written there are for maintainers only.
