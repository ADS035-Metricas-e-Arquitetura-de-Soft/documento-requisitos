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
- [ ] RF 1
- [ ] RF 2
- [ ] RF 3
- [ ] RF 4
- [ ] RF 5

### Requisitos Não-Funcionais
- [ ] RNF 1
- [ ] RNF 2
- [ ] RNF 3
- [ ] RNF 4
- [ ] RNF 5

### Regras de Negócio
- [ ] RGN 1
- [ ] RGN 2
- [ ] RGN 3
- [ ] RGN 4
- [ ] RGN 5

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

#### RC 1. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 7, 8, 9, 10, 11, 12, 13, 14]

Pré-condições: Descrição da pré-condição. [cite: 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18]

Pós-condições: Descrição da pós-condição. [cite: 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18]

Pri M B A

#### RF 2. Recuperar Senha

* O sistema deve permitir que o usuário solicite a recuperação de senha.
* O sistema deve solicitar um identificador do usuário (ex: e-mail, nome de usuário).
* O sistema deve enviar um link ou código de recuperação para o identificador fornecido.
* O sistema deve permitir que o usuário defina uma nova senha após a verificação do link/código.

#### RC 4. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 10, 11, 12, 13, 14]

Pré-condições: Descrição da pré-condição. [cite: 10, 11, 12, 13, 14, 15, 16, 17, 18]

Pós-condições: Descrição da pós-condição. [cite: 10, 11, 12, 13, 14, 15, 16, 17, 18]

Pri M B A

#### RF 3. Bloquear Conta

* O sistema deve bloquear a conta do usuário após um número configurável de tentativas de login inválidas.
* O sistema deve informar ao usuário que a conta foi bloqueada e o tempo para desbloqueio ou o procedimento para desbloqueá-la.

RC 10. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 14, 15, 16, 17, 18]

Pré-condições: Descrição da pré-condição. [cite: 15, 16, 17, 18]

Pós-condições: Descrição da pós-condição. [cite: 15, 16, 17, 18]

Pri M B A

#### RF 4. Logout

* O sistema deve permitir que o usuário faça logout da sua sessão.
* O sistema deve invalidar a sessão do usuário após o logout.

RC 11. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 18]

Pré-condições: Descrição da pré-condição. [cite: 18]

Pós-condições: Descrição da pós-condição. [cite: 18]

Pri M B A

Requisitos Não Funcionais

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

• Descrição do requisito funcional.
[cite: 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51] Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional.

• Descrição do requisito funcional.
[cite: 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51] Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional.

RC 1. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 39, 40, 41, 42, 43]

Pri M B A

#### RGN 2. Título da Regra de Negócio - Teste

• Descrição do requisito funcional.
[cite: 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51] Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional.

• Descrição do requisito funcional.
[cite: 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51] Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional.

RC 4. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 43, 44, 45, 46, 47]

Pri M B A

#### RGN 3. Título da Regra de Negócio - Revisão

• Descrição do requisito funcional.
[cite: 44, 45, 46, 47, 48, 49, 50, 51] Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional.

• Descrição do requisito funcional.
[cite: 44, 45, 46, 47, 48, 49, 50, 51] Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional.

RC 10. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 47, 48, 49, 50, 51]

Pri A M B

#### RGN 4. Título da Regra de Negócio - Concluído

• Descrição do requisito funcional.
[cite: 48, 49, 50, 51] Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional.

• Descrição do requisito funcional.
[cite: 48, 49, 50, 51] Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional. Descrição do requisito funcional.

RC 11. Título do Requisito Complementar (Opcional): Descrição do requisito complementar. [cite: 51]
