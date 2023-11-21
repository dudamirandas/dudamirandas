import random

def jogo_adivinhacao():
    # Escolher um número randômico entre 0 e 10
    numero_secreto = random.randint(0, 10)
    
    # Número de tentativas
    tentativas = 3

    while tentativas > 0:
        # Perguntar ao usuário pelo palpite
        palpite = int(input("Chute um número de 0 a 10: "))

        # Verificar se o palpite está correto
        if palpite == numero_secreto:
            print("Parabéns! Você acertou!")
            break
        else:
            tentativas -= 1
            print(f"Incorreto. Você tem mais {tentativas} {'tentativa' if tentativas == 1 else 'tentativas'}.")

    if tentativas == 0:
        print(f"Fim do jogo! O número correto era {numero_secreto}.")

# Chamar a função para iniciar o jogo
jogo_adivinhacao()

