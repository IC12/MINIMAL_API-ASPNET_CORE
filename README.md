# Curso da Microsoft Learn: Criar uma API Web com API mínima, ASP.NET Core e .NET

.NET 6 precisa estar instalado na sua máquina

- Para criar o projeto mínimo de API digite 'dotnet new web -o PizzaStore -f net6.0' no terminal da IDE;
- Para usar o Swagger e a interface do usuário na API, instale o pacote Swashbuckle;
    (Digite 'dotnet add package Swashbuckle.AspNetCore --version 6.1.4'
        'dotnet add package Swashbuckle.AspNetCore --version 6.2.3')
- Para instalar o pacote EntityFrameworkCore, digite 'dotnet add package Microsoft.EntityFrameworkCore.InMemory --version 6.0';
- No terminal digite 'dotnet run' para executar o aplicativo;
- No navegador: vá até o ponto de extremidade swagger 'http://localhost:{PORT}/swagger'
    (A PORT vc encontra no arquivo launchSettings.json)
- Esse é o suporte para OpenAPI para a API mínima usando Swagger;
- No terminal, tecle ctrl+C para encerrar o porgrama.


Até então os dados testados estavam sendo salvos no banco de dados em memória e sendo perdidos ao reiniciar o app.
Para persistir os dados, vamos usar o banco de dados relacional SQLite para armazenar os mesmos.

- Instale o provedor do SQLite para EF Core 'dotnet add package Microsoft.EntityFrameworkCore.Sqlite --version 6.0';
- Istale a ferramenta para realizar tarefas de desenvolvimento de tempo de design 'dotnet tool install --global dotnet-ef';
- Pacote que contém toda a lógica de tempo de design para EF Core criar o banco 'dotnet add package Microsoft.EntityFrameworkCore.Design --version 6.0';
- EF Core cria uma pasta chamada Migrações no diretório que contém arquivos com migrações do banco de dados 'dotnet ef migrations add InitialCreate';
- Aplicar as migrações 'dotnet ef database update'.


# Criação de app pilha completa front-end usando React e API Minimal para ASP.NET Core

- Para criar um app React que funcione rápido, vamos usar o scaffolder create-react-app usando npx;
- Num terminal, crie o app usando 'npx create-react-app pizza-web'. Obteve um diretório chamado pizza-web;
- Para iniciar o app, 'cd pizza-web' e em seguida 'npm start';
- No navegador, acesse http://localhost:3000;
- Pressione Ctrl+C para encerrar a execução;
- Para melhorar a aparência da interface do usuário, uma das sugestões seria usar a biblioteca styled-components;
    (Digite 'npm add styled-components' depois 'npm install')
    
- Iniciar servidor fictício 'npx json-server --watch --port 5000 db.json';
- No mesmo local do subdiretório PizzaStore execute 'dotnet ef database' para aplicar as migrações dbs com tabelas;
    (Se o dotnet ef não puder ser encontrado 'dotnet tool install -g dotnet-ef', e repita o comando anterior)