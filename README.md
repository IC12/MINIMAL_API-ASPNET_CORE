# Curso da Microsoft Learn: Criar uma API Web com API mínima, ASP.NET Core e .NET

.NET 6 precisa estar instalado na sua máquina

- Para criar o projeto mínimo de API digite 'dotnet new web -o PizzaStore -f net6.0' no terminal da IDE;
- Para usar o Swagger e a interface do usuário na API, instale o pacote Swashbuckle;
    (Digite 'dotnet add package Swashbuckle.AspNetCore --version 6.1.4')
- No terminal digite 'dotnet run' para executar o aplicativo;
- No navegador: vá até o ponto de extremidade swagger 'http://localhost:{PORT}/swagger'
    (A PORT vc encontra no arquivo launchSettings.json)
- Esse é o suporte para OpenAPI para a API mínima usando Swagger;
- No terminal, tecle ctrl+C para encerrar o porgrama.