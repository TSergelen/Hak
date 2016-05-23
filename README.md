import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class Log extends JFrame {

/**
	 * 
	 */
	

public static void main(String[] args) {
Log frameTabel = new Log();
}

JButton blogin = new JButton("Нэвтрэх");
JPanel panel = new JPanel();
JTextField txuser = new JTextField(20);
JPasswordField pass = new JPasswordField(20);

Log(){
super("Нэвтрэх хэсэг");
setSize(300,200);
setLocation(300,280);
panel.setLayout (null); 


txuser.setBounds(70,30,150,20);
pass.setBounds(70,65,150,20);
blogin.setBounds(110,110,80,20);

panel.add(blogin);
panel.add(txuser);
panel.add(pass);

getContentPane().add(panel);
setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
setVisible(true);
actionlogin();
}

public void actionlogin(){
blogin.addActionListener(new ActionListener() {
@SuppressWarnings("deprecation")
public void actionPerformed(ActionEvent ae) {
String puname = txuser.getText();
String ppaswd = pass.getText();
if(puname.equals("user1") && ppaswd.equals("12345")) {
newframe regFace =new newframe();
regFace.setVisible(true);
dispose();
} else {

JOptionPane.showMessageDialog(null,"Wrong Password / Username");
txuser.setText("");
pass.setText("");
txuser.requestFocus();
}

}
});
}
}
