# Projeto do Semestre

## Tema

Aplicativo de agenda de treinos.

## Stack

- Frontend: React Native com TypeScript
- Backend fake: `json-server`
- Fluxo: login -> home -> CRUD de treinos

## Requisitos atendidos

- Modelagem simples com usuario e treinos
- Tela de login integrada ao back
- Tela home com dados do back
- Funcao principal completa funcionando com CRUD

## Modelagem do banco

### Tabela `usuarios`

- `id`: number
- `nome`: string
- `email`: string
- `senha`: string

### Tabela `treinos`

- `id`: number
- `usuarioId`: number
- `titulo`: string
- `descricao`: string
- `intensidade`: string
- `horario`: string
- `concluido`: boolean

## Endpoints usados

- `GET /usuarios?email=...&senha=...`
- `GET /treinos?usuarioId=1`
- `POST /treinos`
- `PATCH /treinos/:id`
- `DELETE /treinos/:id`

## Funcao principal

Gerenciamento de treinos:

1. Fazer login com usuario salvo no `json-server`
2. Listar treinos do usuario
3. Cadastrar novo treino
4. Marcar treino como finalizado
5. Excluir treino

## Estrutura do projeto

```text
src/
  api/
    api.ts
  components/
    WorkoutCard.tsx
  screens/
    LoginScreen.tsx
    HomeScreen.tsx
  services/
    authService.ts
    treinosService.ts
  types/
    index.ts
App.tsx
db.json
```

## Roteiro de apresentacao

1. Mostrar o `db.json`
2. Rodar o `json-server`
3. Abrir o app no Expo Go
4. Fazer login com o usuario de teste
5. Mostrar os treinos carregados
6. Cadastrar, finalizar e excluir um treino
