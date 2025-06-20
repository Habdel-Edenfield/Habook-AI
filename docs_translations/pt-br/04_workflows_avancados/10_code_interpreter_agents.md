# Workflows Avançados: Code Interpreter Agents

Esses agentes utilizam a ferramenta `code_interpreter` para executar trechos de código e retornar o resultado. É útil para análises de dados, geração de gráficos ou qualquer tarefa que exija execução dinâmica de scripts.

```python
from praisonaiagents import Agent
from praisonaiagents.tools import code_interpreter

agent = Agent(tools=[code_interpreter])
agent.start("Calculate the factorial of 5")
```

A saída do código é repassada para o agente, permitindo ciclos de raciocínio baseados em resultados programáticos.
Veja [[../05_ferramentas/00_visao_geral_ferramentas]].

## Exercícios

1. Revise os conceitos apresentados acima.
2. No terminal, navegue até `examples` e execute um dos scripts relacionados.
3. Modifique algum parâmetro e observe os resultados.
