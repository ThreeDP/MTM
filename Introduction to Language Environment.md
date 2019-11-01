### LE : Language Environment

Linguagens combiladas como COBOL, C e PL/1 precisão de dois componentes. Um compiler que é usado para criar executaveis. E um runtime que são alguns modulos usados para dar suporte na execução de um programa.


### The Runtime environment
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/1.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/2.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/3.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/4.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/5.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/6.png)

**Conflito entre compilers e runtimes** 
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/7.png)

**Runtime libraries comuns para todos os compilers de cada determinada linguagem**
O LE é um componente do sistema z/OS.
Ele é um Runtime que fornece ferramentas para todas as linguagens.

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/8.png)

**Personalizando o ambiente de processamento LE**



Independete de onde o programa é executado: in batch, CICS, IMS, UNIX ou TSO os programas atuais sempre irão rodar via Language Environment.

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/9.png)

No entando nem todas as linguagens usam o LE.
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/10.png)

Programas Assembler executam independete de um ambiente de runtime, e não precisam usar LE. No entando LE provem macros para executar programs assembler.

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/11.png)


**Language Environment separa o processo em processes, enclaves e threads**

Processes
> No sistema z/OS um process é equivalente a uma tarefa, uma transação CICS, uma transação IMS e um processo z/OS UNIX são processes LE.

Enclave
> Um enclave é um grupo de programas e subrotinas usadas para fazer alguma coisa juntas. COBL run units, C code within a main() statement, and code within a PL/I Procedure statement are all enclaves.

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/12.png)

Thread
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/13.png)


O Language Environment oferece serviços opcionais que podem ser chamados a partir de programas do usuário.

**Language Environment possui serviços que podem ser chamados em programas**
> Esses são:

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/14.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/15.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/16.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/17.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/18.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/19.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/20.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/21.png)

Esse serviços podem ser chamados por qualquer linguagem exceto Fortran.

[Todos esses serviços podem ser encontrados no Manual de Referencias LE](https://github.com/ThreeDP/MTM/blob/master/Manuais/Language%20Environment%20Programming%20Reference.pdf)

**Chamando funções LE em C**
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/22.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/23.png)

**Chamando funções LE em COBOL**
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/24.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/25.png)

**Chamando funções LE em PL/I**
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/26.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/27.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/28.png)


**Parametros para customizar o processamento na LE**

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/30.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/31.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/32.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/33.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/34.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/35.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/36.png)

### Stack storage ou runtime stack
> É alocado quando uma thread é criada pelo LE. Uma pilha(stack) inicial é alocada e isso pode ser adicionado pelo LE, conforme necessário. A pilha é liberada quando o encadeamento é finalizado.
________________________________________________________
> É usada para armazenar informações de ligação do módulo, salvamentos, variáveis automáticas C e PL / I e COBOL LOCAL-STORAGE. Cada thread tem sua própria pilha.

### Heap storage
> Um armazenamento Heap é usado por programas como COBOL WORKING-STORAGE, C malloc, requested storage, and PL/I ALLOCATE. É normalmente solicitado e é compartilhado entre dos os threads de uma enclave.
________________________________________________
O armazenamento Heap é liberando expecificamente pelo programa ou quando a enclave termina.

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/37.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/38.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/39.png)

# Condições
> UM LE condition é um evento que requer a atenção do programa em execução. pode ser um erro ao abrir um dataset ou uma chama incorreta para um serviço do language Environment.

Exemplo:

    Por exemplo, um programa C pode chamar a função raise () ou um programa PL / I a instrução SIGNAL. Os programas também podem chamar a função LE CEESGL para criar uma condição.
    
> Cada condição tem uma gravidade. Alguns podem ser graves, exigindo o término do Enclave. Outros podem ser informativos ou de aviso, onde o programa pode continuar processando.

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/40.png)

> o LE fornece condições(condition) para tomar ações programadas quando um erro ocorrer. Quando um erro ocorre o LE irar realizar uma pesquisa das condition existentes entre todos os programas ativos atualmente partindo da ultima chamada até a primeira, se nenhuma condition for encontrada, o tratamento padrão será executado.

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/41.png)

**Quando uma condição ocorre e uma mensagem é enviada onde ela é alocada?**

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/42.png)

- Caso esteja sendo executada no CICS a messagem será gravada no diretorio transitorio CESE.
- Caso o LE MSGFILE esteja configurado um DD (data set) especifico irá armazenar a menssagem.
- Caso contrário as mensagens serão gravadas no DD SYSOUT.

### sessões de uma messagem de Language Environment

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/43.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/44.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/45.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/46.png)

**Problemas Graves**

[Manual para casoso graves](https://github.com/ThreeDP/MTM/blob/master/Manuais/MVS%20System%20Codes.pdf)

> Em casos graves o sistema pode dicidir abandonar o processo. Depois do abandono o sistema mostra uma mensagem com o código do erro.

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/47.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/48.png)

**Abandono Usuário**
O Usuário pode decidir abandonar se encontrar algum erro, nesse caso o sistema indicara um abandono anormal do usuário os códigos de abandono do usuário começão com U e parte de 4012 esse codigos podem ser encontrados [no Language Environment Programming Reference](https://github.com/ThreeDP/MTM/blob/master/Manuais/Language%20Environment%20Programming%20Reference.pdf)

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/49.png)

O usuário pode abandonar um programa usando os codigos **LE CEE3ABD** or **CEE3AB2**, as outra linguagens podem ter seus proprios comandos para finalizar.

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/50.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/51.png)
Quando o sistema é interropido ele pode produzir um SVC dump que possui o diagnostico do problema.

**Formas de analisar dumps(diagnosticos de erros)**
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/52.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/53.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/54.png)

### LE dumps

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/55.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/56.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/57.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/58.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/59.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/60.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/61.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/62.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/63.png)

**Leitura de uma dump**

![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/64.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/65.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/66.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/67.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/68.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/69.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Introduction%20to%20Language%20Environment/70.png)
