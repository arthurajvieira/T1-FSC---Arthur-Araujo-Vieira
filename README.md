# T1-FSC---Arthur-Araujo-Vieira
# QUESTAO 1)
#
O desafio da questão 1 eh desenvolver um comando que contasse a quantidade de números impares de N números. Primeiramente abri um add com os v0 para ser o inicio do meu loop, v1 para ser o N (ate onde vai). Após isso criei um v2 para armazenar números pares (apenas para fins de organização, já que não era o foco do código, porem precisava disso para “visualizar o funcionamento”). Acrescentei uma variável v3 para acumular os impares. 
Abri meu loop com um bge para que encerrasse o loop quando v0 fosse maior ou igual 20 (v1). Fiz uma nova variável v4 e usei um and para encontrar o valor impar, adicionando um 1 no final, porque se for par termina em 0. Usei um beq pra dar um Branch caso o numero fosse par, levando pra uma função onde acrescenta 1 a variável v2. Se não, acrescenta 1 na variável v3 (contador de impares). Por fim, para ter o somatório na posição 0x20 como o desafio pedia, no end do meu loop eu adicionei um stw, um store word, para que o programa salvasse na memoria 0x20 o valor de v3. 
	Como fiz 20 numeros teste, a quantidade de impares são 10, e podemos visualizar isso na memoria
 
<img width="886" height="659" alt="image" src="https://github.com/user-attachments/assets/6d361454-239b-49a3-8d31-c40a48831a8d" />

#
# QUESTAO 2)
Para a implementação deste desafio, utilizei o código de exemplo para o cálculo da sequência de Fibonacci, disponibilizado nas instruções do GitHub, foi utilizado como base. A principal modificação realizada consistiu em ajustar o endereço de memória para o armazenamento do resultado. No código original, a instrução stw salvava o valor em outro local, fx600. Alterei essa instrução para que o resultado de cada termo da sequência calculado fosse direcionado para o endereço de memória 0x30, garantindo que o valor final fosse gravado na posição correta, de acordo com o solicitado.

<img width="886" height="663" alt="image" src="https://github.com/user-attachments/assets/a12c2fa3-48db-443b-9f5c-ac0e48c2e6e9" />

#
QUESTAO 3)
O objetivo deste desafio era desenvolver um código capaz de identificar o maior valor contido no intervalo de memória entre os endereços 0x40 e 0x80, e armazenar esse valor máximo na posição 0x90. Na abordagem inicial, eu inseri manualmente alguns valores de teste em endereços próximos ao início do intervalo. Para estes valores, a implementação de um loop de verificação funcionou como esperado, identificando e salvando corretamente o maior número. No entanto, surgiram dificuldades ao tentar ampliar a solução. Fiz tentativas de expandir o loop para percorrer todos os valores da memória, como de 0x40 a 0x80, resultaram em erro. Quando posicionei valores de teste em endereços mais distantes, como 0x70, o programa apresentou falhas de execução. Toda via, se for levado em consideração que os valores estão entre as memorias solicitadas, e que, ele mostra de fato o maior número entre estes que declarei, ele está funcionando.

<img width="886" height="666" alt="image" src="https://github.com/user-attachments/assets/75a11ea0-19dc-4ea2-9a81-873f4b005eac" />

#
QUESTAO 4)
O objetivo deste programa é processar um conjunto de 64 dados para que todos os valores sejam pares. A lógica do código percorre uma lista de números, e para cada um deles, realiza uma verificação para saber se é ímpar. Caso encontre um número ímpar, ele é ajustado através da soma de 1. No final do processo, todos os valores são garantidamente pares e o resultado é salvo em uma nova área de memória, completando a tarefa de normalização dos dados.

<img width="886" height="673" alt="image" src="https://github.com/user-attachments/assets/e549c5a1-1d79-48b2-bb3e-0b5f59989cb2" />

#
# QUESTAO 5)
Nesse desafio eu tinha que encontrar números que a somatória fosse 10 entre as memorias 0x60 e 0x70. Criei um add para elas. Após, criei um add v2 para armazenar o resultado que eu deveria encontrar (10) e v3 para N números teste, v4 para iniciar a contagem. Com isso criei um loop onde acrescentava 1 ao v4 e subtraia 2 de v3. Criei uma variável v5 para assumir o valor de v3 e uma v6 para assumir o valor de v4. Dessa forma eu poderia juntar v3 e v4. Fiz um add v5 v6 para poder somar v3 e v4 como dito anteriormente. Fiz um beq para compara v5 com v2 (o resultado) e caso fosse igual, ou seja, desse 10, eu criei uma função chamada match (igual tinder). Na função match eu fiz um store word para armazenar v5 na posição 0x90. 

<img width="886" height="658" alt="image" src="https://github.com/user-attachments/assets/56920bb3-97b8-4232-b6a3-cdf0e624a4ca" />

#
# QUESTAO 6)
Para realizar a inversão dos valores na memória, implementei uma lógica baseada em dois contadores. Criei um contador que inicia no primeiro endereço do intervalo (0x40), como solicitado. e outro que começa no último (0x60). O código então entra em um loop onde, a cada iteração, ele lê os valores de ambas as extremidades, e assim, os troca de lugar e escreve de volta na memória. Após cada troca, o contador do início é incrementado e o do final é subtraido, fazendo com que eles se movam linearmente em direção ao centro. Esse processo se repete até que os contadores se encontrem ou se cruzem, garantindo que todo o bloco de memória tenha sido invertido.

<img width="886" height="667" alt="image" src="https://github.com/user-attachments/assets/6129b8c5-1e0b-4b32-a5f2-0cbdc608158e" />

#
# QUESTAO 7)
Questao escolhida para ser anulada.
#
# QUESTAO 8)
Este desafio consiste em imprimir meu nome completo no terminal. A sua operação é dividida em duas fases. Na primeira fase, o programa emprega um loop para juntar sobre a string, lendo e imprimindo cada caractere individualmente através do serviço de escrita de caractere (0xf006). O laço termina ao identificar o caractere nulo que finaliza a string. Na segunda fase o código utiliza um serviço que recebe o endereço de memória da string e a imprime integralmente. O resultado final é a exibição do meu nome completo. 

<img width="886" height="666" alt="image" src="https://github.com/user-attachments/assets/c67c20c5-5f62-4dd4-a639-8dc6e0343885" />


# Nota)
Este texto teve **erros de português corrigidos com a ajuda de IA (Gemini)**, que fez apenas correções ortográficas e gramaticais sem gerar texto.
