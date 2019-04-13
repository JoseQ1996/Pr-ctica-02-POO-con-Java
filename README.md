# Practica 02-POO en Java

Segunda Practica de Programacion Aplicada realizada por José Quinde

**NOMBRE:** José Quinde

**TITULO PRACTICA:** Enlaces de Clases

**CARRERA:** Computacion

## OBJETIVO ALCANZADO:

El objetivo que se alcanzo fue el poder tener un mayor conocimiento de cómo manejar objetos en java, también se obtuvo el conocimiento de cómo funciona la herencia de la clase padre a la clase hija, así como también se aprendió a utilizar el downcasting que cambiar el tipo de dato de un atributo, y también el instanceof para saber si un objeto pertenece a una clase hija, también se utilizó una lista para poder guardar los datos y después imprimirlos al recorrer la lista.

## ACTIVIDADES DESARROLLADAS

**1.Crear un repositorio en GitHub con el nombre “Práctica 02 – POO con Java”**
-Se procedió a crear un repositorio con los parámetros dados para poder subir la practica 2
 

**2. Sincronizar el repositorio creado con un proyecto en NetBeans. Realizar un commit y push por cada requerimiento de los puntos a continuación descritos (incluir un mensaje que identifique claramente los commits realizados a GitHub).**

-Se realizaron 8 commits en el proyecto

 
**3. Crear un paquete para las clases, otro para las interfaces, otro para las pruebas.**

-Se procedió a crear los tres paquetes el de clases, el de interfaces y el de pruebas
 
**4. Crear una jerarquía de clases de tres niveles, es decir, una clase “abuelo”, dos clases “padres” y cuatro clases “hijas” (dos de cada padre).**

-Para el proyecto la clase abuelo es Vehículo

-Las clases padres son Terrestres y Aéreos

-las clases hijas son Auto, Moto, Avión y Helicóptero
 
**5. Todas las clases deben tener por lo menos cuatros atributos (aparte de los de herencia), tres métodos (aparte de los getters y setters) y método toString().**

**-**	Se implementos en cada clase 4 atributos a continuación se los mostrara
-de la clase abuelo Vehículo. 
 
-de las clases padres Aéreos y Terrestres.
   
-Finalmente de las clases hijas Auto, Moto, Avión y Helicóptero.

**-** También se implementaron 3 métodos y el toString

-los métodos de la clase abuela Vehículo.

    /**
    *Método que imprime un mensaje que el vehículo este prendido
    */
    public void encender(){
        System.out.println("El vehiculo de modelo "+this.getModelo()+" y marca "+ this.getMarca()+" esta encendido");
    }
    /**
    *Metodo que imprime un mensaje que el vehiculo esta apagado
    */
    public void apagar(){
        System.out.println("El vehiculo de modelo "+this.getModelo()+" y marca "+ this.getMarca()+" esta apagado");
    }
    /**
    *Metodo que imprime un mensaje qdel estado del auto 
    */
    public void estado(){
        System.out.println("El vehiculo de modelo "+this.getModelo()+" y marca "+ this.getMarca()+" esta condiciones optimas para su funcionamiento");
    }
    /**
    *toString de la clase Vehiculo
    */
    @Override
    public String toString() {
        return "Vehiculo\n" 
                + "Codigo: " + codigo +
                "\nModelo: " + modelo + 
                "\nMatricula: " + matricula + 
                "\nMarca: " + marca;
    }

-Métodos y toString de las clases padres Terrestres y Aéreos.

**Terrestres**

    /**
    *este metodo nos dice si el vehiculo terrestre va arrancar
    */
    public void arrancar(){
        System.out.println("El vehiculo de modelo "+this.getModelo()+" y tipo de transmision "+this.getTipoTransmision()+" va ha arrancar"); 
    }
    /**
    *este metodo nos dice si el vehiculo terrestre va frenar
    */
    public void frenar(){
        System.out.println("El vehiculo de modelo "+this.getModelo()+" y tipo de transmision "+this.getTipoTransmision()+" va frenar"); 

    }
    /**
    *este metodo nos dice si el vehiculo terrestre va ha disminuir la velocidad
    */
    public void desminuirVelocidad(){
         System.out.println("El vehiculo de modelo "+this.getModelo()+" y tipo de transmision "+this.getTipoTransmision()+" esta disminuyendo la velocidad"); 

    }
    /**
    *to String imprime los datos clase padre Vehiculo y clase hija Terrestres
    */
    @Override
    public String toString() {
        return super.toString()+"\nVehiculo Terrestre\n" 
                + "Numero De Neumaticos: " + numeroNeumaticos + 
                "\nTipo De Transmision: " + tipoTransmision + 
                "\nTipo De Transporte: " + tipoTransporte + 
                "\nVelocidad Maxima: " + velocidadMaxima +" km/h";
    }
    
**Aereos**

    /**
    *Este metodo nos indica que el Vehiculo aereo va ha despegar
    */
    public void despegar(){
        System.out.println("El vehiculo modelo "+this.getModelo()+" y numero de asientos "+this.getNumeroAsientos()+" va ha despegar");
    }
    /**
    *Este metodo nos indica que el Vehiculo aereo va ha aterrizar
    */
    public void aterrizar(){
        System.out.println("El vehiculo modelo "+this.getModelo()+" y numero de asientos "+this.getNumeroAsientos()+" va ha aterrizar");
    }
    /**
    *Este metodo nos indica que el Vehiculo aereo va ha disminuir Altura
    */
    public void disminuirAltura(){
        System.out.println("El vehiculo modelo "+this.getModelo()+" y numero de asientos "+this.getNumeroAsientos()+" va ha disminuir la altura");
    }
     /**
    *to String imprime los datos clase padre Vehiculo y clase hija Aereos
     */
    @Override
    public String toString() {
        return super.toString()+"\nVehiculo Aereo\n" + 
                "Numero De Motores: " + numeroMotores + 
                "\nNumero De Asientos: " + numeroAsientos + 
                "\nElevacion Maxima: " + elevacionMaxima + " m"+
                "\nCarga Maxima: " + cargaMaxima+ " toneladas";
    }


-Métodos y toString de las clases hijas Auto, Moto, Avión y Helicóptero.

**Auto**

    /**
    *Metodo que indica si el auto esta reproducciendo musica
    */
    public void reproduceMusica(){
        System.out.println("El Auto de modelo "+this.getModelo()+" y con traccion "+this.getTipoTranccion()+" esta reproducciendo musica");  
    }
    /**
    *Metodo que indica si el auto esta en Reversa
    */
    public void deReversa(){
        System.out.println("El Auto de modelo "+this.getModelo()+" y con traccion "+this.getTipoTranccion()+" esta de reversa");  
    }
/**
    *toString imprime todos los atributos clase abuelo Vehiculo clase padre Terrestres y clase hija Auto
     */
    @Override
    public String toString() {
        return super.toString()+"\nAuto\n" + 
                "Tipo De Tranccion:" + tipoTranccion + 
                "\nNumero De Puertas: " + numeroPuertas + 
                "\nCilindraje: " + cilindraje + 
                "\nDescapotable: " + descapotable;
    }
    
**Moto**

    /**
    *Metodo que indica si la moto esta en una pista de carrera
    */
    public void enPista(){
        System.out.println("La moto de modelo "+this.getModelo()+"y de altura maxima "+this.getAlturaMaxima()+" esta en pista");
    }
    /**
    *Metodo que indica si la moto esta en carretera normal
    */
    public void enCarretera(){
        System.out.println("La moto de modelo "+this.getModelo()+"y de altura maxima "+this.getAlturaMaxima()+" esta en carretera noraml");
    }
    /**
    *ToString que imprime todos los atributos de la clase abuela Vehiculo, la clase Padre Terrestres y la clase hija Moto
     */
    @Override
    public String toString() {
        return super.toString()+"\nMoto\n" + 
                "Limitador: " + limitador + 
                "\nAltura Maxima: " + alturaMaxima + " m"+ 
                 "\nCapacidad del Sillin:" +capacidadSillin+" personas"+
                "\nLuces:" + luces;
    }
    
**Avión**
  
    
    public void disponibilidad(){
        System.out.println("El avion de modelo "+this.getModelo()+" perteneciente a la Aerolinea "+this.getAerolinea()+" tiene disponibilidad en su vuelo");
    }
    
    /**
    *Metodo que indica que el vuelo tiene escalas
    */
    
    public void vueloConEscala(){
        System.out.println("El avion de modelo "+this.getModelo()+" perteneciente a la Aerolinea "+this.getAerolinea()+" es un vuelo que tiene algunas escalas");
    }
    
    /**
    *Metodo que indica que el vuelo no tiene escalas
    */
    
    public void vueloSinEscala(){
        System.out.println("El avion de modelo "+this.getModelo()+" perteneciente a la Aerolinea "+this.getAerolinea()+" es un vuelo que va directo a su destino sin escalas");
    }
    /**
    *ToString que imprime los atributos de la clase abuelo Vehiculo,de la calase padre Aereos y de la clase hija Avion
     */
    @Override
    public String toString() {
        return super.toString()+"\nAvion\n" 
                + "Aerolinea: " + aerolinea + 
                "\nNumero De Filas: " + numeroFilas + 
                "\nTiempo De Despegue:" + tiempoDespegue + " s" +
                "\nEspacio De Aterrizaje: " + espacioAterrizaje + " m";
    }
    
**Helicóptero**

    /**
    *Metodo que indica si e helicoptero esta en movimiento
    */
    public void enMovimiento(){
        System.out.println("El Helicoptero de modelo "+this.getModelo()+" con el numero de rotores de "+this.getNumeroRotores()+" esta en movimiento");
    }
    /**
    *Metodo que indica si e helicoptero esta en reposo
    */
     public void enReposo(){
        System.out.println("El Helicoptero de modelo "+this.getModelo()+" con el numero de rotores de "+this.getNumeroRotores()+" esta en reposo");
    }
    /**
    *ToString que imprime los atributos de la clase abuelo Vehiculo,de la calase padre Aereos y de la clase hija Helicoptero
     */
    @Override
    public String toString() {
        return super.toString()+"\nHelicoptero\n" + 
                "Velocidad De La Helice: " + velocidadHelice +" km/h"+
                "\nNumero De Rotores: " + numeroRotores + 
                "\nNumero De Helices: " + numeroHelices + 
                "\nAncho De Cabina: " + anchoCabina + " m";
    }
    
**6. Cada clase padre debe tener por lo menos un método abstracto cada una.**
-En las clases padres se implementaron un método abstracto.
-En la clase Terrestres se implementó el método abstracto nivel de Consumo que calcula el consumo de gasolina.

    /**
    *declaracion metodo abstract a implementar en clases hijas devuelve un double
    */
    public abstract double nivelConsumo();
-En la clase Aéreos se implementó el método abstracto que calcula el tiempo de vuelo.
     /**
    *Declaracion metodo abstracto devuelve valor double
    */
    public abstract double tiempoDeVuelo();
    
**7. Los métodos abstractos deben ser sobre-escritos (implementados) en cada clase hija.**
-La implementación de los abstractos en las clases hijas se dio de manera diferente como se lo muestra a continuación.
-En la clase Auto

    /**
    *Metodo abstracto que calculo el nivel de consume de acuero al cilindraje si es Auto de 4 cilindros 1.6 litro en carretera,
    *Auto de 6 cilindros 2,4 litro en carretera ,Auto de 3.2 litro en carretera 
    */
    @Override
    public double nivelConsumo() {
        if(cilindraje==4){
            return 1.6;
        }else if(cilindraje==6){
            return 2.4;
        }else if (cilindraje==8){
            return 3.2;
        }
        return 4.5;
    }
    
-En la clase Moto

    /**
    *Metodo abstracto que devuele el consumo de la Moto sin ningun parametro nos devuelme el consumo promedio de una moto  2,7 litros en 100km 
    */
    @Override
    public double nivelConsumo() {
        return 2.7;
    }
-En la clase Avión
    /**
    *Metodo abstracto que indica el promedio de tiempo de vuelo de un avion devuelve un valor 17,15 es el valor que devuelde ya que es un double
     */
    @Override
    public double tiempoDeVuelo() {
        return 17.15;
    }
    
-En la clase Helicóptero

    /**
    *Metodo abstracto que indica el promedio de tiempo de vuelo de un helicoptero devuelve un valor 14,16 es el valor que devuelde ya que es un double
     */
    @Override
    public double tiempoDeVuelo() {
        return 14.16;
    }


**8. Todas las clases hijas deben ser clases finales.**

-Se procedió a hacer a todas las clases hijas que son Auto, Moto, Avion y Helicoptero
 
 

**9. Crear una interface, con al menos dos métodos abstractos. Estos métodos deben ser implementados en cada clase hija.**

-Se creó dos métodos abstractos en la interface y se los implemento en las clases hijas en este caso se creó los métodos de girar a la derecha y girar a la izquierda.
 
-También se los implemento en todas las clases hijas en este caso mostraremos los ejemplos de la clase Moto y Helicóptero.
 
-Aquí se muestra como se implementa los métodos abstractos en las clases hijas en este caso en la clase Helicóptero.

    /**
    *Método de la clase interface que indica si gira a la derecha
    */
     @Override
    public void girarDerecha() {
        System.out.println("El Helicoptero de modelo "+this.getModelo()+" esta girando a la derecha");
    }
    /**
    *Método de la clase interface que indica que gira a la izquierda
     */
    @Override
    public void girarIzquierda() {
        System.out.println("El Helicoptero de modelo "+this.getModelo()+" esta girando a la izquierda");
    }

**10. Crear una clase “Prueba”, en donde se demostrará el funcionamiento del proyecto. Además, se pide demostrar el uso de downcasting con el operador instanceof. También, se pide demostrar el uso de clases anónimas.**

-En la clase Prueba se ingresó 2 objetos por cada clase hija, y un objeto de la clase anónima.
-También se hizo el downcasting y el instance of.

        /*
        Se recorre la lista tambien se hace el casting y el instance Of para saber a que clase hija pertenece y se imprime
        */
        for (Vehiculo vehiculo : lista) {
            if (vehiculo instanceof Auto){
                Auto temp=(Auto) vehiculo;
                System.out.println(temp);
                 System.out.println("-----------------------------------------------------------------------------------------------------------------");
            }
            else if (vehiculo instanceof Moto){
                Moto temp=(Moto) vehiculo;
                System.out.println(temp);
                 System.out.println("-----------------------------------------------------------------------------------------------------------------");
            }
            else if (vehiculo instanceof Avion){
                Avion temp=(Avion) vehiculo;
                System.out.println(temp);
                 System.out.println("-----------------------------------------------------------------------------------------------------------------");
            }
            else if (vehiculo instanceof Helicoptero){
                Helicoptero temp=(Helicoptero) vehiculo;
                System.out.println(temp);
                 System.out.println("-----------------------------------------------------------------------------------------------------------------");
            }
        }
        
-También se demostró el ingreso de la clase anónima.

        /*
        Se crea un vehiculo anonimo y se lo imprime
        */
        Vehiculo anonimo=new Vehiculo(9, "Corvette", "DFF-96", "Chevroleth");
        System.out.println(anonimo);
        
A continuación, se podrá la información de GitHub

**Perfil:** JoseQ1996

**URL del proyecto:** https://github.com/JoseQ1996/Pr-ctica-02-POO-con-Java.git

## CONCLUSIONES:

Como conclusión puedo decir que el poder utilizar la herencia es de mucha utilidad ya que así no tenemos que repetir atributos en varias clases, también el uso de métodos abstractos ya que al declararlos en la clase padre los podemos implementar de diferentes maneras en las clases hijas, y el downcasting y el instanceof también son muy utilice para poder guardar todos los objetos en una lista de la clase padre y a través del instanceof ver a que clase hija pertenece y con el downcasting se puede cambiar el tipo de objeto, finalmente podría decir que así podemos realizar un trabajo mucho más productivo y mucha más fácil de entender.

## RECOMENDACIONES:

La implementación de enlaces en java es mucho más factible para realizar proyectos al igualas que los métodos abstractos.

