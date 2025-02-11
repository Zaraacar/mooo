# mooo
HIIII
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Special</title>
    <style>
        body {
            text-align: center;
            font-family: 'Arial', sans-serif;
            color: black;
            padding-top: 50px;
        }
        h1 {
            font-size: 50px;
        }
        .question {
            font-size: 30px;
            margin-top: 20px;
        }
        .button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 10px;
            background-color: lightpink;
        }
        #response {
            font-size: 30px;
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <!-- Start of the conversation -->
    <h1>Hiiii babyyyy</h1>
    <div id="question1" class="question">
        <button class="button" onclick="nextQuestion(1)">Weiter</button>
    </div>

    <!-- 1st Question: Valentine -->
    <div id="question2" class="question" style="display:none;">
        Ich weiß nicht, ob du was von Valentinstag hältst, aber it's ok.
        <br>
        <button class="button" onclick="nextQuestion(2)">Weiter</button>
    </div>

    <!-- 2nd Question: Do you love me -->
    <div id="question3" class="question" style="display:none;">
        Do you love me?
        <br>
        <button class="button" onclick="answerLove('yes')">Yes</button>
        <button class="button" onclick="answerLove('no')">No</button>
    </div>

    <div id="response3" class="question" style="display:none;"></div>

    <!-- 3rd Question: I Love You Moo -->
    <div id="question4" class="question" style="display:none;">
        I love you moo
        <br>
        <button class="button" onclick="answerMoo('mommy')">I love you too mommy</button>
        <button class="button" onclick="answerMoo('zara')">I love you too zara</button>
        <button class="button" onclick="answerMoo('mamushi')">I love you too mamushi</button>
    </div>

    <div id="response4" class="question" style="display:none;"></div>

    <!-- 4th Question: Sorry i have to ask this -->
    <div id="question5" class="question" style="display:none;">
        Sorry i have to ask this...
        <br>
        <button class="button" onclick="nextQuestion(5)">ok???</button>
    </div>

    <!-- 5th Question: Will you be my valentine -->
    <div id="question6" class="question" style="display:none;">
        Will you like be my valentine or do you find this cringe???!? (please be my valentine and touch me ob innappriate areas!)
        <br>
        <button class="button" onclick="answerValentine('weird')">No your weird</button>
        <button class="button" onclick="answerValentine('mommy')">Ok mommy</button>
        <button class="button" onclick="answerValentine('yesmommy')">Yes mommy</button>
        <button class="button" onclick="answerValentine('goodgirl')">Yes good girl</button>
        <button class="button" onclick="answerValentine('yesplease')">Yes please</button>
    </div>

    <div id="response6" class="question" style="display:none;"></div>

    <script>
        let currentQuestion = 1;

        // Go to the next question
        function nextQuestion(questionNumber) {
            if (questionNumber === 1) {
                document.getElementById("question1").style.display = 'none';
                document.getElementById("question2").style.display = 'block';
            } else if (questionNumber === 2) {
                document.getElementById("question2").style
