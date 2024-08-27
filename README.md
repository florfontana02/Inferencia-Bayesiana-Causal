# IBC1.2024.2

Este es el repositorio oficial de la materia `Inferencia Bayesiana Causal 1`, 2024, segundo semestre.
<!--
<tr>
  <td width="50%" align="center"><img src="auxiliar/static/ecyt.jpeg" width="250"/></td>
</tr>-->

## Materia `Inferencia Bayesiana Causal 1`. (IBC1.2024.2)

La materia `Inferencia Bayesiana Causal 1` se imparte como optativa de forma paralela en las licenciaturas de ciencias de datos de la Escuela de Ciencia y Tecnología de la UNSAM y en las licenciatura de ciencia de datos, ciencias de la computación y posgrado de Facultad de Ciencias Exactas y Naturales, UBA.

<br>

<table>
  <tr>
    <td width="50%" align="center"><img src="https://github.com/glandfried/images/blob/master/logos/ecyt.jpeg" width="250"/></td>
    <td width="50%" align="center"><img src="https://github.com/glandfried/images/blob/master/logos/UNSAM_blanco.png" width="250"/></td>
  </tr>
  <tr>
    <td width="50%" align="center"><b>Campus Migueletes - EscuelaCyT</b></td>
    <td width="50%" align="center"><b>Universidad Nacional de San Martín - Argentina</b></td>
  </tr>
</table>

  <br>

<table>
  <tr>
    <td width="50%" align="center"><img src="https://github.com/glandfried/images/blob/master/logos/fcen.png" width="250"/></td>
    <td width="50%" align="center"><img src="https://github.com/glandfried/images/blob/master/logos/UBA2_blanco.jpg" width="250"/></td>
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

## Objetivos.

Esta materia está enfocada en la evaluación de argumentos causales alternativos mediante la (aproximación a) la aplicación estricta de las reglas de la probabilidad, el sistema de razonamiento en contextos de incertidumbre. La materia tiene por principal objetivo revisar los métodos desarrollados en las últimas décadas para:

- Especificar matemáticamente los argumentos causales expresados en lenguaje natural mediante métodos gráficos intuitivos
- Precisar cómo la estructura causal influye en el flujo de inferencia entre las variables del modelo.
- Identificar el efecto causal entre variables de un modelo causal en base de datos observacionales (sin intervenciones).
- Diseñar experimentos que permitan evaluar teorías causales alternativos
- Seleccionar decisiones óptimas en ciclos de acción-percepción con una naturaleza oculta (simulada).

El problema real detrás de este problema de conocimiento es responder preguntas esenciales como **¿Qué acciones generan bienestar?**.

## Marco Conceptual

**Definición de Inferencia**. Las "verdades" son proposiciones válidas para todas las personas. Las ciencias con datos deben validar sus proposiciones (hipótesis) en sistemas naturales abiertos. ¿Tiene sentido hablar de "verdad" si justamente tenemos incertidumbre respecto de su valor real? Al menos podemos evitar mentir: no afirmar más de lo que se sabe (maximizando incertidumbre) sin ocultar todo aquello que sí se sabe (dada la información disponible o restricciones).

**Definición de Bayes**. Evaluación de todo el espacio de hipótesis mediante la (aproximación a la) aplicación estricta de las reglas de la probabilidad: preservar la creencia previa que sigue siendo compatible con los datos (regla del producto) y predecir con la contribución de todas las hipótesis (regla de la suma). Debido al costo computacional de las reglas de la probabilidad, durante el siglo 20 propusieron una gran cantidad criterios arbitrarios de selección de hipótesis, que genera siempre efectos secundarios indeseados como ocurre con el overfitting. Afortunadamente, la aplicación estricta de las reglas de la probabilidad no exhiben estos problemas. Si lo hicieran, no tendríamos aún un sistema de razonamiento para contexto de incertidumbre.

**Definición de Causal**. El problema real de todo organismo vivo es orientar el ciclo de acción-percepción con la naturaleza en favor de su reproducción, supervivencia y bienestar. Los problemas del conocimiento científico obtienen su relevancia y jerarquía de los objetivos que persigue alcanzar. Luego de una percepción evaluamos los argumentos causales alternativos maximizando la incertidumbre dada la información disponible, y antes de actuar seleccionamos la acción minimizando la incertidumbre esperada en relación al objetivo que perseguimos.

## Programa

### Primera parte

#### Unidad 1. Introducción a la especificación y evaluación de argumentos causales

- Explicación causal. Creencias honestas. Reglas de razonamiento en contextos de incertidumbre. Métodos gráficos de especificación de argumentos causales.
- La naturaleza generativa de los argumentos causales. Evaluación de modelos causales alternativos. Ejemplos identificables y no identificables.
- Modelos conjugados. Emergencia del overfitting por selección y balance natural por evaluación. Ejemplo con modelos polinomiales de complejidad creciente.
- Bibliografía sugerida: Bishop 2013 (1-4). Bishop 2006 (1.1-1.3, 2.1-2.3, 3.3-3.4) Otras: Jaynes (paper), Samaja (3.1-3.4), Klimovsky (4), Jaynes (paper)

#### Unidad 2. Sorpresa: el problema de la comunicación con la realidad

- Niveles de base empírica. La estructura invariante del dato. El isomorfismo con los sistemas de comunicación emisor-receptor de la teoría de la información.
- Evaluación de sistemas de comunicación alternativos en base a su tasa de predicción en el tiempo, expresada en órdenes de magnitud. Entropía y divergencia.
- Especificación de modelos mediante factor graphs. Descomposición de las reglas de la probabilidad como pasaje de mensajes entre los nodos de las red causal.
- Bibliografía sugerida:  MacKay (1.1, 2.4-6, 4.1), Kelly (paper). Otras: Klimovsky (2), Samaja (3.5, 3.6.2-5).

#### Unidad 3. Estructuras causales dinámicas (teorías) y flujo de inferencia.

- Estructuras causales dinámicas (teorías). Su especificación mediante gates. Los niveles de razonamiento causal: asociacional, intervencional y contrafactual.
- Flujo de inferencia en teorías causales: pipe, fork, collider. Apertura y cierre de flujos de inferencia entre regiones de la red causal (d-separation).
- Los conceptos de potential outcome y do-operator. El efecto de las intervenciones: truncated factorization. Buenos y malos controles. Ejemplos varios.
- Bibliografía sugerida. Winn (paper), Bishop 2006 (8.2-8.2.2, 8.4-8.4.4, 8.4.7). Neal (2.1, 3, 4.1), Pearl (1).

##### Unidad 4. Estimación pasiva de efectos causales.

- Enfoques de estimación de efecto causal: adjustment formula, inverse probability weighting, propensity scores
- Métodos para predicción de contrafactuales: twin networks. Método principal para estimación de efectos causales: el criterio backdoor.
- Otros criterios: frontdoor y do-calculus. Ejemplos de identificación de variables de control. Alternativas: deconfounder, variables instrumentales y otras.
- Bibliografía sugerida. Pearl (3,6-7), Hernán (parte I), Cinelli (paper), Neal (4, 6, 7.5-7.6).

### Segunda parte

#### Unidad 5. Acción-percepción: el problema de la interacción con la realidad

- Persistencia de la vida fuera del equilibrio. Intercambio acción-percepción agente-ambiente. El intento por minimizar la sorpresa esperada.
- Reformulación ergódica de la teoría de utilidad esperada. Planificación como inferencia. Evaluación de acciones mediante pseudo-posteriors.
- Control óptimo en Partial Observed Markov Decision Process (POMDP). Ejemplos de selección de acciones. Valor de la información.
- Bibliografía: Parr (1-3), Schrodinger (4-7),  Peters (paper), Levine (1-2), Pearl (4). Otras: Koller (21)

#### Unidad 6. Evaluación activa de argumentos causales.

- Evaluación de argumentos causales como un juego de interacción acción-percepción con el ambiente. Métodos de Monte Carlo para evaluar teorías.
- Ejemplos de evaluación de modelos causales a través de datos obtenidos por interacción con una simulador causal subyacente oculto.
- Planificación del diseño experimental. La emergencia de la estrategia falsacionista como comportamiento óptimo.
- Bibliografía sugerida. Kass (paper), Pearl (7,9). Hernán (parte II)

#### Unidad 7. Inferencia causal en series temporales.

- Modelos de historia completa. Problemas de usar el último posterior como prior del siguiente evento. Propagación de la información por toda la red histórica causal.
- Estimación de efecto causal por simulación de contrafactuales. Intervenciones en series temporales. Monte Carlo para series temporales.
- Evaluación de modelos causales alternativos. Apuestas óptimas en deportes: criterio Kelly, fractional Kelly y otros criterios.
- Bibliografía sugerida. Brodersen (paper), Dangauthier (paper), Bishop (13.2.3-13.2.4, 13.3), Hernán (parte II).

#### Unidad 8. Isomorfismo probabilidad-evolución y hackatón “apuestas de vida”.

- Isomorfismo entre las ecuaciones fundamentales de la teoría de la probabilidad (teorema de Bayes) y la teoría de la evoluición (replicator dynamic).
- Las emergencia de las variantes que reducen las fluctuaciones por diversificación individual, cooperación, especialización cooperativa y heterogeneidad.
- Presentación de una competencia de inferencia, intervención, apuestas e intercambios de recursos. Cierre y conclusiones.
- Bibliografía sugerida. Czegel (paper).

## Bibliografía

Bibliografía en links, en `github.com/glandfried/biblio/releases/tag/teca`, Sci-hub o Libgen.

- Bishop. Pattern recognition and machine learning. Springer; 2006
- Levine S. Reinforcement learning and control as probabilistic inference: Tutorial and review. arXiv. 2018.
- Parr T, Pezzulo G, Friston KJ. Active Inference. MIT Press; 2022
- Pearl J. Causality. Cambridge university press; 2009.
- Peters O. The ergodicity problem in economics. Nature Physics. 2019.
- Winn J. Causality with gates. In: Artificial Intelligence and Statistics. PMLR; 2012.

### Complementaria:

- Bishop. Model-based machine learning. Philosophical Transactions of the Royal Society A: Mathematical, Physical and Engineering Sciences. 2013
- Brodersen KH, Gallusser F, Koehler J, Remy N, Scott SL. Inferring causal impact using Bayesian structural time-series models. The Annals of Applied Statistics. 2015;
- Chopin N, Papaspiliopoulos O, et al. An introduction to sequential Monte Carlo. Vol. 4. Springer; 2020.
- Cinelli C, Forney A, Pearl J. A crash course in good and bad controls. Sociological Methods & Research. 2022
- Czégel D, Giaffar H, Tenenbaum JB, Szathmáry E. Bayes and Darwin: How replicator populations implement Bayesian computations. BioEssays. 2022.
- Dangauthier P, Herbrich R, Minka T, Graepel T. Trueskill through time: Revisiting the history of chess. In: Advances in Neural Information Processing Systems; 2008
- Gronau QF, Sarafoglou A, Matzke D, Ly A, Boehm U, Marsman M, et al. A tutorial on bridge sampling. Journal of mathematical psychology. 2017.
- Hernán MA, Robins JM. Causal inference: What if. 2020.
- Jaynes ET. Bayesian methods: General background; 1984.
- Kass RE, Raftery AE. Bayes factors. Journal of the American Statistical Association. 1995.
- Kelly jr JL. A New Interpretation of Information Rate. Bell System Technical Journal. 1956
- Klimovsky G. Las desventuras del conocimiento científico; 1994
Koller D, Friedman N. Probabilistic graphical models: principles and techniques. MIT press; 2009.
- MacKay DJ. Information theory, inference and learning algorithms. Cambridge university press; 2003.
- McElreath R. Statistical rethinking: A Bayesian course with examples in R and Stan. 2020
- Neal. Introduction to causal inference. Course Lecture Notes (draft). 2020;
- Perrakis K, Ntzoufras I, Tsionas EG. On the use of marginal posteriors in marginal likelihood estimation via importance sampling. Computational Statistics & Data Analysis. 2014.
- Popper K. La lógica de la investigación científica; 1967.
- Samaja J. Epistemologı́a y metodología: elementos para una teoría de la investigación científica. EUDEBA; 1999.
- Schrodinger E. ¿Qué es la vida?. Espasa-Calpe. 1948.
- Vousden W, Farr WM, Mandel I. Dynamic temperature selection for parallel tempering in Markov chain Monte Carlo simulations. Monthly Notices of the Royal Astronomical Society. 2018

<!--La palabra átomo proviene de los vocablos griegos $\alpha$  (sin) y $\tau o \mu o \nu$ (tomon o corte), por lo que significa indivisible.
Sin embargo, hoy sabemos que los átomos están compuestos de electrones, protones y neutrones, y que además los protones y neutrones están compuestos de cuarks.
Los electrones y cuarks forman parte del conjunto de 17 partículas consideradas elementales, sobre las que se ignora su estructura interna.

<br>

Las 17 partículas elementales conocidas por el modelo estándar se clasifican por sus propiedades de <em>materia</em>, <em>carga</em> y <em>espín</em>.
Estas propiedades interactúan entre sí, formando una enorme diversidad de agregaciones de partículas elementales, cada una con sus propias propiedades emergentes.
Algunas de estas interacciones o agregaciones son más fuertes o estables y se encuentran presentes en mayor proporción que otras, como son los protones y los neutrones, que luego se agregan para formar los núcleos de los $118$ átomos conocidos hasta la actualidad.

<table align="center">
  <tr align="center">
    <td width="50%" align="center"><img src="https://raw.githubusercontent.com/glandfried/images/master/atomo_de_oxigeno.png" width="250"/></td>
   </tr>
  <tr>
    <td width="50%" align="center"><b>Átomo de oxígeno</b></td>
  </tr>
</table>

A su vez, las interacciones entre los $118$ átomos puede producir una cantidad no acotada de interacciones o agregaciones conocidas como moléculas, algunas de las cuales son más fuertes o estables que otras y se encuentran presentan en mayor proporción que otras.
Y a su vez, la interacción o agregación entre moléculas produce lo que conocemos, el agua, y nuestro cuerpo.

<br>

Las propiedades de la molécula $H_20$ son emergentes de un tipo de interacción o agregación entre los átomos de oxígeno $O$ e hidrógeno $H$, y las propiedades del agua son emergentes de la interacción o agregación entre moléculas $H_20$.
Las moléculas del agua nacen y mueren durante procesos químicos, como por ejemplo los que ocurren durante la combustión.
En particular, la electrólisis del agua transforma el agua líquida ($2 \cdot H_2O$) en hidrógeno y oxígenos gaseosos ($H_2 + O_2$).

$$\begin{align*}
& \text{Cátodo: } 2 \cdot H_2O+ 2e^{−} \rightarrow  H_2 + 2\cdot OH^{−} \\
& \text{Ánodo: } 4 \cdot OH^{−} \rightarrow O_2​ + 2\cdot H_2​O + 4e^{−}.
\end{align*}$$

Y a la inversa, la combustión de hidrógeno y oxígeno gaseosos producen átomos de agua y energía en forma de calor o luz.

$$ 2\cdot H_2​ + O_2​ \rightarrow 2\cdot H_2​O + \text{energía}$$.

Si bien el agua nace y muere, no decimos que el agua sea una forma de vida pues ella no se reproduce.
Pero entre los cientos de millones de moléculas conocidas, existen algunas que tienen la propiedad emergente de reproducirse, como ocurre con los fragmentos de ARN que llamamos virus.
Hay menos controversia en considerar a los virus como forma de vida debido a su indiscutible capacidad para  reproducirse, sobrevivir y diversificarse en el tiempo, adaptándose a los cambios ambientales que ocurren en su entorno, como el sistema inmune del ser humano.

<br>-->

<!--Todas las formas de las materia se encuentran en permanente cambio y movimiento, adaptaciones al entorno.
-->

