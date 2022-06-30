import java.util.Scanner;

/**
 * date: 15/03/2022
 *
 * @author Oscar David Guerra Arrieta IG: osdaguear
 *
 */

public class PrimerAporte {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        int num = 0, aux = 2; // num, donde se guardara el numero a probar
        boolean NoEsPrimo = false; /*Para que no se siga verificando la condiccion
                                    sino que pare apenas la condicion sea verdadera 
                                    */

        System.out.print("Digite un número, para saber si es primo o no: "); // sms en pantalla para el usuario
        num = sc.nextInt(); //captura del numero

        if (num == 1) { // sabemos que el 1 no es un numero primo
            System.out.println("\n1 NO es un número primo"); // lo indicamos en un sms
        } else { // sino
            while ((num >= aux) && (NoEsPrimo == false)) { /*
                Indica que se va a seguir en el bucle hasta que el auxiliar sea
                pues mayor a al numero; es decir, se va a verificar que dicho
                numero sea o no divisible por un numero diferente de el mismo
                */
                /*
                Ademas, en el momento que la condicion (No sea el numero primo),
                entonces deje de seguir verificando y termine el ciclo
                */
                if (((num % aux) == 0) && (aux != num)) { /*
                    Primero, si ese número al ser auxiliar, que es el numero que
                    le sigue a 1; es decir (2), y sucedera por una cifra mayor
                    hasta verificar todas las condiciones
                    */
                    /* segundo obviamente cuando se verifique la última condición 
                    y el auxiliar sea el mismo que el numero, va a ser 0, por lo
                    tanto el auxiliar debe ser distinto del numero*/
                    System.out.println("\n" + num + " NO es un número primo"); // muestre enpantalla que el numero no es primo
                    NoEsPrimo = true; // cambie el valor del bolean, así ya no se cumple una condicion del cilo
                } else if (num == aux) { /* sino se cumplo o anterior
                    y numero es igual al axuliar, podemos decir que...
                    */
                    System.out.println("\n" + num + " SÍ es un número primo"); // ese número es primo, y enviamos un sms en pantalla
                }
                aux++; /*
                Como lo dicho anteriormente el auxiliar que es que va ir verificando
                que ese numero no sea multiplo de otro número
                */

            }
        }

    }

}
