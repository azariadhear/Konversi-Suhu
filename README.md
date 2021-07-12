# Konversi-Suhu
package konversisuhu;
import java.util.Scanner;
public class KonversiSuhu {
  public static void main(String[] args) {
  double suhu, T;
  String derajat, drjt;
  T = 1.0;
  char ulang = 'y';
  char e = 'y';
  Scanner scan = new Scanner(System.in);
  while((ulang == 'y') || (ulang == 'Y')){
      e = 'y';
      
  System.out.println("KONVERSI SUHU");
  System.out.print("Masukkan suhu = ");
  suhu = scan.nextDouble();
  scan.nextLine();
  
  System.out.println("Pilih satuan: c/r/f/K");
  System.out.print("Masukkan satuan = ");
  derajat = scan.nextLine();

     if(derajat.equals("c")){
     T = 1/5.0 * suhu;
     } else if(derajat.equals("r")){
         T = 1/4.0 * suhu;
     }else if(derajat.equals("f")){
         T = 1/9.0 * (suhu-32);
     }else if(derajat.equals("K")){
         T = 1/5.0 * (suhu-273.15);
     }   
  System.out.println("Pilih satuan: c/r/f/K");
  System.out.print("Masukkan satuan yang ingin dihasilkan = ");
    drjt= scan.nextLine();
    
    if(drjt.equals("c")){
      T *= 5;
    }else if(drjt.equals("r")){
        T *= 4;
    }else if(drjt.equals("f")){
        T = T * 9 + 32;
    }else if(drjt.equals("K")){
        T = T * 5 + 273.15;
    }
    System.out.println("Suhu " + suhu + derajat + " = " + T + drjt);
    System.out.println("\nMau ulang? Tekan y jika ya");
            ulang = scan.next().charAt(0);
  }
  }
}
