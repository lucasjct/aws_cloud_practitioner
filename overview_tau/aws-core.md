### Core dos serviços de computação da AWS

#### Categorias  

* Computação  
* Armazenamento
* Rede
* Banco de Dados  

#### Computação:  
* EC2  
* Lightsail(voltados para plataforma)  
* ECS/EKS (Voltados para plataforma - docker e containers)  
* Beanstalk ()
* Lambda (Serveless)   

#### EC2  

EC2 são máquinas virtuais, possui diferentes modos de precificação.

Disponibilibilidade dos serviços: On-demand, Reserved Instance, Spot Instance e Dedicated Host.    

EC2 - Placement Groups  (Como podemos organizar nossas instâncias?)  

* Cluster: instâncias mais próximas
	- Baixa latência, high workload, HPC

* Partition: divide instâncias em partições tal dorma que cada partição não divide o mesmo hardware.

	- Replicação de workloads, workloads distribuídos, handoop, cassandra

* Spread: divide instâncias de tal forma que cada instância não compartilha o mesmo hardware.   
	-  workload crítico, redução de falhas e mix de instances types

link: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html   


#### EC2 - Instance Families  

* Uso Geral:
	- M Family
	- Burstable instances -T family (Burt above limit)
	- Mac
* Compute Optimized - C Family
* Memory Optimized - R,X,U and Z Family  
* Accelerated Computing - P, inf, G and F Family
* Storage Optimized - I, D and H Family.


link: https://aws.amazon.com/pt/ec2/instance-types/  


### EC2 Storage (Tipo de armazenamento nas instâncias)  

* Instance Store (quando termino minha instância, o dados são excluídos). Voltado para teste...
* EBS (Dado persistentes, se termino a instância, mantenho os dados). Voltado para quando colocamos uma aplicação em produção. Podemos esclher entre HD e SSD.  


### Ligthsail  
* Ajuda a construir um servidor para uma aplicação simples, de maneira amigável, passo a passo, facilidade de configurar. Usado para aplicações simples, ambientes de testes...  

###  ECS Elastic Container Service  

* Ferramenta para a orquestração de containers
* Orquestração gerenciada pela AWS
* Use cases: aplicação em microsserviços, batch workloads, docker containers.  


### ECS Features  
* AWS Copilot  (CLI especializada para o ECS) 
* AWS Outposts (Hack da AWS que auxilia fazer a configuração da aws, mas on premisse)  
* EC2 vs Fargate (gerencia as configurações da máquina).  

### Auto Scaling (serviço para garantir escalabilidade)   

* Possibilidade de aumentar e reduzir instâncias conforme necessário;  
	- Scale out, scale in  
* AutoScaling é um tipo de escalomanto vertical. Tipo de escalonamento que aumento e diminui máquinas.  

### Auto Scaling - Tipos de escalonamento  

* Manual (Tiro ou add não mão as instancias)
* Dinâmico - Cloud Watch alarm based (Configuro o melhor momento para subir as máquinas)
	- Target tracking
	- Simple Scaling
		- Cooldown (tempo limite para add ou rem uma máquina) 
	- Step Scaling (posso controlar a quantidade de máquinas)

* Predictive Scaling - Machine Learning to predict cycle traffic  
* Scheduled Scaling - Scheduled actions. Serve para nos antecipar e a partir de um determinado período, preparar a escalabilidade.   


### Load Balancers - Balanceadores de Carga  
* Distribui o tráfego na rede conforme o necessário.  

A AWS pode distribuir o load balance por tipos de protocoles dentro das camadas de redes. São eles:  

* Aplication Load Balancer -  Tráfego vindo da internet: aplicações web (HTTP/HTTPS) camada 7.   

* Network Load Balancer - Tráfego interno entre instâncias, bancos de dados, (TCP, TLS e UDP), camada 4.  

* Gatway Load Balancer - conexão direta com softwares terceiros: protocolo GENEVA.   


### AWS Elastic Beanstalk  
* Orquestrador totalmente gerenciado pela aws   
* Fácil deploy de aplicações, load balancers, auto scaling, groups.   


### Lambda  

* Function as a service  
* Infraestrutura é 100% gerenciada pela AWS  
* Servelss  (O servidor é gerenciado pela AWS, não que não exista sem servidor)
* Cold Starts  
* Timeout máximo de 15 minutos. 





