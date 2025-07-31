peso = float(input('Digite o peso da carga: '))
entregas = int(input('Digite quantas entregas são: '))
frete2 = int(input('Digite o valor de frete correto: '))
frete1 = int(input('Digite o frete que apareceu: '))

soma2 = (entregas-3)*18
soma1 = frete2-frete1


#BATE O PESO E TEM MAIS DE 3 ENTREGAS 
if peso >= 3200 and peso <= 4500:
    
    if entregas >= 4 :
     print(f'O valor do frete esta com : R$ -{soma1}')
     print(f'O peso de {peso:.3f} esta na faixa Do Adicional de R$44')
     print(f'De Acordo com a QTND de ENTREGAS O VALOR DE ADICIONAL DE ENTREGA SERA DE : R${soma2}')
     resultado_soma1 = soma1+soma2+44
     print(f'o valor de acrescimo correto sera de: R${resultado_soma1}')
     
    elif entregas <= 3:
       print(f'O valor do frete esta com : R$ -{soma1}')
       print(f'O peso de {peso:.3f} esta na faixa Do Adicional de R$44')
       print('O Valor nao tem adicional de frete')
       resultado_soma3 = soma1+44
       print(f'O Valor de Acrescimo sera de {resultado_soma3}')


#BATE AS ENTREGAS MAIS NAO TEM O PESO ADICIONAL
elif peso < 3200 or peso > 4500:
    
    if entregas >= 4:
        print(f'O valor do frete esta com : R$ -{soma1}')
        print(f'O peso de {peso:.3f}, Não esta na faixa Do Adicional de R$44')
        print(f'De Acordo com a QTND de ENTREGAS O VALOR DE ADICIONAL DE ENTREGA SERA DE : R${soma2}')
        resultado_soma2 = soma1+soma2
        print(f'o valor de acrescimo correto sera de: R${resultado_soma2}')

#NAO TEM NENHUM ADICIONAL 

    elif entregas < 4:
       print(f'O valor do frete esta com : R$ -{soma1}')
       print(f'O peso de {peso:.3f}, Não esta na faixa Do Adicional de R$44')
       print('Nao tem adicional de entregas')
       print(f'o valor de acrescimo correto sera de: R${soma2}')


else : 
   print('ALGO ESTA ERRADO')
