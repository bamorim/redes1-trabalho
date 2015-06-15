# Data Processing (sahara)

O Sahara tem como objetivo fornecer aos usuários meios simples de configurar um cluster do Hadoop no OpenStack, especificando vários parâmetros como a versão Hadoop, topologia de cluster e os nós de detalhes de hardware. 

A arquitetura Sahara consiste de vários componentes:
* Componente Auth: responsável pela autenticação e autorização do cliente. Se comunica com o Keystone
* DAL - Data Access Layer, persiste modelos internos em Banco de Dados
* Engine de provisionamento: componente responsável pela comunicação com Nova, Heat, Cinder e Glance
* Fornecedor de Plugins: mecanismo responsável pela configuração e lançamento Hadoop em VMs provisionadas
* EDP - Processamento de Dados Elastico. Responsável pelo agendamento e gerenciamento de tarefas em clusters Hadoop provisionados pelo Sahara
* API REST: expõe a funcionalidade Sahara via REST
