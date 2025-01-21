# Friend Grok - Your Fun AI Explainer

An Alexa skill that lets you chat with Grok, an AI friend who makes complex topics simple and fun using a friendly American male voice.

## Features

- Simple, engaging explanations of complex topics
- Friendly American male voice (Justin)
- Uses latest Grok model (auto-detected)
- Casual, approachable conversation style
- Comprehensive error handling
- Credit usage monitoring

## Usage

Just say:
- "Alexa, ask friend grok to explain blockchain"
- "Alexa, ask friend grok what's quantum computing"
- "Alexa, ask friend grok about machine learning"

## Skill Structure

This repository follows the Alexa-hosted skills package format:

```
.
├── lambda/
│   ├── lambda_function.py
│   └── requirements.txt
│
└── skill-package/
    ├── interactionModels/
    │   └── custom/
    │       └── en-US.json
    └── skill.json
```

## Setup Instructions

1. Create a new Alexa-hosted skill:
   - Go to [Alexa Developer Console](https://developer.amazon.com/alexa/console/ask)
   - Click "Create Skill"
   - Name: "Friend Grok"
   - Choose "Custom" model
   - Choose "Alexa-Hosted (Python)"
   - Click "Import skill"
   - Enter this repository's .git URL

2. Set Environment Variable:
   - Key: `OPENROUTER_API_KEY`
   - Value: Your OpenRouter API key

## Development

This skill is designed to be hosted on Alexa-hosted skills, which provides:
- Free SSL certificate
- AWS Lambda function
- CloudWatch logs
- Auto-scaling

### Local Testing

1. Clone this repository
2. Install dependencies:
   ```bash
   cd lambda
   pip install -r requirements.txt
   ```
3. Set environment variables:
   ```bash
   export OPENROUTER_API_KEY=your_key_here
   ```
4. Run tests:
   ```bash
   python -m unittest test_lambda_function.py
   ```

## Special Features

- **Dynamic Model Selection**: Automatically detects and uses the latest available Grok model
- **Casual Style**: Makes complex topics approachable and fun
- **Memory Management**: Efficient caching of model information
- **Error Recovery**: Graceful fallback to stable model versions

## Error Handling

The skill provides clear feedback for different scenarios:

1. API Key Issues:
   - "Oops, looks like I need a quick setup. Ask the skill administrator to help me out!"

2. Credit-Related Errors:
   - "I need a quick recharge! Check back with me later?"

3. General Errors:
   - "My brain's a bit fuzzy right now. Mind trying that question again?"

## Part of the AI Friends Series

This skill is part of a series of AI friend skills:
- [Friend DeepSeek](https://github.com/Rmohid/alexa-friend-deepseek) - Educational explanations
- Friend Grok (this skill) - Simple, fun explanations
- [Friend GPT](https://github.com/Rmohid/alexa-friend-gpt) - Sophisticated insights

## License

MIT License