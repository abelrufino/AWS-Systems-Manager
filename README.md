# AWS-Systems-Manager
Usar o AWS Systems Manager

<img width="128" height="128" alt="aws" src="https://github.com/user-attachments/assets/93da4daf-5642-4bac-8b1c-6c9707016fee" />

Este laboratório **Criar uma VPC (Virtual Private Cloud) através do Console da AWS (Amazon Web Services).**.

---

## 🚀 Você poderá usar o Systems Manager para fazer o seguinte: 🚀

- Verificar configurações e permissões.
- Verificar configurações e permissões.
- Atualizar as configurações da aplicação.
- Acessar a linha de comando em uma instância.

---

##  Etapa 1: Gerar listas de inventário para instâncias gerenciadas

1. No Console de Gerenciamento da AWS, na caixa  de pesquisa, insira Systems Manager e selecione Enter. Essa opção levará você à página do console do Systems Manager.
2. No painel de navegação à esquerda, em Gerenciamento de nós, selecione Fleet Manager.
3. No menu Gerenciamento de contas e selecione Configurar inventário.

4. Para criar uma associação que coletará informações sobre software e configurações para a instância gerenciada, selecione as seguintes opções:
Na seção Fornecer detalhes do inventário, em Nome, insira Inventory-Association.
Na seção Destinos, selecione as seguintes opções:
Em Especificar destinos por, selecione Selecionar instâncias manualmente.
Selecione a linha de Instância gerenciada.
Deixe as outras opções com as configurações padrão.

5. Selecione Configurar inventário.
6. Selecione o link ID do nó, que direciona você para a Visão geral do nó.
7. Selecione a guia Inventário.

---

##  Etapa 2: Instalar uma aplicação personalizada usando a opção Executar comando

<img width="2391" height="1309" alt="InstallApplication" src="https://github.com/user-attachments/assets/77388b51-3934-4d4f-b2eb-aa4312cd342d" />
No diagrama anterior, o Systems Manager instala uma aplicação em uma instância do EC2 em uma nuvem privada virtual (VPC). Ele é instalado usando a opção Executar comando. A opção Executar comando executará o "script install" e o seguinte: servidor web Apache, PHP, SDK da AWS e o aplicativo web. Depois de tudo instalado, ele também inicia o servidor web.

1. No canto superior esquerdo, expanda o ícone de menu. Em Gerenciamento de nós, selecione Executar comando.
2. Selecione [Executar comando].
3. Em seguida clicar em Adicionar nova sub-rede
4. Em Sub-rede 1 de 1, digite o nome da sub-rede: Public Subnet 1
5. Em Zona de disponibilidade selecionar Oeste dos EUA (Oregon) / us-west-2-a
6. Em CIDR IPv4 digitar o endereçamento IP conforme o diagrama: 10.0.0.0/24
7. Em seguida clicar em Adicionar nova sub-rede
8. Em Sub-rede 2 de 2, digite o nome da sub-rede: Public Subnet 2
9. Em Zona de disponibilidade selecionar Oeste dos EUA (Oregon) / us-west-2-b
10. Em CIDR IPv4 digitar o endereçamento IP conforme o diagrama: 10.0.2.0/24
11. Em seguida clicar em Adicionar nova sub-rede
12. Em Sub-rede 3 de 3, digite o nome da sub-rede: Private Subnet 1
13. Em Zona de disponibilidade selecionar Oeste dos EUA (Oregon) / us-west-2-a
14. Em CIDR IPv4 digitar o endereçamento IP conforme o diagrama: 10.0.1.0/24
15. Em seguida clicar em Adicionar nova sub-rede
16. Em Sub-rede 4 de 4, digite o nome da sub-rede: Private Subnet 2
17. Em Zona de disponibilidade selecionar Oeste dos EUA (Oregon) / us-west-2-b
18. Em CIDR IPv4 digitar o endereçamento IP conforme o diagrama: 10.0.3.0/24
19. Em seguida clicar em Criar sub-rede
20. Pronto, as sub-redes foram criadas e configuradas
---
