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

## Exemple Concret avec Mockito

Cette methode de test vérifie que le nom de l'utilisateur trouvé est bien égal à `"Axel"`, si oui le test passe.

```java
    @Override
    public String getStudent(UUID studentId) {
        return studentRepository.findById(studentId).map(Student::getName).orElse("L'étudiant n'éxiste pas");
    }
```

```java
@ExtendWith(MockitoExtension.class)
class StudentServiceTest {

    @Mock
    StudentRepository studentRepository;

    @InjectMocks
    StudentService studentService;

    @Test
    void getStudent() {
        /* Arrange */
        Student student = new Student(
                "Axel",
                "axel@gmail.com",
                LocalDate.of(2000,04,03)
        );

        Mockito.when(studentRepository.findById(student.getId())).thenReturn(Optional.of(student));

        /* Act */
        String result = studentService.getStudent(student.getId());

        /* Assert */
        Assertions.assertEquals("Axel", result);
    }
}
```
