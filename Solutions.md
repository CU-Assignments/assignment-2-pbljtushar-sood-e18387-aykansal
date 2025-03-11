# Solutions

## Solution 1: Product Class

```java
public class Product {
    private int id;
    private String name;
    private double price;

    public Product(int id, String name, double price) {
        this.id = id;
        this.name = name;
        this.price = price;
    }

    public void displayProductDetails() {
        System.out.println("Product Details:");
        System.out.println("ID: " + id);
        System.out.println("Name: " + name);
        System.out.println("Price: " + price);
    }

    public static void main(String[] args) {
        Product product = new Product(101, "Laptop", 75000);
        product.displayProductDetails();
    }
}
```

## Solution 2: Library Management System

```java
class Book {
    private String title;
    private String author;
    private double price;

    public Book(String title, String author, double price) {
        this.title = title;
        this.author = author;
        this.price = price;
    }

    public void displayBookDetails() {
        System.out.println("Title: " + title);
        System.out.println("Author: " + author);
        System.out.println("Price: " + price);
    }
}

class Fiction extends Book {
    public Fiction(String title, String author, double price) {
        super(title, author, price);
    }

    @Override
    public void displayBookDetails() {
        System.out.println("Fiction Book Details:");
        super.displayBookDetails();
    }
}

class NonFiction extends Book {
    public NonFiction(String title, String author, double price) {
        super(title, author, price);
    }

    @Override
    public void displayBookDetails() {
        System.out.println("Non-Fiction Book Details:");
        super.displayBookDetails();
    }
}

public class LibraryManagement {
    public static void main(String[] args) {
        Fiction fictionBook = new Fiction("Harry Potter", "J.K. Rowling", 500);
        NonFiction nonFictionBook = new NonFiction("Sapiens", "Yuval Noah Harari", 700);

        fictionBook.displayBookDetails();
        nonFictionBook.displayBookDetails();
    }
}
```

## Solution 3: Student Information System

```java
abstract class Person {
    protected String name;
    protected int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public abstract void displayDetails();
}

class Student extends Person {
    private int rollNumber;

    public Student(String name, int age, int rollNumber) {
        super(name, age);
        this.rollNumber = rollNumber;
    }

    @Override
    public void displayDetails() {
        System.out.println("Student Details:");
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Roll Number: " + rollNumber);
    }
}

class Teacher extends Person {
    private String subject;

    public Teacher(String name, int age, String subject) {
        super(name, age);
        this.subject = subject;
    }

    @Override
    public void displayDetails() {
        System.out.println("Teacher Details:");
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Subject: " + subject);
    }
}

public class StudentInfoSystem {
    public static void main(String[] args) {
        Student student = new Student("Alice", 20, 101);
        Teacher teacher = new Teacher("Mr. Smith", 40, "Mathematics");

        student.displayDetails();
        teacher.displayDetails();
    }
}
```
