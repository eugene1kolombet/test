Нужно установить 2 переменные окружения:
TAURI_PRIVATE_KEY в значение приватного ключа без кавычек из файла myapp.key 
TAURI_KEY_PASSWORD в значение p без кавычек

нужно на хостинге создать папку
/windows/x86_64/0.6.6
тут версия текущая (версия из tauri.conf.json 
  "package": {
    "productName": "axe-project",
    "version": "0.6.6"

при запуске экзешника возбмется эта версия, подставится в 

    "updater": {
      "active": true,
      "endpoints": [
	"https://raw.githubusercontent.com/eugene1kolombet/test/main/windows/x86_64/{{current_version}}"

вместо current_version и полезет туда и скачает json
в скачанном json такая информация:

{
  "version": "v0.6.7",
  "notes": "Test version",
  "platforms": 
  {
    "windows-x86_64": 
    {
      "signature": "dW50cnVzdGVkIGNvbW1lbnQ6IHNpZ25hdHVyZSBmcm9tIHRhdXJpIHNlY3JldCBrZXkKUlVUcHppd1BqVGJMbFRYNjI4WEMxQVNyU05JckQ3cXVrenJnY0VEanhSdFl1YWU5SXcxZCtLQ25FZEFnaG1RYitMYThScVRkT2RPU2x6WUhVWWxLdG9aMVZRVmpybEMvOEFrPQp0cnVzdGVkIGNvbW1lbnQ6IHRpbWVzdGFtcDoxNjkwOTkxMzg2CWZpbGU6YXhlLXByb2plY3RfMC42LjdfeDY0LXNldHVwLm5zaXMuemlwClFkNmgyTkoyTnJjcitqY1FBTlVwdFVjdmFKSytyOTlmajVDakpUQkI2R29VNHBCV0d1b2ZsUmk3a2lRZGs4MTVLRTBNZlRXdEtqL2V0djNMK2ZzNUFnPT0K",
      "url": "https://raw.githubusercontent.com/eugene1kolombet/test/main/axe-project_0.6.7_x64-setup.nsis.zip"
    }
  }
}

здесь
"version": "v0.6.7", - новая версия
"url": файл axe-typescript-pixi-game\src-tauri\target\release\bundle\nsis\axe-project_0.6.7_x64-setup.nsis.zip 
"signature" содержимое файла axe-typescript-pixi-game\src-tauri\target\release\bundle\nsis\axe-project_0.6.7_x64-setup.nsis.zip.sig 
