# pkmassofttestjunit5
## What’s New In JUnit 5
### JUnit 5 motivation
### JUnit 5 inception
####　Test Engine SPI
two engine
- junit-vintage-engine
- junit-jupiter-engine


## JUnit 5 Standard Tests
### Test lifecycle
junit 5 annotation:
- @BeforeEach
- @AfterEach
- @BeforeAll
- @AfterAll

### Test instance lifecycle
This default behavior can be changed in JUnit 5, simply by annotating a test class with ```@TestInstance(Lifecycle.PER_CLASS)```. 

### Skipping tests
```
import org.junit.jupiter.api.Disabled;
import org.junit.jupiter.api.Test;
class DisabledTest {    
  @Disabled    
  @Test    
  void skippedTest() {    
  }
}
```

### Display names
```
import org.junit.jupiter.api.DisplayName;
```


### Asserting exceptions
```
import static org.junit.jupiter.api.Assertions.assertEquals;
import static org.junit.jupiter.api.Assertions.assertThrows;
import org.junit.jupiter.api.Test;
class ExceptionTest {    
@Test    
void exceptionTesting() {          
  Throwable exception = assertThrows(IllegalArgumentException.class,() -> {
  throw new IllegalArgumentException("a message");});         
  assertEquals("a message", exception.getMessage());   
}
}
```
