# Projeto de AMS
## REVISÃO:
* Process Diagrams (Private and Public) Represents regular
	flow between tasks, events and decision
	points to complete a process in the organization.

* Pools - independent organizational entities
	e.g.  Customer, Supplier, University, Laboratory
	represents a process Participant.
	Sequence flows cannot cross Pool boundaries
	Message flows can cross Pool boundaries

* Lanes - resource/role classes in the same organizational
	space and sharing common systems
	e.g 	- Sales Department, Marketing Department
		Clerk, Manager, Engineer
	a sub-division of a Pool. Used to organize and
	categorize the activities of a Participant.
	Sequence flows can cross Lane boundaries


## BPMN
* pools:
	* BAIK manutenção
		* lanes: Funcionários, Coordenador
	* BAIK ERP
	* BAIK CRM
	* BAIK TAXAÇÃO
	* BAIK MEDIAÇÃO
* participantes envolvidos somente em processos públicos
	* BICA
	* Cliente Particular
	* GatewayBank
* Processos:
	* 1 - Registo de cliente particular
	* 2 - Levantamento, Utilização e Devolução da bicicleta
	* 3 - Serviço de Manutenção das bicicletas

#### Registo de cliente particular
* Cliente executa bike app primeira vez
	* Apresentado um form para fazer o seu registo
		* indicar dados (... detalhes no enunciado...)

* O BAIK-ERP é questionado sobre a correção da info:
	* verifica a validação de cada um dos dados (ver enunciado)
		* valido: envia para telemovel token de ativação
		* registo do cliente fica num estado pendente
* Caso Sucesso:
	* informação registada
	* aguarda max 4 horas que o token de ativação seja introduzido
	* se o cliente introduzir token na BIKE-APP:
		* conclui-se registo e ativação
		* enviando email da plataforma com a confirmação
* Caso Inválido:
	* tem até 48 horas para alterar info para valida
		* caso contrario: O registo inicial é eliminado do sistema
* No final o cliente fica em ativo ou invalido. Em qualquer situação:
	* É enviado um email e uma notificação móvel ao cliente com a respectiva
	* notificação

#### Levantamento, Utilização e Devolução da bicicleta
* A qualquer momento, um cliente com BAIK-APP pode utilizar uma bica para isso:
	* escolhe modelo pretendido num local de estacionamento das bica
* Ao aceder à BAIK-APP o seu registo e aquisição são verificados:
	* Caso não esteja registado: processo de negócio termina
	* Caso esteja registado e aprovado: a aquisição do produto ativa e rune
	as condições para levantar a bicicleta
* Caso as condições de eligibilidade para aceder ao serviço sejam cumpridas
é pedido ao cliente:
	* introduza o número da VICA (para emparelhar com dispositivo movel do
		cliente e saber onde esta o cliente e com que bicicleta)
	* é verificado pelo  BAIK-ERP se o cliente tem montante disponivel e
		suficiente para a reserva inicial (de acordo com modalidade de pagamento)
	* Caso as condições anteriores se verifiquem:
		* a bicicleta é desbloqueada remotamente
		* assume-se que o cliente está a utilizar o Serviço
* Assim, cada BICA vai continuamente emitindo a sua localização para o
  BAIK-MEDIAÇÃO

## UML
* atores que interagem com SI-BAIK:
	* Cliente Particular
	* Gateway Bancária
	* BICA
	* Técnico do Departamente de Manutenção
	* Coordenador do Departamente de Manutenção
	* Técnico do Departamente de Apoio ao Cliente
