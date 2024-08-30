
import java.util.*;

class rock_paper_scissor {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("make a move!(rock/paper/scissor)");
        String player_move = sc.nextLine();
        Random rand = new Random();
        int randdomnum = rand.nextInt(3);
        String computer_move;

        if (randdomnum == 0) {
            computer_move = "rock";
        } else if (randdomnum == 1) {
            computer_move = "paper";
        } else {
            computer_move = "scissor";
        }

        System.out.println("Computer chose: " + computer_move);

        if (player_move.equals("rock")) {
            if (computer_move.equals("rock")) {
                System.out.println("It's a tie!");
            } else if (computer_move.equals("paper")) {
                System.out.println("You lose!");
            } else {
                System.out.println("You win!");
            }
        } else if (player_move.equals("paper")) {
            if (computer_move.equals("paper")) {
                System.out.println("It's a tie!");
            } else if (computer_move.equals("scissor")) {
                System.out.println("You lose!");
            } else {
                System.out.println("You win!");
            }
        } else if (player_move.equals("scissor")) {
            if (computer_move.equals("scissor")) {
                System.out.println("It's a tie!");
            } else if (computer_move.equals("rock")) {
                System.out.println("You lose!");
            } else {
                System.out.println("You win!");
            }
        } else {
            System.out.println("Invalid move!");
        }
    }
}

