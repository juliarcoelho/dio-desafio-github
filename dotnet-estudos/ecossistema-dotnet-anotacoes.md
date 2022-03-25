# .NET
## .NET vs ASP .NET
- dotnet é uma plataforma de desenvolvimento com várias ferramentas, *linguagens de programação* e bibliotecas que permitem o desenvolvimento de diversos tipos de aplicações. 
- asp .net é um framework que estende .net para a criação de web apps - ou seja o asp .net fica DENTRO do dotnet
- dotnet core - mac, windows, linux
- dotnet framework - windows (ta defasado e fraco desempenho)
- linguagens de programação: C-sharp, F-sharp, Visual Basic (C# é a mais usada dessas)
- asp .net e asp .net core só muda o desempenho pq o core é mais novo
*typescript é da microsoft*  
## .NET framework
- focado em windows
- JIT - just in time compiler
- cada linguagem tem seu compilador mas no .net ao invés do compilador já compilar a linguagem de alto nível pra uma linguagem que o pc entende, ele compila em uma linguagem intermediaria aí entra o JIT que traduz em tempo de execução traduzir a linguagem pra uma linguagem de maquina
- gerenciamento de memória
- sistemas de tipos comum > tipos definidos pelo próprio framework
- interoperabilidade entre linguagens
- compatibilidade de versões
- usa .net standard

## .NET e .NET core
- plataforma cruzada (linux, windows e mac)
- open source
- base de código unica 
- .NET = .NET core + framework + tamarin + mono
- bibliotecas modularizadas (melhor desempenho)
### ASP .NET core
- apps web
- aplicações backend para mobile
- uso do padrão MVC (ASP .NET core MVC)
- model binding - mapear dado passado no navegador pra o controller
- model validation - validação automática no lado do cliente e do servidor
- razor pages e razor markup (substitui o MVC) - simplificado (razor markup + c# + HTML)
- blazor - framework que é executado no navegador
- integração com angular, recai e bootstrap
### xamarin
- plataforma de desenvolvimento mobile de alto desempenho
- open source
- cria interface nativa de cada plataforma (Android, iOS, macOS etc)
- possui os benefícios da plataforma .NET
- usa C#/XAML 
-> usa um código só pra Android e iOS (em c#/XAML) mas na hora de compilar para cada sistema é diferente
#### xamarin.forms 
- framework para desenvolvimento de interfaces
- unica base de código
- criação UI com XAML e lógica C#
- biblioteca xamarin.essecials
#### xamarin.android
- compila C# para uma linguagem intermediaria, e na hora da execução é compilado para linguagem nativa (JIT)
- executado no ambiente mono e ART
#### xamarin.iOS
- compilação do C# direto para linguagem nativa
- executado no ambiente mono e AOT (ahead of time)
- compilado antes da execução 
- não tem permissão para executar código gerado dinamicamente (linguagem intermediaria)
## padrões de codificação
### bom código
- confiável
- sustentável
- eficiente
- o mais simples possível
### padronização
- comunicação entre a equipe
- facilita manutenção do código
- documentação
- boas práticas (ex clean code)
### clean code
- conjunto de boas práticas para codar
- obtém maior legibilidade
- mais fácil fazer manutenção
- seguir as convenções da equipe
- KEEP IT STUPID SIMPLE
- devolver código mais limpo do que encontrou
- entender o problema e solucionar a partir da sua raiz
- ser consistente na escrita do código
- variáveis concisas e que passem a informação necessária
- atentar a necessidade de criar objetos de valor ao invés de uso de tipos primitivos
- evitar dependencias lógicas
- evitar condicionais negativas
#### regras para nomeação
- escolher nomes descritivos para classes, variáveis e métodos
- para variáveis semelhantes, faça uma distinção identificável (evitar exemplo1, exemplo2 mas sim exemplodetask etc)
- utilizar nomes que facilitam a leitura
- utilize constantes para guardar string a serem comparadas
- nua usar prefixos ou caracteres especiais
- métodos não devem ser grandes e devem possuir somente um objetivo/responsabilidade
- evitar a exigência de muitos parâmetros dentro do método
- evitar que uma função altere valores de outra classe sem ser a própria classe
- evitar flags desnecessárias
#### comentários
- evitar comentários desnecessário, o código tem que ser autoexplicativo
- não seja redundante
- não deixe código desnecessário comentado (polui o código, não é uma boa pratica)
- comentários são úteis para falar sobre a intenção de uma classe ou método
- comentários podem explanar regras mais complexas e alertas sobre consequências mais sérias 
#### regras de estruturação de código
- declarar variável perto de usar
- agrupar métodos similares
- declarar funções de cima pra baixo
- manter linhas curtas e poucas
- usar espaçamento e ideação correta
### convenções para nomeclatura
- camel case
-> escreve palavras ou frases compostas com a 1 letra sempre minúscula e a 1 letra das palavras que se seguem maiúsculas
> ex: valorDoDesconto  
- pascal case
-> escreve palavras ou frases compostas sempre a 1 letra de cada palavra sendo maiúscula
> ex: ValorDoDesconto  

*no C# nome de classes e métodos: PascalCase; nomes de variáveis e parâmetros: camelCase*
(no caso de interfaces recomenda-se o uso do prefixo “I”. Ex: IEntidade)

#### recomendações de microsoft
- uso do pascal case
-> classes
-> interfaces
-> membros de tipos públicos
- uso do camel case
-> campos privados e internos - deve ainda usar com prefixo “_”
-> campos estáticos privados ou internos -  usar prefixo “s_”
## ferramentas e linguagens
### ferramentas
- visual studio
-> IDE: ambiente de desenvolvimento integral
- visual studio code
-> editor de código
-> multiplataforma
- omniSharp
-> suíte de desenvolvimento integrada
-> voltado pra .NET
-> funciona em várias plataformas (inclusive o vscode)
- IONIDE
-> pacote de extensão do vscode (voltado pra F#)
- jetbrains rider
-> IDE
-> plataforma cruzada porém paga
-> usa ReShaper
- console (terminal)
-> incluida no SDK do .NET
### linguagens
- C#
-> popular
-> desenvolve qualquer tipo de aplicação para execução em qualquer plataforma
-> open source
-> baseada em C/C++ e influência de JAVA
-> POO
- F#
-> open source
-> mais utilizado pra ciência de dados
-> windows, linux, mac
-> bom desempenho
-> *paradigma funcional*, imperativo, poo
> enfatiza uso de funções  
> expressões ao invés de instruções  
> valores IMUTÁVEIS em variáveis  
> programação declarativa ao invés de imperativa  
- visual basic
-> dirigida a eventos
-> uma das linguagens mais utilizadas do mercado
-> visual basic .NET é uma linguagem derivada do visual basic mas é POO
#### outras linguagens suportadas
- javascript
- typescript (desenvolvida pela microsoft)
- python
- SQL
- C++
## o que usar e quando usar
### .NET
- necessidade de plataforma cruzada
- direcionamento de microsserviços
- necessitar de docker
-> hospedagem e infraestrutura linux e windows
- alto desempenho e escalonáveis
- necessidade de versões diferentes do .NET
### .NET framework
- quando não houver necessidade de migração para .NET
- biblioteca de 3os não disponíveis para .NET
- tecnologias não disponíveis para .NET

*ASP .NET core é melhor que o ASP .NET 4.x*

## o que usar pra cada tipo de aplicação
### aplicações desktop
- xamarin.MAC
### aplicações baseadas em containers
- AZURE: plataforma de nuvem completa que pode hospedar apps e simplificar o desenvolvimento de novos apps

## .NET standard
- é uma especie de interface que define as APIs que cada versão do .NET irá oferecer suporte

*plataforma cruzada é um termo para um software compatível com mais de um sistema*