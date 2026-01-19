# To-Do API
To-Do API, made for Day 4 of Hack Club's Haxmas, is a simple REST API built for managing tasks. Made with TypeScript and the Hono framework, it utilizes a SQLite database managed by Drizzle to keep your tasks organized.\
<br>
Key Features:
- Hono servers
- SQLite database via Drizzle ORM

## Usage
To install dependencies:
```sh
bun install
```
To run:
```sh
bun run dev
```
Open http://localhost:3000 \
<br>
Once the server is running, you can interact with it using the routes listed below.\

## Available Endpoints
```
[GET]      /api/todo                          - List all to-dos
[GET]      /api/todo/complete                 - List completed to-dos
[GET]      /api/todo/incomplete               - List incomplete to-dos
[GET]      /api/todo/:id                      - Get a to-do by ID
[POST]     /api/todo                          - Create a new to-do
[PATCH]    /api/todo/:id                      - Update a to-do's task or description
[PATCH]    /api/todo/:id/toggleComplete       - Toggle a to-do's completion status
[DELETE]   /api/todo/:id                      - Delete a to-do by ID
[DELETE]   /api/todo/complete                 - Delete all completed to-dos
```
## Usage Example:
```
  curl -X POST http://localhost:3000/api/todo
       -H "Content-Type: application/json"
       -d '{"task": "Join Hack Club", "description": "Make cool stuff with code!"}'
```
