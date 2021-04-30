---
title: Configuring npm for use with GitHub Packages
intro: 'You can configure npm to publish packages to {% data variables.product.prodname_registry %} and to use packages stored on {% data variables.product.prodname_registry %} as dependencies in an npm project.'
product: '{% data reusables.gated-features.packages %}'
redirect_from:
  - /articles/configuring-npm-for-use-with-github-package-registry
  - /github/managing-packages-with-github-package-registry/configuring-npm-for-use-with-github-package-registry
  - /github/managing-packages-with-github-packages/configuring-npm-for-use-with-github-packages
  - /packages/using-github-packages-with-your-projects-ecosystem/configuring-npm-for-use-with-github-packages
versions:
  free-pro-team: '*'
  enterprise-server: '>=2.22'
  github-ae: '*'
---

{% data reusables.package_registry.packages-ghes-release-stage %}
{% data reusables.package_registry.packages-ghae-release-stage %}

{% data reusables.package_registry.admins-can-configure-package-types %}

{% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.22" or currentVersion == "github-ae@latest" %}
### Limits for published npm versions

If you publish over 1,000 npm package versions to {% data variables.product.prodname_registry %}, you may see performance issues and timeouts occur during usage.

In the future, to improve performance of the service, you won't be able to publish more than 1,000 versions of a package on {% data variables.product.prodname_dotcom %}. Any versions published before hitting this limit will still be readable.

If you reach this limit, consider deleting package versions or contact Support for help. When this limit is enforced, our documentation will be updated with a way to work around this limit. For more information, see "{% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@3.0" %}[Deleting and restoring a package](/packages/learn-github-packages/deleting-and-restoring-a-package){% elsif currentVersion ver_lt "enterprise-server@3.1" or currentVersion == "github-ae@latest" %}[Deleting a package](/packages/learn-github-packages/deleting-a-package){% endif %}" or "[Contacting Support](/packages/learn-github-packages/about-github-packages#contacting-support)."

{% endif %}

### Authenticating to {% data variables.product.prodname_registry %}


{% if currentVersion ver_gt "enterprise-server@2.22" %}
### Using the official NPM registry

{% data variables.product.prodname_registry %} allows you to access the official NPM registry at `registry.npmjs.com`, if your {% data variables.product.prodname_ghe_server %} administrator has enabled this feature. For more information, see [Connecting to the official NPM registry](/admin/packages/configuring-packages-support-for-your-enterprise#connecting-to-the-official-npm-registry).
{% endif %}

### Further reading

- "{% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@3.0" %}[Deleting and restoring a package](/packages/learn-github-packages/deleting-and-restoring-a-package){% elsif currentVersion ver_lt "enterprise-server@3.1" or currentVersion == "github-ae@latest" %}[Deleting a package](/packages/learn-github-packages/deleting-a-package){% endif %}"
