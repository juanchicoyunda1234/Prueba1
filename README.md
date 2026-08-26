classDiagram 
    class Vehiculo { 
        #String placa 
        #String marca 
        #String modelo 
        #int anio 
        #double precio 
        #boolean disponible 
        +mostrarInformacion()* 
    } 
    class Automovil { 
        -int numeroPuertas 
        -boolean electrico 
        +mostrarInformacion() 
    } 
    class Motocicleta { 
        -int cilindrada 
        -boolean tieneMaletero 
        +mostrarInformacion() 
    } 
    class RegistroVehiculos { 
        -Vehiculo[] vehiculos 
        -int cantidad 
        +registrar(Vehiculo) boolean 
        +mostrarTodos() 
    } 
    Vehiculo <|-- Automovil 
    Vehiculo <|-- Motocicleta 
    RegistroVehiculos o-- Vehiculo 
