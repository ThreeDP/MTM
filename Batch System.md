# Aprendizado

**In this module, you will discover how the IBM enterprise environment is built to enable maximum batch processing in major corporations.**

> After completing this module, you will be able to:

- Identify the Function of Job Entry Subsystem (JES)
- Identify How Job Control Language (JCL) Controls the Running of a Program
- Define Batch Processing
- Define System Display and Search Facility (SDSF)


### Processamento Batch
> Batch são tarefas executadas em segundo plano e não são componentes visiveis, eles atuam quando um gatilho de um sistema online, IMS e CICS, é ativado ou em um periodo de tempo programado.
    
    Por exemplo:
    A cada hora, dia ou mês.
    
![](https://github.com/ThreeDP/MTM/blob/master/img/Batch%20system/1.png)

**JES - Job Entry Subsystem**
> O sistema z/OS prove duas opções para subsistemas de processamento em lote. Os dois foram desenvolvidos em 1960 e fornecem scheduling of execution and spooling.

- spooling: refere-se a um processo de transferência de dados colocando-os em uma área de trabalho temporária onde outro programa pode acessá-lo para processá-lo em um tempo futuro.

JES subsystem é inicidado como uma tarefa executada no z/OS e controla scheduling, prioridades, entradas e saidas de jobs.
> Essas tarefas incluem processos de execução demorada, geralmente considerados tarefas em lote, e subsistemas que podem ser executados como tarefas, incluindo CICS, DB2, UNIX Systems Services e outros processos intrínsecos.

![](https://github.com/ThreeDP/MTM/blob/master/img/Batch%20system/2.png)

Os jobs são enviados para o JES e dependendo dos parametros dos jobs como classes e prioridade podem tomar rumas diferentes como:

        executa-los imediatamente
        aguardar disponibilidade de recursos
        rejeitar por informações incorretas
        
O JES irá garantir que o Job seja executado, irá monitorar sua execução e irá manipular sua saida.

![](https://github.com/ThreeDP/MTM/blob/master/img/Batch%20system/3.png)

**Atrasvés do JCL definimos jobs para o z/OS. o Job Control Language (JCL) é composto de instruções alttamente estruturadas como:**

- Indentifica o trabalho e sua informações, prioridade e agenda.
- Define o programa ou processo a ser executado.
- Define os recursos que serão usados para a execução do programa, por exemplo conjunto de datasets.
- Define as condições para controlar o fluxo do trabalho.

![](https://github.com/ThreeDP/MTM/blob/master/img/Batch%20system/4.png)

**A JCL é exclusiva para o ambiente de mainframe IBM. O exemplo acima é a JCL que é armazenada em um membro de um conjunto de dados particionado e contém:**

![](https://github.com/ThreeDP/MTM/blob/master/img/Batch%20system/5.png)

- Uma instrução JOB que descreve as características do trabalho no sistema
- Uma etapa chamada STEP1 que chama o programa IDCAMS
- Uma etapa chamada STEP2 que chama o programa CYBB002

As instruções são executadas sequencialmente, o que significa que o STEP2 não pode ser executado antes que o STEP1 seja concluído.

![](https://github.com/ThreeDP/MTM/blob/master/img/Batch%20system/6.png)
![](https://github.com/ThreeDP/MTM/blob/master/img/Batch%20system/7.png)

