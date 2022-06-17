# Well-named recap

Always separate tests from regular functionality - E.g., E.g., `testPairToNumber` and `GetColorFromPairNumber`.
Or else all clients of this software will receive test code as well.

Add new functionality in [its own file](https://github.com/clean-code-craft-tcq-4/well-named-in-cpp-gautam-sh/blob/e6eecc4da206e41da2092446d60dc5ac5d4fab65/telco_color_coding_manual.hpp)

Avoid hard-coding numbers like 25

`for (int number = 1; number <= 25; number++)`

---

Major-minor code repetition

```java
public static MinorColor fromIndex(int index) {
            for(MinorColor color: MinorColor.values()) {
                if(color.getIndex() == index) {
                    return color;
                }
            }
            return null;
        }
```

[Separation of content-formation](https://github.com/clean-code-craft-tcq-4/well-named-in-cs-harsha-bg/blob/9307a23f42b21c4c1cc2258e00c69f210e1631a9/TelCo.ColorCoder/ColorCodeManual.cs) makes the manual testable

A generic name of the file like `utilities.py` will attract all functionality, growing bigger over time.
