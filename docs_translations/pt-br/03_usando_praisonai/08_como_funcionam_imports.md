# Como Funcionam os Imports e Dependências

Entender o mecanismo de importação do Python é essencial para organizar projetos complexos. Nesta lição veremos como o PraisonAI estrutura seus módulos, como importar somente o necessário e dicas para lidar com dependências opcionais.

## Importação Básica

```python
import praisonaiagents
```

Esse formato carrega o pacote inteiro. É útil ao explorar os submódulos ou quando você precisa acessar várias classes de forma repetida.

## Importando Apenas o Necessário

Para otimizar a inicialização e evitar dependências desnecessárias, importe apenas o que será usado:

```python
# Import only what we need for testing
from praisonaiagents.guardrails import GuardrailResult, LLMGuardrail
```

Esse exemplo carrega somente duas classes relacionadas aos *guardrails*. Ideal para scripts de teste rápidos ou módulos que não exigem o restante da biblioteca.

## Dependências Extras

Alguns recursos do PraisonAI são opcionais e requerem instalação de extras:

```bash
pip install "praisonaiagents[llm,memory]"
```

Consulte [[../08_contribuindo_e_desenvolvimento/00_contribuindo_e_dev_local.md]] para detalhes sobre os extras disponíveis.

## Aplicação Prática

A combinação de imports seletivos e extras permite criar scripts enxutos e com dependências sob medida. Veja a lição [[07_importes_e_funcoes_essenciais.md]] para o panorama geral das importações mais usadas.

## Exercícios

1. Importe `GuardrailResult` e `LLMGuardrail` e execute `simple_guardrail_test.py` para ver os resultados.
2. Instale o pacote com diferentes extras e observe quais módulos adicionais ficam disponíveis.
