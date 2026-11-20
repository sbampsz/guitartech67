# guitartech67 (Android)

## Jeito mais fácil: gerar o APK na nuvem (sem instalar nada)
1. Crie uma conta grátis em github.com e um repositório novo.
2. Envie TODOS os arquivos desta pasta para o repositório (inclusive a pasta `.github`).
3. Abra a aba **Actions** do repositório. O "Gerar APK guitartech67" roda sozinho (leva uns 5 a 10 minutos). Se não rodar, clique nele e em **Run workflow**.
4. Quando ficar verde, abra a execução e baixe **guitartech67-apk** na parte "Artifacts". Dentro tem o arquivo `guitartech67.apk`.
5. Passe o APK para o celular, abra e permita "instalar de fontes desconhecidas".

## Jeito local (Android Studio)
```
npm install
npx cap add android
```
No arquivo `android/app/src/main/AndroidManifest.xml`, antes de `<application>`, coloque:
```
<uses-permission android:name="android.permission.RECORD_AUDIO" />
<uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
```
Depois `npx cap sync`, `npx cap open android` e, no Android Studio, Build > Build APK(s).

## IA no celular
Learn AI, Tone Lab, Creative Lab e Tab Assistant usam a API da Anthropic. Na primeira vez o app pede a sua chave (console.anthropic.com), que fica salva só no aparelho. Use este APK só para você.

## Observações
- Afinador e Chord Explorer funcionam sem internet. A fonte e a IA precisam de internet.
- Para mudar o app, edite `www/index.html`.
