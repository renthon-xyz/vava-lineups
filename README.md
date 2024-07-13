
![1473](https://github.com/user-attachments/assets/67ebb1b5-c35d-4fa8-b639-d4bd7b7c1e1a)

# VavaLineups
![PHP Badge](https://img.shields.io/badge/PHP-6c69f5?style=for-the-badge&logo=PHP&logoColor=white) ![MySQL Badge](https://img.shields.io/badge/MySQL-507ca4?style=for-the-badge&logo=MySQL&logoColor=white) ![CSS Badge](https://img.shields.io/badge/Css-0095ff?style=for-the-badge&logo=CSS3&logoColor=white) ![JS Badge](https://img.shields.io/badge/Javascript-fff200?style=for-the-badge&logo=Javascript&logoColor=black) ![JQuery Badge](https://img.shields.io/badge/JQuery-1f48b8?style=for-the-badge&logo=JQuery&logoColor=black) ![HTML Badge](https://img.shields.io/badge/HTML-ff6600?style=for-the-badge&logo=HTML5&logoColor=black)

O projeto [VavaLineups](https://heitordutra.infinityfreeapp.com/vavalineups/) é uma plataforma de serviço que permite ao usuário ver jogadas para se fazer com a personagem "Viper" do jogo "Valorant". Também dá a opção do usuário comprar o passe VIP da plataforma, integrando assim com a API do Mercado Pago, e com a do Stripe. Neste projeto implementei funções novas como: ReCaptcha e criptografia OpenSSL e Base_64.

###### Esse projeto foi feito numa época em que eu ainda não havia entrado na faculdade para aprender sobre: Design Patterns, SOLID, Gof, GRASP, CRUD, Estrutura de Dados, ou Modelagem de Banco de Dados, entre outros. Então foi feito meio que de qualquer jeito essa parte da Estruturação, e o que eu estava mais focando era em fazer códigos funcionarem, já que era um dos meus primeiros projetos.

## Índice 

* [Título e Descrição](#pesquisa-fipe)
* [Índice](#índice)
* [Funcionalidades do Projeto](#-funcionalidades-do-projeto)
* [Tecnologias Utilizadas](#%EF%B8%8F-técnicas-e-tecnologias-utilizadas)
* [Acesso ao Projeto](#-acesso-ao-projeto)
* [Abrir e Rodar o Projeto](#%EF%B8%8F-abrir-e-rodar-o-projeto)
* [Detalhamento do Código](#-detalhamento-do-código)

## 🔨 Funcionalidades do projeto

O VavaLineups oferece as seguintes funcionalidades:

- Cadastro e login da uma conta VIP.
- Confirmação via email do pagamento.
- Suporte a pagamentos via PIX ou Cartão de Crédito.
- Upload de sua própria imagem para perfil ou escolher uma das 5 padrões.
- Seleção prévia do mapa desejado pelo usuário, para então ver as jogadas.

## ✔️ Técnicas e tecnologias utilizadas

- `PHP`: Linguagem principal utilizada no desenvolvimento do projeto.
- `CSS`: Estilização das interfaces e responsividade para diferentes dispositivos.
- `JS & JQuery`: Utilizado para fazer a comunicação com o backend.
- `HTML`: Linguagem de marcação para estruturação das páginas.

## 📁 Acesso ao projeto

Você pode ver o projeto funcionando [aqui](https://heitordutra.infinityfreeapp.com/vavalineups/).

## 🛠️ Abrir e rodar o projeto

Para abrir e rodar o projeto, siga os seguintes passos:

1. Baixe o xampp e clone o repositório na pasta `htdocs`.

2. Crie um banco de dados no `localhost/phpmyadmin` e altere os valores do arquivo `lib/db.class.php` para os respectivos do seu BD.

3. Acesse `http://localhost/`.

### Detalhamento do código:

O código PHP fornecido implementa um programa para exibir ao usuário uma plataforma de consultas a lineups de um jogo eletrônico, e que ele pode pagar pela versão VIP de tal serviço.

#### 404, *.html
Arquivos que servindo de interfaces, funcionam como as páginas acessadas pelo usuário para interagir com a aplicação. Servindo ou para exibir opções para o jogador, ou para já mostrar as jogadas possíveis com vídeos indexados de outro servidor. Na página também é incluido a paginação com uma barra lateral ou o Footer.

#### alter, *.js
Arquivos que contém scripts e funções para funcionamento do site, e comunicação do front-end com back-end, tanto como animações para que a utilização do usuário seja mais coerente.

#### api/recaptcha.js
Arquivo encarregado de verificar o valor do Recaptcha para Login ou Logon, e que se estiver liberado, faz a requisição para o Back-end, passando os dados do usuário.

#### api/*.php
Arquivos que contém scripts e funções para funcionamento da lógica de negócio, fazer verificações e validações nos dados inseridos do usuário, enviar emails, inserem e removem dados no Banco de Dados, etc.
mp-ongoing, st-cancel, st-success: verificam status do pagamento do usuário com requisições para as APIs dos respectivos sistemas de pagamentos: Mercado Pago e Stripe; e se o pagamento estiver confirmado, ativam a conta no DB.

###### Esse projeto foi feito numa época em que eu ainda não havia entrado na faculdade para aprender sobre: Design Patterns, SOLID, Gof, GRASP, CRUD, Estrutura de Dados, ou Modelagem de Banco de Dados, entre outros. Então foi feito meio que de qualquer jeito essa parte da Estruturação, e o que eu estava mais focando era em fazer códigos funcionarem, já que era um dos meus primeiros projetos.

#### stripe/stripe.php
Responsável pela geração do link de pagamento, caso a escolha do usuário seja cartão de crédito, fazendo uma requisição para a API, e setando os valores corretos necessários.
O resto dos arquivos deste diretório da pasta são dependências da ferramenta gerenciadas pelo Composer, requisitada pelo próprio sistema de pagamento.

#### mercado-pago/index.php
Responsável pela geração do pix para o usuário, fazendo uma requisição para a API, e setando os valores corretos necessários, como: preço, descrição, email do comprador, etc. Também envia para o email do usuário o código QR CODE do pix, e o link para ativação da conta após o pagamento.
O resto dos arquivos deste diretório da pasta são dependências da ferramenta gerenciadas pelo Composer, requisitada pelo próprio sistema de pagamento.


### Exemplo de Uso
Ao executar o programa, o usuário pode escolher entre um dos mapas exibidos e clicar em "Escolher" para ir direto aos Lineups. Se quiser também pode criar uma conta indo na página "Vip" e escolhendo uma forma de pagamento, e concluindo a autenticação de sua conta.


https://github.com/user-attachments/assets/0fc8a297-0f7a-4e97-9bc2-41faa9df3770


---

Este é o README atualizado para o projeto VavaLineups. Ele fornece uma visão geral do projeto, suas funcionalidades, tecnologias utilizadas e como acessar e rodar o projeto. Para mais detalhes, você pode explorar os arquivos do código fonte mencionados.
