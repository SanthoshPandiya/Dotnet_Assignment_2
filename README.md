  # Dotnet_Assignment_2

  using System;

namespace CSharpAssignment
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("=== TASK 2: CLASSES, CONSTRUCTORS & OBJECTS ===");

            // Creating an object from the Student class using the constructor
            Student myStudent = new Student("Alex", 20, "Computer Science");

            // Displaying the object's details using its properties
            Console.WriteLine("Student Name: " + myStudent.Name);
            Console.WriteLine("Student Age: " + myStudent.Age);
            Console.WriteLine("Student Major: " + myStudent.Major);

            // Modifying a property value
            myStudent.Age = 21;
            Console.WriteLine("\nUpdated Student Age: " + myStudent.Age);
        }
    }

    class Student
    {
        // 1. Fields (internal data storage)
        private string studentId;

        // 2. Properties (public accessors for our data)
        public string Name { get; set; }
        public int Age { get; set; }
        public string Major { get; set; }

        // 3. Constructor (initializes the object when created)
        public Student(string name, int age, string major)
        {
            Name = name;
            Age = age;
            Major = major;
            
            // Assigning a generated ID to our private field
            Random rnd = new Random();
            studentId = "STU-" + rnd.Next(1000, 9999);
        }
    }
}
