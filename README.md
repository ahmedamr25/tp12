# tp12





##Lancement de Medusa

```bash
python medusa.py
```

Sélection du device :

```text
emulator-5554
```
<img width="1101" height="630" alt="Screenshot 2026-04-26 170356" src="https://github.com/user-attachments/assets/b88f3694-c4ec-46d0-b1ed-660f9ba3bf10" />

---

## Recherche des modules

```bash
search root
```


---
<img width="563" height="270" alt="Screenshot 2026-04-26 172923" src="https://github.com/user-attachments/assets/a864c25d-e47e-4376-8f90-e958fa4ada72" />

## Activation du module

```bash
use root_detection/universal_root_detection_bypass
```

---

## Lancement de l’application

```bash
run -f owasp.mstg.uncrackable3
```
<img width="1919" height="851" alt="Screenshot 2026-04-26 174014" src="https://github.com/user-attachments/assets/fdaf7323-ed8a-498b-bd97-6ed963d6bd28" />

---

## Résultats obtenus

Logs observés :

```text
Bypass return value for binary: su
Bypass test-keys check
Bypass return value for binary: Superuser.apk
[!] overwriting is debugger connected
```



## Analyse

Le bypass de root est **réussi**, mais l’application implémente des protections supplémentaires :

* Détection de debugger
* Détection d’instrumentation (Frida)
* Vérifications natives

Ces mécanismes entraînent la terminaison du processus.

