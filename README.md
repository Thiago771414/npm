# NPM (Node Package Manager) 

## Introdução ao NPM
O NPM (Node Package Manager) é uma ferramenta poderosa que vem junto com o Node.js e atua como um gerenciador de pacotes para projetos JavaScript. Ele permite que os desenvolvedores instalem, gerenciem e compartilhem facilmente pacotes e bibliotecas de código reutilizáveis.

## Pacote e Package.json
No NPM, um pacote é uma coleção de código reutilizável que pode ser facilmente instalado e usado em seus projetos. Cada pacote normalmente inclui um conjunto de arquivos, juntamente com um arquivo package.json que contém metadados e configurações importantes para o pacote.

## Entendendo o Package.json
package.json: Este arquivo é o coração de todo projeto NPM. Ele contém informações essenciais sobre o seu projeto, como nome, versão, dependências, scripts e muito mais. O arquivo package.json ajuda o NPM a entender como lidar com seu projeto e suas dependências.

## Três Tipos de Módulos
Ao trabalhar com o NPM, você encontrará três tipos de módulos:

Módulos Core (Internos): São módulos integrados que vêm com o próprio Node.js, como process, os e dns. Você pode usá-los diretamente em seu código sem precisar instalar nada adicional.

Módulos Locais: São módulos que você cria dentro do seu projeto. Eles podem ser armazenados em arquivos separados, e você pode organizar a funcionalidade do seu projeto em unidades menores e mais gerenciáveis.

Módulos de Terceiros: Esses módulos são criados por outros desenvolvedores e estão disponíveis no registro do NPM. Alguns exemplos populares incluem express para criar aplicativos da web e mongoose para trabalhar com bancos de dados MongoDB.

## Contexto Global e Local
Ao trabalhar com pacotes do NPM, é essencial entender a diferença entre o contexto global e local:

Contexto Global: Refere-se ao sistema de computador como um todo, e os pacotes instalados globalmente podem ser acessados a partir de qualquer projeto. No Windows, os pacotes globais geralmente estão localizados em %app-data%\Roaming\npm\node_modules.

Contexto Local: Refere-se ao contexto específico do seu projeto. Pacotes locais são instalados na pasta node_modules dentro do diretório do seu projeto. Para executar pacotes instalados localmente, você pode usar npx para executá-los sem configurar o PATH do sistema.

## Inicializando um Package.json
Para inicializar um arquivo package.json para o seu projeto, você pode usar o seguinte comando:
````json
  npm init
````
Esse comando irá guiá-lo pelo processo de criação de um arquivo package.json. Ele solicitará várias informações sobre o seu projeto, como o nome do pacote, versão, descrição, autor e muito mais. Você também pode especificar o ponto de entrada do seu projeto (geralmente index.js) e adicionar palavras-chave para descrever o seu projeto.

## Instalando Módulos
Você pode instalar módulos do NPM localmente ou globalmente. Módulos locais são instalados na pasta node_modules dentro do seu projeto, enquanto módulos globais são acessíveis em todo o sistema.

Para instalar um módulo localmente, use o seguinte comando:
````json
  npm install express
````
Você também pode instalar uma versão específica de um módulo:
````json
  npm install express@3.0.0
````
Ao instalar um módulo, você pode usar a opção --save ou --save-dev para adicionar o pacote ao seu arquivo package.json como uma dependência ou uma dependência de desenvolvimento, respectivamente.

## Entendendo a Estrutura do Package.json
O arquivo package.json tem uma estrutura específica que contém informações importantes sobre o seu projeto. Aqui estão alguns dos campos-chave:
````json
"name": "O nome do seu pacote".
"version": "A versão do seu pacote".
"description": "Uma breve descrição do seu pacote".
"homepage": "A URL do site do seu pacote".
"contributors": "Nomes dos colaboradores do pacote".
"dependencies": "Uma lista de dependências necessárias para o funcionamento do seu pacote".
"devDependencies": "Uma lista de dependências usadas apenas no ambiente de desenvolvimento".
"main": "O ponto de entrada do seu pacote".
"scripts": "Scripts personalizados que podem ser executados usando npm run".
"keywords": "Palavras-chave que descrevem o seu pacote para facilitar a descoberta".
````
## Gitignore
O arquivo .gitignore é usado para especificar quais arquivos e diretórios devem ser ignorados pelos sistemas de controle de versão, como o Git. Ele ajuda a excluir arquivos desnecessários, como a pasta node_modules e outros artefatos de construção, para que não sejam rastreados no repositório.

## Comandos da CLI do NPM
npm list: Lista os pacotes instalados no contexto local.

npm list -g: Lista os pacotes instalados globalmente.

npm outdated: Mostra uma lista de pacotes desatualizados que precisam de atualizações.

npm update: Atualiza os pacotes desatualizados para suas versões mais recentes.

## Versionamento Semântico
Ao especificar dependências em seu package.json, você pode usar o versionamento semântico para definir as restrições de versão de um pacote. O versionamento semântico consiste em três partes: MAJOR.MINOR.PATCH.

MAJOR: Representa versões principais com mudanças que quebram a compatibilidade.
MINOR: Representa novas funcionalidades e mudanças compatíveis com versões anteriores.
PATCH: Representa correções de bugs e mudanças compatíveis com versões anteriores.
Você pode usar diferentes sintaxes na seção dependencies para especificar intervalos de versão:

````json
"dependencies": {
  "express": "4.16.3",    // Versão exata 4.16.3
  "express": "^4.16.3",   // Aceita versões 4.*.*
  "express": "~4.16.3",   // Aceita versões 4.16.*
  "express": ">4.16.3",   // Aceita versões superiores a 4.16.3
  "express": ">=4.16.3",  // Aceita versões superiores ou iguais a 4.16.3
  "express": "<4.16.3",   // Aceita versões inferiores a 4.16.3
  "express": "<=4.16.3"   // Aceita versões inferiores ou iguais a 4.16.3
}
````
## Conclusão
O NPM é uma ferramenta essencial para gerenciar projetos JavaScript. Ele permite que você instale, atualize e compartilhe pacotes facilmente. Entender a estrutura do package.json e o versionamento semântico ajudará você a trabalhar de forma eficiente com o NPM e manter as dependências do seu projeto organizadas. Boa codificação!


