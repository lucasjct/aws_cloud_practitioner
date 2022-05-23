# Tópicos sobre características da nuvem e serviços da AWS.  


### Vantagens na Nuvem AWS:  

* A AWS gerencia a manutenção da infraestrutura de nuvem. Essa solução é responsável pela proteção da infraestrutura que executa todos os serviços oferecidos na Nuvem da AWS. Essa infraestrutura é composta por hardware, software, redes e instalações que executam os servicos na nuvem da AWS.  

* A AWS gerencia o planejamento de capacidade para servidores físicos. Essa solução é um exemplo de segurança "da" nuvem. O planejamento de capacidade da nuvem é um controle herdado da AWS. A AWS compra servidores adicionais conforme necessário, com base na demanda geral do cliente.

https://aws.amazon.com/pt/compliance/shared-responsibility-model/

### Benefícios da Nuvem AWS  

* As __despesas de capital__ são substituídas por __despesas variáveis__. 
* As empresas ganham maior agilidade. Os recursos de TI são diposnibilizados para desenvolvedores em minutos, ao inves de semanas. Isso resulta em tempo e custo reduzidos para desenvolvimento, aumentando a agilidade. 
[Seis vantagens da computação em nuvem](https://docs.aws.amazon.com/pt_br/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)  

###   Isolamento físico de instâncias Amazon EC2 de um cliente para as instâncias de outros clientes  

* Com hosts dedicados, um servidor físico é dedicado ao seu uso. Hosts dedicados fornecem visibilidade e a opção de controlar como você coloca suas instâncias em um servidor físico isolado.

[hosts dedicados](https://aws.amazon.com/pt/ec2/dedicated-hosts/)  


### Design de  Arquitetura da nuvem AWS compatível com distribuição de cargas em varias zonas de disponibilidade.

[AWS Well-Architected Framework](https://docs.aws.amazon.com/pt_br/wellarchitected/latest/performance-efficiency-pillar/wellarchitected-performance-efficiency-pillar.pdf#welcome)

* A AWS recomenda que você distribua as cargas de trabalho em várias zonas de disponibilidade. Essa distribuilão garantirá a disponibilidade contínua da aplicacção, mesmo que ela não esteja disponível em uma única zona de dispobibilidade.    


### Princípio de redução das interdependências.  
* Acoplamento fraco. O acoplamento fraco ajuda a isolar o comportamento de um componente de outro componente que dependem dele, aumentando a resiliências e a agilidade. Uma alteração ou falha em um dos componentes não deve afetar outros componentes.  


[AWS Well-Architected Framework](https://docs.aws.amazon.com/pt_br/wellarchitected/latest/performance-efficiency-pillar/wellarchitected-performance-efficiency-pillar.pdf#welcome)


### Exemplo de modelo de responsabilidade compartilhada da AWS.  
* Proteção da infraestrutura física.  A AWS Mantém totalmente o controle físico.  
[Responsabilidade Compartilhada](https://aws.amazon.com/pt/compliance/shared-responsibility-model/)  



### Monitorar e receber alertas sobre eventos de login do Console de Gerenciamento da AWS que envolvem o usuário raiz da conta.  

* O CloudWatch monitora os recursos da AWS e as aplicações executadas em tempo real na AWS. Você pode usar o CloudWatch para monitorar e receber alertas sobre eventos de login do console que envolvam o usuário raiz da conta da AWS.

[AWS CludWatch](https://docs.aws.amazon.com/pt_br/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)


### Exemplo de boas práticas relacionadas ao AWS Identity and Access Management (IAM)

* Recomendação de segurança de menor privilégio, uma prática recomendada do IAM é conceder permissões detalhadas aos usuários usando IAM roles.  

[Privilégios mínimos](https://docs.aws.amazon.com/pt_br/IAM/latest/UserGuide/best-practices.html#grant-least-privilege)  

### Um serviço precisa acessar outro, por exemplo, um servidor de aplicações precisa acessar o bucket privado do Amazon S3.  
* Para isso, A IAM rolres são credenciais temporárias que expiram. As IAM roles são mais seguras do que as cheves de acesso de longo prazo porque reduzem o risco caso as credenciais sejam exposta acidentalmente.  

[IAM Rule](https://docs.aws.amazon.com/pt_br/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html)   



### Exemplo de dois serviços relacionados a segurança:  

* Trusted Advisor baseia-se nas melhores práticas aprendidas ao atender centenas de milhares de clientes da AWS. Essas melhores práticas incluem verificações de segurança   
[Aws Trusted Advisor](https://aws.amazon.com/pt/premiumsupport/technology/trusted-advisor/best-practice-checklist/)  

* Proteção de Dados e Criptografia
[Uso de Criptografia](https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/UsingEncryption.html)   

### Exemplo de duas recomendações associadas ao Trusted Advisor  

* O Trusted Advisor verifica permissões de bucket do S3 no Amazon S3 com permissões de acesso aberto. As permissões de bucket que concedem acesso de listagem a todos podem resultar em custos superiores aos esperados se os objetos do bucket forem acessados por usuários indesejados com alta frequência. As permissões de bucket que concedem acesso de upload e exclusão a todos os usuários criam possíveis vulnerabilidades de segurança, pois permitem que qualquer pessoa adicione, modifique ou remova itens em um bucket. Essa verificação do Trusted Advisor examina permissões explícitas de bucket e políticas de bucket associadas que podem substituir as permissões de bucket.   

* O Trusted Advisor confere a conta raiz e avisa se a MFA (Autenticação Multifator) não está habilitada.  

[TrustedAdvisor](https://aws.amazon.com/pt/premiumsupport/technology/trusted-advisor/best-practice-checklist/)     


### Conexão privada dedicada entre suas operações locais e a Nuvem AWS.  

* O Direct Connect fornece uma conexão privada dedicada entre suas instalações locais e a Nuvem AWS. O Direct Connect é uma alternativa ao uso da Internet para acessar os serviços de nuvem da AWS.   

[AWS DirectConnect](https://aws.amazon.com/pt/directconnect/)  


###  Aspecto da infraestrutura da AWS fornece __implementação global__ de computação e armazenamento  

*  Uma região é um local físico onde há clusters de datacenters da AWS. A AWS oferece muitas regiões diferentes nas quais é possível implantar infraestrutura em todo o mundo. Com o uso de várias regiões, você pode obter uma implementação global de computação, armazenamento e bancos de dados.

[Regiões](https://aws.amazon.com/pt/about-aws/global-infrastructure)   

### Exemplo de produtos da AWS são compatíveis com a replicação de dados em todas as regiões AWS   
*  Amazon S3 é compatível com a replicação entre regiões. Com a replicação entre regiões, você designa um bucket do S3 de destino em outra região. Quando a replicação entre regiões estiver ativada, qualquer novo objeto carregado será replicado no bucket do S3 de destino.  
*  Amazon RDS (Rekational Database Service) para hospedar bancos de dados relacionais na AWS. Uma instância de banco de dados do RDS reside em uma única região. Com o Amazon RDS, você pode criar réplicas de leitura entre regiões. O Amazon RDS replica todos os dados da instância do banco de dados primário na réplica de leitura entre regiões.  
[AmazonRDS](https://docs.aws.amazon.com/pt_br/AmazonRDS/latest/UserGuide/USER_ReadRepl.html)   

### Sites estáticos e hospedagem no S3 com latência baixa e alta taxa de transferência.  
* Entrega rápida de conteúdo. Amazon CloudFront.  CloudFront é um serviço da Web que acelera a distribuição do conteúdo estático e dinâmico da Web, como arquivos .html, .css, .js e de imagem aos usuários. O conteúdo é armazenado em cache nos pontos de presença. O conteúdo acessado repetidamente pode ser fornecido pelos pontos de presença em vez do bucket do S3 de origem.
[Amazon CloudFront](https://docs.aws.amazon.com/pt_br/AmazonCloudFront/latest/DeveloperGuide/IntroductionUseCases.html#IntroductionUseCasesStaticWebsite)


