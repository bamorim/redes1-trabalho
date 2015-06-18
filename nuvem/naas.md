# NaaS - Rede como Serviço

A Rede como serviço NNaaS) é uma framework que integra serviços de computação em nuvem atuais com o acesso direto, porém seguro, do cliente para a infra-estrutura de rede. Usando Naas, os clientes podem facilmente implantar o roteamento personalizado e protocolos de multicast. Além disso, ao modificar o conteúdo de pacotes "on-path", eles podem de forma eficiente implementar serviços avançados de rede, tais como a agregação em rede de dados, eliminação de redundância e cache inteligente.

O modelo tradicional oferecido por provedores de nuvem rigidamente separa computação nos hospedeiros finais de encaminhamento de rede "end-to-end". Os proponentes de NaaS argumentam que esta separação compromete tanto o desempenho no plano de dados quanto a flexibilidade no plano de controle da malha de rede.

As funcionalidades do NaaS são divididas em:
* __Visibilidade de Rede__: Muitos aplicativos são construídos em cima de redes "overlay" (sobrepostas). Para atingir alto desempenho, grande esforço deve ser feito para optimizar o mapeamento entre as topologias lógica e física.
* __Forwarding Customizado__: é a capacidade de controlar o encaminhamento de pacotes em comutadores. Isso permitiria a implementação de protocolos de roteamento customizados.
* __Processamento In-Network__: Ao realizar a agregação em rede, é possível uma redução significativa do tráfego total enviado através da rede, reduzindo os tempos de execução. Note-se que estas funções de agregação são específicas do aplicativo e, portanto, não podem ser fornecidas como um serviço de rede tradicional.
