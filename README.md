# 🕵️ Linux Monitor Furtivo

Este projeto te ajuda a "espiar" o que acontece no seu sistema Linux de uma forma bem discreta. Ele monitora a execução de programas e comandos importantes, usando ferramentas que já vêm no próprio Linux, como `auditctl`, `ausearch` e `auditd`.

A ideia é que você possa ver atividades suspeitas em tempo real, sem precisar de scripts complicados e sem que alguém mal-intencionado perceba que está sendo monitorado.

## 🎯 O Que Ele Faz?

* **Rastreia o início de programas:** Ele fica de olho quando certos programas são executados.
* **Identifica comandos importantes:** Ajuda a ver o uso de programas comuns, mas que podem ser usados de forma indevida (como `bash`, `python` ou `netcat`).
* **Observa em tempo real:** As informações são coletadas na hora em que acontecem.
* **É invisível:** O monitoramento é feito de forma que não chame atenção do atacante.
* **Usa ferramentas do próprio Linux:** Não precisa instalar nada extra, só as ferramentas que já existem no sistema.

## 🚀 Como Usar (Exemplo Simples)

Quer ver quando alguém usa o comando `bash` (o terminal) no seu sistema? Você pode configurar uma regra assim:

```bash
sudo auditctl -a always,exit -F arch=b64 -S execve -F path=/bin/bash -k monitor_bash

"É fundamental ressaltar: este projeto foi desenvolvido exclusivamente para fins de proteção e defesa, visando fortalecer a segurança do seu sistema, e não para qualquer tipo de uso ofensivo ou malicioso."

