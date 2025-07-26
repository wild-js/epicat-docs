# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Mintlify documentation site for Epicat, built using the Mintlify documentation framework. The project contains structured documentation pages in MDX format, API reference documentation, and configuration for a modern documentation website.

## Development Commands

### Local Development
```bash
# Install Mintlify CLI globally (if not already installed)
npm i -g mint

# Start local development server
mint dev

# Update Mintlify CLI to latest version
mint update
```

The development server must be run from the root directory where `docs.json` is located.

## Project Architecture

### Documentation Structure
- **Root pages**: `index.mdx`, `quickstart.mdx`, `changelog.mdx`, `faq.mdx`, `development.mdx`
- **Projects**: Comprehensive guides for agents, orchestration, integrations, deployment, and scaling
- **Security**: Overview and secrets management documentation
- **MCP Servers**: Model Context Protocol server documentation (stdio, http)
- **API Reference**: OpenAPI-based endpoint documentation with examples
- **Models**: Documentation for various AI model integrations (Anthropic, OpenAI, Gemini, OpenRouter)
- **Integrations**: Built-in integrations and Slack documentation
- **Authentication**: Setup guides for authentication and personalization

### Configuration Files
- `docs.json`: Main Mintlify configuration defining navigation, theme, colors, and structure
- `style.css`: Custom styling overrides
- `openapi.json`: API specification for generating reference documentation

### Navigation Architecture
The site uses a dropdown-based navigation structure with three main sections:
1. **Documentation**: Core product documentation and guides
2. **API Reference**: Technical API documentation and examples  
3. **Changelog**: Version history and updates

### Content Organization
- MDX files support React components and enhanced markdown features
- Images stored in `/images/` with organized subdirectories for icons
- Reusable snippets in `/snippets/` for content modularity
- Logo assets available in both light and dark variants

## Key Technical Details

### Theme Configuration
- Uses "maple" theme with primary color `#00a6f4`
- Light mode default with strict appearance enforcement
- Lucide icon library integration
- Custom favicon and branding

### Troubleshooting Development Issues
- If dev environment fails: Run `mint update` to get latest CLI version
- If pages load as 404: Ensure running from directory containing `docs.json`
- Development server requires global Mintlify CLI installation

### Publishing
Changes are automatically deployed when pushed to the default branch via GitHub App integration.