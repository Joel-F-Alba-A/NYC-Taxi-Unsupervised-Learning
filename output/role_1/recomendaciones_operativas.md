## Recomendaciones operativas basadas en esta ejecución

1. **Concentración espacial.** Las 7 celdas principales (de 64) reúnen 98.5% de las recogidas limpias; entre las tres primeras están R05C02, R06C03, R05C03. Considerarlas como candidatos de staging y contrastar esa cuota con la capacidad disponible antes de mover flota.

2. **Cobertura horaria.** El mayor volumen ocurre a las 18:00 (6.3% de los viajes); el máximo por tipo de día es 20:00 en laborables y 18:00 en fin de semana. Alinear disponibilidad y relevos con esos picos observados.

3. **Incertidumbre de ubicación.** Pico mañana (07-09) presenta 2.165 bits/viaje y Valle (00-05), 1.880 bits/viaje. Mantener mayor flexibilidad de posicionamiento en la franja más incierta; comprobar el efecto con tiempos de espera, que este dataset no mide.

4. **Planes por tipo de día.** Usar el perfil laboral en fin de semana tiene D_KL=0.0184 bits/viaje y entropía cruzada 2.1689, frente a H(fin de semana)=2.1506 bits/viaje. Mantener perfiles diferenciados si esa discrepancia informativa justifica operar dos planes; no equivale directamente a costo monetario.

5. **Calidad y ruido.** El filtro de recogidas excluye 0.000% de orígenes fuera de NYC; 0.016% de destinos y 0.328% de duraciones fuera de rango se reportan por separado. Con ruido, H(origen) cambia +0.0000, H(destino) +0.0018, I(hora;origen) +0.0000 e I(hora;destino) +0.0003 bits/viaje. Conservar estas validaciones antes de interpretar variaciones de mapa como cambios reales de demanda.

6. **Dotación diaria.** H(Demanda | tipo de día)=1.5584 bits/día en tres niveles definidos con terciles del entrenamiento; usar esta incertidumbre para evitar dotaciones rígidas sin contrastar más días.
