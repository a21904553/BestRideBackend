# BestRide Backend

## Instalação


Para poder correr o codigo é necessário ter a versão 3 do python
e em seguida correr os seguintes comandos na linha de comandos:

python -m pip install Django

-pip install djangorestframework

-pip install markdown

-pip install django-filter

-pip install mysqlclient

-python -m pip install boto3 

-python -m pip install urllib3

-pip install djangorestframework-gis

-pip install psycopg2

## Video

https://www.youtube.com/gxU4hCzMXTc


#Manual de Utilização
##Web Services utilizados:
####Login:
Recebe como argumento JSON com o username e a password;
Envia em JSON os dados do User (Turista);

####GetUser: 
Recebe como argumento o token do user;
Envia em JSON os dados do User (Turista);

####RecoverUser:
Recebe como argumento JSON com o email;
Envia em JSON a reposta se é possível efetuar a recuperação;

####UpdateUser:
Recebe como argumento o token do user;
Envia em JSON os dados do User (Turista);

####ChangePassword:
Recebe como argumento um JSON com a password antiga, a nova e o token do user;
Envia em JSON com a resposta se foi ou não possível mudar a password;

####SaveUser:
Recebe como argumento um JSON com o id do user, o email e a imagem;
Envia em JSON os dados do User (Turista);

####ConfirmRecoverUser:
Recebe como argumento um JSON com o email, o código (que foi enviado por e-mail) e a password nova;
Envia em JSON se foi possível efetuar a recuperação com ou sem sucesso;

####VerifyAccount:
Recebe como argumento um JSON com o email e o código que foi enviado para verificar a conta apos o login;
Envia em JSON os dados do User (Turista);


####ResendCode:
Recebe como argumento um JSON com email;
Envia em JSON a resposta do sucesso da operação

####CancelAccount:
Recebe como argumento um JSON com o token do user;
Envia em JSON como sucesso ou insucesso da operação;

####Translate:
Recebe como argumento um JSON com o texto e com a linguagem de output;
Envia em JSON com o texto traduzido para determinada lingua;

####ShowRoadVehicles
Recebe como argumento o id do roteiro;
Envia em JSON os dados da(s) viatura(s);

####ShowRoadMap:
Recebe como argumento um JSON com a distância máxima de uma determinada latitude e longitude (ambos os argumentos passados por JSON);
Envia em JSON os dados do(s) roteiros que cumpram a distância máxima passada no argumento;

####ShowInterestPoints:
Não recebe argumentos;
Envia em JSON com os dados de todos os pontos de interesse existentes de um determinado roteiro;

####ShowRoadMapsCity:
Recebe como argumento a cidade da qual se pretende os roteiros;
Envia em JSON os dados de todos os roteiros dessa cidade;

####GetRoadMapsByEnterprise:
Recebe como argumento o id da empresa;
Envia em JSON os dados de todos os roteiros criados pela empresa;

####GetRoadMapsById:
Recebe como argumento o id do roteiro;
Envia em JSON os dados do roteiro;

####CreateRoute:
Recebe como argumento um JSON com os dados do roteiro;
Envia em JSON os dados do roteiro (incluindo o id do roteiro);

####DeleteRoute:
Recebe como argumento o id do roteiro;
Envia em JSON o sucesso ou insucesso da operação;

####GetVehicle:
Não recebe argumentos;
Envia em JSON os dados de todos os veículos;

####PostVehicle:
Recebe como argumento em JSON os dados do veículo;
Envia em JSON os dados do veículo (incluindo o id do veículo);

####DeleteVehicle:
Recebe como argumento o id do veículo;
Envia em JSON o sucesso ou insucesso da operação;

####GetVehicleByEnterprise:
Recebe como argumento o id da empresa;
Envia em JSON os dados do(s) veículo(s) da empresa;

####GetVehicleById:
Recebe como argumento o id do veículo;
Envia em JSON os dados do veículo;

####UpdateVehicle:
Recebe como argumento o id do veículo e um JSON com os dados do veículo;
Envia em JSON os dados atualizados do veículo;

####GetComments:
Recebe como argumento o id do comentário;
Envia em JSON os dados do comentário;

####PostComments:
Recebe como argumento um JSON com os dados do cometário;
Envia em JSON os dados do comentário (incluindo o id do comentario);

####GetAverageComments:
Recebe como argumento o id do roteiro;
Envia em JSON a média de todos os comentários de um determinado roteiro;

####GetTravels:
Não recebe argumentos;
Envia em JSON com todas as viagens existentes;

####Travels:
Recebe como argumento o id do turista;
Envia em JSON os dados de todas as viagens do turista;

####CreateTravel:
Recebe como argumento um JSON com os dados de uma nova viagem;
Envia em JSON os dados da viagem (incluindo o id da viagem);

####CreatePointInterest:
Recebe como argumento um JSON com os dados de um novo ponto de interesse;
Envia em JSON os dados do ponto de interesse (incluindo o id do ponto de interesse);

####GetPointInterest:
Não recebe argumentos;
Envia em JSON os dados de todos os pontos de interesse;

####MakePayment:
Recebe como argumento um JSON com o preço a pagar e com o token do turista;
Envia em JSON o sucesso ou insucesso da operação;

####UploadImage:
Recebe como argumento um JSON com o nome do ficheiro;
Envia o sucesso ou insucesso da operação;


####LoginDriver:
Recebe como argumento JSON com o username e a password;
Envia em JSON os dados do condutor;

####GetDriver: 
Recebe como argumento o token do condutor;
Envia em JSON os dados do condutor;

####RecoverDriver:
Recebe como argumento JSON com o email;
Envia em JSON a reposta se é possível efetuar a recuperação;

####UpdateDriver:
Recebe como argumento o token do condutor;
Envia em JSON os dados do condutor;

####ChangePasswordDriver:
Recebe como argumento um JSON com a password antiga, a nova e o token do condutor;
Envia em JSON com a resposta se foi ou não possível mudar a password;

####SaveDriver:
Recebe como argumento um JSON com o id do condutor, o email e a imagem;
Envia em JSON os dados do condutor;

####ConfirmRecoverDriver:
Recebe como argumento um JSON com o email, o código (que foi enviado por e-mail) e a password nova;
Envia em JSON se foi possível efetuar a recuperação com ou sem sucesso;

####VerifyAccountDriver:
Recebe como argumento um JSON com o email e o código que foi enviado para verificar a conta apos o login;
Envia em JSON os dados do condutor;


####ResendCodeDriver:
Recebe como argumento um JSON com email;
Envia em JSON a resposta do sucesso da operação

####CancelAccountDriver:
Recebe como argumento um JSON com o token do condutor;
Envia em JSON como sucesso ou insucesso da operação;

####PostEmergencyContact:
Recebe como argumento um JSON com os dados do contacto de emergência;
Envia em JSON os dados do contacto de emergência;

####PostFKDriverEnterprise:
Recebe como argumento um JSON com o id do condutor e da empresa;
Envia em JSON os dados do condutor e da empresa;

####LoginEnterprise:
Recebe como argumento JSON com o username e a password;
Envia em JSON os dados da empresa;

####GetDriverEnterprise: 
Recebe como argumento o token da empresa;
Envia em JSON os dados da empresa;

####RecoverDriverEnterprise:
Recebe como argumento JSON com o email;
Envia em JSON a reposta se é possível efetuar a recuperação;

####UpdateDriverEnterprise:
Recebe como argumento o token da empresa;
Envia em JSON os dados da empresa;

####ChangePasswordDriverEnterprise:
Recebe como argumento um JSON com a password antiga, a nova e o token da empresa;
Envia em JSON com a resposta se foi ou não possível mudar a password;

####SaveDriverEnterprise:
Recebe como argumento um JSON com o id da empresa, o email e a imagem;
Envia em JSON os dados da empresa;

####ConfirmRecoverDriverEnterprise:
Recebe como argumento um JSON com o email, o código (que foi enviado por e-mail) e a password nova;
Envia em JSON se foi possível efetuar a recuperação com ou sem sucesso;

####VerifyAccountDriverEnterprise:
Recebe como argumento um JSON com o email e o código que foi enviado para verificar a conta apos o login;
Envia em JSON os dados da empresa;

####ResendCode:
Recebe como argumento um JSON com email;
Envia em JSON a resposta do sucesso da operação

####CancelAccount:
Recebe como argumento um JSON com o token da empresa;
Envia em JSON como sucesso ou insucesso da operação;
