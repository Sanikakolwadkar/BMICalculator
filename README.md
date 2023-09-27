import javax.swing.JOptionPane;

public class bmi2 {
    public static void main(String[] args) {
        String weightInput = JOptionPane.showInputDialog("Enter your weight (in kilograms):");
        String heightInput = JOptionPane.showInputDialog("Enter your height (in meters):");
        
        double weight = Double.parseDouble(weightInput);
        double height = Double.parseDouble(heightInput);
        
        double bmi = calculateBMI(weight, height);
String category = interpretbmi2(bmi);

        
        JOptionPane.showMessageDialog(null, "Your BMI is: " + bmi);
		 JOptionPane.showMessageDialog(null, "Your BMI Category is: " + category);
    }
    
    public static double calculateBMI(double weight, double height) {
        return weight / (height * height);
}
 public static String interpretbmi2(double bmi) {
        if (bmi < 18.5) {
            return "Underweight";
        } else if (bmi >= 18.5 && bmi < 25) {
            return "Normal Weight";
        } else if (bmi >= 25 && bmi < 30) {
            return "Overweight";
        } else {
            return "Severe Obesity";
        }
   
    }
}
