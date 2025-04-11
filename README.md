import java.util.Scanner;
import java.util.Random;
public class pedra_papel_tesoura{
    public static void main (String [] args){
        Scanner ler= new Scanner(System.in);
        Random random = new Random ();
        int jogada, pontos_pc=0, pontos_user=0;
        int cjogada= random.nextInt(3);

        random.nextInt(cjogada);
        
        String painel = ("\n *** Vamos jogar pedra, papel, tesoura! *** ");
              painel += ("\n * Digite a opção referente a sua jogada: * ");
              painel += ("\n ************* 0 - Para pedra. *************");
              painel += ("\n ************* 1 - para papel. *************");
              painel += ("\n ************* 2 para tesoura. *************");
              painel += ("\n **** Para finalizar o jogo, digite 3. ****.");
        for (int i=0; i<3; i++){      
        System.out.printf (painel);
        jogada= ler.nextInt();
        
        String pc="";
        if (cjogada==0) pc = ("pedra");
        if (cjogada==1) pc = ("papel");
        if (cjogada==2) pc = ("tesoura");
        
        String user="";
        if (jogada==0) user = ("pedra");
        if (jogada==1) user = ("papel");
        if (jogada==2) user = ("tesoura");
        
        String vitoria = "\n *** Você jogou %s *** " + user
                       + "\n *** O computador jogou %s *** " + pc
                       + "\n ***** %s ganha de %s *******" + user +pc;
              
        String derrota = "\n *** Você jogou %s *** "
                       + "\n *** O computador jogou %s *** "
                       + "\n ***** %s ganha de %s *******";
              
        String empate = "\n *** Você jogou %s *** "
                      + "\n *** O computador jogou %s *** "
                      + "\n ***** %s empata %s *****";
              
        switch (jogada){
            case (0):
                if (cjogada==0) System.out.printf (empate);
                if (cjogada==1){   
                 System.out.printf (derrota);
                 pontos_pc= pontos_pc + 1;
                }
                if (cjogada==2) System.out.printf (vitoria);
            break;
            case (1):
                if (cjogada==0){
                 pontos_pc= pontos_pc + 1;
                 System.out.printf (derrota);
                }
                if (cjogada==1) System.out.printf (empate);
                if (cjogada==2) System.out.printf (derrota);
            break;
            case (2):
                if (cjogada==0) System.out.printf (empate);
                if (cjogada==1) System.out.printf (vitoria);
                if (cjogada==2) System.out.printf (derrota);
            break;
        }
        
       
        
       

        
       }
    }
}
