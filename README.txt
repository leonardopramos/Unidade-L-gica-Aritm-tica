Nomes: Leonardo Preczevski Ramos, Matheus Machado Berwaldt, Davi Oliveira Paris Nunes

Exemplos de funcionamento da ULA

ADD - Se quisermos somar dois valores na ULA, precisamos, primeiramente, colocar nos registradores A e B os valores em oito bits e passar para o multiplexador(mux) a entrada da adição, que 
é a porta 4, para isso, é preciso passar para o seletor o valor 1 1, referente a quarta porta. Após isso está pronto, só precisamos dar 8 sinais de clock para a ULA e ela 
irá fazer toda a soma sozinha.

SUB - Para que seja possível realizar subtração na ULA, precisamos, assim como na adição, colocar os valores nos respectivos registradores A e B, e selecionar a porta 
da adição no mux passando para o seletor 1 1 referente a quarta entrada, porém, será preciso fazer dois passos a mais para que seja possível realizar a operação. Para 
subtrair dois valores, basta somar o primeiro com o segundo valor negativo, e é isso que precisaremos fazer aqui. Para transformar um valor binário em negativo precisamos
inverter ele, o que é 0 vira 1 e vice-versa e adicionar mais um bit. Para fazer isso na ULA, precisamos ligar o B inverte, passando para ele o valor 1 e também adicionar
colocar no carry o valor 1, assim, invertendo o B e adicionando 1 para ele. Logo após isso é so dar 8 sinais de clock para a ula e ela funcionara perfeitamente.

AND - Para usar a porta lógica AND, é necessário selecionar no mux a primeira porta lógica, referente a porta AND, passando no seletor o valor 0 0 e passar para os 
registradores A e B, seus respectivos valores. Após isso é so dar 8 sinais de clock para a ULA funcionar.

OR - Para usar a porta lógica OR é necessário passar para o seletor do mux o valor 0 1 referente a porta lógica or, e registrar nos registradores A e B os seus valores 
em 8 bits. Logo após é so dar 8 sinais de Clock para a ULA.

NOT - Para o fazer o NOT, precisamos fazer algumas operações. Como o NOT é o inverso do valor, nós precisamos selecionar alguma função lógica onde, na tabela verdade, 
seja possível realizar essa inversão. Para isso, nessa ula, nos utilizamos o XOR, pelo fato de que na sua tabela verdade, ao por os valores 1 1 ele retorna 0, e os 
valores 1 0 ou 0 1, retorna 1, logo, ao fazer o XOR de um binário em 8 bits qualquer, com o binário 1111 1111 ele retorna o inverso, pois onde for 1 1 ele retorna 0 
e em qualquer outra situação ele retorna 1. Então para realizar o NOT, precisamos por no registrador B o valor a ser negado e no A o binário 1111 1111, após isso, 
precisamos passar para o seletor do mux o valor 1 0, para usar a porta lógica referente ao XOR. Feito isso precisamos dar 8 pulsos de clock para a ULA para que ela
funcione.

XOR - Para usar a porta lógica XOR é necessário selecionar no mux a terceira porta lógica, referente a porta Xor, passando no seletor o valor 1 0 e passar para os 
registradores A e B, seus respectivos valores. Após isso é so dar 8 sinais de clock para a ULA funcionar.

Exemplos de Uso:

1° Vamos levar em conta os valores 0010 0110 para A, ou 26 em hexadecimal, e 0001 1000 para B, ou 18 em hexadecimal, e vamos fazer sua soma e subtração.
Após por os valores nos registradores, eu coloquei no seletor do mux o valor 1 1 referente a 4 porta lógica, a porta da Soma e dei 8 sinais de clock para a ULA, após isso o 
valor retornado foi 0011 1110 ou 3E em hexadecimal; Depois de fazer a soma, foi feita a subtração dos dois valores, para isso foi ligado o B inverte, passando para ele o valor
 1 e colocamos no carry o valor 1 no primeiro clock, e apos os 8 clocks necessários para a ula funcionar ela nos retornou o valor correto de 0000 1110 ou 0E em hexadecimal.

2° Pegando os valores 0101 1100 para A, ou 5C em hexadecimal, e 0000 1100 para B, ou 0C em hexadecimal, vamos realizar a soma e subtração dos dois.
Após por os valores nos registradores, eu coloquei no seletor do mux o valor 1 1 referente a 4 porta lógica, a porta da Soma e dei 8 sinais de clock para a ULA, após isso o 
valor retornado foi 0110 1000 ou 68 em hexadecimal; Depois de fazer a soma, foi feita a subtração dos dois valores, para isso foi ligado o B inverte, passando para ele o valor
 1 e colocamos no carry o valor 1 no primeiro clock, e apos os 8 clocks necessários para a ula funcionar ela nos retornou o valor correto de 0101 0000 ou 50 em hexadecimal.

3° Vamos pegar 2 valores para B e vamos anular os bits 4 mais significativos e os menos significativos de ambos, vamos considerar os valores 1101 1011 e 1010 1101 para esse
exemplo. Para anular os bits mais significativos é necessário pegar para valor de A o valor 0000 1111 e a porta lógica AND, pois como na tabela verdade da AND, apenas o 
1 1 sera 1, então ao por no a um valor com os 4 bits mais significativos como 0 e os 4 menos significativos como 1, ele vai anular os 4 mais significativos e deixar os menos 
significativos normal. Já para anular os menos significativos é a mesma lógica, só muda o valor de A, que será 1111 0000, assim anulando os menos significativos.
Na ULA, será necessário por no seletor do mux o valor 0 0 e por no A o valor 0000 1111 para os mais significativos e dar 8 sinais de clock. Após isso o valor retornado de ambos 
é 0000 1011 e 0000 1101 e para os menos significativos sera necessário por no seletor do mux o valor 0 0 também, mas no A sera o valor 1111 0000 e dar 8 sinai sde clock
apos isso o valor retornado sera 1101 0000 e 1010 0000.

4° Para exemplo de OR vamos pegar os valores 99 e FF em hexadecimal, que em binario são, respectivamente 1001 1001 e 1111 1111 e vamos aplicar OR neles. 
Para isso, precisamos por no seletor do mux o valor referente a porta logica OR, que é o valor 0 1. Após isso, vamos por no registrador A o valor 1001 1001 e no registrador B 
o valor 1111 1111. Após selecionado a porta logica do OR e passado os valores pára os registradores, vamos dar 8 sinais de clock na ULA. 
O resultado aprensentado sera 1111 1111 pois na tabela verdade, para o resultado ser 1, basta que algum dos valores tenham 1, e como o FF é 1111 1111, o resultado sera ele mesmo.

5° Para outro exemplo de OR vamor pegar os valores 0110 0110 e 1001 1001, que respectivamente são 66 e 99 em hexadecimal. 
Vamor selecionar no seletor do mux a porta logica do OR que cujo valor é 1 0 e passar para os registradores A e B os respectivos valores citados acima. Apos isso vamos dar 8 sinais 
de clock na ULA e ela nos retornara 1111 1111, pois como ja explicado, na tabela verdade do OR basta que algum dos valores tenham 1 que será 1.


6° Agora vamos pegar para B os valore 1010 1111 e 0110 1011 e vamos negar eles, como explicado anteriormente, precisamos por no registrador A o valor 1111 1111 para que seja possível 
negar o valor desejado e, no mux, escolher a porta lógica XOR. Então vamos por no seletor do mux o valor 1 0 para selecionar a porta lógica referente ao XOR, por no registrador A o valor
1111 1111 e vamos por no registrador B o primeiro valor, apos isso vamos dar 8 sinais de clock. Logo apos vamos por o segundo valor em B e por no A o valor 1111 1111 e dar novamente os
8 sinais de clock, não é necessário selecionar novamente a porta logica XOR, pois ela está selecionada.
Feito isso, o primeiro valor retornado sera 0101 0000 e o segundo sera 1001 0100.


7° Para exemplo de XOR vamos pegar os valores 99 e FF em hexadecimal, que em binario são, respectivamente 1001 1001 e 1111 1111 e vamos aplicar XOR neles. 
Para isso, precisamos por no seletor do mux o valor referente a porta logica XOR, que é o valor 1 0. Após isso, vamos por no registrador A o valor 1001 1001 e no registrador B 
o valor 1111 1111. Após selecionado a porta logica do XOR e passado os valores pára os registradores, vamos dar 8 sinais de clock na ULA. 
O resultado aprensentado sera 0110 0110 pois na tabela verdade do XOR, se for 0 0 ou 1 1, o resultado sera 0. Para ser 1 é preciso que seja 1 0 ou 0 1.













