package Task3;
import java.util.Scanner;
public class ATMMachine {
	private double bal=1000;
	void deposit(double amt) {
		if(amt>0) {
			bal+=amt;
			System.out.println("Amount deposited successfully.");
		}
		else {
			System.out.println("Invalid Amount");
		}
	}
	void withdraw(double amt) {
		if(amt>0 && amt<=bal) {
			bal-=amt;
			System.out.println("Amount withdrawn successfully.");
		}
		else {
			System.out.println("Insufficient balance or invalid amount.");
		}
	}
	void checkBalance() {
		System.out.println("Current Balnace: "+bal);
	}
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		ATMMachine a=new ATMMachine();
		boolean running=true;
		while(running) {
			System.out.println("\n****** ATM MENU ******");
			System.out.println("1. Deposit");
			System.out.println("2. Withdraw");
			System.out.println("3. Check Balance");
			System.out.println("4. Exit");
			System.out.println("Enter your choice: ");
			int ch=sc.nextInt();
			switch(ch) {
			case 1:
				System.out.println("Enter amount to deposit: ");
				double damt=sc.nextDouble();
				a.deposit(damt);
				break;
			case 2:
				System.out.println("Enter amount to withdraw: ");
				double wamt=sc.nextDouble();
				a.withdraw(wamt);
				break;
			case 3:
				a.checkBalance();
				break;
			case 4:
				System.out.println("Thank you fo using ATM!");
				running=false;
				break;
			default:
				System.out.println("Invalid Choice.");
			}
		}

	}

}
