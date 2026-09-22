# ftth-dti-generator

- **slug:** `dti-generator`
- **private repo:** https://github.com/<ton-compte>/ftth-dti-generator
- **archive:** `dti-generator.zip` — AES-256, 7 file(s)
- **sha256:** `aaedfda98c5b793aec6a12ea9d594d128c892334929e39bab4ea5a5df8e64184`
- **password:** NOT in this folder — see `secrets/dti-generator.pw` on the build machine.
  Send it to recruiters through a different channel than the repo link.

Decrypt and verify:

```bash
python3 decrypt.py '<mot-de-passe>'
sha256sum -c MANIFEST.sha256
```
