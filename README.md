# Sistema de Gerenciamento de Tarefas

## Descrição
Este projeto é uma API RESTful para gerenciamento de tarefas utilizando Flask e SQLAlchemy.

## Tecnologias Utilizadas
- Python
- Flask
- Flask-SQLAlchemy

## Instalação

1. Clone o repositório:
    ```sh
    git clone https://github.com/DiogoPacker/DiogoPacker.git
    cd task_management
    ```

2. Crie e ative um ambiente virtual:
    ```sh
    python -m venv env
    source env/bin/activate  # no Windows use `env\Scripts\activate`
    ```

3. Instale as dependências:
    ```sh
    pip install -r requirements.txt
    ```

4. Configure o banco de dados:
    ```sh
    flask db init
    flask db migrate -m "Initial migration."
    flask db upgrade
    ```

5. Execute a aplicação:
    ```sh
    python app.py
    ```

## Uso
A API oferece os seguintes endpoints:

- `GET /tasks`: Retorna todas as tarefas.
    ```sh
    curl http://127.0.0.1:5000/tasks
    ```

- `POST /tasks`: Adiciona uma nova tarefa.
    ```sh
    curl -X POST http://127.0.0.1:5000/tasks -H "Content-Type: application/json" -d '{"title":"Minha primeira tarefa", "description":"Descrição da tarefa"}'
    ```

- `PUT /tasks/<id>`: Atualiza uma tarefa existente.
    ```sh
    curl -X PUT http://127.0.0.1:5000/tasks/<id> -H "Content-Type: application/json" -d '{"title":"Nova descrição da tarefa"}'
    ```

- `DELETE /tasks/<id>`: Deleta uma tarefa.
    ```sh
    curl -X DELETE http://127.0.0.1:5000/tasks/<id>
    ```
