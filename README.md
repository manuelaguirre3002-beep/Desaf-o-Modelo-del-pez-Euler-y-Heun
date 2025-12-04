# DESAFIO DEL PEZ Y CRECIMIENTO DE UN ORGANISMO
Metodos Numericos – UMSA

Autor: Carlos Manuel Miranda Aguirre  
Carrera: Informatica – Universidad Mayor de San Andres (UMSA)

---

## 1. Objetivo del trabajo

Estudiar el crecimiento de organismos usando ecuaciones diferenciales ordinarias y comparar:

- Solucion exacta (resuelta analiticamente).
- Metodo de Euler.
- Metodo de Heun (Euler mejorado).

Todo se implemento en Excel / Google Sheets y se analizaron los errores de cada metodo.

---

## 2. Modelo 1: Crecimiento del pez

- Se modela el peso del pez con una ecuacion diferencial del tipo von Bertalanffy.
- Datos: a = 5, b = 2 y peso inicial w(0) = 0.5 lb.
- A partir de la ecuacion se obtiene una solucion exacta que tiende a un **peso maximo teorico de 15.625 lb**.
- En Excel se trabajo con paso h = 0.5 para 0 <= t <= 10 dias.
- Se calcularon tres columnas: solucion exacta, Euler y Heun, mas sus errores.

**Observacion principal:**  
Al final del intervalo, todos los metodos se acercan a ~15.6 lb, pero Euler presenta un error del orden de centesimas, mientras que Heun es claramente mas preciso (error varias veces menor) usando el mismo paso.

---

## 3. Modelo 2: Crecimiento de un organismo

- Se modela la masa de un organismo con una ecuacion diferencial de crecimiento con masa maxima.
- Datos: k = 0.3, masa maxima m_max = 300 kg y masa inicial m(0) = 1 kg.
- La solucion exacta del modelo se aproxima a la **masa limite de 300 kg**.
- En Excel se uso paso h = 10 dias para 0 <= t <= 400 dias.
- De nuevo se compararon solucion exacta, Euler y Heun, con sus errores.

**Observacion principal:**  
Tanto Euler como Heun siguen bien la curva exacta y convergen cerca de 300 kg; los errores numericos son muy pequenos, pero Heun vuelve a ser ligeramente mas exacto que Euler.

---

## 4. Conclusion general

- Ambos modelos muestran un crecimiento que se estabiliza en un valor maximo determinado por los parametros del sistema.
- Las implementaciones en Excel permiten ver paso a paso como evolucionan las soluciones numericas.
- El metodo de Euler es mas simple pero menos preciso.
- El metodo de Heun ofrece **mejor aproximacion con el mismo tamano de paso**, por lo que es mas recomendable cuando se busca buena precision sin refinar demasiado la malla de tiempo.
