# CT Verification Workspace

Актуальная зафиксированная версия: **ct_verif_1_0_148.zip**.

Дата фиксации: 12.05.2026.

## Что зафиксировано в 1.0.148

- аварийно-приоритетная команда возврата ЛАТРа в начало;
- возврат не блокируется при автоматическом прогоне;
- backend не отдаёт `409 ЛАТР занят` для возврата в начало;
- перед возвратом принудительно снимаются `UP` и `DOWN`;
- после возврата всегда выполняется `STOP`;
- при `GPIO busy` используется прямой backend `pinctrl/raspi-gpio`, затем fallback через `RPi.GPIO`;
- обычные `UP/DOWN` блокируются, пока идёт принудительный возврат.

## SHA256 архива

```text
55256e3662dae15fd9a66e7df60622ee7f5053f35c041ec96563c326979de9a2  ct_verif_1_0_148.zip
```

## Быстрая загрузка с локального компьютера

Если архив `ct_verif_1_0_148.zip` лежит рядом, выполнить:

```bash
rm -rf ct_verification_push
mkdir ct_verification_push
cd ct_verification_push
unzip ../ct_verif_1_0_148.zip
git init
git branch -M main
git remote add origin https://github.com/Irv1n/ct_verification.git
git add .
git commit -m "Initial CT Verification Workspace 1.0.148"
git push -u origin main
```
