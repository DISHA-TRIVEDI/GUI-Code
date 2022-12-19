# GUI-Code
import java.awt.Color;
import javax.swing.*;
import javax.swing.plaf.PanelUI;
public class createGUI implements ActionListener{
   int count=0;

    public createGUI(){
     
     JButton button= new JButton("Click Me");
     button.setBounds(9,5, 9, 5);
     button.setVisible(true);
     button.addActionListener(this);
     JLabel label= new JLabel("Number of clicks= 0");
     label.setVisible(true);

     JPanel panel= new JPanel();
     panel.setBackground(Color.YELLOW);
     panel.setBounds(20, 30, 40, 30);
     panel.setEnabled(true);
    
     panel.add(button);
     panel.add(label);

     JFrame frame= new JFrame();
     frame.setLayout(null);
     frame.setBounds(20, 30, 40, 30);;
     frame.setTitle("GUI by SWING");

     frame.add(panel);
    }

    public static void main(String[] args) {
        newGUI ng= new newGUI();

    }
    @Override
    public void action(ActionEvent e) {
        count++;
        JLabel label= new JLabel();
        label.setText("Number of clicks= "+ count);
    }
}
