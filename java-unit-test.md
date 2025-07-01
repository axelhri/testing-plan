# Example de Test Unitaire Java

## Example simple

Cette methode de test vérifie que la variable `result` renvoie bien true.

```java
@Service
public class CalculatorService {
    public int add(int a, int b) {
        return a + b;
    }
}
```

```java
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;

public class CalculatorServiceTest {

    private final CalculatorService calculatorService = new CalculatorService();

    @Test
    void testAdd() {
        int result = calculatorService.add(3, 4);
        assertEquals(7, result);
    }
}
```
