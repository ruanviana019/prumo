# Prumo – APK

## Opção A: sem instalar nada (GitHub)
1. Crie uma conta em github.com e um repositório novo (pode ser privado).
2. Envie todo o conteúdo desta pasta para ele (botão "Add file > Upload files"; inclua a pasta `.github`).
3. Abra a aba **Actions**, escolha **Gerar APK** e clique em **Run workflow**.
4. Ao terminar (uns 5 a 10 min), abra a execução e baixe **Prumo-apk** em "Artifacts". Dentro do zip está o `app-debug.apk`.
5. No Android, copie o APK, toque nele e permita "instalar apps desconhecidos".

## Opção B: no seu computador
Requisitos: Node 18+, Java 17 e Android Studio (SDK).
    npm install
    npx cap add android
    npx cap sync android
    cd android && ./gradlew assembleDebug
O APK sai em `android/app/build/outputs/apk/debug/app-debug.apk`.

## Observações
- É um APK de **debug** (assinado com chave de teste): serve para instalar e usar, mas não para publicar na Play Store.
- Os dados ficam no armazenamento do próprio app. Desinstalar apaga tudo.
- Para alterar o app, edite `www/index.html` e gere o APK de novo.
