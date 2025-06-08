# Workflows Avançados: Callback Agents

Callback Agents permitem executar funções específicas em pontos determinados da conversa, como antes ou depois do uso de uma ferramenta. Isso facilita monitoramento e extensões personalizadas.

```python
from praisonaiagents import Agent

def log_step(data):
    print("Agent step:", data)

agent = Agent(callbacks=[log_step])
agent.start("Tell me a joke")
```

Use callbacks para registro, métricas ou integrações extras.
Veja [[../05_ferramentas/00_visao_geral_ferramentas]].

## Exercícios

1. Revise os conceitos apresentados acima.
2. No terminal, navegue até `examples` e execute um dos scripts relacionados.
3. Modifique algum parâmetro e observe os resultados.
