📌 Descrição do Projeto
Biblioteca de Jogos Digitais é um projeto Fullstack desenvolvido com Node.js (Express) no backend, MySQL como banco de dados e React (Vite) no frontend.
Ele permite que os usuários adicionem jogos a uma biblioteca, associando-os a gêneros, e pesquisem jogos por gênero.

📂 Tecnologias Utilizadas

✅ Frontend: React (Vite), Axios, React Router DOM, CSS Puro

✅ Backend: Node.js, Express.js, MySQL2, CORS, Dotenv

✅ Banco de Dados: MySQL (XAMPP, MySQL Workbench)

📌 Funcionalidades

✅ Criar, listar e pesquisar jogos

✅ Cadastrar e gerenciar gêneros

✅ Filtrar jogos por gênero na Home

📌 Como Executar o Projeto

1️⃣ Clonar o Repositório
git clone https://github.com/seu-usuario/biblioteca-jogos.git
cd biblioteca-jogos

2️⃣ Configurar o Banco de Dados

Abra o MySQL Workbench ou phpMyAdmin e execute:
CREATE DATABASE biblioteca_jogos;

USE biblioteca_jogos;


CREATE TABLE generos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL UNIQUE
);


CREATE TABLE jogos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    titulo VARCHAR(255) NOT NULL,
    descricao TEXT NOT NULL,
    imagem_url VARCHAR(255),
    video_url VARCHAR(255),
    genero_id INT,
    FOREIGN KEY (genero_id) REFERENCES generos(id) ON DELETE SET NULL
);

(Opcional) Adicione gêneros e jogos de teste:


INSERT INTO generos (nome) VALUES ('Ação'), ('RPG'), ('Estratégia'), ('Corrida');


INSERT INTO jogos (titulo, descricao, imagem_url, video_url, genero_id) VALUES
('God of War', 'Jogo de ação e aventura.', 'https://example.com/gow.jpg', 'https://youtube.com/watch?v=123', 1),
('The Witcher 3', 'RPG épico.', 'https://example.com/witcher3.jpg', 'https://youtube.com/watch?v=456', 2);

3️⃣ Configurar o Backend

Acesse a pasta do backend:

cd backend

Instale as dependências:

npm install

Crie o arquivo .env e configure o banco de dados:
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_DATABASE=biblioteca_jogos

Execute o servidor:
node server.js
O backend rodará em http://localhost:5000 🚀

4️⃣ Configurar o Frontend

Acesse a pasta do frontend:

cd ../frontend

Instale as dependências:

npm install

Execute o frontend:

npm run dev

O frontend estará disponível em http://localhost:5173 🌎

📌 Como Usar

Acesse http://localhost:5173

Adicione um gênero em "Adicionar Gênero"

Adicione um jogo em "Adicionar Jogo"

Veja os jogos listados na Home

Use o filtro para pesquisar jogos por gênero

📌 Autor

👨‍💻 Desenvolvido por andrensaraiva

