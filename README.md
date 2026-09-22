# Générateur automatique de DTI — Dossier Technique d'Immeuble (FTTH)

> **🔒 The source code in this repository is encrypted.**
> The archive `dti-generator.zip` is protected with **WinZip AES-256** encryption.
> The password is shared privately with recruiters / reviewers on request.

## What it does

Application Python qui génère les DTI (Dossiers Techniques d'Immeuble) à partir de shapefiles, de fichiers Excel de route optique et de photos terrain.

- **Extraction multi-sources** : shapefiles (`dbfread`), Excel (`pandas`), données IMB, PBO, BPE, câbles et PTECH.
- **Génération Excel** : classeurs multi-feuilles (`openpyxl`), template choisi automatiquement selon 4 cas de configuration réseau, remplissage des cellules fusionnées, insertion et redimensionnement des photos, liens Google Maps depuis les coordonnées X/Y, recalcul des formules via LibreOffice headless.

## Results

- **100+ DTI générés** automatiquement.
- De **plusieurs heures à quelques secondes** par bâtiment.
- Suppression des erreurs de saisie, livrables standardisés.

## Stack

Python · pandas · openpyxl · dbfread · Pillow · PyQGIS · regex · subprocess · LibreOffice headless

## Decrypt & run

```bash
pip install pyzipper
python3 decrypt.py          # prompts for the password, extracts to ./src
# or without the helper (7-Zip / WinZip / unzip all support AES-256):
7z x dti-generator.zip -p
```

## Integrity

Every file inside the archive is listed with its SHA-256 in `MANIFEST.sha256`.
Verify **from the repository root** (the paths are relative to it):

```bash
sha256sum -c MANIFEST.sha256      # Linux / macOS / Git Bash
certutil -hashfile src\main.py SHA256   # Windows, per file
```

---
*Ali Nouna — alinouna@gmail.com — linkedin.com/in/AliNouna*
