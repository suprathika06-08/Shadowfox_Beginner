import java.util.ArrayList;
import java.util.Scanner;

class contact{
    private String name;
    private String phoneNumber;
    private String email;

    public contact(String name, String phoneNumber, String email){
        this.name = name;
        this.phoneNumber = phoneNumber;
        this.email = email;
    }

    public String getName(){
        return name;
    }
    public void setName(String name){
        this.name = name;
    }
    public String getPhoneNumber(){
        return phoneNumber;
    }
    public void setPhoneNumber(String phoneNumber){
        this.phoneNumber = phoneNumber;
    }
    public String getEmail(){
        return email;
    }
    public void setEmail(String email){
        this.email = email;
    }

    @Override
    public String toString(){
        return "Name: " + name + "\nPhone Number: " + phoneNumber + "\nEmail: " + email;
    }

}
public class contactManagement {
    private static ArrayList<contact> contacts = new ArrayList<>();

    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        while (true) {
            System.out.println("\nContact Management System");
            System.out.println("1. Add Contact");
            System.out.println("2. View Contacts");
            System.out.println("3. Update Contact");
            System.out.println("4. Delete Contact");
            System.out.println("5. Exit");
            System.out.print("Enter your choice: ");

            int choice = sc.nextInt();
            sc.nextLine();

            switch (choice) {
                case 1:
                    addContact(sc);
                    break;
                case 2:
                    viewContacts();
                    break;

                case 3:
                    updateContact(sc);
                    break;

                case 4:
                    deleteContact(sc);
                    break;

                case 5:
                    System.out.println("Exiting the System!");
                    sc.close();
                    return;

                default:
                    System.out.println("Invalid choice, please try again.");
            }
        }
    }

    private static void addContact(Scanner sc){
        System.out.print("Enter Name: ");
        String name = sc.nextLine();
        System.out.print("Enter phone number: ");
        String phoneNumber = sc.nextLine();
        System.out.print("Enter email address: ");
        String email = sc.nextLine();
        contacts.add(new contact(name, phoneNumber, email));
        System.out.println("Contact added successfully.");    
    }

    private static void viewContacts(){
        if (contacts.isEmpty()){
            System.out.println("No contacts available.");
        }
        else{
            System.out.println("Contact List: ");
            for(int i=0;i<contacts.size();i++){
                System.out.println((i + 1) + ". "+ contacts.get(i));
            }
        }
    } 

    private static void updateContact(Scanner sc){
        if (contacts.isEmpty()){
            System.out.println("No contacts available.");
            return;
        }
        viewContacts();
        System.out.print("Enter the contact number to update: ");
        int index = sc.nextInt() -1;
        sc.nextLine(); 
        if(index >= 0 && index < contacts.size()){
            contact cont = contacts.get(index);
            System.out.println("update contact: "+cont);

            System.out.print("Enter new name (leave blank to keep current): ");
            String name = sc.nextLine();
            if(!name.isEmpty()){
                cont.setName(name);
            }

            System.out.print("Enter new phone number (leave blank to keep current): ");
            String phoneNumber = sc.nextLine();
            if(!phoneNumber.isEmpty()){
                cont.setName(phoneNumber);
            }

            System.out.print("Enter new email address (leave blank to keep current): ");
            String email = sc.nextLine();
            if(!email.isEmpty()){
                cont.setName(email);
            }

            System.out.println("Contact updated successfully.");
        }
        else{
            System.out.println("Invalid Contact Number.");
        }
    }

    private static void deleteContact(Scanner sc){
        if (contacts.isEmpty()){
            System.out.println("No contacts available.");
            return;
        }
        viewContacts();
        System.out.print("Enter the contact number to delete: ");
        int index = sc.nextInt() -1;
        sc.nextLine();

        if(index >= 0 && index < contacts.size()){
            contacts.remove(index);
            System.out.println("Contact deleted successfully.");
        }
        else{
            System.out.println("Invalid Contact Number.");
        }
    }
}
