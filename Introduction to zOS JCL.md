# Estrutura de JOB JCL

**Operation**
> O campo de operação especifica que tipo de instrução JCL é. Podendo ser uma ação EXEC, DD ou JOB

**Name**
> O campo de nome atribui um identificador que pode ser referido por outras instruções ou pelo sistema.

> O campo nome pode ter de 1 á 8 caracteres que podem ser letras, números ou caracteres nacionais(#, @, $). O primeiro caracter sempre deve ser uma letra ou caracter nacional.

**Comments**
> Os comentários podem se estender à coluna 80 e permitir que você insira texto de forma livre que geralmente fornece uma descrição da atividade ou outras informações importantes.


**Parameters**
> Os parâmetros posicionais e de palavra-chave especificam detalhes sobre como a operação é executada.

**//**
> Os caracteres // identificam a linha como uma instrução JCL.

### The most common JOB Statement parameters

    [,REGION=value]
    
> Usado para especificar a quantidade de armazenamento que você irá encontrar

    [,PRTY=value]
    
> É usado para atribuir um grau de prioridade ao seu job.

    [,TYPRUN=value]
    
> É usado para especificar a ação tomada pelo job quando é submetido.

    [,LINES=(value,option)]
    
> É usado para definir um máximo de linhas para o output produzido pelo job e o segundo parametro defini a ação a ser tomada quando ultrapassar esse limite.

    [,CLASS=jobclass]

> É usado para especificar a classe em que o JOB será executado.

    [,RESTART=stepname]
    
> É usado para definir o ponto de partidar caso o programa seja reiniciado.

    [,TIME=(min,sec)]
    
> Define o tempo limit de espera até que o JOB seja executado.

    [,NOTIFY=userid]
    
> É usado especificamente para dar uma menssagem ao userid espeficicado quando o job foi completo.


