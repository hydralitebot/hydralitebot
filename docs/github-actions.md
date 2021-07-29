# Usage in GitHub Actions

To use me in API calls and actions in an GitHub Actions workflow, either use `${{ secrets.HYDRABOT_GH_PAT }}` in the action's `with.token` key (sometimes its `with.gh-token` or `with.repo-token` or as an environment variable, like this:

```yml
# in an usual script
- name: Publish cz-commitlint-config package
  run: |
    cd cz-commitlint-config
    echo "@hydralite:registry=https://npm.pkg.github.com"
    npm version ${{ github.ref }} # assuming it was triggered by an pushing an Git tag
    npm publish
  env:
    NPM_TOKEN: ${{ secrets.HYDRABOT_BH_PAT }}

# Copied from https://github.com/code-server-boilerplates/nodejs-starter/blob/7bffa154b7e8c6246b25a19094f578cd689fabe3/.github/workflows/update-labels.yml#L17-L36
# The difference would be in this one we use HYDRABOT_GH_PAT instead of the usual GH_SERVICE_ACCOUNT_API_KEY from The Pins Team's projects.
- name: Update issue labels
  if: success()
  uses: crazy-max/ghaction-github-labeler@v3
  with:
    github-token: ${{ secrets.HYDRABOT_GH_PAT }}
    yaml-file: .github/labels.yml
    skip-delete: false
    dry-run: false
    # These labels included in your default labels settings are excluded
    # you need to manually add them to .github/labels.yml and remove the entries here
    exclude: |
      documentation
      help wanted
      wontfix
      bug
      invalid
      question
      enhancement
      duplicate
      good first issue
```

## More Examples

* [Development Container CI](https://ithub.com/MadeByThePinsHub/hydralite/blob/gitpodify/.github/workflows/docker-dev_container.yml)
