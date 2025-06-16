<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kalkulator Lanjutan</title>
  <style>
    body {
      background:#FFFF;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    /DI ATAS CODINGAN UNTUK MERUBAH BACKGROUND DASAR/

    .calculator {
      background: #FF7F00; 
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 0 100px rgba(0,0,0,0.3);
      width: 250px;
    }
/WARNA ORANGE CONTOHNYA/
    /DI ATAS UNTUK MERUBAH TAMPILAN TABEL CALCULATOR/

    #display {
        
      width: 100%;
      height: 50px;
      color:#FFFF00;
      font-size: 24px;
      margin-bottom: 15px;
      padding: 10px;
      border: none;
      border-radius: 5px;
      text-align: right;
    }
/CONTOH WARNA HURUF DISPLAY KUNING/
    /DI ATAS UNTUK MERUBAH TAMPILAN ANGKA DAH DISPLAY CALCULATOR/

    .buttons {
      display: GRID;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;

    }

    button {
      padding: 15px;
      font-size: 18px;
      background: #444;
      color: #00FF00;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
   /* CONTOH WARNA HIJAU
    CODINGAN DI ATAS UNTUK MENGUBAH WARNA DAN UKURAN TOMBOL */

    button:hover {
      background: #BF00FF;
    }
/CONTOH WARNA UNGU/
    /CODINGAN DI ATAS UNTUK WARNA KETIKA COURSE DI ARAHKAN KE TOMBOL/

    .zero {
      grid-column: span 2;
    }

    /CODINGNA DI ATAS UNTUK JARAK SPASI ANTAR ANGKA/
  </style>
</head>

<!-- CODINGNA DI ATAS DIGUNAKAN UNTUK UNTUK MERUBAH TAMPILAN CALCULATOR -->




<body>

<div class="calculator">
  <input type="text" id="display" disabled>
  <div class="buttons">
    <button onclick="clearDisplay()">C</button>  
    <button onclick="deleteLast()">←</button>
    <button onclick="appendValue('/')">/</button>
    <button onclick="appendValue('')"></button>

    <button onclick="appendValue('7')">7</button>
    <button onclick="appendValue('8')">8</button>
    <button onclick="appendValue('9')">9</button>
    <button onclick="appendValue('-')">-</button>

    <button onclick="appendValue('4')">4</button>
    <button onclick="appendValue('5')">5</button>
    <button onclick="appendValue('6')">6</button>
    <button onclick="appendValue('+')">+</button>

    <button onclick="appendValue('1')">1</button>
    <button onclick="appendValue('2')">2</button>
    <button onclick="appendValue('3')">3</button>
    <button onclick="calculate()">=</button>

    <button class="zero" onclick="appendValue('0')">0</button>
    <button onclick="appendValue('.')">.</button>
  </div>
</div>

<script>
  let display = document.getElementById('display');
  let hasCalculated = false;

  function appendValue(val) {
    if (hasCalculated && !isOperator(val)) {
      display.value = val; // Mulai dari awal jika input angka setelah "="
} 



else if (hasCalculated && isOperator(val)) {
      display.value += val; // Lanjutkan perhitungan jika input calculator setelah "="
    }


     else {
      display.value += val;
    }
    hasCalculated = false;
  }

  function isOperator(char) {
    return ['+', '-', '*', '/'].includes(char);
  }

  // CODINGAN DI ATAS UNTUK PENGOPRASIAN BOTTON ( TAMBAH KURANG BAGI KAI)

  function clearDisplay() {
    display.value = '';
    hasCalculated = false;
  }

  function deleteLast() {
    display.value = display.value.slice(0, -1);
  }

  function calculate() {
    try {
      display.value = eval(display.value);
      hasCalculated = true;
    } catch {
      display.value = 'Error';
      hasCalculated = true;
    }
  }
</script>

</body>
</html>
