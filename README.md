
    ```mermaid
graph TD
    A[Inicio] --> B[Listar Interfaces de Red]
    B --> C{¿Interfaz Seleccionada?}
    C -- Sí --> D[Configurar modo promiscuo]
    D --> E[Loop de Captura]
    E --> F{¿Llega paquete?}
    F -- Sí --> G[¿Cumple filtro?]
    G -- Sí --> H[Desglosar Cabeceras L2, L3, L4]
    H --> I[Mostrar en pantalla]
    I --> E
    G -- No --> E
    F -- No --> E
    E --> J[Detener Captura]
    J --> K[Guardar archivo PCAP]
    K --> L[Fin]
```
