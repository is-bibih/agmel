# Diseño de marmitas y simulación de dinámica de fluidos para AGMEL

Se puede descaargar una versión comprimida del repositorio desde Google Drive: https://drive.google.com/drive/folders/1KyC3ZxNy4q8cKd6olZpOQBJz8WHimrHQ?usp=sharing

Incluye las geometrías ya generadas.

# Generaación de geometrías

Para generar la geometría desde cero, primero navegar al directorio relevante.
Por ejemplo, para la marmita sin modificaciones:

```
cd v4-marmita
```

Después, ejecutar los siguientes comandos:

```
blockMesh
snappyHexMesh -cellZones -overwrite
changeDictionary -region heater
changeDictionary -region v4
changeDictionary -region water
changeDictionary -region air
```

# Ejecución de simulaciones

Dentro del directorio relevante, ejecutar el siguiente comando:

```
chtMultiRegionFoam
```
