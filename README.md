import static org.junit.Assert.*;
import org.junit.Before;
import org.junit.Test;

public class AccountTest {
    private Account account;

    @Before
    public void setUp() {
        account = new Account("12345", 0); // Creació del compte bancari amb saldo inicial 0
    }

    @Test
    public void testDepositAmount() {
        account.depositAmount(100);
        assertEquals(100, account.getBalance(), 0);  // Verificar que el saldo és de 100 després del dipòsit
    }

    @Test(expected = IllegalArgumentException.class)
    public void testDepositNegativeAmount() {
        account.depositAmount(-50); // Prova per verificar la gestió de quantitats negatives
    }

    @Test
    public void testWithdrawAmount() {
        account.depositAmount(100);  // Dipositar 100
        account.withdrawAmount(50);  // Retirar 50
        assertEquals(50, account.getBalance(), 0);  // Verificar que el saldo final és de 50
    }

    @Test(expected = IllegalArgumentException.class)
    public void testWithdrawInsufficientBalance() {
        account.withdrawAmount(200); // Saldo insuficient per retirar
    }
}
