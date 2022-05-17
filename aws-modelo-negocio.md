## Benefícios de se usar a AWS

Segurança
Confiabilidade (preparada para se recuperar de resgates)
Alta disponibilidade
Agilidade (tudo pelo console)
Cobrança On Demand
Escalabilidade (aumentar a infraestrutura, ex: máquina)
Elasticidade (Aumentar e diminuir a infraestrutura de acordo com a necessidade da aplicação)
Alcance Global
Economia de escala

## Valor da nuvem AWS

Redução de custos
Produtividade em equipe
Resiliênica operacional
Agilidade empresarial

### License Manager

Se temos licenças de softwares, podemos levá-las para dentro da imfraestrutura da aws se, custos.

### Redução de custos através da Nuvem

- Right Sizing - Encontrar o tamanho correto de recursos para a aplicação.
- Automação - Automatizar processos e padrões paara reduzir cliques e custos.
- Redução do escopo de conformidade
- Serviços gerencaidos (a manutenção é responsabilidade da AWS).


### Designs de Nuvem 

Design a prova de falhas

	- Redundancia, infraestrutura em diferentes Availability zones.

	- Serviços gerenciados oferecem soluções automáticas de 	  recuperação de falha.  
	- Diferença entre recuperação de desestres e tolerância a falhas.

Desacoplamento de componentes  
	- Arquitetura em microsserviços  

Arquitetura Elástica  
	- Capacidade de diminuir e aumentar recursos computacionais 	  conforme a demanda.

Pensamento Paralelo  
	- Possibilidade de resolver mais de uma demanda conforme 	necessário.   


## Segurança e conformidade  

### Modelo de responsabilidade compartilhada da AWS   
https://aws.amazon.com/pt/compliance/shared-responsibility-model/

AWS é responsável pela segurança "da" neuvem (of the cloud).
CLIENTE é responsável pela segurança "na" nuvem (in the cloud).

Responsabilidades variam conforme o serviço: 

IaaS - Infrastructure as a Service  
PaaS - Platform as a Service 
SaaS - Software as a Service 

Cada um dos acima, corresponderá da melhor maneira conforme a necesidade da aplicação (não existe um modelo melhor que outro).

O cliente é responsável por dados sensível e permicionamento.

### Responsabilidade da AWS
- Proteger a infraestrutura que executa todos os serviços da AWS.
- Hardware, software, redes, instalações 

# Segurança
## Compliance (Conformidade)
https://aws.amazon.com/pt/compliance

- Estar de acordo com os padrões de segurança do mercado.  
Deve estar em conformidade com os padrões:  

HIPAA/HITECH
SOC
PCU/DSS
LGPD (https://aws.amazon.com/pt/compliance/brazil-data-privacy/)
Serviços cobertos  


### Criptografia de dados na AWS

Opções: 

AMAZON KMS (Seviço recoemendado)
Cliente pode gerenciar as próprias chaves ou a AWS se responsabiliza por elas.  

### Auditoria e Relatórios 

- CloudTrail (Auditoria) - Log sobre o que as pessoas estão fazendo na conta. Quem subiu uma máquina? Quem criou um bucket? etc.
	- Data Event (Eventos de dados sobre operações específicas, ex: o put de um objeto no S3, o create de um item numa lambda) e Manegement Events (quem fez uma ação na nuvem)

- CloudWatch  (logs, métricas, monitoramento)
	- Realização e coleta de logd e métricas 
	- Métricas incorporadas e personalizadas
	- Visualizações de métricas, criação de dashboards
	- Criação de alarmes  

- AWS Config 
	- Gerenciar o histórico de configurações
	- Detecção na mudança de configurações.


### Gerenciamento de usuários

- Least Privilege Princeple -> Regra dos menores privilégios
	- Uma conta deve ter permissão de acesso apenas para os recursos que serão utilizados.
- Controle e auditoria
- IAM (gerencia usuários, credenciais, chave de gerenciamento para chamadas via api via ssh, alternancia de senha, controle de autenticação MFA[MULTIFACTOR AUTHENTICATION]).

Detalhes: https://www.learnaws.org/2022/03/03/iam-roles-policies/#:~:text=to%20multiple%20entities.-,IAM%20Roles%20vs.,to%20access%20any%20AWS%20resources.


#### User, groups(Permissionar o grupo) e roles(permissão para aplicações que estão fora da conta, não são usuários da conta, exe: Grafana) (Esses tres itemns compõeem o IAM).
	- Root account AWS -> Possui todos os privilégios(inclusive de contratar serviços, faturamento, encerrar conta, etc). Ela não deve ser utilizada para serviços diários.
	- O ideal é utilizar IAM para criar um usuário para as tarefas necessárias.
	- Policy - definição entre uma ou mais permissões da aws.


### Recursos para suporte de segurança

- Amazon WAF (serviço de firewall de aplicação web)
- Network Access List (Firewall de recursos da nuvem)
- Security Groups (Firewall restristo de máquina e recursos de um grupo)
- AWS Marktplace (soluções de parceiros que podem ser adquiridas)



#### Trusted Advisor  
- Serviço de recomendações de melhores práticas
- Um de seus pilares é a segurança
