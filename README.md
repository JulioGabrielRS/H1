# Agenda de Treinos

Projeto do semestre com:

- Frontend em React Native + TypeScript
- Backend fake com `json-server`
- Tela de login
- Tela home inicial
- Funcao completa de treinos integrada ao back

## O que foi ajustado

- Recriacao da pasta `src/` que estava faltando no projeto
- Fluxo funcional de login
- Home com CRUD basico de treinos
- Estrutura compativel com Expo Go, sem bibliotecas nativas extras

## Como executar

1. Instale as dependencias:

```bash
npm install
```

2. Inicie o backend fake:

```bash
npm run server
```

3. Em outro terminal, inicie o app:

```bash
npm start
```

4. Abra no Expo Go pelo QR Code.

Se aparecer erro de timeout no Expo Go, use:

```bash
npm run start:tunnel
```

Esse modo costuma funcionar melhor quando a rede local ou o firewall bloqueia a conexao direta com o Metro.

## Importante para Expo Go

O app agora tenta descobrir automaticamente o IP do computador a partir da URL do Expo, entao normalmente nao precisa editar `src/api/api.ts`.

Se o app abrir no Expo Go, mas login e treinos continuarem carregando para sempre, confirme se o backend esta rodando com:

```bash
npm run server
```

## Login de teste

- Email: `julio@email.com`
- Senha: `123456`

## Endpoints usados

- `GET /usuarios?email=...&senha=...`
- `GET /treinos?usuarioId=1`
- `POST /treinos`
- `PATCH /treinos/:id`
- `DELETE /treinos/:id`

## Observacao importante

O projeto usa `json-server`, entao o backend precisa ficar rodando enquanto o app estiver aberto.
