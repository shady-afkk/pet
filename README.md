# pet
using System;

class VirtualPet
{
    private string name;
    private int age;
    private int health;
    private int hunger;

    public VirtualPet(string name)
    {
        this.name = name;
        age = 0;
        health = 100;
        hunger = 0;
    }

    public void ShowStatus()
    {
        Console.WriteLine($"{name} is {age} years old.");
        Console.WriteLine($"{name} has {health} health.");
        Console.WriteLine($"{name} has {hunger} hunger.");
    }

    public void Play()
    {
        if (age >= 3)
        {
            Console.WriteLine($"{name} is too old to play. :(");
            return;
        }

        Console.WriteLine($"{name} is playing. :D");
        health += 10;
        hunger += 5;
 public void Feed()
 {
     if (hunger <= 0)
     {
         Console.WriteLine($"{name} is not hungry. :D");
         return;
     }

     Console.WriteLine($"{name} is being fed. :D");
     health += 10;
     hunger -= 10;
 }

 public void Sleep()
 {
     if (age < 3)
     {
         Console.WriteLine($"{name} is too young to sleep. :(");
         return;
     }

     Console.WriteLine($"{name} is sleeping. Zzz");
     health += 10;
     hunger += 5;
 }
