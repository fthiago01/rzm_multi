# 🧭 **Zabbix Host Migrator** - Migração de Hosts para o Zabbix

O **Zabbix Host Migrator** é uma ferramenta desenvolvida para facilitar a migração de hosts para o Zabbix de forma simples e eficiente. Através de uma interface gráfica (GUI) com o Tkinter, o programa permite a criação automatizada de hosts diretamente do seu arquivo Excel. Ideal para profissionais de TI que precisam realizar grandes migrações de uma maneira ágil e sem erros manuais.

## 🚀 **Como Usar**

### Requisitos

- **Windows** ou **Linux**
- **Planilha Excel** contendo informações dos hosts a serem migrados para o Zabbix

### Passo a Passo

1. **Baixe o Arquivo Executável:**
   - Para Windows, baixe o arquivo `.exe` disponibilizado.
   - Para Linux, baixe o arquivo executável compatível com sua distribuição.

2. **Abra o Programa:**
   - Ao abrir o programa, você verá a interface gráfica do **Zabbix Host Migrator**.

3. **Configuração de Conexão:**
   - **URL da API do Zabbix**: Insira a URL da API do seu servidor Zabbix (por exemplo, `https://seu-zabbix.com/api_jsonrpc.php`).
   - **Usuário e Senha**: Insira as credenciais de acesso da sua conta Zabbix com permissões suficientes para criar hosts.

4. **Seleção de Planilha:**
   - Clique no botão **"📁 Selecionar Planilha"** para escolher um arquivo Excel (.xlsx) que contém a lista de hosts a serem migrados.
   - A planilha deve ter as seguintes colunas:
     - **name**: Nome do host
     - **ip_address**: Endereço IP ou DNS do host
     - **group_name**: Nome do grupo de hosts no Zabbix
     - **template_name**: Nome do template que será aplicado ao host
     - **snmp_community**: Comunidade SNMP do host

5. **Opções de SNMP e Status:**
   - **Versão SNMP**: Selecione a versão SNMP para os hosts (1, 2 ou 3).
   - **Status do Host**: Escolha se o host será **Ativo** ou **Inativo**.
   - **IP ou DNS**: Escolha se os hosts devem ser configurados com **IP** ou **DNS**.

6. **Iniciar Migração:**
   - Clique em **"▶️ Iniciar Migração"** para começar a criação dos hosts no Zabbix.
   - O programa fará a migração dos hosts um a um e exibirá o progresso no painel de logs.
   - Se um host já existir, o programa pulará automaticamente e informará no log.

7. **Resultados:**
   - Após a migração, a lista de hosts criados será exibida na interface, mostrando o nome do host e um símbolo de confirmação ✅.

8. **Logs:**
   - O painel de logs exibe detalhes sobre cada host criado e eventuais erros encontrados durante a migração.

### Exemplo de Entrada no Excel

| name             | ip_address     | group_name     | template_name     | snmp_community |
|------------------|----------------|----------------|-------------------|----------------|
| CLI-PI-TSA-SLINK| 192.168.1.100  | Servers        | Template OS Linux | public         |
| CLI-PI-DB-SERVER| 192.168.1.101  | Databases      | Template DB       | public         |

### Personalizando a Migração

- **SNMP Version**: A versão SNMP pode ser configurada diretamente na interface, podendo ser **1**, **2**, ou **3**, dependendo do tipo de configuração do host.
- **Status do Host**: O status dos hosts pode ser configurado para **Ativo** ou **Inativo**, dependendo da necessidade da sua infraestrutura.


### 🔐 **Aviso de Segurança**

- Certifique-se de não compartilhar suas credenciais do Zabbix de forma insegura. Utilize práticas recomendadas de segurança como armazenamento seguro de senhas e autenticação com tokens.

---

## 🌟 **Dicas**

- O programa pode ser usado para migrar dezenas ou centenas de hosts em poucos minutos, economizando tempo e evitando erros comuns em configurações manuais.
- Durante o uso, sempre monitore o painel de logs para garantir que todos os hosts foram criados corretamente.
- Não se esqueça de verificar se todos os dados na planilha Excel estão corretos antes de iniciar a migração.

---

## 📜 **Licença**

Este software é distribuído sob a **MIT License**. Consulte o arquivo LICENSE para mais detalhes.

---

## 📝 **Autor**

**Felipe Thiago (@Rayzecon)**

---

![Zabbix Logo]([https://upload.wikimedia.org/wikipedia/commons/7/73/Zabbix_Logo.png](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6f/Zabbix_logo.svg/1280px-Zabbix_logo.svg.png))
