# Desafio DIO - Laboratório EC2 na AWS

## Sobre este desafio
Neste desafio da DIO, meu objetivo foi aprender a criar e gerenciar uma **instância EC2 na AWS**.  
Aqui estão documentados os passos que realizei e o que aprendi durante a prática.

---

## Objetivos
- Entender o processo de criação e configuração de uma instância EC2;  
- Testar acesso à instância via SSH;  
- Registrar aprendizados e experiências de forma organizada.  

---

## Passo a Passo

1. **Criação da Instância**
   - Escolhi o sistema operacional **Amazon Linux 2**;  
   - Tipo da instância: **t2.micro** (gratuita no Free Tier);  
   - Criei um par de chaves para poder acessar a instância via SSH;  
   - Mantive o armazenamento padrão de 8GB.  

2. **Configuração do Grupo de Segurança**
   - Liberada a porta **22 (SSH)** somente para o meu IP;  
   - Liberada a porta **80 (HTTP)** para poder acessar páginas pelo navegador.  

3. **Acesso à Instância**
   - Usei o terminal para me conectar via SSH;  
   - Comando utilizado:  
     ```bash
     ssh -i "minha-chave.pem" ec2-user@SEU_IP_PUBLICO
     ```  

4. **Testes Realizados**
   - Atualizei os pacotes da instância:  
     ```bash
     sudo yum update -y
     ```  
   - Instalei o servidor Apache e iniciei o serviço:  
     ```bash
     sudo yum install -y httpd
     sudo systemctl start httpd
     sudo systemctl enable httpd
     ```  
   - Acessei `http://SEU_IP_PUBLICO` no navegador e a página padrão do Apache carregou.

---

## Aprendizados
- Entendi como criar e configurar uma instância EC2 do zero;  
- Notei a importância de liberar as portas corretas no grupo de segurança;  
- Aprendi que ao parar a instância, o IP público muda;  
- Ganhei confiança em usar SSH e executar comandos básicos na instância.

---

## Referências
- [Documentação oficial AWS EC2](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/concepts.html)  
- Material da **DIO** sobre EC2 e AWS.
