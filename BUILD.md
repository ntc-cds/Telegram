## Setup

1. Crie uma keystore e coloque dentro da pasta TMessagesProj/config/debug
2. [**Obter api_id**](https://core.telegram.org/api/obtaining_api_id) para aplicação.
3. Dentro do arquivo BuildVars.java set o APP_ID e APP_HASH com o id e hash gerado no site do telegram
4. [** Obter Hockey App Hash **](https://hockeyapp.net/)
5. Ainda dentro do BuildVars.java set HOCKEY_APP_HASH com o token da aplicação gerada dentro do hockey app
6. [** Google Developers **](https://console.developers.google.com/) Crie um novo projeto dentro do google console developers,
no menu lateral escolha o item Credenciais e crie um novo ID Client Oauth 2.0, coloque o mesmo certificado digital da keystore usada para gerar build.
7. Habilite também a API do GCM no painel do google.

Dentro da pasta TMessagesProj crie o arquivo google-services.json com o seguinte conteúdo

```javascript
{
  "project_info": {
    "project_number": PROJECT_ID_GOOGLE_CONSOLE
  },
  "client": [
    {
      "api_key": [{ "current_key": "" }],
      "client_info": {
        "android_client_info": {
          "package_name": "br.com.cetsp.zap"
        }
      }
    }
  ]
}
```
