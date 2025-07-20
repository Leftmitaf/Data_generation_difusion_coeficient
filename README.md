El código contiene la solución de la ecuación de difusión. Aquí sólo hay que realizar una carpeta que diga skin224.
En la carpeta skin224 se depositaran las siguientes soluciones: 
-nu_000000001
      ci_001.png
      ci_002.png
      .........
      ci_900.png
nu_000000002
      ci_001.png
      ci_002.png
      .........
      ci_900.png
................
Un total de 200 clases con 900 imágenes cada una, ya que se demostró que el modelo no estaba aprendiendo con la data anterior. 

También en multiprocesing puede modificar la parte y añadir más núcleos, 
if __name__ == "__main__":
    combinations = [(i, j) for i in range(1, 201) for j in range(1, 901)]
    with Pool(processes=1) as pool:
        pool.map(run_case, combinations)

En donde dice processes = 1 se puede modificar y agregar los núcleos necesarios para realizarlo en paralelo, esto puede ser una tarea costosa.
