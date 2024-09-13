# Plusoft3Sprint


## Integrantes
- Raphael Pabst rm98525
- Silvio Junior rm550821
- Pedro Braga rm551061
- Eduardo Reis Braga rm551987
- Vinícius Martins Torres Abdala rm99455

# Arquitetura da API

## Abordagem Monolítica

A arquitetura adotada para esta API é **monolítica**, onde toda a aplicação é estruturada em um único projeto e executada como uma única unidade. Essa escolha é justificada pela simplicidade do sistema, o que facilita o desenvolvimento e a manutenção, especialmente dado o tamanho atual da aplicação.

Optou-se por essa abordagem devido a fatores como:

- **Simplicidade**: A estrutura monolítica permite que toda a aplicação seja desenvolvida e gerenciada de forma mais simples.
- **Facilidade de manutenção**: Ideal para projetos menores, onde é mais fácil gerenciar dependências e controlar a evolução do código.
- **Desempenho interno**: A comunicação entre componentes é rápida e direta, uma vez que ocorre dentro de um único processo.
- **Eficiência no gerenciamento de times**: Mais adequado para equipes menores e ciclos de entrega mais curtos.

Esse tipo de arquitetura é especialmente vantajoso nas fases iniciais de um projeto, onde a simplicidade de implementação, depuração e testes são essenciais. Para APIs relativamente pequenas, a ausência da sobrecarga de rede presente em uma arquitetura de microserviços traz ganhos de desempenho na comunicação interna.

---

## Endpoints CRUD

Os endpoints da API seguem o padrão **CRUD** (Create, Read, Update, Delete) para os recursos:

- **Clientes**
- **Emails**
- **Endereços**
- **Produtos**

Cada recurso interage com o banco de dados **Oracle** utilizando o **Entity Framework Core**, garantindo a integração e manipulação de dados de forma eficiente. Os seguintes métodos RESTful são implementados:

- **GET**: Recupera recursos.
- **POST**: Cria novos recursos.
- **PUT**: Atualiza recursos existentes.
- **DELETE**: Exclui recursos.

Esses métodos estão disponíveis para todos os recursos mencionados, garantindo conformidade com as práticas recomendadas de APIs RESTful.

**HTTP responses**
| Código | Descrição |
|---|---|
| 200 | Requisição executada com sucesso (success)|
| 400 | Bad request|
| 404 | Registro pesquisado não encontrado (Not found)|
| 500 | Internal server error|
---


### Listar Cliente

#### Endpoint

- **Método**: GET  
- **URL**: 'localhost:7146/api/Clientes'

#### Descrição
Este endpoint retorna a lista de todos os clientes cadastrados no sistema.

Exemplo Corpo de resposta
![image](https://github.com/user-attachments/assets/10a7ef6f-3cac-4e4b-b472-fd63fd61cc64)



### Buscar Cliente

#### Endpoint

- **Método**: GET  
- **URL**: 'localhost:7146/api/Clientes/4'

- #### Descrição
Este endpoint retorna o ID do cliente cadastrado no sistema.

Exemplo Corpo de resposta
![image](https://github.com/user-attachments/assets/e141ccf3-a6a7-46ae-bec2-806384c60b7b)








