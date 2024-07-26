This is an experiment for a monorepo of Twilio flex plugins. It's failing on start with the error:

```
[DEBUG] Found command "flex:plugins:start" plugin: @twilio-labs/plugin-flex
 » twilio-cli encountered an unexpected error. To report this issue, execute the command with the "-l debug" flag, then copy the output to a new issue here: "https://github.com/twilio/flex-plugin-builder/issues"
[DEBUG] Cannot read properties of undefined (reading '@twilio/flex-ui')
[DEBUG] TypeError: Cannot read properties of undefined (reading '@twilio/flex-ui')
    at Object.isPluginFolder (/Users/leonardo/.twilio-cli/node_modules/@twilio/flex-dev-utils/dist/fs.js:782:83)
    at new Telemetry (/Users/leonardo/.twilio-cli/node_modules/@twilio/flex-dev-utils/dist/telemetry/lib/telemetry.js:73:16)
    at FlexPluginsStart.run (/Users/leonardo/.twilio-cli/node_modules/@twilio-labs/plugin-flex/dist/sub-commands/flex-plugin.js:312:27)
    at process.processTicksAndRejections (node:internal/process/task_queues:95:5)
    at async FlexPluginsStart._run (/Users/leonardo/.twilio-cli/node_modules/@oclif/core/lib/command.js:80:22)
    at async Config.runCommand (/usr/local/Cellar/twilio/5.21.1/libexec/node_modules/@oclif/core/lib/config/config.js:301:25)
```

## To reproduce

Install with `pnpm`

```
pnpm i
```

Then run command:

```
twilio flex:plugins:start --name team-filters -l debug
```
