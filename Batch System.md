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

