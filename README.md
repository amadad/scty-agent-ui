# SCTY Agent UI
## CopilotKit <> Agno Starter

This is a starter template for building AI agents using [Agno](https://agno.com) and [CopilotKit](https://copilotkit.ai). It provides a modern Next.js application with an integrated investment analyst agent that can research stocks, analyze market data, and provide investment insights.

## Prerequisites

- Node.js 18+ 
- Python 3.8+
- OpenAI API Key (for the Agno agent)
- Any of the following package managers:
  - pnpm (recommended)
  - pnpm (required)

## Getting Started

1. Install Node.js dependencies:
```bash
pnpm install
```

2. Install Python dependencies for the Agno agent:
```bash
pnpm install:agent
```

3. Set up your OpenAI API key in a `.env.local` file in the root directory:
```bash
# .env.local
OPENAI_API_KEY=your-api-key-here
```

4. Start the development servers:
```bash
pnpm dev
```
export OPENAI_API_KEY="your-openai-api-key-here"

## Development

### Available Scripts

- `pnpm dev` - Starts both UI and agent servers in development mode
- `pnpm dev:debug` - Starts development servers with debug logging enabled
- `pnpm dev:ui` - Starts only the Next.js UI server
- `pnpm dev:agent` - Starts only the Agno agent server
- `pnpm build` - Builds the Next.js application for production
- `pnpm start` - Starts the production server
- `pnpm lint` - Runs ESLint for code linting
- `pnpm install:agent` - Installs Python dependencies for the agent

## Documentation

The main UI component is in `src/app/page.tsx`. You can:
- Modify the theme colors and styling
- Add new frontend actions
- Customize the CopilotKit sidebar appearance

## 📚 Documentation

- [Agno Documentation](https://docs.agno.com/introduction) - Learn more about Agno and its features
- [CopilotKit Documentation](https://docs.copilotkit.ai) - Explore CopilotKit's capabilities
- [Next.js Documentation](https://nextjs.org/docs) - Learn about Next.js features and API
- [YFinance Documentation](https://pypi.org/project/yfinance/) - Financial data tools

## Contributing

Feel free to submit issues and enhancement requests! This starter is designed to be easily extensible.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Troubleshooting

### Agent Connection Issues
If you see "I'm having trouble connecting to my tools", make sure:
1. The Agno agent is running on port 8000
2. Your OpenAI API key is set in `.env.local`
3. Both servers started successfully

### Python Dependencies
If you encounter Python import errors:
```bash
# In the project root
pnpm install:agent
```

Or manually:
```bash
# In the project root
pip install -r agent/requirements.txt
```