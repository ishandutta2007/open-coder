# Open Coder

🤖 An open-source AI-powered coding agent that brings the power of large language models to your terminal. Like Google Gemini CLI, OpenAI Codex, or Claude Code, but fully open-source and customizable.

## ✨ Features

- **🧠 Intelligent Code Generation**: Generate, complete, and refactor code in any programming language
- **🔍 Context-Aware Assistance**: Understands your project structure and coding patterns
- **💬 Interactive Chat**: Natural language interface for coding help and explanations
- **🔧 Multi-Language Support**: Works with Python, JavaScript, TypeScript, Go, Rust, Java, C++, and more
- **📁 Project Integration**: Seamlessly integrates with your existing codebase
- **🎯 Customizable Prompts**: Tailor the AI's behavior to your specific needs
- **🔒 Privacy-First**: Run locally or with your own API keys, no data sent to third parties
- **🚀 Fast Performance**: Optimized for quick responses and minimal latency

## 🚀 Quick Start

### Prerequisites

- Node.js 16+ or Python 3.8+
- Git
- An OpenAI API key or compatible LLM endpoint

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/open-coder.git
cd open-coder

# Install dependencies
npm install  # or: pip install -r requirements.txt

# Set up your API key
export OPENAI_API_KEY="your-api-key-here"
# or create a .env file:
echo "OPENAI_API_KEY=your-api-key-here" > .env
```

### Basic Usage

```bash
# Start the interactive coding agent
npm start  # or: python main.py

# Get help with a specific file
./opencode help src/app.js

# Generate code for a new feature
./opencode generate "Create a REST API endpoint for user authentication"

# Refactor existing code
./opencode refactor "Optimize this function for better performance" src/utils.js

# Explain code
./opencode explain "What does this function do?" src/components/Header.jsx
```

## 📖 Usage Examples

### Code Generation

```bash
# Generate a complete function
opencode> "Create a function that validates email addresses in JavaScript"

# Generate a class
opencode> "Create a Python class for managing a todo list"

# Generate API endpoints
opencode> "Create Express.js routes for CRUD operations on users"
```

### Code Explanation

```bash
# Explain complex code
opencode> "Explain this React hook: const [state, setState] = useState(initialValue)"

# Explain algorithms
opencode> "How does this quicksort implementation work?"
```

### Code Refactoring

```bash
# Improve performance
opencode> "Refactor this for better performance"

# Add error handling
opencode> "Add proper error handling to this function"

# Convert between patterns
opencode> "Convert this callback-based code to async/await"
```

### Debugging Help

```bash
# Debug issues
opencode> "Why is this React component not re-rendering?"

# Fix bugs
opencode> "Fix the memory leak in this JavaScript code"
```

## ⚙️ Configuration

Create a `.opencoderc.json` file in your project root:

```json
{
  "model": "gpt-4",
  "temperature": 0.1,
  "maxTokens": 2000,
  "contextWindow": 8000,
  "includeFiles": ["src/**/*.{js,ts,jsx,tsx}"],
  "excludeFiles": ["node_modules/**", "dist/**"],
  "customPrompts": {
    "review": "Review this code for security vulnerabilities and best practices",
    "test": "Write comprehensive unit tests for this code"
  }
}
```

### Environment Variables

```bash
OPENAI_API_KEY=your-api-key
OPENAI_BASE_URL=https://api.openai.com/v1  # Custom endpoint
MODEL=gpt-4  # Default model
TEMPERATURE=0.1  # Default temperature
```

## 🔧 Advanced Features

### Custom Prompts

Create custom prompt templates in `prompts/`:

```markdown
# prompts/security-review.md
You are a security expert. Review the following code for:
1. SQL injection vulnerabilities
2. XSS vulnerabilities
3. Authentication bypasses
4. Data exposure risks

Code: {code}

Provide specific recommendations for fixing any issues found.
```

### Plugin System

Extend Open Coder with custom plugins:

```javascript
// plugins/custom-plugin.js
module.exports = {
  name: 'custom-plugin',
  description: 'Custom functionality',
  execute: async (input, context) => {
    // Your custom logic here
    return result;
  }
};
```

### Integration with IDEs

#### VS Code

Add to your `settings.json`:

```json
{
  "terminal.integrated.commandsToSkipShell": [
    "opencode"
  ]
}
```

#### Vim/Neovim

```vim
" Add to your .vimrc
command! OpenCoder !opencode <args>
```

## 🏗️ Architecture

```
open-coder/
├── src/
│   ├── core/           # Core engine
│   ├── agents/         # AI agents
│   ├── parsers/        # Code parsers
│   ├── plugins/        # Plugin system
│   └── utils/          # Utilities
├── prompts/            # Custom prompts
├── config/             # Configuration files
├── tests/              # Test suite
└── docs/               # Documentation
```

## 🧪 Development

### Setting up Development Environment

```bash
# Clone the repository
git clone https://github.com/yourusername/open-coder.git
cd open-coder

# Install development dependencies
npm install --dev  # or: pip install -r requirements-dev.txt

# Run tests
npm test  # or: pytest

# Run in development mode
npm run dev  # or: python main.py --dev
```

### Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Code Style

- Use ESLint/Prettier for JavaScript
- Follow PEP 8 for Python
- Write comprehensive tests
- Document new features

## 📊 Comparison

| Feature | Open Coder | Gemini CLI | Claude Code | OpenAI Codex |
|---------|------------|------------|-------------|--------------|
| Open Source | ✅ | ❌ | ❌ | ❌ |
| Custom Models | ✅ | ❌ | ❌ | ❌ |
| Local Deployment | ✅ | ❌ | ❌ | ❌ |
| Plugin System | ✅ | ❌ | ❌ | ❌ |
| Privacy | ✅ | ❌ | ❌ | ❌ |
| Free | ✅ | ❌ | ❌ | ❌ |

## 🤝 Community

- **Discord**: [Join our Discord server](https://discord.gg/opencoder)
- **GitHub Discussions**: [Ask questions and share ideas](https://github.com/yourusername/open-coder/discussions)
- **Twitter**: Follow us [@opencoder_ai](https://twitter.com/opencoder_ai)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- OpenAI for the powerful language models
- The open-source community for inspiration and feedback
- All contributors who help make this project better

## 🗺️ Roadmap

- [ ] Support for more LLM providers (Anthropic, Cohere, local models)
- [ ] GUI interface for non-terminal users
- [ ] Advanced code analysis and visualization
- [ ] Team collaboration features
- [ ] Integration with more development tools
- [ ] Mobile app companion

## 📞 Support

If you encounter any issues or have questions:

1. Check the [FAQ](docs/FAQ.md)
2. Search [existing issues](https://github.com/yourusername/open-coder/issues)
3. Create a [new issue](https://github.com/yourusername/open-coder/issues/new)
4. Join our [Discord community](https://discord.gg/opencoder)

---

**Made with ❤️ by the open-source community**