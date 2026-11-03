# Bitty para Windows

Este repositorio empaqueta el HTML original de Bitty como una aplicación de escritorio para Windows usando Electron.

## Cómo generar el instalador desde GitHub

1. Crea un repositorio nuevo en GitHub llamado `Bitty`.
2. Sube **todo el contenido** de esta carpeta (incluida la carpeta `.github`).
3. En GitHub, entra en la pestaña **Actions** y habilita los workflows si GitHub te lo solicita.
4. El workflow `Build Bitty for Windows` se ejecutará al subir cambios a `main`. También puedes iniciarlo manualmente desde **Actions → Build Bitty for Windows → Run workflow**.
5. Cuando termine, abre la ejecución y baja hasta **Artifacts**.
6. Descarga `Bitty-Windows-Installer`; dentro estará `Bitty-Setup-1.0.0.exe`.

## Probar en tu propio PC (opcional)

Necesitas Node.js instalado. Abre una terminal en esta carpeta y ejecuta:

```bash
npm install
npm start
```

Para crear el instalador localmente en Windows:

```bash
npm run dist
```

El instalador aparecerá en la carpeta `dist`.

## Notas

- El progreso de Bitty se guarda en el almacenamiento local de la aplicación y permanece entre aperturas.
- Las fuentes de Google del HTML original necesitan conexión a Internet; si no hay conexión, se usarán las fuentes alternativas del sistema.
- El instalador está configurado para Windows de 64 bits.
