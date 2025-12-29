1 - Objeto Pretendido

Pretende-se o desenvolvimento de um protótipo para um sistema de execução de tarefas de 
uma frota de robots e drones. O sistema será denominado RobDroneGo.  

O sistema deve ser constituído pelos seguintes módulos:  
• Gestão de dispositivos 
• Gestão de requisição de tarefas  
• Planeamento de execução de uma tarefa 

Tratando-se de um sistema protótipo, nem todos os módulos serão desenvolvidos e é aceitável 
que apenas algumas funcionalidades estejam implementadas, devendo constar no relatório de 
proposta quais as funcionalidades implementadas. 

2 - Visão geral

O ISEP pretende desenvolver uma solução para gestão de uma frota de drones e robots que 
possam executar tarefas no interior do seu campus. 

Considere que o ISEP adquire robots de dois tipos: 

• robisep: robot móvel que se movimenta através de um sistema de rodas podendo 
deslocar-se nos corredores dos edifícios ou através de elevadores entre pisos de um 
edifício, mas não consegue subir escadas. O robot pode ir de um edifício para outro, mas 
só através dos corredores cobertos de ligação entre edifícios1. Os robiseps podem ter 
instalados sistemas que efetuam diversas tarefas, tais como vigilância ou limpeza do 
corredor ou ainda acesso a uma sala/gabinete para buscar/entregar um item (por 
exemplo, um comando de um projetor ou uma caneta para quadro branco). 

• droneisep: drone que se movimenta no espaço exterior aos edifícios existentes no ISEP. 
O droneisep pode ir de um ponto para outro ponto do espaço deslocando-se através de 
trajetos em linha reta permitidos. As tarefas desses drones poderão ser várias, tais como 
fazer entregas de objetos, vigilância, aquisições de imagem, operações de limpeza de 
janelas exteriores, etc. 

Existirão os seguintes tipos de utilizadores do sistema:  
• Administrador de sistema – gere os utilizadores e autorizações dos mesmos  
• Gestor de frota – gere os dados dos robots e drones e tipos de tarefas 
• Gestor de campus – gere os dados dos percursos e mapas 
• Utente (aluno, docente, funcionário) – pede a execução de tarefas 

A solução pretendida deve permitir que o gestor de frota configure os robots e drones existentes 
para que possam mais tarde ser utilizados na execução de tarefas. 

Os utentes do campus podem registar-se no sistema para requisitar tarefas a serem executadas 
pelos robots e drones. Por exemplo:

- um docente pode registar-se no sistema e requisitar a entrega de canetas de quadro branco no seu gabinete. O sistema avaliará o pedido e escalonará 
a sua execução. Numa primeira fase, a aprovação de pedidos de tarefas bem como o seu 
escalonamento será efetuado de forma manual pelo Gestor de Tarefas, podendo no futuro 
evoluir para um sistema automático.

Para a execução do pedido o sistema irá planear o percurso 
que o dispositivo (drone ou robot) deve executar. Por exemplo:

- para ir de uma dada sala/gabinete do piso J2 (segundo piso do edifício J) para uma sala/gabinete do piso G4 (4º piso 
do edifício G) o caminho poderá ser: partir da sala/gabinete do 2º piso do edifício J para ir através 
do corredor para o 2º piso do edifício I; usar o corredor do 2º piso do edifício I para ir para o 2º 
piso do edifício H; usar o corredor do 2º piso do edifício H para ir para o 2º piso do edifício G; 
usar o elevador do edifício G para ir do 2º piso para o 4º piso e dirigir-se a sala/gabinete 
pretendido.
