# Java-Swing-GUI-Part-21
Java Swing GUI Part#21:JTree creation using DefaultMutableTreeNode class |JTree Components &amp; Methods
import java.util.*;
import javax.swing.*;
import java.awt.*;


public class Test1 extends JFrame {
	public static void main(String[] args) {
		new Test1();

	}

	public Test1() {
		setSize(640,400);
		setTitle("JFrame");
		

		setLayout(new GridLayout(5,5));

		JLabel label = new JLabel("Beethoven vs Bruce Lee");
		add(label);
		
		JButton button = new JButton("my button");
		add(button);

		JTextField field = new JTextField("High Life");
		add(field);

		JPasswordField password = new JPasswordField("Daft Punk");
		add(password);

		JTextArea area = new JTextArea();
		JScrollPane scroll = new JScrollPane(area);
		add(scroll); 

		JCheckBox box = new JCheckBox("chupalo");
		add(box);
		
		JPanel panel = new JPanel();
		//TitledBorder title = BorderFactory.createTitledBorder("Hello");
		//setBorder(title);

		JRadioButton radio = new JRadioButton("aa");
		JRadioButton radio1 = new JRadioButton("aa");
		
		
		ButtonGroup group = new ButtonGroup();
		group.add(radio);
		group.add(radio1);

		panel.add(radio);
		panel.add(radio1);
		add(panel);
		
		
		String[] myListItems = new String[] {"itme1", "item2", "item3"};
		JList<String> myList = new JList<String>(myListItems);
		
		add(myList);
		
		String[] myCombo = new String[] {"itme1", "item2", "item3"};
		JComboBox<String> comboBox = new JComboBox<String>(myCombo);		
		add(comboBox); 

		JSlider mySlider = new JSlider(0,100,30);
		add(mySlider);
		String a1 = "Harder";
		String a2 = "Better";
		String a3 = "Faster";
		DefaultMutableTreeNode tree1 = new DefaultMutableTreeNode(a1);
		DefaultMutableTreeNode branch1 = new DefaultMutableTreeNode(a2);
		DefaultMutableTreeNode branch2 = new DefaultMutableTreeNode(a3);
		
		tree1.add(branch1);
		tree1.add(branch2);

		JTree myTree = new JTree(tree1);
		add(myTree);		

		setVisible(true);
		setDefaultCloseOperation(EXIT_ON_CLOSE);		
		
		
	}
}
