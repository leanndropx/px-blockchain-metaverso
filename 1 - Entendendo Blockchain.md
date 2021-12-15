# 1. Uma blockchain - conceitualmente - é:



1. Uma lista em crescimento contínuo de registros, chamados de blocos, que são ligados uns aos outros de maneira segura por meio de criptografia. 

2. Um livro de registros imutável, ou seja, nada que você cadastra ali pode ser alterado, sendo assim, é como se fosse um cartório, mas de forma completamente descentralizada e consequentemente com menos custos. Tudo o que se cadastra ali, ali permanecerá para sempre pois a dinâmica por trás da estrutura de uma blockchain não permite com que seus dados sejam alterados ou deletados. Esta dinâmica será explicada mais pra frente.

3. É uma nova maneira de armazenar e mover dados com segurança. Os dados consistem principalmente em transações que incluem mensagens trocadas entre duas partes. 

4. Qualquer coisa pode ser cadastrada em uma blockchain: transações, contratos - conhecidos neste ambiente como smart contrato - , registros de arte - conhecidos como NFT's, e por aí vai. 

   

5. Um bloco de uma blockchain é composto por um conjunto de 5 dados:

   

   1. **Número do bloco**
   2. **Conteúdo guardado no bloco**
   3. **Hash do bloco:**  é a identificação única, uma espécie de impressão digital de cada bloco, é um número de identificação dos dados com 64 digitos, em formato hexadecimal, ou seja, numeros e letras.  A escala hexadecimal vai de 0 a 16, ou seja, vai de zero a 9 com números normais, e depois entram as letas, a que vale 10, b que vale 11, c que vale 12 e assim vai até 16.
   4. **Hash do bloco anterior:** impressão digital do bloco anterior
   5. **Nonce:** number used once a time / número usado apenas uma vez - como se fosse uma senha usada por mineradores para adicionar um bloco na cadeia.

   

6. A principal ideia de um blockchain é: **registro de um acontecimento sem risco de alteração**, ou seja, imutável, e os dados informados acima fazem parte deste registro. 

7. Muitas pessoas logo associam blockchain somente com criptomoedas, mas, na verdade, ela pode ser usada para qualquer coisa que se precise registrar, um sistema de blockchain pode ser aplicado ao mercado de moedas apenas porque pode servir como para registrar todas as transações de troca de valores com segurança. 

8. Qualquer mercado que precise registrar com segurança trocas e transações poderá usar uma blockchain como livro de registros seguro. 

   

9. Registro de propriedades e registro de extração de diamantes são outros dois exemplos muito utilizados para a tecnologia blockchain

10. Qualquer situação que precise de registros sequenciais pode se beneficiar do uso da tecnologia blockchain, aliás, não só sequenciais, qualquer tipo de dado que precise ser gravado e que se espere a imutabilidade deles ao logo do tempo, pode ser beneficiado por uma blockchain

11. O bloco número 1 normalmente tem o nome Bloco Gênesis, porque ele da origem a blockchain como um todo

```
amount: 30
sender: Alice
receiver: Bob
```



# 2. Uma blockchain - tecnicamente - é:

1. Um dicionário com:
   1. Um ou mais variáveis contendo conteúdos
   2. Uma varivável contendo uma hash
   3. Uma variável contendo uma hash do bloco anterior
   4. Uma variável contendo um Nonce
2. Cada dicionário é um bloco diferente, ou seja, cada dicionário contém uma transação, que pode ser um smart contrat, ou uma transação de moeda, ou qualquer outra coisa



# 3. Para criar uma blockchain:

1. crie uma variável bloco com uma lista e um dicionário contido dentro que receba algum conteúdo

2. cria uma variável **blockchain** com uma lista vazia que irá receber cada um dos blocos mais tarde

3. defina uma função que receba a data atual usando a biblioteca datetime

4. defina uma função que criará a hash de cada bloco usando a biblioteca hash 

5. Este tópico está sendo estudado e ainda não está completo

   



# Uma blockchain é segura porque:

1. Porque quando alguêm tentar invadir para alterar o dado de algum bloco, automaticamente a hash daquele bloco é alterada também, e consequentemente a hash do bloco anterior também, e isso cria um efeito em cadeia de alteração de todos os blocos. A hash é única e completamente vinculada ao dado criado. 	
2. O que garante a segurança é o fato de que cada bloco de transação contém também hash do bloco anterior, ou seja, isso o vincula. 



# 2. O Hash SHA256

1. E um algoritmo desenvolvido pela NSA - Agência de Segurança Nacional dos Estados Unidos. 

2. E seguro e usado por inúmeras aplicações, como checagem de passaporte e armazenamento de senhas. 

3. O algoritmo não é fechado, ou seja, qualquer pessoa pode ler o código e entender como o algoritmo funciona

4. Então, ele é um algoritmo que vai criar um número com base hexadecimal de 64 digitos, e este número de 64 digitos vai ser único para aquele conteúdo e vai ser chamado então de **hash**

5. SHA = Secure Hash Algorithm e 256 = número de bits que ocupa na memória do computador. 

6. Quando se fala em blockchain, geralmente as pessoas associam a criptomoedas, mas o algoritmo funciona com qualquer tipo de documento digital, não apenas palavras ou textos, mas você pode criar hash para vídeo, você pode criar hash para áudio, arquivos executáveis, até um sistema operacional. 

7. O hash é um dos principais elementos de segurança de um blockchain, pois qualquer alteração mínima que você faça no conteúdo daquele bloco, automaticamente muda o valor da hash, e isso muda todos os outros blocos também, pois os blocos anteriores estão vinculados 

   

# 3. O livro razão imutável

1. A ideia de livro razão imutável é justamente para representar a ideia de que nenhum tipo de registro de dado dentro de cada bloco pode ser alterado, justamente pelas explicações do tópico de hash apresentado anteriormente. 

2. Qualquer situação que precise de registros sequenciais pode se beneficiar do uso da tecnologia blockchain, aliás, não só sequenciais, qualquer tipo de dado que precise ser gravado e que se espere a imutabilidade deles ao logo do tempo, pode ser beneficiado por uma blockchain.

3. Registro de propriedades e registro de extração de diamantes são outros dois exemplos muito utilizados para a tecnologia blockchain

   

# 4. A rede distribuída P2P

1. A rede distribuída também é outro elemento extremamente importante que garante a segurança de uma blockchain.

2. Computadores do mundo todo estão ligados a rede oficial da blockchain da Bitcoin por exemplo, todos eles tem uma cópia da blockchain original. Quando um hacker ataca algum desses computafores e altera algum dado, todos os outros computadores do mundo perceberiam essa alteração e mandariam novamente as informações originais para o bloco

3. Um hacker teria que atacar pelo menos 50% + 1 dos computadores ligados a rede ao mesmo tempo, por isso uma blockchain pode ser tão segura, pois isso é praticamente impossível. 

4. Quanto masi distribuída uma rede, mais segura ela será, já que mais computadores precisarão ser atacados ao mesmo tempo. É desta forma que a segurança é garantida em um sistema de falta de segurança, ou seja, a falta de confiança entre as pessoas é garantida por um sistema que verifica constantemente se há algumas alterações, e se houver, evita que alterações fraudulentas ocorram, já que os dados são sempre copiados conforme o original 

   

# 5. O Nonce e a criptografia

1. É o minerador quem coloca um cloco na rede, para isso, ele precisa realizar um processo computacional para encontrar o Nonce. Quando o nonce é encontrado, as transações são efetivamente gravadas em um novo bloco. O bloco é gerado de maneira automática pela mineração.

2. O minerador nada mais é do que um computador que está ligado na rede

3. O nonce é um número que é diretamente vinculado ao hash, como o hash pode se repetir e o nonce não, é o nonce que vai dizer 

4. nonce = number used once a time, ou seja, número utilizado apenas uma vez. 

5. Ele auxilia na criação do hash do próprio bloco

6. Ele é usado para mineração

7. No caso da mineração, a rede blockchain define automaticamente o valor alvo do hash da mineração 

8. A mineração então, consiste no minerador testar quais são os nonces possíveis em relação ao bloco que quer adicionar na blockchain, quem chegar primeiro ao Golden Nonce adiciona o bloco a blockchain e recebe a recompensa. 

   

