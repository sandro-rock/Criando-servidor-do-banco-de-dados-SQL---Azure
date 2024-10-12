# Criando-servidor-do-banco-de-dados-SQL---Azure
Criando servidor do banco de dados SQL - Azure

Faça login no portal do Azure.
No painel do Azure, procurando por "SQL Database" na barra de pesquisa e selecione "SQL Databases".
Criar uma instância de banco de dados
Clique em "+ Create" (Criar) ou "+ Add" para criar um novo banco de dados.

Preencha os detalhes:

Subscription: Selecione sua assinatura do Azure.
Resource Group: Crie ou escolha um grupo de recursos onde o banco de dados será armazenado.
Database Name: Nome do banco de dados.
Server: Selecione um servidor existente ou crie um novo:
Se estiver criando um novo servidor, você precisará definir um nome de servidor, localização e credenciais de login (nome de usuário e senha).
Compute + Storage: Escolha o tamanho e o desempenho do banco de dados conforme sua necessidade (pode ajustar para otimizar custo ou performance).
Backup Redundancy: Escolha o nível de redundância de backup (local ou geo-redundante).
Após preencher, clique em "Review + Create" e, em seguida, em "Create".

Configurar firewall e acesso
No painel de gerenciamento do servidor de banco de dados SQL, vá até as configurações de firewall.
Adicione o endereço IP do computador que irá se conectar ao banco de dados ou permita conexões de qualquer endereço IP (não recomendado para ambientes de produção).
Clique em "Salvar".

Conectar ao banco de dados
Após a criação, você pode se conectar ao banco de dados SQL usando ferramentas como:

Azure Data Studio
SQL Server Management Studio (SSMS)
Ao conectar, use o nome do servidor, nome do banco de dados, nome de usuário e senha criados anteriormente.

Criar tabelas e gerenciar dados
Depois de conectado, você pode usar comandos SQL padrão para criar tabelas, inserir dados e realizar consultas, como:

sql
Copiar código
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName NVARCHAR(50),
    LastName NVARCHAR(50),
    HireDate DATE
);

Dicas adicionais:
Monitoramento e alertas: Utilize o Azure Monitor para acompanhar o desempenho do banco de dados.
Segurança: Considere habilitar criptografia e outros recursos de segurança como Azure Defender.
