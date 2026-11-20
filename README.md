# ProSimulo AI Data — Cursor Plugin

Connect Cursor's MCP client to **ProSimulo AI Data**, an independent service for organizing, retrieving, and maintaining user-authorized information across supported AI providers.

## What this plugin does

This plugin supplies a connection to ProSimulo's existing remote MCP service. Through the tools available to an authorized account, users can work with Items, Records, attachments, reminders, and shared information. The ProSimulo service is separate from Cursor; installing this plugin does not import conversations automatically.

## Install and authorize

1. Install **ProSimulo AI Data** in Cursor from its marketplace listing (once approved), or use Cursor's supported local plugin testing flow.
2. Open Cursor's MCP/plugin connection settings and authorize ProSimulo when prompted.
3. Sign in to the intended ProSimulo account and complete the OAuth consent flow.
4. In a new session, ask Cursor to list your ProSimulo Items; confirm that the results belong to the intended account.
5. Before any save, inspect the proposed changes and explicitly Confirm, Edit, or Cancel as appropriate. Do not assume a draft was saved.

If Cursor cannot discover the MCP tools, verify the connection state and reopen the session after reauthentication. ProSimulo may advise reauthentication if the host retains older tool definitions.

## Remote MCP connection

- MCP endpoint: `https://dev.prosimulo.ai/api/mcp`
- Transport: remote HTTPS MCP (configured in `mcp.json`)
- Authentication: ProSimulo account OAuth, handled by the client and service
- No API keys, tokens, backend code, or account data are embedded in this package

The endpoint is controlled by ProSimulo. Its tool definitions and server behavior are maintained independently of this plugin repository.

## Privacy and service

Privacy policy: https://prosimulo.ai/privacy

The integration is free. ProSimulo also provides a limited free hosted tier and optional paid subscriptions for expanded hosted services. Availability and entitlement of features are determined by the user's ProSimulo account.

## Support

Publisher: PROSIMULO LLC  
Website: https://prosimulo.ai  
Publisher contact: admin@prosimulo.com  
Support: support@prosimulo.com

## License and scope

The MIT license in this repository applies **only** to the small, publicly distributed Cursor plugin configuration and documentation here. It does not license, publish, or transfer ownership of ProSimulo's hosted Neutral MCP implementation, application backend, website, databases, service software, user data, or trademarks. Those remain separately controlled by PROSIMULO LLC.

## Local validation

- Validate `.cursor-plugin/plugin.json` and `mcp.json` as JSON.
- Use Cursor's local plugin install process and verify it discovers the remote ProSimulo MCP server.
- Complete a real OAuth connection with an authorized disposable test account.
- Check one read-only Item listing. Record the actual result before claiming live acceptance.

Cursor marketplace approval and publication are separate from local validation.
