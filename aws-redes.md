### Serviços de rede   

### VPC - Virtual Private Cloud  (serviço chave de redes da AWS).    

* Permite criar uma rede isolada, que a princípio não pode ser acessível da interntet  
* Subnets, são literalmente subporções da rede virtual (VPC). Cada subnet se situa em uma avaibility zone diferente:  
	* Network Access Control Lists: Listas que controlam o acesso, são stateless, ordena as regrras em prioridades.  

* Route Tables: Estão associadas a subnet e dizem pra onde deve ser roteados os IPs que chegam a subnet. 
  
* __Internet Gateway__. Ferramenta que possibilita que a VPC se comunique com a internet.


![](Imagem da Infraaestrutura de Rede AWS.)   


### Security Groups (Quem é que pode acessar a máquina e o que a máquina pode acessar fora da rede)    

Definição das regas Inbound(tráfego de entrada) e Outbound (Tráfego de saída).  
* Definem quais são os ips permitidos naquele grupo de segurança.  
* É possível especificar IPs ou outros security groups.  
* São statefull.  

### Amazon Route 53   

* Serviço de DNS - Domain Name System.   
* Mapeia IPs para domínios.  
* Routing policies:  

	* Simple routing: roteamento padrão, mais simples e sem nehuma especialidade;  
	* Filover routing: muda o roteamento conforme o IP para de responder (active-passive).  
	* Geolocation routing: Faz o roteamento de acordo com a geolocalização dos usuários (exemplo: brasilerio acessam o servidor em SP). 
	* Geo Proximity routing: faz o roteamento de acordo com a localização geográfica dos usuários e dos recurso. Possui regras mais complexas para definir o roteamento.
	* Latency-based routing: Roteamento para regiões de menor latência.  
	* Multivalue answer routing: Define um conjunto de IPs (porcentagem) e o Route 53 escolhe um para rotear.     
	* Weighted Routing: associa pesos a diferentes recursos para rotear.   


### Amazon Route 53 - Tipos de record  
* alias - aponta para o nome de um recursos AWS (específico do Route 53)  
* Tipo A:  endereço de IP (192.168.10.12)
* CNAME - nome do domínio (www.exemplocname.com)  
* MX - nome do servido de email     


link: https://docs.aws.amazon.com/pt_br/Route53/latest/DeveloperGuide/Welcome.html

### Amazon Cloud Front 

* Serviço de CDN (content delivery network) 
* Distribui conteúdos com baixa latência utilizando cache 
* Distribuir vídeo on demand (VOD) - Live stream  
* Definir uma oringin S3, EC2 ou outro webserver.   


### VPN  (São gerenciadas pela AWS)

* Sito-to-Site VPN - Totalmente gerenciada, coneta toda a VPC com uma rede privada, IPsec, VPN. 
* Client VPN - Totalmente gerenciada, TLS VPN, acesso aos recursos de qualquer lugar.  
* VPN Cloud Hub - Totalmente gerenciada, configurar inúmeras VPNs Site-to-Site.   


### Amazon Direct Connect  
* Conexão dedicada on-premises-nuvem
* Não passa pela internet, me conecto diretamente com os serviços da AWS.      
