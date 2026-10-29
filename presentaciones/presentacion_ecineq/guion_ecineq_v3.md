# Guión ECINEQ-LAC · Montevideo, 29 oct 2026 · 20 min

**Gabriel Otero** (teoría y discusión) · **Ignacio Zavala** (datos, modelo y resultados)

Cómo usar este guión: bajo cada diapo, **DECIR** es el texto en inglés (≤ 100 palabras, para hablar, no leer); **SEÑALAR** es el orden de punteros en cada figura; **CIFRAS** son los números que hay que tener a mano; **PASAR** es la frase de transición. Al final: preguntas probables con respuestas (Q&A), hoja de cifras y pendientes por confirmar.

Numeración de la versión actual del deck (sin la diapo opcional de Gabriel "Origin is not a residue…"). Si la pegaste después de la 3, todo desde ahí se corre una.

---

## Plan de tiempos (meta: 20 min)

| Quién | Diapos | Tiempo |
|---|---|---|
| Gabriel | 1–5 (+ opcional) | 4:45 (5:30 con la extra) |
| Ignacio | 6–15 | 12:15 |
| Ignacio, luego Gabriel | 16–17 | 2:30 |
| Total | | ≈ 19:30 (20:15 con la extra) |

Si vas pasado de tiempo, recorta en este orden: (1) diapo 14 (tabla por estatus): lee solo la columna final; (2) diapo 10 (dos cantidades): 30 s; (3) diapo 7 (datos): 45 s; (4) diapo 9: omite la fórmula.

---

## 1 · Título (Gabriel, 0:15)

**DECIR.** Good morning. We present work on the intergenerational sources of homogeneity and occupational segregation in personal networks in Santiago, Chile. Gabriel will lay out the argument; Ignacio will show the data, the model and the results.

---

## 2 · Networks reproduce inequality (Gabriel, 1:00)

**DECIR.** Personal networks are not only a mirror of inequality; they help reproduce it. Information, job opportunities and support circulate through them, so their composition decides which advantages accumulate. Chile is a demanding setting: high inequality, low intergenerational mobility, and strong residential and school segregation. Our question: how are origin and destination positions associated with the homogeneity and the occupational segregation of contact networks in Santiago, and does that differ between close ties and acquaintances?

**SEÑALAR.** Clic final: caja con la pregunta de investigación. Léela entera.

---

## 3 · The literature anchors similarity in current position (Gabriel, 1:15)

**DECIR.** Studies of network composition measure similarity from one reference: ego's current occupation, the destination. But social origin organizes the earliest and most durable ties: family, neighborhood, school. Those contacts are not necessarily erased when position changes. Destination gives contemporary exposure; origin, a historical imprint. The dashed arrow is what this paper adds: if origin matters, segregation reproduces inherited disadvantage; if only destination matters, it reflects present stratification.

**SEÑALAR.** La flecha punteada (origen → red).

### 3b · (Opcional) "Origin is not a residue of destination" (Gabriel, 0:45)

**DECIR.** There are two competing expectations. One: origin is a residue of destination; once we know where people are now, where they come from adds nothing, because position absorbs it. Two: origin plays a role despite the positions that currently configure networks, through inherited ties and early socialization. We let both anchors compete in the same model, each estimated net of the other.

---

## 4 · Homogeneity and segregation: two levels of analysis (Gabriel, 1:30)

**DECIR.** These concepts operate at different levels. Homogeneity is read from the ego: whom each person reports knowing. Segregation is read at the level of access to groups: whether the members of an occupation are known by many people or by a few circles. Because those circles form through similarity, segregation inevitably captures some homogeneity. The studies that use both concepts do not distinguish their levels. We keep them apart and link them through concentration: when contacts pile up among similar egos, counts become overdispersed, omega above one.

**SEÑALAR.** Figura (simulada, no son datos): misma media en los dos paneles; el segundo concentra el acceso (ω = 3).

**NO DECIR** "no son lo mismo". Decir: "operan en niveles distintos".

**PASAR.** "The distance coefficients are ego-level; the explained share of omega is access-level. Ignacio will show both."

---

## 5 · Three questions for Santiago (Gabriel, 0:45)

**DECIR.** Three questions. One, homogeneity: does origin keep a role in whom people know, net of destination, and which weighs more? Two, segregation: are high- and low-status occupations more segregated than middle ones, and how much does status similarity explain, from origin or from destination? Three, tie closeness: do both patterns get stronger among close ties than among acquaintances? All exploratory. Ignacio will show how we measure this and what we find.

---

## 6 · What comes next (Ignacio, 0:15)

**DECIR.** I will go through data, method and variables, then results, then discussion. The appendix has two slides, on identification and on how to read the explained share.

---

## 7 · Data (Ignacio, 1:00)

**DECIR.** We use the 2025 Social Survey of Class, Networks and Political Attitudes: 1,124 adults in the Santiago metropolitan region, probabilistic, face to face. A position generator asks how many people you know in 27 occupations and, of them, how many are close friends or family. That gives 30,348 ego–occupation counts, modeled separately for close ties and acquaintances. About three quarters are zeros. Each occupation has an ISEI score, grouped into high, middle and low status.

**SEÑALAR.** Tabla de 27 ocupaciones a la derecha: solo apunta a un ejemplo por columna (Doctors 89, Electricians 43, Farmers 16).

**CIFRAS.** N = 1,124 · 41 comunas · 30,348 díadas · ceros: 75,9% (cercanos) y 74,9% (conocidos) · alto ≥ 66, medio 41–65, bajo ≤ 40.

---

## 8 · Distance between ego and each occupation (Ignacio, 1:30)

**DECIR.** Each ego has two reference positions: destination, the ISEI of their own occupation, and origin, the ISEI of the household head at fifteen. Distance is absolute, in tens of ISEI points, from each anchor. Both go in the model together, so each is estimated net of the other. Reading a coefficient: it is multiplicative. Minus 0.189 means 17 percent fewer contacts per ten points, and 43 percent fewer at thirty, not three times 17.

**SEÑALAR.** Figura de la izquierda, de abajo hacia arriba: mismo ego ilustrativo (contador cuyo jefe de hogar era vendedor). Abogados: 38 puntos desde el destino, 54 desde el origen. Guardias: 20 desde el destino, 4 desde el origen. Luego el recuadro de lectura del coeficiente (¡lento!).

**PASAR.** "Next, the model that uses these distances."

---

## 9 · From baseline segregation to the covariate model (Ignacio, 1:45)

**DECIR.** Baseline: if everybody had the same chance of knowing anyone, counts would be Poisson. When the chance varies across people, counts are overdispersed by a factor omega: one is random mixing, above one is segregation. The covariate model adds what we observe: sex, education and age, plus the two distances. The overdispersion that remains is omega prime. Since occupation size and sociability are controlled, each distance coefficient is homogeneity relative to contact opportunity. Estimation is Bayesian, in Stan, separately for each tie type.

**SEÑALAR.** Tabla pequeña de la derecha: columna "Barrier effects" = segregación total (ω); columna "Covariate model" = segregación que queda sin explicar (ω′). La fórmula del modelo solo se nombra; no se lee.

**CIFRAS.** 4 cadenas × 2.000 iteraciones · R-hat ≤ 1,01 · sin divergencias · priors débiles normal(0, 1) en los β.

---

## 10 · Two quantities (Ignacio, 0:45)

**DECIR.** Two quantities summarize what the covariates explain. The explained proportion is omega minus omega prime, over omega minus one: zero is nothing explained, one is everything. The unique contribution of a block drops one anchor and asks how much the explained proportion falls: that is how we compare destination and origin. Omega is not comparable in level between close ties and acquaintances, so we only use these ratios.

**SEÑALAR.** Barra: residual (ω′ − 1) en azul oscuro, explicado (ω − ω′) en celeste; ejemplo ω = 3, ω′ = 2,2, ω_prop = 0,40.

---

## 11 · Coefficients: contacts decline with distance from both anchors (Ignacio, 2:00)

**DECIR.** Each dot is the change in the log contact rate per ten points of distance; left of the dashed line means fewer contacts. All four intervals exclude zero: origin matters in both tie types, it is never zero. Close ties decline faster than acquaintances from both anchors: 17 against 9.5 percent from destination, 13 against 8 from origin. And destination weighs more than origin only among close ties; among acquaintances we cannot tell them apart.

**SEÑALAR (orden).**
1. Línea punteada en 0: a la izquierda = menos contactos. Rojo = lazos cercanos, azul = conocidos.
2. Fila de arriba (DESTINO): rojo −0,189 (−17,2%), azul −0,100 (−9,5%).
3. Fila de abajo (ORIGEN): rojo −0,141 (−13,1%), azul −0,087 (−8,4%).
4. Compara rojo con azul dentro de cada fila (tipo de vínculo): cercanos caen más.
5. Compara los dos rojos (destino vs origen): diferencia 0,049, IC [0,017; 0,081], prob. 0,999. Compara los dos azules: 0,012, IC [−0,019; 0,044], prob. 0,79.

**CIFRAS a 30 puntos.** Cercanos: −43,3% (destino), −34,4% (origen). Conocidos: −25,8% y −23,0%. Tipo de vínculo: destino −0,090 [−0,119; −0,061]; origen −0,054 [−0,081; −0,027].

**FRASE CLAVE.** "Current position organizes similarity more than origin does, but only among close ties; origin matters in both tie types."

---

## 12 · Origin keeps pulling contacts even when destination changes (Ignacio, 1:45)

**DECIR.** This shows the model's implications for three ego profiles. Diamond is destination, circle is origin; the dashed line is what we would see without distance. High origin, high destination: contacts pile up at the top. Low and low: at the bottom. The key row is the mobile one: low origin, high destination keeps a peak at its origin and another at its destination. Same destination, a low instead of high origin cuts high-status contacts from 54 to 32 percent. Origin is not a residue of destination.

**SEÑALAR (orden; la figura aparece junto con el primer punto).**
1. Leyenda: ◆ navy = destino; ○ rojo = origen; si coinciden, se superponen. Sólida = predicción; punteada = sin términos de distancia. Columna izquierda cercanos; derecha conocidos.
2. Fila 1 (alto–alto): línea sólida sobre la punteada en ISEI ≈ 72 y 87 (pico ≈ 30%); por debajo en el extremo bajo.
3. Fila 3 (bajo–bajo): imagen espejo; pico ≈ 40% cerca de ISEI 27; arriba vacío.
4. Fila 2 (origen bajo, destino alto): conserva el pico en el origen (≈ 27, ≈ 20%) y los del destino (≈ 72).
5. Compara fila 1 con fila 2 (mismo destino, otro origen) = papel del origen; fila 2 con fila 3 (origen similar, otro destino) = papel del destino.

**CIFRAS (cercanos, proporción de contactos alto/medio/bajo).** Alto–alto 54/29/17 · bajo–alto 32/34/34 · bajo–bajo 10/27/64 · referencia sin distancia 29/32/40. Conocidos: 37/34/29 · 25/35/41 · 13/30/57 · ref. 24/33/43. Mismo destino alto, origen bajo en vez de alto: alto 54→32, bajo 17→34. Origen bajo, destino alto en vez de bajo: bajo 64→34, alto 10→32.

**CUIDADO (decir solo si preguntan, pero ten claro).** Es una implicación del modelo, no una prueba independiente: las pendientes son comunes a todos los egos. El perfil móvil queda cerca de la punteada porque, para un ego entre ambos anclajes, la distancia al destino más la distancia al origen es constante: los dos tirones se compensan. Las ondulaciones salen de suavizar 27 ocupaciones discretas (kernel gaussiano, ancho 3). Las bandas reflejan solo incertidumbre en β y baselines.

**PASAR.** "That was homogeneity, at the ego level. Now segregation, at the level of access to occupations."

---

## 13 · All 27 occupations are segregated (Ignacio, 1:15)

**DECIR.** Now overdispersion by occupation, ordered by status. One is random mixing, and every occupation sits above it, in both tie types. The most segregated are at both ends: farmers, 3.0, and professors, 2.7, among close ties. The least: everyday trades and services, such as electricians, 1.1. Covariates, in red, reduce omega mostly at the top: lawyers fall from 2.4 to 1.7. At the bottom, the red dot sits on the blue.

**SEÑALAR (orden).**
1. Línea punteada en ω = 1 (mezcla aleatoria): todos los puntos a su derecha. Azul = sin covariables (ω), rojo = con covariables (ω′).
2. Panel de cercanos, abajo: electricistas, el punto más cerca de la línea (1,11; IC 1,03–1,21).
3. Extremos de cada panel: alto (médicos, profesores universitarios, altos funcionarios) y bajo (agricultores, vendedores ambulantes, repartidores) con ω más alto. Mitad: oficios y servicios cotidianos poco segregados (electricistas, mecánicos, contadores, guardias), pero profesoras/es, carabineros y enfermeras/os sí lo son.
4. Compara azul y rojo en la banda alta: abogados 2,44→1,66; médicos 2,60→2,04; ingenieros 1,91→1,35. En la banda baja el rojo cae sobre el azul (agricultores 3,04→3,06).

**CIFRAS (cercanos).** Agricultores 3,04 · vendedores ambulantes 3,00 · profesores básica/media 2,90 · profesores universitarios y altos funcionarios 2,74 · médicos 2,60. Conocidos: profesores univ. 5,77, agricultores 4,32.

**NO HACER.** No leer fila por fila. **Advertir:** los niveles de ω no son comparables entre paneles; se lee la forma de cada perfil.

---

## 14 · Close ties show a U-shape by status (Ignacio, 0:45)

**DECIR.** The previous figure by status. Among close ties we see a U-shape: high 2.4, middle 1.9, low 2.0. Middle strata are the least segregated, a point of contact between the extremes. Among acquaintances only the top stands out. With covariates the profile flattens, mainly at the top, and the explained share is largest there: 0.39 against 0.12 at the bottom.

**SEÑALAR.** Columna "Baseline" (2,44 / 1,85 / 2,04); columna "Covariates" (1,90 arriba); última columna "Explained" (0,39 · 0,16 · 0,12; conocidos 0,23 · 0,07 · 0,03).

**SI PREGUNTAN.** Conocidos, bajo vs medio (2,76 vs 2,75): con corte por terciles, bajo sí supera a medio (2,91 vs 2,46); la conclusión es sensible al corte.

---

## 15 · Distance and ego traits explain about 20% (Ignacio, 1:15)

**DECIR.** This is the explained share by occupation. On average, distance and ego traits explain about 20 percent of the excess overdispersion among close ties, 10 percent among acquaintances. Most segregation stays unexplained. It is highest at the top: engineers 0.61, lawyers 0.54. And the unique contributions: among close ties, destination adds 0.033 and origin 0.018; among acquaintances both are below 0.01, we cannot tell them apart.

**SEÑALAR (orden).**
1. Línea punteada en cada panel = promedio (0,20 y 0,10).
2. Arriba del panel de cercanos: ingenieros 0,61, abogados 0,54, gerentes 0,44, arquitectos y médicos 0,35. Abajo: carabineros y comerciantes ≈ 0,06; agricultores ≈ 0 (negativo = nada explicado).
3. Los dos paneles se parecen (r = 0,80); la proporción es mayor en cercanos en 24 de 27 ocupaciones.
4. Contribución única (no está en la figura): destino 0,033 vs origen 0,018; destino mayor en 15 de 27, origen en 12 (conocidos: 0,004 y 0,007).

**CIFRAS por ocupación (Δω_prop, cercanos).** Destino > origen: abogados 0,190 vs 0,004; ingenieros 0,096 vs −0,009; mecánicos 0,074 vs 0,014. Origen > destino (origen vs destino): auxiliares de aseo 0,074 vs 0,014; arquitectos 0,071 vs 0,012; altos funcionarios 0,033 vs −0,006.

**PASAR.** "So distance in status anchors contacts, but explains a modest part of segregation. Let me summarize."

---

## 16 · Preliminary answers (Ignacio, 1:15)

**DECIR.** Three answers. One, homogeneity: contacts fall with distance from both anchors; origin is not a residue of destination. Destination weighs more only among close ties. Two, segregation: every occupation is segregated, most at both ends among close ties; distance and traits explain about 20 percent for close ties and 10 for acquaintances, mostly at the top. Three, close ties are more homogeneous and their segregation is more explained. All preliminary; next steps: slopes by mobility group, separating family from friends, and more covariates.

**PASAR.** "Gabriel will say what we make of the large unexplained part."

---

## 17 · If status similarity explains little, access barriers have other sources (Gabriel, 1:15)

**DECIR.** If status distance explains only a fifth of segregation, access is organized by something else: where people live and study, the organizations that bring them together, class-specific socialization, and the size of groups. A literature that reads segregation as similarity in status, from origin or from destination, may underestimate those sources. The middle strata work as a point of contact, though not all of them. And origin keeps a role net of destination. The open question: which settings produce the segregation that status distance does not explain?

---

## 18 · Thank you

Agradecer; mencionar el financiamiento (ANID/FONDECYT 11240249). Si hay preguntas, saltar al apéndice según el tema (ver tabla abajo).

---

## 19 · Appendix A: why one coefficient per anchor (en reserva)

**DECIR.** Signed distance to an occupation equals distance up minus distance down, and it is additive in ego's position and in the occupation. Ego sociability and occupation baselines already absorb those terms. What is identified is the average slope; the difference between upward and downward slopes comes from the prior, not the data. So we do not claim a "social ceiling". Substantive results are unchanged: omega-prop correlates 0.9998 across specifications. Caveat: close ties mix family and friends, so shared origin may be kinship; read the gap as an upper bound.

## 20 · Appendix B: reading the explained share with care (en reserva)

**DECIR.** Three cautions. Omega scales with the average count, so we never compare levels across tie types. The ratio is unstable when omega is near one. And absolute distance folds the ISEI scale, so distance may explain more at the extremes for geometric reasons; we have not yet checked it, and the bottom occupations, also extreme, are poorly explained, so geometry is not the whole story.

---

# Dónde ir según la pregunta

| Si preguntan por… | Ir a la diapo |
|---|---|
| ¿Origen es solo un proxy de destino? | 12 (perfiles) y 11 (coeficientes) |
| Movilidad ascendente vs descendente | 19 (Apéndice A) |
| Relación "mecánica" de la sobredispersión | 20 (Apéndice B) y 10 |
| Diferencia entre homogeneidad y segregación | 4 |
| Cercanos vs conocidos | 11 y 15 |
| Ocupaciones específicas | 13 y 15 |

---

# Q&A: preguntas probables y respuestas

Convención: **[G]** responde Gabriel (teoría), **[I]** Ignacio (método). Respuestas en inglés, 30–60 palabras.

## A. Origen y destino

**A1. "Isn't origin just a proxy for destination?" [I]**
*Idea:* ambos entran juntos; cada coeficiente es neto del otro; y el del origen es conservador.
*Answer:* Both distances enter the model together, so each coefficient is net of the other. The origin coefficient is, if anything, conservative: part of origin's effect probably operates through destination (origin shapes where people end up), and that mediated part is absorbed by destination. So the net origin role we report is a lower bound of its total role. [Confirmar la correlación ISEI origen–destino antes de hablar; no está en las tablas de la presentación.]

**A2. "Why would destination weigh more in close ties, if close ties include family?" [G]**
*Idea:* sorprende a favor de destino aun con familia; mecanismos son hipótesis.
*Answer:* Family would favor origin, so finding that destination weighs more in close ties is notable. Contemporary exposure (work, neighborhood, school of one's children) is a plausible mechanism, but we do not test it. We cannot yet separate family from friends; that is our next step.

**A3. "For whom does destination matter?" [I]**
*Idea:* sí por tipo de vínculo y por ocupación; por perfil de ego, no con estos datos.
*Answer:* By tie type, yes: the destination gradient is steeper in close ties (probability 0.999), not in acquaintances (0.79). By occupation, yes: destination adds more for lawyers and engineers; origin for cleaners, architects and senior officials. By ego group, not yet: slopes are common to all egos, so the profile figure is a model implication. Testing it needs group-specific slopes, for example by mobility group. That is the next step.

**A4. "Is the 'mobile keeps both anchors' result real or built into the model?" [I]**
*Answer:* It is an implication of the model: with one slope per anchor, for an ego between the two anchors the sum of both distances is constant, so the pulls offset each other and the curve stays close to the no-distance line. We present it as what the estimates imply, not as independent evidence of compensation.

**A5. "Does origin matter because of family ties, i.e., kinship?" [I]**
*Answer:* Partly, in close ties; that is why we flag the close-tie gap as an upper bound on selective similarity. But origin also matters among acquaintances (−8.4% per ten points, interval excludes zero), where kinship is not the story.

## B. Confusores y variables omitidas

**B1. "What about confounders: income, neighborhood, education, religion?" [I]**
*Idea:* lo que absorbe α_i y lo que no; lista de variables pendientes.
*Answer:* Anything that varies only by ego (general sociability, overall network size, say) is absorbed by the ego term, and anything that varies only by occupation by the occupation baseline. A confounder has to vary by ego and by occupation together, such as education matching occupation, residence, or gender composition. We control sex, education and age with occupation-specific effects. Not yet: income, children and partner, municipality size, religion or politics. They are in the next version.

**B2. "ISEI already contains education and income; isn't distance just educational distance?" [I]**
*Answer:* ISEI is built from education and income, so distance in ISEI partly carries both. We control ego's education with occupation-specific effects, so the distance coefficient is net of ego's own education level. We do not separate dimensions of status; a multidimensional distance (class, education, income) is a natural extension.

**B3. "Why ISEI and not social class?" [I/G]**
*Answer:* ISEI gives a continuous, comparable scale for all 27 occupations, which is what a distance needs. Classes would give categories and no natural distance. We acknowledge a single status dimension as a limit; a class-based version is a sensitivity analysis we would like to do.

**B4. "How good is origin as measured, household head at fifteen?" [I]**
*Answer:* It is retrospective and one-dimensional: the head's occupation, not education or wealth, and recall at fifteen. Measurement error would attenuate the origin coefficient, so, again, the origin role is conservative.

## C. Endogeneidad y causalidad

**C1. "Isn't this endogenous? Networks help people get jobs, so destination depends on contacts." [I]**
*Idea:* sí, es transversal; origen está predeterminado, destino no; interpretamos asociaciones.
*Answer:* Yes. The design is cross-sectional and we claim associations, not causal effects. Origin is predetermined at fifteen, so it is less exposed to reverse causation; destination is not: contacts may help people reach their position. Position generators cannot separate the two. We read the destination coefficient as association, and that is a reason to give weight to the origin result.

**C2. "Selection into ties: do people choose similar others or are they constrained?" [G]**
*Answer:* We cannot separate choice from constraint with these data: homogeneity reflects both preferences and opportunity structure. What we do is control for occupation size and sociability, so the coefficients are homogeneity relative to opportunity. Constraint (residential, school, workplace) is exactly where we think the unexplained 80–90 percent comes from.

**C3. "Do you claim distance causes segregation?" [I]**
*Answer:* No. We measure how much of the overdispersion is statistically accounted for by distance and traits. About 20 percent among close ties, 10 among acquaintances; the rest is open.

## D. Sobredispersión y relación mecánica

**D1. "Isn't the overdispersion mechanically related to the covariates, or to the number of contacts?" [I]**
*Idea:* tres puntos (apéndice B).
*Answer:* Three points. First, omega scales with the average count, so we never compare levels across tie types or occupations; we use ratios. Second, the ratio omega-prop divides by omega minus one, so it is unstable for occupations near random mixing, and we do not interpret those individually. Third, absolute distance folds the ISEI scale: occupations at the extremes get more variation in distance across egos than middle ones, so part of "more explained at the top" could be geometry. We have not checked it yet, and low-status occupations are also extreme but poorly explained.

**D2. "Could the overdispersion come from excess zeros, with 75% zeros?" [I]**
*Answer:* The model treats zeros through the negative binomial and the occupation baselines; we have not estimated a zero-inflated alternative, and we list it as a robustness check. Comparisons of omega with omega prime use the same model, so the ratio is internally consistent.

**D3. "Why are the delta contributions so small (0.03, 0.02) when the betas are large?" [I/G]**
*Idea:* niveles distintos (puente con Gabriel).
*Answer:* Because they answer different questions at different levels. The betas are ego-level: how strongly distance shapes each person's contacts. The delta is access-level: how much of the concentration of contacts in an occupation, across egos, is organized around that anchor. An anchor can matter a lot for each person and still explain little of the cross-ego concentration if there are other settings that group people.

**D4. "Why are close-tie and acquaintance omegas so different (2.4 vs 3.5 at the top)?" [I]**
*Answer:* Omega scales with the mean number of contacts, so levels are not comparable. We compare through omega-prop and the shape of each profile.

## E. Diseño, datos y estimación

**E1. "Why can't you say whether contacts fall faster upward than downward?" [I]**
*Answer:* Because signed distance is additive in ego's position and in the occupation, and the model already has an ego term and an occupation term. The difference between upward and downward slopes is not identified; it would be set by the prior. Details in Appendix A. Results for segregation are essentially the same (omega-prop correlation 0.9998 across specifications).

**E2. "Sample size and representativeness?" [I]**
*Answer:* 1,124 adults, 41 communes of the Santiago metropolitan region, probabilistic, multistage, stratified, face to face. So the results speak for Santiago, not for Chile. [Confirmar si se usan ponderadores en la estimación.]

**E3. "Priors and convergence?" [I]**
*Answer:* Weakly informative, normal(0, 1) on the distance coefficients. Four chains of 2,000 iterations, no divergences, R-hat at most 1.01. We report posterior means and 95% credible intervals, and posterior probabilities for comparisons.

**E4. "Why Bayesian?" [I]**
*Answer:* The covariate model of Baum estimates overdispersion per occupation with hierarchical structure; in Stan we get full posteriors for omega, omega-prime and the derived ratios, with no extra approximation for the uncertainty.

**E5. "Position generator and recall: do people over- or under-report?" [I]**
*Answer:* Yes, counts come from self-report and "knowing" is subjective, so noise and heaping are possible. It affects levels more than comparisons across occupations or anchors within the same instrument.

## F. Interpretación y política

**F1. "What are the implications?" [G]**
*Answer:* If origin keeps a role net of destination, then mobility does not erase inherited network advantage or disadvantage: people who move up carry part of their origin's network with them. And since status distance explains little of the segregation, interventions that only mix people by status will miss the settings where segregation arises: neighborhoods, schools, organizations.

**F2. "Why does the middle look less segregated?" [G]**
*Answer:* It echoes Chilean evidence that middle classes hold the most heterogeneous networks, and could bridge the edges. But not all middle occupations: teachers, police and nurses are highly overdispersed, while everyday trades and services are close to mixing. We read it as a hypothesis to examine further.

**F3. "Is Chile special?" [G]**
*Answer:* Chile is a demanding case: high inequality, low mobility, strong residential and school segregation. If origin and destination can be told apart here, it is likely a feature of other stratified societies; comparison with other countries is the next step.

---

# Hoja de cifras rápida

**Coeficientes (por 10 puntos ISEI).** Cercanos: destino −0,189 (−17,2%), origen −0,141 (−13,1%). Conocidos: destino −0,100 (−9,5%), origen −0,087 (−8,4%). Todos con IC que excluyen 0.
**Contrastes.** Destino vs origen: cercanos 0,049 [0,017; 0,081], prob. 0,999; conocidos 0,012 [−0,019; 0,044], prob. 0,79. Cercanos vs conocidos: destino −0,090, origen −0,054, prob. ≈ 1.
**Omega por estatus (cercanos).** Alto 2,44→1,90 (0,39) · medio 1,85→1,72 (0,16) · bajo 2,04→1,93 (0,12). **Conocidos.** 3,48→2,94 (0,23) · 2,75→2,60 (0,07) · 2,76→2,70 (0,03).
**ω_prop promedio.** 0,20 (cercanos), 0,10 (conocidos). Residual promedio: 0,85 y 1,73 puntos.
**Δω_prop promedio.** Cercanos: destino 0,033, origen 0,018. Conocidos: 0,004 y 0,007.
**Perfiles (cercanos, alto/medio/bajo).** 54/29/17 · 32/34/34 · 10/27/64 · ref. 29/32/40.

---

# Pendientes por confirmar antes de imprimir

1. Correlación entre ISEI de origen y de destino (para A1).
2. Si la estimación usa ponderadores muestrales (E2).
3. La diapo 3b (extra de Gabriel): ajustar el texto del guión a lo que finalmente pegaste.
4. Chequeo de la "componente geométrica" (Apéndice B): varianza de la distancia entre egos por ocupación vs ω_prop. Si no alcanzas a hacerlo, deja la frase como límite abierto.
