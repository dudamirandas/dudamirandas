function jogoAdivinhacao() {
    // Escolher um número randômico entre 0 e 10
    const numeroSecreto = Math.floor(Math.random() * 11);
  
    // Número de tentativas
    let tentativas = 2;
  
    while (tentativas > 0) {
      // Perguntar ao usuário pelo palpite
      const palpite = parseInt(prompt("Chute um número de 0 a 10:"));
  
      // Verificar se o palpite está correto
      if (palpite === numeroSecreto) {
        alert("Parabéns! Você acertou!");
        break;
      } else {
        tentativas -= 1;
        alert(`Incorreto. Você tem mais ${tentativas} ${tentativas === 1 ? 'tentativa' : 'tentativas'}.`);
      }
    }
  
    if (tentativas === 0) {
      alert(`Fim do jogo! O número correto era ${numeroSecreto}.`);
    }
  }
  
  // Chamar a função para iniciar o jogo
  jogoAdivinhacao();

  

