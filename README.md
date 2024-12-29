# AluGames

## Descrição
AluGames é um projeto de estudo em Kotlin com o objetivo de explorar conceitos como:
- Consumo de APIs REST usando a biblioteca `HttpClient`.
- Manipulação de JSON com a biblioteca `Gson`.
- Uso de estruturas de dados e boas práticas de orientação a objetos.
- Implementação de lógicas para ordenação, filtragem e remoção de itens.
- Validação de dados e geração de identificadores exclusivos para os "Gamers".

O projeto simula um sistema de cadastro de jogadores (gamers), com a possibilidade de buscar e gerenciar informações de jogos consumidas de uma API externa.

---

## Funcionalidades

- Cadastro de gamers com validação de nome e e-mail.
- Geração automática de IDs exclusivos para os gamers.
- Busca de informações de jogos por meio da API [CheapShark](https://www.cheapshark.com/api).
- Ordenação e filtragem de jogos buscados.
- Possibilidade de adicionar descrições personalizadas aos jogos.
- Remoção de jogos da lista de buscados.

---

## Tecnologias Utilizadas

- **Linguagem:** Kotlin
- **Gerenciador de Dependências:** Maven
- **APIs Utilizadas:** [CheapShark](https://www.cheapshark.com/api)
- **Bibliotecas:**
  - `Gson`: Manipulação de JSON.
  - `HttpClient`: Consumo de APIs REST.
  - `JUnit 5`: Testes unitários.

---

## Estrutura do Projeto

- **`Gamer`**: Classe que representa o jogador, com métodos para validação de e-mail, criação de IDs e gerenciamento de jogos.
- **`Jogo`**: Classe que representa os jogos buscados na API, incluindo título, capa e descrição.
- **`ConsumoApi`**: Classe responsável pelo consumo da API CheapShark.
- **`Main`**: Contém a lógica principal do programa, incluindo interação com o usuário para cadastro de gamers e busca de jogos.

---

## Como Executar

### Requisitos
- Java 11+
- Maven instalado
- Conexão com a internet para consumir a API

### Passos
1. Clone este repositório:
   ```bash
   git clone[https://github.com/LuanadeSouza/Alugames.git)
   cd AluGames
   ```

2. Compile o projeto:
   ```bash
   mvn compile
   ```

3. Execute a aplicação:
   ```bash
   mvn exec:java
   ```

---

## Exemplo de Execução

1. Cadastro de Gamer:
   - Digite nome e e-mail.
   - Escolha se deseja adicionar mais informações (data de nascimento e usuário).

2. Busca de Jogos:
   - Informe o ID de um jogo.
   - Escolha adicionar uma descrição personalizada ou usar o título do jogo como descrição.

3. Gerenciamento de Jogos:
   - Ordene os jogos buscados por título.
   - Filtre jogos por palavras-chave.
   - Remova jogos da lista conforme necessário.

---

## Estrutura de Diretórios
```
AluGames/
├── src/
│   ├── main/
│   │   ├── kotlin/
│   │   │   ├── Gamer.kt
│   │   │   ├── Jogo.kt
│   │   │   ├── ConsumoApi.kt
│   │   │   └── Main.kt
│   ├── test/
│   │   ├── kotlin/
│   │   │   └── TestesUnitarios.kt
├── pom.xml
```

---

## Inspiração
Este projeto foi inspirado pela necessidade de praticar conceitos de consumo de APIs, manipulação de dados e boas práticas de programação orientada a objetos. Também foi projetado para explorar a manipulação de listas e o uso de lógicas condicionais em Kotlin.

---

## Contribuições
Contribuições são bem-vindas! Abra um pull request ou relate problemas na aba de issues.

---

## Licença
Este projeto está licenciado sob a [MIT License](LICENSE).
