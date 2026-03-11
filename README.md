# CODSOFT
CodSoft Internship Tasks
import java.util.Scanner;
Class StudentGradeCalculation{
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        System.out.print("Enter all the chosen subjects: ");
        int s=sc.nextInt();
        int total=0;
        for(int i=0;i<=s;i++){
            System.out.print("Enter the subject name: ");
            String sname=sc.nextLine();
            System.out.print("Enter the marks for "+sname+": ");
            int m=sc.nextInt();
            total+=m;
        }
        double avg=(double)total/s;
        char grade;
        if(avg>=90 && avg<=100){
            grade='A';
        }
        else if(avg>=80 && avg<90){
            grade='B';
        }
        else if(avg>=70 && avg<80){
            grade='C';
        }
        else if(avg>=60 && avg<70){
            grade='D';
        }
        else{
            grade='F';
        }
        System.out.println("Total Marks: "+total);
        System.out.println("Average Percentage: "+avg);
        System.out.println("Grade: "+grade);
    }
}
