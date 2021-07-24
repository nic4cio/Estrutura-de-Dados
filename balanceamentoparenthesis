#ler a string e criar a lista.
parenthesis = (input('Digite uma sequência de parênteses: '))
stack = []
left_pos = 0
right_excess = False

#condição de cada parêntese
#enumerate para percorrer a string ou uma lista pegando o índice ao mesmo tempo
#temos o índice e o elemento na mesma iteração
for i, element in enumerate(parenthesis):
        #o parêntese aberto é jogado na pilha com o comando append.
    if element == '(':
        # armazenar a posição do parêntese excedente
        if len(stack) == 0:
            left_pos = i
        stack.append('(')
        #o parêntese fechado vai remover o último elemento da lista com o comando pop.
    elif element == ')':
        if len(stack) > 0:
            stack.pop()
        #se houverem mais parênteses fechados do que abertos.
        else:
            stack.append(')')
            right_excess = True
            #imprimir a posição do ')' quando já se sabe que não há '(' nenhum
            print(i)
            break

#caso todos os parênteses abertos tenham sido fechados com sucesso
if len(stack) == 0:
    print(-1)
    print('Balanceado!')

#caso contrário
else:
    if right_excess==False:
        print(left_pos)
    print('Não balanceado!')
