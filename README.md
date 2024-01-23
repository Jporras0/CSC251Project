# CSC251Project
 Repository for hosting the CSC251 Programming Project
public class InsuranceApp {
    public static void main(String[] args) {
       
        String policyNumber = getUserInput("Please enter the Policy Number: ");
        String providerName = getUserInput("Please enter the Provider Name: ");
        String firstName = getUserInput("Please enter the Policyholder’s First Name: ");
        String lastName = getUserInput("Please enter the Policyholder’s Last Name: ");
        int age = Integer.parseInt(getUserInput("Please enter the Policyholder’s Age: "));
        String smokingStatus = getUserInput("Please enter the Policyholder’s Smoking Status (smoker/non-smoker): ");
        int height = Integer.parseInt(getUserInput("Please enter the Policyholder’s Height (in inches): "));
        double weight = Double.parseDouble(getUserInput("Please enter the Policyholder’s Weight (in pounds): "));
        
        Policy policy = new Policy(policyNumber, providerName, firstName, lastName,
                age, smokingStatus, height, weight);

    
        displayPolicyDetails(policy);
    }

    
    private static String getUserInput(String prompt) {
        /*
        Scanner scanner = new Scanner(System.in);
        System.out.print(prompt);
        return scanner.nextLine();
        */
        return "SampleUserInput";  
    }


    private static void displayPolicyDetails(Policy policy) {
        System.out.println("\nSample Output:");
        System.out.println("Policy Number: " + policy.getPolicyNumber());
        System.out.println("Provider Name: " + policy.getProviderName());
        System.out.println("Policyholder’s First Name: " + policy.getPolicyholderFirstName());
        System.out.println("Policyholder’s Last Name: " + policy.getPolicyholderLastName());
        System.out.println("Policyholder’s Age: " + policy.getPolicyholderAge());
        System.out.println("Policyholder’s Smoking Status: " + policy.getSmokingStatus());
        System.out.println("Policyholder’s Height: " + policy.getHeightInInches() + " inches");
        System.out.println("Policyholder’s Weight: " + policy.getWeightInPounds() + " pounds");
        System.out.println("Policyholder’s BMI: " + policy.calculateBMI());
        System.out.println("Policy Price: $" + policy.calculateInsurancePrice());
    }
}
