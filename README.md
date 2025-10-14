
# print("TALLER — Arreglos y Ordenación")

# # 1) Índices y acceso (Básico)
# a = [7, 3, 9, 5, 9]
# print("1) Índices y acceso:")
# print("a =", a)
# print("1) print(a[0]) =>", a[0])
# print("2) print(a[3]) =>", a[3])
# print("3) print(a[len(a)-1]) =>", a[len(a)-1])
# print("4) Explicación: El último índice es len(a)-1 porque los índices empiezan en 0.\n   Si hay n elementos, el primero es 0 y el último es n-1.\n")

# # 2) Recorrido y conteo (Básico)
# notas = [12, 8, 15, 19, 10, 14]
# contador = 0
# print("2) Recorrido y conteo: notas =", notas)
# for i in range(len(notas)):   
#     if notas[i] >= 14:
#         contador += 1
# print("Cantidad de notas ≥ 14:", contador, "\n")

# # 3) Llenado con datos simulados (Básico)
# edades = [0, 0, 0, 0, 0]
# valores = [21, 18, 30, 25, 19]
# print("3) Llenado con datos simulados:")
# for i in range(len(edades)):
#     edades[i] = valores[i]
#     print(f"{i} -> {edades[i]}")
# print()    

# # 4) Actualización por índice (Básico)
# nombres = ['Ana','Luis','Mar','Sofi']
# print("4) Actualización por índice: nombres iniciales =", nombres)
# nombres[2] = 'María'
# print("Elemento actualizado (índice 2):", nombres[2])
# print("Arreglo completo:", nombres, "\n")

# # 5) Inserción conceptual con desplazamiento (Intermedio)
# arr = [10, 20, 30, 40, None]
# print("5) Inserción con desplazamiento: arr inicial =", arr)

# pos = 2
# valor = 25

# for i in range(len(arr)-2, pos-1, -1):  
#     print(f"Desplazando arr[{i}] -> arr[{i+1}] (moviendo {arr[i]})")
#     arr[i+1] = arr[i]
#     print("Estado parcial:", arr)
# arr[pos] = valor
# print("Insertado", valor, "en posición", pos)
# print("Resultado final:", arr, "\n")

# # 6) Borrado conceptual con desplazamiento (Intermedio)
# arr2 = [4, 6, 8, 10, 12]
# print("6) Borrado con desplazamiento: arr2 inicial =", arr2)
# borrar = 2
# for i in range(borrar, len(arr2)-1):
#     arr2[i] = arr2[i+1]
#     print(f"Desplazando arr2[{i+1}] -> arr2[{i}] (valor movido: {arr2[i]})")
# arr2[-1] = None
# print("Arreglo resultante tras borrar índice", borrar, ":", arr2, "\n")

# # 7) Búsqueda lineal (Intermedio)
# datos = [7, 2, 9, 4, 2]
# buscar = 2
# encontrado = False
# indice_encontrado = -1
# print("7) Búsqueda lineal en datos =", datos)
# for i in range(len(datos)):
#     if datos[i] == buscar:
#         encontrado = True
#         indice_encontrado = i
#         print("Encontrado en índice:", indice_encontrado)
#         break
# if not encontrado:
#     print("No encontrado")
# print()

# # 8) Traza de Burbuja (Intermedio)
# a_burbuja = [5, 1, 4, 2]
# print("8) Traza de Burbuja (cada pasada): a =", a_burbuja)
# n = len(a_burbuja)
# pass_num = 0
# for pasada in range(n-1):
#     pass_num += 1
   
#     for j in range(0, n-1-pasada):
#         if a_burbuja[j] > a_burbuja[j+1]:
#             a_burbuja[j], a_burbuja[j+1] = a_burbuja[j+1], a_burbuja[j]
#     print(f"Después de la pasada {pass_num}: {a_burbuja}")
# print("Resultado final ordenado:", a_burbuja, "\n")


# a_opt = [3, 2, 4, 1, 5]
# print("9) Burbuja optimizada: a =", a_opt)
# comparaciones = 0
# intercambios = 0
# n = len(a_opt)
# for i in range(n-1):
#     hubo_intercambio = False
#     for j in range(0, n-1-i):
#         comparaciones += 1
#         if a_opt[j] > a_opt[j+1]:
#             a_opt[j], a_opt[j+1] = a_opt[j+1], a_opt[j]
#             intercambios += 1
#             hubo_intercambio = True
#     print(f"Pasada {i+1} -> {a_opt} (intercambio en pasada: {hubo_intercambio})")
#     if not hubo_intercambio:
#         print("No hubo intercambios en la pasada; algoritmo detenido anticipadamente.")
#         break
# print("Comparaciones totales:", comparaciones)
# print("Intercambios totales:", intercambios)
# print("Arreglo final:", a_opt, "\n")

# # 10) Inserción (Insertion Sort) con traza (Avanzado)
# a_ins = [9, 7, 8, 3]
# print("10) Insertion Sort con traza: a =", a_ins)

# for i in range(1, len(a_ins)):
#     valor_actual = a_ins[i]
#     j = i - 1
#     desplazamientos = 0
#     print(f"\ni = {i}, valor actual = {valor_actual}")
   
#     while j >= 0 and a_ins[j] > valor_actual:
#         a_ins[j+1] = a_ins[j]
#         j -= 1
#         desplazamientos += 1
#         print(f"  Desplazamiento: movido a_ins[{j+1}] = {a_ins[j+1]}")
    
#     a_ins[j+1] = valor_actual
#     print(f"Desplazamientos realizados: {desplazamientos}")
#     print("Arreglo tras insertar:", a_ins)
# print("\nArreglo ordenado final:", a_ins)
