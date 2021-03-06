# Telemetry (ceilometer)

O Ceilometer é um serviço de telemetria que providencia um ponto de contato único para sistemas de pagamento.
Cada um dos serviços de Ceilometer são projetados para escalar horizontalmente. Trabalhadores adicionais e os nós podem ser adicionados dependendo da carga prevista. Ceilometer oferece cinco serviços centrais, os agentes de dados projetados para trabalhar de forma independente da coleção e alarmante, mas também projetados para trabalhar juntos como uma só solução:
  * __Agente de votação__: daemon projetado para sondar serviços OpenStack e construir Meters
  * __Agente de notificação__: daemon projetado para ouvir as notificações a fila de mensagens e convertê-los para eventos e amostras
  * __Coletor__: daemon projetado para reunir dados de evento e registro de pressão e medição criado por agentes de notificação e de votação
  * __API__: serviço para consultar e visualizar dados registrados pelo serviço de colecionador
  * __Alarming__: daemons para avaliar e notificar com base em regras definidas
