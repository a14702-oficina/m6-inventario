# 💻 Inventário de Computadores – Aplicação Web

[![Tecnologia](https://img.shields.io/badge/Tecnologia-PHP%20%7C%20SQL%20%7C%20Bootstrap-blue.svg)](https://www.php.net/)
[![Status](https://img.shields.io/badge/Status-Concluído-success.svg)]()

## 🎯 Visão Geral do Projeto

Este projeto consiste no desenvolvimento de uma **aplicação web para a gestão centralizada do inventário de computadores** de uma sala de informática. O objetivo principal é fornecer uma ferramenta eficiente para a organização e consulta de informações técnicas e de software dos equipamentos.

A aplicação foi desenvolvida no âmbito da disciplina de **REDES – M6 – Programação de Sistemas de Informação** do curso GPSI – 2.º Ano.

## ✨ Funcionalidades Principais

A aplicação oferece as seguintes funcionalidades para facilitar a gestão do inventário:

| Funcionalidade | Descrição |
| :--- | :--- |
| **Listagem por Sala** | Visualização organizada dos computadores, agrupados por sala, com contadores de equipamentos. |
| **Detalhe do Computador** | Página dedicada para cada equipamento, exibindo especificações técnicas (Processador, RAM, SO, Gráfica) e o software instalado. |
| **Pesquisa Avançada** | Sistema de pesquisa e filtragem que permite localizar computadores por **nome**, **processador**, **sistema operativo** ou **software instalado**. |
| **Dashboard Interativo** | Interface moderna e responsiva (Bootstrap 5) com cards de salas e indicadores visuais. |
| **API de Pesquisa (AJAX)** | Endpoint dedicado (`api_pesquisa.php`) para consultas rápidas e dinâmicas. |

## 🛠️ Tecnologias Utilizadas

O projeto foi construído com as seguintes tecnologias:

*   **Backend:** PHP (com PDO para acesso seguro à base de dados)
*   **Base de Dados:** SQL (MySQL/TiDB)
*   **Frontend:** HTML5, CSS3 (Personalizado), Bootstrap 5, Bootstrap Icons
*   **Estrutura:** Arquitetura MVC simplificada (com ficheiros PHP independentes para lógica e visualização).

## 📂 Estrutura do Projeto

O projeto é composto pelos seguintes ficheiros principais:

| Ficheiro | Descrição |
| :--- | :--- |
| `index.php` | Página principal. Responsável pela listagem de salas, contadores e a listagem inicial de computadores. |
| `detalhe.php` | Página de visualização das especificações técnicas e software de um computador específico. |
| `config.php` | Ficheiro de configuração da ligação à base de dados (PDO). |
| `pesquisa.php` | Página para a funcionalidade de pesquisa geral. |
| `api_pesquisa.php` | Endpoint para requisições AJAX, devolvendo resultados de pesquisa em formato JSON. |

### 🗄️ Modelo de Dados (Base de Dados)

O sistema utiliza um modelo relacional simples com as seguintes tabelas:

*   `salas`
*   `computadores`
*   `software`
*   `computador_software` (Tabela de ligação N:N entre `computadores` e `software`)

## 🚀 Como Executar o Projeto

Para configurar e executar este projeto localmente, siga os passos abaixo:

1.  **Requisitos:** Certifique-se de ter um ambiente de servidor web (como XAMPP, WAMP ou MAMP) com **PHP** e **MySQL** instalados.
2.  **Base de Dados:** Crie uma base de dados MySQL e importe o esquema de tabelas (o esquema não está incluído, mas as tabelas necessárias são `salas`, `computadores`, `software` e `computador_software`).
3.  **Configuração:** Edite o ficheiro `config.php` com as suas credenciais de base de dados:
    ```php
    $host = "seu_host";
    $dbname = "seu_db_name";
    $user = "seu_usuario";
    $pass = "sua_senha";
    ```
4.  **Acesso:** Coloque os ficheiros do projeto no diretório raiz do seu servidor web e aceda através do seu navegador.

## 🌐 Demonstração Online

Pode visualizar uma demonstração do projeto em funcionamento através do seguinte URL:

[https://a14702-oficina.infinityfree.me/m6-inventario/index.php](https://a14702-oficina.infinityfree.me/m6-inventario/index.php)

## 👤 Contexto e Autoria

Este projeto foi desenvolvido por **Daniel Oliveira Santos** como parte do trabalho prático da disciplina de **REDES – M6 – Programação de Sistemas de Informação**.

### 🤖 Uso de Inteligência Artificial (IA)

A IA foi utilizada como uma **ferramenta de apoio técnico e criativo**, auxiliando nas seguintes áreas:

*   **Apoio ao Código:** Escrita, correção e sugestões de boas práticas em código PHP.
*   **Design e Interface:** Sugestões para melhoria do layout CSS, cores, ícones e organização do dashboard.
*   **Resolução de Problemas:** Esclarecimento de erros e sugestões de soluções práticas, especialmente na implementação de filtros complexos com múltiplas tabelas SQL.

### 🚧 Dificuldades Superadas

As principais dificuldades encontradas e superadas durante o desenvolvimento foram:

1.  Implementação de **filtros e pesquisa** que abrangessem dados de múltiplas tabelas (`computadores` e `software`).
2.  Ajuste do **layout para garantir a responsividade** e um design visualmente agradável.
3.  Garantir a **segurança e boas práticas** na ligação e manipulação da base de dados com PHP (PDO).
