<!-- markdownlint-disable -->
<div align="center">
    <br />
    <h3>@kostya-main/discord-rpc</h3>
    <br />
    <p>
        <a href="https://www.npmjs.com/package/@kostya-main/discord-rpc" target="_blank"><img src="https://img.shields.io/npm/v/@kostya-main/discord-rpc.svg" alt="npm version"/></a>
        <a href="https://discord.com/invite/xTAR8nUs2g" target="_blank"><img src="https://img.shields.io/discord/965168309731487805.svg" alt="discord"/></a>
        <a href="https://github.com/xhayper/discord-rpc/blob/main/LICENSE" target="_blank"><img src="https://img.shields.io/github/license/xhayper/discord-rpc.svg" alt="license"/></a>
    </p>
</div>
<!-- markdownlint-enable -->

## About

`@kostya-main/discord-rpc` is a fork of [discordjs/RPC](https://github.com/discordjs/RPC) with type safety and some additional features. The difference from xhayper/discord-rpc is that [ws](https://www.npmjs.com/package/ws) does not use the native modules utf-8-validate and bufferutil.

## Example

```ts
import { Client } from "@kostya-main/discord-rpc";

const client = new Client({
    clientId: "123456789012345678"
});

client.on("ready", () => {
    client.user?.setActivity({
        state: "Hello, world!"
    });
});

client.login();
```

## Compatibility

| OS      | Normal | snap | flatpak |
| ------- | ------ | ---- | ------- |
| Windows | Y      | -    | -       |
| macOS   | Y      | -    | -       |
| Linux   | Y      | Y    | Y       |

-   Linux is tested on Kubuntu 22.04

## Credits

-   [discordjs](https://github.com/discordjs): Making [discordjs/RPC](https://github.com/discordjs/RPC)
-   [JakeMakesStuff](https://github.com/JakeMakesStuff): [snap support](https://github.com/discordjs/RPC/pull/152)
-   [Snazzah](https://github.com/Snazzah): [snap + flatpak support](https://github.com/Snazzah/SublimeDiscordRP/blob/c13e60cdbc5de8147881bb232f2339722c2b46b4/discord_ipc/__init__.py#L208)
-   [leonardssh](https://github.com/leonardssh): Making [coc-discord-rpc](https://github.com/leonardssh/coc-discord-rpc) which inspried me to make this package due to how old [discordjs/RPC](https://github.com/discordjs/RPC) is
