**Que:** Difference Between `main()` and `runApp()` Function.
**Ans:** 

`main()` is the entry point of every Dart or Flutter application.
`runApp()` is a Flutter function that takes a Widget and makes it the root of the widget tree to start rendering the UI.

<details>
<summary>Gujarati</summary>

`main()` એ દરેક Dart અથવા Flutter એપ્લિકેશનનો પ્રારંભ બિંદુ (entry point) છે.
`runApp()` એ Flutter નું ફંક્શન છે જે કોઈ Widget લે છે અને તેને એપ્લિકેશનના મૂળ Widget તરીકે ચલાવે છે, જેથી UI સ્ક્રીન પર દેખાય.
</details>

#### **EXAMPLE:**
```dart
void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Center(child: Text('Hello Flutter!')),
    );
  }
}
```

* Here, `main()` starts the program.
* `runApp(MyApp())` loads the `MyApp` widget and displays the UI.

```scss
        ┌─────────────┐
        │  main()     │
        │ Entry Point │
        └──────┬──────┘
               │
               ▼
        ┌─────────────┐
        │ runApp()    │
        │ Loads Widget│
        └──────┬──────┘
               │
               ▼
        ┌──────────────┐
        │ Render UI    │
        │ (Widget Tree)│
        └──────────────┘
```

#### **EXPLANATION:**
`main()` ફંક્શન એ એપ્લિકેશન ક્યાંથી શરૂ થાય છે તે નક્કી કરે છે — એટલે કે Dart કોડ અહીંથી અમલમાં આવે છે.
જ્યારે આપણે `runApp()` બોલાવીએ છીએ, ત્યારે તે Flutter framework ને કહે છે કે આપેલું Widget (જેમ કે `MyApp`) સ્ક્રીન પર બતાવવાનું છે.
`runApp()` પછી આખી Widget Tree બને છે અને Flutter engine UI રેન્ડર કરવાનું શરૂ કરે છે.

સરળ શબ્દોમાં —
+ `main()` = પ્રોગ્રામનો પ્રવેશદ્વાર.
+ `runApp()` = UI શરૂ કરવાનું આદેશ.
---