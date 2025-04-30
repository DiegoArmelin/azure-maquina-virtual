Documentação: Configuração de Instância de Banco de Dados no Microsoft Azure
Objetivo
Este documento tem como objetivo detalhar o processo de criação e configuração de uma instância de banco de dados na plataforma Microsoft Azure. Ele foi elaborado como material de apoio para estudos e futuras implementações.

Pré-requisitos
    • Conta ativa no Microsoft Azure.
    • Cartão de crédito válido (necessário para validar a conta, mesmo em planos gratuitos).
    • Navegador web atualizado.

Etapas da Configuração
1. Acessar o Portal do Azure
    1. Acesse: https://portal.azure.com
    2. Faça login com sua conta Microsoft.
2. Criar um Grupo de Recursos
    1. No menu lateral, clique em "Grupos de recursos".
    2. Clique em "+ Criar".
    3. Preencha:
        ◦ Assinatura: Selecione sua assinatura.
        ◦ Grupo de recursos: Nome identificador (ex: meu-grupo-banco).
        ◦ Região: Escolha a região mais próxima de você ou de seus usuários.
    4. Clique em "Revisar + Criar" e depois em "Criar".
3. Criar a Instância do Banco de Dados
    1. No menu lateral, clique em "Criar um recurso".
    2. Selecione "Banco de Dados" > "Banco de Dados SQL".
    3. Preencha os campos:
        ◦ Assinatura e Grupo de Recursos: selecione os criados anteriormente.
        ◦ Nome do banco de dados: ex: meuBancoEstudo.
        ◦ Servidor: clique em "Criar novo".
            ▪ Nome do servidor (único globalmente).
            ▪ Login e senha do administrador.
            ▪ Região.
    4. Escolha o plano de desempenho (pode começar com o plano gratuito ou básico).
    5. Clique em "Próximo: Configurações adicionais":
        ◦ Pode optar por usar um banco de dados vazio ou restaurar de backup/exemplo.
    6. Clique em "Revisar + Criar" e depois em "Criar".
4. Configurar o Firewall do Servidor
    1. Após a criação, vá até o recurso do servidor SQL.
    2. Clique em "Configurações de firewall e redes virtuais".
    3. Adicione o IP atual para permitir conexões:
        ◦ Clique em "+ Adicionar ao IP do cliente".
        ◦ Salve as alterações.
5. Conectar-se ao Banco de Dados
Você pode usar ferramentas como:
    • Azure Data Studio
    • SQL Server Management Studio (SSMS)
    • Visual Studio Code (com extensão SQL)
Dados de conexão:
    • Servidor: nomedoservidor.database.windows.net
    • Banco de dados: meuBancoEstudo
    • Usuário: fornecido na criação
    • Senha: fornecida na criação
6. Testar a Conexão
    1. Abra a ferramenta escolhida.
    2. Insira os dados de conexão.
    3. Teste com um comando SQL simples, como:
SELECT GETDATE();

Considerações Finais
    • Lembre-se de sempre revisar as configurações de segurança (firewall, autenticação, criptografia).
    • É possível escalar a instância conforme as necessidades do projeto.
    • Os custos variam de acordo com o plano e o uso — monitore pelo portal do Azure.

Referências
    • Documentação oficial do Azure SQL
    • Preços do Azure SQL Database

Autor: [Diego Armelin Silva] Data: [30/04/25]
