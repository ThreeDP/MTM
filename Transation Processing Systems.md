### Transation

**ACID**
> Transações ACID tem uma execução isolada, isso significa que apesar de ocorrerem transações em um mesmo tempo os dados que cada uma está manipulando não pode ser alterado por nenhuma outra transação ou qualquer ação do sistema.

- As transações ACID são ideais para lidar com o mundo real de volumes, taxas de transação e simultaneidade muito altos, mas algumas restrições devem ser aplicadas.

- As transações ACID devem ter um curto espaço de tempo, pois bloqueiam recursos e impedem a execução de outras transações por esse período.

- As transações de ACID não devem ter um escopo muito grande. Eles não devem tentar atualizar um banco de dados inteiro quando uma linha por vez é possível.

![Explicação sobre master catalog:](https://github.com/ThreeDP/MTM/blob/master/img/Transation_Processing_Systems/1.png)

*Relax isolation*
> É uma forma de evitar deadlock em momentos em que duas transações tentam acessar o mesmo recurso.

![Explicação sobre master catalog:](https://github.com/ThreeDP/MTM/blob/master/img/Transation_Processing_Systems/2.png)

**Sistemas de Gerenciamento de transações**
> 

![Explicação sobre master catalog:](https://github.com/ThreeDP/MTM/blob/master/img/Transation_Processing_Systems/3.png)

*Tipos de Sistemas*
**IMS DC (agora IMS TM)**
> a comunicação entre programas com IMS pode ser feita por uma interface de linguagem ou por uma chamada de API DL/I.

Interfaces DL/I especificas são indicadas para linguagens de programação especificas ou também podemos usar dois modelos genericos CEE ou AIB.
  
    Interfaces para cada linguagem:
    
                      | CEETDLI   # generica
    COBOL ------------| CBLTDLI   # interface mais indicada
                      | AIBTDLI   # generica
    
                      | CEETDLI   # generica
    Assembler --------| ASMTDLI   # interface mais indicada
                      | AIBTDLI   # generica
                      
                      | CEETDLI   # generica
    PL/I -------------| PLITDLI   # interface mais indicada
                      | AIBTDLI   # generica
                      
                      | CEETDLI   # generica
    C ----------------| CTDLI     # interface mais indicada
                      | AIBTDLI   # generica
                      
                      | CEETDLI   # generica
    PASCAL -----------| PASTDLI   # interface mais indicada
                      | AIBTDLI   # generica


    Outras linguagens -----------| AIBTDLI  
                                 | CEETDLI                         
    
                      
**CICS (agora CICS Transation Server)**
> É usado para acesso e gerenciamento onine de dados em banco de dados IMS DB, DB2 ou data sets nativos como VSAM.

![Explicação sobre master catalog:](https://github.com/ThreeDP/MTM/blob/master/img/Transation_Processing_Systems/4.png)

WebSphere Aplication Server
