# Serviços e recursos da AWS
As palavras-chaves estão entre parênteses.  

### Análises:
* Amazon Athena (Análise de dados no S3) 
  * O Amazon Athena é um serviço de consultas interativas que facilita a análise de dados no __Amazon S3__ usando SQL padrão. O Athena não precisa de servidor. Portanto, não há infraestrutura para gerenciar e você paga apenas pelas consultas executadas.  [Amazon AthEna](https://aws.amazon.com/pt/athena/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc)  
  
* Amazon Kinesis (Streamer de dados e videos, real time)
    * O Amazon Kinesis facilita a coleta, o processamento e a análise de dados de streaming em tempo real, permitindo que você obtenha insights oportunos e reaja rapidamente às novas informações. [Amazon Kinesis](https://aws.amazon.com/pt/kinesis/)
* Amazon QuickSight (Serviço de BI)  
    * O Amazon QuickSight permite que todos em sua organização entendam seus dados por meio de perguntas em linguagem natural, do uso de painéis interativos ou procurando automaticamente padrões e discrepâncias com tecnologia de machine learning.  [Amazon QuickSight](https://aws.amazon.com/pt/quicksight/)

### Integração de aplicações:
* Amazon Simple Notification Service (__Amazon SNS__) (Serviço de notificação por Email e SMS) 
    * O Amazon Simple Notification Service (Amazon SNS) é um serviço de mensagens totalmente gerenciado para a comunicação de aplicação para aplicação (A2A) e de aplicação para pessoa (A2P). [Amazon SNS](https://aws.amazon.com/pt/sns/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc)


* Amazon Simple Queue Service (__Amazon SQS__)  (Serviço de mensageiria)  
   * O Amazon Simple Queue Service (SQS) é um serviço de filas de mensagens gerenciado que permite o desacoplamento e a escalabilidade de microsserviços, sistemas distribuídos e aplicações sem servidor. [Amazon SQS](https://aws.amazon.com/pt/sqs/)



### Serviços de computação e sem servidor:   

* AWS Batch (processamento em lote)  
   *   O AWS Batch possibilita que desenvolvedores, cientistas e engenheiros executem de modo fácil e eficiente centenas de milhares de tarefas de computação em lote na AWS. O AWS Batch provisiona dinamicamente a quantidade e o tipo de recursos computacionais ideais (por exemplo, instâncias otimizadas para CPU ou memória) com base nos requisitos de volume e recursos específicos das tarefas em lote enviadas.  [Amazon Batch](https://aws.amazon.com/pt/batch/?nc=sn&loc=0) 


* Amazon EC2 (recursos computacionais, virtualização)   
   * O Amazon Elastic Compute Cloud (Amazon EC2) oferece a plataforma de computação mais ampla e profunda, com mais de 500 instâncias e opções do processador, armazenamento, redes, sistema operacional e modelo de compra mais recentes para ajudar você a atender melhor às necessidades da sua workload. [Amazon EC2](https://aws.amazon.com/pt/ec2)  
   
* AWS Elastic Beanstalk (Facilidade para buildar e configurar a aplicação)   
  * Basta fazer o upload de seu código e o Elastic Beanstalk se encarrega automaticamente da implementação, desde o provisionamento de capacidade, o balanceamento de carga e a escalabilidade automática até o monitoramento da saúde do aplicativo. Ao mesmo tempo, você mantém total controle sobre os recursos da AWS que possibilitam a operação do seu aplicativo e pode acessar os recursos subjacentes a qualquer momento. [AWS Elastic Beanstalk ](https://aws.amazon.com/pt/elasticbeanstalk/).  
  
* AWS Lambda (Serveless, executar código sem servidores)  
   *  AWS Lambda é um serviço de computação sem servidor e orientado a eventos que permite executar código para praticamente qualquer tipo de aplicação ou serviço de backend sem provisionar ou gerenciar servidores. [AWS Lambda](https://aws.amazon.com/pt/lambda/)   
  
* Amazon Lightsail (Facilidade em começar a usar a AWS)
  * O Amazon Lightsail é um provedor de servidor privado virtual (VPS) e a maneira mais fácil de começar a usar a AWS para desenvolvedores, pequenas empresas, estudantes e outros usuários que precisam de uma solução para construir e hospedar suas aplicações na nuvem. [AWS Lightsail](https://aws.amazon.com/pt/lightsail/faq/)
  
* Amazon WorkSpaces (Acesso seguro, confiável e escalável aos desktops persistentes a partir de qualquer local).   
  * Amazon WorkSpace é um desktop virtual na cloud que atua como substituto de um desktop tradicional. Um WorkSpace é disponibilizado na forma de um pacote com sistema operacional, recursos computacionais, espaço de armazenamento e aplicações de software que permitem a um usuário executar tarefas do dia a dia da mesma forma como faria com um desktop tradicional.  Amazon WorkSpaces é um serviço de desktop gerenciado e protegido na cloud. Você pode usar o Amazon WorkSpaces para provisionar desktops Windows ou Linux em apenas alguns minutos e escalar rapidamente para oferecer milhares de desktops a funcionários em todo o mundo. [Amazon WorkSpaces](https://aws.amazon.com/pt/workspaces/faqs/?nc=sn&loc=4)


### Contêineres:  

* Amazon Elastic Container Service (Amazon ECS) )(Containers)  
   * O Amazon Elastic Container Service (Amazon ECS) é um serviço de gerenciamento de contêineres altamente rápido e escalável. Você pode usá-lo para executar, interromper e gerenciar contêineres em um cluster. No Amazon ECS, seus contêineres são definidos em uma definição de tarefa que você usa para executar tarefas individuais ou tarefas em um serviço. [Amazon ECS](https://docs.aws.amazon.com/pt_br/AmazonECS/latest/developerguide/Welcome.html).  


* Amazon Elastic Kubernetes Service (Amazon EKS) (Gerenciamento de Containers)   
  * O Kubernetes é um sistema de orquestração de contêineres de código aberto que permite implantar e gerenciar aplicações em contêineres em grande escala. [Amazon EKS](https://aws.amazon.com/pt/eks/faqs/).


* AWS Fargate (Computação sem servidor para contêineres)
  * O AWS Fargate é um mecanismo de computação sem servidor para contêineres que funciona tanto com o Amazon Elastic Container Service (ECS) quanto com o Amazon Elastic Kubernetes Service (EKS). O AWS Fargate facilita a concentração no desenvolvimento de suas aplicações. [AWS Fargate](https://aws.amazon.com/pt/fargate/faqs/?nc=sn&loc=4).    


### Banco de dados:
* Amazon Aurora (Banco de Alta performance e disponibilidade)
   * Amazon Aurora é um Relational Database Management System (RDBMS – Sistema de gerenciamento de banco de dados relacional) criado para a nuvem com total compatibilidade com MySQL e PostgreSQL. O Aurora oferece a performance e a disponibilidade de bancos de dados de nível comercial por um décimo do custo. [Amazon Aurora](https://aws.amazon.com/pt/rds/aurora/)  


* Amazon DynamoDB (NoSQL)
  * O Amazon DynamoDB é um banco de dados de chave-valor NoSQL, sem servidor e totalmente gerenciado, projetado para executar aplicações de alta performance em qualquer escala. O DynamoDB oferece segurança integrada, backups contínuos, replicação multirregional automatizada, armazenamento em cache na memória e ferramentas de exportação de dados. [Amazon DynamoDB](https://aws.amazon.com/pt/dynamodb/)  
  
* Amazon ElastiCache (Latência de microssegundos e dimensione com cache na memória)   
  * O Amazon ElastiCache é um serviço de cache na memória totalmente gerenciado que oferece suporte a casos de uso flexíveis e em tempo real. Você pode usar o ElastiCache para armazenamento em cache, o que acelera a performance de aplicações e bancos de dados, ou como um armazenamento de dados principal para casos de uso que não exigem durabilidade, como armazenamentos de sessões, placares de jogos, streaming e análises. O ElastiCache é compatível com o Redis e o Memcached. [Amazon ElastiCache](https://aws.amazon.com/pt/elasticache/)


* Amazon RDS   (Serviços para banco de dados relacionais)
   * O Amazon Relational Database Service (RDS) é uma coleção de serviços gerenciados que facilita a configuração, operação e escalabilidade de bancos de dados na nuvem. Escolha entre sete opções de mecanismos bastante utilizados: Amazon Aurora compatível com MySQL, Amazon Aurora compatível com *PostgreSQL, MySQL, MariaDB, PostgreSQL, Oracle e SQL Server*. Depois, implante on-premises com o Amazon RDS on AWS Outposts. [Amazon RDS](https://aws.amazon.com/pt/rds/)   


* Amazon Redshift (Serviço para BigData)   
  * Amazon Redshift usa SQL para analisar dados estruturados e semiestruturados em data warehouses, bancos de dados operacionais e data lakes, usando hardware e machine learning projetados pela AWS para oferecer a melhor performance de preço em qualquer escala. [Amazon Redshift](https://aws.amazon.com/pt/redshift/)

### Ferramentas de desenvolvedor:
* AWS CodeBuild (Compilar, buildar, Continuous Integration) 
  * O AWS CodeBuild é um serviço de integração contínua totalmente gerenciado que compila o código-fonte, realiza testes e produz pacotes de software prontos para implantação. Com o CodeBuild, você não precisa provisionar, gerenciar e escalar seus próprios servidores de compilação. O CodeBuild escala continuamente e processa múltiplas compilações ao mesmo tempo, o que evita que elas fiquem esperando em uma fila. [AWS CodeBuild](https://aws.amazon.com/pt/codebuild/)  
    
* AWS CodeCommit (Versionamento de código)
  * O AWS CodeCommit é um serviço de controle de origem gerenciado seguro e altamente dimensionável que hospeda repositórios privados do Git. Ele torna mais fácil para as equipes colaborarem com segurança no código com contribuições criptografadas em trânsito e em repouso. [ AWS CodeCommit](https://aws.amazon.com/pt/codecommit/)  


* AWS CodeDeploy
* AWS CodePipeline
* AWS CodeStar   


### Interação com os clientes: 
* Amazon Connect   

### Gerenciamento, monitoramento e governança:
* AWS Auto Scaling
* AWS Budgets
* AWS CloudFormation
* AWS CloudTrail
* Amazon CloudWatch
* AWS Config
* Relatório de Custos e Uso da AWS
* Amazon EventBridge (Amazon CloudWatch Events)
* AWS License Manager
* AWS Managed Services
* AWS Organizations
* AWS Secrets Manager
* AWS Systems Manager
* AWS Systems Manager Parameter Store
* AWS Trusted Advisor  


### Redes e entrega de conteúdo:
* Amazon API Gateway
* Amazon CloudFront
* AWS Direct Connect
* Amazon Route 53
* Amazon VPC   

### Segurança, identidade e conformidade:
* AWS Artifact
* AWS Certificate Manager (ACM)
* AWS CloudHSM
* Amazon Cognito  
* Amazon Detective
* Amazon GuardDuty
* AWS Identity and Access Management (IAM)
* Amazon Inspector
* AWS License Manager
* Amazon Macie
* AWS Shield
* AWS WAF  

### Armazenamento:  

* AWS Backup 
* Amazon Elastic Block Store (Amazon EBS)
* Amazon Elastic File System (Amazon EFS)
* Amazon S3
* Amazon S3 Glacier
* AWS Snowball Edge
* AWS Storage Gateway
