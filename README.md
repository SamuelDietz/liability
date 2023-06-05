![Don't install this package](liability.png)

![npm](https://img.shields.io/npm/v/liability)
![npm](https://img.shields.io/npm/dt/liability)
![GitHub](https://img.shields.io/github/license/SamuelDietz/liability)

# This package is a liability

It constantly triggers vulnerabilities of different severity levels by rotating installs of vulnerable packages. New versions are released every 5+ minutes.

If you do the mistake of executing

```bash
npm install liability
```

you can use of this package to test commands like `npm audit` or to test your CI/CD pipeline. It's also a good way to test your [Dependabot](https://github.com/dependabot) configuration.

_Please don't use this package in production._

## Package versions used to trigger vulnerabilities

| severity | package@version       |
| -------- | --------------------- |
| critical | lodash@4.17.4         |
| high     | lodash@4.17.20        |
| moderate | swagger-ui-dist@4.1.2 |
| low      | timespan@2.3.0        |
