# Synced Repository-Project Template
Repository with actions to automatically groom a project board.

Relies on 2 actions:
- [add-to-project]()  
  Based on [this marketplace action](https://github.com/marketplace/actions/add-to-github-projects).  
  Any opened actions will be added to the configured project.
- [issue-link](https://github.com/marketplace/actions/add-an-issue-link)  
  Based on [this marketplace action](https://github.com/marketplace/actions/add-an-issue-link).  
  For any branch that starts with the prefix `issue-<number>`, the corresponding PR's text description will be automatically edited to link it to an existing issue.  
  _Note: linking the PR to the issue could actually be achieved manually like [this](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue) too._
  

## Configuration
### Project URL
Project URL's is in the form:
`https://github.com/<orgs/users>/<orgName|userName>/projects/<projectNumber>`.  
Edit it [here](https://github.com/r1oga/repo-project-template/blob/962ac27dde90c6f7cbc58327a7b1855bfba91cb2/.github/workflows/add-to-project.yml#L14).

### Token
- Create a GitHub [personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token), give it the `repo` and `projects` full permissions. Copy token value.
- Create a `TOKEN` [encrypted secret](https://docs.github.com/en/actions/security-guides/encrypted-secrets#creating-encrypted-secrets-for-a-repository). Paste token value for the `TOKEN` secret

### More
Label filters, add PRs to project, other event triggers, edit issue link text...  
Consult directly GH actions documentation:  
- [add-to-project](https://github.com/marketplace/actions/add-to-github-projects)
- [issue-link](https://github.com/marketplace/actions/add-an-issue-link)
