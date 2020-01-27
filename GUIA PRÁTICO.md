# SIGLAS:

1. **TSO**
> Time Sharing Option, is a command line interface.

2. **ISPF**
> Interactive System Productivity Facility, is a text based interface.

3. **SDFS**
> System Display and Search Facility, is another text base interface.

# COMANDOS

### COMANDOS ISPF

**PREFIX**

    prefix *; owner z#####; st #exibi os status de todos os trabalhos do ID vinculado.

_______________________________________________________________

### COMANDOS SDSF

**XDC ------------------------------------------------------------------------------**

    xdc
    Comando dado dentro no SDSF na Coluna NP. Confira imagens.
    
![](https://github.com/ThreeDP/MTM/blob/master/MTM_img/xdc_01.png)

> The xdc action will write the output to a member name within a data set name
  Tab to Data set name input area and type p2.output - DO NOT enter yet
  Tab to Member to use input area and type #02 - DO NOT enter yet
  Tab to Disposition input area and type shr - Now you can enter
  
![](https://github.com/ThreeDP/MTM/blob/master/MTM_img/xdc_02.png)

**P --------------------------------------------------------------------------------**

    p (purge)
    comando dado no SDSF na coluna NP para fechar/ finalizar um job.

![](https://github.com/ThreeDP/MTM/blob/master/MTM_img/purge.png)
    
### COMANDOS TSO

**ISPF -----------------------------------------------------------------------------**

    ispf
    comando dado no painel de comando tso para voltar para a interface doo ispf.
    
![](https://github.com/ThreeDP/MTM/blob/master/MTM_img/tso_ispf.png)

**LISTC ----------------------------------------------------------------------------**

    listc
    Comando dado para mostrar uma lista atual de data sets. Mostra todos os seus data sets.
    
![](https://github.com/ThreeDP/MTM/blob/master/MTM_img/tso_list.png)

**NETSTAT HOME ---------------------------------------------------------------------**

    netstat home
    Mostra o IP do systema.
    
![](https://github.com/ThreeDP/MTM/blob/master/MTM_img/tso_net.png)

**TIME -----------------------------------------------------------------------------**

    time
    Mostra a data e a hora.
    
![](https://github.com/ThreeDP/MTM/blob/master/MTM_img/tso_time.png)
