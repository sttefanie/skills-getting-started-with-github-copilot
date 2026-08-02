# API de Atividades da Mergington High School

Uma aplicação FastAPI super simples que permite que estudantes vejam e se inscrevam em atividades extracurriculares.

## Funcionalidades

- Listar todas as atividades extracurriculares disponíveis
- Permitir inscrição de estudantes em atividades

## Como começar

1. Instale as dependências:

   ```
   pip install fastapi uvicorn
   ```

2. Execute a aplicação:

   ```
   python app.py
   ```

3. Abra no navegador:
   - Documentação da API (Swagger UI): http://localhost:8000/docs
   - Documentação alternativa (Redoc): http://localhost:8000/redoc

## Endpoints da API

| Método | Endpoint                                                         | Descrição                                                             |
| ------ | ---------------------------------------------------------------- | --------------------------------------------------------------------- |
| GET    | `/activities`                                                     | Retorna todas as atividades com detalhes e contagem de participantes  |
| POST   | `/activities/{activity_name}/signup?email=student@mergington.edu` | Inscreve um estudante em uma atividade                                |

## Modelo de dados

A aplicação armazena dados em memória (serão perdidos ao reiniciar o servidor).

1. Activities — identificada pelo nome da atividade:
   - description
   - schedule
   - max_participants
   - participants (lista de emails)

2. Students — identificado por email:
   - name
   - grade level
