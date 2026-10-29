def lexico(codigo):
    codigo = codigo + " "
    n = len(codigo)
    i = 0
    tokens = []
    estado = 0

    while i < n:
        c = codigo[i]

        if estado == 0:
            if c.isdigit():
                i += 1
                estado = 3
                continue
            elif c.isalpha():
                i += 1
                estado = 4
                continue
            elif c.isspace():
                i += 1
                continue
            else:
                return "ERROR LEXICO"

        elif estado == 3:
            if c.isdigit():
                i += 1
                continue
            elif c == '.':
                i += 1
                estado = 5
                continue
            else:
                tokens.append(3000)
                estado = 0
                continue

        elif estado == 4:
            if c.isalpha() or c.isdigit():
                i += 1
                continue
            else:
                tokens.append(1000)
                estado = 0
                continue

        elif estado == 5:
            if c.isdigit():
                i += 1
                estado = 6
                continue
            else:
                return "ERROR: se esperaba un numero"

        elif estado == 6:
            if c.isdigit():
                i += 1
                continue
            else:
                tokens.append(2000)
                estado = 0
                continue

    return tokens


codigo = '''
    abc
    0
    1.4
    
'''
