# `grafana.base` - ContEco

Grafana Base image, with configuration changes.  
See `conteco.docs.overview` for more information on the ContEco ecosystem.

## Configuration Changes

```bash
### server ###
# Serve Grafana from subpath specified in `root_url` setting. By default it is set to `false` for compatibility reasons.
serve_from_sub_path = true

# Log web requests
router_logging = false

### Anonymous Auth ###
[auth.anonymous]
# enable anonymous access
enabled = true

# specify organization name that should be used for unauthenticated users
org_name = Conteco.

# specify role for unauthenticated users
org_role = Editor

### Logging ####
[log]
# Either "console", "file", "syslog". Default is console and  file
# Use space to separate multiple modes, e.g. "console file"
mode = console

# For "console" mode only
[log.console]
level = info

# log line format, valid options are text, console and json
format = json
```

## Tags

* 7.0.5    
* 6.3.5  
