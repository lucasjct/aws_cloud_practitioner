## Revisão da AWS para Cloud Practitioner  
*** 



__O que é computação em nuvem?__

*É a entrega de serviços computacionais atrvavés da internet e cobrado no modelo sob demanda.*  



Infraestrutura: Regiões e zonas de disponibilidades.

Modelo de Interação com a nuvem: Console, CLI e SDKs. 


__Vantagens da computação em nuvem:__

- Troca de despesas capitais por despesas variáveis
- Obternha benefícios da imensa economia de escala
- Pare de tentar advinhar a capacidade
- Aumente a velocidade e a agilidade
- Foque no que importa
- Torna-se global em minutos.  


__Well Architected Framework:__ 

* __Excelência Operacional__ (monitoramento e melhoria contínua de processo)  
* __Segurança__ (proteção da informação, das aplicações)
* __Confiabilidade__ (recuperação rápida caso haja alguma falha)
* __Eficiencia de performance__ (trabalhar com recursos de forma eficiente para atender as demandas)
* __Otimização de custos__ (trabalhar de forma eficiente pagando apenas pelo o que está em uso para obter bom custo benefício)
* __Sustentabilidade__ - Extrair valor real dos recursos que utilizamos, sem diperdiçar.  



__Segurança - Segurança é uma prioridade na aws.__  


Segurança __DA__ nuvem => responsabilidade da AWS
Segurança __NA__ nuvem => Cliente

__Princípio do mínimo privilégio possível. Boa prática para permissões na nuvem:__

Trabalhar com permissionamento granular para recursos e usuários. 

__Mais recomendações:__  

- Criptografia em transito e Criptografia em descanso. 

- Não utilizar usuário do root user para trabalhar com rotinas diárias. Precisamos utilizar políticas do IAM para definir permissões.  

__Serviço IAM__ - Serviço que utilizamos para criar e gerenciar usuário da conta aws.   

- Recurso de __Groups__ para agregar usuários com as mesmas permissões definidas nas Polices.  

- __Policies__, definem acesso ou restrição de permissionamento aos serviços da nuvem.  Elas são escritas em um formato JSON.

- __Roles__. Sempre que tivermos um serviço que precisa se comunicar com outros serviços, precisamos colocar permissões para a Roule com as permissões que precisamos executar. Serviços falando com serviços, trabalhamos com as roles.

- __MFA__ - Camada a mais de proteção para autemticar ma conta aws.

__Amazon Inspector__

- Avalia as vulnerabilidades nas redes onde está o EC2 e indica qual seria a melhor prática a ser aplicada. 
- Analisa e identifica casos de exposição de dados na intencional na rede (por exemplo, dados sensíveis).
- Disponibiliza uma lista detalhada com as descobertas e oferece dicas visando boas práticas.  


__AWS Shield__ - Protege contra ataques DDOS

Todos o cliente tem acesso ao Shield na modalidade básica. Camada de rede e transporte são cobertas com a modalidade básica.

Modelo avança, a camada de aplicação é coberta pelo AWS Shield.

Detecção sempre ativas.  

 - A AWS é segura por ser reconhecida por diversos serviços de conformidade. São certificações disponíveis na AWS Artifact.     


### Tecnologia  



__Região__

O serviços da AWS estão em regiões, cada região possui pelo menos duas zonas de disponibilidade para garantir alta disponibilidade. 

Cada região é independente entre uma e outra.

__Zonas de disponibilidade  (AZ)__

- Data centers em uma região. Um ou mais em cada zona de disponibilidade.
- São projetadas para isolamento de falhas
- São interconectadas usando links privados de alto velocidade.
- São usadas para alcançar alta disponibilidade.  


__Edge Locations__

- Serviços de escopo global.   
- Suporte por exemplo para o Route 53, CloudFront (reduz tempo de latência), Shield.  

__Amazon EC2__

* Pode computacional dimensionavel dentro da nuvem.  
EC2 é de escopo de Zona de disponibilidade (AZ)

* Modelo de pagamento On demand.

* São separados em famílias de acordo com o caso de uso.

* Para subir o EC2 escolho uma __AMI (Amazon Machine Image)__ e subo essa imagem e minha instância, esoclher em qual rede ela funcionará, definir a zona de disponibilidade, o tipo de armazenamento, o firewal de segurança e a chave privada, após isso estará pornta. 

* A instancia EC2 em si, é o poder computacional.


__EBS - Amazon Elastic Block Store.__

- Ele é o volume de blocos de uma instancia EC2. - Anexado à instancia, serve para dar persistência aos seus dados.
- Protegido por replicação, garantia contra perda de dados.
- Possui a funionalidade de snapshot para backups.
- Pode ser elástico em minutos.
- Podemos escolher hardware SSD (IOPS) ou HDD (Troughput).
- Pode ser criptografado
- Pagamos apenas pelo que provisionamos. 


__Amazon S3 (Escopo regional)__  

- Os dados são armazenados como objetos em buckets 
- O nome do bucket deve ser único
- O armazenamento é ilimitado
- Objeto único é limitado em 5 TB
- É 99,999999999 % durável
- Acesso granular (definir permissões) a buckets e objetos.

__Classe de Armazenamento:__

* __Standart__ - Acesso frequente, replicado em AZs  
* __Infrequent Access (IA)__ - Acessos menos frequentes
* __One Zone (IA)__ - replicado dentro de uma única zona de disponibilidade.  

__Classes de arquivamento__

* __S3 Glacier instant Retrieval__. Posso deixar armazenado, mas ter o acesso imediato quando precisar.

* __S3 Glacier Flexible Retrieval__ - Não tenho acesso imediato, devo aguardar de 1 até 12 horas.

* __S3 Deep Archieve__ - Armazenamento de longo prazo. 7 a 12 anos. Distribuido em 3 AZs.


### Banco de dados

__Gerenciados e Não Gerenciados__

__Gereciados__  

Totalmente gerenciado pela AWS, o cliente não precisa de preocupar com patchs de segurança, provisionamento e configurações adicionais.

__Não Gerenciados__

* Acesso ao sistema operacional
* Precisa de recursos de aplicações específicos. 

__Amazon RDS (Relational Databse Service)__ 
* Amazon Aurora
* PostgtreSQL
* MySQL
* MariaDB
* Oracle DataBase
* Microsoft SQL server

__Características gerais:__  
- Fáceis de configurar, gerenciar e manter
- Alta disponibilidade com alguns cliques
- Foco no desempenho
- Infraestrutura gerenciada
 


__Amazon Aurora (escopo regional)__

- Banco de dados relacional corporativo
- Reduz custo
- Replica seis cópias em 3 AZs para alta disponibilidade
- Alto desempenho
- Podemos trabalhar até com 15 replicas de leitura (read replicas)
- Podemos trabalhar serviless ou com instâncias.


__DynamoDB__

- No SQL, estrutura chave-valor
- Serveless
- __Totalmente gerenciado__
- Dimensionamento automático
- Multiregião multiplicando o que escrevemos em uma tabela para outras demais regiões.
- DAX Acelerador de consultas.


__VPC - Virtual Private Cloud__

- Logicamente isolada de qualquer outras redes
- Região, nome e range de ips que desejo trabalhar
- Definição de subredes e porções de ips alocadas
- Definição em qual zona de disponibilidade essa subrede vai morar. *Uma subrede é restrita em uma única zona de disponibilidade.*

* Por padrão as VPCs são privadas, por isso não tem comunicação com o mundo exterior. Para comunicar com a internet, precisamos configurar o __Internet Gatway (porta de comunicação com o mundo exterior)__. Após isso defino as rotas. __Subredes__  entrarão em comunicação com a internet são públicas.

* Se a conexão não é com a internet,utilizando __VPN__ ou __Direct connect__ para conectar com datacenter comporativo, utilizo um __VGW - VIRTUAL PRIVATE GATEWAY__.

__Camadas de segurança VPC__

* Security Group, definimos recursos que podem entrar e acessar a vpc.
* Firewal de subrede, que são os __ACLs (network access control list)__, controla o acesso em uma o mais subrede.



### PRECIFICAÇÃO    

* Pagamento por utilização
* Reserva quando há consumo de 1 a 3 anos (economia de 72%)
* Pague menos utilizando mais (economia em escala para armazenamento, como ocorre com o S3 por exemplo)  
* Extimativa de custo baseada em caso de uso
* Calculadora de preços da AWS (voltadas para simular orçamentos para implantação da  nuvem).  

__Conceitos de preços__.  

* Comutação  - Cobrado por hora/segundo; Varia por tipo de instânica.  
* Armazenamento - Cobrado geralmente por GB  
* Transferência de dados - A saída é agregada e cobrada; A entrada não tem encargos (com alguma excessões); a cobrança é feita por GB.     

__Planos de suporte__   

* Basic  (nível gratuito por 12 meses, possui as recomendações básicas do __TrustedAdvisor__). 
* Development  (Não gratuito, mas ideal para quem quer experimentar os serviços da nuvem, possui as recomendações básicas do TrustedAdvisor).
* Business  (Modelo que oferece suporte, porém mais econômico em relação ao Enterprise. Nesse tier, também há todas a verificações avançadas do TrustedAdvisor).
* Enterprise (Conta com TAM dedicado e tempo de SLA de até 15 minutos além de todas a verificações avançadas do TrustedAdvisor).
