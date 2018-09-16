# JavaDigitalClock
* Java Digital Clock * World Short Code only 46 lines In AWT Not Swings

# Lib Used are
*java.util.; <br>
*java.text.; <br>
*java.awt 

# Developers Info 
<br>
   Made By:- <b>Tejas Sanjay Chaudhari</b><br>
   Co-Founder :- <b> kiranazone.com </b><br>
  Mail:-  <b>  tejaschaudhari038@gmail.com </b><br>
   Phone :- <b> <a href="tel:9158110065">+91 9158110065</a></b> 
<hr>
<center><i style="color:royalblue">Love And Joy</i>
</center>

# code

import java.util.*;
import java.text.*;
import java.awt.*;

public class time{

  public static void main(String args[]){
  
  timeShow ts = new timeShow();
  ts.showFrame();

 }
 }

 class timeShow{
    
    Frame f = new Frame();
    Date date = new Date();
    Timer timer = new Timer();
    Label TimeLabel = new Label();
    Label DateLabel = new Label();
    SimpleDateFormat tFormat = new SimpleDateFormat("dd/MM/yyy");
    SimpleDateFormat tTime = new SimpleDateFormat("hh:mm:ss");

    public String time;
    public String dateS;
     
     void showFrame(){

      TimerTask task = new TimerTask(){
     
      public void run(){
     
      Date date = new Date();
      time = tTime.format(date);
      dateS = tFormat.format(date); 
      
      TimeLabel.setText(time);
      DateLabel.setText(dateS);

     }
    };

    timer.scheduleAtFixedRate(task,0,1*1000);

    DateLabel.setBounds(150,200,200,50);
    DateLabel.setBackground(Color.yellow);
    DateLabel.setForeground(Color.blue);
    DateLabel.setFont(new Font("Courier New", Font.PLAIN,23));
    DateLabel.setAlignment(Label.CENTER);
   
    TimeLabel.setBackground(Color.blue);
    TimeLabel.setForeground(Color.white); 
    TimeLabel.setBounds(150,70,200,80);
    TimeLabel.setFont(new Font("Castellar", Font.PLAIN,30));
    TimeLabel.setAlignment(Label.CENTER);
   
    f.add(TimeLabel);
    f.add(DateLabel);  
    f.setTitle("Digital Clock");
    f.setSize(500,300);
    f.setLayout(null);
    f.setVisible(true);
 }
}

# Run
To run the project from the command line, go to the dist folder and type the following:

java  "time.java" 
 
# ScreenShoot

jtejas.png
