## Lempar! 

**Automated & Integrated Deployment Tools for cPanel**.

## What it does?

- Create a preview & stagging Url, hosted on your cPanel account.
- Create a deployment to your production environment when you Merge the git.

## How it works?

We utilize your cPanel hosting account to be your automated preview and stagging hosting whenever you make a PR, or push the commits to a certain branch. This means you can always find any hosting provider that suites your need to be used as your preview site without affecting your production.

Essentially, this is like *(cough)N*tlify(cough)*, but it hosted in your cPanel account.

## Requirements

### Account Plan Requirements

- Domain, one subdomain that have wilcardly directed to your cPanel instance. (e.g `*.lihat.christianto.net` → `pokémonname.cpanelhostingservice.tld`)
  - Essentially this means your account have to have the ability to add, edit, remove domains. (for now)
- DNS Zone Edit permission
- Database, with ability to create and delete the database.
- Enough disk to host your repo.

### Platform Requirements

- GitHub / GitLab integration (meaning the vendor have to create a GitHub / GitLab Apps, get the consumer tokens and secrets registered to the system)
- Uninterrupted Internet connection to GitHub / GitLab.
- This project's system requirements.

## Features

- Phase 1
  - Autodeploy when MR/PR is created.
  - Autopull on commit push (should we use git functionality from cPanel?)
  - Bot that give comments containing the url
- Phase 2 (still in research, this might change with no notice)
  - Dynamic DNS (use single wildcard domain, root folder change done in `htaccess`)
  - Instance cap limit
    - Max active instance
    - Stale instance removal

## License

[MIT](LICENSE).