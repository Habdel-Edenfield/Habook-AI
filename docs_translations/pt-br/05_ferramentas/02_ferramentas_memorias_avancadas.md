# Ferramentas e Memórias Avançadas

Este módulo complementa a [[00_visao_geral_ferramentas.md]] e traz exemplos práticos de recursos lançados em 2024/2025 que aumentam as capacidades dos agentes.

## Graph Memory com Mem0

A integração com o serviço Mem0 permite armazenar relações complexas entre informações em bancos como Neo4j ou Memgraph. O script `examples/python/memory/graph-memory-agent.py` demonstra o uso combinado de grafo e banco vetorial (Qdrant).

```bash
pip install "praisonaiagents[graph]"
python examples/python/memory/graph-memory-agent.py
```

> [!NOTE]
> Configure as variáveis de ambiente do Neo4j ou Memgraph antes de executar o exemplo.

## Ferramentas Personalizadas

Você pode criar funções próprias e registrá-las como ferramentas. Consulte o exemplo [[../../examples/python/general/example_custom_tools.py]] para ver como disponibilizar buscas na web ou validação de dados.

Combine essas ferramentas com memória de longo prazo para workflows mais autônomos.

## Boas Práticas para Memória Persistente

Utilize bancos vetoriais como Qdrant ou Chroma, aliados a quantizações em 8/4 bits e drivers de GPU recentes para otimizar a busca de grandes coleções. Para detalhes sobre os tipos de memória veja [[../02_conceitos_fundamentais/05_memoria.md]].

## Exercícios

1. Execute `graph-memory-agent.py` e observe como as informações são gravadas no grafo.
2. Altere alguma ferramenta do exemplo de ferramentas personalizadas e teste o agente novamente.
