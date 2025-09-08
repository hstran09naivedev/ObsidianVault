```
{
  "LOG": true,
  "API_TIMEOUT_MS": 600000,
  "Providers": [
    {
      "name": "azure-openai",
      "api_base_url": "https://mgm-datascience-openai-sweden.openai.azure.com/openai/deployments/gpt-4o/chat/completions?api-version=2025-01-01-preview",
      "api_key": "GIxeVlJLLArBOKNBARRLqKpDmGPBrbUhjY0SXUAEsBBTEHDT7zaqJQQJ99BGACfhMk5XJ3w3AAABACOGi2cm",
      "models": ["gpt-4", "gpt-4o"]
    }
  ],
  "Router": {
    "default": "azure-openai,gpt-4"
  }
}

```

