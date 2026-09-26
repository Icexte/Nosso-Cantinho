# Configuração rápida no GitHub

1. Crie um projeto no Firebase.
2. Authentication > Sign-in method > Email/Password: ative.
3. Firestore Database: crie o banco.
4. Adicione um app Android com `com.ice.casal`.
5. Baixe `google-services.json`.
6. No GitHub: Settings > Secrets and variables > Actions > New repository secret.
7. Nome: `GOOGLE_SERVICES_JSON`.
8. Cole o conteúdo inteiro do arquivo JSON como valor.
9. Envie esta pasta para o repositório.
10. Abra Actions > `construir` > Run workflow.
11. Ao terminar, abra o artifact `Nosso-Cantinho-debug` e baixe o APK.

IMPORTANTE: as regras `firestore.rules` são uma base para desenvolvimento. Antes de publicar, restrinja leitura/escrita às duas contas efetivamente vinculadas ao mesmo casal.
