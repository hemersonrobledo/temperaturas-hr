# Definición de la función para calcular la temperatura promedio por ciudad
def calcular_temperaturas_promedio(temperaturas):
    """
    Esta función recibe una lista de listas, donde cada sublista contiene las temperaturas
    de una ciudad durante varias semanas. La función calcula el promedio de temperaturas
    por ciudad y devuelve un diccionario con el resultado.

    :param temperaturas: Una lista de listas de temperaturas, donde cada sublista
                          corresponde a una ciudad.
    :return: Diccionario con las ciudades y su temperatura promedio.
    """
    promedios = {}  # Diccionario para almacenar el promedio de cada ciudad

    # Nombres de las ciudades
    ciudades = ["Esmeraldas", "Guayaquil", "Manabí"]

    for idx, ciudad in enumerate(temperaturas):
        promedio_ciudad = sum(ciudad) / len(ciudad)  # Calcular el promedio
        promedios[ciudades[idx]] = promedio_ciudad  # Guardar el resultado usando el nombre de la ciudad

    return promedios


# Datos: Temperaturas de 3 ciudades durante 4 semanas
temperaturas = [
    [30, 31, 32, 33],  # Esmeraldas
    [28, 29, 30, 31],  # Guayaquil
    [26, 27, 28, 29]   # Manabí
]

# Llamada a la función
promedios = calcular_temperaturas_promedio(temperaturas)

# Mostrar los resultados
for ciudad, promedio in promedios.items():
    print(f"Temperatura promedio en {ciudad}: {promedio:.2f} °C")

