## Hi there 👋

<!--
**OMANABM/OMANABM** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
--><!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>استبيان</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }

        h1, h2 {
            color: #333;
        }

        form {
            margin-bottom: 20px;
        }

        input[type="radio"] {
            margin-right: 10px;
        }

        button {
            padding: 10px 20px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #0056b3;
        }

        #result {
            font-size: 18px;
            font-weight: bold;
            color: #007BFF;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>استبيان تقييم</h1>
        <form id="surveyForm">
            <p>1. كيف تقيم تجربتك؟</p>
            <input type="radio" name="q1" value="1"> سيئة<br>
            <input type="radio" name="q1" value="2"> جيدة<br>
            <input type="radio" name="q1" value="3"> ممتازة<br>

            <p>2. هل تنصح الآخرين بتجربة هذه الخدمة؟</p>
            <input type="radio" name="q2" value="1"> لا<br>
            <input type="radio" name="q2" value="2"> نعم<br>

            <button type="button" onclick="submitSurvey()">اعتمد الإجابة</button>
        </form>

        <h2>النتيجة:</h2>
        <p id="result"></p>
    </div>

    <script>
        function submitSurvey() {
            var form = document.forms['surveyForm'];
            var score = 0;

            // جمع الدرجات من الأسئلة
            if (form.q1.value) {
                score += parseInt(form.q1.value);
            }
            if (form.q2.value) {
                score += parseInt(form.q2.value);
            }

            // عرض النتيجة
            document.getElementById('result').textContent = 'مجموع الدرجات: ' + score;
        }
    </script>
</body>
</html>

