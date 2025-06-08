# AGENTS Documentation

This file provides an overview of the project structure and testing workflow for **PraisonAI** (fork maintained by Habdel‑Edenfield). The goal is to give quick orientation when working with the repository.

## Repository Layout

- `src/`
  - `praisonai/` – Python package with the CLI (`praisonai`) and sample YAML configs.
  - `praisonai-agents/` – Core library implementing `Agent`, `Task`, memory and tools.
  - `praisonai-ts/` – TypeScript implementation with matching modules (`agent`, `llm`, `knowledge`, etc.).
- `docs_translations/pt-br/` – Course material in Portuguese. Follow the folder numbers to progress through the lessons.
- `examples/` – Sample agents and workflow scripts used throughout the docs.
- `docker/` – Container examples for development and deployment.
- `Discord.md` – Quick summary of the project for sharing on the OpenTibiaBR server.

## Docs Structure

The PT‑BR documentation is split into numbered modules:

1. **Introdução** – Visão geral e metodologia de aprendizado.
2. **Instalação** – Passos para instalar e configurar variáveis de ambiente.
3. **Conceitos Fundamentais** – Agentes, tarefas, ferramentas, processos, memória e RAG.
4. **Usando o PraisonAI** – Guias Python/YAML/JS e criação do primeiro agente.
5. **Workflows Avançados** – Colaboração, roteamento, agentes autônomos, multimodais, etc.
6. **Ferramentas** – Como utilizar e criar ferramentas.
7. **Modelos LLM** – Configuração de diferentes provedores.
8. **Exemplos Práticos** – Casos de uso completos.
9. **Contribuindo e Desenvolvimento** – Estrutura do código e contribuição.

The file `plan.md` lists completed lessons and topics to expand.

## Testing

A full testing suite lives under `src/praisonai/tests/`. Key references:

- `README.md` – Detailed explanation of test categories and runner usage.
- `TESTING_GUIDE.md` – Overview of unit, integration, and end‑to‑end tests.

### Quick commands

```bash
# Fast diagnostics (no pytest import required)
python tests/simple_test_runner.py --fast

# Run core unit tests
python tests/test_runner.py --unit

# Run integration tests (mocked)
python tests/test_runner.py --integration
```

Real end‑to‑end tests require API keys. Review `TESTING_GUIDE.md` for environment variables and cost warnings.

## Development Tips

- Example YAML configurations are found in `src/praisonai` (`agents.yaml`, `agents-advanced.yaml`).
- The CLI entry point is `src/praisonai/praisonai/cli.py`.
- Additional tools and integrations (UI, realtime voice, call interface) are under `src/praisonai/praisonai/api` and `ui` folders.
- TypeScript sources mirror the Python layout (`src/praisonai-ts/src`).
- Review `docs_translations/pt-br/08_contribuindo_e_desenvolvimento/01_estrutura_do_codigo.md` for a guide to the directory structure.

## Adding Documentation


New Portuguese lessons should be placed in the appropriate numbered folder under `docs_translations/pt-br`. Update `docs_translations/pt-br/README.md` to keep the index current. When expanding existing material, incorpore detalhes e tecnologias recentes (2024/2025) para ampliar o entendimento do usuário, conforme o plano em `docs_translations/pt-br/plan.md`.

Use wiki‑style crosslinks (`[[path/to/file.md]]`) whenever you reference another
lesson so navigation stays consistent in Obsidian. Installation guides for
Windows, Linux and macOS must remain sincronizadas e conter as mesmas
recomendações sobre Python 3.11+, `pipx` e modelos locais.



## Link Style
Use Obsidian-style wiki links (`[[path/to/page]]`) when referenciando outras lições para navegação consistente.
## Open Improvements

The documentation mentions interfaces (chat/code/voice/call) and integration with external tools (Mem0, Crawl4AI). Check `docs_translations/pt-br/plan.md` for pending sections. Missing pages can be created following the existing structure.


## Maintaining this File
- Keep sections concise and reference documentation paths.
- Update the repository layout or testing commands if they change.
- Add notes for new interfaces or tools as they are implemented.

