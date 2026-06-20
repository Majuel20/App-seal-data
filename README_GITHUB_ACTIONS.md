# APP Seal Data - GitHub Actions

Este paquete permite que GitHub ejecute el extractor de SEAL automáticamente, sin depender de que tu PC esté encendida.

## Qué hace

- Ejecuta `seal_cortes_final_v2.py` todos los días a las 07:00 Perú.
- Genera archivos en la carpeta `docs/`.
- Actualiza:
  - `docs/cortes_seal_latest.json`
  - `docs/cortes_seal_latest.xlsx`
  - `docs/cortes_seal_latest.csv`
  - `docs/cortes_seal_latest.txt`
  - `docs/historial_cortes.sqlite`

## Pasos

1. Crea un repositorio en GitHub, por ejemplo:
   `app-seal-data`

2. Sube estos archivos al repositorio:
   - `seal_cortes_final_v2.py`
   - `requirements.txt`
   - `.github/workflows/actualizar_cortes.yml`

3. En GitHub entra a:
   Settings > Actions > General

4. En "Workflow permissions" activa:
   "Read and write permissions"

5. Entra a:
   Actions > Actualizar cortes SEAL > Run workflow

6. Cuando termine, se creará la carpeta `docs`.

7. Activa GitHub Pages:
   Settings > Pages > Build and deployment
   Source: Deploy from a branch
   Branch: main
   Folder: /docs

8. La app Android podrá leer:
   `https://TU_USUARIO.github.io/app-seal-data/cortes_seal_latest.json`

También puedes usar el raw:
`https://raw.githubusercontent.com/TU_USUARIO/app-seal-data/main/docs/cortes_seal_latest.json`
