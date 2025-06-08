# Guia de Instalação Local (macOS)

Este guia descreve como preparar o PraisonAI em sistemas macOS recentes.

## Pré‑requisitos

1. **Python 3.11+**
   - O macOS Ventura ou superior já traz Python 3 instalado via Xcode Command Line Tools. Verifique com:
     ```bash
     python3 --version
     ```
   - Se necessário, instale versões atualizadas com [Homebrew](https://brew.sh/):
     ```bash
     brew install python@3.11
     ```
2. **Homebrew** para instalar dependências facilmente.
3. **Git** (opcional, para clonar o repositório).

## Configurando Variáveis de Ambiente

Abra o Terminal e exporte sua `OPENAI_API_KEY` ou, para modelos locais, configure `OPENAI_BASE_URL` e `OPENAI_MODEL_NAME`. Acrescente as linhas ao `~/.zshrc`:
```bash
export OPENAI_API_KEY=sua_chave
# ou para Ollama/LM Studio
export OPENAI_BASE_URL=http://localhost:11434/v1
export OPENAI_MODEL_NAME=llama3:latest
```
Reabra o Terminal ou execute `source ~/.zshrc` para aplicar.

## Instalando o PraisonAI com `pipx`

`pipx` permite instalar a CLI de forma isolada:
```bash
python3 -m pip install --user pipx
pipx install praisonai
```
Caso encontre erros de permissão, garanta que a pasta `~/Library/Python/3.x/bin` esteja no `PATH`.

### Teste Rápido

Execute:
```bash
praisonai --auto "Gere um resumo sobre PraisonAI"
```
Se tudo correr bem, a resposta aparecerá no terminal. Para desenvolvimento, você também pode clonar o repositório e instalar em modo editável com `pip` ou `uv`.

