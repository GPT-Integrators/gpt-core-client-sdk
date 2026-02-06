# GPT Core Client SDK

The official TypeScript SDK for GPT Core Platform - document extraction, AI agents, and workspace management.

## Quick Start

```bash
npm install @gpt-core/client
```

```typescript
import { GPTCore } from '@gpt-core/client';

const client = new GPTCore({
  apiKey: process.env.GPT_API_KEY,
  baseURL: 'https://api.gptintegrators.com'
});

// Extract documents
const result = await client.extraction.documents.create({
  workspaceId: 'ws_123',
  fileId: 'file_456',
  agentId: 'agent_789'
});

console.log(result.data);
```

## Documentation

- **[API Reference](https://gpt-integrators.github.io/gpt-core-client-sdk/docs/client)** - Interactive API docs with Try It
- **[Quick Start Guide](https://gpt-integrators.github.io/gpt-core-client-sdk/quickstart)** - Getting started guide

## Tooling

Download API collections for your preferred client:

| Tool | Download |
|------|----------|
| [Postman](https://www.postman.com) | [Download Collection](https://gpt-integrators.github.io/gpt-core-client-sdk/collections/postman/gpt-core-client.postman_collection.json) |
| [Bruno](https://www.usebruno.com) | [Browse on GitHub](https://github.com/GPT-Integrators/gpt-core-client-sdk/tree/main/collections/bruno/client) |
| [Insomnia](https://insomnia.rest) | [Download Collection](https://gpt-integrators.github.io/gpt-core-client-sdk/collections/insomnia/gpt-core-client.insomnia.json) |

## Packages

| Package | Version | Description |
|---------|---------|-------------|
| [@gpt-core/client](https://www.npmjs.com/package/@gpt-core/client) | [![npm version](https://badge.fury.io/js/%40gpt-core%2Fclient.svg)](https://www.npmjs.com/package/@gpt-core/client) | Client SDK for end users |

## Links

- **[Platform Dashboard](https://dashboard.gptintegrators.com)** - Web interface
- **[API Status](https://status.gptintegrators.com)** - Uptime monitoring
- **[Support](mailto:support@gptintegrators.com)** - Get help

## Features

- **Document Extraction** - Extract structured data from PDFs, images, and Office documents
- **AI Agents** - Build and deploy AI-powered extraction agents
- **Workspaces** - Multi-tenant workspace management
- **Streaming** - Real-time SSE streaming for long-running operations
- **TypeScript** - Full type definitions included
- **Pagination** - Built-in helpers for paginated responses

## License

Proprietary - All rights reserved. &copy; 2026 GPT Integrators.

## Support

For support, email [support@gptintegrators.com](mailto:support@gptintegrators.com) or contact us through the platform dashboard.
