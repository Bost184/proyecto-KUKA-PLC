# Conectividad PLC Siemens - Robot KUKA

Proyecto de integración de una célula robotizada utilizando un PLC Siemens S7-1200 como maestro y un robot KUKA (KSS) para tareas de paletizado y descarte.

## 🛠️ Tecnologías y Materiales
- **PLC:** Siemens S7-1200 (TIA Portal)
- **Robot:** KUKA KSS (EthernetKRL / PROFINET)
- **Comunicación:** Buses industriales y E/S digitales

## 🚀 Fases de Desarrollo
1. **Configuración:** Comunicación GSDML en TIA Portal.
2. **Mapeo:** Sincronización de señales de inicio, parada y selección de programa.
3. **Lógica KRL:** Programación del robot con esperas de señales ($IN / $OUT).
4. **Seguridad:** Pruebas de parada de emergencia sincronizada.

## 📈 Niveles de Implementación
- **Básica:** Control por señales digitales (24V).
- **Intermedia:** Comunicación PROFINET (Intercambio de Bytes).
- **Avanzada:** Datos complejos vía EthernetKRL.