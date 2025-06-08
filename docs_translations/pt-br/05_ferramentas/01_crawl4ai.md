# Ferramenta: Crawl4AI

Crawl4AI é um serviço de *web crawling* e raspagem de páginas voltado para integração com LLMs. Com ele os agentes do PraisonAI podem obter conteúdo recente da internet de forma programática.

## Obtendo a chave de API

1. Acesse [https://crawl4.ai](https://crawl4.ai/) e crie uma conta gratuita.
2. No painel do usuário, gere uma chave de API.
3. Defina a variável de ambiente `CRAWL4AI_API_KEY`:
   ```bash
   export CRAWL4AI_API_KEY="sua_chave_aqui"
   ```

## Configurando no PraisonAI

### Em YAML
```yaml
roles:
  pesquisador_web:
    role: "Pesquisador Web"
    goal: "Buscar informações atualizadas."
    tools:
      - "crawl4ai_search"
keys:
  CRAWL4AI_API_KEY: ${CRAWL4AI_API_KEY}
```

### Em Python
```python
from praisonaiagents import Agent

agent = Agent(
    role="Pesquisador Web",
    goal="Buscar informações atualizadas.",
    tools=["crawl4ai_search"],
)
```

## Limites e cuidados

- O Crawl4AI possui cota gratuita limitada; rastreamentos extensos podem gerar custos adicionais.
- Consulte a página oficial para valores e políticas de uso.
- Respeite os termos do serviço e as regras dos sites rastreados (como `robots.txt`).
- Mantenha sua chave de API em local seguro e evite publicá-la em repositórios.
