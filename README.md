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
  baseURL: 'https://api.gptplatform.com'
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

- **[API Reference](/docs/client)** - Interactive API docs with Try It
- **[Quick Start Guide](/quickstart)** - Getting started guide

## Tooling

Download API collections for your preferred client:

| Tool | Download |
|------|----------|
| [Postman](https://www.postman.com) | [Download Collection](/collections/postman/gpt-core-client.postman_collection.json) |
| [Bruno](https://www.usebruno.com) | [Browse Folder](/collections/bruno/client/) - Clone the Bruno folder |
| [Insomnia](https://insomnia.rest) | [Download Collection](/collections/insomnia/gpt-core-client.insomnia.json) |

## Packages

| Package | Version | Description |
|---------|---------|-------------|
| [@gpt-core/client](https://www.npmjs.com/package/@gpt-core/client) | [![npm version](https://badge.fury.io/js/%40gpt-core%2Fclient.svg)](https://www.npmjs.com/package/@gpt-core/client) | Client SDK for end users |

## Links

- **[Platform Dashboard](https://dashboard.gptplatform.com)** - Web interface
- **[API Status](https://status.gptplatform.com)** - Uptime monitoring
- **[Support](mailto:support@gptplatform.com)** - Get help

## Features

- **Document Extraction** - Extract structured data from PDFs, images, and Office documents
- **AI Agents** - Build and deploy AI-powered extraction agents
- **Workspaces** - Multi-tenant workspace management
- **Streaming** - Real-time SSE streaming for long-running operations
- **TypeScript** - Full type definitions included
- **Pagination** - Built-in helpers for paginated responses

## License

Proprietary - All rights reserved. &copy; 2025 GPT Integrators.

## Support

For support, email [support@gptplatform.com](mailto:support@gptplatform.com) or contact us through the platform dashboard.
