<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Quiz 03:Continuity and Differentiability(by AnoopSV)</title>
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
  <style>
    body { font-family: Arial, sans-serif; margin: 20px; }
    .question { margin-bottom: 20px; }
    button { padding: 10px; background: #007BFF; color: white; border: none; cursor: pointer; border-radius: 5px; }
    button:hover { background: #0056b3; }
    #result { margin-top: 20px; font-weight: bold; }
    .correct { color: green; }
    .incorrect { color: red; }
    .explanation { font-style: italic; color: #444; }
  </style>
</head>
<body>
  <h2>Quiz: Differentiability and Geometry of Functions of One Variable</h2>
  <form id="quizForm">

    <div class="question">
      <p>1. If \(f(a) < 0 < f(b)\) and \(f\) is continuous on \([a,b]\), then:</p>
      <label><input type="radio" name="q1" value="a"> \(f\) has at least one zero in \((a,b)\)</label><br>
      <label><input type="radio" name="q1" value="b"> \(f\) has infinitely many zeros in \((a,b)\)</label><br>
      <label><input type="radio" name="q1" value="c"> \(f\) is differentiable in \((a,b)\)</label><br>
      <label><input type="radio" name="q1" value="d"> Nothing can be said</label>
    </div>

    <div class="question">
      <p>2. The left-hand derivative of \(f(x)=|x|\) at \(x=0\) is:</p>
      <label><input type="radio" name="q2" value="a"> 1</label><br>
      <label><input type="radio" name="q2" value="b"> -1</label><br>
      <label><input type="radio" name="q2" value="c"> 0</label><br>
      <label><input type="radio" name="q2" value="d"> Does not exist</label>
    </div>

    <div class="question">
      <p>3. If \(f\) is differentiable at \(c\), then:</p>
      <label><input type="radio" name="q3" value="a"> \(f\) must be continuous at \(c\)</label><br>
      <label><input type="radio" name="q3" value="b"> \(f\) may be discontinuous at \(c\)</label><br>
      <label><input type="radio" name="q3" value="c"> Nothing can be said</label><br>
      <label><input type="radio" name="q3" value="d"> \(f\) is bounded near \(c\)</label>
    </div>

    <div class="question">
      <p>4. For \(f(x) = \sin x\) on \([0,\pi]\), the sup and inf are:</p>
      <label><input type="radio" name="q4" value="a"> sup = 1, inf = 0</label><br>
      <label><input type="radio" name="q4" value="b"> sup = \(\pi\), inf = 0</label><br>
      <label><input type="radio" name="q4" value="c"> sup = 0, inf = -1</label><br>
      <label><input type="radio" name="q4" value="d"> sup = 1, inf = -1</label>
    </div>

    <div class="question">
      <p>5. For \(f(x)=x^2-4x+3\) on \([0,3]\):</p>
      <label><input type="radio" name="q5" value="a"> Minimum at \(x=2\)</label><br>
      <label><input type="radio" name="q5" value="b"> Maximum at \(x=2\)</label><br>
      <label><input type="radio" name="q5" value="c"> Minimum at \(x=3\)</label><br>
      <label><input type="radio" name="q5" value="d"> Maximum at \(x=0\)</label>
    </div>

    <div class="question">
      <p>6. If \(f(x) = x^3\), then \(f'(0) = ?\)</p>
      <label><input type="radio" name="q6" value="a"> 0</label><br>
      <label><input type="radio" name="q6" value="b"> 1</label><br>
      <label><input type="radio" name="q6" value="c"> Does not exist</label><br>
      <label><input type="radio" name="q6" value="d"> 3</label>
    </div>

    <div class="question">
      <p>7. The function \(f(x)=|x|\) is:</p>
      <label><input type="radio" name="q7" value="a"> Differentiable at 0</label><br>
      <label><input type="radio" name="q7" value="b"> Continuous but not differentiable at 0</label><br>
      <label><input type="radio" name="q7" value="c"> Discontinuous at 0</label><br>
      <label><input type="radio" name="q7" value="d"> Not defined at 0</label>
    </div>

    <div class="question">
      <p>8. The slope of the tangent to \(y=x^2\) at \(x=1\) is:</p>
      <label><input type="radio" name="q8" value="a"> 1</label><br>
      <label><input type="radio" name="q8" value="b"> 2</label><br>
      <label><input type="radio" name="q8" value="c"> 0</label><br>
      <label><input type="radio" name="q8" value="d"> Does not exist</label>
    </div>

    <div class="question">
      <p>9. The slope of the normal to \(y=x^2\) at \(x=1\) is:</p>
      <label><input type="radio" name="q9" value="a"> -1/2</label><br>
      <label><input type="radio" name="q9" value="b"> -2</label><br>
      <label><input type="radio" name="q9" value="c"> 1/2</label><br>
      <label><input type="radio" name="q9" value="d"> 2</label>
    </div>

    <div class="question">
      <p>10. If \(f(x)=\sin(2x)\), then by the chain rule \(f'(x) = ?\)</p>
      <label><input type="radio" name="q10" value="a"> \(\cos(2x)\)</label><br>
      <label><input type="radio" name="q10" value="b"> \(2\cos(2x)\)</label><br>
      <label><input type="radio" name="q10" value="c"> \(2\sin(2x)\)</label><br>
      <label><input type="radio" name="q10" value="d"> \(-\sin(2x)\)</label>
    </div>

    <button type="button" onclick="checkAnswers()">Submit</button>
  </form>

  <div id="result"></div>

  <script>
    const correctAnswers = {
      q1: {ans: "a", exp: "By Bolzano’s theorem, a continuous function with opposite signs at endpoints has a zero inside."},
      q2: {ans: "b", exp: "Left-hand derivative of |x| at 0 is -1."},
      q3: {ans: "a", exp: "Differentiability implies continuity at that point."},
      q4: {ans: "a", exp: "On [0,π], sin x ranges from 0 to 1."},
      q5: {ans: "a", exp: "The parabola has a minimum at x=2 within [0,3]."},
      q6: {ans: "a", exp: "Derivative of x³ at 0 is 0."},
      q7: {ans: "b", exp: "|x| is continuous everywhere but not differentiable at 0."},
      q8: {ans: "b", exp: "Derivative of x² at x=1 is 2."},
      q9: {ans: "a", exp: "Normal slope = -1/(tangent slope) = -1/2."},
      q10: {ans: "b", exp: "Chain rule: derivative of sin(2x) = cos(2x)·2 = 2cos(2x)."}
    };

    function checkAnswers() {
      let score = 0;
      let resultHTML = "<h3>Results:</h3>";

      for (let q in correctAnswers) {
        let userAnswer = document.querySelector(`input[name="${q}"]:checked`);
        if (userAnswer) {
          if (userAnswer.value === correctAnswers[q].ans) {
            score++;
            resultHTML += `<p>Question ${q.substring(1)}: <span class="correct">Correct</span> — ${correctAnswers[q].exp}</p>`;
          } else {
            resultHTML += `<p>Question ${q.substring(1)}: <span class="incorrect">Incorrect</span>. Correct answer: <b>${correctAnswers[q].ans.toUpperCase()}</b>. ${correctAnswers[q].exp}</p>`;
          }
        } else {
          resultHTML += `<p>Question ${q.substring(1)}: <span class="incorrect">Not answered</span>. Correct answer: <b>${correctAnswers[q].ans.toUpperCase()}</b>. ${correctAnswers[q].exp}</p>`;
        }
      }

      resultHTML += `<p><strong>Total Score: ${score} / ${Object.keys(correctAnswers).length}</strong></p>`;
      document.getElementById("result").innerHTML = resultHTML;
    }
  </script>
</body>
</html>
