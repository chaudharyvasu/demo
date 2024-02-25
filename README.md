# demo
This is my first repository
<br>
Author -  Vasu Chaudhary
import java.util.Scanner;
import java.util.Random;
class Game{
   public int userinput;
   public int computerinput;
   public int noofguesses = 0;
    public int getNoofguesses(){
        return noofguesses;
    }
    public void setNoofguesses(int noofguesses){
        noofguesses = noofguesses;
    }
     Game(){
        Random rc = new Random();
        computerinput = rc.nextInt(100);
    }
    public int takeuserinput() {
        System.out.println("guess the numberr");
        Scanner sc = new Scanner(System.in);
        userinput = sc.nextInt();
        return userinput;
    }
    boolean iscorrectnumber(){
        noofguesses++;
        if(userinput==computerinput){
            System.out.format("you guessed the number right which is %d in %d no of attempts",computerinput,noofguesses);
            return true;
        }
        else if(userinput>computerinput){
            System.out.println("too highhh");
        }
        else if(userinput<computerinput){
            System.out.println("too low");
        }
        return false;
    }

}
public class guessthenumber {
    public static void main(String[] args) {
        Game g = new Game();
        boolean b = false;
        while(!b){
            g.takeuserinput();
            b = g.iscorrectnumber();
        }


    }
}

