# Coverage recap

"Improve coverage via low complexity"

"modularity with the understanding of domain"

"avoid duplicate code"

"divide code into smaller modules and make them independent"


This code checks the return value, but passes when email content is wrong (e.g., copy-pasted same for high and low).
Why not separate the logic to convert TOO_LOW to human-readable form?
Would that be easy to test? Would it be easy to adapt to e.g., SMS?

```js
it('Send mail on TOO_LOW alert ', () => {
  expect(emailAlerts.sendToEmail('TOO_LOW'))
      .equals('TOO_LOW_STATUS_EMAIL_ALERT_SENT');
});
```

Using primitives in strong-typed languages: Reconsider - are you expressing the meaning / purpose of the function?

```java
public static boolean sendToController(BreachType breachType) {
  int header = 0xfeed;
  System.out.printf("%i : %i\n", header, breachType);
  printControllerMsg(breachType, header);
  return true;
}
```

If you cannot test exception condition, it means there is no defined way to handle it. Maybe it should not be handled (caught) here at all?

```cs
catch (Exception) {
    return null;
}
```

What if you had to test the content of the email or the message to the controller, without actually having to see it in an inbox or hardware? How far can you go with unit tests?

