![Python](https://img.shields.io/badge/python-3.10+-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-production-ready-green)
![License](https://img.shields.io/badge/license-MIT-brightgreen)
![Deploy](https://img.shields.io/badge/deployed-Render-blue)


# AI Prompt Cost Estimator API

Estimate token usage and approximate USD cost for AI prompts before execution.

## Why this exists
AI costs scale fast, and most developers run prompts without knowing the cost impact.
This API helps you estimate usage and budget **before** making real API calls.

## Features
- Input, output, and total token estimation
- USD cost calculation per model
- Lightweight and fast (FastAPI)
- Production-ready and API-first
- Clear disclaimer to prevent billing confusion

## Supported Models
- gpt-4o
- gpt-4o-mini
- gpt-3.5-turbo

## API Endpoint

### POST /estimate

**Request**
```json
{
  "model": "gpt-4o",
  "prompt": "Write a landing page headline",
  "expected_output_tokens": 200
}


## Response
{
  "input_tokens": 10,
  "output_tokens": 200,
  "total_tokens": 210,
  "estimated_cost_usd": 0.00305,
  "confidence": "±10%",
  "note": "Estimated cost based on tokenizer approximation. Actual AI billing may vary."
}
