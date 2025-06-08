# Workflows Avançados: Structured Output

Em muitas aplicações, é importante que as respostas sigam um formato fixo, como JSON ou tabelas. Os agentes podem ser configurados com instruções claras para sempre retornarem dados estruturados.

```python
from praisonaiagents import Agent

agent = Agent(instructions="Answer using a JSON object with keys 'summary' and 'sources'.")
agent.start("Summarise the benefits of solar energy")
```

Definir um esquema de saída torna o pós-processamento muito mais simples.
Veja [[../05_ferramentas/00_visao_geral_ferramentas]].

## Exercícios

1. Revise os conceitos apresentados acima.
2. No terminal, navegue até `examples` e execute um dos scripts relacionados.
3. Modifique algum parâmetro e observe os resultados.
