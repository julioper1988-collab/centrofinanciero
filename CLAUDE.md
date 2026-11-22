# Notas del negocio (memoria para Claude)

Datos en Supabase: proyecto `sdpysvowvwucjfnyosuf`, tabla `cf_app_state` (id `main`, JSON en `data`).

## Trabajadores asaditería
- Sueldo: Gs. 100.000 por día trabajado, lunes a sábado (domingos y feriados no cuentan).
- Gastos con `counterparty` del trabajador (categoría Colaboradores) se suman a lo que debe.

### Javier Flores
- Deuda base: Gs. 1.205.000 hasta el 15/09/2026 (en `debts`).
- Desde el 16/09: saldo = deuda − (días trabajados × 100.000) + gastos anotados a Javier.
- 28/09/2026 feriado (no trabajó). Faltó 2 días aparte de feriados y domingos (fechas no especificadas).
- Saldo final al 03/10/2026: **Gs. 525.000** (te debe).
- **Último día: sábado 03/10/2026 (medio día, Gs. 50.000).**

### Germán González
- **Empezó a trabajar el lunes 05/10/2026.**
- Deuda base: Gs. 1.363.000 hasta el 15/09/2026 (en `debts`). Misma regla que Javier: + gastos desde 16/09 − días trabajados desde 05/10.
- Saldo al 22/11/2026: **Gs. 1.152.000** (42 días × 100.000; gastos 3.989.000).

## Días trabajados (fuente)
- Días abiertos de Asaditos: tabla `asaditos_v2_app_state`, `data->'days'`; trabajado = `cash.ef > 0` (misma regla que `conc_diario` en Conciliación).
- Es por negocio, no por persona: faltas individuales no quedan registradas.
- De Conciliación solo se toman los DÍAS trabajados. El sueldo para la deuda es SIEMPRE Gs. 100.000/día (ignorar `conc_config.params`).
