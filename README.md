# GitHub Finder

Este é um projeto React com TypeScript que utiliza a API do GitHub. O projeto foi desenvolvido por Matheus Battisti, do canal "Hora de Codar".

![screencapture-github-finder-eight-gray-vercel-app-2023-11-22-10_44_31](https://github.com/jessica-sobreira/github_finder/assets/117686537/3f6d0436-44a6-47f4-a1f6-b92fde951185)

## Resumo do Componente Home em React

O componente `Home` é a página principal do projeto. Ele utiliza componentes funcionais, hooks do React e TypeScript para buscar e exibir informações de usuários do GitHub. Aqui estão os principais pontos:

### Importações
- Importa as interfaces e tipos necessários do diretório `../types/user`.
- Importa os componentes `Search`, `User` e `Error` de diretórios específicos.

### Estado e Hooks
- Utiliza o hook `useState` para gerenciar o estado do usuário (`user`) e um estado de erro (`error`), inicializados como `null` e `false`, respectivamente.

### Função `loadUser`
- Uma função assíncrona que recebe um nome de usuário como parâmetro.
- Reinicia o estado de erro e usuário para preparar a próxima consulta.
- Faz uma requisição à API do GitHub para obter informações do usuário.
- Trata o caso de usuário não encontrado (código de status 404) configurando o estado de erro.
- Extrai os dados relevantes da resposta e atualiza o estado do usuário.

### Renderização
- Retorna um JSX contendo o componente `Search` e condicionalmente os componentes `User` e `Error` com base nos estados de usuário e erro.

### Componentes Filhos
- Renderiza o componente `Search`, que permite aos usuários pesquisarem perfis do GitHub.
- Renderiza o componente `User` com as informações do usuário se o estado `user` não for nulo.
- Renderiza o componente `Error` se o estado `error` for verdadeiro.

---

*Este código representa uma página principal que integra a busca de usuários do GitHub e a exibição de informações do usuário em componentes React funcionais.*
