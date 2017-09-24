# Classe-E-Oficial
Diretório do código do Foguete Classe E

Código funciona porém sem telemetria implementada. Apenas ligando o APC220 no RX-TX Arduino é possível implementar uma telemetria,
pois o APC220 sera interpretado como uma port serial fisica (Se fizer isso, lembre-se que upar o código com o APC220 ligado no RX-TX não é possível).

Um mecanismo mais eficiente de implementar a telemetria é conectar os pinos D5 e D7 do Arduino no TX e no RX (respectivamente) do APC (além do ground e do VCC) e descomentar no código as linhas 24 (nessa linha, troque o 6 por um 5), 49, 72, 85, 86 e 177-189. Dessa forma, o código que é printando na porta Serial do Arduino também será exibido na porta Serial usada pelo APC220 de recepção, que estará ligado ao computador, sem necessidade de desconectar o APC para upar o código do Arduino.
