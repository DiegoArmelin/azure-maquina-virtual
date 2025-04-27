
# Resumo sobre Criação e Configuração de Máquina Virtual no Microsoft Azure

## ☁️ O que é o Azure
O **Microsoft Azure** é a plataforma de computação em nuvem da Microsoft que oferece uma ampla variedade de serviços, como máquinas virtuais, bancos de dados, redes e armazenamento.  
Ela permite criar, gerenciar e implantar aplicativos em uma rede global de datacenters.  
Utilizar o Azure para criar máquinas virtuais facilita o acesso a infraestrutura escalável, segura e sob demanda, ideal para testes, desenvolvimento e produção.

---

## 🛠️ Passo a Passo para Criar uma Máquina Virtual

1. **Acessar o portal Azure**
   - Ir até [portal.azure.com](https://portal.azure.com/).
   - Fazer login com sua conta Microsoft.

2. **Criar um novo recurso -> Máquina Virtual**
   - No painel lateral, clicar em **Criar um recurso**.
   - Selecionar **Máquina Virtual** no catálogo.

3. **Escolher o sistema operacional**
   - Escolher a imagem do sistema operacional desejado (exemplo: **Windows Server 2022**, **Ubuntu 20.04 LTS**).

4. **Definir o tamanho (SKU) da VM**
   - Escolher o tamanho (quantidade de vCPUs, RAM e armazenamento) conforme a necessidade.
   - Exemplo de SKUs: `B1s` (baixo custo), `D2s_v3` (desempenho padrão).

5. **Configurar o método de autenticação**
   - Definir o usuário administrador.
   - Escolher entre:
     - Senha
     - Chave pública SSH (recomendado para Linux)

6. **Ajustar as configurações de rede**
   - Associar a VM a uma Rede Virtual (VNet).
   - Criar ou configurar um **Network Security Group (NSG)** para controlar o tráfego de entrada/saída.
   - Definir se a VM terá um IP público.

7. **Revisar e criar a VM**
   - Revisar todas as configurações.
   - Corrigir eventuais alertas ou erros destacados.
   - Clicar em **Criar** e aguardar a implantação.

---

## 💡 Dicas Importantes

- **Utilizar tags**: Adicione tags aos seus recursos (ex: `ambiente=teste`, `projeto=azure-lab`) para facilitar a organização e o controle de custos.
- **Configurar backups automáticos**: Para garantir que seus dados estejam protegidos contra falhas.
- **Manter o sistema operacional atualizado**: Ative as atualizações automáticas para proteger a VM contra vulnerabilidades.

---

## ⚠️ Erros Comuns e Como Resolver

- **Problemas de conexão**
  - Verifique se as regras de NSG permitem o tráfego da porta necessária (exemplo: RDP porta 3389 para Windows, SSH porta 22 para Linux).
  - Confirme se a máquina possui um IP público.

- **Custo elevado**
  - Escolha SKUs menores para ambientes de testes e desenvolvimento.
  - Desligue as máquinas que não estão em uso para evitar cobranças desnecessárias.

---

> Este documento faz parte do projeto de documentação de criação e configuração de VMs na plataforma Microsoft Azure.
