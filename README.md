Prerequisites:
1) [JDK 8](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
2) [IntelliJ](https://www.jetbrains.com/idea/download/#section=windows)
3) [Maven] (https://maven.apache.org/)

Run the program:
- Run 'mvn clean install' in the terminal.
- Go to the input file under resources and apply correct input.
- Go to the IsFlush class and run its main method.
- Go to output file (under resources) and check the output.
- Type 'mvn test' in the terminal to run the unit tests.


Brief description of the algorithm:

We have one general method that is called isFlush. It takes String array and returns boolean based
on the input from the file. Inside that method we check two things (methods):

  1) areSameColor() - takes the list of cards, extract the color of each and compares every element
  with the next one.
  If some of the elements is not the same color as the previous one - we don't have Flush for sure
  and we exit the method returning false.

  2) areConsecutive() - takes the list of cards, extract the card rank of each. It converts
  Ten, Jack, Queen, King and Ace to integer representations so we can sort them and check if
  they are consecutive.
    *We have a special case check here - the case when we have Straight with 2, 3, 4 ,5 and Ace.
    If so we return true (as they are consecutive by the Poker rules).
