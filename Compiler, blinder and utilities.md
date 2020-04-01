**Blinder**
> Muitos programas chamam rotinas locais ou providas pelos sistema para adquirir memoria, executar ações de I/O e muitos outros motivos, o blinder assegura que essas ligações entre rotinas funcionem corretamente no tempo de execução.

![Exemplo](https://github.com/ThreeDP/MTM/blob/master/img/compiler%20blinder%20utilities/img02.png)
![Exemplo](https://github.com/ThreeDP/MTM/blob/master/img/compiler%20blinder%20utilities/img01.png)
 > O fichário carrega programas e rotinas das bibliotecas de objetos na memória de ponta a ponta e, em seguida, resolve as referências externas em cada seção, convertendo símbolos, como RTN02, em endereços, como 006800.

> A maioria dos programas não é executada após a edição do link. Em vez disso, eles são armazenados em um LOADLIB como módulos de carregamento. Eles podem ser chamados com o parâmetro PGM de uma instrução de controle de tarefa EXEC.
