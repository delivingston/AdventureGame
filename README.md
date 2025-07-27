This program is a good adventure game that utilizes a simple user interface to choose from, with input from the console. Here is the code of the game. The game also uses switch statements.

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

       System.out.println("Welcome to the Ultimate Adventure Game!");
       System.out.println("Your goal is to find the hidden treasure. Choose wisely!");

       System.out.println("You are at a crossroad. Do you wan to go left or right?");
       System.out.println("Type 'left' or 'right': ");

        Scanner scanner = new Scanner(System.in);
        String choice1 = scanner.nextLine().toLowerCase();

        switch (choice1){
            case "left":
                System.out.println("You walk down a dark path to find a mysterious cave.");
                System.out.println("Do you want to enter the cave or walk past it?");
                System.out.println("Type 'enter' or 'walk': ");
                String choice2 = scanner.nextLine().toLowerCase();
                switch (choice2){
                    case "enter":
                        System.out.println("Inside the cave, you found a sleeping dragon!");
                        System.out.println("Do you want to fight the dragon or sneak past it? ");
                        System.out.println("Type 'fight' or 'sneak': ");
                        String choice3 = scanner.nextLine().toLowerCase();
                        switch (choice3){
                            case "fight":
                                System.out.println("You bravely fought the dragon and...");
                                System.out.println("You are victorious! The dragon guards the treasure. You win!");
                                break;
                            case "sneak":
                                System.out.println("You sneak past the dragon and found the treasure behind the dragon. You win!");
                                break;
                            default:
                                System.out.println("Invalid choice. You got caught by the dragon. You lost!");
                                break;
                        }
                        break;
                    case "walk":
                        System.out.println("You walked past the cave and fall into a hidden trap. Game over!");
                        break;
                    default:
                        System.out.println("\"Invalid choice. You got lost in the wilderness.");
                        break;
                }
                break;
            case "right":
                System.out.println("You walked through a dense forest and found a river.");
                System.out.println("Do you want to swim across or build a raft?");
                System.out.println("Type 'swim' or 'raft': ");
                String choice2b = scanner.nextLine().toLowerCase();
            switch (choice2b){
                case "swim":
                    System.out.println("You swim across the river and encounter a wild bear!");
                    System.out.println("Do you want to run away or climb a tree?");
                    System.out.println("Type 'run' or 'climb': ");
                    String choice3b = scanner.nextLine().toLowerCase();
                    switch (choice3b){
                        case "run":
                            System.out.println("You ran away safely and find a hidden path to the treasure. You win!");
                            break;
                        case "climb":
                            System.out.println("You climb the tree, but the bear waits for you. You are stuck. Game over!");
                            break;
                        default:
                            System.out.println("Invalid choice. The bear catches you. Game over!");
                            break;
                    }
                    break;
                case "raft":
                    System.out.println("You built a raft and safely cross the river. You found the treasure on the other side. You Win!");
                    break;
                default:
                    System.out.println("Invalid choice. You got swept away by the river. Game over!");
                    break;
            }
                break;
            default:
                System.out.println("Invalid choice. You got lost in the wilderness.");
        }

        scanner.close();
    }
}
