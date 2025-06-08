# Workflows Avançados: Math Agents

Math Agents são especializados em resolver cálculos e problemas matemáticos. Combinam o raciocínio do modelo de linguagem com ferramentas que efetuam operações precisas.

O propósito principal desses agentes é atuar como módulos confiáveis de cálculo. Ao integrar bibliotecas matemáticas e um interpretador de código, eles permitem que o modelo foque no raciocínio e delegue as operações numéricas a ferramentas dedicadas.

```python
from praisonaiagents import Agent
from praisonaiagents.tools import math_tool, code_interpreter

agent = Agent(tools=[math_tool, code_interpreter])
agent.start("Calcule a derivada de x**2 + 3*x em relação a x e avalie para x=2")
```

**Exemplo YAML Conceitual:**
```yaml
framework: praisonai
roles:
  calculista:
    role: "Assistente de Cálculos"
    instructions: "Utilize math_tool e code_interpreter para resolver problemas numéricos."

tasks:
  - name: calcular_estatisticas
    agent: calculista
    description: "Calcule média e desvio padrão de [1,2,3,4,5]."
    expected_output: "Média e desvio padrão"
tools:
  - math_tool
  - code_interpreter
```

Esse padrão ajuda a garantir respostas numéricas corretas e detalhadas. É útil para automação de planilhas, cálculos estatísticos e outras tarefas que exigem precisão.
Veja [[../05_ferramentas/00_visao_geral_ferramentas]].
