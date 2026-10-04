# cpa-plugins

CLIProxyAPI plugin store registry for the plugins we run, each pointing at a fork whose source
was reviewed before release. Releases are built by GitHub Actions in each fork, from the tagged
source.

Add to CPA's `config.yaml`:

```yaml
plugins:
  store-sources:
    - "https://raw.githubusercontent.com/trancong12102/cpa-plugins/main/registry.json"
```

CPA only offers an update to a plugin from the source it was installed from, so a plugin
installed from here will not be "updated" back to the official store build.
