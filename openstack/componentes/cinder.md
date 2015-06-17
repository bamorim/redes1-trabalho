# Block Storage (cinder)

O Cinder providencia dispositivos de  armazenamento persistente para serem usados com instâncias do Compute do OpenStack.
Ele utiliza uma base de dados central baseada em SQL que é compartilhada por todos os serviços do Cinder no sistema. A quantidade e profundidade dos dados se encaixa bem em um banco de dados SQL. Para pequenas implementações esta parece ser uma solução ideal. Para implantações maiores, e especialmente se a segurança é uma preocupação, o Cinder estará se movendo em direção a vários armazenamentos de dados com algum tipo de sistema de agregação.
