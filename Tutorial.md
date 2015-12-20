Usar jnumericallib es sumamente sencillo. En esta sección presentaremos algunos ejemplos de uso para ilustrar lo sencillo que es el uso de la librería.

## Ejemplo Método Numérico ##

En este caso veremos un ejemplo del uso del **Método de Bisección**. Para aplicar este método lo único que debemos hacer es seguir los siguientes pasos.

**1- Creamos la función:**

En el primer paso creamos la función  a la cual le aplicaremos el método. En este caso la función que vamos a la que le vamos a aplicar el **Método de Bisección** es _x<sup>3</sup>+4x<sup>2</sup>-10_.
Y se define así:

```
final Funcion f2 = new Funcion(){
    public double eval(double x){
            //Definimos la función haciendo uso de la clase Math de java.utils
            return  Math.pow(x,3) + 4 * Math.pow(x,2) - 10;
        }
    };
```

**2- Aplicamos el método:**

Una vez que tenemos la función solo resta aplicar el método. Para eso llamamos el método bisection de la clase MetodosNumericos.

```
double calculateRoot =  MetodosNumericos.bisection(function, a, b, error, iterations);
```

Notese que aparte de la función el método recibe otros parámetros. esos otros parámetros cambian de método en método, para conocer que poner en cada uno solo basta leer la documentación del método. La misma se puede encontrar [aquí]

_Nota: En este caso la clase MetodosNumericos sirve solamente como un facade. Los mismos métodos pueden ser accedidos e inclusive extendidos usando cada clase en particular._

Y eso es todo. Así de fácil...


## Ejemplo Interpolador ##

En este caso veremos un ejemplo utilizando el **Interpolador Lineal**. Los interpoladores reciben una serie de puntos y retornan una función. Para usarlos solo hace falta seguir estos pasos:

**1- Creamos los puntos:**

Creamos los puntos que vamos a pasarle al método para que interpole. En este caso vamos a crear puntos arbitrarios de la nada, pero en un caso de uso normal probablemente esta serie de puntos es el resultado de algún otro método

```
 List<Point2D.Double> points = new ArrayList<Point2D.Double>();
        points.add(new Point2D.Double(0, 0));
        points.add(new Point2D.Double(2, 4));
        points.add(new Point2D.Double(4, 0));
        points.add(new Point2D.Double(5, 8));
        return points;
```

**2- Aplicamos la interpolación:**

Una vez que ya tenemos los puntos que queremos interpolar llamamos al interpolador correspondiente usando la clase Interpoladores de la siguiente manera:

```
Funcion interpolation = Interpoladores.interpolarLinealmente(points);
```

_Nota: En este caso la clase Interpoladores sirve solamente como un facade. Los mismos métodos pueden ser accedidos e inclusive extendidos usando cada clase en particular._


Así de sencillo. Cualquier duda remitirse a la documentación, o contactate con nosotros. Gustosos estaremos de responder cualquier duda que pueda surgir.