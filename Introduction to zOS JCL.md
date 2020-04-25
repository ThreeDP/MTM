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

