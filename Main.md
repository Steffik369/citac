package citac;

import java.util.Scanner;

public class Citac {

    static Scanner sc = new Scanner(System.in);
    static int volba = 0;
    static int pocetmoznosti = 4;
    static log c = new log();

    public static void main(String[] args) {
        int pom;
        
        do{
            zobrazMenu();
            switch(nactiVolbu()){
                case 1:
                    c.inkrementuj();
                    break;
                case 2:
                    System.out.print("Zadej nove cislo: ");
                    pom = sc.nextInt();
                    c.setMax1(pom);
                    c.reset();
                    break;
                case 3:
                    System.out.print("Zadej nove cislo: ");
                    pom = sc.nextInt();
                    c.setMax2(pom);
                    c.reset();
                    break;
                case 4:
                    c.reset();
                    break;
                case 0:
                    System.out.println("KONEC");
                    break;               
            }
        }while(volba != 0);
        
        
        
        
        

    }

    public static int nactiVolbu() {
        boolean dobre = true;
        System.out.print("Zadej volbu: ");
        do {
            volba = sc.nextInt();
            System.out.println("");
            if (volba < 0 || volba > pocetmoznosti) {
                dobre  = false;
                System.out.println("chyba volby");
                System.out.print("Zadej volbu: ");
            }else{
                dobre = true;
            }
        } while (!dobre);
        return volba;    
    }
    
    public static void zobrazMenu(){
        System.out.println("");
        c.tisk();
        System.out.println("---- MENU  ----");
        System.out.println("1. Inkrementuj");
        System.out.println("2. nastav max prave");
        System.out.println("3. nastav max leve");
        System.out.println("4. reset");
        System.out.println("0. konec");
    }

}

