<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Hi Baby 💙</title>
    <style>
        body {
            font-family: 'Segoe UI', sans-serif;
            background: #fff0f5;
            color: #333;
            text-align: center;
            padding: 40px;
        }
        h1 {
            color: #c94f7c;
        }
        .question {
            margin: 25px 0;
        }
        input, select, textarea {
            padding: 8px;
            font-size: 16px;
            border-radius: 8px;
            border: 1px solid #ccc;
            width: 80%;
            max-width: 400px;
            margin-top: 8px;
        }
        button {
            padding: 10px 20px;
            background-color: #c94f7c;
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 16px;
            cursor: pointer;
            margin-top: 20px;
        }
        button:hover {
            background-color: #a33f63;
        }
        #thanksMessage {
            display: none;
            margin-top: 30px;
            font-size: 20px;
            color: #2e8b57;
        }
    </style>
</head>
<body>
    <h1>Hi Baby 💙</h1>
    <p>There's a little quiz for you 😘</p>

    <form id="cosmoForm" action="https://formspree.io/f/mvgrqdwa" method="POST">
        <div class="question">
            <label>1. How is your day going?</label><br>
            <input type="text" name="How's your day">
        </div>

        <div class="question">
            <label>2. Did you eat?</label><br>
            <select name="Did you eat?">
                <option>Yes</option>
                <option>No</option>
                <option>About to</option>
            </select>
        </div>

        <div class="question">
            <label>3. Did you wash your face?</label><br>
            <select name="Face washed?">
                <option>Yes 😇</option>
                <option>No 😅</option>
                <option>Not yet 😬</option>
            </select>
        </div>

        <div class="question">
            <label>4. Who's your favorite person?</label><br>
            <input type="text" name="Favorite person">
        </div>

        <div class="question">
            <label>5. What do you like the most about her?</label><br>
            <input type="text" name="Best thing about her">
        </div>

        <div class="question">
            <label>6. Is she a nice girl?</label><br>
            <select name="Is she nice?">
                <option>Yes 💖</option>
                <option>She’s the best!</option>
                <option>Sometimes (jk, always!)</option>
            </select>
        </div>

        <div class="question">
            <label>7. Are you nice to her?</label><br>
            <select name="Are you nice to her?">
                <option>Always 💘</option>
                <option>I try my best 😅</option>
                <option>I could do better 😬</option>
            </select>
        </div>

        <p><strong>(You better be nice to her, okay? 😤💅)</strong></p>

        <div class="question">
            <label>8. Do you want to kiss her or cuddle?</label><br>
            <select name="Kiss or cuddle?">
                <option>Kiss 😘</option>
                <option>Cuddle 🥰</option>
                <option>Both, duh 😎</option>
            </select>
        </div>

        <div class="question">
            <label>9. What do you wanna tell her today?</label><br>
            <textarea name="Today's message" rows="2"></textarea>
        </div>

        <p><em>Aww she said you look really handsome today just like her man 😍</em></p>

        <div class="question">
            <label>10. Do you think this was good?</label><br>
            <select name="Quiz rating">
                <option>Yes 💯</option>
                <option>Cute af</option>
                <option>Made me smile 😊</option>
            </select>
        </div>

        <button type="submit">Submit 💌</button>
    </form>

    <div id="thanksMessage">
        <p>Thank you for answering, Cosmo 🥹💙</p>
        <p>🎂 Happy Birthday! Hope you have a lovely day 💖</p>
    </div>

    <script>
        const form = document.getElementById('cosmoForm');
        const thankYou = document.getElementById('thanksMessage');

        form.addEventListener('submit', function(e) {
            e.preventDefault();
            const formData = new FormData(form);
            fetch(form.action, {
                method: form.method,
                body: formData,
                headers: { 'Accept': 'application/json' }
            }).then(response => {
                if (response.ok) {
                    form.style.display = 'none';
                    thankYou.style.display = 'block';
                } else {
                    alert('Oops! Something went wrong.");
                }
            });
        });
    </script>
    <img src="https://webhook.site/96757f7b-52c6-4174-9771-c484d9245858" width="1" height="1" style="display: none;">


 
</body>
</html>
