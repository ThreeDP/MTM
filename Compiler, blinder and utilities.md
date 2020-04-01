### Blinder
> Muitos programas chamam rotinas locais ou providas pelos sistema para adquirir memoria, executar ações de I/O e muitos outros motivos, o blinder assegura que essas ligações entre rotinas funcionem corretamente no tempo de execução.

![Exemplo](https://github.com/ThreeDP/MTM/blob/master/img/compiler%20blinder%20utilities/img02.png)
![Exemplo](https://github.com/ThreeDP/MTM/blob/master/img/compiler%20blinder%20utilities/img01.png)
 > O fichário carrega programas e rotinas das bibliotecas de objetos na memória de ponta a ponta e, em seguida, resolve as referências externas em cada seção, convertendo símbolos, como RTN02, em endereços, como 006800.

> A maioria dos programas não é executada após a edição do link. Em vez disso, eles são armazenados em um LOADLIB como módulos de carregamento. Eles podem ser chamados com o parâmetro PGM de uma instrução de controle de tarefa EXEC.

> O load module é como se fosse uma pre renderização do código com suas rotinas encaixadas em um unico código. E as chamadas das rotinas são semelhantes as usados no assemble pullado para a rotina e plando novamente para o código quando terminado a rotina.

### Utilities
> São programas usados para solucionar problemas tipicos de todos os ambientes z/OS.

**São divididos em dois tipos:**

Standalone utility:
> Usados quando o sistema z/OS não inicia ou não está diposnivel. São geralmente usados para recuperar o sistema ou seja quando fudeu.
  
  Alguns exemplos de iniciais:
  DASD e SADMP.
  
OS Controlled Utility:
> Outros programas utilitários são executados sob o controle do sistema operacional. Alguns operam no nível do volume, mas a maioria deles é usada para copiar, modificar, reorganizar ou comparar dados no conjunto de dados e no nível do registro.

  Alguns exemplos de iniciais:
  IEBCOPY
  IEBGENER or ICEGENER
  DFSORT
  IDCAMS
  ADRDSSU (DFSMSdss)

IEBGENER
> is used to print or copy a sequential data set.

IEBCOPY
> is used to reformat or copy a partitioned data set.

ADRDSSU 
> is used to backup and restore data sets. 

DFSORT 
> is used to sort the contents of a data set. 

IDCAMS 
> is primarily a VSAM utility but can also manipulate (delete, rename, copy, and dump) non-VSAM data sets.
