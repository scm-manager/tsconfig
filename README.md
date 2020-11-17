<p align="center">
  <a href="https://www.scm-manager.org/">
    <img alt="SCM-Manager" src="https://download.scm-manager.org/images/logo/scm-manager_logo.png" width="500" />
  </a>
</p>
<h1 align="center">
  @scm-manager/tsconfig
</h1>

TypeScript configuration for all SCM-Manager related projects.

## Installation

Install the `@scm-manager/tsconfig` as dev dependency:

```bash
yarn add --dev @scm-manager/tsconfig
# or 
npm install --save-dev @scm-manager/tsconfig
```

In order to use the config create a `tsconfig.json` in the root of the project with the following content:

```json
{
  "extends": "@scm-manager/tsconfig",
  "include": [
    "./src/main/js"
  ]
}
```

## Need help?

Looking for more guidance? Full documentation lives on our [homepage](https://www.scm-manager.org/docs/) or the dedicated pages for our [plugins](https://www.scm-manager.org/plugins/). Do you have further ideas or need support?

- **Community Support** - Contact the SCM-Manager support team for questions about SCM-Manager, to report bugs or to request features through the official channels. [Find more about this here](https://www.scm-manager.org/support/).

- **Enterprise Support** - Do you require support with the integration of SCM-Manager into your processes, with the customization of the tool or simply a service level agreement (SLA)? **Contact our development partner Cloudogu! Their team is looking forward to discussing your individual requirements with you and will be more than happy to give you a quote.** [Request Enterprise Support](https://cloudogu.com/en/scm-manager-enterprise/).
