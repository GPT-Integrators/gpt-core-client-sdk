# Quick Start Guide

Get up and running with the GPT Core Client SDK in minutes.

## Installation

```bash
npm install @gpt-core/client
```

## Configuration

Create a client instance with your API key:

```typescript
import { GPTCore } from '@gpt-core/client';

const client = new GPTCore({
  apiKey: process.env.GPT_API_KEY,
  baseURL: 'https://api.gptplatform.com'
});
```

### API Key

Get your API key from the [Platform Dashboard](https://dashboard.gptplatform.com).

### Environment Variables

```bash
# .env
GPT_API_KEY=sk_live_your_key_here
GPT_BASE_URL=https://api.gptplatform.com
```

## Basic Usage

### Document Extraction

```typescript
// Upload and extract a document
const result = await client.extraction.documents.create({
  workspaceId: 'ws_123',
  fileId: 'file_456',
  agentId: 'agent_789'
});

console.log(result.data);
// { id: 'ext_123', status: 'completed', data: {...} }
```

### Streaming Results

```typescript
// Stream extraction results in real-time
const stream = await client.extraction.documents.stream({
  documentId: 'ext_123'
});

for await (const chunk of stream) {
  console.log(chunk);
}
```

### List Workspaces

```typescript
// List all workspaces with pagination
const workspaces = await client.platform.workspaces.list({
  page: { number: 1, size: 20 }
});

console.log(workspaces.data);
```

## Error Handling

```typescript
import { GPTCore, ApiError } from '@gpt-core/client';

try {
  const result = await client.extraction.documents.create({...});
} catch (error) {
  if (error instanceof ApiError) {
    console.error('API Error:', error.status, error.message);
    if (error.status === 401) {
      console.error('Invalid API key');
    } else if (error.status === 429) {
      console.error('Rate limit exceeded');
    }
  }
}
```

## Next Steps

- [Full API Documentation](/docs/client)
- [API Collections](/collections) for Postman/Bruno/Insomnia

## Need Help?

- Email: [support@gptplatform.com](mailto:support@gptplatform.com)
- [API Status](https://status.gptplatform.com)
