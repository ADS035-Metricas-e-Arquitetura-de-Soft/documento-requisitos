# TRABALHO DE ARQUITETURA DE SOFTWARE

## Projeto 1 - Levantamento de Requisitos / 2025

### Componente Curricular: Arquitetura de Software
### Professor: Alessandro Borges de Morais
### Turma: 2CB | Aulas: Terça e Sexta

### Curso: ADS Integrantes:
- [@Sérgio Silva](https://github.com/sergiobslva-iesb)
- [@Sarah Evelyn](https://github.com/SarahDevIesb)
- [@Rhuan Justino](https://github.com/RhuanJSouza)

## Gestão de Barbearias V1
[Escopo Completo - Repositório do Projeto de Dispositivos Móveis](https://github.com/ADS023-Programacao-Dispositivos-Moveis/projeto-pdm-01/)

## O que é o Projeto
A proposta deste projeto é criar um app que seja caapaz de auxiliar os barbeiros com as suas atividades mais comuns do dia-a-dia.. Dando a eles a possibilidade de verificar ganhos mensais, agendamentos de clientes, gestão de planos mensais e pagamento tudo via APP.

## Requisitos do Sistema

### Caso de Uso
![Diagrama de Caso de Uso de Login V1](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documento-requisitos/blob/main/caso-de-uso-login-v1.svg)

### Script de Caso de Uso [PlantUML](https://www.plantuml.com/plantuml/uml/SyfFKj2rKt3CoKnELR1Io4ZDoSa70000)
    @startuml
    left to right direction
    actor "Usuário" as User
    
    rectangle "Sistema de Login" {
      usecase "Autenticar Usuário" as Authenticate
      usecase "Recuperar Senha" as RecoverPassword
      usecase "Bloquear Conta" as BlockAccount
      usecase "Logout" as Logout
      usecase "Exibir Mensagens de Erro" as DisplayError
    }
    
    User -- Authenticate
    User -- RecoverPassword
    User -- Logout
    
    Authenticate --|> DisplayError : <<include>>
    RecoverPassword --|> DisplayError : <<include>>
    
    Authenticate ..> BlockAccount : <<extend>>
    
    @enduml

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

#### RC 1. O sistema deve realizar auditoria das tentativas de login, registrando informações como data, hora, nome de usuário e resultado da tentativa. 


#### RNF 2. Desempenho

* O tempo de resposta para o login deve ser inferior a 2 segundos.
* O sistema deve suportar um número máximo de logins simultâneos (definir um número).

#### RC 4. O sistema deve utilizar mecanismos de cache para otimizar o processo de autenticação. 


#### RNF 3. Usabilidade

* A interface de login deve ser intuitiva e fácil de usar.
* As mensagens de erro devem ser claras e informativas.
* O sistema deve fornecer feedback visual ao usuário durante o processo de login.

#### RC 10. A interface de login deve ser acessível a usuários com deficiência visual (e.g., suporte a leitores de tela). 


#### RNF 4. Manutenibilidade

* O código do módulo de login deve ser modular e fácil de manter.
* As configurações de segurança (ex: número de tentativas de login) devem ser facilmente configuráveis.

RC 11. O sistema deve implementar mecanismos de redundância e failover para garantir a alta disponibilidade. 

### Regras de Negócio

#### RGN 1. Formato das Credenciais

* O nome de usuário deve ter no mínimo X caracteres e no máximo Y caracteres.
* A senha deve ter no mínimo A caracteres, conter pelo menos um caractere maiúsculo, um caractere minúsculo, um número e um caractere especial.

#### RC 1. As configurações do sistema de login (e.g., número de tentativas de login, tempo de bloqueio) devem ser facilmente alteráveis.


#### RGN 2. Validação de E-mail

* O e-mail fornecido para recuperação de senha deve ser um e-mail válido.

#### RC 4. O sistema deve verificar a força da senha durante o cadastro e fornecer feedback ao usuário.  


#### RGN 3. Tempo de Bloqueio

* A conta do usuário deve ser bloqueada por N minutos após M tentativas de login inválidas.

#### RC 10. O sistema deve permitir que o usuário escolha o método de MFA preferido.


#### RGN 4. Expiração da Senha

* A senha do usuário deve expirar a cada D dias, forçando a troca.

#### RC 11. O sistema deve definir um processo para reativar contas inativas. 

---

## Artefatos Elaborados e Entregues
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

## Legenda
* RF - `Requisito Funcional`
* RNF - `Requisito Não Funcional`
* RGN - `Regra de Negócio`
* RC - `Requisito Complementar`
