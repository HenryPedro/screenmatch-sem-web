# ScreenMatch Console ☕

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)

Este projeto é uma aplicação de console desenvolvida em Java para buscar e exibir informações sobre séries de TV, utilizando a OMDb API.

## 🚀 Sobre o Projeto

O **ScreenMatch** é uma aplicação interativa que roda diretamente no terminal. O usuário pode buscar por uma série pelo nome e a aplicação consome a [OMDb API](https://www.omdbapi.com/) para obter e exibir dados detalhados sobre suas temporadas e episódios.

Este projeto foi desenvolvido como parte dos estudos da Formação Java da Alura, com foco em aplicar conceitos como consumo de APIs, desserialização de JSON e utilização do framework Spring para injeção de dependências em um contexto não-web.

### ✨ Funcionalidades

- **Busca de Séries:** Permite ao usuário buscar por uma série específica pelo título.
- **Listagem de Temporadas:** Exibe todas as temporadas da série encontrada.
- **Listagem de Episódios por Temporada:** Mostra os detalhes de todos os episódios de uma temporada específica.
- **Estatísticas da Série:** Apresenta dados como o top 5 melhores episódios baseados na avaliação.

## 🛠️ Tecnologias Utilizadas

O projeto foi construído com as seguintes tecnologias:

- **[Java](https://www.java.com/)**: Linguagem de programação principal.
- **[Spring Boot](https://spring.io/projects/spring-boot)**: Utilizado para gerenciar o ciclo de vida da aplicação e facilitar a injeção de dependências, mesmo sem o módulo web.
- **[Maven](https://maven.apache.org/)**: Gerenciador de dependências e automação de build do projeto.
- **[Jackson](https://github.com/FasterXML/jackson)**: Biblioteca para converter (desserializar) os dados em formato JSON recebidos da API em objetos Java.
- **[OMDb API](https://www.omdbapi.com/)**: API externa utilizada como fonte de dados para as informações sobre as séries.

## 🔧 Como Executar

Para executar este projeto localmente, siga os passos abaixo:

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/HenryPedro/screenmatch-sem-web.git](https://github.com/HenryPedro/screenmatch-sem-web.git)
   ```

2. **Navegue até o diretório do projeto:**
   ```bash
   cd screenmatch-sem-web
   ```
   
3. **Obtenha uma API Key:**
   - Acesse o site [OMDb API](https://www.omdbapi.com/apikey.aspx) e solicite uma chave de API gratuita.
   - Dentro do código, localize o local onde a chave da API é utilizada (geralmente na classe `ConsumoApi` ou em um arquivo de propriedades) e substitua pelo seu valor.

4. **Execute a aplicação usando o Maven:**
   ```bash
   mvn spring-boot:run
   ```
   
A aplicação será iniciada no seu terminal e você poderá interagir com o menu.

---
*Projeto desenvolvido por [HenryPedro](https://github.com/HenryPedro).*
