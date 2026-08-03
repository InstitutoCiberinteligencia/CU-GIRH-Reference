<p align="center">
  <img src="assets/Oneiros-light-horizontal.png" alt="Oneiros Academy" width="420">
</p>

<h1 align="center">CU-GIRH Reference</h1>

<p align="center">
  <em>Índice navegable de los General Intelligence Requirements (CU-GIRH v7.0) y guía en español para convertirlos en PIRs, EEIs y planes de obtención.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CU--GIRH-v7.0-7FD4B4">
  <img src="https://img.shields.io/badge/GIRs%20indexados-513-92CDE6">
  <img src="https://img.shields.io/badge/Uso-educativo-5FBF9E">
  <img src="https://img.shields.io/badge/Fuente-Intel%20471-6FC9C2">
  <img src="https://img.shields.io/badge/Oneiros-Academy-6FC9C2">
</p>

---

> ### ⚠️ Esto no es el CU-GIRH
>
> Este repositorio **no reproduce** el *Cyber Underground General Intelligence Requirements Handbook*. Contiene un **índice de códigos y títulos** para navegación e interoperabilidad, más **material propio en español** sobre cómo usar la taxonomía en Dirección de Inteligencia.
>
> Las definiciones y los **Elementos Esenciales de Información (EEIs)** de cada GIR son contenido autoral de Intel 471 y se citan por número de página, no se transcriben. El handbook completo se descarga gratuitamente desde la fuente oficial:
>
> ### 👉 **<https://www.intel471.com/cyber-underground-handbook>**

## ¿Qué es el CU-GIRH?

Es la taxonomía de requerimientos de inteligencia publicada por **Intel 471**: un catálogo estructurado de las preguntas que una organización se hace recurrentemente sobre el cibercrimen. Cada GIR incluye una definición y los elementos esenciales de información necesarios para responder quién, qué, cuándo, dónde, por qué y cómo.

Su utilidad práctica es que **convierte una conversación difusa con un stakeholder en una lista priorizable**. En vez de preguntar *"¿qué necesitas saber?"* —pregunta que suele producir un silencio incómodo o una respuesta inabarcable— le pides que seleccione y rankee hasta 10 GIRs de un catálogo cerrado. Esa lista ordenada es su conjunto de PIRs.

## Contenido del repositorio

| Archivo | Qué contiene |
|---------|--------------|
| [`GIR-INDEX.md`](GIR-INDEX.md) | Índice completo de las 6 familias y sus 513 códigos, con notas de uso por familia |
| [`LICENSE`](LICENSE) | Licencias aplicables: contenido de Intel 471 y material propio |

## Cómo se lee un código GIR

La numeración es jerárquica y las subcategorías **heredan** atributos y EEIs de su categoría padre:

```
1          Familia          MALWARE
1.1        Categoría        Malware variants
1.1.1      Subcategoría     Ransomware malware
```

Un requerimiento formulado sobre una hoja del árbol es más específico —y por lo tanto más obtenible— que uno formulado sobre la raíz. `1.1` obliga al analista a buscar "todo sobre malware"; `1.1.1` acota a ransomware.

## Las seis familias

| # | Familia | Pregunta que acota |
|---|---------|--------------------|
| 1 | Malware | ¿Qué se ejecuta? |
| 2 | Vulnerabilidades y exploits | ¿Por dónde entra? |
| 3 | Infraestructura maliciosa | ¿Desde dónde opera? |
| 4 | Fraude, identidad y acceso | ¿Cómo se monetiza? |
| 5 | Tácticas del adversario | ¿Cómo se comporta? |
| 6 | Industria o región | ¿A quién afecta? |

La familia 6 no se prioriza sola: **acota** a las demás. Un GIR geográfico aislado produce un requerimiento inobtenible; combinado (`1.1.1` + `6.1.3.1` + `6.2.8`) produce una pregunta que un equipo de obtención puede responder.

## Del GIR al plan de obtención

El GIR es el punto de partida, no el destino. La cadena completa:

```
GIR  →  PIR/EEI  →  CMF  →  ICP / IAP
```

| Etapa | Qué hace |
|-------|----------|
| **GIR** | Define el dominio permanente de interés |
| **PIR** | Convierte el dominio en una pregunta priorizada con plazo |
| **EEI** | Descompone la pregunta en datos observables concretos |
| **CMF** | Valida si existe visibilidad para responder |
| **ICP / IAP** | Organiza la búsqueda, o habilita la capacidad que falta |

Para practicar esta cadena con un caso real, este repositorio tiene un laboratorio complementario: **[GIR + CCIRM Lab](https://github.com/InstitutoCiberinteligencia/GIR-CCIRM)**.

## Talleres relacionados

Esta referencia es la base teórica de una secuencia de tres piezas que se usan en orden:

| Repositorio | Rol en la secuencia |
|-------------|---------------------|
| [Threat Modeling Lab](https://github.com/InstitutoCiberinteligencia/Threat-Modeling) | Identifica el riesgo: produce escenarios de amenaza priorizados |
| [GIR + CCIRM Lab](https://github.com/InstitutoCiberinteligencia/GIR-CCIRM) | Convierte esos escenarios en requerimientos y en un plan de obtención |
| **CU-GIRH Reference** *(este repo)* | Provee la taxonomía que ambos talleres usan como catálogo |

## Correcciones aplicadas al índice

El índice se cotejó contra el PDF v7.0. Se corrigieron tres inconsistencias tipográficas de origen y se completó una sección ausente en catálogos derivados de versiones anteriores:

- `6.1.12.2` Industrial automation industry — aparecía duplicando el código `6.1.12.1`
- `6.1.11.1` Scientific research and development organizations — grafía
- `6.1.7.5` Tenants and occupiers industry — grafía
- `6.2.9.1` a `6.2.9.27` — subcategorías del Caribe, ausentes en algunos catálogos derivados

Si detectas una divergencia frente al PDF oficial, **el PDF manda**. Abre un issue y se corrige.

## Créditos y atribución

La taxonomía **CU-GIRH** es obra de **Intel 471, Inc.**, publicada bajo licencia **CC BY-NC-ND 4.0**. Este repositorio no está afiliado, patrocinado ni respaldado por Intel 471.

El material en español —notas de uso, guía de conversión GIR→PIR y estructura del índice— fue desarrollado por **Oneiros Academy** como apoyo docente para el curso *Cyber Threat Intelligence Operations*.

## Licencia

Este repositorio combina dos licencias. Consulta [`LICENSE`](LICENSE) para el detalle:

- **Códigos, títulos y estructura de la taxonomía:** © Intel 471, Inc. — CC BY-NC-ND 4.0
- **Notas, guía y material docente en español:** © Oneiros Academy — CC BY-NC 4.0

---

<p align="center"><sub>Oneiros Academy · CU-GIRH Reference · Taxonomía © Intel 471, Inc.</sub></p>
