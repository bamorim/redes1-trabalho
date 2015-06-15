# Database Service (trove)

Trove é um "Database as a Service" (Banco de Dados como Serviço) que provisiona bancos de dados relacionais e não-relacionais. Os serviços do trove são: API, taskmanager, guestagent e conductor.
* API: A api do Trove oferece uma API RESTful que suporta JSON e XML para provisionar e gerenciar instâncias Trove.
* Taskmanager: Provisiona instâncias, administra os ciclos de vida das instâncias e faz operações na instância do Banco de Dados.
* Guestagent: é um serviço que é executado dentro da instância do guest, responsável pela gestão e execução de operações no próprio banco de dados. O Gestagent aguarda por mensagens RPC através do barramento de mensagens e executa a operação solicitada
* Conductor: é um serviço que é executado no host, responsável pela recepção de mensagens de instâncias de guests para atualizar as informações sobre o host. Por exemplo, status de instância e o status atual de um backup. Com conductor, instâncias de guests não precisam de uma conexão direta ao banco de dados do host.
