# Multiprocessing

### Tightly Coupled Configuration
> Uma única imagem do z / OS com dois ou mais CPs que compartilham o mesmo armazenamento, canais e dispositivos centrais é fortemente acoplada. Um único programa de controle ou sistema operacional gerencia recursos e atribui tarefas. Os PCs estão fisicamente conectados um ao outro e são capazes de se comunicar através de um mecanismo de interrupção.

> Se você estiver executando um sistema Tightly coupled e um processador falhar, o processador que estiver tentando conversar com o processador com falha entrará em um loop de rotação. Isso pode ser recuperado pelo operador ou por software automatizado, e o programa de controle tentará continuar trabalhando nos processadores restantes. Este trabalho continuará, mas em um estado degradado, até que o processador com falha esteja novamente online.

### Loosely Coupled Configuration
> Dizem que duas ou mais imagens do z / OS com seu próprio armazenamento central, CPs e canais que compartilham dispositivos são loosely coupled. Uma configuraçãoloosely coupled possui mais de um CPC que compartilha DASD, mas não canais ou armazenamento central.


### Parallel Sysplex
> è o mode de acomplamento ao qual loosely coupled trabalham em conjunto para processar o trabalho. Ele possui uma fonte de tempo comum chamada de sysplec timer que sincroniza os relógios da do dia em vários CPCs, um caminho de comunicação chamado coupling facility(CF) e um condiguration database (the couple data sets).

> O objetivo é alcaçar um sistema fortemente acomplado (tight coupled) com o poder de processamento de um fracamente acoplado (loosely coupled).
