package Task1;
import java.util.Scanner;
import java.util.Random;
public class NumberGame {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		Random r=new Random();
		int score=0;
		String playAgain="yes";
		while(true) {
			int num=r.nextInt(100)+1;
			int attempts=0;
			int max=5;
			boolean guess=false;
			System.out.println("\nGuess the number between 1 and 100");
			System.out.println("You have "+max+" attempts.");
			while(attempts<max) {
				System.out.print("Enter you guess: ");
				int uguess=sc.nextInt();
				attempts++;
				if(uguess==num) {
					System.out.println("Congratulations! You guessed the number.");
					guess=true;
					score++;
					break;
				}
				else if(uguess>num) {
					System.out.println("Too high!");
				}
				else {
					System.out.println("Too low!");
				}
				System.out.println("Attempts Remaining: "+(max-attempts));
			}
			if(!guess) {
				System.out.println("The correct number was: "+num);
			}
			System.out.println("Your final score: "+score);
			System.out.print("Do you want to play again?(y/n): ");
			playAgain=sc.next();
			if(!playAgain.equalsIgnoreCase("y")) {
				break;
			}
		}
	}

}
