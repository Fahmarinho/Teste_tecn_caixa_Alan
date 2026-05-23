## 🚀  SPREAD: Desafio Técnico de Testes de Software

Objetivo desse documento é ter uma visão simplificada do que foi elaborado no desafio técnico splicitado pela Spread cliente que envolve o 
ServeRest é uma API REST gratuita que simula uma loja virtual que aborda os seguintes fluxos:

- Usuários: `<Criação/ Listar/ Atualização / Exclusão>` 💻 *Pré-requisitos : N/A*
- Usuários: `<Criação Login >`  💻 *Pré-requisitos : Ter usuário*
- Produtos :`<Criação/ Listar/ Atualização / Exclusão>` 💻 *Pré-requisitos : Ter usuário,Login e Token ativo

   **💻 *Pós condição:	`#RRGGBB`** através da API listar produtos Validar processos adição de um novo produtos, estorno de produtos ou diminuição da quantidade da sua quantidade no estoque
- Carrinho :`<Criação/ Listar/Exclusão/ Cancelar compra>` 💻 *Pré-requisitos : Ter usuário,Login, Produtos cadastrados e Token ativo*
    *💻 *Pós condição:* através da API listar produtos Validar processos estorno de produtos ou diminuição da quantidade da sua quantidade no estoque

### Toda API que estiver com ícone de um cadeado requer autenticação via Token, nesse testes da Spread o utilizado é o *Bearer token*, durante os processos de envio de Requisições que requer autorização irá apresentar a seguinte mensagem:

*"Token de acesso ausente, inválido, expirado ou usuário do token não existe mais"*

Por padrão de configuração da *Serverrest* a duração da autorização é de 10 minutos, então quando o token de acesso expirar, sua aplicação deverá gerar um novo Token de autorização

*Ponto de atenção:* Para obter  ganho de tempo e assim obter mais produtividade na execução dos seus testes é recomedado que token esteja previamente automatizado via script ou variável para facilitar utilização do mesmo em todas as APIs que possui o mesmo como *Pré-Condição* :


###  APIs que tem como  *Pré- Condição* a geração do Tokem:
- API de Usuários: `<Cadastro/ Atualização / Exclusão>`
- API de Produtos :`<Cadastro/ Atualização / Exclusão>`
- API de Carrinho :`<Cadastro/ Atualização / Exclusão>`



### Como Gerar um novo Token

Ponto de atenção: Para obter  ganho de tempo e assim obter mais produtividade na execução dos seus testes é recomedado que token esteja previamente automatizado no script ou variável para facilitar utilização do mesmo em todas as APIs que possui o mesmo como *Pré-Condição* :

1. Executar a API de *Criação de usuário*
2. Executar a API de *Realizar Login*
3. Realizar a atualização do token gerado na própria Variável (global ou ambiente)  via ou Script ṕara funcionamento geral das requisições que necessitam do mesmo


### ATIVIDADES

Estruturação/escrita de ao menos 3 casos de teste contemplando cenários: positivos (fluxo básico e alternativos) e
cenários negativos (fluxos de exceção):


Cobertura de testes da API de Usuário:

1. Positivo (201): *Criar usuário*
2. Negativo (400) : * Cadastro de usuário com e-mail existente*

Cobertura de testes da API de Login:

1. Positivo (200): *Realizar Login com credenciais válidas   (Status code 200)*
2. Negativo (401) : * Realizar Login com senha incorreta   (Status code 401)*
   
Cobertura de testes da API de Produtos:
   
1.Nagativo (401) *Tentar cadastrar produto sem token (Status code 401 )*
2.Positivo (201): *Cadastro de produto com sucesso*
3.Fluxo FA (400 ): * Cadastrar produto com nome já existente*


Cobertura de testes da API de Carrinho:

1. Positivo (201) : *Criar um carrinho contendo produtos válidos*
2. Negativo (400 ) : *Adicionar quantidade de produto acima do estoque disponível*
3. Negativo (400) :Tentar cadastrar mais de um carrinho para um único  usuário*
4. Fluxo FA (200) : Cancelar compra devolvendo produtos ao estoque 
    
## 💻 Pré-requisitos

Antes de começar, verifique se você atendeu aos seguintes requisitos:

- Você instalou a versão mais recente de `<linguagem / dependência / requeridos>`
- Você tem uma máquina `<Windows / Linux / Mac>`. Indique qual sistema operacional é compatível / não compatível.
- Você leu `<guia / link / documentação_relacionada_ao_projeto>`.

## 🚀 Instalando <nome_do_projeto>

Para instalar o <nome_do_projeto>, siga estas etapas:

Linux e macOS:

```
<comando_de_instalação>
```

Windows:

```
<comando_de_instalação>
```

## ☕ Usando <nome_do_projeto>

Para usar <nome_do_projeto>, siga estas etapas:

```
<exemplo_de_uso>
```
<img src="imagem.png" alt="Exemplo imagem">

> testes Linha adicional de texto informativo sobre o que o projeto faz. Sua introdução deve ter cerca de 2 ou 3 linhas. Não exagere, as pessoas não vão ler.

Adicione comandos de execução e exemplos que você acha que os usuários acharão úteis. Forneça uma referência de opções para pontos de bônus!

## 📫 Contribuindo para <nome_do_projeto>

Para contribuir com <nome_do_projeto>, siga estas etapas:

1. Bifurque este repositório.
2. Crie um branch: `git checkout -b <nome_branch>`.
3. Faça suas alterações e confirme-as: `git commit -m '<mensagem_commit>'`
4. Envie para o branch original: `git push origin <nome_do_projeto> / <local>`
5. Crie a solicitação de pull.

Como alternativa, consulte a documentação do GitHub em [como criar uma solicitação pull](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).

## 🤝 Colaboradores

Agradecemos às seguintes pessoas que contribuíram para este projeto:

<table>
  <tr>
    <td align="center">
      <a href="#" title="defina o título do link">
        <img src="https://avatars3.githubusercontent.com/u/31936044" width="100px;" alt="Foto do Iuri Silva no GitHub"/><br>
        <sub>
          <b>Iuri Silva</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="#" title="defina o título do link">
        <img src="https://s2.glbimg.com/FUcw2usZfSTL6yCCGj3L3v3SpJ8=/smart/e.glbimg.com/og/ed/f/original/2019/04/25/zuckerberg_podcast.jpg" width="100px;" alt="Foto do Mark Zuckerberg"/><br>
        <sub>
          <b>Mark Zuckerberg</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="#" title="defina o título do link">
        <img src="https://miro.medium.com/max/360/0*1SkS3mSorArvY9kS.jpg" width="100px;" alt="Foto do Steve Jobs"/><br>
        <sub>
          <b>Steve Jobs</b>
        </sub>
      </a>
    </td>
  </tr>
</table>

## 😄 Seja um dos contribuidores

Quer fazer parte desse projeto? Clique [AQUI](CONTRIBUTING.md) e leia como contribuir.

## 📝 Licença

Esse projeto está sob licença. Veja o arquivo [LICENÇA](LICENSE.md) para mais detalhes.
