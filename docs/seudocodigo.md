# Seudocódigo - Análisis de Tiempos de Espera y Causas de Inasistencia
**Proyecto:** MediSchedule  
**Asignatura:** Programación con Estructuras de Datos  
**Semana 3 - 2026**

## Descripción del problema
Los pacientes de clínicas en Granada y Diriomo esperan demasiado tiempo y muchos faltan a sus citas.  
Este algoritmo analiza 10 pacientes para calcular estadísticas de espera y causas de inasistencia, y genera recomendaciones automáticas.

## Seudocódigo

INICIO

1. DEFINIR los datos de los 10 pacientes:
   - Lista de tiempos de espera
   - Lista de asistencia (Sí / No)
   - Lista de causas de inasistencia

2. FUNCIÓN validar_datos(tiempos):
   - PARA cada tiempo en la lista:
       - SI el tiempo no es un número o es menor o igual a 0 ENTONCES
           - LANZAR error "Dato inválido"
   - RETORNAR verdadero si todos son válidos

3. FUNCIÓN calcular_estadisticas(tiempos):
   - Calcular la media (promedio) de los tiempos
   - Calcular la mediana
   - Contar cuántos pacientes esperaron más de 30 minutos
   - Calcular el porcentaje que esperó más de 30 minutos
   - RETORNAR media, mediana, cantidad y porcentaje

4. FUNCIÓN analizar_causas(asistencias, causas):
   - Contar cuántos faltaron por "Olvido"
   - Contar cuántos faltaron por "Dificultad para comunicarse"
   - Contar cuántos faltaron por otras causas
   - RETORNAR los contadores

5. FUNCIÓN generar_recomendaciones(porcentaje_espera, causas):
   - SI el porcentaje de espera > 50% ENTONCES
       - Mostrar recomendación: "Implementar recordatorios automáticos y mejorar gestión de agendas"
   - SI hay muchas faltas por olvido ENTONCES
       - Mostrar recomendación: "Enviar recordatorios por SMS o WhatsApp 24 horas antes"
   - SI hay faltas por comunicación ENTONCES
       - Mostrar recomendación: "Permitir cancelación y reprogramación fácil desde la aplicación"
   - RETORNAR las recomendaciones

6. FUNCIÓN principal():
   - INTENTAR (try):
       - Llamar a validar_datos()
       - Llamar a calcular_estadisticas()
       - Llamar a analizar_causas()
       - Llamar a generar_recomendaciones()
       - Mostrar todos los resultados de forma clara
   - CAPTURAR (except) cualquier error:
       - Mostrar mensaje de error amigable

7. LLAMAR a la función principal()

FIN