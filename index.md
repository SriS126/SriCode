


## Sri's Page
### My name is Sri, and I like coding in Python. I am excited to take CSP as I can put my coding skills to the test. Below is my Freeform picture that can describe me.

![](images/IMG_3155.jpg)

## This is my favorite Youtuber and one of his videos
<iframe
    width="640"
    height="480"
    src="https://www.youtube.com/embed/guXTAOcrZaY"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>


<html>
<head>
    <title>Get To Know Me Game</title>
</head>
<body>
    <h1>Hello. Welcome to the Get To Know Me Game.</h1>
    <p>This is a multiple choice test that will test your knowledge about me.</p>

    <form id="quizForm">
        <div id="questionContainer"></div>
        <button type="button" onclick="checkAnswer()">Submit</button>
    </form>

    <script>
        const questions = ["What is my favorite movie?", "What is my favorite food?", "What is my favorite car?"];
        const responses = [
            ["A. Interstellar", "B. Spiderman: No Way Home", "C. Free Guy", "D. Avengers: Endgame"],
            ["A. Pizza", "B. Popcorn", "C. Ravioli", "D. Mac&Cheese"],
            ["A. Lamborghini Huracan", "B. Mclaren 720s", "C. Ferrari LaFerrari", "D. Bugatti Chiron"]
        ];
        const answers = ["C", "B", "D"];
        let currentQuestion = 0;

        function displayQuestion() {
            const questionContainer = document.getElementById("questionContainer");
            questionContainer.innerHTML = `
                <h2>${questions[currentQuestion]}</h2>
                ${responses[currentQuestion].map((response, index) => `
                    <label>
                        <input type="radio" name="answer" value="${index}">
                        ${response}
                    </label><br>
                `).join("")}
            `;
        }

        function checkAnswer() {
            const selectedAnswerIndex = parseInt(document.querySelector('input[name="answer"]:checked').value);
            const selectedAnswer = responses[currentQuestion][selectedAnswerIndex];
            const correctAnswer = answers[currentQuestion];

            if (selectedAnswer.charAt(0) === correctAnswer) {
                alert("Correct!");
            } else {
                alert("Incorrect");
            }

            currentQuestion++;
            if (currentQuestion < questions.length) {
                displayQuestion();
            } else {
                alert("Quiz completed!");
            }
        }

        displayQuestion();
    </script>
</body>
</html>

## Here are some of my social media profiles:
## [Github](https://github.com/SriS126)  

## [Instagram](https://www.instagram.com/sri__s126/?next=%2F)