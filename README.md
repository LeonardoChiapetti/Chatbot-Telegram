🌤️ Telegram Weather Chatbot (n8n)
📌 Descrição do Projeto

Este projeto apresenta um chatbot construído no n8n, integrado ao Telegram Bot API e à OpenWeather API.

O bot recebe uma cidade enviada pelo usuário e responde com a temperatura atual, de forma automática e formatada.

⚙️ Funcionalidades

✅ Recebe mensagens via Telegram
✅ Normaliza e valida o texto digitado
✅ Consulta a OpenWeather API
✅ Extrai e arredonda a temperatura
✅ Trata erros (cidade inválida / não encontrada)
✅ Retorna resposta amigável ao usuário

🧩 Estrutura do Workflow

O workflow é composto basicamente por:

Telegram Trigger → Recebe mensagens

Function / Set Node → Normaliza entrada

HTTP Request → Consulta OpenWeather

Function Node → Processa temperatura

IF Node → Trata erros

Telegram Node → Envia resposta

🚀 Como Importar o Workflow

Abra o n8n

Clique em Import Workflow

Selecione o arquivo:

workflow-telegram-chatbot.json

🔑 Credenciais Necessárias
🤖 Telegram Bot

Criar bot via BotFather

Copiar o TELEGRAM_BOT_TOKEN

Inserir em:

n8n → Credentials → Telegram

🌍 OpenWeather API

Criar conta em: https://openweathermap.org/

Gerar uma API Key

Inserir no n8n como credencial ou variável:

OPENWEATHER_API_KEY

🌎 Variáveis Utilizadas

O workflow espera as seguintes variáveis:

OPENWEATHER_API_KEY

TELEGRAM_BOT_TOKEN

Cada usuário deve inserir suas próprias credenciais.

▶️ Execução

Ative o workflow no n8n

Envie uma mensagem para o bot no Telegram

📨 Formato esperado:

Cidade,UF
Exemplo: São Paulo,SP
❌ Tratamento de Erros

Caso a cidade não seja encontrada ou esteja inválida:

❌ Cidade não encontrada.
Use o formato Cidade,UF (ex.: São Paulo,SP).
🌐 Configuração do Webhook (se aplicável)

Se estiver rodando o n8n localmente:

Utilize ngrok ou similar

Configure a variável:

WEBHOOK_URL=https://seu-endereco.ngrok-free.dev

Reinicie o n8n

🛠️ Troubleshooting

Bot não responde

Verifique se o workflow está ativo

Confirme se o token do Telegram está correto

Cheque se o webhook foi registrado

Erro na API OpenWeather

Verifique a validade da API Key

Confirme limites de requisição

Cidade não encontrada

Use o formato: Cidade,UF

⚠️ Segurança

🔒 Este repositório não contém tokens ou credenciais.

Todas as chaves de API devem ser configuradas manualmente após a importação.

🛠️ Tecnologias Utilizadas

n8n

Telegram Bot API

OpenWeather API

👨‍🎓 Contexto Acadêmico

Projeto desenvolvido para fins educacionais como requisito de avaliação da pós-graduação em:

🎓 IA e Automação
