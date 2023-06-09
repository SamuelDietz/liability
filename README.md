![Don't install this package](liability.png)

[![Create liabilities](https://github.com/SamuelDietz/liability/actions/workflows/create-liabilities.yml/badge.svg)](https://github.com/SamuelDietz/liability/actions/workflows/create-liabilities.yml)
![npm](https://img.shields.io/npm/dt/liability)
![GitHub](https://img.shields.io/github/license/SamuelDietz/liability)

# This package is a liability

It constantly triggers vulnerabilities of different severity levels by rotating installs of vulnerable packages. New versions are released every 60+ minutes.

if you make the mistake of executing

```bash
npm install liability
```

you can use this package to test your monitoring tools such as your [Dependabot](https://github.com/dependabot) configuration.

Due to the frequent updates, you probably want to screen for outdated and deprecated packages as well. Some useful commands to handle this liability are `npm audit`, `npm outdated` and `npm update`. For more help, check out the [npm cli commands](https://docs.npmjs.com/cli/v9/commands).

## Manual testing

If you don't like constant insecurity updates you might want to explicitly install a specific version of this package to test for the respective "feature":

| feature                           | install command                                   |
| --------------------------------- | ------------------------------------------------- |
| low severity vulnerability        | `npm i liability@1.2.9-low-vulnerability`         |
| moderate severity vulnerability   | `npm i liability@1.3.0-moderate-vulnerability`    |
| high severity vulnerability       | `npm i liability@1.3.1-high-vulnerability`        |
| critical severity vulnerability   | `npm i liability@1.3.2-critical-vulnerability`    |
| deprecated                        | `npm i liability@1.3.3-deprecated`                |
| fixed - but not for long          | `npm i liability@1.3.4-fixed`                     |

## Package versions used to trigger vulnerabilities

| severity | package@version       |
| -------- | --------------------- |
| critical | lodash@4.17.4         |
| high     | lodash@4.17.20        |
| moderate | swagger-ui-dist@4.1.2 |
| low      | timespan@2.3.0        |

Taken from the [GitHub Advisory Database](https://github.com/advisories?query=type%3Areviewed+ecosystem%3Anpm).

---

_Please don't use this package in production._
