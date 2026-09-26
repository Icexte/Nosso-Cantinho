# Nosso Cantinho ❤️ — V1

App Android de casal com login, código de conexão, localização compartilhada, contador de relacionamento e botão WhatsApp.

## Firebase
1. Crie um projeto no Firebase.
2. Adicione um app Android com package `com.ice.casal`.
3. Baixe `google-services.json` e coloque em `app/google-services.json` para build local.
4. Ative Authentication > Email/Password.
5. Crie o Firestore Database.
6. Para GitHub Actions, coloque o conteúdo do `google-services.json` em Settings > Secrets and variables > Actions como `GOOGLE_SERVICES_JSON`.

## Firestore
A V1 usa as coleções `users`, `couples` e `couples/{id}/locations`. Para produção, configure regras para que somente membros do casal leiam/escrevam suas localizações.

Exemplo conceitual de regra: validar `request.auth.uid` contra os membros autorizados do casal. Não use regras abertas em produção.

## Uso
- Cada pessoa cria sua própria conta.
- Uma pessoa cria o código de 6 dígitos.
- A outra entra usando esse código.
- O Android pede permissão de localização.
- A localização compartilhada aparece no mapa enquanto o app está ativo.
- O botão WhatsApp abre a conversa usando o número salvo.

## Observações
Esta V1 não lê mensagens do WhatsApp, não captura sessão do WhatsApp Web e não rastreia localização escondida. O compartilhamento deve ser autorizado pelos dois usuários.
