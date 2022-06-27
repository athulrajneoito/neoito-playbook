# Working with Secrets in Source Control
The best way to avoid leaking secrets is to store them in local/private files and exclude these from git tracking with a [.gitignore](https://git-scm.com/docs/gitignore) file. E.g. the following pattern will exclude all files with the extension `.private.config`:
```
# remove private configuration

*.private.config
```
For more details on proper management of credentials and secrets in source control, and handling an accidental commit of secrets to source control, please refer to the [Secrets Management](https://neoito-hub.github.io/code-with-engineering-playbook/continuous-delivery/secrets-management/) document which has further information, split by language as well.

As an extra security measure, apply [credential scanning](https://neoito-hub.github.io/code-with-engineering-playbook/continuous-integration/dev-sec-ops/secret-management/recipes/detect-secrets/) in your CI/CD pipeline.