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
