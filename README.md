# Electricidad
Fallos eléctricos 
# Diagnóstico de fallos eléctricos en motos
def diagnosticar_fallo(voltaje_bateria, fusibles_ok, chispa_ok):
    if voltaje_bateria < 12.5:
        return "La batería está descargada. Cárgala o sustitúyela."
    elif not fusibles_ok:
        return "Revisa los fusibles. Posiblemente uno esté quemado."
    elif not chispa_ok:
        return "No hay chispa. Revisa la bobina o el CDI."
    else:
        return "El sistema eléctrico parece estar funcionando correctamente."

# Ejemplo de uso
voltaje = float(input("Introduce el voltaje de la batería: "))
fusibles = input("¿Los fusibles están bien? (sí/no): ").lower() == "sí"
chispa = input("¿Hay chispa en la bujía? (sí/no): ").lower() == "sí"

resultado = diagnosticar_fallo(voltaje, fusibles, chispa)
print(resultado)
