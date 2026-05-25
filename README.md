# ☁️ Desafio DIO: Gerenciamento de Instâncias EC2 na AWS

## 📌 Visão Geral
Este repositório contém a documentação e os insights práticos do desafio "Gerenciamento de Instâncias EC2 na AWS" da [DIO](https://www.dio.me/). O objetivo do projeto foi aplicar na prática os conceitos de provisionamento, configuração e acesso seguro a servidores virtuais na nuvem AWS.

## 🛠️ Tecnologias e Serviços Utilizados
* **Amazon EC2 (Elastic Compute Cloud):** Provisionamento da máquina virtual.
* **Amazon VPC:** Utilização da rede padrão e sub-redes públicas.
* **Security Groups:** Configuração de regras de firewall para controle de tráfego de entrada e saída.
* **Key Pairs:** Geração de chaves criptográficas para acesso seguro via SSH.
* **Git e GitHub:** Versionamento e documentação do projeto.

## 🚀 Passo a Passo da Implementação

1. **Acesso ao Console AWS:** Login na conta AWS e navegação até o serviço EC2.
2. **Criação do Par de Chaves:** Geração de um arquivo `.pem` para garantir a autenticação segura no servidor sem o uso de senhas.
3. **Lançamento da Instância:**
   * **AMI:** Amazon Linux 2 (Elegível para o Free Tier).
   * **Tipo de Instância:** `t2.micro`.
4. **Configuração de Rede e Segurança:**
   * Criação de um novo Security Group.
   * Liberação da porta **22 (SSH)** para permitir o acesso remoto pelo terminal.
   * Liberação da porta **80 (HTTP)** para permitir o tráfego web futuro.
5. **Conexão Remota:** Utilização do terminal (Linux/Mac) ou PuTTY/MobaXterm (Windows) para acessar a instância via SSH utilizando o IP Público e a chave `.pem`.

## 💡 Insights e Aprendizados
Durante a execução deste laboratório prático, reforcei os seguintes conceitos:
* **Segurança em primeiro lugar:** A importância de aplicar o princípio do menor privilégio nos Security Groups, evitando deixar a porta 22 aberta para o mundo (`0.0.0.0/0`) em ambientes de produção.
* **Gestão de Custos:** A necessidade de encerrar (terminate) as instâncias após o uso em laboratórios de estudo para evitar cobranças indesejadas no billing da AWS.
* **Acesso seguro:** Entendimento prático do funcionamento das chaves assimétricas para a conexão remota a servidores Linux.

---
*Desafio realizado como parte da jornada de aprendizado na plataforma DIO.*
