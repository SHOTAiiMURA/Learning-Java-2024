# Learning-Java-2024

package xxxx;

public class Basic {
    public static void main(String[] args)
    {
        System.out.println("Hello World");
## Data Type
        int a = 1;
        // Precision 32 bit
        float b = 1.1F;
        // Precision 64 bit
        double c = 2.2;
## String Type
        String str = "Hello World";

        System.out.println(str + 1);
        //Hello World1
        System.out.println(1 + str);
        //1HelloWorld
        System.out.println(1 + 1 + str);
        //2Helloworld
        System.out.println(1 + 1 + "");
        //output("2")
        System.out.println("" + 1 + 1);
        //output("1" 1)
## for loop
        int sum = 0;
        for(int i = 0; i < 10; i++)
        {
            if(i % 2 == 0)
                continue;
            sum += i;

        }
        System.out.println(sum);
        //0,2,8,18,32
## While loop
//        sum = 0;
        int counter = 0;
        while(true)
        {
            counter++;
            System.out.println("Hello World");
            if(counter >= 5)
                break;
        }
## for loop but == while loop
        System.out.println();
        counter = 0;
        for(;;) {
            counter++;
            System.out.println("Hello World");
            if(counter >= 5)
                break;
        }
## Array
        int[] arr = new int[5];

        for(int i = 0; i < 5; i++)
        {
            arr[i] = i * i;
        }

        for(int i = 0; i < 5; i++)
        {
            System.out.println(arr[i] * 2);
        }
## Dimentional Array
        // 5 x 5
        // 5, 3, 7, 10
        int[][] arr_2d = new int[5][];

        for(int i = 0; i < 5; i++)
        {
        // input internal array number below. DO NOT INPUT ANY VALUE OF INTERNAL ARRAY.
            arr_2d[i] = new int[5];
        }
## Nested Loop
        for(int i = 0; i < 5; i++)
        {
            for(int j = 0; j < 5; j++)
            {
                arr_2d[i][j] = i * 5 + j;
            }
        }

        for(int i = 0; i < 5; i++)
        {
            for(int j = 0; j < 5; j++)
            {
                System.out.print(arr_2d[i][j] + ", ");
            }
            System.out.println();
        }
## Switch
        //switch: do not need to write if else sentence by writting below code.
        int input = 2;

        String mode = "Alpha";
        switch(mode)
        {
            case "Alpha" -> System.out.println("User Input 1 : Menu Mode");
            case "Bete" -> System.out.println("User Input 2 : Game Mode");
            case "Omega" -> System.out.println("User Input 3 : Finance App");
        }

        sum = 0;
        for(int i = 0; i < 30; i++)
        {
            if(i % 3 == 0)
                sum += i;
        }
        System.out.println(sum);
    }
}
# Class, Inheritance, Override, Overload, Getter/Setter 
package xxx;

public class Car {
### public, private, protected: public is able to look from outside, private is not able to look from outside, protected is accessible in the same package and in subclasses
<img width="712" alt="Screenshot 2024-05-25 at 15 57 58" src="https://github.com/SHOTAiiMURA/Learning-Java-2024/assets/91776514/ecef47f3-05bf-4b3d-a399-ba5c4dc78960">

### Encapsulation
    private int weight;
    private int height;
    private int noWheel;
    private  int noSheet;

## Constructor
    // Manual
    public Car(int weight, int height, int noWheel, int noSheet)
    {
        this.weight = weight;
        this.height = height;
        this.noWheel = noWheel;
        this.noSheet = noSheet;
        verifyCar();
    }

    // Sendan
## Overload
    public Car(int weight, int height)
    {
        this(weight, height, 4, 4);
    }

## Getter Setter
    public int getWeight(){
        return weight;
    }

    public int getNoWheel() {
        return noWheel;
    }

    public int getNoSheet() {
        return noSheet;
    }

    public String describeYourself()
    {
        return String.format("Weight %d, Height %d, Wheel %d, Sheet %d", weight, height, noWheel, noSheet);
    }

    public boolean verifyCar()
    {
        if(noWheel == 2 && noSheet == 2)
        {
            System.out.println("Coupe Created");
            return true;
        }
        else if(noWheel == 4 && noSheet == 4)
        {
            System.out.println("Sedan Created");
            return true;
        }
        else{
            System.out.println("Invalid car type");
            return false;
        }
    }

    public static void IdentifyCarType(int noWheel, int noSheet)
    {
        if(noWheel == 2 && noSheet == 2)
        {
            System.out.println("Coupe");
        }
        else if(noWheel == 4 && noSheet == 4)
        {
            System.out.println("Sedan");
        }
        else{
            System.out.println("Invalid car type");
        }
    }
}
