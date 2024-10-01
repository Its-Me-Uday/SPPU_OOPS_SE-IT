import java.util.Scanner;

class Complex {
    private double real;
    private double imaginary;

    
    public Complex() 
   {
        this.real = 0;
        this.imaginary = 0;
    }

 
    public Complex(double real, double imaginary)
   {
        this.real = real;
        this.imaginary = imaginary;
    }

   
    public Complex add(Complex c) 
    {
        return new Complex(this.real + c.real, this.imaginary + c.imaginary);
    }

  
    public Complex subtract(Complex c)
    {
        return new Complex(this.real - c.real, this.imaginary - c.imaginary);
    }

    
    public Complex multiply(Complex c)
    {
        double realPart = (this.real * c.real) - (this.imaginary * c.imaginary);
        double imaginaryPart = (this.real * c.imaginary) + (this.imaginary * c.real);
        return new Complex(realPart, imaginaryPart);
    }

   
    public Complex divide(Complex c)
    {
        double denominator = c.real * c.real + c.imaginary * c.imaginary;
        double realPart = (this.real * c.real + this.imaginary * c.imaginary) / denominator;
        double imaginaryPart = (this.imaginary * c.real - this.real * c.imaginary) / denominator;
        return new Complex(realPart, imaginaryPart);
    }

    
    public void display()
    {
        if (imaginary >= 0) {
            System.out.println(real + " + " + imaginary + "i");
        } else {
            System.out.println(real + " - " + Math.abs(imaginary) + "i");
        }
    }
}

public class ComplexNumberOperations {
    public static void main(String[] args) 
      {
        Scanner scanner = new Scanner(System.in);

       
        System.out.println("Enter the real and imaginary part of the first complex number:");
        double real1 = scanner.nextDouble();
        double imaginary1 = scanner.nextDouble();
        Complex c1 = new Complex(real1, imaginary1);

       
        System.out.println("Enter the real and imaginary part of the second complex number:");
        double real2 = scanner.nextDouble();
        double imaginary2 = scanner.nextDouble();
        Complex c2 = new Complex(real2, imaginary2);

       
        while (true) {
            System.out.println("\nSelect an operation:");
            System.out.println("1. Add");
            System.out.println("2. Subtract");
            System.out.println("3. Multiply");
            System.out.println("4. Divide");
            System.out.println("5. Exit");

            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    Complex sum = c1.add(c2);
                    System.out.print("Sum: ");
                    sum.display();
                    break;
                case 2:
                    Complex difference = c1.subtract(c2);
                    System.out.print("Difference: ");
                    difference.display();
                    break;
                case 3:
                    Complex product = c1.multiply(c2);
                    System.out.print("Product: ");
                    product.display();
                    break;
                case 4:
                    if (c2.real == 0 && c2.imaginary == 0) {
                        System.out.println("Division by zero is not allowed!");
                    } else {
                        Complex quotient = c1.divide(c2);
                        System.out.print("Quotient: ");
                        quotient.display();
                    }
                    break;
                case 5:
                    System.out.println("Exiting the program.");
                    scanner.close();
                    return;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }
    }
}
