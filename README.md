<h1 align="center">
  Shared Github actions for the Dyne Organizations</br>
</h1>

<br><br>

<h4 align="center">
 <a href="#-node-ecosystem">📦 Node ecosystem</a>
  <span> • </span>
  <a href="#-docker">🐋 Docker</a>
  <span> • </span>
  <a href="#-acknowledgements">😍 Acknowledgements</a>
  <span> • </span>
  <a href="#-links">🌐 Links</a>
  <span> • </span>
  <a href="#-contributing">👤 Contributing</a>
  <span> • </span>
  <a href="#-license">💼 License</a>
</h4>



***
## 📐 Starters ecosystem

### Deploy a pocketbase instance

Deploy automatically on the pocketbase server create a file 
under `.github/workflows/pocketbase.yml` with the following content

```
name: 🚀 Backend deploy

on:
  push:
    branches: [ "main" ]

jobs:
  build:
    uses: dyne/workflows/.github/workflows/pocketbase-deploy.yml@main
    secrets: inherit
    with:
      project_name: your_project_name
      fqdn: "https://your-backend.dyne.org:8090"
```


## 📦 Node ecosystem

### Deploy on baloo.dyne.org the staging environment

Deploy automatically on the staging server create a file 
under `.github/workflows/deploy-baloo.yml` with the following content

```
name: 🚀 Staging deploy

on:
  push:
    branches: [ "main" ]

jobs:
  build:
    uses: dyne/workflows/.github/workflows/node-staging-deploy.yml@main
    secrets: inherit
    with:
      deploy_url: https://your-site-name.dyne.org
```

***
## 🐋 Docker

### Publish your docker image on the github ghcr hub

Create and release docker images that you can see in the packages section
of your project.
Create a file under `.github/workflows/docker-publish.yml` with the
following content:

```
name: 🐳 Create and publish a Docker image

on:
  push:
    branches: ['main']

jobs:
  publish_docker_image:
    uses: dyne/workflows/.github/workflows/docker-publish-to-ghcr.yml@main
    secrets: inherit
```

***
## 😍 Acknowledgements

<img alt="software by Dyne.org" src="https://files.dyne.org/software_by_dyne.png" height="250"/>

Copyleft (ɔ) 2022 by [Dyne.org](https://www.dyne.org) foundation, Amsterdam

Maintained by Puria Nafisi Azizi and Alberto Lerda.


**[🔝 back to top](#toc)**

***
## 🌐 Links

https://docs.github.com/en/actions/using-workflows/sharing-workflows-secrets-and-runners-with-your-organization

https://dyne.org/

**[🔝 back to top](#toc)**

***
## 👤 Contributing

Please first take a look at the [Dyne.org - Contributor License Agreement](CONTRIBUTING.md) then

1.  🔀 [FORK IT](../../fork)
2.  Create your feature branch `git checkout -b feature/branch`
3.  Commit your changes `git commit -am 'Add some fooBar'`
4.  Push to the branch `git push origin feature/branch`
5.  Create a new Pull Request
6.  🙏 Thank you


**[🔝 back to top](#toc)**

***
## 💼 License
    Shared workflows for the Dyne organization
    Copyleft (ɔ) 2022 Dyne.org foundation, Amsterdam

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU Affero General Public License as
    published by the Free Software Foundation, either version 3 of the
    License, or (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU Affero General Public License for more details.

    You should have received a copy of the GNU Affero General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

**[🔝 back to top](#toc)**
