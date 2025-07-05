YouTube Playlist Stats (API v3)
Script Python que conecta na API do YouTube usando OAuth2, lista os vídeos de uma playlist pública e exibe a quantidade de visualizações de cada vídeo. Simples, funcional e autorizado (literalmente).

O que esse projeto faz
Conecta na YouTube Data API v3 usando credenciais OAuth2

Acessa uma playlist do YouTube (via playlistId)

Recupera os IDs dos vídeos

Busca as estatísticas de visualizações

Imprime no console: id - views

Pré-requisitos

1. Ativar API do YouTube
Acesse: https://console.developers.google.com/

Crie um projeto e ative a YouTube Data API v3

Gere um OAuth 2.0 Client ID (tipo: Desktop app)

Baixe o arquivo secrets.json

2. Instalar dependências

pip install --upgrade google-auth-oauthlib google-api-python-client

Como funciona

O script usa a biblioteca google_auth_oauthlib para autenticar via navegador (OAuth2)

Usa o método playlistItems().list() para pegar os vídeos

Depois chama videos().list() com os IDs para puxar as estatísticas

Exemplo de saída

yt_video_id_1 - 12345
yt_video_id_2 - 98765
yt_video_id_3 - 45678

Avisos importantes

Não compartilhe seu secrets.json — ele dá acesso à sua conta do Google.

A playlistId deve ser pública.

O token gerado é temporário e armazenado localmente (padrão do flow interativo).

Para mais estatísticas (likes, comentários, etc), adicione no part="statistics".

