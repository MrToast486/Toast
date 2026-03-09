import java.util.Scanner;


public class Main {
   public static void main(String[] args) {
       Scanner scanner = new Scanner(System.in);
       int option = 0;
       char letter = ' ';
       int stateOption = 0;


       while (option != 2) {
           System.out.println("ScholarShips For Minorities");
           System.out.println("Main Menu ");
           System.out.println("1) Continue  ");
           System.out.println("2) Exit");
           System.out.print("Enter option: ");
           option = scanner.nextInt();


           if (option == 1) {
               letter = ' ';
               System.out.println("Please enter your name to get Started");
               scanner.nextLine();
               String name = scanner.nextLine();
               while (letter != 'q') {
                   System.out.println("What Minority are you a part of");
                   System.out.println("a) Women in Stem");
                   System.out.println("b) Student with Disabilities");
                   System.out.println("c) LGBTQ+ individuals");
                   System.out.println("d) Veterans");
                   System.out.println("e) other");
                   System.out.println("q) Back to Menu");
                 


                       boolean validOption = false;
                       String otherMinority = "";


                       while(!validOption) {
                           System.out.println("Enter option: ");
                           letter = scanner.next().charAt(0);


                           if (letter == 'a'|| letter == 'b'|| letter == 'c'|| letter == 'd'|| letter == 'e'|| letter == 'q') {
                               validOption = true;


                               if (letter == 'e') {
                                   scanner.nextLine();
                                   System.out.println("Enter the name of the minority group");
                                    otherMinority = scanner.nextLine();
                               }
                           } else {
                               System.out.println("Invalid answer please try again");
                           }
                       }
                       if (letter!= 'q') {
                       stateOption = 0;
                       while (stateOption != 1 && stateOption != 2) {


                           System.out.println("In-State or Out-of-State");
                           System.out.println("1) In");
                           System.out.println("2) Out");
                           System.out.print("Enter option: ");


                           stateOption = scanner.nextInt();


                           if (stateOption != 1 && stateOption != 2) {
                               System.out.println("Invalid answer please try again");
                           }
                       }
                       scanner.nextLine();
                       System.out.println("What school do you attend");
                       String schoolname = scanner.nextLine();




                       double gpa = -1;




                       while (gpa < 0.0 || gpa > 4.0) {
                           System.out.print("Enter your GPA (0.00 - 4.00): ");
                           gpa = scanner.nextDouble();




                           if (gpa < 0.0 || gpa > 4.0) {
                               System.out.println("Invalid GPA. Please enter between 0.00 and 4.00.");
                           }
                       }


                       String[] userInfo = new String[5];


                           userInfo[0] = "Name: " + name;
                           String thing = " ";
                           if (letter == 'a') {
                               thing = "Women in Stem";
                           } else if (letter == 'b') {
                               thing = "Student with Disabilities";
                           } else if (letter == 'c') {
                               thing = "LGBTQ+ individuals";
                           } else if (letter == 'd') {
                               thing = "Veterans";
                           } else if (letter == 'e') {
                               thing = otherMinority;
                           }
                           userInfo[1] = "Minority Option: " + thing;
                           userInfo[2] = "State Status: " + (stateOption == 1 ? "In-State" : "Out-of-State");
                           userInfo[3] = "School: " + schoolname;
                           userInfo[4] = "GPA: " + gpa;




                           System.out.println("Results:");
                       System.out.println("-------------------");


                       System.out.println("Your Information:");
                       for (int i = 0; i < userInfo.length; i++) {
                           System.out.println(userInfo[i]);
                       }


                       System.out.println();
                       System.out.println("Based on your information, the following scholarships are available:");
                       System.out.println();




                       if (gpa <= 2.50) {
                           System.out.println("Better luck next time.");
                           System.out.println("Currently no scholarships available.");
                       } else if (gpa <= 3.20) {
                           System.out.println(" 2 scholarships available:");
                           if (letter == 'a') {
                               System.out.println("1.Women in STEM Excellence Scholarship");
                               System.out.println("2.Future Women Leaders Scholarship");
                           } else if (letter == 'b') {
                               System.out.println("1.Accessible Education Scholarship");
                               System.out.println("2.Vision Achievement Scholarship");
                           } else if (letter == 'c') {
                               System.out.println("1.Pride Leadership Scholarship");
                               System.out.println("2.Equality in Education Scholarship");
                           } else if (letter == 'd') {
                               System.out.println("1.Community Opportunity Scholarship");
                               System.out.println("2.Rural Education Advancement Scholarship");
                           } else if (letter == 'e') {
                               System.out.println("1.First-Generation College Student Scholarship");
                               System.out.println("2.Community Opportunity Scholarship");
                           }
                       }
                           else {
                           System.out.println("3 scholarships available:");
                           if (letter == 'a') {
                               System.out.println("1.Women in STEM Excellence Scholarship");
                               System.out.println("2.Future Women Leaders Scholarship");
                               System.out.println("3.Single Mother Education Scholarship");
                           } else if (letter == 'b') {
                               System.out.println("1.Accessible Education Scholarship");
                               System.out.println("2.Vision Achievement Scholarship");
                               System.out.println("3.Learning Difference Success Scholarship");
                           } else if (letter == 'c') {
                               System.out.println("1.Pride Leadership Scholarship");
                               System.out.println("2.Equality in Education Scholarship");
                               System.out.println("3.Rainbow Future Scholarship");
                           } else if (letter == 'd') {
                               System.out.println("1.Community Opportunity Scholarship");
                               System.out.println("2.Rural Education Advancement Scholarship");
                               System.out.println("3.Global Opportunity Scholarship");
                           } else if (letter == 'e') {
                               System.out.println("1.First-Generation College Student Scholarship");
                               System.out.println("2.Community Opportunity Scholarship");
                               System.out.println("3.Rural Education Advancement Scholarship");
                           }
                       }
                       System.out.println("Enter any number to Return to Main Menu");
                       System.out.print("Enter option: ");


                       int nextOption = scanner.nextInt();
                       if (nextOption != 1) {
                           letter = 'q';                       }


                   }
               }
           } else if (option == 2) {
               System.out.println(" Thank you for visting the ScholarShip For Minorites website");
           } else {
               System.out.println(" Invalid answer please try again");
           }
       }
   }
}
