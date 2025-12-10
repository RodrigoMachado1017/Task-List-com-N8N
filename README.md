# Task-List-com-N8N

Este é um projeto desenvolvido no n8n para realizar a transcrição de mensagens de voz recebidas no Telegram para criar uma task em um board no Trello. As técnologias utilizadas foram

## Instalação e Configuração

### Pré-requisitos

- n8n instalado ([https://n8n.io](https://n8n.io))
- rodar o n8n via URL publica, sem isso o workflow não funciona (telegram não premite requisições para workflows locais)
- Conta no Telegram que possua bot no bot father
- Conta no AssemblyAI
- Conta no Trello
- Node.js 14+ (se executando localmente)

### Passos de Instalação

1. **Clone ou baixe o projeto**

```bash
git clone <seu-repositório>
cd Task-List-com-N8N
```

2. **Importe o workflow no n8n**

    - Abra o n8n com "n8n start --tunnel" ou utlize alguma ferramenta com tunel https, sugerimos o ngrok + docker

    - Clique em "Import" e selecione o arquivo JSON do workflow

    - Confirme a importação

3. **Configure as credenciais**

    - Telegram: 
        -> Crie o bot a partir do BotFather
        -> Adicione seu bot token no primeiro step do workflow (credencial do Telegram)

    - AssemblyAI:
        -> Faça login ou crie uma conta no AssemblyAI e gere uma chave api (sera importantes na autentucação dos 3 passos referentes ao Assembly)
        -> Caso haja duvidas procurar se infomrar na documentação https://www.assemblyai.com/docs

    - Trello: 
        -> Entre na documentação do Trello para poder saber como configurar seu ambiente (logue no trello e coloque https://trello.com/power-ups/ na url)
        -> Autorize sua conta e selecione o board/lista

4. **Ative o workflow**
    - Clique em "Activate" para iniciar o workflow
    - Teste enviando uma mensagem de voz no Telegram

### Estrutura do Projeto
- `V_msg_trans.json` - Arquivo principal do workflow
- `README.md` - Este arquivo

### Suporte
Para dúvidas, consulte a [documentação do n8n](https://docs.n8n.io).
