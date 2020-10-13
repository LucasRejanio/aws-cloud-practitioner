# AWS-Cloud-Practitioner-Certificate 
Nesse repositório colocarei uma serie de anotações relevantes para certificação da Amazon Cloud Practitioner. Todas as anotações são baseadas no AWS Training and Certificate disponibilizado no próprio site da Amazon. 

Link do trainamento: https://www.aws.training/Details/Curriculum?id=27076

## Overview 
- [ ] Definição de cloud AWS
- [ ] Principais serviços AWS
- [ ] Infraestrutura Global AWS
- [ ] Serviços integrados
- [ ] AWS Well-Architected Framework (Estrutura bem arquitetada)
- [ ] Segurança

## Definição de cloud AWS
Cloud Computing se refere à entrega sob demanda de recursos e aplicativos de TI via internet. Com Cloud Computing, em vez de ter que projetar e construir nossos próprios data centers, acessamos um data center e todos seus recursos via internet, permitindo-nos aumentar ou diminuir com base nas nossas necessidades reais, sem precisar planejar o pior cenário possível. Com essa abordagem para gerenciamento de mudanças, testes, confiabilidade e o planejamento de capacidade é mais ágil e eficiente. 
Ao usar a nuvem AWS, podemos reduzir os riscos, dimensionar automaticamente nossa computação para atender nossas necessidades, garantir uma cobertura confiável mesmo em face de um natural desastre e proteger nossos dados.

### Redução de custo
Cloud computing pode ajudá-lo a reduzir os risco sendo ágil, ser capaz de aprender e se adaptar rapidamente às mudanças, essa agilidade reduz o custo de mudança. Então, como você reduz o risco de um grande investimento em TI, não está retornando benefícios suficiente? 

### Redução do risco de segurança
Teste com frequência, faça correções rapidamente e responda na velocidade da luz. A computação em nuvem permite que as empresas respondam rapidamente e elasticamente às mudanças nas condições do mercado, isso facilita escalabilidade agilidade e inovação.

### Escalabilidade
Um dos principais benefícios da AWS é a capacidade para usar serviços em seu próprio ritmo. Na computação em nuvem, o termo escalabilidade significa capacidade para redimensionar seus recursos conforme necessário. 

### Agilidade
Três dos principais fatores que influenciam a agilidade são: velocidade crescente, facilidade de experimentação e cultivar uma cultura de inovação. Então podemos afirmar que temos agilidade na criação de recursos, no acesso a esses recursos, redução de tempo em configurações de infraestrutura e testes.  

### Elasticidade
Elasticidade é o poder de aumentar ou diminuir os recursos da computação facilmente. Com AWS cloud, você pode rapidamente implementar novos aplicativos, aumentar instantaneamente conforme a carga de trabalho aumenta e desligar instantaneamente recursos que não são mais necessários. Portanto, se você precisa de um servidor ou milhares por apenas algumas horas ou 24/7, a AWS fornece uma infraestrutura elástica que pode atender às suas necessidades. 
Usando ferramentas como Auto Scaling e Load Balance você pode realizar o balanceamento do seu aplicativo automaticamente, aumentando ou diminuindo conforme a demanda. 

### Confiabilidade
Confiabilidade é a capacidade de um sistema se recuperar de  falhas de infraestrutura ou serviço. Na computação em nuvem, confiabilidade significa ser capaz de adquirir recursos de computação para atender à demanda e mitigar interrupções. A fim de alcançar confiabilidade, sua arquitetura  e os sistemas devem ter uma base bem planejada, que lida com mudanças na demanda, detecta falhas e se cura automaticamente, usando a AWS as organizações podem obter maior flexibilidade, reduzindo a incerteza das necessidades de hardware de previsão. Além disso a escala AWS oferece aos clientes a capacidade e confiabilidade que é difícil para as soluções locais combinarem. A confiabilidade é um componente-chave da nuvem AWS, é por isso que os data centers da Amazon são hospedados em todo o mundo, no que chamamos de regiões AWS. Cada região é uma área geográfica separada que tem vários locais isolados conhecidos como zonas de disponibilidade, então, quando você usa nuvem AWS, você pode recursos como instâncias e dados em vários locais. 

### Interfaces AWS
Os usuários AWS podem criar e gerenciar recursos de três maneiras únicas, usando AWS Menagement Console, AWS Command Line interface (AWS CLI) ou os kits de desenvolvimento de software da AWS, ou SDKs. Todas as interfaces são construídas por API.
AWS Menagement Console oferece uma interface gráfica para acessar e criar os recursos, o AWS CLI permite que você controle os serviços da linha de comando, e claro, o SDK, que irá permitir que você acesse AWS usando uma variedade de linguagens de programação populares. 
O AWS CLI permite que você automatize e repita a implantação de recursos AWS de uma forma que é agnóstica a linguagem de programação, onde os SDKs da AWS podem ajudá-lo a usar a AWS em seus aplicativos existentes. O AWS CLI e o SDKs vão dar-lhe a flexibilidade para personalizar os recursos da AWS e cria suas próprias ferramentas específicos para seus negócios.

## Principais serviços AWS

### ec2 (Elastic Compute cloud)
É um serviço Web que disponibiliza capacidade computacional segura e redimensionável na nuvem. Computer refere-se aos recursos que estão sendo apresentados, cloud se refere ao fato de que estes são  recursos de computação hospedados na nuvem e Elastic se refere ao fato de que, se configurado corretamente você pode aumentar ou diminuir a quantidade de servidores exigido por um aplicativo automaticamente de acordo com as demandas atuais dessa aplicação

### EBS (Elastic Block Store)
Os volumes EBS podem ser usados como uma unidade de armazenamento para suas instâncias ec2, então sempre que você acha que precisa de espaço em disco para suas instâncias em execução na AWS, você pode pensar sobre elas. Esses volumes podem ser discos rígidos ou dispositivos SSD. O EBS permite que você aumente ou mude o tipo do seu armazenamento, isso significa que você pode mudar de disco rígido para SSD. 

### S3 (Simple Storage)
Amazon S3 é um serviço de armazenamento totalmente gerenciado que fornece uma API simples para armazenar e recuperar dados, isso significa que os dados que você armazena no Amazon S3 não está associado a nenhum servidor em particular e você não precisa gerenciar nenhuma infraestrutura sozinho, você pode colocar quantos objetos quiser no Amazon S3, como imagens, vídeos ou registros de servidor. Sempre que você armazenar um dado é redundantemente armazenado em várias instalações da AWS em sua região selecionada. O serviço Amazon S3 foi projetado para armazenar dados de maneira duradoura, mesmo no caso de perda simultânea de dados em duas instalações da AWS.

#### Casos de Uso
Local para quaisquer dados da aplicação, o bucket fornece esse local compartilhado para armazenar objetos onde qualquer instância da sua aplicação pode acessar, incluindo aplicativos em ec2 ou até mesmo em servidores tradicionais. Isso pode ser útil para armazenar arquivos gerados pelo usuário, logs do servidor ou aplicação em um local comum, além disso, pelo conteúdo ser disponibilizado na web seus aplicativos permite que o cliente faça buscas dos próprios dados diretamente no Amazon S3.
Para hospedagem estática na web, o S3 podem servir o conteúdo estático do seu site, incluindo HTML, CSS, JavaScript e outros aplicativos.
A alta durabilidade do Amazon S3 o torna um bom candidato para armazenar backups de seus dados para uma disponibilidade ainda maior e capacidade de recuperação de desastres, o S3 pode ser configurado para suportar a replicação entre regiões.
Armazenamento escalável e o desempenho do Amazon S3 torná-lo um ótimo candidato para encenação ou armazenamento de dados a longo prazo, você também pode importar ou exportar grande volume de dados. 

## Infraestrutura Global AWS
A Infraestrutura Global da AWS pode ser dividida em três tópicos: regiões da AWS, zona de disponibilidade e edge locations. Regiões são áreas geográficas que hospedam duas ou mais zonas de disponibilidade e eles são o nível de organização dos serviços da AWS. Zonas de disponibilidade são um conjunto de data center em uma região específica, cada zona de disponibilidade é fisicamente isolada mas conectadas, cada zona de disponibilidade é uma infraestrutura independente. Já os locais do AWS edge hospedam uma rede de entrega de conteúdo, ou CDN chamado Amazon CloudFront. O CloudFront é usado para fornecer conteúdo aos seus clientes, as solicitações de conteúdo são encaminhadas automaticamente para o local Edge mais próximo para que o conteúdo seja entregue o mais rapidamente aos usuários finais.

### VPC (Virtual Private Cloud)
Virtual Private Cloud é o serviço de rede AWS que atenderá seus requisitos de rede. Amazon VPC permite que você crie uma rede privada dentro da nuvem AWS que usa muitos dos mesmos conceitos e constrói como uma rede local.

### Security Group
Na AWS o Security Group como um firewall embutido para seus servidores virtuais, com isso, você passa a ter o controle total sobre como suas instâncias são acessadas.  

## Serviços integrados

### Load Balance 
O Elastic Load Balancing distribui automaticamente o tráfego de entrada de aplicativos entre diversos destinos, como instâncias do Amazon EC2, contêineres, endereços IP e funções Lambda. O serviço pode lidar com a carga variável de tráfego dos aplicativos em uma única zona de disponibilidade ou em diversas zonas de disponibilidade. O Elastic Load Balancing oferece três tipos de load balancers, todos eles com a alta disponibilidade, a escalabilidade automática e a segurança robusta necessárias para tornar os aplicativos tolerantes a falhas.

### Auto Scaling 
Auto Scaling ajuda a garantir que você tenha o número correto de instâncias ec2 disponíveis para Lidar com a carga da sua aplicação.

### Router 53 
Route 53 é um sistema de nomes de domínio ou DNS, que é um serviço projetado para fornecer a empresas e desenvolvedores de forma confiável e altamente escalável para rotear usuários finais para terminais. 

### RDS
Amazon RDS é o serviço da AWS que proporciona a criação de um banco de dados relacional hospedado totalmente na nuvem AWS sem precisar de uma administração contínua. 

### Lambda 
AWS lambda é um serviço de computação que permite executar código sem provisionar e gerenciar servidores, podemos usá-lo para computação orientada a evento.

### Elastic Beanstalk 
Elastic Beanstalk é uma plataforma como serviço (PaaS). Significa que você tem toda a infraestrutura e toda a plataforma de desenvolvimento criada para você, basta fazer o upload de seu código e o Elastic Beanstalk se encarrega automaticamente da implementação. 

### SNS (Simple Notification Service) 
O Amazon Simple Notification Service (SNS) é um serviço de mensagens totalmente gerenciado para comunicação de sistema para sistema e de aplicativo para pessoa (A2P). Ele permite que você se comunique entre sistemas por meio de padrões de publicação/assinatura (pub/sub) que permitem mensagens entre aplicativos de microsserviços dissociados ou para se comunicar diretamente com os usuários via SMS, push móvel e e-mail. Exemplo; posso enviar um email toda vez que subir ou excluir um arquivo do meu Bucket S3 configurando um evento e vinculando ao SNS

### CloudWatch
Amazon CloudWatch é basicamente um serviço de monitoramento que permite monitorar seus recursos AWS e os aplicativos que você executa neles em tempo real. Alguns recursos do Amazon CloudWatch incluem coleta e rastreamento de métricas como utilização de CPU, transferência de dados, utilização de disco e etc, também podemos monitorar serviços para recursos e aplicativos em nuvem, além disso, você tem a  capacidade de definir alarmes em qualquer uma das suas métricas para enviar notificações ou realizar alguma ação automatizada. 

#### Metrics
É daí que vêm os dados sobre o desempenho do seu sistema, ele realmente representa um conjunto de pontos de dados ordenado por tempo que serão publicados no CloudWatch, por padrão, vários serviços oferecem métrica gratuitas para seus recursos, como ec2, volume EBS, RDS, mas você também pode aplicar suas próprias métricas de aplicativo por uma taxa adicional.

#### Alarmes
Os alarmes observam uma única métrica, ele pode realizar uma ou mais ações com base no valor dessa métrica, então essa ação pode ser uma ação ec2 como parar, iniciar, encerrar, reiniciar, pode ser uma ação de Auto Scaling, como iniciar uma configuração de Auto Scaling e adicionar mais instâncias ao meu pool de aplicativos, ou pode ser apenas uma notificação enviada via tópico SNS. Ele invoca ações apenas para mudanças de estados sustentadas. 

#### Eventos
CloudWatch eventos são seu stream quase em tempo real de eventos do sistemas que descrevem mudanças em seus recursos da AWS, ele usa regras simples para combinar eventos e, em seguida, encaminhá-los para uma ou mais funções ou fluxos de destino. Ele pode estar ciente das mudanças operacionais à medida que ocorrem, ele também pode responder a mudanças operacionais e tomar as medidas corretivas necessárias, além disso, você também pode agendar ações automatizadas, aquele auto-acionamento em certos momentos usando cron job ou expressão de taxa. 

#### Log
Basicamente, você pode usar o CloudWatch logs para monitorar e solucionar problemas de sistema e aplicações usando os arquivos de log existentes, portanto, ele pode monitorar seus arquivos para frases, valores ou padrões específicos.

### CloudTrail
Amazon CloudTrail são todas as ações da API que acontecerem na sua conta. E uma vez que tudo o que basicamente acontece dentro da AWS seja do console, do CLI ou acesso direto à API, é tudo baseado na API, isso dá a você um registro completo de quem fez o quê, quando , em seu ambiente. 

### CloudFront
Para entregar conteúdo aos seus usuários o Amazon CloudFront usa uma rede global de mais de 80 pontos de presença em mais de 10 Edge locations radial para entregar de conteúdo. Os locais reais estão localizados em vários países em todo o mundo , e esse número aumenta com frequência, então basicamente, usando CloudFront, você pode aproveitar vários locais ao redor do mundo para entregar seu conteúdo, permitindo que seus usuários interagir com sua aplicação em uma latência mais baixa. Por exemplo, se sua aplicação estiver sendo executada em Cingapura e seus usuários estão em Nova York, você pode usar o CloudFront para armazenar o conteúdo localmente em Nova York e deixar o serviço ajudá-lo a dimensionar quaisquer que sejam suas solicitações de demanda. Podemos resumir o Amazon CloudFront como uma rede de distribuição de conteúdo, ou CDN, para abreviar. CloudFront permite que você economize dinheiro devido a suas taxas mais baixas de transferência de dados e também ajuda você a deixar seus clientes mais felizes porque pode armazenar conteúdo próximo a eles, o que aumenta as chances de entregar seu conteúdo mais rapidamente. Você pode usar o CloudFront para fornecer conteúdo dinâmico na distribuição na web também. 

#### Casos de Uso
Cache de ativos estáticos 
Streaming de vídeos ao vivo sob demanda 
Segurança e proteção DDoS 
aceleração de API 

### CloudFormation (Infraestrutura como codigo)  
CloudFormation simplifica a tarefa de criar grupos repetidos e previsivelmente de recursos, ou seja, você pode realizar o processo de automatização em provisionamento de recursos na AWS usando chamadas API. CloudFormation lê as instruções de um modelo de arquivo sobre quais recursos realmente devem ser realizados e provisionados, construindo os recursos listados no arquivo de modelo, e a saída deste processo é o seu ambiente, conhecido como pilha (Stack). Você pode criar modelo que cria um único recurso ou uma pilha com centenas de recursos.

## AWS Well-Architected Framework
Pilares de arquitetura bem estruturada: segurança, confiabilidade, eficiência de desempenho, otimização de custos e excelência operacional. 

### Segurança: 
O pilar de segurança abrange a capacidade para proteger seus sistemas de informação e ativos ao mesmo tempo que agrega valor ao negócio por meio de avaliações de riscos e estratégia de mitigação. A segurança é dividida em cinco áreas: 

- AWS Identify and Acess Menagement (IAM): IAM é fundamental para garantir que apenas o autorizado e usuários autenticados podem acessar seus recursos apenas da maneira que você pretende. 

- Detective Controls: Os controles de detecção podem ser usados para identificar um potencial incidente de segurança, considerando abordagens como a captura ou analisando logs e integrando controles de auditoria.

- Infrastructure protection: Proteção de infraestrutura garante que os sistema e serviços dentro da sua arquitetura estão protegidos contra acesso não intencional e não autorizados.

- Data protection: Com a proteção de dados, existem várias abordagens e métodos a serem considerados, alguns incluem certificação de dados, criptografia, backup de dados. 

- Incident response: Responsável por responder quaisquer possíveis incidentes de segurança 

### Confiabilidade
O pilar de confiabilidade abrange a capacidade de um sistema para recuperar de falhas de infraestrutura ou serviço, também se concentra na habilidade para aderir dinamicamente recursos da computação para atender demanda e mitigar interrupções.ou seja, confiabilidade serve para auxiliar na capacidade de recuperação de falhas e atender a demanda. A confiabilidade na nuvem é composta por três áreas. 

- Fundações: Para alcançar a confiabilidade, sua arquitetura e sistema devem ter uma fundação bem planejada no local que pode lidar com mudanças na demanda ou requisitos. 

- Gerenciamento de Mudanças: Com o gerenciamento de mudanças, é importante compreender totalmente e esteja ciente de como a mudança pode afetar seu sistema.

- Gerenciamento de falhas: Validar seus procedimentos de falha, os usuários podem simular e expor diferentes falhas e então testar suas reações antes que uma falha real possa ocorrer.


### Eficiência de desempenho: 
As quatro peças que compõem a eficiência do desempenho incluem seleção, revisão, monitoramento e trade-offs

- Seleção e revisão: Com a seleção é importante escolher a melhor solução, isso vai otimizar sua arquitetura, obtenha a ferramenta certa para o trabalho certo, no entanto as soluções é claro, variam com base no tipo de carga de trabalho que você tem.

- Monitoramento: Depois de implementar sua arquitetura, você precisará monitorar sua arquitetura para garantir que você pode corrigir qualquer problema.

- Trade-offs: Um exemplo de um trade-off que garante uma abordagem ideal é negociar consistência, durabilidade e latência.

### Otimização de custo
Isso inclui o processo contínuo de refinamento e melhoria de um sistema ao longo de todo seu ciclo de vida, essa pilha engloba a ideia que você pode construir e operar sistemas cientes de custo e maximizar o retorno do seu investimento. Para isso existem quatro tópicos fundamentais, incluindo recursos econômicos, oferta por demanda, consciência de despesas e otimização ao longo do tempo. 

### Excelência operacional
A excelência operacional se concentra na execução e sistema de monitoramento para agregar valor ao negócio em melhorar continuamente os processos e procedimentos para você, para isso utilizam gerenciamento e automação de mudanças.

### Tolerante a falhas
A tolerância a falha refere-se à capacidade para um sistema permanecer operacional mesmo se alguns dos componentes desse sistema falharem, pode ser visto como a redundância embutida dos componentes de um aplicativo. 

Alta disponibilidade: Conceito referente a todo o sistema, seu objetivo é garantir que seus sistemas estão sempre funcionando e acessíveis e que o tempo de inatividade é minimizado tanto quanto possível sem necessidade de intervenção humana. 
	
#### Serviços que ajudam a alta disponibilidade

- LoadBalance: Realiza a distribuição de carga de entrada

- CloudWatch: Sistema de coleta de estatística, ele coleta e rastreia suas métricas 

- ElasticIP: Mantém um IP estático em uma rede Dinâmica 

- Router 53: Serviço DNS, traduz nome de domínio para endereços IP

- Auto Scaling: Inicia ou encerra instâncias com base em condições específicas(demanda)

## Segurança
AWS oferece uma plataforma escalonável que é projetado para alta disponibilidade e confiabilidade, fornecendo a você as ferramentas que permitem que você execute uma ampla gama de aplicativos, ajudando você a proteger a confiabilidade, integridade e disponibilidade de seus sistemas e dados.

### Modelo de responsabilidade
Quando seu aplicativo está sendo executado na AWS, em algum ponto alguém tem que ser responsável em última instância para proteger seu aplicativo. É A, você, ou B, AWS? A resposta correta é C, todas as opções acima. É preciso ambas as partes, você e a AWS para trabalhar em conjunto para proteger todo o seu aplicativo. Mas no modelo de responsabilidade da AWS é dividido em algumas partes: 

#### Dispositivos físicos - Responsabilidade da AWS
- Rede - Responsabilidade da AWS
- Hypervisor - Responsabilidade da AWS 
- Guest OS - Responsabilidade do Usuário 
- Aplicação - Responsabilidade do Usuário 
- User Data - Responsabilidade do Usuário 

### Gerenciamento de Identidade de acesso (IAM) 
IAM é o sistema de gerenciamento de identidade de acesso da AWS, existem alguns pilares que compõem ele, tais como: 

- User: No caso do IAM, o que estamos falando aqui é um operador nomeado permanente, podendo ser humano ou máquina. A ideia são minhas credenciais que são permanentes e permanecem com o usuário nomeado até que haja uma rotação forçada, seja um nome ou uma senha, chave privada ou combinações de credenciais, é a maneira de autenticação da AWS.

- Group: Grupo, é uma coleção de usuários, podendo ter muitos usuários que permanecem de diversos grupos. 

- Função: É aqui que entende o porque AWS IAM  é importante, porque no AWS IAM, uma função não é suas permissões. Uma função é um método de autenticação. A parte principal é que as credenciais com uma função são temporárias.

- Políticas: Permissões, em todos os casos acontece em um objeto separado conhecido como documento de política.

### Amazon Inspector 
Amazon Inspector é um serviço automatizado de avaliação de segurança que ajuda você a melhorar a segurança e conformidade de aplicativos implementados na AWS. O serviço avalia automaticamente os aplicativos para vulnerabilidades ou desvios das melhores práticas. Depois de realizar a análise, Amazon Inspector produz um relatório detalhado com etapas priorizadas para correção

### Escudo AWS (Shield) 
AWS Shield é uma negação de serviço distribuída gerenciada, ou DDoS, serviço de proteção, que protege os aplicativos em execução na AWS, o serviço fornece detecção sempre ativa e mitigação automáticas inline, que irá minimizar o tempo de inatividade e latência do aplicativo. 

Ataque DoS é uma tentativa deliberada para tornar seu site ou aplicativo disponível para os usuários inundando-o com o tráfego de rede.

Ataque DDoS um invasor usa várias fontes para orquestrar um ataque contra você, as fontes podem incluir grupos distribuídos de computadores infectados com malware, roteadores, dispositivos IoT e outros terminais

### Trusted Advisor
Trusted Advisor é uma ferramenta que oferece as melhores práticas e verifica todos os seus recursos em sua conta para ver se eles estão de acordo com essas práticas recomendadas. E faz isso em quatro categorias diferentes, sendo elas: segurança, tolerância a falhas, desempenho e otimização de custo.

## Conlusão
Depois desse conteúdo, você deve saber definir os topicos: 

- [x] Definição de cloud AWS
- [x] Principais serviços AWS
- [x] Infraestrutura Global AWS
- [x] Serviços integrados
- [x] AWS Well-Architected Framework (Estrutura bem arquitetada)
- [x] Segurança
