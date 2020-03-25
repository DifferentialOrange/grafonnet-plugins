# Grafonnet-plugins, a library with grafonnet extensions

A library that extends [grafonnet](https://github.com/grafana/grafonnet-lib) with some [plugin](https://grafana.com/grafana/plugins) panel templates.

## Getting started

### Prerequisites

[grafonnet](https://github.com/grafana/grafonnet-lib) and its dependencies must be installed.

### Install grafonnet-plugins

Clone this git repository inside the grafonnet one:

```
git clone https://github.com/DifferentialOrange/grafonnet-plugins.git
```

You can use [Jsonnet Bundler](https://github.com/jsonnet-bundler/jsonnet-bundler) instead:
```json
{
  "dependencies": [
    {
      "source": {
        "git": {
          "remote": "https://github.com/grafana/grafonnet-lib",
          "subdir": "grafonnet"
        }
      },
      "version": "master"
    },
    {
      "source": {
        "git": {
          "remote": "https://github.com/DifferentialOrange/grafonnet-plugins",
        }
      },
      "version": "master"
    }
  ],
  "legacyImports": true
}

```

Then import the plugins with grafonnet in your jsonnet code:

```jsonnet
local grafana = (import 'grafonnet/grafana.libsonnet')
              + (import 'grafonnet-plugins/plugins.libsonnet');
```

## List of supported plugins

### Status panel (by Vonage)

[Status panel (by Vonage)](https://grafana.com/grafana/plugins/vonage-status-panel). See [tests](./tests/vonage_status_panel/) for example.

## Contributing

Feel free to submit issues, as well as pull requests.
