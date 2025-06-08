# Workflows Avançados: Interface de Chamada

A Interface de Chamada integra o PraisonAI com a API de voz da Twilio, permitindo
interagir com o agente através de ligações telefônicas. É útil para criar assistentes
por telefone ou serviços automatizados que funcionam 24 horas.

## Configuração

1. Crie uma conta em [Twilio](https://www.twilio.com/) e obtenha:
   - `TWILIO_ACCOUNT_SID`
   - `TWILIO_AUTH_TOKEN`
   - `TWILIO_PHONE_NUMBER`
2. Opcionalmente configure `NGROK_AUTH_TOKEN` para expor o servidor.
3. Exporte também `OPENAI_API_KEY` para acesso ao modelo.

```bash
pip install "praisonai[call]"
```

## Execução

```bash
# Servidor local
praisonai --call --port 8090

# Exponha publicamente com ngrok
praisonai --call --public
```

## Vídeo

[Call Interface](https://www.youtube.com/watch?v=m1cwrUG2iAk)
Veja [[../04_workflows_avancados/16_interface_voz]].
