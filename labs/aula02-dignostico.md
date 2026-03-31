| Etapa                | Comando                                           | Objetivo                       |
| -------------------- | ------------------------------------------------- | ------------------------------ |
| 🔍 Verificar         | `timedatectl`                                     | Exibir data, hora e fuso atual |
| 🌎 Definir fuso      | `sudo timedatectl set-timezone America/Sao_Paulo` | Ajustar para São Paulo         |
| ⏱️ Ativar NTP        | `sudo timedatectl set-ntp true`                   | Sincronizar automaticamente    |
| 🔄 Reiniciar serviço | `sudo systemctl restart systemd-timesyncd`        | Aplicar sincronização          |
| ✅ Confirmar          | `timedatectl`                                     | Validar configuração final     |


| Problema                     | Causa provável   | Solução                       |
| ---------------------------- | ---------------- | ----------------------------- |
| 🕒 Hora errada               | Fuso incorreto   | Definir `America/Sao_Paulo`   |
| ⛔ Não atualiza               | NTP desativado   | `set-ntp true`                |
| 🌐 Hora não sincroniza       | Sem internet     | Verificar rede                |
| ⚙️ Diferença persistente     | Serviço parado   | Reiniciar `systemd-timesyncd` |
| 🛠️ Ajuste manual necessário | Ambiente isolado | Definir hora manual           |
