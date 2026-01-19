# 💻 Inventário de Computadores

## Descrição do Projeto

Este projeto é um sistema simples de **Inventário de Computadores** desenvolvido em PHP e MySQL. O seu objetivo é permitir a gestão e visualização dos equipamentos informáticos distribuídos por diferentes salas.

A aplicação oferece uma visão geral do número de computadores por sala e permite consultar os detalhes de hardware e software instalado em cada máquina.

## Funcionalidades

*   **Visualização por Sala:** Apresenta um resumo do total de computadores por sala.
*   **Filtro Interativo:** Permite filtrar a lista de computadores por sala.
*   **Detalhe do Computador:** Exibe as especificações de hardware (Processador, RAM, Armazenamento, Sistema Operativo) e a lista de software instalado para um computador específico.
*   **Design Responsivo:** Utiliza Bootstrap 5 para uma interface moderna e adaptável.

## Tecnologias Utilizadas

| Categoria | Tecnologia | Versão |
| :--- | :--- | :--- |
| **Backend** | PHP | - |
| **Base de Dados** | MySQL (via PDO) | - |
| **Frontend** | HTML5, CSS3 | - |
| **Framework CSS** | Bootstrap | 5.3.2 |
| **Ícones** | Bootstrap Icons | 1.11.1 |

## Estrutura da Base de Dados (Schema)

O sistema utiliza uma base de dados relacional com as seguintes tabelas:

### 1. `salas`

Armazena informações sobre as localizações dos computadores.

| Coluna | Tipo | Descrição |
| :--- | :--- | :--- |
| `id_sala` | INT (PK) | Identificador único da sala. |
| `nome_sala` | VARCHAR | Nome da sala (ex: "Sala 1.1"). |
| `localizacao` | VARCHAR | Localização física (ex: "Piso 1"). |

### 2. `computadores`

Armazena as especificações de hardware de cada máquina.

| Coluna | Tipo | Descrição |
| :--- | :--- | :--- |
| `id_computador` | INT (PK) | Identificador único do computador. |
| `id_sala` | INT (FK) | Chave estrangeira para a tabela `salas`. |
| `nome_computador` | VARCHAR | Nome de identificação da máquina. |
| `processador` | VARCHAR | Modelo do processador (CPU). |
| `ram` | VARCHAR | Quantidade de memória RAM. |
| `armazenamento` | VARCHAR | Capacidade de armazenamento (HDD/SSD). |
| `sistema_operativo` | VARCHAR | Sistema operativo instalado. |

### 3. `software`

Lista o software que pode ser instalado nos computadores.

| Coluna | Tipo | Descrição |
| :--- | :--- | :--- |
| `id_software` | INT (PK) | Identificador único do software. |
| `nome_software` | VARCHAR | Nome do software (ex: "Microsoft Office"). |
| `versao` | VARCHAR | Versão do software. |

### 4. `computador_software`

Tabela de ligação (muitos-para-muitos) entre `computadores` e `software`.

| Coluna | Tipo | Descrição |
| :--- | :--- | :--- |
| `id_computador` | INT (FK) | Chave estrangeira para a tabela `computadores`. |
| `id_software` | INT (FK) | Chave estrangeira para a tabela `software`. |

## Configuração e Instalação

Para colocar o projeto a funcionar, siga os seguintes passos:

### 1. Configuração do Servidor

O projeto requer um ambiente de servidor web com suporte a PHP e MySQL (ex: XAMPP, WAMP, MAMP ou um servidor dedicado).

### 2. Base de Dados

Crie a base de dados no seu servidor MySQL e importe o schema (estrutura) das tabelas acima.

### 3. Ficheiro de Configuração (`config.php`)

Edite o ficheiro `config.php` com as credenciais da sua base de dados.

**Credenciais Atuais (Atenção: Mude estas credenciais por motivos de segurança!)**

```php
<?php
$host = "localhost"; // MUDAR
$dbname = "inventario_db"; // MUDAR
$user = "root"; // MUDAR
$pass = ""; // MUDAR (no XAMPP/WAMP, pode ser vazio "")

try {
    $pdo = new PDO("mysql:host=$host;dbname=$dbname;charset=utf8", $user, $pass);
    $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
} catch (PDOException $e) {
    die("Erro na ligação à BD: " . $e->getMessage());
}
?>
```

### 4. Acesso

Coloque os ficheiros `config.php`, `index.php` e `detalhe.php` no diretório raiz do seu servidor web (ex: `htdocs` no XAMPP).

Aceda à aplicação através do seu navegador: `http://localhost/index.php` (ou o caminho correspondente).
