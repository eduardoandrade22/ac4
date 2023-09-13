# ac4
ac4
#parcelas,juros,divida
def calculo_juros(valor_divida, parcelas):
    if parcelas ==1:
        return 0
    elif parcelas ==3:
        return valor_divida * 0.10
    elif parcelas  == 6:
        return valor_divida * 0.15
    elif parcelas == 9:
        return valor_divida * 0.20
    elif parcelas == 12:
        return valor_divida * 0.25
    else:
     return None

def calcular_divida_inteira(valor_divida, parcelas):
    juros = calculo_juros(valor_divida, parcelas)
    if juros is not None:
        return valor_divida + juros
    else:
        return None

def imprimir_opções(valor_divida):
    print("Número de parcelas % de Juros valor inteiro     valor da parcela")
    for parcelas in (1, 3, 6, 9, 12):
        juros = calculo_juros(valor_divida, parcelas)
        divida_inteira = calcular_divida_inteira(valor_divida, parcelas)
        if juros is not None and divida_inteira is not None:
            valor_parcela = divida_inteira / parcelas
            print(f"{parcelas:<22} {juros:<13} R$ {divida_inteira:<13} {parcelas:<18} R$ {valor_parcela: .2f}")

valor_divida =float(input("insira o valor da divída:"))
imprimir_opções(valor_divida)




#

intervalo_0_25 = 0
intervalo_26_50 = 0
intervalo_51_75 = 0
intervalo_76_100 = 0

while True:
    numero = float(input("Insira um número positivo (ou um número negativo para encerrar): "))

    if numero < 0:
        break

    if 0 <= numero <= 25:
        intervalo_0_25 += 1
    elif 26 <= numero <= 50:
        intervalo_26_50 += 1
    elif 51 <= numero <= 75:
        intervalo_51_75 += 1
    elif 76 <= numero <= 100:
        intervalo_76_100 += 1


print("Quantidade de números no intervalo [0-25]:", intervalo_0_25)
print("Quantidade de números no intervalo [26-50]:", intervalo_26_50)
print("Quantidade de números no intervalo [51-75]:", intervalo_51_75)
print("Quantidade de números no intervalo [76-100]:", intervalo_76_100)







#questão números primos


def e_primo(num):
    for div in range(2, num):
        if num % div == 0:
            print("0 número não é primo")
            break
    else:
        print("O número é primo")

e_primo(7)
e_primo(16)
