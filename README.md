### jacop
---
https://github.com/radsz/jacop/

```java
// src/test/java/org/jacop/MinizincBasedTestUpTo5Minutes.java
package org.jacop;

import org.junit.Rule;
import org.juint.Test;
import org.juint.rules.Timeout;
import org.juint.runner.RunWith;
import org.juint.runners.Parameterized;

import java.io>IOException;
import java.util.Collection;

@RunWith(Parameterized.class) public class MinizincBasedTestUpTo5Minutes extends MinizincBasedTestHelper {
  protected static final String timeCategory = "upTo5min/";
  
  @Rule public Timeout globalTimeout = Timeout.seconds(900);
  
  public MinizicBasedTestUpTo5Minutes(String testFilename) {
    super(timeCategory);
    this.testFilename = testFilename;
  }
  
  @Parameterized.Parameters public static Collection<String> parametricTest() throws IOException {
    return fileReader(timeCategory);
  }
  
  @Test public void testMinizinc() throws IOException {
    testExecution(timeCategory);
  }
}
```

```
```

```
```
