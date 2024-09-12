# Plusoft3Sprint


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
