## 🚀  SPREAD: Desafio Técnico de Testes de Software

Objetivo desse documento é ter uma visão simplificada do que foi solicitado e elaborado nos documentos de evidências solicitado no desafio técnico splicitado pela Spread cliente que envolve o  ServeRest é uma API REST gratuita que simula uma loja virtual que aborda a criação dos seguitens fluxos :

1. API Usuários : <Criação/ Listar/ Atualização / Exclusão>`
2. API Login: <Criação Login >`
3. API Produtos : <Criação/ Listar/ Atualização / Exclusão>`
4. API Carrinho : <Criação/ Listar/Exclusão/ Cancelar compra>`


## 🚀  SPREAD: Desafio Técnico de Testes de Software:

**Toda API que estiver com ícone de um cadeado requer autenticação via Token, nesse testes da Spread o utilizado é o *Bearer token*, durante os processos de envio de Requisições que requer autorização irá apresentar a seguinte mensagem:**

*"Token de acesso ausente, inválido, expirado ou usuário do token não existe mais"*

Por padrão de configuração da *Serverrest* a duração da autorização é de 10 minutos, então quando o token de acesso expirar, sua aplicação deverá gerar um novo Token de autorização

**Ponto de atenção:** Para obter  ganho de tempo e assim obter mais produtividade na execução dos seus testes é recomedado que token esteja previamente automatizado via script ou variável para facilitar utilização do mesmo em todas as APIs que possui o mesmo como *Pré-Condição* :

**APIs que tem como  *Pré- Condição* a geração do Tokem:**

- API de Usuários: `<Cadastro/ Atualização / Exclusão>`
- API de Produtos :`<Cadastro/ Atualização / Exclusão>`
- API de Carrinho :`<Cadastro/ Atualização / Exclusão>`

**Como Gerar um novo Token**

Ponto de atenção: Para obter  ganho de tempo e assim obter mais produtividade na execução dos seus testes é recomedado que token esteja previamente automatizado no script ou variável para facilitar utilização do mesmo em todas as APIs que possui o mesmo como *Pré-Condição* :

1. Executar a API de *Criação de usuário*
2. Executar a API de *Realizar Login*
3. Realizar a atualização do token gerado na própria Variável (global ou ambiente)  via ou Script ṕara funcionamento geral das requisições que necessitam do mesmo


### ATIVIDADES

Estruturação/escrita de pelo ao menos 3 casos de teste contemplando cenários: positivos (fluxo básico e alternativos) e
cenários negativos (fluxos de exceção):

**LISTA DE CENÁRIOS DE TESTES QUE ESTÃO NO DOCUMENTO CB_FLUXO_GERAL_TESTES_APIs_USUÁRIO_LOGIN_PROD_CARRINHO**
**Ao abrir esse documento pelo GIT e para visualizar por inteiro, no final da página deve-se clicar em 'More pages'**

**CB -Cobertura de testes da API de Usuário:**

1. Positivo (201): *Criar usuário*
2. Negativo (400) : * Cadastro de usuário com e-mail existente*

**CB- Cobertura de testes da API de Login**

1. Positivo (200): *Realizar Login com credenciais válidas*
2. Negativo (401) : * Realizar Login com senha incorreta*
   
**CB - Cobertura de testes da API de Produtos:**

1. Negativo (201) : *Tentar cadastrar produto sem token*
2. Positivo (201) : *Cadastro de produto com sucesso*
3. Fluxo Alternativo(400): *Cadastrar produto com nome já existente*

**CB -Cobertura de testes da API de Carrinho:**

1. Positivo (201) : *Criar um carrinho contendo produtos válidos*
2. Negativo (400 ) : *Adicionar quantidade de produto acima do estoque disponível*
3. Negativo (400) :Tentar cadastrar mais de um carrinho para um único  usuário*
4. Fluxo Alternativo (200) : Cancelar compra devolvendo produtos ao estoque 
   

🚀 🤝  😄 **Muito agradecida por Lê até aqui**



