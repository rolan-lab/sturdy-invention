/*
 * id : 446001241 
name : rolan obied alqurshy 
group : 
 */
package lap_3_rolan;
 
import java.util.Scanner;


class Employee {
   
    public String name;
    public double salary;
    public int hireYear;

    // Method to calculate years of service
    public int getYearsOfService(int currentYear) {
        return currentYear - hireYear;
    }

    // Method to display the employee's information
    public void printInfo(int currentYear) {
        System.out.println("************ Employee ***************");
        System.out.println("Name: " + name);
        System.out.println("Salary: " + salary);
        System.out.println("Hire year: " + hireYear);
        System.out.println("Years Of Service: " + getYearsOfService(currentYear));
        System.out.println();
    }
}


public class Lap_3_rolan {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

   
        int currentYear = 2024;

   
        Employee employee1 = new Employee();
        Employee employee2 = new Employee();

     
        System.out.println("Enter the name of the 1st employee:");
        employee1.name = input.nextLine();

        System.out.println("Enter the salary of the 1st employee:");
        employee1.salary = input.nextDouble();

        System.out.println("Enter the hire year of the 1st employee:");
        employee1.hireYear = input.nextInt();
        input.nextLine(); // clear the extra newline

        
        System.out.println("Enter the name of the 2nd employee:");
        employee2.name = input.nextLine();

        System.out.println("Enter the salary of the 2nd employee:");
        employee2.salary = input.nextDouble();

        System.out.println("Enter the hire year of the 2nd employee:");
        employee2.hireYear = input.nextInt();


        System.out.println();
        employee1.printInfo(currentYear);
        employee2.printInfo(currentYear);

      
        input.close();
    }
}

