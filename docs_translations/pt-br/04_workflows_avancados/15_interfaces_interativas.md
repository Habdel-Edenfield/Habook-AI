# Workflows Avançados: Interfaces Interativas

O PraisonAI possui diferentes interfaces gráficas para facilitar a interação com um ou mais agentes.
As opções incluem uma interface geral de UI para fluxos multiagentes, a Chat Interface para conversas simples
por texto e a Code Interface para trabalhar com bases de código. Esses modos são úteis para demonstrar e
testar seus agentes de forma visual.

## Instalação rápida

```bash
# Instale os componentes desejados
pip install "praisonai[ui]" "praisonai[chat]" "praisonai[code]"
# ou utilize o script de setup
./src/praisonai/setup.sh --all --run
```

É necessário definir `OPENAI_API_KEY` no ambiente antes de iniciar qualquer interface.

## Execução

```bash
# Interface completa para múltiplos agentes
praisonai ui

# Chat Interface (Chainlit)
praisonai --chat

# Code Interface
praisonai --code
```

## Vídeos relacionados

- [User Interface](https://www.youtube.com/watch?v=tg-ZjNl3OCg)
- [Chat Interface](https://www.youtube.com/watch?v=sw3uDqn2h1Y)
- [Code Interface](https://www.youtube.com/watch?v=_5jQayO-MQY)
