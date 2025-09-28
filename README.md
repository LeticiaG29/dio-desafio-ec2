# Desafio DIO - Gerenciamento de Instâncias EC2 na AWS

## 📌 Descrição
Este repositório faz parte do desafio proposto pela **DIO (Digital Innovation One)**, com o objetivo de consolidar conhecimentos sobre **gerenciamento de instâncias EC2 na AWS**.  
Aqui estão documentados os passos realizados, anotações e insights adquiridos durante a prática.

---

## 🎯 Objetivos de Aprendizagem
- Aplicar os conceitos aprendidos em um ambiente prático;
- Documentar processos técnicos de forma clara e organizada;
- Utilizar o GitHub como ferramenta de compartilhamento de documentação técnica.

---

## 🚀 Passo a Passo Realizado

1. **Criação da Instância EC2**
   - Sistema operacional escolhido: **Amazon Linux 2**
   - Tipo de instância: **t2.micro (Free Tier)**
   - Configurações adicionais: armazenamento padrão de 8GB e criação de um par de chaves para acesso SSH.

2. **Configuração do Grupo de Segurança**
   - Porta **22 (SSH)** liberada apenas para meu IP;
   - Porta **80 (HTTP)** liberada para acesso via navegador;
   - Sem outras regras adicionais.

3. **Acesso à Instância**
   - Método de acesso: **Terminal via SSH**
   - Comando utilizado:  
     ```bash
     ssh -i "minha-chave.pem" ec2-user@SEU_IP_PUBLICO
     ```

4. **Testes Realizados**
   - Atualização dos pacotes:  
     ```bash
     sudo yum update -y
     ```
   - Instalação do Apache:  
     ```bash
     sudo yum install -y httpd
     sudo systemctl start httpd
     sudo systemctl enable httpd
     ```
   - Teste no navegador acessando `http://SEU_IP_PUBLICO`, exibindo a página padrão do Apache.

---

## 📷 Evidências (prints de tela)
- Instância criada no **console da AWS**  
- Conexão bem-sucedida via **SSH**  
- Página padrão do **Apache** acessada pelo navegador  

*(Se quiser, pode criar uma pasta `/images` no repositório e salvar os prints.)*

---

## 💡 Insights e Aprendizados
- Aprendi a criar e configurar uma instância EC2 do zero;  
- Entendi a importância de configurar corretamente o grupo de segurança para liberar portas;  
- Descobri que ao **parar a instância**, o **IP público muda**, o que pode impactar no acesso;  
- A prática reforçou o cuidado com permissões e chaves privadas para garantir segurança.

---

## 📚 Referências
- [Documentação oficial da AWS EC2](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/concepts.html)  
- Materiais da **DIO** sobre AWS e EC2  

---

## ✅ Conclusão
Esse desafio foi essencial para reforçar a prática em **EC2 na AWS**, entendendo desde a criação e configuração de instâncias até a conexão e uso em ambiente real.
