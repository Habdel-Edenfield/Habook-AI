# Workflows Avançados: Interface de Voz

A interface de voz permite conversar em tempo real com os agentes utilizando microfone e alto-falantes.
É ideal para demonstrações e para quem deseja interação mais natural sem digitar comandos.

## Instalação

```bash
pip install "praisonai[realtime]"
# ou
./src/praisonai/setup.sh -r --run
```

Configure a variável `OPENAI_API_KEY` e certifique-se de que seu dispositivo de áudio está funcionando.

## Como usar

```bash
# Inicie a interface de voz
praisonai --realtime
```

Também é possível executar via módulo Python:

```bash
python3 -m praisonai realtime
```

## Vídeo

[Realtime Voice Interface](https://www.youtube.com/watch?v=frRHfevTCSw)
Veja [[../04_workflows_avancados/15_interfaces_interativas]].

## Exercícios

1. Revise os conceitos apresentados acima.
2. No terminal, navegue até `examples` e execute um dos scripts relacionados.
3. Modifique algum parâmetro e observe os resultados.
