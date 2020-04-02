# Channel Subsystem
> O channel recebe instruções do supervisor para executar funções que acessam dispositivos e os executa ou recebe informações de onde gravar os dados.

> O channel executa ações sem correlação com o processador, isso permite que o processador execute outras ações em espera enquanto o channel realiza as tarefas a ele atribuidas.


### Como funciona o Channel pro dentro do sistema z/OS
**User Program**
> O user program faz solicitações de entrada ou saida. Essas solicitações podem ser macros instrutions de GET, PUT, READ ou WRITE. A macro solicita o Acess method que interpreta as requisições e determina quais recursos serão destinados para a tarefa.

**Acess Method**
> O acess method executa as seguintes funções:
  
    - Cria o programa de canal, que contém instruções para o subsistema de canais
    - Implementa o buffer
    - Garante sincronização
    - Se houver uma falha, ele redirecionará automaticamente a solicitação de I/O

**EXCP Processor**
> O processador EXCP converte o programa de canal que recebeu do método de acesso em um formato que o subsistema de canal pode usar e chama os serviços do supervisor de I / O (IOS).

**IOS**
> 
O supervisor de I / O conectará a solicitação de I / O à fila apropriada do dispositivo de I / O, se já houver solicitações de I / O pendentes para este dispositivo de E / S e sinalize o subsistema de canais sobre o excelente trabalho.

> O processador central pode então processar outro trabalho enquanto aguarda a conclusão da I / O.
