# Dart Practice Problems

### Total Problems - 54

### Question Sources - [w3resource.com](https://w3resource.com)

---

1. Write a Dart program to print the following string in a specific format
   *Sample String :* "Twinkle, twinkle, little star, How I wonder what you are! Up above the world so high, Like a diamond in the sky. Twinkle, twinkle, little star, How I wonder what you are" *Output*:

   ```
   Twinkle, twinkle, little star,
   	How I wonder what you are! 
   		Up above the world so high,   		
   		Like a diamond in the sky. 
   Twinkle, twinkle, little star, 
   	How I wonder what you are
   ```

   Code - 

   ```dart
   main() {
     var value =  '''
     Twinkle, twinkle, little star,
     \tHow I wonder what you are!
     \t\tUp above the world so high,
     \t\tLike a diamond in the sky.
     Twinkle, twinkle, little star,
     \tHow I wonder what you are
     ''';
     print(value);
   }
   ```

2. Write a Dart program to get the Python version you are using.

   Code - 

   ```dart
   import 'dart:io' show Platform;
   
   main() {
     print(Platform.version);
   }	
   ```

3. Write a Dart program to display the current date and time.
   *Sample Output :* 
   Current date and time : 
   2014-07-05 14:34:14

   Code - 

   ```dart
   main() {
     var now = new DateTime.now();
     print(now);
   }
   ```

4. Write a Dart program which accepts the radius of a circle from the user and compute the area.

   Code - 

   ```dart
   import 'dart:io';
   
   main() {
     const pi = 3.14;
     dynamic radius = stdin.readLineSync();
     radius = double.parse(radius);
     print('The area is: ${pi*radius*radius}');
   }
   ```

5. Write a Dart program which accepts the user's first and last name and print them in reverse order with a space between them.

   Code - 

   ```dart
   import 'dart:io';
   
   main() {
     print('Enter First Name');
     var firstName = stdin.readLineSync();
     print('Enter Last Name');
     var lastName = stdin.readLineSync();
     print('$lastName $firstName');
   }
   ```

6.  Write a Dart program which accepts a sequence of comma-separated numbers from user and generate a list and a tuple with those numbers.
   *Sample data :* 3, 5, 7, 23
   *Output :* 
   List : ['3', ' 5', ' 7', ' 23'] 
   Set : ('3', ' 5', ' 7', ' 23')

   Code - 

   ```dart
   import 'dart:io';
   
   main() {
     var elements = stdin.readLineSync();
     var eleList = elements.split(',');
     print('List: $eleList');
     var eleSet = <String> {};
     for (var x in eleList) {
       eleSet.add(x);
     }
     print('Set: $eleSet');
   }
   ```

7. Write a Dart program to accept a filename from the user and print the extension of that.
   *Sample filename :* abc.java 
   *Output :* java

   Code - 

   ```dart
   import 'dart:io';
   
   main() {
     var fileName = stdin.readLineSync();
     var fileSplit = fileName.split('.');
     print(fileSplit[1]); 
   }
   ```

8. Write a Dart program to display the first and last colors from the following list.
   color_list = ["Red","Green","White" ,"Black"]

   Code - 

   ```dart
   main() {
     var color_list = ['Red', 'Green', 'White', 'Black'];
     print('${color_list.first} and ${color_list.last}');
   }
   ```

9.  Write a Dart program to display the examination schedule. (extract the date from exam_st_date).

   Code - 

   ```dart
   main() {
     var exam_st_list = {11, 12, 2014};
     print(exam_st_list.join('/'));
   }
   ```

10. Write a Dart program that accepts an integer (n) and computes the value of n+nn+nnn.

    Code - 

    ```dart
    import 'dart:io';
    
    main() {
      var sum = 0;
      dynamic n = stdin.readLineSync();
      var numberList = [n, n*2, n*3];
      for (var x in numberList) {
        sum += int.parse(x);
      }
      print(sum);
    }
    ```

11. Write a Dart program to print the calendar of a given month and year.

    Code - 

    ```dart
    import 'dart:io';
    
    void main() {
      var month = stdin.readLineSync();
      var year = stdin.readLineSync();
      Process.run('cal', [month, year]).then((ProcessResult results) {
        print(results.stdout);
      });;
    }
    ```

12. Write a Dart program to print the following here document.
    *Sample string* :
    a string that you "don't" have to escape
    This
    is a ....... multi-line
    heredoc string --------> example

    Code - 

    ```dart
    void main() {
      var output = '''
      a string that you \"don\'t\" have to escape
      this
      is a ....... multi-line
      heredoc string --------> example
      ''';
      print(output);
    }
    ```

13. Write a Dart program to calculate number of days between two dates.
    *Sample dates* : (2014, 7, 2), (2014, 7, 11)
    *Expected output* : 9 days

    Code - 

    ```dart
    void main() {
      var initialDate = new DateTime.utc(2014, 07, 02);
      var finalDate = new DateTime.utc(2014, 07, 11);
      var difference = finalDate.difference(initialDate);
      print(difference.inDays);
    
    } 
    ```

14. Write a Dart program to get the volume of a sphere with radius 6.

    Code - 

    ```dart
    import 'dart:math';
    import 'dart:io';
    
    void main() {
      dynamic radius = stdin.readLineSync();
      radius = double.parse(radius);
      print(4/3*(pi*pow(radius, 3)));
    }
    ```

15. Write a Dart program to get the difference between a given number and 17, if the number is greater than 17 return double the absolute difference.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var number = double.parse(stdin.readLineSync());
      double result = number - 17;
      var diff = result.abs();
      if (number > 17) {
        print(2*diff);
      }
      else {
        print(result);
      }
    }
    ```

16. Write a Dart program to test whether a number is within 100 of 1000 or 2000.

    Code - 

    ```dart
    import 'dart:io';
    
    void main() {
      var number = int.parse(stdin.readLineSync());
      if ((1000-number).abs() <= 100 || (2000-number).abs() <= 100) {
        print('True');
      }
      else {
        print('False');
      }
    }
    ```

17. Write a Dart program to calculate the sum of three given numbers, if the values are equal then return three times of their sum.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var sum = 0;
      var numbers = (stdin.readLineSync()).split(' ');
      numbers = numbers.sublist(0, 3);
      numbers.forEach((f){
        int.parse(f);
        sum += int.parse(f);
      });
      if(numbers[0] == numbers[1] && numbers[1] == numbers[2] && numbers[0] == numbers[2]) {
        print(3*sum);
      }
      else {
        print(sum);
      }
    }
    ```

18. Write a Dart program to get a new string from a given string where "Is" has been added to the front. If the given string already begins with "Is" then return the string unchanged.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var value = stdin.readLineSync();
      if (value.substring(0,2) == 'Is') {
        print(value);
      }
      else {
        print('Is$value');
      }
    }
    ```

19. Write a Dart program to get a string which is n (non-negative integer) copies of a given string.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var value = stdin.readLineSync();
      var numbers = int.parse(stdin.readLineSync());
      print('${value*numbers}');
    }
    ```

20. Write a Dart program to find whether a given number (accept from the user) is even or odd, print out an appropriate message to the user.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var number = int.parse(stdin.readLineSync());
      if (number % 2 == 0) {
        print('The number is even');
      }
      else {
        print('The number is odd');
      }
    }
    ```

21. Write a Dart program to count the number 4 in a given list.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      int count = 0;
      var numberList = (stdin.readLineSync()).split(' ');
      numberList.forEach((f) {
        if (int.parse(f) == 4) {
          count += 1;
        }
      });
      print(count);
    }
    ```

22. Write a Dart program to get the n (non-negative integer) copies of the first 2 characters of a given string. Return the n copies of the whole string if the length is less than 2.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var value = stdin.readLineSync();
      var numbers = int.parse(stdin.readLineSync());
      if (value.length <= 2){
        print('${value*numbers}');
      }
      else {
        print('${(value.substring(0, 2))*numbers}');
      }
    }
    ```

23. Write a Dart program to test whether a passed letter is a vowel or not.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var vowels = ['a', 'e', 'o', 'u', 'i'];
      var value = stdin.readLineSync();
      value = value.substring(0,1);
      vowels.forEach((f){
        if (f == value) {
          print('True');
          exit(0);
        }
        else {
          print('False');
          exit(0);
        }
      });
    }
    ```

24. Write a Dart program to check whether a specified value is contained in a group of values.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var valueList = (stdin.readLineSync()).split(' ');
      var value = int.parse(stdin.readLineSync());
      valueList.forEach((f){
        if (int.parse(f) == value) {
          print('True');
          exit(0);
        }
      });
      print('False');
    }
    ```

25. Write a Dart program to create a histogram from a given list of integers.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var numbers = (stdin.readLineSync()).split(' ');
      numbers.forEach((f){
        var pattern = '';
        for (var x=0; x< int.parse(f); x++) {
          pattern += '@';
        }
        print(pattern);
      });
    }
    ```

26. Write a Dart program to concatenate all elements in a list into a string and return it.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var numbers = (stdin.readLineSync()).split(' ');
      var result = '';
      numbers.forEach((f){
        result += f;
      });
      print(result);
    }
    ```

27. Write a Dart program to print all even numbers from a given numbers list in the same order and stop the printing if any numbers that come after 237 in the sequence.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var numbers = (stdin.readLineSync()).split(' ');
      numbers.forEach((f){
        if (int.parse(f) == 237) {
            exit(0);
          }
        if (int.parse(f) % 2 ==0) {
          print(f);
        }
      });
    }
    ```

28. Write a Dart program to print out a set containing all the colors from color_list_1 which are not present in color_list_2.
    *Test Data* : 
    color_list_1 = set(["White", "Black", "Red"]) 
    color_list_2 = set(["Red", "Green"])
    *Expected Output* : 
    {'Black', 'White'}

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var color_1 = <String> {};
      var color_2 = <String> {};
      var input1 = (stdin.readLineSync()).split(' ');
      input1.forEach((f) {
        color_1.add(f);
      });
      var input2 = (stdin.readLineSync()).split(' ');
      input2.forEach((f) {
        color_2.add(f);
      });
    
      var difference = color_1.difference(color_2);
      print(difference);
    }
    ```

29. Write a Dart program that will accept the base and height of a triangle and compute the area.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var base = double.parse(stdin.readLineSync());
      var height = double.parse(stdin.readLineSync());
      print(0.5*base*height);
    }
    ```

30. Write a Dart program to compute the greatest common divisor (GCD) of two positive integers.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var numbers = (stdin.readLineSync()).split(' ');
      print(int.parse(numbers[0]).gcd(int.parse(numbers[1])));
    }
    ```

31. Write a Dart program to get the least common multiple (LCM) of two positive integers.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var numbers = (stdin.readLineSync()).split(' ');
      var gcd = int.parse(numbers[0]).gcd(int.parse(numbers[1]));
      print((int.parse(numbers[0])*int.parse(numbers[1]))~/gcd);
    }
    ```

32. Write a Dart program to sum of three given integers. However, if two values are equal sum will be zero.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var sum = 0;
      var numbers = (stdin.readLineSync()).split(' ');
      numbers = numbers.sublist(0, 3);
      numbers.forEach((f){
        int.parse(f);
        sum += int.parse(f);
      });
      if(numbers[0] == numbers[1] || numbers[1] == numbers[2] || numbers[0] == numbers[2]) {
        print(0);
      }
      else {
        print(sum);
      }
    }
    ```

33. Write a Dart program to sum of two given integers. However, if the sum is between 15 to 20 it will return 20.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var numbers = (stdin.readLineSync()).split(' ');
      var sum = int.parse(numbers[0]) + int.parse(numbers[1]);
      if (sum >=15 && sum <= 20 ) {
        print(20);
      }
      else {
        print(sum);
      }
    }
    ```

34. Write a Dart program that will return true if the two given integer values are equal or their sum or difference is 5.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var numbers = (stdin.readLineSync()).split(' ');
      if (int.parse(numbers[0]) == int.parse(numbers[1]) || int.parse(numbers[0]) - int.parse(numbers[1]) == 5 || int.parse(numbers[0]) + int.parse(numbers[1]) == 5 ) {
        print(true);
      }
      else {
        print(false);
      }
    }
    ```

35. Write a Dart program to display your details like name, age, address in three different lines.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var name = stdin.readLineSync();
      var age = int.parse(stdin.readLineSync());
      var address = stdin.readLineSync();
      print('$name\n$age\n$address');
    }
    ```

36.  Write a Dart program to solve (x + y) * (x + y).
    *Test Data* : x = 4, y = 3
    *Expected Output* : (4 + 3) ^ 2) = 49

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var x = int.parse(stdin.readLineSync());
      var y = int.parse(stdin.readLineSync());
      print((x+y)*(x+y));
    }
    ```

37. Write a Dart program to compute the future value of a specified principal amount, rate of interest, and a number of years.

    *Test Data* : amt = 10000, int = 3.5, years = 7
    *Expected Output* : 12722.79

    Code - 

    ```dart
    import 'dart:io';
    
    import 'dart:math';
    
    void main(List<String> args) {
      var amount = double.parse(stdin.readLineSync());
      var interest = double.parse(stdin.readLineSync());
      var years = double.parse(stdin.readLineSync());
      print(amount*(pow((1+(0.01*interest)), years)));
    }
    ```

38. Write a Dart program to compute the distance between the points (x1, y1) and (x2, y2).

    Code - 

    ```dart
    import 'dart:io';
    
    import 'dart:math';
    
    void main(List<String> args) {
      var pos_1 = (stdin.readLineSync()).split(' ');
      var pos_2 = (stdin.readLineSync()).split(' ');
      var distance = pow(double.parse(pos_1[0]) - double.parse(pos_2[0]), 2) + pow(double.parse(pos_1[1]) - double.parse(pos_2[1]), 2);
      print(sqrt(distance)); 
    }
    ```

39. Write a Dart program to check whether a file exists.

    Code - 

    ```dart
    import 'dart:io';
    
    void main(List<String> args) {
      var filename = stdin.readLineSync();
      File(filename).exists().then((x) => print(x));
    }
    ```

40. Write a Dart program to get the number of processors.

    Code - 

    ```dart
    import 'dart:io' show Platform;
    
    main() {
      print(Platform.numberOfProcessors);
    }
    ```

41. Write a Dart program to get OS name, platform and release information.

    Code - 

    ```dart
    import 'dart:io' show Platform;
    
    void main() {
    print(" ${Platform.operatingSystemVersion}");
    }
    
    ```

42. Write a Dart program to call an external command in Dart.

    Code - 

    ```dart
    import 'dart:io';
    
    void main() {
    Process.run('ls', ['-l']).then((ProcessResult results) {
        print(results.stdout);
      });
    }
    
    ```

43. Write a Dart program to get the path and name of the file that is currently executing.

    Code - 

    ```dart
    import 'dart:io' show Platform;
    
    void main() {
    print(Platform.script);
    }
    
    ```

44. Write a Dart program to parse a string to Float or Integer.

    Code - 

    ```dart
    import 'dart:io';
    
    void main() {
      var value = stdin.readLineSync();
      int parse_int = int.parse(value);
      double parse_double = double.parse(value);
      print("Integer: $parse_int\nDouble: $parse_double");
    
    }
    ```

45. Write a Dart program to list all files in a directory.

    ```dart
    import 'dart:io';
    
    void main() {
      var currentDir = Directory('.');
      currentDir.list(recursive: true, followLinks: false)
        .listen((FileSystemEntity entity) {
          print(entity.path);
        });
    }
    ```

46. Write a Dart program to print without newline or space.

    ```dart
    import 'dart:io';
    
    void main() {
      for(int x=0; x<10; x++) {
        stdout.write("*");
      }
    }
    ```

47. Write a Dart program to print to stderr.

    ```dart
    import 'dart:io';
    
    void main() {
      stderr.write('Hello');
    }
    ```

48. Write a Dart program to access environment variables.

    ```dart
    import 'dart:io';
    
    void main() {
      print(Platform.environment);
    }
    ```

49. Write a Dart program to get the current username

    ```dart
    import 'package:system_info/system_info.dart';
    
    void main() {
      print(SysInfo.userName);
    }
    ```

50.  Write a Dart program to get height and width of the console window.

    ```dart
    import 'dart:io';
    
    void main() {
      print("Terminal Height: ${stdout.terminalLines}, Terminal Width: ${stdout
          .terminalColumns}");
    }
    ```

51.  Write a program to get execution time for a Dart method.

    ```dart
    void helloWorld() {
      print('Hello World');
    }
    
    void main() {
      final stopwatch = Stopwatch()..start();
      helloWorld();
      print('helloWorld() executed in ${stopwatch.elapsed}');
    }
    
    ```

52.  Write a Dart program to sum of the first n positive integers.

    ```dart
    import 'dart:io';
    
    void main() {
      var number = int.parse(stdin.readLineSync());
      var sum = 0;
      for (var x=1; x<=number; x++) {
        sum += x;
      }
      print('The sum is ${sum}');
    
    }
    ```

53.  Write a Dart program to convert height (in feet and inches) to centimetres.

    ```dart
    import 'dart:io';
    
    void main() {
      print('Enter the size:\t');
      var size = double.parse(stdin.readLineSync());
      print('Choose any one:\n1. Feet to Centimeter\n2. Inches to Centimeter');
      var choice = int.parse(stdin.readLineSync());
      if (choice == 1) {
        print('The size in Centimeter is: ${size * 30.48}');
      } else if (choice == 1) {
        print('The size in Centimeter is: ${size * 2.54}');
      }
    }
    
    ```

54. Write a Dart program to calculate the hypotenuse of a right angled triangle.

    ```dart
    import 'dart:io';
    import 'dart:math';
    
    void main() {
      stdout.write('Enter length of first side:\t');
      var side1 = double.parse(stdin.readLineSync());
      stdout.write('Enter length of second side:\t');
      var side2 = double.parse(stdin.readLineSync());
      var hypt = sqrt(pow(side1, 2) + pow(side2, 2));
      print('The hypotenuse of a right angled triangle is: ${hypt}');
    }
    ```

    
