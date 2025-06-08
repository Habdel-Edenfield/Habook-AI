# Debug e Boas Práticas

Mesmo seguindo os guias de instalação, alguns problemas podem surgir ao executar o PraisonAI. Esta página traz dicas rápidas para inspecionar logs e resolver falhas comuns.

## Problemas Comuns

### Erros de instalação
* Dependências não encontradas ou conflitos normalmente indicam que o ambiente virtual não está ativado. Reinstale com `uv pip install -e .` ou `pip install -e .`.
* Caso o `pip` apresente mensagens de "permission denied", verifique se você está usando uma conta com permissões suficientes ou prefira o modo virtualenv/pipx.

### `ModuleNotFoundError`
Se scripts acusarem que o pacote `praisonaiagents` não existe, instale-o manualmente:
```bash
pip install praisonaiagents
```
Ou, dentro do repositório clonado, execute `uv pip install -e .`.

### Variáveis de ambiente ausentes
Modelos como os da OpenAI requerem `OPENAI_API_KEY`. Confirme com:
```bash
printenv OPENAI_API_KEY
```
Caso não esteja definida, exporte-a no terminal antes de executar os exemplos.

## Inspecionando Logs

O PraisonAI utiliza mensagens no console para relatar o progresso das tarefas. Para tornar a saída mais detalhada, defina:
```bash
export LOGLEVEL=debug
```
Isso habilita mensagens extras durante a execução das ferramentas e dos agentes, facilitando identificar onde algo falhou.

Se estiver utilizando os exemplos em Python, também é possível imprimir pilhas de erro completas adicionando `-v` ao comando `pytest` ou executando os scripts diretamente em modo verbose.

## Dicas de Solução de Problemas

1. **Verifique a Conexão com a Internet** – Muitos provedores de modelo exigem acesso online.
2. **Atualize Dependências** – Rode `pip install -U praisonai praisonaiagents` para garantir versões compatíveis.
3. **Limpe Configurações** – Apague ou renomeie `config.yaml` se suspeitar que opções antigas estão causando conflitos.
4. **Consulte os Testes** – Execute `python tests/simple_test_runner.py --fast` para garantir que o ambiente está saudável.

Seguindo estas recomendações você terá um ponto de partida sólido para depurar problemas recorrentes.
