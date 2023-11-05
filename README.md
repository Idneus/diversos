Este projeto foi criado inicialmente com a única intenção de obter um maior range de distância para abertura e fechamento do portão da garagem.

Dispositivos:

Nodemcu V3;
Placa LoRa eByte E32-433T20D;
Antena 5 dbi.

Contextualizando:

Transmissor:
Nosso transmissor estará sempre instalado dentro no carro, com a ligação pós chave, desta forma sempre que o carro estiver ligado ele também estará.
Fiz uma formatação do envio de mensagem com um formato de Json, para que fosse possível adicionar mais informações ao toque do botão e não apenas on e off.
Foi adicionado ao mesmo uma forma de conexão ao wifi do hot spot do meu celular, mas esta não é a prioridade do receptor, mesmo não conectado continuará funcionando. Para que o timestam funcione também foi adicionado um server NTP e um delay para que espere alguns segundos após a conexão wifi para que inicie a conexão.

Receptor:
Nosso receptor ficará num local estratégico para favorecer a recepção com o mínimo de interferência, mas que também consiga conexão com o wifi.
Este ao iniciar fará a conexão no wifi principal da casa, e logo após ao server mqtt, publicará em tópicos específicos com um pequeno delay.
Foi configurado para que o tópico a ser transmitido quando receber o sinal do transmissor seja composta pelos dados em Json e publicado no mqtt em tópico específico.
Ainda estou tentando configurar corretamente o mqtt Discovery para que seja automaticamente criada uma entidade no mqtt do Home Assistant.



A intenção inicial permanece, mas agora tendo pouco mais de noção sobre as ferramentas e dispositivos que possuo pretendo estudar e ampliar a aplicação destes.

