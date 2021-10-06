# Unity Coroutine Provider
A small hack that allows you to use coroutines in classes not inherited from MonoBehaviour

## Usage
You can use coroutines in your classes that do not use MonoBehaviour. For example, like this:
```csharp
using System;
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using TinyPlay.Utils;

public class MyClass{
  // Constructor
  public MyClass(){
  }
  
  // Simple Method for Run Coroutine
  public void DoSomeStuff(){
    CoroutineProvider.Start(MyRoutine());
  }
  
  // Coroutine
  private IEnumerator MyRoutine(){
    yield return new WaitForSeconds(10f);
    Debug.Log("It's Work!");
  }
}
```
