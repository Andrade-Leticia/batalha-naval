import random

######### legenda
# ✅= acertou (acertou a embarcação)
# ❌ = errou (nao tinha embarcação naquele local)
# L = linha
# C = coluna

###################################### MENU DE BOAS VINDAS #########################################################
print("SEJA MUITO BEM-VINDO(A)")

print('''
██████╗░░█████╗░████████╗░█████╗░██╗░░░░░██╗░░██╗░█████╗░  ███╗░░██╗░█████╗░██╗░░░██╗░█████╗░██╗░░░░░
██╔══██╗██╔══██╗╚══██╔══╝██╔══██╗██║░░░░░██║░░██║██╔══██╗  ████╗░██║██╔══██╗██║░░░██║██╔══██╗██║░░░░░
██████╦╝███████║░░░██║░░░███████║██║░░░░░███████║███████║  ██╔██╗██║███████║╚██╗░██╔╝███████║██║░░░░░
██╔══██╗██╔══██║░░░██║░░░██╔══██║██║░░░░░██╔══██║██╔══██║  ██║╚████║██╔══██║░╚████╔╝░██╔══██║██║░░░░░
██████╦╝██║░░██║░░░██║░░░██║░░██║███████╗██║░░██║██║░░██║  ██║░╚███║██║░░██║░░╚██╔╝░░██║░░██║███████╗
╚═════╝░╚═╝░░╚═╝░░░╚═╝░░░╚═╝░░╚═╝╚══════╝╚═╝░░╚═╝╚═╝░░╚═╝  ╚═╝░░╚══╝╚═╝░░╚═╝░░░╚═╝░░░╚═╝░░╚═╝╚══════╝
''')

print('''░░░░░░░░░░░░░░░░░░░░░░░░░░░░░                 
░░░░░░░░░░▄███████▄░░░░░░░░░░
░░░░░░░░░▐██▀░░░▀██▌░░░░░░░░░
░░░░░░░░░▐██░░░░░██▌░░░░░░░░░
░░░░░░░░░▐██▄░░░▄██▌░░░░░░░░░
░░░░░░░░░░▀███████▀░░░░░░░░░░
░░░░░░░░░░░░▐█▄█▌░░░░░░░░░░░░
░░░░░░░░░░▐███▄███▌░░░░░░░░░░
░░░░░░░░░░░░▐█▄█▌░░░░░░░░░░░░
░░░░░░░░░░░░▐█▄█▌░░░░░░░░░░░░
░░░░░░░░░░░░▐█▄█▌░░░░░░░░░░░░
░░░░░░░░░░░░▐█▄█▌░░░░░░░░░░░░
░░░░░░░░░░░░▐█▄█▌░░░░░░░░░░░░
░░░░░░░░░░░░▐█▄█▌░░░░░░░░░░░░
░░▄█▄░░░░░░░▐█▄█▌░░░░░░░▄█▄░░
▄█████▄░░░░░▐█▄█▌░░░░░▄█████▄
░░███░░░░░░░▐█▄█▌░░░░░░░███░░
░░███▄░░░░░▄██▄██▄░░░░░▄███░░
░░▀████▄▄▄████▄████▄▄▄████▀░░
░░░░▀█████████▄█████████▀░░░░
░░░░░░▀███████▄███████▀░░░░░░
░░░░░░░░░▀████▄████▀░░░░░░░░░
░░░░░░░░░░░░▀█▄█▀░░░░░░░░░░░░
░░░░░░░░░░░░░░▀░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
''')

nomeJogador = str(input('Jogador, digite o seu nome: '))

#######################################################################################################

### INICIAR VARIÁVEL DOS PONTOS
pontosJogador = 0
pontosComputador = 0


# jogo acaba quando um dos jogadores afundar a tropa adversária.

##############################################################################################

def mensagem(msg):  ## ESTILIZAR AS MENSAGEN
    print('-' * len(msg))
    print(msg)
    print('-' * len(msg))


#### FUNÇÃO PARA CRIAR TABULEIROS
def criar_tabuleiro(l, c):
    tabuleiro = []
    for i in range(l):
        tabuleiro.append(c * [0])
    return tabuleiro


#### CHAMANDO AS FUNÇÕES DE CRIAR TABULEIRO
tabuleiroJogador = criar_tabuleiro(5, 10)
tabuleiroEscondidoJogador = criar_tabuleiro(5, 10)
tabuleiroComputador = criar_tabuleiro(5, 10)
tabuleiroEscondidoComputador = criar_tabuleiro(5, 10)


##### FUNÇÃO POSIÇÕES JOGADOR
def definir_tabuleiro_jogador(l, c):
    tabuleiroEscondidoJogador[l][c] = 1


##### FUNÇÃO ESCOLHA POSIÇÕES JOGADOR:
def escolher_posicao_jogador(tabuleiroEscondidoJogador):
    i = 0
    while i < 5:
        try: #### CASO O JOGADOR ESCOLHA ALGO QUE NAO SEJAM NÚMEROS VÁLIDOS
            jogL = int(input("Escolha uma linha de 0 a 4: "))
         #### caso escolha uma opção inválida
        except ValueError:
            print('Escolha uma posição válida para linha ou coluna!')
            jogL = int(input("Escolha uma linha de 0 a 4: "))
        try:
            jogC = int(input("Escolha uma coluna de 0 a 9: "))
        except ValueError:  #### caso escolha uma opção inválida
            print('Escolha uma posição válida para linha ou coluna!')
            jogC = int(input("Escolha uma coluna de 0 a 9: "))

        if (jogL > 4) or (jogC > 9):
            print('Escolha uma posição válida para linha ou coluna!')
        elif tabuleiroEscondidoJogador[jogL][jogC] == 1:
            print("Tente novamente: ")
        elif tabuleiroEscondidoJogador[jogL][jogC] == 0:
            definir_tabuleiro_jogador(jogL, jogC)
            i += 1

#### FUNÇÃO ESCOLHA POSIÇÕES RANDOMIZADAS DO COMPUTADOR:
def escolher_posicao_computador(tabuleiroEscondidoComputador):
    i = 0
    while i < 5:
        compC = random.randint(0, 4)
        compL = random.randint(0, 9)
        if tabuleiroEscondidoComputador[compC][compL] == 0:
            tabuleiroEscondidoComputador[compC][compL] = 1
            i += 1


#### FUNÇÃO DE ATAQUE DO JOGADOR:
def mudar_tabuleiro_escondido_computador(ataqueJogadorL, ataqueJogadorC, tabuleiroEscondidoComputador):
    tabuleiroEscondidoComputador[ataqueJogadorL][ataqueJogadorC] = 0


#### ATUALIZAR TABULEIRO COMPUTADOR
def mudar_tabuleiro_computador(ataqueJogadorL, ataqueJogadorC, tabuleiroComputador):
    tabuleiroComputador[ataqueJogadorL][ataqueJogadorC] = "✅" #### EMOJI DE EMBARCAÇÃO AFUNDADA


#### FUNÇÃO DE ATAQUE DO COMPUTADOR:
def mudar_tabuleiro_escondido_jogador(tabuleiroEscondidoJogador, ataqueComputadorL, ataqueComputadorC):
    tabuleiroEscondidoJogador[ataqueComputadorL][ataqueComputadorC] = 0



#### ATUALIZAR TABULEIRO JOGADOR
def mudar_tabuleiro_jogador(tabuleiroJogador, ataqueComputadorL, ataqueComputadorC):
    tabuleiroJogador[ataqueComputadorL][ataqueComputadorC] = "✅"


def printar_tabuleiros_escondidos(tabuleiroEscondidoComputador):
    # print("Tabuleiros Escondidos:")
    # print()
    # print("Tabuleiro do Jogador Escondido:")
    # for i in range(5):
    #    print(tabuleiroEscondidoJogador[i])
    # print()
    print("Tabuleiro Computador Escondido: ")
    for i in range(5):
        print(tabuleiroEscondidoComputador[i])


#### FUNÇÃO PRINTAR TABULEIROS
def printar_tabuleiros(tabuleiroJogador, tabuleiroComputador):
    print()
    print(f"Tabuleiro de {nomeJogador}:")
    for i in range(5):
        print(tabuleiroJogador[i])
    mensagem(f"Embarcações restantes de {nomeJogador}: {5 - pontosComputador}. ")  # ATUALIZAR QUANTIDADE RESTANTE DE EMBARCAÇÕES
    print()
    print("Tabuleiro do Computador:")
    for i in range(5):
        print(tabuleiroComputador[i])
    mensagem(f"Embarcações restantes do computador: {5 - pontosJogador}. ")  # ATUALIZAR QUANTIDADE RESTANTE DE EMBARCAÇÕES
    print()


################################################################ COMEÇO DO JOGO #########################################################################################

#### POSICIONAR FROTAS JOGADOR

mensagem(f"{nomeJogador}, posicione sua frota.")

#### JOGADOR ESCOLHE SUAS POSIÇÕES:
escolher_posicao_jogador(tabuleiroEscondidoJogador)

#### COMPUTADOR ESCOLHE SUAS POSIÇÕES:
escolher_posicao_computador(tabuleiroEscondidoComputador)
printar_tabuleiros(tabuleiroJogador, tabuleiroComputador)
printar_tabuleiros_escondidos(tabuleiroEscondidoComputador)

#### LOOP DE JOGO:
while pontosJogador < 6 and pontosComputador < 6:
    #### ATAQUE JOGADOR:
    mensagem(f"{nomeJogador}, é sua vez de atacar.")
    try:
        ataqueJogadorL = int(input("Escolha sua posição de ataque na linha: (linha de 0 a 4): "))
    except ValueError:
        print("Digite uma posição de ataque válida. Apenas NÚMEROS!!!")
        ataqueJogadorL = int(input("Escolha sua posição de ataque na linha: (linha de 0 a 4): "))

    try:
        ataqueJogadorC = int(input("Escolha sua posição de ataque na coluna: (coluna de 0 a 9): "))
    except ValueError:
        print("Digite uma posição de ataque válida. Apenas NÚMEROS!!!")
        ataqueJogadorC = int(input("Escolha sua posição de ataque na coluna: (coluna de 0 a 9): "))

    if (ataqueJogadorL > 4) or (ataqueJogadorC > 9):
        while (ataqueJogadorL > 4) or (ataqueJogadorC > 9):
            print('Posição para ataque inválida. Ataque novamente: ')
            ataqueJogadorL = int(input("Escolha sua posição de ataque na linha: (linha de 0 a 4): "))
            ataqueJogadorC = int(input("Escolha sua posição de ataque na coluna: (coluna de 0 a 9): "))
    if tabuleiroComputador[ataqueJogadorL][ataqueJogadorC] == ("✅" or "❌"):
        mensagem('Posição para ataque já escolhida. Ataque novamente: ') #### POSIÇÃO JA ATACADA
        #### PEDIR QUE ATAQUE NOVAMENTE POR TER ESCOLHIDO UMA POSIÇÃO JA USADA
        while tabuleiroComputador[ataqueJogadorL][ataqueJogadorC] == ("✅" or "❌"): 
            print('Posição para ataque inválida. Ataque novamente: ')
            ataqueJogadorL = int(input("Escolha sua posição de ataque na linha: (linha de 0 a 4): "))
            ataqueJogadorC = int(input("Escolha sua posição de ataque na coluna: (coluna de 0 a 9): "))
            
    #### ACERTOU UMA EMBARCAÇÃO
    elif tabuleiroEscondidoComputador[ataqueJogadorL][ataqueJogadorC] == 1:
        mudar_tabuleiro_escondido_computador(ataqueJogadorL, ataqueJogadorC, tabuleiroEscondidoComputador)
        mudar_tabuleiro_computador(ataqueJogadorL, ataqueJogadorC, tabuleiroComputador)
        pontosJogador += 1
        mensagem(f"Parabéns, você derrubou uma embarcação adversária!")
        printar_tabuleiros(tabuleiroJogador, tabuleiroComputador)
        # printar_tabuleiros_escondidos(tabuleiroEscondidoComputador)

        #### JOGADOR GANHOU
        if pontosJogador == 5:
            mensagem('A VITÓRIA É SUA, MANDOU MUITO BEM! OBRIGADO POR JOGAR. ')
            mensagem('CRÉDITOS: EROS SANTOS; LAURA DAMBROS; LETICIA VIEIRA.')
            print('''───│─────────────────────────────────────
                    ───│────────▄▄───▄▄───▄▄───▄▄───────│────
                    ───▌────────▒▒───▒▒───▒▒───▒▒───────▌────
                    ───▌──────▄▀█▀█▀█▀█▀█▀█▀█▀█▀█▀▄─────▌────
                    ───▌────▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄───▋────
                    ▀██████████████████████████████████████▄─
                    ──▀███████████████████████████████████▀──
                    ─────▀██████████████████████████████▀────
                    ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
                    ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
                    ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
                    ''')
            break

        #### COMPUTADOR ATACA
        else:
            mensagem("Agora é a vez do computador atacar...")

            #### ATAQUE COMPUTADOR:
            ataqueComputadorL = random.randint(0, 4)
            ataqueComputadorC = random.randint(0, 9)
            #### COMPUTADOR ACERTOU
            if tabuleiroEscondidoJogador[ataqueComputadorL][ataqueComputadorC] == 1:  #### ACERTOU
                mudar_tabuleiro_escondido_jogador(tabuleiroEscondidoJogador, ataqueComputadorL, ataqueComputadorC)
                mudar_tabuleiro_jogador(tabuleiroJogador, ataqueComputadorL, ataqueComputadorC)
                pontosComputador += 1
                mensagem(
                    f"O computador atacou na posição {[ataqueComputadorL]}{[ataqueComputadorC]} e acertou uma de suas embarcações.")
                printar_tabuleiros(tabuleiroJogador, tabuleiroComputador)
            #### COMPUTADOR ERROU
            else:
                tabuleiroJogador[ataqueComputadorL][ataqueComputadorC] = '❌'  #### ERROU
                mudar_tabuleiro_escondido_jogador(tabuleiroEscondidoJogador, ataqueComputadorL, ataqueComputadorC)
                mudar_tabuleiro_jogador(tabuleiroJogador, ataqueComputadorL, ataqueComputadorC)
                mensagem(
                    f"O computador atacou na posição {[ataqueComputadorL]}{[ataqueComputadorC]} e errou. Você escapou por pouco!!")
                printar_tabuleiros(tabuleiroJogador, tabuleiroComputador)
    #### NÃO ACERTOU A EMBARCAÇÃO
    else:
        tabuleiroComputador[ataqueJogadorL][ataqueJogadorC] = '❌'
        mensagem(f"Mirou mal... Nenhuma embarcação adversária foi afundada!")
        printar_tabuleiros(tabuleiroJogador, tabuleiroComputador)
        #### RETORNA O LOOP DO COMPUTADOR
        mensagem("Agora é a vez do computador atacar...")

        # COMPUTADOR ATACA
        ataqueComputadorL = random.randint(0, 4)
        ataqueComputadorC = random.randint(0, 9)

        #### COMPUTADOR ACERTA UMA EMBARCAÇÃO
        if tabuleiroEscondidoJogador[ataqueComputadorL][ataqueComputadorC] == 1:
            mudar_tabuleiro_escondido_jogador(tabuleiroEscondidoJogador, ataqueComputadorL, ataqueComputadorC,)
            mudar_tabuleiro_jogador(tabuleiroJogador, ataqueComputadorL, ataqueComputadorC)
            pontosComputador += 1
            mensagem(
                f"O computador atacou na posição {[ataqueComputadorL]}{[ataqueComputadorC]} e acertou uma de suas embarcações.")  #### ACERTOU
            printar_tabuleiros(tabuleiroJogador, tabuleiroComputador)
            #### COMPUTADOR VENCE
            if pontosComputador == 5:
                mensagem('O COMPUTADOR VENCEU... BOA SORTE NA PRÓXIMA, OBRIGADO POR JOGAR.')
                mensagem('CRÉDITOS: EROS SANTOS; LAURA DAMBROS; LETICIA VIEIRA.')
                print('''───│─────────────────────────────────────
                        ───│────────▄▄───▄▄───▄▄───▄▄───────│────
                        ───▌────────▒▒───▒▒───▒▒───▒▒───────▌────
                        ───▌──────▄▀█▀█▀█▀█▀█▀█▀█▀█▀█▀▄─────▌────
                        ───▌────▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄───▋────
                        ▀██████████████████████████████████████▄─
                        ──▀███████████████████████████████████▀──
                        ─────▀██████████████████████████████▀────
                        ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
                        ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
                        ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
                    ''')                            
                break
        #### COMPUTADOR ERRA A EMBARCAÇÃO
        else:
            tabuleiroJogador[ataqueComputadorL][ataqueComputadorC] = '❌'
            mensagem(
                f"O computador atacou na posição {[ataqueComputadorL]}{[ataqueComputadorC]} e errou. Você escapou por pouco!!")  #### ERROU
            printar_tabuleiros(tabuleiroJogador, tabuleiroComputador)
            # mensagem(f'Restam {5 - pontosComputador} embarcações.')
