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

# Funcion
def contar_titulos_populares(matriz, calificacion_minima, anio_limite):

    contador = 0

    for titulo in matriz:

        nombre = titulo[0]
        anio = titulo[1]
        calificacion = titulo[2]
        genero = titulo[3]

        if calificacion >= calificacion_minima and anio >= anio_limite:
            contador += 1

    return contador


# Datos de prueba
calificacion_minima = 8.5
anio_limite = 2022

# Llamado de la funcion
resultado = contar_titulos_populares(
    videoteca,
    calificacion_minima,
    anio_limite
)

# Mostrar resultado
print("Cantidad de titulos populares y recientes:", resultado)



