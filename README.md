# bot-pat-example

To address concerns with allowing a GitHub Action to run with too much privilege, we can use a Personal Access Token or
PAT. These can be configured for specific repositories and if using [fine-grained tokens][pat-docs], can be strictly
limited.

[pat-docs]: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#fine-grained-personal-access-tokens

## Configuration

### Repository

#### Settings -> Actions -> General -> Workflow permissions

Select `Read and write permissions`

### Bot User Account

#### Settings -> Developer Settings -> Personal Access Tokens -> Fine-grained tokens

- Click `Generate new token`
- Add a meaningful name
- Choose an appropriate expiration time for your purposes
- Select `Only select repositories` for `Repository access`
- Click `Account permissions`
  - Select `Access: Read and write` for `Contents` and `Pull Requests`
  - Select `Access: Read-only` for `Secrets`
