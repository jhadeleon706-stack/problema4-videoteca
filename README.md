# Problema 4 - Videoteca Digital
# Matriz de la videoteca
videoteca = [
    ["Stranger Things", 2022, 9.1, "Ciencia Ficcion"],
    ["Avatar 2", 2023, 8.5, "Accion"],
    ["Titanic", 1997, 9.0, "Drama"],
    ["Wednesday", 2022, 8.2, "Terror"],
    ["The Batman", 2022, 8.8, "Accion"],
    ["Encanto", 2021, 7.9, "Animacion"],
    ["Dune", 2023, 9.3, "Ciencia Ficcion"]
]

# Función para contar títulos que cumplen los criterios
def contar_titulos_populares(matriz, calificacion_minima, año_limite):

    contador = 0

    for titulo in matriz:

        nombre = titulo[0]
        año = titulo[1]
        calificacion = titulo[2]
        genero = titulo[3]

        if calificacion >= calificacion_minima and año >= año_limite:
            contador += 1

    return contador


# Datos de prueba
calificacion_minima = 8.5
año_limite = 2022

# Llamado de la función
resultado = contar_titulos_populares(
    videoteca,
    calificacion_minima,
    año_limite
)

# Mostrar resultado
print("Cantidad de títulos populares y recientes:", resultado)


