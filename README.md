#Projeto de AMS
## REVISAO:
* Process Diagrams (Private and Public) � Represents regular
	flow between tasks, events and decision
	points to complete a process in the organization.

* Pools � independent organizational entities
	e.g. 	� Customer, Supplier, University, Laboratory
	represents a process Participant.
	Sequence flows cannot cross Pool boundaries
	Message flows can cross Pool boundaries

* Lanes � resource/role classes in the same organizational
	space and sharing common systems
	e.g 	- Sales Department, Marketing Department
		� Clerk, Manager, Engineer
	a sub-division of a Pool. Used to organize and
	categorize the activities of a Participant.
	Sequence flows can cross Lane boundaries


## BPMN
* pools:
	* BAIK manuten��o
		* lanes: Funcion�rios, Coordenador
	* BAIK ERP
	* BAIK CRM
	* BAIK TAXA��O
	* BAIK MEDIA��O
* participantes envolvidos somente em processos p�blicos
	* BICA
	* Cliente Particular
	* GatewayBank
* Processos:
	* 1 - Registo de cliente particular
	* 2 - Levantamento, Utiliza��o e Devolu��o da bicicleta
	* 3 - Servi�o de Manuten��o das bicicletas

#### Registo de cliente particular
* Cliente executa bike app primeira vez
	* Apresentado um form para fazer o seu registo
		* indicar dados (... detalhes no enunciado...)

* O BAIK-ERP � questionado sobre a corre��o da info:
	* verifica a valida��o de cada um dos dados (ver enunciado)
		* valido: envia para telemovel token de ativa��o
		* registo do cliente fica num estado pendente
* Caso Sucesso:
	* informa��o registada
	* aguarda max 4 horas que o token de ativa��o seja introduzido
	* se o cliente introduzir token na BIKE-APP:
		* conclui-se registo e ativa��o
		* enviando email da plataforma com a confirma��o~
* Caso Inv�lido:
	* tem at� 48 horas para alterar info para valida
		* caso contrario:
		* O registo inicial � eliminado do sistema



## UML
* atores que interagem com SI-BAIK:
	* Cliente Particular
	* Gateway Banc�ria
	* BIA
	* T�cnico do Departamente de Manuten��o
	* Coordenador do Departamente de Manuten��o
	* T�cnico do Departamente de Apoio ao Cliente
