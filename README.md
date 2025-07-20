# Linux-Stealth-Audit---Monitoramento-invisivel-kernel 2
Um sistema de auditoria furtiva para Linux, focado em monitoramento de processos em nível de kernel sem scripts, utilizando apenas ferramentas nativas."
Linux Stealth Audit - Monitoramento Invisível Nível Kernel
Este projeto de contra inteligência digital simula uma operação de monitoramento avançado e furtivo de processos em sistemas Linux. Utilizando ferramentas nativas como auditctl, ausearch e auditd, o "Linux Stealth Audit" captura execuções críticas em tempo real, sem a necessidade de scripts automatizados.
⚙️ Funcionalidades
 * Rastreio de execuções com 'execve': Monitore a execução de binários importantes.
 * Captura de chamadas a binários sensíveis: Registre o uso de ferramentas como bash, python, netcat, entre outros.
 * Leitura de eventos em tempo real: Obtenha insights imediatos sobre atividades suspeitas.
 * Defesa sem alertar o atacante: Atue de forma discreta para não revelar sua presença.
 * Baseado apenas em ferramentas nativas (sem scripts): Garante menor pegada e maior furtividade.
🚀 Exemplo de Uso
Para monitorar chamadas execve e capturar a execução de binários sensíveis como bash:
sudo auditctl -a always,exit -F arch=b64 -S execve -F path=/bin/bash -k rastreiam_bash
sudo ausearch -k rastreiam_bash

