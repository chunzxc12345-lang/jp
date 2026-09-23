[index.html](https://github.com/user-attachments/files/32553494/index.html)
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>히라가나 가타카나 퀴즈</title>
<style>
body{font-family:Arial,sans-serif;text-align:center;background:#f5f5f5;padding:40px 15px}
.game{background:white;max-width:420px;margin:auto;padding:30px;border-radius:18px;box-shadow:0 4px 15px #0002}
#character{font-size:90px;margin:25px}
input{font-size:24px;width:160px;padding:10px;text-align:center}
button{font-size:17px;padding:10px 18px;margin:10px 4px;cursor:pointer}
#result{font-size:20px;font-weight:bold;height:30px;margin:15px}
#score{margin-top:20px}
</style>
</head>
<body>
<div class="game">
<h1>🇯🇵 일본어 문자 퀴즈</h1>
<p>문자를 보고 로마자로 입력하세요!</p>
<div id="character">あ</div>
<input id="answer" type="text" placeholder="예: a" autocomplete="off">
<br>
<button onclick="checkAnswer()">정답 확인</button>
<button onclick="showAnswer()">정답 보기</button>
<button onclick="nextQuestion()">다음 문제</button>
<div id="result"></div>
<div id="score">점수: <span id="scoreNumber">0</span></div>
</div>

<script>
const quiz=[
["あ","a"],["い","i"],["う","u"],["え","e"],["お","o"],
["か","ka"],["き","ki"],["く","ku"],["け","ke"],["こ","ko"],
["さ","sa"],["し","shi"],["す","su"],["せ","se"],["そ","so"],
["た","ta"],["ち","chi"],["つ","tsu"],["て","te"],["と","to"],
["な","na"],["に","ni"],["ぬ","nu"],["ね","ne"],["の","no"],
["は","ha"],["ひ","hi"],["ふ","fu"],["へ","he"],["ほ","ho"],
["ま","ma"],["み","mi"],["む","mu"],["め","me"],["も","mo"],
["や","ya"],["ゆ","yu"],["よ","yo"],["ら","ra"],["り","ri"],
["る","ru"],["れ","re"],["ろ","ro"],["わ","wa"],["を","wo"],["ん","n"],
["ア","a"],["イ","i"],["ウ","u"],["エ","e"],["オ","o"],
["カ","ka"],["キ","ki"],["ク","ku"],["ケ","ke"],["コ","ko"],
["サ","sa"],["シ","shi"],["ス","su"],["セ","se"],["ソ","so"],
["タ","ta"],["チ","chi"],["ツ","tsu"],["テ","te"],["ト","to"],
["ナ","na"],["ニ","ni"],["ヌ","nu"],["ネ","ne"],["ノ","no"],
["ハ","ha"],["ヒ","hi"],["フ","fu"],["ヘ","he"],["ホ","ho"],
["マ","ma"],["ミ","mi"],["ム","mu"],["メ","me"],["モ","mo"],
["ヤ","ya"],["ユ","yu"],["ヨ","yo"],["ラ","ra"],["リ","ri"],
["ル","ru"],["レ","re"],["ロ","ro"],["ワ","wa"],["ヲ","wo"],["ン","n"]
];

let current, score=0, answered=false;

function nextQuestion(){
  current=quiz[Math.floor(Math.random()*quiz.length)];
  document.getElementById("character").textContent=current[0];
  document.getElementById("answer").value="";
  document.getElementById("result").textContent="";
  answered=false;
  document.getElementById("answer").focus();
}

function checkAnswer(){
  if(answered)return;
  const input=document.getElementById("answer").value.trim().toLowerCase();
  if(input===current[1]){
    document.getElementById("result").textContent="⭕ 정답입니다!";
    score++;
    document.getElementById("scoreNumber").textContent=score;
    answered=true;
  }else{
    document.getElementById("result").textContent="❌ 오답입니다! 다시 시도하거나 '정답 보기'를 눌러보세요.";
  }
}

function showAnswer(){
  document.getElementById("result").textContent="💡 정답: " + current[1];
  answered=true;
}

document.getElementById("answer").addEventListener("keydown",e=>{
  if(e.key==="Enter")checkAnswer();
});
nextQuestion();
</script>
</body>
</html>
