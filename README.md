//Problema 1
public class lab4 {

    public static void main(String[] args) {
        System.out.println(mijloc("3501"));
        System.out.println(mijloc("350"));
    }

    public static String mijloc(String cuvant) {
        StringBuilder builder = new StringBuilder();
        if (cuvant.length() % 2 == 0) {
            builder.append(cuvant.charAt(cuvant.length() / 2 - 1));
            builder.append(cuvant.charAt(cuvant.length() / 2));

        } else {
            builder.append(cuvant.charAt(cuvant.length() / 2));

        }
        return builder.toString();

    }
}

// Problema 2
public class SumaCifrelor {
    public static int sumaCifrelor(int numar) {
        int suma = 0;

        while (numar != 0) {
            suma += numar % 10;
            numar /= 10;
        }

        return suma;
    }

    public static void main(String[] args) {
        int numar = 12345;
        int rezultat = sumaCifrelor(numar);
        System.out.println("Suma cifrelor numărului " + numar + " este: " + rezultat);
    }
}

// Problema 3
public class Dog {
    private String name;
    private String breed;

    public Dog(String name, String breed) {
        this.name = name;
        this.breed = breed;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getBreed() {
        return breed;
    }

    public void setBreed(String breed) {
        this.breed = breed;
    }
}

public class Main {
    public static void main(String[] args) {

        Dog dog1 = new Dog("Max", "Golden Retriever");
        Dog dog2 = new Dog("Buddy", "Labrador");

        System.out.println("Proprietățile inițiale ale primului câine:");
        System.out.println("Nume: " + dog1.getName());
        System.out.println("Rasă: " + dog1.getBreed());

        System.out.println("\nProprietățile inițiale ale celui de-al doilea câine:");
        System.out.println("Nume: " + dog2.getName());
        System.out.println("Rasă: " + dog2.getBreed());

        dog1.setName("Rocky");
        dog2.setBreed("German Shepherd");

        System.out.println("\nProprietățile modificate ale primului câine:");
        System.out.println("Nume: " + dog1.getName());
        System.out.println("Rasă: " + dog1.getBreed());

        System.out.println("\nProprietățile modificate ale celui de-al doilea câine:");
        System.out.println("Nume: " + dog2.getName());
        System.out.println("Rasă: " + dog2.getBreed());
    }
}

// Problema 4
public class Rectangle {
    private double width;
    private double length;

    public Rectangle(double width, double length) {
        this.width = width;
        this.length = length;
    }

    public double getWidth() {
        return width;
    }

    public void setWidth(double width) {
        this.width = width;
    }

    public double getLength() {
        return length;
    }

    public void setLength(double length) {
        this.length = length;
    }

    public double calculateArea() {
        return width * length;
    }

    public double calculatePerimeter() {
        return 2 * (width + length);
    }

    public static void main(String[] args) {
        Rectangle myRectangle = new Rectangle(5.0, 10.0);

        System.out.println("Aria dreptunghiului: " + myRectangle.calculateArea());
        System.out.println("Perimetrul dreptunghiului: " + myRectangle.calculatePerimeter());
    }
}

// Problema 5
class Person {
    private String name;
    private String email;

    public Person(String name, String email) {
        this.name = name;
        this.email = email;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getEmail() {
        return email;
    }

    public void setEmail(String email) {
        this.email = email;
    }
}

class Student extends Person {
    private int[] grades;

    public Student(String name, String email, int[] grades) {
        super(name, email);
        this.grades = grades;
    }

    public int[] getGrades() {
        return grades;
    }

    public void setGrades(int[] grades) {
        this.grades = grades;
    }
}

class Professor extends Person {
    private String[] courses;

    public Professor(String name, String email, String[] courses) {
        super(name, email);
        this.courses = courses;
    }

    public String[] getCourses() {
        return courses;
    }

    public void setCourses(String[] courses) {
        this.courses = courses;
    }
}

public class Main {
    public static void main(String[] args) {

        Person person = new Person("John Doe", "john@example.com");
        int[] studentGrades = { 90, 85, 78 };
        Student student = new Student("Alice Smith", "alice@example.com", studentGrades);
        String[] professorCourses = { "Math", "Physics", "Computer Science" };
        Professor professor = new Professor("Dr. Smith", "smith@example.com", professorCourses);

        System.out.println("Informații despre persoana:");
        System.out.println("Nume: " + person.getName());
        System.out.println("Email: " + person.getEmail());

        System.out.println("\nInformații despre student:");
        System.out.println("Nume: " + student.getName());
        System.out.println("Email: " + student.getEmail());
        System.out.println("Note: " + java.util.Arrays.toString(student.getGrades()));

        System.out.println("\nInformații despre profesor:");
        System.out.println("Nume: " + professor.getName());
        System.out.println("Email: " + professor.getEmail());
        System.out.println("Cursuri predate: " + java.util.Arrays.toString(professor.getCourses()));
    }
}
