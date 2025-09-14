# ScreenMatch Console 🎬

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)

Este projeto é uma aplicação de console (via terminal) desenvolvida em Java para buscar e exibir informações sobre séries de TV, utilizando a OMDb API como fonte de dados.

## 🚀 Sobre o Projeto

O **ScreenMatch** permite que o usuário, através de uma interface de linha de comando, pesquise por suas séries favoritas e obtenha detalhes sobre suas temporadas e episódios. É um projeto focado no aprendizado e na prática de conceitos essenciais do ecossistema Java, como o consumo de APIs, a desserialização de dados (JSON) e a manipulação de objetos.

### Funcionalidades Principais
- **Busca de Séries:** Pesquise por qualquer série pelo título.
- **Listagem de Dados:** Visualize todas as temporadas e episódios da série encontrada.
- **Estatísticas:** Gere estatísticas, como o top 5 melhores episódios baseados na avaliação.
- **Interação via Console:** Toda a interação acontece de forma simples e direta no terminal.

## 💻 Tecnologias Utilizadas

Este projeto foi construído com as seguintes tecnologias:

- **Java:** Linguagem de programação principal, utilizada em sua versão 17 ou superior.
- **Spring Boot:** Utilizado para simplificar a configuração e a injeção de dependências, mesmo sem o módulo web. Ele gerencia o ciclo de vida dos componentes da aplicação de forma eficiente.
- **Maven:** Ferramenta de automação de build e gerenciamento de dependências. Responsável por baixar as bibliotecas necessárias para o projeto.
- **Jackson Databind:** Biblioteca para converter (desserializar) os dados no formato JSON, recebidos da API, em objetos Java, facilitando a manipulação dos dados.
- **OMDb API:** API externa que serve como fonte de dados para todas as informações sobre filmes e séries.

## 🏗️ Estrutura do Projeto

O código é organizado de forma modular, separando as responsabilidades em diferentes pacotes e classes:

- `br.com.alura.screenmatch.main.Principal`: Classe principal que contém o método `main`. É o ponto de entrada da aplicação e responsável por exibir o menu e interagir com o usuário.
- `br.com.alura.screenmatch.service.ConsumoApi`: Classe de serviço responsável por realizar as chamadas HTTP para a OMDb API e obter os dados brutos em formato JSON.
- `br.com.alura.screenmatch.service.ConverteDados`: Serviço que utiliza a biblioteca Jackson para desserializar a resposta JSON em objetos Java.
- `br.com.alura.screenmatch.model`: Pacote que contém as classes ou `Records` (`DadosSerie`, `DadosTemporada`, `DadosEpisodio`) que mapeiam a estrutura dos dados retornados pela API.

## ▶️ Como Executar

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/HenryPedro/screenmatch-sem-web.git](https://github.com/HenryPedro/screenmatch-sem-web.git)
   ```

2. **Navegue até o diretório do projeto:**
   ```bash
   cd screenmatch-sem-web
   ```

3. **Obtenha uma chave da API:**
   - Acesse [OMDb API](http://www.omdbapi.com/apikey.aspx) para obter sua chave de API gratuita.
   - Você precisará adicionar essa chave no código, provavelmente na classe `ConsumoApi` onde a URL da API é montada.

4. **Compile e execute o projeto:**
   - Sendo um projeto Maven, você pode executá-lo através da sua IDE (Eclipse, IntelliJ) ou compilá-lo e executá-lo via terminal.

```bash
# Compilar o projeto
mvn clean install

# Executar o arquivo .jar gerado (verifique o nome do arquivo na pasta /target)
java -jar target/screenmatch-0.0.1-SNAPSHOT.jar
```

---
*Este README foi gerado com a ajuda do Gemini.*
