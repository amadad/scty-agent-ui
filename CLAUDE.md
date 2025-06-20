# Claude Code Instructions for AG-UI Playground

## Project Context
AG-UI is a CopilotKit + Agno playground for exploring AI agent possibilities. This starter template demonstrates the powerful integration between Next.js frontend and Python-based Agno agents. The current implementation showcases an investment analyst agent with YFinance tools, but serves as a foundation for building any type of AI agent - from research assistants to creative tools to specialized domain experts.

## Development Philosophy
- **Agent-first architecture**: Build around AI agent capabilities with seamless frontend integration
- **Concurrent development**: UI and agent servers run simultaneously for real-time testing
- **Tool-driven capabilities**: Extensible tool system for any domain (finance, research, creative, etc.)
- **Playground mentality**: Experiment with different agent types and capabilities
- **Responsive by default**: Modern Next.js frontend with Tailwind CSS for optimal user experience

## Key Architecture Components
- **Next.js App Router**: File-based routing with app directory structure
- **CopilotKit Integration**: React components and runtime for AI agent communication
- **Agno Agent Framework**: Python-based agents with extensible tool system
- **Example Implementation**: Investment analyst with YFinance tools (easily replaceable/extendable)
- **Styling**: Tailwind CSS with modern UI components
- **Concurrent Servers**: UI (port 3000) and agent (port 8000) development environment

## Important Files & Structure
```
src/
├── app/
│   ├── api/
│   │   └── copilotkit/      # CopilotKit API integration
│   │       └── route.ts     # API route for agent communication
│   ├── globals.css          # Global Tailwind styles
│   ├── layout.tsx           # Root layout with CopilotKit providers
│   └── page.tsx             # Main UI with chat interface
├── components/
│   └── tool.tsx             # Custom tool components
agent/
├── agent.py                 # Main Agno agent with YFinance tools
└── requirements.txt         # Python dependencies
package.json                 # Node.js dependencies and scripts
.env.local                   # OpenAI API key configuration
```

## Code Standards & Patterns
- **Prefer editing existing files** over creating new ones
- **Follow CopilotKit patterns** for agent integration and UI components
- **Use TypeScript** for all frontend components with proper prop typing
- **Agent tool patterns**: Follow Agno framework conventions for tool development
- **No comments** unless explicitly requested by user
- **Consistent styling** using Tailwind CSS utility classes

## Development Guidelines
- **Agent integration**: Use CopilotKit hooks and components for agent communication
- **Tool development**: Follow Agno patterns for creating new financial analysis tools
- **Environment setup**: Ensure both frontend and agent servers are running concurrently
- **Responsive design**: Test components at sm, md, lg, xl breakpoints
- **Error handling**: Implement proper error boundaries for agent connection issues

## Development Workflow
1. **Start concurrent servers** using `pnpm dev` for both UI and agent
2. **Develop agent tools** in `agent/agent.py` following Agno patterns
3. **Create frontend components** in `src/components/` using CopilotKit integration
4. **Test agent communication** through the CopilotKit chat interface
5. **Verify functionality** with real financial data and analysis

## Current Technical Context
- **Agent Framework**: Agno with OpenAI GPT-4o model integration
- **Financial Tools**: YFinance for stock prices, analyst recommendations, and fundamentals
- **UI Framework**: Next.js 15 with React 19 and TypeScript
- **Styling System**: Tailwind CSS with modern component patterns
- **Development Environment**: Concurrent servers with hot reload for both UI and agent

## Key Patterns Established
- **CopilotKit integration** handles agent communication and UI state
- **Agno agent pattern** with tools, model, and instructions configuration
- **Tool composition** using YFinance for comprehensive financial analysis
- **Concurrent development** pattern for seamless UI and agent testing

## Common Commands
```bash
# Run both UI and agent servers concurrently
pnpm dev

# Run with debug logging
pnpm dev:debug

# Install Python agent dependencies
pnpm install:agent

# Run only the UI server
pnpm dev:ui

# Run only the agent server
pnpm dev:agent

# Build for production
pnpm build

# Lint codebase
pnpm lint
```

## Current Focus
**AG-UI exploration and agent extensibility** - demonstrating the full potential of Agno<>CopilotKit integration. The finance agent serves as one example implementation, with focus on creating patterns and tools that enable rapid development of diverse agent types - from specialized domain experts to creative assistants to research tools.

## Agent & Component Development
When creating new agent tools:
- Follow Agno framework patterns for tool definition
- Use descriptive names that reflect the tool's capabilities and domain
- Include proper error handling for API calls and data processing
- Test tools with real data before integration
- Consider reusability across different agent implementations

When creating UI components:
- Use CopilotKit hooks for agent state management
- Accept className prop for customization while maintaining base styles
- Include responsive design considerations from the start
- Design components to be domain-agnostic when possible
- Follow established patterns for data visualization and interaction

## Agent Extensibility Patterns
**Tool Categories to Explore:**
- **Data Analysis**: APIs, databases, file processing, research tools
- **Creative Tools**: Image generation, content creation, design assistance  
- **Domain Experts**: Legal, medical, educational, technical specialists
- **Productivity**: Task management, scheduling, communication tools
- **Research**: Web scraping, academic databases, fact-checking
- **Development**: Code analysis, debugging, deployment assistance

**Agent Architecture Patterns:**
- **Single-domain specialists**: Deep expertise in one area (like the finance example)
- **Multi-tool generalists**: Broad capabilities across domains
- **Workflow orchestrators**: Agents that coordinate other agents/tools
- **Interactive assistants**: Conversational agents with real-time capabilities