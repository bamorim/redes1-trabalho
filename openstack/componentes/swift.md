# Object Storage (swift)

O Swift é um sistema da armazenamento redundante escalável. Seus principais componentes são:

* Servidor Proxy: é responsável por organizar o resto da arquitectura Swift. Para cada request, ele irá procurar a localização da conta, recipiente ou objeto no Anel e encaminhar o pedido.
* Anel: Um anel representa um mapeamento entre os nomes das entidades armazenados no disco e a sua localização física. Há anéis separados para contas, contêineres e um objeto anel por política de armazenamento. Quando outros componentes precisam realizar qualquer operação em um objeto, recipiente, ou conta, eles precisam interagir com o anel apropriado para determinar a sua localização no cluster
* Object Server: é um servidor de armazenamento blob muito simples que pode armazenar, recuperar e excluir objetos armazenados em dispositivos locais. Os objetos são armazenados como arquivos binários no sistema de arquivos com metadados armazenados em atributos estendidos do arquivo (xattrs)
* Container Server: A principal tarefa do Container Server é lidar com listagens de objetos. Ele não sabe onde os objetos listados estão, só sabe que estão em um recipiente específico. As listas são armazenadas como arquivos de banco de dados SQLite e replicadas em todo o cluster
* Account Server: é muito parecido com o Contaied Server, com exceção de que ele é responsável por anúncios de containers ao invés de objetos
