public class BankAccount {
    // Atributos públicos
    public double balance; // Saldo de la cuenta

    // Constructor para inicializar el saldo
    public BankAccount(double initialBalance) {
        this.balance = initialBalance;
    }

    // Método público para realizar un depósito
    public void depositAmount(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Depósito exitoso. Nuevo saldo: " + balance);
        } else {
            System.out.println("El monto a depositar debe ser mayor que 0.");
        }
    }

    // Método público para realizar un retiro
    public void withdrawAmount(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("Retiro exitoso. Nuevo saldo: " + balance);
        } else {
            System.out.println("Monto de retiro no válido o saldo insuficiente.");
        }
    }

    // Método público para mostrar el saldo
    public void displayBalance() {
        System.out.println("Saldo actual: " + balance);
    }

    // Método principal para probar las operaciones
    public static void main(String[] args) {
        // Crear una cuenta con un saldo inicial
        BankAccount myAccount = new BankAccount(500.0);
        
        // Mostrar el saldo inicial
        myAccount.displayBalance();
        
        // Realizar un depósito
        myAccount.depositAmount(200.0);
        
        // Realizar un retiro
        myAccount.withdrawAmount(100.0);
        
        // Mostrar el saldo final
        myAccount.displayBalance();
    }
}
