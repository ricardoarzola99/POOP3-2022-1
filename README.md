# POOP3-2022-1
Práctica 3 correspondiente a utilerías y clases de uso general

import java.text.SimpleDateFormat;
import java.util.ArrayList;
import java.util.Calendar;
import java.util.Date;
import java.util.Enumeration;
import java.util.Hashtable;

public class POOP3 {

    public static void main(String[] args) {
        System.out.println("-------Arreglos--------");
        int num [];//Se puede escribir de esta forma un arreglo
        int [] num1;//También se puede escribir de esta forma
        num1=new int[10];
       int [] num2={1,2,3,4,5};
        System.out.println("Elementos del num1 "+num1.length);//Length es un operador
        System.out.println("Elementos del num2 "+num2.length);
        System.out.println("-------For each--------");
        for (int o: num2) {//Para cada valor del número dos, el bucle imprime estos en o
        System.out.println(o);  
        }
        System.out.println("-------Concatenar cadenas--------");
        String s=new String("hola mundo");//Forma de objeto
        String s1="Hola mundo 2";//Forma de tipo primitivo
        System.out.println(s);
        System.out.println(s1);
        String nombre="Ricardo";
        String apellido="Arzola";
        String nombreCompleto=nombre+" "+apellido;
        System.out.println(nombreCompleto);
        System.out.println("-------Operador punto--------");
        System.out.println("Elementos en la cadena "+nombreCompleto.length());//length es un método por los paréntesis
        System.out.println(nombreCompleto.toUpperCase());//Método para transformar la cadena a mayúsculas, pero no guarda en memoria la cadena en mayúscula
        System.out.println(nombreCompleto);
        System.out.println("-------Wrappper y autoboxing--------");
        Integer k=new Integer(50);//Entero con formato de obejto
        Integer m=66;//Entero con formato de primitivo
        String s3=m.toString();//Convierte el entero a cadena
        System.out.println(s3);
        int r=k;
        String s4=r+"";//Se pone el espacio vacío porque de no hacerlo marcaría error
        System.out.println(s4);
        System.out.println("-------Colección--------");
        System.out.println("-------1. Arraylist-----");
        ArrayList<Integer>miArrayList=new ArrayList<Integer>();//() Estos parentesis indican que es un método, esto provoca que sea dinámico y se pueda modificar muchas veces
        miArrayList.add(99);//Add agrega elementos a la lista
        miArrayList.add(6);
        System.out.println(miArrayList.size());
        System.out.println(miArrayList.get(1));
        miArrayList.add(77);
        System.out.println(miArrayList.size());
        miArrayList.add(0,4);//Agregar números en una posición específica, esto se logra sólo con elementos dinámicos
        miArrayList.forEach(e -> {
            System.out.println(e);
        });
        System.out.println("-------HashTable--------");    
        Hashtable<String,Integer> miTabla=new Hashtable<String,Integer>();
        miTabla.put("Ricardo",443342);
        miTabla.put("Roberto",999525);
        miTabla.put("Ligia",4431050);
            System.out.println("Número de elementos en la tabla: "+miTabla.size());
            for (Integer valor: miTabla.values()) {// size Extrae los datos sin orden
                System.out.println(valor); 
            }
            for (String clave: miTabla.keySet()) {
                System.out.println(clave);  
            }
        System.out.println("-------Enumeración--------"); 
        String eClave;
        Integer eValor;
        Enumeration<String>iteraClaves=miTabla.keys();
        while(iteraClaves.hasMoreElements())  {
        eClave=iteraClaves.nextElement();
        eValor=miTabla.get(eClave);
            System.out.println("Clave "+eClave+ " Valor "+eValor);
        }
        System.out.println("-------Math--------"); 
        System.out.println(Math.PI);
        System.out.println(Math.abs(-9));
        System.out.println(Math.pow(2.5, 3));
        System.out.println(Math.sqrt(9));
        System.out.println(Math.max(6,99));
        System.out.println("-------Date--------"); 
        Date hoy=new Date();
        System.out.println(hoy);
        System.out.println("-------Calendar--------");
        Calendar calendarioHoy=Calendar.getInstance();
        System.out.println(calendarioHoy);
        System.out.println("-------Formato Calendar--------");
        SimpleDateFormat formatofecha=new SimpleDateFormat("dd-MM-yyyy");
        System.out.println(formatofecha.format(hoy));
        }
    }
