# IBC1.2024.2

Este es el repositorio oficial de la materia `Inferencia Bayesiana Causal 1`, 2024, segundo semestre.

## Materia `Inferencia Bayesiana Causal 1`. (IBC1.2024.2)

La materia `Inferencia Bayesiana Causal 1` se imparte como optativa de forma paralela en las licenciaturas de ciencias de datos de la Escuela de Ciencia y Tecnología de la UNSAM y en las licenciatura de ciencia de datos, ciencias de la computación y posgrado de Facultad de Ciencias Exactas y Naturales, UBA.

<br>

<table>
  <tr>
    <td width="50%" align="center"><img src="auxiliar/static/ecyt.jpeg" width="250"/></td>
    <td width="50%" align="center"><img src="auxiliar/static/UNSAM_blanco.png" width="250"/></td>
  </tr>
  <tr>
    <td width="50%" align="center"><b>Campus Migueletes - EscuelaCyT</b></td>
    <td width="50%" align="center"><b>Universidad Nacional de San Martín - Argentina</b></td>
  </tr>
</table>

  <br>

<table>
  <tr>
    <td width="50%" align="center"><img src="auxiliar/static/fcen.png" width="250"/></td>
    <td width="50%" align="center"><img src="auxiliar/static/UBA2_blanco.jpg" width="250"/></td>
  </tr>
  <tr>
    <td width="50%" align="center"><b>Pabellón 0 + Inf - FacultadCEN</b></td>
    <td width="50%" align="center"><b>Universidad Nacional de Buenos Aires - Argentina</b></td>
  </tr>
</table>


## Evaluación

Si sos estudiante, es necesario que tengas una copia privada de este repositorio oficial (con el equipo docente como colaboradores), donde deberán subir los ejercicios y donde podrán actualizar los materiales de la materia haciendo pull del repo fuente.

Habrá dos formas de evaluación.

1. Por un lado podrán realizar auto-evaluaciones descargando del repositorio oficial los casos de test con lo que verificar la correctitud de sus ejercicios.
2. Por otro lado, el equipo docente al tener acceso a su repositorio privado tendrá acceso a sus soluciones y ejecutará tests adicionales.

El resultado de las evaluaciones será enviado mediante un mensaje de commit y eventualmente un archivo explicando el tipo de error.

### Copia privada del repositorio oficial (con equipo docente como colaboradores)

Seguir los siguientes pasos para crear el repositorio.

1. Crear la carpeta donde vivirá su repositorio privado.

    git init nombre_de_carpeta_a_crear

2. Conectarlo con el repositorio oficial.

    git remote add upstream git@github.com:MetodosBayesianos/IBC1.2024.2.git

3. Descargar el contenido del repositorio oficial.

    git pull upstream main

4. Crear un repositorio **privado vacío** en github.

    # Entrar con sus usuario a github.com y crear un repositorio privado vacío.

5. Agregar una referencia al repositorio privado recién creado.

    git remote add origin git@github.com:usuario/nombre_del_repositorio.git

5. Subir los cambios locales a la plataforma.

    git push origin main

6. Dar acceso de edición a equipo docente.

    # En Setting > Collaborators, agregar a @glandfried.

