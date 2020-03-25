# Status panel extension for grafonnet

A library that extends [grafonnet](https://github.com/grafana/grafonnet-lib) with [Status panel (by Vonage)](https://grafana.com/grafana/plugins/vonage-status-panel) plugin template.

Based on version 1.0.6 of Status panel.

## Getting started

### Prerequisites

[grafonnet](https://github.com/grafana/grafonnet-lib) and its dependencies must be installed.

### Install grafonnet-status-panel

Clone this git repository inside the grafonnet one:

```
git clone https://github.com/DifferentialOrange/grafonnet-status-panel.git
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
          "remote": "https://github.com/DifferentialOrange/grafonnet-status-panel",
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
              + (import 'grafonnet-status-panel/plugin.libsonnet');
```

## Example of usage

See [tests](./tests/test.jsonnet) for example.

## Contributing

Feel free to submit issues, as well as pull requests.
