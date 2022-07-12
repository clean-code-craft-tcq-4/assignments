# Reduce complexity - Recap

## Purpose of asserts

```c
checkFinalResult(int result)
{
     if(result)
    {
        assert(result == 1);
        printf("Battery is ok");
    }
    else
    {
        assert(result == 0);
        printf("Battery was not ok due to the parameters set to zero");
    }
}
```

[Conditions nested in code](https://github.com/clean-code-craft-tcq-4/simple-monitor-in-cs-Naveen-R-Mundaganur/blob/8963ae3ed27bbd82cf1c85f2d6045a4dab440162/checker.cs) - but temperature is independent of soc in real-life.
This will cause code to get 'modified' when the customer asks to 'add' the ability to give multiple independent alerts.

Function that can check any of the parameters

```cpp
template <typename paramtype, class Charge_Discharge_SOC_Temp>
bool ChargeTemp_SOC_CRate_Check(paramtype temp_SOC, Charge_Discharge_SOC_Temp ClsName)
```

Separation of consolidation

```cpp
inline bool Combined_Check(bool chargetemp, bool SOC, bool Charge_Rate){
    bool Check_m = (chargetemp && SOC && Charge_Rate);
    return Check_m;
}
```

[One function for all parameters](https://github.com/clean-code-craft-tcq-4/simple-monitor-in-py-harinisuresh2701/blob/14b581d9296479a527474abe40e8bb4c5e1d95d8/check_limits.py)

Three classes or one class with parameters?

- https://github.com/clean-code-craft-tcq-4/simple-monitor-in-cpp-ankit-88/blob/714e62b76caff73c3230c8d95654fd3920dd2fdd/checker.hpp
- https://github.com/clean-code-craft-tcq-4/simple-monitor-in-py-rahulkumar082
