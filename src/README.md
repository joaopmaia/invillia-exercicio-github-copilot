<<<<<<< HEAD
<<<<<<< HEAD
# Mergington High School Activities API

A super simple FastAPI application that allows students to view and sign up for extracurricular activities.

## Features

- View all available extracurricular activities
- Sign up for activities

## Getting Started

1. Install the dependencies:
=======
=======
>>>>>>> main
# API de Atividades da Escola Secundária Mergington

Uma aplicação extremamente simples usando FastAPI que permite aos estudantes visualizar e se inscrever em atividades extracurriculares.

## Funcionalidades

- Visualizar todas as atividades extracurriculares disponíveis
- Inscrever-se em atividades

## Como começar

1. Instale as dependências:
<<<<<<< HEAD
>>>>>>> dd563bf (Initial commit)
=======
>>>>>>> main

   ```
   pip install fastapi uvicorn
   ```

<<<<<<< HEAD
<<<<<<< HEAD
2. Run the application:
=======
2. Execute a aplicação:
>>>>>>> dd563bf (Initial commit)
=======
2. Execute a aplicação:
>>>>>>> main

   ```
   python app.py
   ```

<<<<<<< HEAD
<<<<<<< HEAD
3. Open your browser and go to:
   - API documentation: http://localhost:8000/docs
   - Alternative documentation: http://localhost:8000/redoc

## API Endpoints

| Method | Endpoint                                                          | Description                                                         |
| ------ | ----------------------------------------------------------------- | ------------------------------------------------------------------- |
| GET    | `/activities`                                                     | Get all activities with their details and current participant count |
| POST   | `/activities/{activity_name}/signup?email=student@mergington.edu` | Sign up for an activity                                             |

## Data Model

The application uses a simple data model with meaningful identifiers:

1. **Activities** - Uses activity name as identifier:

   - Description
   - Schedule
   - Maximum number of participants allowed
   - List of student emails who are signed up

2. **Students** - Uses email as identifier:
   - Name
   - Grade level

All data is stored in memory, which means data will be reset when the server restarts.
=======
=======
>>>>>>> main
3. Abra seu navegador e acesse:
   - Documentação da API: http://localhost:8000/docs
   - Documentação alternativa: http://localhost:8000/redoc

## Endpoints da API

| Método | Endpoint                                                          | Descrição                                                                  |
| ------ | ----------------------------------------------------------------- | -------------------------------------------------------------------------- |
| GET    | `/activities`                                                     | Obter todas as atividades com detalhes e número atual de participantes     |
| POST   | `/activities/{activity_name}/signup?email=student@mergington.edu` | Inscrever-se em uma atividade                                              |

## Modelo de Dados

A aplicação utiliza um modelo de dados simples com identificadores claros:

1. **Atividades** - Usa o nome da atividade como identificador:

   - Descrição
   - Horários
   - Número máximo permitido de participantes
   - Lista de e-mails dos estudantes inscritos

2. **Estudantes** - Usa o e-mail como identificador:
   - Nome
   - Ano escolar

<<<<<<< HEAD
Todos os dados são armazenados em memória, portanto os dados serão redefinidos quando o servidor for reiniciado.
>>>>>>> dd563bf (Initial commit)
=======
Todos os dados são armazenados em memória, portanto os dados serão redefinidos quando o servidor for reiniciado.
>>>>>>> main
