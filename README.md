# TRABALHO DE ARQUITETURA DE SOFTWARE

## Projeto 1 - Levantamento de Requisitos / 2025

### Componente Curricular: Arquitetura de Software
### Professor: Alessandro Borges de Morais
### Turma: 2CB | Aulas: Terça e Sexta

### Curso: ADS Integrantes:
- [@Sérgio Silva](https://github.com/sergiobslva-iesb)
- [@Sarah Evelyn](https://github.com/SarahDevIesb)
- [@Rhuan Justino](https://github.com/RhuanJSouza)

## Artefatos
### Requisitos Funcionais
- [x] RF 1
- [x] RF 2
- [x] RF 3
- [x] RF 4
- [x] RF 5

### Requisitos Não-Funcionais
- [x] RNF 1
- [x] RNF 2
- [x] RNF 3
- [x] RNF 4
- [x] RNF 5

### Regras de Negócio
- [x] RGN 1
- [x] RGN 2
- [x] RGN 3
- [x] RGN 4
- [x] RGN 5

## Gestão de Barbearias V1
[Repositório do Projeto de Dispositivos Móveis](https://github.com/ADS023-Programacao-Dispositivos-Moveis/projeto-pdm-01/)

## O que é o Projeto
A proposta deste projeto é criar um app que seja caapaz de auxiliar os barbeiros com as suas atividades mais comuns do dia-a-dia.. Dando a eles a possibilidade de verificar ganhos mensais, agendamentos de clientes, gestão de planos mensais e pagamento tudo via APP.

## Requisitos do Sistema

### Requisitos Funcionais

#### RF 1.  Autenticar Usuário

* O sistema deve permitir que um usuário existente faça login fornecendo suas credenciais (usuário e senha).
* O sistema deve verificar as credenciais fornecidas com as armazenadas no banco de dados.
* O sistema deve conceder acesso ao usuário se as credenciais forem válidas.
* O sistema deve exibir uma mensagem de erro se as credenciais forem inválidas.

#### RC 1. O sistema deve oferecer a opção de "lembrar-me" para manter o usuário logado por um período estendido.

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O usuário deve ter uma conta registrada no sistema.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema deve estabelecer uma sessão para o usuário autenticado.


#### RF 2. Recuperar Senha

* O sistema deve permitir que o usuário solicite a recuperação de senha.
* O sistema deve solicitar um identificador do usuário (ex: e-mail, nome de usuário).
* O sistema deve enviar um link ou código de recuperação para o identificador fornecido.
* O sistema deve permitir que o usuário defina uma nova senha após a verificação do link/código.

#### RC 4. O sistema deve implementar medidas de segurança para prevenir o uso indevido da funcionalidade de recuperação de senha (e.g., limitação de tentativas). 

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O usuário deve ter uma conta registrada no sistema com um e-mail válido associado.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema deve permitir que o usuário defina uma nova senha.


#### RF 3. Bloquear Conta

* O sistema deve bloquear a conta do usuário após um número configurável de tentativas de login inválidas.
* O sistema deve informar ao usuário que a conta foi bloqueada e o tempo para desbloqueio ou o procedimento para desbloqueá-la.

#### RC 10. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 14, 15, 16, 17, 18]

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O sistema deve definir um período de tempo para o bloqueio da conta (e.g., 5 minutos, 1 hora). 
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O usuário deve ter inserido credenciais incorretas um número específico de vezes.


#### RF 4. Logout

* O sistema deve permitir que o usuário faça logout da sua sessão.
* O sistema deve invalidar a sessão do usuário após o logout.

#### RC 11. O sistema deve definir um período de tempo para o bloqueio da conta (e.g., 5 minutos, 1 hora). 

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O usuário deve ter inserido credenciais incorretas um número específico de vezes.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema deve impedir o acesso à conta até que o bloqueio seja removido.


#### RF 5. Exibir Mensagens de Erro

* O sistema deve exibir mensagens de erro claras e informativas para falhas de login (e.g., credenciais inválidas, conta bloqueada). 

#### RC 12. As mensagens de erro devem ser localizadas para diferentes idiomas.

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O usuário deve ter inserido credenciais inválidas.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema deve permanecer na tela de login, aguardando novas tentativas ou ações do usuário.

### Requisitos Não Funcionais

#### RNF 1. Segurança

* As senhas devem ser armazenadas de forma segura (ex: criptografadas com bcrypt).
* A comunicação entre o cliente e o servidor deve ser criptografada (HTTPS).
* O sistema deve prevenir ataques de força bruta (ex: limitação de taxa de tentativas de login).
* O sistema deve gerar logs de auditoria de tentativas de login (sucesso e falha).

#### RC 1. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 22, 23, 24, 25, 26]

Pri M B A

#### RNF 2. Desempenho

* O tempo de resposta para o login deve ser inferior a 2 segundos.
* O sistema deve suportar um número máximo de logins simultâneos (definir um número).

#### RC 4. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 26, 27, 28, 29, 30]

Pri M A B

#### RNF 3. Usabilidade

* A interface de login deve ser intuitiva e fácil de usar.
* As mensagens de erro devem ser claras e informativas.
* O sistema deve fornecer feedback visual ao usuário durante o processo de login.

RC 10. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 30, 31, 32, 33, 34]

Pri M B A

#### RNF 4. Manutenibilidade

* O código do módulo de login deve ser modular e fácil de manter.
* As configurações de segurança (ex: número de tentativas de login) devem ser facilmente configuráveis.

RC 11. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 34, 35, 36, 37, 38, 39, 40, 41, 42, 43]

Pri M B A

Regras de Negócio

#### RGN 1. Formato das Credenciais

* O nome de usuário deve ter no mínimo X caracteres e no máximo Y caracteres.
* A senha deve ter no mínimo A caracteres, conter pelo menos um caractere maiúsculo, um caractere minúsculo, um número e um caractere especial.

#### RC 1. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 39, 40, 41, 42, 43]

Pri M B A

#### RGN 2. Validação de E-mail

* O e-mail fornecido para recuperação de senha deve ser um e-mail válido.

RC 4. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 43, 44, 45, 46, 47]

Pri M B A

#### RGN 3. Tempo de Bloqueio

* A conta do usuário deve ser bloqueada por N minutos após M tentativas de login inválidas.

RC 10. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 47, 48, 49, 50, 51]

Pri A M B

#### RGN 4. Expiração da Senha

* A senha do usuário deve expirar a cada D dias, forçando a troca.

RC 11. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 51]
