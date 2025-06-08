# Guia de Instalação Local (Linux)

Este documento explica como preparar um ambiente Linux para executar o PraisonAI. Siga os passos para configurar variáveis de ambiente, instalar o Python 3.11 ou superior e usar `pipx` para a CLI.

## Pré‑requisitos

1. **Python 3.11+**
   - Verifique sua versão:
     ```bash
     python3 --version
     ```
   - A maioria das distribuições já possui pacotes atualizados. Se precisar, use `apt`, `dnf` ou `pacman` (dependendo da distro) ou instale com [`pyenv`](https://github.com/pyenv/pyenv).
2. **Git** (opcional, para clonar o repositório).

## Configurando Variáveis de Ambiente

Defina `OPENAI_API_KEY` para acessar modelos comerciais ou utilize `OPENAI_BASE_URL` e `OPENAI_MODEL_NAME` para modelos locais (ex.: Ollama ou LM Studio). Para exportar temporariamente:
```bash
export OPENAI_API_KEY=sua_chave
```
Coloque essas linhas no arquivo `~/.bashrc` ou `~/.zshrc` para torná‑las permanentes.

## Instalando o PraisonAI

O método mais simples é usar `pipx` para isolar a CLI:
```bash
python3 -m pip install --user pipx
pipx install praisonai
```
Isso instala a ferramenta sem interferir em outros projetos Python. Se preferir, use ambientes virtuais e o `pip` padrão.

Para executar com modelos locais, defina:
```bash
export OPENAI_BASE_URL=http://localhost:11434/v1
export OPENAI_MODEL_NAME=llama3:latest
```
Assim a CLI utilizará o servidor Ollama/LM Studio.


## Uso de GPU e TensorRT

Se sua máquina possui uma GPU NVIDIA, instale o PyTorch com CUDA conforme as instruções em `https://pytorch.org`.
Um exemplo:
```bash
pip install torch --index-url https://download.pytorch.org/whl/cu121
```
Para acelerar modelos locais (Ollama, LM Studio), instale também o TensorRT compatível com seus drivers e verifique com `nvidia-smi` se a placa está ativa.
Quantizações 8/4 bits ajudam a economizar memória durante a inferência.

### Uso Básico

Depois da instalação, teste no terminal:
```bash
praisonai --auto "Explique o que é um agente autônomo."
```
Se ocorrerem erros de importação, verifique se `pipx` adicionou sua pasta de executáveis ao `PATH`.

Veja [[../03_usando_praisonai/01_usando_com_python]].
Se surgirem dificuldades durante a instalação, confira [[../08_contribuindo_e_desenvolvimento/02_debug_e_boas_praticas]] para dicas de depuração.

## Exercícios

1. Revise os conceitos apresentados acima.
2. No terminal, navegue até `examples` e execute um dos scripts relacionados.
3. Modifique algum parâmetro e observe os resultados.
