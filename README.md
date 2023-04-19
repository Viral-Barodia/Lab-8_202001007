# Lab-8_202001007
Lab-8

### 3. To test the Boa class:

#### Code:

import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {

    private Boa healthyBoa;
    private Boa unhealthyBoa;

    @Before
    public void setUp() throws Exception {
        healthyBoa = new Boa("Healthy Boa", 6, "granola bars");
        unhealthyBoa = new Boa("Unhealthy Boa", 8, "mice");
    }

    @Test
    public void testIsHealthy() {
        assertTrue(healthyBoa.isHealthy());
        assertFalse(unhealthyBoa.isHealthy());
    }

    @Test
    public void testFitsInCage() {
        assertTrue(healthyBoa.fitsInCage(7));
        assertFalse(unhealthyBoa.fitsInCage(6));
    }

}


#### Explanation:

We first import the necessary JUnit classes and the Boa class we want to test.
We then create two Boa objects in the setUp() method. One is a healthy Boa and the other is an unhealthy one.
In the testIsHealthy() method, we test the isHealthy() method of both Boa objects. We expect the healthy Boa to be healthy and the unhealthy Boa to be unhealthy.
In the testFitsInCage() method, we test the fitsInCage() method of both Boa objects. We expect the healthy Boa to fit in a cage of length 7 and the unhealthy Boa not to fit in a cage of length 6.
We use the assertTrue() and assertFalse() methods to make assertions about the expected results of the methods being tested.

### 4. Modifying the set-up method

#### Code:

public class BoaTest {

    private Boa jen;
    private Boa ken;

    @Before
    public void setUp() throws Exception {
        jen = new Boa("Jennifer", 2, "grapes");
        ken = new Boa("Kenneth", 3, "granola bars");
    }

    // test methods go here
}

#### Explanation
This creates two Boa objects named jen and ken with different values for their name, length, and favorite food properties. The jen object has a name of "Jennifer", a length of 2 feet, and a favorite food of "grapes". The ken object has a name of "Kenneth", a length of 3 feet, and a favorite food of "granola bars". The private fields jen and ken are added to the BoaTest class so that they can be accessed in the test methods.
