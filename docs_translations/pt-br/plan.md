# Plano de Conteúdo do Curso PraisonAI

Este arquivo resume os módulos já existentes na documentação em `docs/pt-br` e aponta temas que ainda podem ser desenvolvidos. Use-o como guia para acompanhar o progresso do material.

## Conteúdo Atual

1. **Introdução**
   - Como usar esta documentação e plugins recomendados para Obsidian.
   - O que é o PraisonAI, filosofia e casos de uso.
   - Metodologia de aprendizado baseada em ciclo científico.
2. **Instalação**
   - Guia completo de instalação no Windows com variáveis de ambiente e verificação do pacote.
3. **Conceitos Fundamentais**
   - Explicação sobre agentes, tarefas, ferramentas, processos, memória e RAG.
4. **Usando o PraisonAI**
   - Uso com Python (`praisonaiagents`).
   - Uso com YAML (CLI `praisonai`).
   - Uso com JavaScript/TypeScript.
   - Guia rápido "Criando Seu Primeiro Agente".
   - Catálogo de modelos de agentes disponíveis nos exemplos.
   - Configurações com YAML para definir agentes de forma declarativa.
   - Importações e funções essenciais para criação de agentes.
   - Como funcionam os imports e gerenciamento de dependências – aula dedicada a importação global versus seletiva, extras opcionais e boas práticas para organizar os módulos. Veja [[03_usando_praisonai/08_como_funcionam_imports.md]].
5. **Workflows Avançados**
   - Colaboração entre agentes, roteamento, orquestração, modo autônomo, paralelização e encadeamento de prompts.
6. **Ferramentas**
   - Visão geral e criação de ferramentas personalizadas.
7. **Modelos LLM**
   - Configuração de diferentes provedores (OpenAI, Ollama, Groq, etc.).
8. **Exemplos Práticos**
   - Estudos de caso demonstrando aplicações reais do framework.
9. **Contribuindo e Desenvolvimento**
   - Passos para trabalhar localmente e contribuir com o projeto.
   - Entendendo a estrutura do código em `src/`.
10. **Dúvidas Frequentes (FAQ)**
    - Respostas rápidas para erros comuns de instalação e execução.

- Documentar a estrutura do código e exemplos de YAML (concluído)
- (atualizado) Guia de instalação no Windows expandido com recomendações de 2024/2025.
- Revisar todos os módulos para incorporar novidades recentes (Python 3.11+, pipx, modelos locais com Ollama/LM Studio e otimizações de GPU).

## Pontos a Desenvolver

### Primeiro Semestre de 2024
- (novo) Lição detalhada sobre funcionamento dos imports e dependências ([[03_usando_praisonai/08_como_funcionam_imports.md]]).
- (atualizado) Guia de instalação no Windows expandido com recomendações de 2024/2025.
- Padronizar links internos usando o formato `[[arquivo.md]]` para facilitar a navegação.
- Incluir guia de depuração e boas práticas para resolução de problemas.
- Explorar exemplos mais detalhados de ferramentas e memórias avançadas.
- Documentar integrações específicas com outros provedores de LLM (ex.: Gemini, Anthropic).

### Segundo Semestre de 2024
- Revisar todos os módulos para incorporar novidades recentes (Python 3.11+, pipx, modelos locais com Ollama/LM Studio e otimizações de GPU). Seções dedicadas estão em [[01_instalacao/00_instalacao_windows#uso-de-gpu-e-tensorrt]] e [[06_modelos_llm/00_usando_diferentes_llms#desempenho-com-gpu-para-modelos-locais]].
- Criar seções para recursos ainda não documentados:
  - (concluído) Agentes Multimodais
  - (concluído) Code Interpreter Agents
  - (concluído) Math Agents
  - (concluído) Agentes com Saída Estruturada
  - (concluído) Callback Agents
  - (concluído) Mini AI Agents
- Documentar a estrutura do código e exemplos de YAML (concluído)

### Concluído
- Instruções de instalação para Linux e macOS.
- Seções de **Exercícios** adicionadas ao final de cada módulo.



Este plano deve ser atualizado sempre que novos módulos ou seções forem criados.
Veja [[README]].
