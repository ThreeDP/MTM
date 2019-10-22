# BAIXANDO E INSTALANDO SEU EMULADOR:
> Antes de começarmos os desafios da maratona master the mainframe precisamos realizar algumas configurações básica. Uma delas é a instalação do emulador:

Nesse link estão os passos a serem seguidos de acordo com seu sistema operacional:
http://mtm2019.mybluemix.net/connectivity_guide/connectivity_guide_software.html

# COMANDOS

**=. ou Return ou press F3**
> Retorna para a tela inicial do emulador.

**=(qualquer seguencia de numeros)**
> Irá acessar um determinada aba a partir da tela inicial. Exemplo: =3.2 Primeiramente será acessado a aba utilities e logo após a aba data set.

**u + Enter**
> Apertando u e dando enter no menu principal o unix shell é acessado.

**x + Enter**
> 


# ACESSO

**IBM ACADEMIC**
https://academic.interskill.com


# ESTUDO DOS TERMOS

**Data set**
> São semelhantes a arquivos. Data set são um conjunto de dados.

**Catalog**
> è um data set que possui informações sobre outro data set, isso inclui tipo, tamanho e formato.

**Master Catalog**

![Explicação sobre master catalog:](https://github.com/ThreeDP/MTM/blob/master/img/datamanagement/1.png)

**RACF**
> É uma ferramenta que define as regras de segurança e de SMS (Storage Management System). O RACF determina por exemplo as regras de acesso de alguns usuários ou de um grupo de usuarios e o SMS determina as regras de alocação do data set.

**Atributos do data set**

![Explicação sobre master catalog:](https://github.com/ThreeDP/MTM/blob/master/img/datamanagement/2.png)

**DASD (Direct Access Storage Device)**
> É como a IBM se refere ao seu armazenamento online ao invez de chama-los somente de disco.

# Armazenamento

Em uma variavel os 4 primeiros bytes de toda a gravação são reservados para identificar o comprimento dos dados alocados.

**Proposta de cada formato flat files**

![Explicação sobre master catalog:](https://github.com/ThreeDP/MTM/blob/master/img/datamanagement/4.png)


### Basic

**QSAM**
>

**PDS - Partitioned Data Set**
> Contém em ordem membros com nomes unicos de até 8 caracteres e tem todas as caracteristiras de um flat file, porém todos os membros possuem o mesmo atributo. Ele é usado para administrar necessidades de um grupo em comum de usuários.

        A função DTRAIN.SOURCE.CNTL é usada para listar os membros de um PDS
        
        A função DTRAIN.SOURCE.CNTL(NOME_MEMBRO) para acesso individual de um membro.
        
> PDS é usado para organizar codigos fontes e executavels que são necessarioas para executar aplicações em um sistema empresarial. Exemplos de tupos de codigos e modulos que contem em um extrutura PDS são: COBOL, SOURCE, COPY, JCL and LOADLIB(executavel).
__________________________________________________________________________

> Em uma estrutura PDS usamos referencia a librarias para organizar grupos de prodution ou application e um sistema de RACF é usado para limitar o acesso, autorizar acesso ou modificações.

**VSAM - Virtual Storage Access Method**
>  É referente á um metodo de acesso direto á um dado, ou um processamento direto, dados que podem ser acessados diretamente são key, record number, sequencial processing of fixed e variable length records.

Alguns formatos que suportam esse acesso são:

        Key Sequenced Data Set (KSDS)
        Relative Record Data Set (RRDS)
        Entry Sequenced Data Set (ESDS)
       
> O VSAM é usado para armazenar na memoria dados para um acesso direto e mais rápido. 

**DBMS**
> Gerencia e controla o acesso as discos de armazenamento.

        Gerencia das seguintes formas:
        - Controle de concorrencia:
        gerencia o a leitura e atualização dos dados que são feitas por aplicações e threads para que não ocorra inconsistencia de dados.
        - Segurança dos dados:
        Controla os acessos, permições e operações realizadas nos dados para que soomente que tenha permição possa acessar.
        - Recuperação e manutenção de logs e backups, permitindo a recuperação em um momneto anterior ao desaastre.
       
A IBM tem dos systemas de banco de dados que provem essas funcionalidades o IMS e o DB2. 

![Explicação sobre master catalog:](https://github.com/ThreeDP/MTM/blob/master/img/datamanagement/5.png)

![Explicação sobre master catalog:](https://github.com/ThreeDP/MTM/blob/master/img/datamanagement/6.png)
       
### Database

**IMS/DB**
>

**IDMS**
>

**DB2**
>

### Offiline

**CART**
>

**HMS**
> 

### Access Methods (AM)

    BSAM - Basic sequential
    QSAM - Queued sequential
    VSAM - Virtual storage
    BDAM - Basic direct
    BPAM - Basic partitioned
    
    
### Flat Files

![Explicação sobre master catalog:](https://github.com/ThreeDP/MTM/blob/master/img/datamanagement/3.png)


