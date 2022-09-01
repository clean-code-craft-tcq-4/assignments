# TDD First step - recap

[Depicting the design](https://github.com/clean-code-craft-tcq-4/tdd-buckets-d6fb7f0c-rahulkumar082/blob/fbe344d8525017d0f73122f8496ac0ff0070df79/test_functionality/range.test.py) via tests

[Stages in the functionality](https://github.com/clean-code-craft-tcq-4/tdd-buckets-d6fb7f0c-baburoshima/blob/cee6951080be1d278c5a5962015f98e96631f30c/testCurrentRangeDetection.py) expressed in tests

[Restricing duplication](https://github.com/clean-code-craft-tcq-4/tdd-buckets-d6fb7f0c-baburoshima/blob/cee6951080be1d278c5a5962015f98e96631f30c/.github/workflows/no-dups.yml) to the minimum permssible

[Document output format](https://github.com/clean-code-craft-tcq-4/tdd-buckets-d6fb7f0c-ramandhiman6243/blob/dbd5d5575846d990d21d443a49992e4f024c85d6/rangeChecker.Tests/RangePrintInCsvTests.cs) in tests

[Abstraction for inputs and outputs](https://github.com/clean-code-craft-tcq-4/tdd-buckets-Supreeth-JR/blob/48aa2370e49caacf3137c1ef705db0b315ab357a/TestDrivenRange/IUtilities.cs)

[A strict duplication gate](https://github.com/clean-code-craft-tcq-4/tdd-buckets-d6fb7f0c-VishnuJin/blob/5fe5e732ed686f04c57373529734f3d4ef1c447b/.github/workflows/no-dups.yml) - will it hold for the last assignment?

---

Call a function by its purpose, not by its code

```c
int cmpfunc (const void * a, const void * b) {
   return ( *(int*)a - *(int*)b );
}

qsort(reading, size, sizeof(int), cmpfunc);
```

The code of `cmpfunc` is to compare. Its purpose is to sort in ascending order.
Try a name like `compareForAscending`

---

Check error?

```python
def check_error(sensor_readings):
  if 4095 in sensor_readings:
    sensor_readings.remove(4095)
  return sensor_readings
```

check_error(readings)
# process further...

---

Use test names / strings to express functionality. Also, `assertTrue` is stronger at expressing, than `assertFalse`.

```java
@Test
public void checkRangesMoreDataFailed() {
    ArrayList<Integer> inputData = new ArrayList<>(Arrays.asList(1, 9, 6, 7, 8, 9, 10, 11));
    Map<String, Integer> result = chargingRange.calculateRanges(inputData);
    assertFalse(result.get("7 - 10") == null);
    assertFalse(result.get("1 - 1") == 2);
}
```
