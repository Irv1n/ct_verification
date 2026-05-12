# Archive parts

Архив `ct_verif_1_0_148.zip` должен быть загружен частями base64.

Восстановление:

```bash
cat ct_verif_1_0_148.zip.b64.part* > ct_verif_1_0_148.zip.b64
base64 -d ct_verif_1_0_148.zip.b64 > ct_verif_1_0_148.zip
sha256sum ct_verif_1_0_148.zip
```

Ожидаемый SHA256:

```text
55256e3662dae15fd9a66e7df60622ee7f5053f35c041ec96563c326979de9a2
```
