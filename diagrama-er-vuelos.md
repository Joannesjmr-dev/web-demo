erDiagram
    AEROPUERTO ||--o{ PROGRAMA_VUELO : "tiene"
    AEROPUERTO ||--o{ ATERRIZAJE : "recibe"
    AEROPUERTO ||--o{ DESPEGUE : "realiza"
    AEROPUERTO }|--|| CIUDAD : "está en"
    AEROPUERTO }|--|| PAIS : "está en"
    AEROPUERTO ||--o{ MODELO_AVION : "puede recibir"
    PROGRAMA_VUELO ||--|{ VUELO : "genera"
    PROGRAMA_VUELO }|--|| LINEA_AEREA : "pertenece a"
    PROGRAMA_VUELO ||--o{ ESCALA_TECNICA : "puede tener"
    VUELO }|--|| MODELO_AVION : "utiliza"
    
    AEROPUERTO {
        string codigo PK
        string nombre
    }
    
    PROGRAMA_VUELO {
        string numero_vuelo PK
        string[] dias_semana
    }
    
    VUELO {
        date fecha
        int plazas_vacias
    }
    
    MODELO_AVION {
        string modelo PK
        int capacidad
    }
    
    CIUDAD {
        string nombre PK
    }
    
    PAIS {
        string nombre PK
    }
    
    LINEA_AEREA {
        string nombre PK
    }
    
    ESCALA_TECNICA {
        int orden
    }
