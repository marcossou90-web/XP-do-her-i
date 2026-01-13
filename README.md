// === Projeto Interativo: Classificador de Nível de Herói ===

// Se estiver usando Node.js, instale o pacote "prompt-sync":
// npm install prompt-sync
// e descomente a linha abaixo
// const prompt = require('prompt-sync')();

// Função para classificar o nível do herói
function classificarHeroi(nomeHeroi, xpHeroi) {
    let nivel = "";

    if (xpHeroi < 1000) {
        nivel = "Ferro";
    } else if (xpHeroi >= 1001 && xpHeroi <= 2000) {
        nivel = "Bronze";
    } else if (xpHeroi >= 2001 && xpHeroi <= 5000) {
        nivel = "Prata";
    } else if (xpHeroi >= 5001 && xpHeroi <= 7000) {
        nivel = "Ouro";
    } else if (xpHeroi >= 7001 && xpHeroi <= 8000) {
        nivel = "Platina";
    } else if (xpHeroi >= 8001 && xpHeroi <= 9000) {
        nivel = "Ascendente";
    } else if (xpHeroi >= 9001 && xpHeroi <= 10000) {
        nivel = "Imortal";
    } else {
        nivel = "Radiante";
    }

    console.log(`O Herói de nome ${nomeHeroi} está no nível de ${nivel}`);
}

// --- Entrada do usuário ---
let continuar = true;

while (continuar) {
    let nomeHeroi = prompt("Digite o nome do herói: ");
    let xpHeroi = parseInt(prompt("Digite a XP do herói: "));

    classificarHeroi(nomeHeroi, xpHeroi);

    // Pergunta se deseja classificar outro herói
    let resposta = prompt("Deseja classificar outro herói? (s/n): ").toLowerCase();
    if (resposta !== 's') {
        continuar = false;
        console.log("Programa encerrado. Até mais!");
    }
}
