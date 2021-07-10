#### Programa que funciona como o jogo "pedra, papel, tesoura",
#### onde um usuário joga contra o computador.
#### A escolha do usuário é fornecida através do comando input(),
#### enquanto que a do computador é escolhida aleatoriamente.
#### O programa deve perguntar se o usuário quer jogar novamente.

import random
opcoes = ['pedra', 'papel', 'tesoura']

resposta = True
while resposta:
    jogada_computador = random.choice(opcoes)
    jogada_usuario = input(
        "Selecione a opção para jogar:\nOpções\npedra\npapel\ntesoura\n-> ")

    if jogada_usuario == "pedra":
        if jogada_usuario == jogada_computador:
            print("Empate!!!")
        elif jogada_usuario != jogada_computador and jogada_computador == 'tesoura':
            print("Usuário Ganhou!!!")
        else:
            print("Computador Ganhou!!!")

    if jogada_usuario == "papel":
        if jogada_usuario == jogada_computador:
            print("Empate!!!")
        elif jogada_usuario != jogada_computador and jogada_computador == 'pedra':
            print("Usuário Ganhou!!!")
        else:
            print("Computador Ganhou!!!")

    if jogada_usuario == "tesoura":
        if jogada_usuario == jogada_computador:
            print("Empate!!!")
        elif jogada_usuario != jogada_computador and jogada_computador == 'papel':
            print("Usuário Ganhou!!!")
        else:
            print("Computador Ganhou!!!")

    resposta = input("Você quer jogar novamente (S/N): ")
    if resposta == "N":
        resposta = False
