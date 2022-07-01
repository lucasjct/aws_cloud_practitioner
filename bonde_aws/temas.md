bonde aws.   
Principais conceitos da certificação

### Domínio de Segurança
*** 
- Conceito de responsabilidade compartilhada

	- Divisão de responsabilidades
	- Responsabilidade DA nuvem (cuidar da estrutura física da nuvem, dos hardwaresm etc) 
	- Responsabilidade NA nuvem (cliente responsável por criptografia de dados de clientes, configuração de firewals[security groups]).

	- AWS deve fazer a segurança da nuvem.
- Conceitos de segurança e conformidade na nuvem
- Conceitos de recursos de segurança
- Ferramentas de gerenciamento de acessos e controle de usuários. 
	- IAM - Acesso e Permissionamento (responsabilidade na nuvem). Recursos do IAM:
	- Roles (conjunto de credencias de acesso temporário)
	- Política do IAM
	- Usuario
	- Grupo de usuario
		- Rules e permissões para grupos
	- MFA
	- Rule - Permissões temporárias. Sempre serão temporárias. (Uma forma é criar um Rule. É um recurso que permite forncer uma permissão e credenciais associada a Rule temporariamente). Por exemplo, o gerente passou mal e precisa de outra pessoa para fazer o deploy em produção. Com isso, faço um Rule para a pessoa.
	- Politicas do IAM. Documento em que se especifica as permissões que podem ser executadas. Pode ser Allow ou Denied. 
	- Autenticação - Definição das credenciais do usuário.
	- Autorização - Para interagir com o ambiente é necessário permissões
		- Denied Explícito - O Denied sempre será acima do Allow. Ele sobrescreve o Allow.
	

Amazon inspector ( Análise e recomendação de segurança)  
	- Avalia vulnerabilidade das aplicações
	- Produz uma lista detalhada de descobertas de segurança
	- Utiliza práticas recomendadas de segurança.
	- Gera um conjunto de descobertas e retorna possíveis medidas para ser tomadas em relação a segurança.
	- "É como se fosse um aviso de mãe" - Sobre os conselhos e ações que são recomendações a partir da análise de vulnerabilidades.


AWS Shield - Serviço para auxiliar e mitigar ataques DDoS
	- Um serviço gerenciado de proteção de DDoS
	- Detecção sempre ativa e mitigações
	- Integração e implementação contínuas
	- Proteção econômica e customizável

AWS WAF - Serviço para criar um firewall para conectar outros recursos que serão protegidos.  


- Monitoramento (saúde operacional, recursos)
- Monitoramento é crucial na segurança. (CloudWatch)
- Notificação (SNS) 
- Monitoramento contínuo
- Resiliência e alta disponibilidade
- Conformidade  

*** 
### Domínio de Tecnologia 

 - Ifraestrutura global aws.
	- Região (área geográfica isolado que contem uma subdivisão que se chama Zona de disponibiliadade)
	- Cada região é completamente independente.
	- A regiões possuem duas ou mais zonas de disponibilidade.

Zonas de disponbilidade
	- Conjunto de datacenters. Ou pelo menos 1 datacenter.
	- As zonas de disponibilidade são fisicamente isoladas, distantes entre si.
	- São concetadas com link de alta velocidade. Pois são arquitetadas para alcançar alta disponibilidades. 
	- Edge Locations (Pontos de infraestrutura de borda). Utilizada para distribuir conteúdo mais próximo do usuário final. Utilizo o serviço de CDN para ser utilizado nesta infraestrutura.
	- Os locais de borda são importantes para garantir latência e disponibilizar conteúdo globalmente, buscando estar mais próximo do cliente para entregar o conteúdo, para isso, utiliza-se o CloudFront.


Amazon EC2  

- Fornece capacidade e recursos computacionais dentro da nuvem. Servem de servidores que podem ser provisionados para diversos propósitos. 
- Podemos escalar estes recursos, tanto verticalmente quanto horizontalmente. Vertical refere ao aumento da capacidade e recursos computacionais da máquina. Horizontal, se refere ao aumento de número de máquinas para suportar a demanda.  
- Existem diversas famílias de instâncias.

Storages  

Amazon EBS (Elastic Blocg Store). Recurso para persistência de dados da intância. Opções em HD (analogia ônibus) e SSD (analogia formula 1).

Bloco e volume é a mesma coisa.
O EBS fica conectado à instância EC2, precisa ficar na mesma região e AZ.
- Protegido por replicação
- Diferentes tipos de unidade
- Aumentar ou diminuir em minutos
- Pague apenas pela provisão
- Funcionalidade de snapshot para versionar
- Criptografia disponível.

Podemos ter mais de um volume associado ao EC2, podem ser encriptados.


AMAZON EC2
 - Amazon Machine Image(AMI)

 - Amazon EC2 Auto Scaling (cresimento horizontal)
	- Ajusta a capacidade conforme necessário
	- Aumente a escala para picos
	- Reduza a escala horizontal em horários fora de pico
	- Substitua instâncias com problemas
	- Pague somente pelo que usar.

- Amazon Load Balancing
	- Distribui as requests para as instâncias ec2 de acordo com o volume do tráfego. 
	- Fz um balanceamento de carga entre duas zonas de disponibilidade.


Amazon CloudWatch
	- Monitora
	- Coleta e rastreia
	- Alarmes (Podem trigar o autoScalling para ele começar a trabalhar)
	- Podemos escalar de acordo com as métricas do CloudWatch. 



Amazon S3.  

Serviço de armazenamento de objetos. 
	- Devemos definir a região que queremos armazenar nossos dados. Após isso, devemos criar um bucket S3, nele iremos armazenzar nossos objetos.

	- Armazenamento ilimitado.
	- Objeto único é limitado em 5TB.
	- O objeto pode ser armazenado em pelo menos 3 zonas de disponibilidade.
	- Podemos definir controle de acesso ao S3.   Sempre que criamos um bucket, ele é privado.

	- Classes de Armazenamento:
		- S3 Standard
		- S3 Standard - Infrequent Access (IA)
		- S3 Inteligent - Tiering
		- S3 One Zone - IA (1 zona de disponibilidade. Para objetos não criticos)
		- S3 Glacier Instant Retrieval
		- S3 Glacier Flexible Retrieval
		- S3 Glacier Deep Archieve  

*** 

### Serviços de Bancos de Dados

Amazon Relational Databne Service. Amazon RDS.

	- Serviço de cunho regional
	- Podemos utilizar o RDS com as seguinte Engines: Amazon Aurora, PostgreSQL, MySQLS, Maria DB, Oracle Database e Microsoft SQL Server.  

Amazon Aurora - Compatível com PostegreSQL e MySQL.Gerenciador de Banco de dados de auto desempenho da própria AWS.

Amazon Dynamo DB. Banco de dados NoSQL. Serveless e orienrado a chave valor.  


Amazon Virtual Private Cloud (Amazon VPC)
- Espaço de rede privado na rede da AWS
- Logicamente isolado
- Controla entrada e saida, provisionamento do que há dentro do espaço logicamente isolado. (analogia do terreno).
- Possui subredes públicas (de frente pra rua) e subredes privadas (fundos do terreno).
- As subredes privadas não possuem rotas diretas para o internet gatway, as subredes privadas possuem rota direta para o internet gateway...
- As definições de rota é na tabela de rotas (route table)
- Security group. Controle State Full, autoriza o tráfego de rotas autorizadas para entrada e saída (output).
Funciona como um Firewall.

Serveless utiliza-se 100% do conceito da nuvem...

*** 
### Faturamento e preço na AWS  

Modelos de pagamento:

On Demand (Pague pelo o que usar)
Saving Plans (Contrato de 1 a 3 anos)


AWS Pricing Calculator = Orçar preços dos serviços que desejo utilizar.

Preço varia de acordo com os seguintes aspectos:

- Computação: cobrado por hora/segundos, varia por tipo de instância.
- Armazenamento: cobrança por GB
- Transferência de dados: A saída é agregada e cobrada, a entrada não tem encargos (com algumas excessoes), cobrança geralmente por GB 

Suporte básico:
- Acesso para documentaçao básica
- Selecao limitada de verificações da AWS Trusted Advisor (baseado em 5 pilares)
- AWS Personal Health Dashboard  


Suporte Developer(possui todos os beneficios anterior)
- Orientação de noas práticas recomendadas
- Ferramentas de diagnóstico do cliente
- Suporte à construção da arquitetura

Suporte Business(possui todos os beneficios anteriores)
- Orientação de caso de uso
- Todas as verificaçoes do AWS Trusted Advisor
- Suporte limitado para software de terceiros.

Suporte Enterprise On Ramp/Enterprise (possui todos os beneficios anteriores)
- Orientação de arquitetura para aplicações
- Gerenciamento de evento de infraestrutura
- Gerente técnico de conta (TAM) disponível.
