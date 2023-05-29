# Java-Insert-elements-into-the-array

## AIM:
To write a java program insert elements into array.

## PROCEDURE:
1. Create a Scanner object to read user input.
2. Prompt the user to enter the size of the array.
3. Create an array of the specified size and prompt the user to enter the elements of the array.
4. Iterate over the array size and store each element in the array and prompt the user to enter the element to be inserted.
5. Prompt the user to enter the position where the element should be inserted, check if the position is valid or not and specify the condition.
6. Create a new array with increased size.
7. Copy the elements from the original array to the new array up to the specified position.
8. Insert the element at the specified position.
9. Copy the remaining elements from the original array to the new array.
10. Print the updated array using Arrays.toString() method.

## PROGRAM:
```
import java.util.Arrays;
import java.util.Scanner;

public class Test {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the size of the array: ");
        int size = sc.nextInt();
        int[] array = new int[size];
        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < size; i++) {
            array[i] = sc.nextInt();
        }
        System.out.print("Enter the element to be new inserted: ");
        int element = sc.nextInt();
        System.out.print("Enter the position to insert the element: ");
        int position = sc.nextInt();
        if (position < 0 || position > size) {
            System.out.println("Invalid position. Please enter a valid position.");
            return;
        }
        int[] newArray = new int[size + 1];

        for (int i = 0; i < position; i++) {
            newArray[i] = array[i];
        }
        newArray[position] = element;
        for (int i = position; i < size; i++) {
            newArray[i + 1] = array[i];
        }
        System.out.println("Array after inserting the element:");
        System.out.println(Arrays.toString(newArray));
    }
}
```

## OUTPUT:
```
C:\Users\Dell\.jdks\openjdk-19.0.2\bin\java.exe "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.3.3\lib\idea_rt.jar=9596:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.3.3\bin" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath "C:\Users\Dell\IdeaProjects\java full stack\out\production\java full stack" Test
Enter the size of the array: 5
Enter the elements of the array:
1
2
3
4
5
Enter the element to be new inserted: 6
Enter the position to insert the element: 5
Array after inserting the element:
[1, 2, 3, 4, 5, 6]

Process finished with exit code 0
```
## RESULT:
Thus the java program to insert elements into an array is created and the output is verified.
