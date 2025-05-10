# App Send Mail
Este é um projeto simples de envio de e-mails utilizando PHP e a biblioteca PHPMailer. O objetivo do projeto é demonstrar como configurar e enviar e-mails através de um formulário web. Este site foi desenvolvido com base no curso da UDEMY ministrado por Jorge Sant Ana e Jamilton Damasceno.

## Funcionalidades
Envio de e-mails utilizando o protocolo SMTP.
Validação de dados do formulário antes do envio.
Exibição de mensagens de sucesso ou erro após o envio do e-mail.
Interface simples e responsiva utilizando Bootstrap 4.

---

## Como Funciona

1. **Formulário de Envio**:
   - O usuário preenche o formulário com o e-mail do destinatário, assunto e mensagem.
   - Os dados são enviados para o arquivo `processa_envio.php` via método `POST`.

2. **Validação dos Dados**:
   - O script valida se todos os campos obrigatórios foram preenchidos.
   - Caso algum campo esteja vazio, o usuário é redirecionado de volta para a página inicial.

3. **Envio do E-mail**:
   - O script utiliza a biblioteca **PHPMailer** para enviar o e-mail através do servidor SMTP do Gmail.
   - As credenciais do servidor SMTP (e-mail e senha) devem ser configuradas no código.

4. **Exibição de Mensagens**:
   - Após o envio, o usuário é informado se o e-mail foi enviado com sucesso ou se ocorreu algum erro.

---

## Configuração

### Requisitos

- **PHP** (versão 7.0 ou superior).
- Servidor local como **XAMPP** ou **WAMP**.
- Biblioteca **PHPMailer** (já incluída no projeto).

### Configuração do Servidor SMTP

1. Substitua as credenciais fictícias no arquivo `processa_envio.php` pelas suas credenciais reais:
   ```php
   $mail->Username = 'seu_email@exemplo.com'; // Substitua pelo seu e-mail
   $mail->Password = 'sua_senha_de_aplicativo'; // Substitua pela senha de aplicativo

2. Certifique-se de que a conta do Gmail utilizada:

Possui uma senha de aplicativo configurada.
Está habilitada para envio de e-mails via SMTP.
3. Configure o remetente no método setFrom:
