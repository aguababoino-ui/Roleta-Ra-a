<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Roleta de Raças</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>
    body {
        background: #111;
        color: #fff;
        font-family: Arial, sans-serif;
        text-align: center;
        padding: 20px;
    }

    h1 {
        font-size: 32px;
        margin-bottom: 20px;
    }

    .container {
        position: relative;
        width: 300px;
        margin: auto;
    }

    /* BASE DE MADEIRA */
    .base {
        width: 300px;
        height: 300px;
        background: #6b3e16;
        border-radius: 12px;
        padding-top: 120px;
        box-shadow: 0 0 25px #000;
    }

    /* ROLETA */
    canvas {
        border-radius: 50%;
        background: #000;
        box-shadow: 0 0 40px #000 inset, 0 0 20px #000;
    }

    /* PONTEIRO */
    .pointer {
        width: 0;
        height: 0;
        border-left: 30px solid white;
        border-top: 15px solid transparent;
        border-bottom: 15px solid transparent;
        position: absolute;
        right: -45px;
        top: 46%;
        z-index: 10;
    }

    /* BOTÃO */
    button {
        background: #ff3c00;
        border: none;
        padding: 15px 30px;
        border-radius: 12px;
        font-size: 20px;
        margin-top: 25px;
        cursor: pointer;
        color: white;
        font-weight: bold;
        box-shadow: 0 0 20px #000;
    }

    button:hover {
        background: #ff5722;
    }

    #resultado {
        margin-top: 20px;
        font-size: 22px;
    }
</style>
</head>
<body>

<h1>🎡 Roleta de Raças</h1>

<div class="container">
    <div class="base">
        <canvas id="wheel" width="300" height="300"></canvas>
    </div>
    <div class="pointer"></div>
</div>

<button onclick="girar()">Girar Roleta</button>

<p id="resultado"></p>

<!-- SONS -->
<audio id="tick-sound" src="https://www.soundjay.com/buttons/sounds/button-09.mp3"></audio>
<audio id="win-sound" src="https://www.soundjay.com/misc/sounds/bell-ringing-05.mp3"></audio>

<script>
const racas = [
    { nome: "Humano", chance: 40, cor: "#e6c68a" },
    { nome: "Elfo", chance: 25, cor: "#00ff44" },
    { nome: "Anão", chance: 20, cor: "#8b4513" },
    { nome: "Bruxa", chance: 10, cor: "#7a00ff" },
    { nome: "Demônio", chance: 5, cor: "#ff3300" }
];

const canvas = document.getElementById("wheel");
const ctx = canvas.getContext("2d");

let anguloFinal = 0;
let girando = false;

/* DESENHAR ROLETA */
function desenharRoleta() {
    const total = 100;
    let anguloInicio = 0;

    racas.forEach(r => {
        let angulo = (r.chance / total) * 2 * Math.PI;

        ctx.beginPath();
        ctx.moveTo(150, 150);
        ctx.arc(150, 150, 150, anguloInicio, anguloInicio + angulo);
        ctx.fillStyle = r.cor;
        ctx.fill();

        ctx.save();
        ctx.translate(150, 150);
        ctx.rotate(anguloInicio + angulo / 2);
        ctx.fillStyle = "#fff";
        ctx.font = "bold 20px Arial";
        ctx.textAlign = "center";
        ctx.fillText(r.nome, 80, 10);
        ctx.restore();

        anguloInicio += angulo;
    });
}

desenharRoleta();

/* EFEITO DE TICK NOS PINOS */
function tocarTickDuranteGiro(duracao) {
    let ticks = 50;
    let intervalo = duracao / ticks;
    let tick = document.getElementById("tick-sound");

    let count = 0;
    let loop = setInterval(() => {
        tick.currentTime = 0;
        tick.play();
        count++;

        if (count >= ticks) clearInterval(loop);
    }, intervalo);
}

function girar() {
    if (girando) return;
    girando = true;

    let extra = Math.random() * 360;
    let rotacao = 360 * 8 + extra;
    anguloFinal = rotacao % 360;

    canvas.style.transition = "transform 4s ease-out";
    canvas.style.transform = `rotate(${rotacao}deg)`;

    tocarTickDuranteGiro(4000);

    setTimeout(() => {
        canvas.style.transition = "none";
        canvas.style.transform = `rotate(${anguloFinal}deg)`;
        identificar(anguloFinal);

        girando = false;

    }, 4050);
}

/* IDENTIFICAR SETOR */
function identificar(angulo) {
    let corrigido = (angulo + 90) % 360;
    let total = 100;
    let pos = (corrigido / 360) * total;

    let acum = 0;
    for (const r of racas) {
        acum += r.chance;
        if (pos <= acum) {
            document.getElementById("resultado").innerHTML =
                `🎉 Você tirou: <b>${r.nome}</b>`;
            document.getElementById("win-sound").play();
            break;
        }
    }
}
</script>
</body>
</html>
