# PTY Terminal Application

This shows you how to set up the PTY/SSH terminal.

**Please mind that this is experimental**.

**It takes the client username and uses it on the server, so your username has to match a system user**

## Install dependencies

In `TerminalExtension`, run `npm install`.

## Configure

In `Terminal/metadata.json`:

```
{
  ...
  "enabled": true,
  "config": {
    "host": "YOUR.IP.ADDRESS.HERE:8080"
  },
  ...
}
```


## Enable

```
grunt packages:enable:Terminal
grunt packages:enable:TerminalExtension
grunt config manifest
```

## Running backend server

**The spawner must run with root privileges to spawn with correct uid**

### Run automatically on node server start

Enable `proxy.enable` in `TerminalExtension/metadata.json` and run grunt steps above.

### Running manually

Run `node src/packages/extras/TerminalExtension/spawner.js`
