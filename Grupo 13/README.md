# Estagio2024 - Grupo 13 - Ideias para o Robô

## Mecânica

1. parachoque triangular - direcionar os avanços do adversário para as asas do robô, diminuindo o próprio ponto fraco.
2. sensor infravermelho - reconhecer as bordas da arena e mover os motores para evitar a saída da arena.
3. abrir as asas - utilizar engrenagens para transferir o movimento inicial do motor para as asas, empurrando-as no início da luta, assim que o robô fizer o primeiro movimento.
4. sensor de toque nas asas - para otimizar o sentido da rotação do robô e aumentar a chance de colocar o adversário numa posição ruim, construir uma mecânica permita que as asas se movimentem também de forma horizontal e colocar um sensor de toque atrás delas, de forma que empurrar uma asa também empurraria o botão do sensor. Assim, seria possível saber o lado que o adversário está pressionando o robô e reagir de acordo.

---

## Código

1. Iniciar a luta chacoalhando o robô para frente e para trás para que as asas abram.
2. Quando o sensor infravermelho na frente do robô detectar a borda da arena, dar ré e girar o robô em meia lua para evitar a saída.
```c
OnFwd(motorDireita,-100);
OnFwd(motorEsquerda,-100);
Wait(500);
OnFwd(motorDireita,-100);
OnFwd(motorEsquerda,75);
Wait(500);
```
3. Quando o sensor de toque nas asas for pressionado, girar o robô na direção oposta à pressão, fazendo o adversário passar reto pela asa.
4. Enquanto o robô não estiver enxergando o adversário, gire até encontrar o adversário.
5. Quando o robô estiver enxergando o adversário, empurre-o para fora da arena.
6. A cada X tempo que o robô estiver enxergando e empurrando o adversário, dar ré de curta distância e girar para empurrar de outro ângulo (nosso robô sempre vai perder numa disputa de forças paralelas).
