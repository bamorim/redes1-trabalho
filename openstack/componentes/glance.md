# Image Service (glance)

O Glance providencia serviços de pesquisa, registro e entrega para imagens de disco e servidor.
O Glance tem uma API RESTful que permite consulta de metadados de imagem VM, bem como a recuperação da imagem real.

Imagens de VM disponibilizados através Glance podem ser armazenados em uma variedade de sistemas de arquivos simples para sistemas como o projeto OpenStack Swift. Como acontece com todos os projetos OpenStack, o Glance é escrito com as seguintes diretrizes de design em mente:
  1 - Arquitetura baseada em componentes: Adicione rapidamente novos comportamentos
  2 - Alta disponibilidade: Escala para cargas de trabalho muito grandes
  3 - Tolerantes a falhas: processos isolados evitam falhas em cascata
  4 - Recuperáveis: Falhas deve ser faceis de diagnosticar, depurar e corrigir
