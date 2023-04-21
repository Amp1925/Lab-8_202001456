# Lab-8_202001456

### Amol Patel
### 202001456
## Creating a new Eclipse project, a package, and a class definition within that project

![image](https://user-images.githubusercontent.com/115399432/233604913-4ef046a1-5eb5-4d24-b8b9-48bab805c6f9.png)

## Adding Test Case

```
  public class BoaTest {
  Boa jen;
  Boa ken;

  @Before
  public void setUp() throws Exception {                                                           
    jen = new Boa("Jennifer", 2, "grapes");
    ken = new Boa ("Kenneth", 3, "granola bars");
  }

  @After
  public void tearDown() throws Exception {
  }

  @Test
    public void testIsHealthy() {
        assertTrue(ken.isHealthy()); // kens favourite food is granola bars
        assertFalse(jen.isHealthy());
    }

    @Test
    public void testFitsInCage() {
        assertFalse(ken.fitsInCage(2));
        assertFalse(ken.fitsInCage(3));
        assertTrue(ken.fitsInCage(5));

        assertFalse(jen.fitsInCage(1));
        assertFalse(jen.fitsInCage(2));
        assertTrue(jen.fitsInCage(3));
    }
}
```

## Running Test Case

![image](https://user-images.githubusercontent.com/115399432/233607149-64661d4b-a71d-48b7-b8d6-8d79b334e2ac.png)

## New method being added to the Boa class

```
public int lengthInInches(){
	// 1 foot is 12 inches
	return this.length*12;
}
```

![image](https://user-images.githubusercontent.com/115399432/233608358-8feb78a3-7569-405c-9e74-b48da1f34636.png)

## Updating the lengthInInches() test with new test cases

```
@Test
public void testlengthInInches() {
	assertEquals("error in lengthInInches()",  36, ken.lengthInInches());
	assertNotEquals("error in lengthInInches()",  35, ken.lengthInInches());
    
	assertEquals("error in lengthInInches()",  24, jen.lengthInInches());
	assertNotEquals("error in lengthInInches()",  30, jen.lengthInInches());
}
```

## Running new Test Case

![image](https://user-images.githubusercontent.com/115399432/233609094-455a62a4-2191-4b55-a0a8-99e947cbd8e0.png)




