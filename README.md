/*Write a (GUI0 application in which you declare an array of 10 first names.
  Write a try block in which you prompy the user for an integer and display
  the name in the requested position(index).Create a catch block that catches the potential
  ArrayIndexOutOfBoundsException thrown when the user enters a number that is out of range .
  The catch block also should display an error message.
*/

package codewithsyre;

import javax.swing.*;

public class Application {

    public static void main(String[] args) {

   // create an array of String type which contains 10 elements /names
        String[] names = {"August", "Jaden", "Jackson", "Chris", "Kanye", "Harray", "Sean", "Taylor", "Drake", "Winfred"};

 /* We create Try-Catch Exception  to handle the Exception if the user enters invalid integer
     or the number that is out of the range of element 1 to 10
  */
        try {
            // Allow the user to enter any integer from 1 to 10
            String input = JOptionPane.showInputDialog("Enter an integer from 1 to 10 to display the name");
            int arrayElementNum =Integer.parseInt(input);
            // storing the index Number
             int indexNum=arrayElementNum-1;
            JOptionPane.showMessageDialog(null,names[indexNum]);

        } catch (ArrayIndexOutOfBoundsException e) {

            JOptionPane.showMessageDialog(null, "INVALID INPUT...\nNumber out of range","WARNING", JOptionPane.WARNING_MESSAGE);

        } catch (Exception e) {
            e.printStackTrace();
        }

    }
}
