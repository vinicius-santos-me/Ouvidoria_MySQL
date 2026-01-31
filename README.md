# 📢 Sistema de Ouvidoria — Python + MySQL

Um sistema de ouvidoria desenvolvido em **Python**, utilizando **MySQL** como banco de dados para armazenar e gerenciar manifestações dos usuários. O projeto oferece uma interface via terminal para realizar operações CRUD completas sobre as manifestações.

---

## 📋 Funcionalidades

| Função | Descrição |
|---|---|
| 📝 Criar manifestação | Registra uma nova manifestação no sistema |
| 📄 Listar todas | Exibe todas as manifestações cadastradas |
| 🗂️ Listar por tipo | Filtra manifestações por **Elogio**, **Sugestão** ou **Reclamação** |
| 🔎 Buscar por código | Pesquisa uma manifestação específica pelo seu código |
| 📊 Total de manifestações | Exibe a quantidade total de registros no banco |
| ❌ Excluir manifestação | Remove uma manifestação pelo seu código |

---

## 🏗️ Estrutura do Projeto

```
Ouvidoria_MySQL/
├── comando-sql.txt            # Scripts SQL para criação do banco e tabelas
├── interface_ouvidoria.py     # Interface no terminal (menu e interação com o usuário)
├── metodos_ouvidoria.py       # Métodos de conexão e operações no banco de dados
└── README.md                  # Documentação do projeto
```

- **`comando-sql.txt`** — contém os comandos necessários para criar o banco de dados e a tabela de manifestações no MySQL.
- **`interface_ouvidoria.py`** — responsável pelo menu interativo no terminal, recebe as entradas do usuário e chama os métodos apropriados.
- **`metodos_ouvidoria.py`** — gerencia a conexão com o MySQL e implementa todas as operações de banco de dados (INSERT, SELECT, DELETE).

---

## 🛠️ Requisitos

- **Python 3.x**
- **MySQL Server** (instalado e rodando)
- **Conector Python MySQL:**
  ```bash
  pip install mysql-connector-python
  ```

---

## 🚀 Como Executar

**1. Clone o repositório:**
```bash
git clone https://github.com/vinicius-santos-me/Ouvidoria_MySQL.git
cd Ouvidoria_MySQL
```

**2. Instale a dependência:**
```bash
pip install mysql-connector-python
```

**3. Configure o banco de dados:**

Abra o seu cliente MySQL (ex: MySQL Workbench ou terminal) e execute os comandos presentes no arquivo `comando-sql.txt` para criar o banco de dados e a tabela necessária.

**4. Configure a conexão:**

No arquivo `metodos_ouvidoria.py`, atualize as credenciais de conexão com o seu MySQL local:
```python
conexao = mysql.connector.connect(
    host="localhost",
    user="seu_usuario",
    password="sua_senha",
    database="nome_do_banco"
)
```

**5. Inicie o sistema:**
```bash
python interface_ouvidoria.py
```

O menu interativo aparecerá no terminal, permitindo realizar todas as operações do sistema.

---

## 💾 Tipos de Manifestação

O sistema suporta três tipos de manifestação:

- **Elogio** — reconhecimento positivo
- **Sugestão** — proposta de melhoria
- **Reclamação** — registro de insatisfação

---

## 📚 Tecnologias Utilizadas

- **Python 3** — linguagem principal
- **MySQL** — banco de dados relacional
- **mysql-connector-python** — biblioteca para conexão entre Python e MySQL

---

## 👤 Autor

Desenvolvido por [Vinícius Santos](https://github.com/vinicius-santos-me)
