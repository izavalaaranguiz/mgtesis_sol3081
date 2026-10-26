# Esquema de presentación — Uruguay (20 min)

**Tesis:** Fuentes intergeneracionales de la homogeneidad y segregación ocupacional en redes de contacto en Santiago
**Formato:** 20 min de exposición → ~11 láminas (≈1,5–2 min cada una), dejando 3–4 min de colchón.
**Estado:** primer esqueleto para revisar con Gabriel. Las cifras son preliminares (modelos actuales) y deben verificarse contra las tablas finales antes de armar las láminas.

---

## Mapa de tiempos

| # | Sección | Min | Lámina(s) |
|---|---|---|---|
| 1 | Problema y pregunta | 3 | 1–2 |
| 2 | Datos y modelo | 4 | 3–4 |
| 3 | Resultado 1: niveles de segregación (ω) | 3 | 5–6 |
| 4 | Resultado 2: cuánto explica la similitud (ω′, ω_prop) | 4 | 7–8 |
| 5 | Resultado 3: origen vs. destino (Δω_prop, β) | 4 | 9–10 |
| 6 | Conclusiones y próximos pasos | 2 | 11 |
| | **Total** | **20** | |

Si hay que recortar: se sacrifica la lámina 4 (priors/diagnósticos, pasan a la voz en una frase) y se condensan 5–6 en una sola.

---

## 1. Problema y pregunta (3 min)

### Lámina 1 — El problema conceptual
**Mensaje:** la *homogeneidad* y la *segregación* de las redes suelen tratarse como lo mismo, pero no lo son.
- Homogeneidad: que los contactos de una persona se parezcan a ella (mirada desde el ego).
- Segregación: que el contacto con ciertos grupos ocupacionales esté desigualmente repartido (mirada desde las ocupaciones, más allá de lo que se esperaría por azar).
- Se tienden a confundir, y por eso no sabemos *de dónde viene* la segregación: ¿de que las personas buscan a quienes se les parecen, o de dónde vienen?
- **Gancho:** especificar el vínculo entre ambas, tal como DiPrete et al. (2011) lo hicieron para subpoblaciones, pero llevándolo a *qué recursos y ambientes ocupacionales* estructuran las redes.

### Lámina 2 — Pregunta e idea central
- **Pregunta:** ¿qué parte de la segregación ocupacional de las redes de contacto se explica por la similitud de estatus, y esa similitud es la del **destino** (posición actual del ego) o la del **origen** (hogar de crianza)?
- Qué revela el orden origen/destino: si pesa el origen, la segregación reproduce desigualdades heredadas; si pesa el destino, refleja la estratificación presente.
- Hipótesis (exploratorias, una línea cada una en pantalla o solo de fondo):
  - H2: los extremos del estatus están más segregados que el medio.
  - H3: la segregación se explica más por el destino que por el origen.
  - H4: la similitud explica más en lazos cercanos que en conocidos.
- *(H1, asimetría arriba/abajo, queda para el cierre o para preguntas.)*

---

## 2. Datos y modelo (4 min)

### Lámina 3 — Datos y medida
- Generador de posiciones con **27 ocupaciones**, N = 1.124 personas, 30.348 díadas ego–ocupación, Santiago.
- Dos tipos de lazo: **cercanos** (amigos cercanos o familiares) y **conocidos** (el resto de los contactos).
- Estatus con **ISEI**, en tres niveles tal como en la Tabla 1 del informe: Alto (≥66, 7 ocupaciones), Medio (41–65, 9), Bajo (≤40, 11).
- Origen = ISEI del sostenedor del hogar a los 15 años; destino = ISEI propio.
- **Visual:** tabla descriptiva corta (Tabla 1) o gráfico de las 27 ocupaciones ordenadas por ISEI con los tres bloques coloreados. Este gráfico se reutiliza como eje en las láminas de resultados.

### Lámina 4 — Modelo (una sola lámina, sin ecuaciones densas)
- Modelo de datos relacionales agregados (ARD): Zheng et al. (2006), DiPrete et al. (2011), **Covariate Model de Baum (2025)**.
- Binomial negativa: Var = ω_k · μ_ik, con ω_k ≥ 1. **ω − 1 = exceso de dispersión = segregación** no explicada por el azar/popularidad.
- Tres modelos encadenados:
  1. **Base** (solo grados y tamaños de grupo) → ω
  2. **Con covariables** (distancia de estatus de destino y origen, arriba/abajo, más controles: educación, sexo, edad) → ω′
  3. Modelos restringidos (sin destino, sin origen) → contribución única de cada polo (Δω_prop)
- Métrica clave: **ω_prop = (ω − ω′)/(ω − 1)**, la proporción del exceso explicada por las covariables. Es libre de escala, por lo que se puede comparar entre ocupaciones y tipos de lazo; ω no.
- Una línea técnica a decir en voz alta: estimación bayesiana en Stan, 4 cadenas × 2.000 iteraciones, sin divergencias, R̂ ≤ 1,01 (detalle en el apéndice).
- **Visual:** diagrama simple de cuatro cajas (base → con covariables → sin destino / sin origen) en vez de fórmulas.

---

## 3. Resultado 1 — Niveles de segregación (3 min) *[Sección 4.2 del informe]*

### Lámina 5 — ¿Dónde hay más segregación? (ω)
- **Visual central:** gráfico estilo Fig. 3 de Baum (2025): ω por ocupación, ordenado de mayor a menor, con IC 95% (**solo para ω y ω′**), un panel por tipo de lazo.
- Qué decir:
  - Todas las ocupaciones tienen ω > 1: hay segregación más allá del azar.
  - Empezar nombrando las ocupaciones de **mayor** y de **menor** dispersión (completar con las del gráfico final), y luego la conclusión general.
  - Cuidado: ω crece con el número medio de contactos, así que no se compara en absoluto entre ocupaciones ni entre tipos de lazo. Esto justifica pasar a ω_prop.

### Lámina 6 — ¿Los extremos están más segregados? (H2)
- **Visual:** ω por nivel de prestigio (Alto / Medio / Bajo), ya sea el mismo gráfico coloreado por banda o una tabla pequeña (ω y ω′ medios por banda).
- Veredicto preliminar:
  - **Lazos cercanos:** H2 apoyada, los extremos se separan del medio.
  - **Conocidos:** apoyo parcial, solo el extremo alto; medio y bajo prácticamente igual (2,75 vs. 2,76). Advertir que el resultado es sensible a dónde se cortan las bandas.
- Mensaje a retener: los grupos medios aparecen como puentes relacionales, menos segregados que los extremos (con la salvedad anterior).

---

## 4. Resultado 2 — Cuánto explica la similitud (4 min) *[Sección 4.3]*

### Lámina 7 — ω vs. ω′: lo que explican las covariables
- **Visual:** gráfico de puntos emparejados por ocupación (ω → ω′), ordenado por ISEI o por ω. Es el gráfico que más fácilmente "se ve" desde el fondo de la sala.
- Qué decir: las covariables reducen la dispersión, pero lo que queda sigue siendo > 1 en la mayoría de los casos.

### Lámina 8 — La respuesta a la pregunta de Bucca: exceso explicado *y* residual
- Contexto en una frase: no basta con mirar la razón ω_prop, hay que mirar el exceso explicado y el no explicado por separado.
- **Visual:** descomposición del exceso total (ω − 1) en *explicado* (ω − ω′) y *residual* (ω′ − 1) por ocupación; opción: barras apiladas para las 27 ocupaciones, o solo para 6–8 casos ilustrativos y la tabla grande va al apéndice.
- Hallazgos clave:
  - ω_prop **por nivel de prestigio** (promedio Alto/Medio/Bajo): cercanos 0,39 / 0,16 / 0,12; conocidos 0,23 / 0,07 / 0,03. La similitud explica sobre todo el extremo alto; casi nada del bajo.
  - El exceso **explicado** se asocia fuertemente con el ISEI (r ≈ 0,79 cercanos, 0,73 conocidos); el exceso **residual** no (r ≈ 0).
  - ω_prop casi no se asocia con el exceso total (r = 0,11 y 0,29): no es un mero reflejo de cuánta segregación hay.
  - Dos casos para ilustrar: **Ingenieros** (poco exceso, mucho explicado, ω_prop 0,61) vs. **Trabajadores agrícolas** (mucho exceso, casi nada explicado, ω_prop ≈ 0).
- Mensaje: la segregación del extremo bajo existe pero **no se explica** por la similitud de estatus; sus fuentes están en otro lado (territorio, redes laborales, etc. → próximos pasos).
- Cautela: sin incertidumbre a nivel de banda; tomarlo como patrón descriptivo.

---

## 5. Resultado 3 — Origen vs. destino (4 min) *[Sección 4.4]*

### Lámina 9 — Contribución única de destino y origen (Δω_prop) — H3 y H4
- **Visual:** gráfico de barras agrupadas con Δω_prop destino vs. origen, por tipo de lazo (2 × 2). Alternativa: dispersión destino (x) vs. origen (y) por ocupación con diagonal.
- Hallazgos:
  - **H3 (destino vs. origen):** apoyada en lazos cercanos (Δ medio 0,034 destino vs. 0,018 origen; el destino domina en 16 de 27 ocupaciones); sin conclusión en conocidos (0,004 vs. 0,006).
  - **H4 (cercanos vs. conocidos):** apoyada. ω_prop medio 0,20 en cercanos vs. 0,10 en conocidos (mayor en 24 de 27 ocupaciones); la contribución del destino es unas 9 veces mayor y la del origen unas 3.
  - Salvedades que decir en voz alta: sin IC para ω_prop/Δω_prop (como en Baum); ω_prop incluye los controles, y falta un modelo sin distancias.

### Lámina 10 — Coeficientes de distancia: la asimetría (H1)
- **Visual:** coefplot con los 4 β (destino arriba/abajo, origen arriba/abajo), por tipo de lazo, con IC 95%, reportados por cada 10 puntos de ISEI.
- Mensaje (verificar con la estimación final, vienen del plan de resultados previo):
  - Todos los β son negativos: la distancia de estatus reduce el contacto.
  - Distancia hacia arriba pesa más que hacia abajo, es decir "techo social" (Blau 1977; DiPrete et al. 2011).
  - La asimetría es clara entre **conocidos** (destino: ratio ≈ 5×) y se diluye en los **cercanos**, sobre todo en el origen.
- *(Opcional si hay tiempo)* Curvas de tasa relativa predicha exp(β × distancia): es la pieza más intuitiva si queda espacio.

---

## 6. Conclusiones y próximos pasos (2 min)

### Lámina 11 — Qué sabemos y qué falta
**Tres conclusiones (una frase cada una):**
1. La segregación ocupacional existe en todas las ocupaciones y no es independiente del estatus: los extremos están más segregados (H2, apoyada en lazos cercanos).
2. La similitud de estatus explica sobre todo el extremo alto; en el bajo la segregación es en gran parte **no explicada**.
3. En lazos cercanos pesa más el destino que el origen (H3b), y la similitud explica más que en conocidos (H4b).

**Próximos pasos:**
- Covariables adicionales: ingreso, hijos, pareja, tamaño de comuna.
- Ampliar los modelos para ocupaciones de bajo prestigio (donde queda más exceso residual).
- Comparación LOO-CV entre especificaciones; análisis de sensibilidad a los priors (Zheng: 1/ω ~ U(0,1)).
- Verificación de la geometría de Var(λ_ik) por ocupación.

---

## Apéndice / diapositivas de reserva (para preguntas)

- A1. Tabla grande de las 27 ocupaciones: ω_prop, Δω_prop, exceso explicado y residual, por tipo de lazo.
- A2. Priors y su fundamento (Zheng 2006; DiPrete 2011); diferencia con la prior de ω (Gamma(2, 0,5) frente a Uniforme(0,1) en 1/ω).
- A3. Diagnósticos: R̂, ESS, E-BFMI, sin divergencias; renormalización posterior de α_i y π_k (identificables sólo hasta una constante).
- A4. Sensibilidad de H2 al corte de las bandas de prestigio.
- A5. Caso inestable: Electricistas (cercanos), exceso 0,11, IC de ω_prop muy amplio ([−2,74; 0,84]).

---

## Decisiones para hablar con Gabriel

1. **Dónde poner el énfasis teórico:** ¿lámina 1–2 más largas (argumento conceptual, 4–5 min) a costa de resultados, o mantener la proporción de arriba?
2. **¿Cuántos resultados?** Propuesta: tres bloques (niveles, explicado/residual, origen/destino). El coefplot (lámina 10) es lo más sustantivo para sociólogos; ¿lo subimos antes y dejamos Δω_prop para el apéndice?
3. **Audiencia en Uruguay:** ¿conocen ARD / Position Generator? Define cuánto tiempo gastar en la lámina 4.
4. **ω_prop negativo y sin IC:** ¿cómo lo explicamos si preguntan? (Baum: no es una falla, ω_prop no es un nivel de segregación.)
5. **Hipótesis como estructura:** ¿presentarlas como H1–H4 explícitas, o solo como tres preguntas? Hoy todas son exploratorias.
6. **Re-correr 0927** con las nuevas bandas de prestigio para regenerar figuras y tablas antes de armar las láminas.

## Figuras y tablas a producir (checklist)

- [ ] Gráfico de las 27 ocupaciones por ISEI con las 3 bandas (lámina 3)
- [ ] Diagrama de modelos (lámina 4)
- [ ] ω por ocupación con IC, 2 paneles (lámina 5)
- [ ] ω y ω′ por nivel de prestigio (lámina 6)
- [ ] Pares ω → ω′ por ocupación (lámina 7)
- [ ] Descomposición explicado / residual (lámina 8)
- [ ] Δω_prop destino vs. origen, 2 × 2 (lámina 9)
- [ ] Coefplot de los 4 β por tipo de lazo (lámina 10)
- [ ] Tabla grande de apéndice (A1)
