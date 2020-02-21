# MENU ISPF

### Copiando Data Sets

**1. Copiar varios data sets simultaneos**
> A ação que quero tomar é simples, copiar todos os membros do data set SOW1.ISPF.ISPPROF para o data set SWO1.EXEC, para essa ação iremos utilizar o comando:

    co /
    *Onde co é ... e / é ...
  
> Na coluna Command do menu em frente ao data set que estão os arquivos que queremos copiar:

![Utilizando o comando co / na coluna command]()

> Feito isso o data set será aberto e seus membros serão exibidos! Para copiar um membro basta acrecentar um (s) á esquerda do membro que deseja copiar e um menu será aberto, falaremos sobre ele no proximo passo, porém queremos realizar a copia de todos os membros do data set em questão. Pensando nisso acrescentaremos em todos os membros que desejar copiar o comando (s).

![Selecionando todos os membros para copia]()

> Em seguida iremos adicionar o data set de destino, no caso o swo1.exec, e daremos um nome ao primeiro data set da seleção, o ideal é usar o mesmo nome para que seja uma copia exata do outro data set, e daremos enter. Automaticamente todos os outros membros serão copiados com seus respectivos nomes e dados para o data set de destino. Ai é só ir conferir!!

![Atribuindo data set de destino]()
![Sucesso da copia]()
