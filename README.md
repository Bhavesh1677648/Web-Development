<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-width=1.0">
    <title>Do You Love Me?</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        text-align: center;
      }
      
      #buttons {
        margin-top: 20px;
      }
      
      #yes-btn, #no-btn {
        width: 100px;
        height: 30px;
        font-size: 16px;
        cursor: pointer;
      }
      
      #result {
        margin-top: 50px;
      }
      
      #mandap {
        width: 200px;
        height: 200px;
        border: 1px solid black;
        margin: auto;
        position: relative;
      }
      
      #mandap-image {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
      
      #mandap-text {
        font-size: 24px;
        font-weight: bold;
        margin-top: 20px;
      }
    </style>
  </head>
  <body>
    <h1 id="question">Do You Love Me?</h1>
    <div id="buttons">
      <button id="yes-btn">Yes</button>
      <button id="no-btn">No</button>
    </div>
    <div id="result" style="display: none;"></div>
    <script>
      let count = 0;
      
      document.getElementById('yes-btn').addEventListener('click', () => {
        document.getElementById('question').style.display = 'none';
        document.getElementById('buttons').style.display = 'none';
        document.getElementById('result').style.display = 'block';
        document.getElementById('result').innerHTML = `
          <div id="mandap">
            <img id="mandap-image" src="./luxurydecor.jpg" alt="Luxury Decor">
          </div>
          <p id="mandap-text">I Love You too! Come on, let's get married!</p>
        `;
      });
      
      document.getElementById('no-btn').addEventListener('click', () => {
        count++;
        if (count < 11) {
          document.getElementById('question').innerText = 'Ek baar fir se soch lo! Mere jaisa chirag leke dhoondne pe bhi nahi milega!';
          setTimeout(() => {
            document.getElementById('question').innerText = 'Do You Love Me?';
          }, 2000);
        } else {
          document.getElementById('question').style.display = 'none';
          document.getElementById('buttons').style.display = 'none';
          document.getElementById('result').style.display = 'block';
          document.getElementById('result').innerHTML = `
            <div id="mandap">
              <img id="mandap-image" src="./luxurydecor.jpg" alt="Luxury Decor">
            </div>
            <p id="mandap-text">I love you! You have to marry me! I don't care if you love me or not!</p>
          `;
        }
      });
    </script>
  </body>
</html>
