# FLOWS with Content Research Crew

Welcome to the Content Research Crew project, powered by [crewAI](https://crewai.com). This project implements a multi-agent AI system that creates comprehensive research guides on any topic. The system leverages crewAI's powerful framework to coordinate multiple AI agents that collaborate on researching, writing, and reviewing content.

## System Architecture

![Flow Diagram](flow_diagram.svg)

The system operates through the following key components:

1. **Guide Creator Flow**: Manages the overall content creation process
2. **Content Research Crew**: Specialized agents working together to:
   - Research and gather information
   - Write comprehensive content
   - Review and improve quality
3. **Output Generation**: Produces structured markdown guides with:
   - Detailed sections
   - Examples and practical applications
   - Citations and references

## Installation

Ensure you have Python >=3.10 <3.13 installed. This project uses [UV](https://docs.astral.sh/uv/) for dependency management.

1. Install UV:
```bash
pip install uv
```

2. Clone and setup the project:
```bash
git clone <repository-url>
cd content-research-crew
crewai install
```

3. Configure your environment:
- Copy `.env.example` to `.env`
- Add your `OPENAI_API_KEY` to `.env`

## Configuration

Customize the system by modifying:

- `src/researcher_content/config/agents.yaml`: Define agent roles and capabilities
- `src/researcher_content/config/tasks.yaml`: Configure research and writing tasks
- `src/researcher_content/crew.py`: Implement custom logic and tools
- `src/researcher_content/main.py`: Adjust input handling and flow control

## Usage

1. Run the content creation flow:
```bash
crewai run
```

2. View the generated content:
- Guide outline: `output/guide_outline.json`
- Complete guide: `output/complete_guide.md`

3. Visualize the flow:
```bash
crewai plot
```
This generates an interactive flow visualization at `guide_creator_flow.html`

## Example Output

The system generates comprehensive guides with:
- Detailed introduction and context
- Multiple content sections with examples
- Practical applications and exercises
- Professional formatting in Markdown

## Development

To extend or modify the system:

1. Add new agent types in `config/agents.yaml`
2. Create custom tasks in `config/tasks.yaml`
3. Implement new tools in `src/researcher_content/tools/`
4. Modify the flow logic in `main.py`

## Support

For assistance:
- [Documentation](https://docs.crewai.com)
- [GitHub Issues](https://github.com/joaomdmoura/crewai/issues)
- [Discord Community](https://discord.com/invite/X4JWnZnxPb)
- [Documentation Chat](https://chatg.pt/DWjSBZn)

## License

[MIT License](LICENSE)
