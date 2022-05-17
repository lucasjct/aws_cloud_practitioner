## Domínio e faturamento  

### Comparação modelos de preço (pricing model)  

* On-demand (pague o que usar)  
* Caso que queira pagar antes, pague mais barato   

Precificação do EC2:  
* On-Demand  (Paga apenas pelo tempo que a máquina estiver utilizando)  
	* Cenário de não saber ou ter previsão do uso de recursos e gastos.  
* Spot  (50 % - 90 % de desconto, não garante a disponibilidade de 100%)  
	* Cenário para testes, em que não usarei como ambiente de produção, pequenos processamentos.    
* Reserved  (é um coprometimento de tempo que irá pagar pela máquina e em troca recebe o desconto)  
	* Cenário em que tenho certeza que o tempo que minha aplicação utilizará a máquina, tráfego esperado.  

 ### Instâncias Reservadas  

* Se comprometer a pagar adiantado  ou não (upfront)  
* Opção de modificar sua RI ou não (convertible)  

* Conforme fazemos o pagamento adiantado, teremos mais discontos em nossa hora máquina(upfront). * Convertible -  As instâncias podem ser convertíveis ou não. De acordo com o que foi comprometido, posso alterar os recursos da minha máquina. Dado o tempo de comprometimento, o pagamento adiantado e a opção se é convertível ou não, impactará no valor do desconto.  



### AWS Organization  

Voltada para BigCorps, opção para organizar diversas contas da AWS.  

* Recurso para agrupar contas da AWS
* A vantagem é ter o Billing unificado, auxilia na redução de custo, uma vez que, em economia de escala, ou seja quanto mais usamos as aplicações menor o custo,  todos estão agrupados em uma mesma conta.  
* Podemos compartilhar as instâncias reservadas entre as contas.   
* Palavra-chave (Consolidated  billing)  


### Identificação de recursos disponíveis para suporte e faturamento.    

* Cost Explorer - Visualizar e compreender gastos na AWS(pode definir tags e colocar no cost explorer, fitrar pela tag e ter acesso aos valores do serviço. É uma ferramenta visual).  

* AWS Cost Usage and Report  - Entrega relatório de gastos em um buckt S3.    

* Amazon Quick Sight - Ferramenta de BI que ingere dados e gera painéis  

* Billing Support Case - Tire dúvidas sobre a sua fatura.  

* Amazon Concierge - Suporte a nível empresarial para a coordenação de gsatos.    

### Ferramentas de exploração/monitoramente de gastos  
* AWS Budgets, configurar alertas de gasto na conta.
* Tags -> Habilitar cost allocation tags. (podemos tagear por ambientes, por aplicações, por responsável. Podeomos agrupar os custos por tag e visulizar no Amazon Quick Sight).  

keywords: Cost Allocation Tags (As tags trazem a ideia de agruopamento).    
  
