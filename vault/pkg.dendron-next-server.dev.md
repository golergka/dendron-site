---
id: 6293d9dc-9bd3-4b01-8428-34d8256f0a32
title: Dev
desc: |
  Development related
updated: 1624923212836
created: 1621630111186
---

## Development

### Pre-req
- [[Symlink|pkg.dendron-cli.dev#symlink]] `dendron-cli`
- [[Setup|dendron.dev.setup]] `plugin-core`
- Read [[Next Server Architecture|pkg.dendron-next-server.arch]]

### Steps

You can test the Dendron Next App by launching a workspace using the CLI and then connecting to it. The instructions below cover using `dendron/test-workspace` which is alreayd pre-configured to use a local nextjs setup.
1. Initialize test-workspace
  ```sh
  cd dendron/test-workspace
  ./scripts/dev.sh
  ```
1. (optional) To connect to the workspace using chrome, enter the following in your localhost (replace WORKSPACE and PORT with your own values) ^MgEdJdyD
   ```sh
   # for example, if you launched the engine at /user/adam/workspace, WORKSPACE should equal /user/adam/workspace
   http://localhost:3000/vscode/sample?ws=$WORKSPACE&port=$PORT
   ```
1. To test the UI with the plugin, see instructions to [[run the extension|dendron.dev.debug#run-extension]]. When running, make sure use `test-workspace` to access the UI

Next Steps:
- read the [[architecture|pkg.dendron-next-server.arch]] documents to understand how the next server fits in with other Dendron plugins and how to build on top of it

### PR Checklist
- see [[Pull Request|dendron.dev.pull-request]]
- [ ] make sure your UI is compatible with light/dark theme 

## Remote Development

Follow the same instructions to run Dendron remotely. If you are using VSCode, use the port forwarding features to forward the ports of both engineServer and the next-server.

## Issues

### Conflicting Views
- if you have conflicting views warning when debugging, its most likely because you've installed Dendron in the same version of VSCode that you are developing on. We highly recommend you keep two instances of VSCode and not install Dendron on the version you use for development


## Cook

### Creating new Async Thunk Method
- [enhance: Only Sync changed notes for preview by kevinslin · Pull Request #969 · dendronhq/dendron](https://github.com/dendronhq/dendron/pull/969)

