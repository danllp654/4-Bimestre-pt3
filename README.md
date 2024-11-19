<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ferramenta de Estudo</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Ferramenta Interativa de Estudo</h1>
        <nav>
            <ul>
                <li><a href="#flashcards">Flashcards</a></li>
                <li><a href="#quiz">Quiz</a></li>
                <li><a href="#sobre">Sobre</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <!-- Sessão de Flashcards -->
        <section id="flashcards">
            <h2>Flashcards</h2>
            <div class="flashcard-container">
                <div class="flashcard">
                    <div class="front">O que é HTML?</div>
                    <div class="back">Uma linguagem de marcação para criar páginas web.</div>
                </div>
            </div>
        </section>

        <!-- Sessão de Quiz -->
        <section id="quiz">
            <h2>Quiz</h2>
            <div class="quiz-container">
                <p>Qual a sigla de CSS?</p>
                <button class="quiz-option" onclick="checkAnswer(this, 'errado')">Computer Style Sheets</button>
                <button class="quiz-option" onclick="checkAnswer(this, 'correto')">Cascading Style Sheets</button>
                <button class="quiz-option" onclick="checkAnswer(this, 'errado')">Creative Style Scripts</button>
            </div>
            <p id="quiz-feedback"></p>
        </section>

        <!-- Sessão Sobre -->
        <section id="sobre">
            <h2>Sobre</h2>
            <p>Essa ferramenta foi criada para ajudar nos estudos de forma prática e interativa.</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Ferramenta de Estudo</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
    background: #f4f4f9;
    color: #333;
}

header {
    background: #007BFF;
    color: white;
    padding: 1rem 0;
    text-align: center;
}

header nav ul {
    list-style: none;
    padding: 0;
}

header nav ul li {
    display: inline;
    margin: 0 15px;
}

header nav ul li a {
    color: white;
    text-decoration: none;
}

main {
    padding: 20px;
}

section {
    margin-bottom: 40px;
}

.flashcard-container {
    display: flex;
    justify-content: center;
    margin-top: 20px;
}

.flashcard {
    width: 300px;
    height: 200px;
    background: #fff;
    border: 2px solid #007BFF;
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-size: 1.2rem;
    cursor: pointer;
    transition: transform 0.3s;
}

.flashcard:hover {
    transform: rotateY(180deg);
}

.front, .back {
    display: none;
}

.flashcard:hover .back {
    display: block;
}

.flashcard:hover .front {
    display: none;
}

.quiz-container button {
    display: block;
    margin: 10px 0;
    padding: 10px;
    background: #007BFF;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background 0.3s;
}

.quiz-container button:hover {
    background: #0056b3;
}

footer {
    background: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
}
