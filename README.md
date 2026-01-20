# 📊 Inventário de Computadores – Aplicação Web (PHP + SQL)

## 👤 Identificação
- **Nome do aluno:**  Daniel Oliveira Santos
- **Turma:** 2I
- **Disciplina:** REDES – M6 – Programação de Sistemas de Informação  
- **Curso:** GPSI – 2.º Ano  

---

## 🎯 Objetivo do Projeto
O objetivo deste projeto é desenvolver uma **aplicação web para gestão de inventário de computadores**, que centralize e organize informações sobre os equipamentos de uma sala de informática.

A aplicação permite:

1. **Consultar informações técnicas dos computadores** – processador, memória RAM, armazenamento, sistema operativo e placa gráfica.  
2. **Visualizar o software instalado em cada computador**, incluindo versões e licenças.  
3. **Pesquisar e filtrar computadores** por sala, nome ou software, facilitando a gestão.  

O sistema utiliza **PHP e SQL** para a lógica e base de dados, e **HTML, CSS e Bootstrap** para a interface web.


---

## 🧱 Estrutura Geral do Projeto
O projeto está organizado da seguinte forma:
- **index.php:** página principal com a listagem de salas e computadores.
- **detalhe.php:** página de detalhe de cada computador, mostrando especificações e softwares instalados.
- **config.php:** ficheiro de ligação à base de dados via PDO.
- **Base de dados:** tabelas `salas`, `computadores`, `software`, `computador_software` (relações N:N).
- **Estilos e layout:** CSS próprio + Bootstrap 5 + Bootstrap Icons.

---

## ⚙️ Funcionalidades Desenvolvidas
- [x] Ligação à base de dados com PHP (PDO)  
- [x] Listagem de computadores por sala  
- [x] Visualização das características técnicas de cada computador  
- [x] Consulta do software instalado  
- [x] Página de detalhe por computador  
- [x] Pesquisa por nome de computador  
- [x] Pesquisa por software  
- [x] Organização do dashboard com cards de salas e contadores  
- [x] Melhorias visuais no interface (cores modernas, gradientes, badges, ícones)  

---

## 🤖 Utilização da Inteligência Artificial (IA)

### 🔹 Onde utilizei IA
- Apoio na escrita e correção de código PHP.  
- Reorganização e melhoria do layout CSS e do dashboard.  
- Sugestões para badges, cores, ícones e animações.  
- Esclarecimento de erros e boas práticas de programação web.

### 🔹 Como utilizei a IA
- Recebi exemplos de código que foram adaptados ao meu projeto.  
- A IA ajudou a compreender erros e sugeriu soluções práticas.  
- Sugeriu melhorias visuais e estruturais que foram aplicadas na interface.  

---

## ✍️ Trabalho Desenvolvido Manualmente
- Personalização e adaptação do código sugerido.  
- Decisões de organização do dashboard e cores.  
- Escolha do estilo da interface. 

---

## 🚧 Dificuldades Encontradas
- Implementar filtros e pesquisa que incluíssem várias tabelas (computadores e software).  
- Ajustar o layout para que ficasse responsivo e visualmente agradável.  
- Entender corretamente como manter segurança e boas práticas em PHP.

---

## 📚 Aprendizagens Realizadas
- Ligação entre PHP e base de dados utilizando PDO.  
- Estruturação de queries SQL com `JOIN` e `COUNT`.  
- Criação de interfaces web modernas usando CSS, Bootstrap e ícones.  
- Organização e documentação do código.  
- Uso consciente de Inteligência Artificial como ferramenta de apoio técnico e criativo.

---
