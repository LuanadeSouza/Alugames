# AluGames

Um sistema de gerenciamento de aluguel de jogos com funcionalidades como cadastro de gamers, jogos, planos de assinatura e recomendação de jogos. Desenvolvido em Kotlin, utilizando Hibernate e MySQL, o projeto explora boas práticas de design orientado a objetos, persistência de dados e consumo de APIs externas.

## Funcionalidades

### Gamers:
- Cadastro de gamers com nome, e-mail, data de nascimento e usuário.
- Geração automática de ID interno exclusivo.
- Possibilidade de recomendação de jogos baseados em notas.

### Jogos:
- Cadastro e busca de jogos com título, capa, descrição e preço.
- Consumo de APIs externas para buscar dados de jogos e criar objetos dinâmicos.
- Recomendação de jogos baseadas em avaliações de gamers.

### Aluguéis:
- Registro de aluguéis de jogos vinculados a gamers.
- Cálculo automático do valor do aluguel baseado no plano do gamer.
- Gerenciamento de período de aluguéis.

### Planos:
- Sistema de planos de assinatura (ex.: Bronze, Prata, Ouro, Platina, Diamante).
- Gerenciamento de mensalidades e descontos baseados em reputação.
- Registro de planos avulsos sem mensalidade fixa.

## Tecnologias Utilizadas

- **Linguagem:** Kotlin
- **Banco de Dados:** MySQL
- **ORM:** Hibernate
- **API REST:** CheapShark API
- **Ferramentas:**
  - Maven
  - Gson
  - JPA (Java Persistence API)
- **Testes:** JUnit

## Estrutura do Projeto

```bash
src
├── dados
│   ├── AluguelDAO.kt
│   ├── GamerDAO.kt
│   ├── JogoDAO.kt
│   ├── PlanoDAO.kt
│   ├── Banco.kt
├── modelo
│   ├── Aluguel.kt
│   ├── Gamer.kt
│   ├── Jogo.kt
│   ├── Plano.kt
├── principal
│   ├── Main.kt
│   ├── OperacoesGamer.kt
│   ├── OperacoesJogo.kt
├── servicos
│   ├── ConsumoApi.kt
├── utilitario
│   ├── Conversores.kt
├── resources
│   ├── META-INF/persistence.xml
├── pom.xml
```

## Como Executar o Projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/usuario/AluGames.git
   ```

2. Configure o banco de dados:
   - Crie um banco de dados MySQL chamado `alugames`.
   - Atualize as credenciais no arquivo `persistence.xml`.

3. Compile e execute o projeto:
   ```bash
   mvn clean install
   mvn exec:java
   ```

4. Execute as operações principais no console, como cadastro de gamers, busca de jogos e registro de aluguéis.

## Exemplo de Uso

### Cadastro de Gamer:
```plaintext
Digite seu nome: John Doe
Digite seu e-mail: john.doe@example.com
Deseja completar seu cadastro com usuário e data de nascimento? (S/N): S
Digite sua data de nascimento (DD/MM/AAAA): 15/06/1990
Digite seu nome de usuário: johndoe90
```

### Busca de Jogo:
```plaintext
Digite um código de jogo para buscar: 12345
Jogo encontrado:
Título: Resident Evil Village
Deseja inserir uma descrição personalizada? (S/N): N
```

### Registro de Aluguel:
```plaintext
Digite o código do jogo para alugar: 12345
Digite o período de aluguél (em dias): 7
Aluguel registrado com sucesso!
```

## Licença

Este projeto é licenciado sob a Licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

---

**Desenvolvido como parte dos estudos no programa da Alura.**
