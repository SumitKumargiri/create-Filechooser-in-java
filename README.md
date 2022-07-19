# create-Filechooser-in-java
import javax.swing.*;
import java.awt.event.*;

class fr12 extends JFrame implements ActionListener {
    JTextField tf;
    JButton bt;
    JFileChooser JFC;

    fr12() {
        setLayout(null);
        setLocationRelativeTo(null);

        tf = new JTextField();
        tf.setBounds(50, 100, 200, 30);
        add(tf);

        bt = new JButton("Browse");
        bt.setBounds(100, 150, 100, 30);
        add(bt);
        bt.addActionListener(this);

        JFC = new JFileChooser("c://");
        JFC.setFileSelectionMode(JFileChooser.FILES_AND_DIRECTORIES);
        // add(JFC);

        setSize(500, 500);
        setVisible(true);
    }

    @Override
    public void actionPerformed(ActionEvent e) {
        int ans = JFC.showOpenDialog(this);
        if (ans == JFileChooser.APPROVE_OPTION) {
            tf.setText("Cancel Clicked.....");
        }
    }

    public static void main(String args[]) {
        fr12 obj = new fr12();
    }
}

/* output:- ![image](https://user-images.githubusercontent.com/96234273/179653539-e9cded32-5463-4d4a-9557-3dd5dc0e5fd0.png)
click on Browse then the files or folder of this pc.
![image](https://user-images.githubusercontent.com/96234273/179653746-19bfe34c-7872-462c-8281-66219bc3915a.png)
*/
