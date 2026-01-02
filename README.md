# esp32_midea_ac_control
Plug In to control air conditioner via Wifi

Placa ESP32 WROOM-32 TYPE-C ch340c/cp2102 wifi + bluetooth ultra-baixo consumo de energia módulo sem fio dual core
Adaptador USB A to C

Use with Arduino IDE 2.3.7.
Configuração da Board: No menu Tools, certifique-se de que a Board seja: ESP32 Dev Module

Pinagem da placa: (não é necessario fazer -- apenas informativo)
  VCC (Pino 1 do USB do AC): Ligue no pino VIN do ESP32.
  D-  (Pino 2 do USB do AC): Ligue no GPIO 16 (RX2).
  D+  (Pino 3 do USB do AC): Ligue no GPIO 17 (TX2).
  GND (Pino 4 do USB do AC): Ligue no GND do ESP32.


Como funciona o Fallback:
Primeira vez: O ESP32 não conhece nenhuma rede. Ele criará o sinal Wi-Fi "AC-Config-Portal".
  Configuração: Você conecta nesse sinal com seu celular, uma tela abrirá automaticamente (Captive Portal), você escolhe a rede "AS_24G", digita a senha e salva.
Uso diário: O ESP32 ligará e conectará direto.
  Se o roteador cair: Ele tentará conectar por alguns segundos. Se falhar, ele reativa o portal de configuração para você poder trocar a rede sem precisar ligar o ESP32 no computador.
