# kibana-express-session

A Kibana plugin to check if a user is authenticated. Uses `express-session-hapi` module
to check for session data in Redis.

## Usage

    ./bin/kibana plugin -i kibana-express-session -u https://github.com/kadishmal/kibana-express-session/releases/download/v1.0.0/kibana-express-session.zip

**Notice** that when specifying a URL via `-u` flag, Kibana requires the URL to point
to a ZIP file which includes all the dependencies. Kibana doesn't run `npm install`
when installing a plugin. So, the ZIP file should be archived and uploaded somewhere.
Follow the **Build** section below for build instructions.

## Options

```yaml
kibana-express-session: 
  cookieName: ''
  # Disable or enable this Kibana plugin.
  enabled: true
  redis:
    host: ''
  secret: ''
```

Basically, the same options accepted by `express-session-hapi` module
are accepted by `kibana-express-session`.

## Build

    grunt build

This generates a ZIP files into `build/` directory. Upload this archive to the **Releases**
tab in the Github repository.
