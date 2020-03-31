# História 
> De inicio o computadores IBM possuiam um problema com a integração de novos dispositivos de entrada e saida (I/O), a troca dos dispositivos para modelos diferentes nem sempre era bem sucedida por haver conflitos de compatibilidade, com a introdução da serie 360 esses problemas foram resolvidos através da intrudução do supervisor responsavel pelo gerenciamento de dispositivos.

*** 
> o supervisor possui a configuração desses dispositivos e faz o gerenciamento dos mesmos. Sendo assim o programas agora não tinham mais a necessidade de possuir suas proprias lógicas para dispositivos de entrada e saida, nesse caso eles necessitariam fazer uma chamada para o supervisor que seria o responsavel por se comunicar com os dispositivos o que é  representador por uma sepervisor call (SVC).

***
> O endereço do dispositivo é uam cambinação do endereço do canal, controlador da unidade e da unidade ( chanel, control unit and unit). Quando há a necessidade do supervisor ler ou escrever algum dado ele passa uma serie de instruções para o channel que por sua vez ordena que as operações sejam executadas pelo control unit que inicia as ações no dispositivo (unit).
O supervisor também tem a responsabilidade de armazenar o status das operações executadas, sucesso ou erro, e interroper o supervisor para informar o termino das operações.

**Multiprogramming**
> Foi introduzida para sanar o tempo em que a CPU espera até enquanto operações são realizadas.
Para criar um ambiente de multiprogramming a central storage foi divididas em regions cada uma delas executando ações diferentes.
***
> Com a introdução da multiprogramação de inicio um grande problema foi que regiões diferentes não poderiam acessar um mesmo dispositivo, o que poderia ocasionar erros, gerando assim a necessidade de dispositivos individuais para cada região. O SPOOL veio para solucionar esse problema, que seria basicmente um data set para gerenciar as operações a serem feitas nos dispositivos.

> O supervisor atribui ao JES todas as ações para dispositivos I/O que por sua vez armazena todas as ações no data set SPOOL com um nome de job retirado do JCL e um numero unico.

> Quando alguma região fica disponivel a JCL le o SPOOL e o programa indicado começa a ser executado. Quando o programa tenta gravar em uma impressora, o supervisor reconhece que a solicitação é para um dispositivo em spool. Ele passa a solicitação para JES, que desvia o registro de saída para um conjunto de dados em spool.

> As informações de status são passadas primeiro ao JES, caso seja necessário um ajuste antes de serem entregues ao programa. Uma técnica semelhante é usado quando um programa tenta ler ou escrever cartões.
# Temas importantes

> Depois que as listagens de programas foram gravadas no spool, o JES pode direcioná-las para as impressoras automaticamente.

> Os operadores podem emitir comandos para o JES para controlar a direção das listagens e garantir que o processo de impressão seja suave e eficiente.

Sendo assim o JES fica responsável por indicar em quais dispositivos serão feitas as leituras ou escritas e o SPOOL fica respósavel por armazenar os pedidos de leitura e escrita do programas tendo como uma especie de ID um numero unico e os seus nomes.

> A introdução do spool trouxe muitas vantagens, incluindo o fato de que agora as imagens dos cartões podiam ser recuperadas do spool, para que os perfuradores dos cartões não fossem mais necessários.

1. Supervisor
2. Spool
3. IPL


# Glossary

**1. SYSRES:**
> The system residence volume.

**2. SVC:**
> The mnemonic fot the superviso call machine instruction.

**3. IPL ( Initial Program Load:**
> The process that loads the system programs from the system auxiliary storage, checks the system hardware, and prepares the system for user operations.

**4. SPOOL ( Simultaneous Peripheral Operations ON-line.):**
> Also SPOOL. Simultaneous Peripheral Operations On-Line. The mechanism by which card and print records can be stored on disk, allowing jobs to be run or listings to be printed at times chosen by an operator.

**5. VDU:**
> A visual display unit.
