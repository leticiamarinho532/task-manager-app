# Task Manager – Laravel API + Vue.js Frontend

Este é um mini sistema de gerenciamento de tarefas desenvolvido com **Laravel (API)** e **Vue.js (frontend)**.  

---

## 🚀 Funcionalidades

- Registro e login de usuário
- Autenticação com Laravel Sanctum
- CRUD completo de tarefas
- Atualização de status (pendente/concluída)
- Logout e limpeza de sessão/token
- Interface simples e responsiva com Vue.js + Vite
- Consumo da API via Axios
- CORS configurado corretamente
- Deploy em ambiente real

---

## 🛠️ Tecnologias utilizadas

### **Backend – Laravel**
- PHP 8+
- Laravel 12+
- Laravel Breeze (API)
- Sanctum
- MySQL
- Eloquent ORM

### **Frontend – Vue.js**
- Vue 3
- Vite
- Axios
- Vue Router
- TailwindCSS

### Infra
- Docker
- Docker Compose
- MySQL 8
- Nginx

---

## 📁 Estrutura do Projeto

backend/ → API Laravel
frontend/ → Aplicação Vue.js

## 🗄️ Backend – Laravel

### 2. Configure o arquivo .env
cp backend/.env.example backend/.env

### Edite as variáveis:
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=taskmanager
DB_USERNAME=root
DB_PASSWORD=root

### 3. Suba os containers

docker-compose up -d --build

Isso irá subir:
- PHP-FPM
- Nginx
- Banco de dados
- Frontend Vite
- Backend Laravel

### 4. Instale as dependências do backend

docker-compose exec backend composer install

### 5. Gere key e rode migrations

docker-compose exec backend php artisan key:generate
docker-compose exec backend php artisan migrate

## 💻 Frontend – Vue.js

O frontend fica no container frontend.

### Instale as dependências

docker-compose exec frontend npm install

### Rodar o ambiente

docker-compose exec frontend npm run dev


