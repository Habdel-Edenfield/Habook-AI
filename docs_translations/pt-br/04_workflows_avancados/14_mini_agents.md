# Workflows Avançados: Mini AI Agents

Mini Agents são versões simplificadas focadas em uma tarefa específica. Por serem leves, podem ser executados em paralelo ou incorporados a aplicações maiores com facilidade.

```python
from praisonaiagents import Agent

agent = Agent(instructions="Answer only with emoji reactions")
agent.start("How are you?")
```

São úteis quando se deseja um comportamento muito pontual sem a complexidade de um workflow completo.
Veja [[../05_ferramentas/00_visao_geral_ferramentas]].

## Exercícios

1. Revise os conceitos apresentados acima.
2. No terminal, navegue até `examples` e execute um dos scripts relacionados.
3. Modifique algum parâmetro e observe os resultados.
