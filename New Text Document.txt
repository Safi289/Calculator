package calculator;

import java.awt.Dimension;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.BorderFactory;
import javax.swing.ImageIcon;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.JTextArea;
import javax.swing.border.Border;


public class Calculator implements ActionListener{

    JFrame frame = new JFrame("calculator");
    JPanel panel = new JPanel();
    JTextArea textarea = new JTextArea(2,10);
    JButton button1 = new JButton();
    JButton button2 = new JButton();
    JButton button3 = new JButton();
    JButton button4 = new JButton();
    JButton button5 = new JButton();
    JButton button6 = new JButton();
    JButton button7 = new JButton();
    JButton button8 = new JButton();
    JButton button9 = new JButton();
    JButton button0 = new JButton();
    JButton buttonadd = new JButton();
    JButton buttonsub = new JButton();
    JButton buttonmul = new JButton();
    JButton buttondiv = new JButton();
    JButton buttonclear = new JButton();
    JButton buttondot = new JButton();
    JButton buttonequal = new JButton();
    
    double num1,num2,res;
    int add=0, sub=0, mul=0, div=0;
    
    public Calculator(){
        frame.setSize(340,400);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
        frame.add(panel);
        panel.add(textarea);
        textarea.setPreferredSize(new Dimension(2,10));
        textarea.setLineWrap(true);
        
        button1.setPreferredSize(new Dimension(100,43));
        button1.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\button.jpg"));
        
        button2.setPreferredSize(new Dimension(100,43));
        button2.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\2.png"));
        
        button3.setPreferredSize(new Dimension(100,43));
        button3.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\3.jpg"));
        
        button4.setPreferredSize(new Dimension(100,43));
        button4.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\4.png"));
        
        button5.setPreferredSize(new Dimension(100,43));
        button5.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\5.jpg"));
        
        button6.setPreferredSize(new Dimension(100,43));
        button6.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\6.jpg"));
        
        button7.setPreferredSize(new Dimension(100,43));
        button7.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\7.jpg"));
        
        button8.setPreferredSize(new Dimension(100,43));
        button8.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\8.jpg"));
        
        button9.setPreferredSize(new Dimension(100,43));
        button9.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\9.jpg"));
        
        button0.setPreferredSize(new Dimension(100,43));
        button0.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\0.jpg"));
        
        buttonadd.setPreferredSize(new Dimension(100,43));
        buttonadd.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\add.jpg"));
        
        buttonsub.setPreferredSize(new Dimension(100,43));
        buttonsub.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\sub.jpg"));
        
        buttonmul.setPreferredSize(new Dimension(100,43));
        buttonmul.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\mul.jpg"));
        
        buttondiv.setPreferredSize(new Dimension(100,43));
        buttondiv.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\div.jpg"));
        
        buttonclear.setPreferredSize(new Dimension(100,43));
        buttonclear.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\c.jpg"));
        
        buttondot.setPreferredSize(new Dimension(100,43));
        buttondot.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\dot.jpg"));
        
        buttonequal.setPreferredSize(new Dimension(100,43));
        buttonequal.setIcon(new ImageIcon("C:\\Users\\Rafi\\Pictures\\equal.png"));
      
        
        panel.add(button1);
        panel.add(button2);
        panel.add(button3);
        panel.add(button4);
        panel.add(button5);
        panel.add(button6);
        panel.add(button7);
        panel.add(button8);
        panel.add(button9);
        panel.add(button0);
        
        panel.add(buttonadd);
        panel.add(buttonsub);
        panel.add(buttonmul);
        panel.add(buttondiv);
        panel.add(buttonclear);
        panel.add(buttondot);
        
        panel.add(buttonequal);
        
        button1.addActionListener(this);
        button2.addActionListener(this);
        button3.addActionListener(this);
        button4.addActionListener(this);
        button5.addActionListener(this);
        button6.addActionListener(this);
        button7.addActionListener(this);
        button8.addActionListener(this);
        button9.addActionListener(this);
        button0.addActionListener(this);
        buttonadd.addActionListener(this);
        buttonsub.addActionListener(this);
        buttonmul.addActionListener(this);
        buttondiv.addActionListener(this);
        buttonclear.addActionListener(this);
        buttondot.addActionListener(this);
        buttonequal.addActionListener(this);
        
    }

    @Override
    public void actionPerformed(ActionEvent e) {
        Object source = e.getSource();
        if(source == buttonclear){
            num1 = 0.0;
            num2 = 0.0;
            textarea.setText("");
        }
        if(source == button1)
            textarea.append("1");
        if(source == button2)
            textarea.append("2");
        if(source == button3)
            textarea.append("3");
        if(source == button4)
            textarea.append("4");
        if(source == button5)
            textarea.append("5");
        if(source == button6)
            textarea.append("6");
        if(source == button7)
            textarea.append("7");
        if(source == button8)
            textarea.append("8");
        if(source == button9)
            textarea.append("9");
        if(source == button0)
            textarea.append("0");
        if(source == buttondot)
            textarea.append(".");
        //throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
       if(source == buttonadd){
           num1=numberreader();
           textarea.setText("");
           add= 1;
           sub=0;
           mul=0;
           div=0;
       }
       if(source == buttonsub){
           num1=numberreader();
           textarea.setText("");
           add= 0;
           sub=1;
           mul=0;
           div=0;
       }
       if(source == buttonmul){
           num1=numberreader();
           textarea.setText("");
           add= 0;
           sub=0;
           mul=1;
           div=0;
       }
       if(source == buttondiv){
           num1=numberreader();
           textarea.setText("");
           add= 0;
           sub=0;
           mul=0;
           div=1;
       }
       if(source == buttonequal){
           num2=numberreader();
           if(add > 0){
               res = num1+num2;
               textarea.setText(Double.toString(res));
           }
           if(sub > 0){
               res = num1-num2;
               textarea.setText(Double.toString(res));
           }
           if(mul > 0){
               res = num1*num2;
               textarea.setText(Double.toString(res));
           }
           if(div > 0){
               res = num1/num2;
               textarea.setText(Double.toString(res));
           }
      
       }
        
    }
     public double numberreader(){
            double num1;
            String s;
            s=textarea.getText();
            num1=Double.valueOf(s);
            return num1;
   
    
}

}