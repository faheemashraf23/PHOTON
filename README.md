void main() {
  double temperature = 27.5;
  print('The current temperature is: $temperature');
}



2.
void main() {
  double calculateArea(double length, double width) {
    return length * width;
  }

  double area = calculateArea(5.0, 3.0);
  print('The calculated area is: $area');
}

3.
import 'dart:io';

void main() {
  int? num;
  while (true) {
    stdout.write("Enter a number: ");
    String? input = stdin.readLineSync();

    try {
      num = int.parse(input!);
      break; // exit the loop if input is valid
    } catch (e) {
      print("Invalid input. Please enter a valid integer.");
    }
  }

  if (num > 0) {
    print("Positive");
  } else if (num < 0) {
    print("Negative");
  } else {
    print("Zero");
  }
}

4.
import 'dart:io';
void main() {
  List<String> countries = ["USA", "Canada", "UK"];

  for (int i = 0; i < countries.length; i++) {
    print("Country at index $i: ${countries[i]}");
  }

  stdout.write("Enter a new country: ");
  String? newCountry = stdin.readLineSync();

  countries.add(newCountry!);

  print("Updated list of countries: $countries");
}

1.
class Student {
  int _grade = 0;

  void setGrade(int grade) {
    if (grade >= 0) {
      _grade = grade;
    } else {
      print("Invalid grade value");
    }
  }

  int getGrade() {
    return _grade;
  }
}

void main() {
  Student student = Student();
  student.setGrade(85);
  student.setGrade(-10);
  print("Student's grade: ${student.getGrade()}");
}

2.

import 'dart:math';

class Shape {
  double calculateArea() {
    return 0;
  }
}

class Rectangle extends Shape {
  double length;
  double width;

  Rectangle(this.length, this.width);

  @override
  double calculateArea() {
    return length * width;
  }
}

class Circle extends Shape {
  double radius;

  Circle(this.radius);

  @override
  double calculateArea() {
    return pi * radius * radius;
  }
}

void main() {
  Rectangle rectangle = Rectangle(5.0, 3.0);
  Circle circle = Circle(2.0);

  print("Area of Rectangle: ${rectangle.calculateArea()}");
  print("Area of Circle: ${circle.calculateArea()}");
}



