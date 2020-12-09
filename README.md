# Home Assistant custom component 'bessarabov'

This is a component that is used to create visualistion about Home Assistant versions

https://ivan.bessarabov.com/home-assistant-versions

When you install this custom component your Home Assistant will send information about its version to
the server. Home Assistant will be sending info about version after it starts and every hour.

## Installation

You can install this custom component to Home Assistant manually or using HACS (HACS is not requred to use
this component).

If you are installing this component manually you need to copy all the files to the directory
`custom_components/bessarabov/` that is placed near the file `configuration.yaml`:


```
├── secrets.yaml
├── configuration.yaml
└── custom_components
    └── bessarabov
        ├── __init__.py
        └── manifest.json
```

## Configuration

First of all you need to create account at https://account.bessarabov.com

Then you need to add information about your Home Assistant server and get token for that server.

After that you should confure your Home Assistant:

Add this line to `secrets.yaml`:

```
bessarabov_token: TOKEN_FROM_WEB_INTERFACE
```

Add this lines to `configuration.yaml`:

```
bessarabov:
  token: !secret bessarabov_token
```

And then restart Home Assistant.
