

# 10) Inserción (Insertion Sort) con traza (Avanzado)
a_ins = [9, 7, 8, 3]
print("10) Insertion Sort con traza: a =", a_ins)

for i in range(1, len(a_ins)):
    valor_actual = a_ins[i]
    j = i - 1
    desplazamientos = 0
    print(f"\ni = {i}, valor actual = {valor_actual}")
   
    while j >= 0 and a_ins[j] > valor_actual:
        a_ins[j+1] = a_ins[j]
        j -= 1
        desplazamientos += 1
        print(f"  Desplazamiento: movido a_ins[{j+1}] = {a_ins[j+1]}")
    
    a_ins[j+1] = valor_actual
    print(f"Desplazamientos realizados: {desplazamientos}")
    print("Arreglo tras insertar:", a_ins)
print("\nArreglo ordenado final:", a_ins)
