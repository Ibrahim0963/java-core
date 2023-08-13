# java-core

### Java Futures: 
- Simple -> Easy to learn and understand
- Portable -> Plattform independen. Java compiled it will convert into platform independent bytecode. The bytecode is interpreted by JVM.
- Object Oriented -> Everything is an Object
- Secured -> Java code is converted into bytecode after compilation which is not understandable by human.
- Dynamic -> 
- Distributed -> 
- Robust -> strong memory management
- Architecture Neutral -> 
- Multi Threaded -> 

Possible Interviews Question:
- What are Java features?

### Java Programm Execution

- **Sample.java** (Source code) -> Compile to  -> **Simple.class** (Bytecode)
- The compiled file can run in any plattform by JVM (Java Virtual Machine)
- The JVM translate bytecode into native machine/platform code to make it understandable for that platform.
- JVM runs Java bytecode

###  JVM Architecture
-> Bild: JVM Architecture
Die JVM-Architektur besteht aus mehreren Komponenten, die zusammenarbeiten, um Java-Programme auszuführen:

1. **Class Loader:** Die Class Loader-Komponente lädt Java-Klassen von verschiedenen Quellen, wie z.B. dem lokalen Dateisystem oder dem Netzwerk, in den Speicher der JVM. Klassen werden dynamisch geladen, wenn sie zur Laufzeit benötigt werden.
   
2. **Runtime Data Areas:** Dies umfasst verschiedene Speicherbereiche, in denen Daten während der Programmausführung verwaltet werden:
    - **Method Area:** Hier werden Klassendefinitionen, statische Variablen und Methodeninformationen gespeichert.
    - **Heap:** Hier werden Objekte und deren Instanzvariablen gespeichert. Der Heap wird zur Laufzeit vom Garbage Collector verwaltet, um nicht mehr referenzierte Objekte zu entfernen.
    - **Stack:** Jeder Thread hat seinen eigenen Stack, auf dem Methodenaufrufe und lokale Variablen gespeichert werden. Diese Bereiche werden zur Laufzeit erstellt und verwaltet. (Zur Speicherung der tempäre Variablen)
    - **PC Registers:** Hier werden die Adressen der aktuellen auszuführenden Instruktionen für jeden Thread gespeichert.
    - **Native Method Stacks:** Hier werden Informationen für die Ausführung von nativen (nicht in Java geschriebenen) Methoden gespeichert.
      
3. **Execution Engine:** Die Execution Engine ist dafür verantwortlich, den maschinenspezifischen Bytecode in ausführbaren Maschinencode zu übersetzen. Es gibt verschiedene Ansätze zur Umsetzung, darunter die Interpretation und die Just-In-Time (JIT)-Kompilierung.
    
4. **Native Interface:** Die JVM bietet eine Schnittstelle, um mit nativem (plattformspezifischem) Code zu interagieren. Dies ermöglicht Java-Programmen, Funktionen von Betriebssystemen oder anderen Programmen zu nutzen, die nicht in Java geschrieben sind.
    
5. **Garbage Collector:** Die JVM enthält Mechanismen, um nicht mehr benötigte Objekte und Speicherbereiche zu erkennen und freizugeben. Dies ermöglicht eine effiziente Speicherverwaltung, ohne dass der Entwickler explizit Speicher freigeben muss.
    
6. **Java Native Interface (JNI):** Dies ist eine Schnittstelle, die es Java-Programmen ermöglicht, mit nativem Code (z.B. C oder C++) zu interagieren. Dies ist besonders nützlich für Aufgaben, die eine hohe Leistung erfordern oder auf plattformspezifische Funktionen zugreifen müssen.

- **Interpretation:** Bei der Interpretation liest die JVM den Java-Bytecode Zeile für Zeile und führt die entsprechenden Anweisungen aus, während sie den Code liest. Das bedeutet, dass der Bytecode nicht im Voraus in Maschinencode kompiliert wird, sondern zur Laufzeit in Echtzeit interpretiert wird
- 
Interview Question: 
- Erkläre JVM / JVM Architecture?
- Unterschied zwischen Compiler und Interpreter?
  Ein Compiler übersetzt den gesamten Quellcode auf einmal, bevor die Ausführung beginnt, während ein Interpreter den Quellcode zeilenweise interpretiert und ausführt.

## Java Runtime Enviroment (JRE)
Das Java Runtime Environment (JRE) ist eine Softwareumgebung, die zur Ausführung von Java-Anwendungen erforderlich ist. Es enthält die notwendigen Komponenten, um Java-Programme auszuführen, ohne dass Entwickler den Quellcode sehen oder bearbeiten müssen. Das JRE stellt die Laufzeitumgebung für Java-Anwendungen bereit und enthält die Java Virtual Machine (JVM) sowie wichtige Bibliotheken und Dateien, die für die Ausführung von Java-Code benötigt werden.

Das JDK enthält die folgenden Hauptkomponenten:
1. **JVM**
2. **Java Bibliotheken und Klassen**: z. B. Dateioperationen, Netzwerkkommunikation, GUI-Erstellung usw.
3. **Laufzeitdateien und -verzeichnisse**: z.B Konfigurationsdateien, Jar-Dateien, Ressourcen usw.
## Java Development Kit (JDK)
Das Java Development Kit (JDK) ist eine Softwareumgebung, die von Entwicklern verwendet wird, um Java-Anwendungen zu erstellen, zu kompilieren, zu debuggen und zu testen. Im Gegensatz zum Java Runtime Environment (JRE), das nur die notwendigen Komponenten für die Ausführung von Java-Anwendungen enthält, bietet das JDK eine vollständige Entwicklungsplattform mit Werkzeugen und Ressourcen, die für die Entwicklung von Java-Software erforderlich sind.

Das JDK enthält die folgenden Hauptkomponenten:
1. **Java Compiler**
2. **JVM**
3. **Java Libraries und APIs**
4. **Entwicklungswerkzeuge**: z.B Java compile (javac), Der Debugger (jdb) usw.
5. **Dokumentation und Beispiel-Code**

Zusammengefasst:  **JDK** enthält **JRE** und **JRE** enthält **JVM** 
- Unterschied zwischen JRE und JDK?
JRE -> für die Ausführung der Java-Code in einer Maschine.
JDK -> für die Entwicklung und Ausführung der Java-Code.

## JDK vs. JRE vs. JVM
**JDK (Java Development Kit):**
- Das JDK ist eine umfassende Entwicklungsplattform für die Erstellung von Java-Anwendungen.
- Es enthält den Java Compiler (`javac`), mit dem Java-Quellcode in Bytecode kompiliert wird.
- Es beinhaltet die Java Virtual Machine (JVM), die benötigt wird, um den generierten Bytecode auszuführen.
- Das JDK bietet eine Vielzahl von Entwicklungswerkzeugen wie Debugger (`jdb`), Profiler (`jvisualvm`), API-Dokumentation, Beispiele und Bibliotheken.
- Das JDK ist für Entwickler gedacht, die Java-Anwendungen erstellen, entwickeln, testen und debuggen möchten.

**JRE (Java Runtime Environment):**
- Das JRE ist eine Laufzeitumgebung, die erforderlich ist, um Java-Anwendungen auszuführen.
- Es enthält die Java Virtual Machine (JVM), die den Java-Bytecode interpretiert oder in nativen Maschinencode übersetzt.
- Das JRE stellt die notwendigen Laufzeitbibliotheken und -ressourcen bereit, um Java-Anwendungen in einer ausführbaren Umgebung zu betreiben.
- Das JRE ist für Endbenutzer gedacht, die Java-Anwendungen ausführen möchten, ohne den Quellcode zu bearbeiten oder zu entwickeln.

**JVM (Java Virtual Machine):**
- Die JVM ist eine abstrakte virtuelle Maschine, die Java-Bytecode ausführt.
- Sie ist Teil des JREs und des JDKs und ermöglicht die plattformübergreifende Ausführung von Java-Anwendungen.
- Die JVM interpretiert den Java-Bytecode oder übersetzt ihn in nativen Maschinencode, um die Ausführung zu beschleunigen.
- Die JVM verwaltet Speicher und Ressourcen für laufende Java-Anwendungen.

Zusammenfassend: Das **JDK** ist die Entwicklungsplattform, die Entwicklern alle Werkzeuge zum Erstellen von Java-Anwendungen zur Verfügung stellt. Das **JRE** ist die Laufzeitumgebung, die erforderlich ist, um Java-Anwendungen auszuführen. Die **JVM** ist die virtuelle Maschine, die den Java-Bytecode interpretiert oder übersetzt, um die Ausführung von Java-Anwendungen zu ermöglichen.
### Umgebung:
- Install java
- install JDK
- install Eclipse

- **Was ist der Zweck von Eclipse?** 
  Eclipse ist eine integrierte Entwicklungsumgebung (IDE), die für die Entwicklung von Software in verschiedenen Programmiersprachen verwendet wird. Sie bietet eine Plattform, auf der Entwickler Code schreiben, kompilieren, debuggen, testen und verwalten können.

## compile and run java program
- Compile the Program -> `javac filename.java`
- Execute the Program -> `java filename.class`


### Namenskonventionen in Java:

##### **Frage 1: Was sind Namenskonventionen in Java und warum sind sie wichtig?** 
Namenskonventionen in Java sind bestimmte Regeln und Konventionen, die festlegen, wie Bezeichner wie Klassen, Methoden, Variablen und Pakete benannt werden sollen. Sie helfen dabei, den Code lesbarer, konsistenter und verständlicher zu gestalten. Durch das Befolgen von Namenskonventionen wird der Code für Entwickler einfacher zu verstehen und zu warten, insbesondere wenn mehrere Entwickler an einem Projekt arbeiten.
#### **Klassen/Interfaces/Enums:**
- Für **Klassen**, **Interfaces**, **Enums** und **Ausnahmen** sollten mit einem Großbuchstaben beginnen und dann in CamelCase geschrieben werden.
- Sie dürfen nicht mit einer Ziffer, Sonderzeichen oder Leerzeichen beginnen.
#### **Methoden/Variablen/Objekte:**
- Für **Methoden**, **Variablen** und **Objekte** sollten mit einem Kleinbuchstaben beginnen und dann in CamelCase geschrieben werden.
- Sie dürfen nicht mit einer Ziffer, Sonderzeichen oder Leerzeichen beginnen.
#### **Pakete:**
- Paketnamen werden komplett in Kleinbuchstaben geschrieben, um Konflikte mit Klassen- oder Schnittstellennamen zu vermeiden.
#### **Konstanten:**
- Konstanten werden komplett in GROSSBUCHSTABEN geschrieben.


### Workspace (Arbeitsbereich), Package (Paket),  Namenskonventionen für Pakete

**Workspace (Arbeitsbereich):** Ein Workspace ist ein zentraler Ort, an dem du deine Projekte organisierst und entwickelst.

**Package (Paket):** Ein Paket ist eine organisatorische Einheit in Java, die Klassen, Schnittstellen und Ressourcen gruppieren hilft. 

**Namenskonventionen für Pakete:** Paketnamen sollten in Kleinbuchstaben geschrieben werden, um Konflikte zu vermeiden. Die Namen sollten umgekehrt zur Domain des Entwicklers sein, beginnend mit dem umgekehrten Domainnamen, um Eindeutigkeit zu gewährleisten. Zum Beispiel: `com.meinefirma.anwendung`. 


### Klassen und Objekte 
#### Klassen
Eine Klasse ist eine Vorlage oder ein Bauplan, der beschreibt, welche Eigenschaften (Attribute) und welche Aktionen (Methoden) ein bestimmtes Objekt haben kann. Klassen dienen dazu, Objekte zu erstellen, die auf ihren Eigenschaften und Verhaltensweisen basieren.

Modifier class ClassName {

}

Hier sind die Hauptbestandteile der Klassendefinition:
1. **Klassenname:** Der Name der Klasse, der den Bauplan repräsentiert. In Java und C++ beginnt der Klassenname normalerweise mit einem Großbuchstaben.
2. **Attribute:** Die Eigenschaften oder Variablen, die die Klasse beschreiben. Hier werden die Daten gespeichert, die ein Objekt der Klasse haben wird.
3. **Konstruktor:** Ein spezieller Methodentyp, der verwendet wird, um ein neues Objekt der Klasse zu erstellen und die Attribute zu initialisieren.
4. **Methoden:** Funktionen oder Aktionen, die von den Objekten dieser Klasse ausgeführt werden können.
#### Objekte
Ein Objekt ist eine Instanz einer Klasse. Es ist eine tatsächliche Einheit, die nach dem Muster der Klasse erstellt wird. Ein Objekt enthält Daten (Attribute) und Methoden, die in der Klasse definiert sind.
#### Arten von Klassen

**Abstrakte Klasse (Abstract Class):**
- Eine abstrakte Klasse ist eine Klasse, die nicht direkt instanziiert werden kann. Das bedeutet, du kannst keine Objekte direkt von einer abstrakten Klasse erstellen.
- Sie kann abstrakte Methoden enthalten, die in abgeleiteten Klassen implementiert werden müssen. Eine abstrakte Methode hat keine Implementierung in der abstrakten Klasse selbst.
- Abstrakte Klassen können sowohl abstrakte Methoden als auch konkrete Methoden enthalten.
- Abstrakte Klassen dienen oft als Basis für andere Klassen und legen eine gemeinsame Struktur oder Funktionalität fest, die von abgeleiteten Klassen verwendet wird.

**Nicht-abstrakte Klasse (Non-Abstract Class):**

- Eine nicht-abstrakte Klasse kann direkt instanziiert werden, um Objekte zu erstellen.
- Alle Methoden in einer nicht-abstrakten Klasse haben eine konkrete Implementierung, das heißt, sie haben einen Codeblock, der ausgeführt wird.
- Eine nicht-abstrakte Klasse kann von einer abstrakten Klasse erben und Methoden der abstrakten Klasse implementieren.
- Sie kann auch eigene Methoden und Attribute enthalten, die spezifisch für diese Klasse sind.

```java
// Abstrakte Klasse
abstract class Shape {
    abstract void draw(); // Abstrakte Methode
}

// Nicht-abstrakte Klasse, die von Shape erbt
class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a circle");
    }
}

public class Main {
    public static void main(String[] args) {
        Circle circle = new Circle();
        circle.draw();
    }
}
```

### Java Variables
**Variablen:** Variablen sind Speicherorte in einem Programm, in denen Werte gespeichert werden können. Sie werden verwendet, um Daten temporär zu speichern und auf sie zuzugreifen.

**Datentypen:** Datentypen definieren, welche Art von Daten in einer Variablen gespeichert werden kann. 

**Variablensyntax:**
`Datentyp variablenName = variablenWert;`

**Arten von Variablen:**

1. **Instanzvariablen:** An ein Objekt gebundene Variablen. Sie werden innerhalb einer Klasse, aber außerhalb von Methoden deklariert.
2. **Statische Variablen:** Auf die Klasse selbst bezogene Variablen. Alle Instanzen einer Klasse teilen sich denselben Wert für eine statische Variable.
3. **Lokale Variablen:** In einer Methode oder einem Codeblock deklarierte Variablen.
4. **Parameter (Methodenargumente):** Übergebene Werte an Methoden. Diese Parameter sind lokale Variablen, die beim Aufruf der Methode mit Werten belegt werden.
Hier ist ein einfaches Beispiel in Java, um die verschiedenen Arten von Variablen zu zeigen:
```java
public class VariablenBeispiel {
    // Instanzvariable
    int instanzVariable;

    // Statische Variable
    static int statischeVariable;

    public void methodeMitVariablen(int lokaleVariable) {
        // Lokale Variable
        int lokal = lokaleVariable;
    }

    public static void main(String[] args) {
        // Aufruf einer statischen Variable
        statischeVariable = 10;

        VariablenBeispiel objekt = new VariablenBeispiel();
        // Aufruf einer Instanzvariable
        objekt.instanzVariable = 20;

        // Aufruf einer Methode mit lokaler Variable
        objekt.methodeMitVariablen(30);
    }
}
```

## Datentypen
Datentypen in Java definieren, welche Art von Daten in einer Variablen gespeichert werden kann. Sie bestimmen auch die Größe des Speicherplatzes, den eine Variable benötigt.
Java Datentypen sind in zwei Hauptkategorien unterteilt.

**Primitive Datentypen:** Diese Datentypen repräsentieren grundlegende Werte und sind nicht auf Objekte angewiesen. Es gibt **acht** primitive Datentypen in Java:
1. **byte:** 8-Bit-Ganzzahl, Bereich von -128 bis 127.
2. **short:** 16-Bit-Ganzzahl, Bereich von -32,768 bis 32,767.
3. **int:** 32-Bit-Ganzzahl, Bereich von -2^31 bis 2^31 - 1.
4. **long:** 64-Bit-Ganzzahl, Bereich von -2^63 bis 2^63 - 1. (123124123L)
5. **float:** 32-Bit-Kommazahl mit begrenzter Genauigkeit. (0.3f)
6. **double:** 64-Bit-Kommazahl mit höherer Genauigkeit als float. (0.3d)
7. **char:** 16-Bit-Unicode-Zeichen.
8. **boolean:** Entweder `true` oder `false`.

**Referenzdatentypen:** Referenzdatentypen werden verwendet, um Objekte oder Instanzen von Klassen zu repräsentieren. Sie speichern Verweise auf die Speicheradressen der Objekte. 
In Java können Entwickler auch benutzerdefinierte Klassen erstellen, um eigene Datentypen zu definieren. Sie speichern nicht den Wert direkt, sondern eine Referenz auf den Speicherort des Werts. Beispiele: Klassen, Schnittstellen, Arrays.

```java
public class DatentypenBeispiel {
    public static void main(String[] args) {
        // Primitive Datentypen
        byte myByte = 10;
        short myShort = 1000;
        int myInt = 50000;
        long myLong = 1234567890L; // 'L' am Ende zeigt, dass es sich um einen long-Wert handelt
        float myFloat = 3.14f; // 'f' am Ende zeigt, dass es sich um einen float-Wert handelt
        double myDouble = 2.71828;
        char myChar = 'A';
        boolean myBoolean = true;

        // Referenzdatentyp (String)
        String myString = "Hallo, Welt!";
    }
}
```
Mögliche Interview Fragen:
1. **Was ist ein Datentyp?**
2. **Wie viele Datentypen gibt es in Java?** In Java gibt es zwei Hauptkategorien von Datentypen: primitive Datentypen und Referenzdatentypen.
3. **Erkläre die primitiven Datentypen in Java.** 
4. **Erkläre die Referenzdatentypen in Java?**

### Primitiven vs. Referenzdatentypen
Der Unterschied zwischen primitiven Datentypen und Referenzdatentypen liegt in der Art und Weise, wie sie Werte speichern, auf sie zugegriffen wird und wie sie im Speicher verwaltet werden:

**Primitive Datentypen:**
1. **Speicherplatz:** Primitive Datentypen speichern den Wert direkt im Speicher. Ihre Größe ist fixiert und hängt von jedem Datentyp ab.
2. **Wertzuweisung:** Beim Zuweisen eines Wertes zu einer primitiven Variable wird der Wert selbst in der Variable gespeichert.
3. **Operationen:** Primitive Datentypen unterstützen grundlegende mathematische Operationen und Vergleichsoperationen.
4. **Performance:** Da die Werte direkt gespeichert werden, sind primitive Datentypen in der Regel schneller in der Verarbeitung.

Beispiele für primitive Datentypen in Java sind `int`, `double`, `char`, `boolean`, usw.

**Referenzdatentypen:**
1. **Speicherplatz:** Referenzdatentypen speichern keine Werte direkt, sondern speichern eine Referenz auf den Speicherort des Wertes im Speicher.
2. **Wertzuweisung:** Bei der Zuweisung eines Wertes zu einer Referenzvariable wird die Referenz auf den Speicherort des Wertes gespeichert, nicht der Wert selbst.
3. **Operationen:** Referenzdatentypen ermöglichen den Zugriff auf die Methoden und Attribute der zugrunde liegenden Klasse oder des Objekts.
4. **Performance:** Aufgrund der indirekten Referenzierung können Referenzdatentypen etwas langsamer in der Verarbeitung sein als primitive Datentypen.

Beispiele für Referenzdatentypen in Java sind Klassen, Schnittstellen, Arrays, usw.


## Operatoren
Operatoren werden verwendet, um Berechnungen, Vergleiche und logische Verknüpfungen in Programmen durchzuführen.
Operatoren können in verschiedene Kategorien unterteilt werden:

**1. Arithmetische Operatoren:** Diese Operatoren werden verwendet, um mathematische Berechnungen durchzuführen.
- `+`: Addition
- `-`: Subtraktion
- `*`: Multiplikation
- `/`: Division
- `%`: Modulo (Restwert)

**2. Vergleichsoperatoren:** Diese Operatoren werden verwendet, um Werte zu vergleichen und Wahrheitswerte zu erzeugen.
- `==`: Gleichheit
- `!=`: Ungleichheit
- `<`: Kleiner als
- `>`: Größer als
- `<=`: Kleiner oder gleich
- `>=`: Größer oder gleich

**3. Logische Operatoren:** Diese Operatoren werden verwendet, um logische Ausdrücke zu verknüpfen.
- `&&`: Logisches UND (AND)
- `||`: Logisches ODER (OR)
- `!`: Logisches NICHT (NOT)

**4. Zuweisungsoperatoren:** Diese Operatoren werden verwendet, um Werte Variablen zuzuweisen.
- `=`: Wertzuweisung
- `+=`: Addition und Zuweisung
- `-=`: Subtraktion und Zuweisung
- `*=`: Multiplikation und Zuweisung
- `/=`: Division und Zuweisung
- `%=`: Modulo und Zuweisung

**5. Inkrement-/Dekrementoperatoren:** Diese Operatoren werden verwendet, um den Wert einer Variable um 1 zu erhöhen oder zu verringern.
- `++`: Inkrement (Erhöhung um 1)
- `--`: Dekrement (Verringerung um 1)

**6. Bitweise Operatoren:** Diese Operatoren werden auf Bit-Ebene verwendet.
- `&`: Bitweises UND -> Wenn beide Bits an der gleichen Position Eins sind, wird das Ergebnisbit an dieser Position Eins, ansonsten Null.
- `|`: Bitweises ODER -> Wenn eines der Bits an der gleichen Position Eins ist, wird das Ergebnisbit an dieser Position Eins, andernfalls Null.
- `^`: Bitweises XOR (ausschließendes ODER) -> Wenn die Bits an der gleichen Position unterschiedlich sind, wird das Ergebnisbit an dieser Position Eins, andernfalls Null.
- `~`: Bitweises NICHT -> Kehrt die Bits um, d.h. Einsen werden zu Nullen und umgekehrt.
- `<<`: Bitweiter Linksverschiebung -> Neue Bits werden auf der rechten Seite mit Nullen aufgefüllt.
- `>>`: Bitweite Rechtsverschiebung (arithmetisch) -> Neue Bits werden auf der linken Seite mit den ursprünglichen Vorzeichenbits (arithmetische Rechtsverschiebung) oder Nullen (logische Rechtsverschiebung) aufgefüllt.
- `>>>`: Bitweite Rechtsverschiebung (logisch) -> Ähnlich wie `>>`, aber füllt immer mit Nullen auf, unabhängig vom Vorzeichen der Zahl.
```java
int a = 4;
int b = 5;
System.out.println(a & b); // 4
System.out.println(a | b); // 5
System.out.println(a ^ b); // 1
System.out.println(a << b); // 16
System.out.println(a >> b); // 1
System.out.println(~b); // -6
System.out.println(~-10); // 9
```

7. **Bedingter (Ternärer) Operator:** Ein bedingter Operator ermöglicht es, abhängig von einer Bedingung, einen von zwei Werten auszuwählen.
    - Bedingter Operator ( ? : ) -> `Bedingung ? Wert_für_wahr : Wert_für_falsch;`
    ```java
    int zahl = 10;
	String ergebnis = (zahl > 5) ? "Größer als 5" : "Kleiner oder gleich 5";
	```


## Type Casting
```java
float floatNumber = 100.0f;
int intNumber = (int)floatNumber;
```
**1. Was ist Typkonvertierung in Java?** ist die Umwandlung eines Datentyps in einen anderen.  Es gibt zwei Arten von Typkonvertierungen: implizite (automatische) Konvertierung und explizite (manuelle) Konvertierung.

**2. Was ist "Widening" in Java?** "Widening" bezieht sich auf die implizite Typkonvertierung von einem Datentyp mit kleinerer Größe in einen Datentyp mit größerer Größe. Dies geschieht automatisch, da keine Daten verloren gehen. Zum Beispiel wird eine Ganzzahl (`int`) in einen Fließkommawert (`double`) umgewandelt.

**3. Was ist "Narrowing" in Java?** "Narrowing" bezieht sich auf die explizite Typkonvertierung von einem Datentyp mit größerer Größe in einen Datentyp mit kleinerer Größe. Da Daten verloren gehen könnten, muss diese Konvertierung manuell durchgeführt werden. Zum Beispiel könnte ein `double` in ein `int` umgewandelt werden.

**4. Was ist implizite Konvertierung in Java?** Implizite Konvertierung, auch als automatische Konvertierung bekannt, tritt auf, wenn Java selbstständig Datentypen konvertiert, um sicherzustellen, dass Daten nicht verloren gehen. Beispielsweise wird eine Ganzzahl in eine Gleitkommazahl umgewandelt, wenn sie in einer Berechnung mit Gleitkommazahlen verwendet wird.
```java
int n1 = 100
float n2 = n1 // Die Umwandlung wird funktionieren.
```

**5. Was ist explizite Konvertierung in Java?** Explizite Konvertierung tritt auf, wenn du manuell eine Datentypkonvertierung durchführst, indem du den gewünschten Datentyp in Klammern vor den Wert schreibst. Dies ist notwendig, wenn Daten bei der Konvertierung verloren gehen könnten, z. B. wenn du eine Gleitkommazahl in eine Ganzzahl umwandelst.
```java
float n1 = 100
int n2 = n1 // Die Umwandlung wird NICHT funktionieren.

float n1 = 100 
int n2 = (int)n1 // Die Umwandlung wird funktionieren.
```

**1. Was ist eine Wrapper-Klasse in Java?** 
Eine Wrapper-Klasse in Java ist eine Klasse, die eine primitive Datenart (wie int, char, boolean usw.) in ein Objekt einhüllt. Jeder primitiven Datentyp in Java hat eine entsprechende Wrapper-Klasse. Zum Beispiel ist die Wrapper-Klasse für den Datentyp `int` die Klasse `Integer`. Diese Wrapper-Klassen bieten Methoden und Funktionen, die es ermöglichen, mit primitiven Datentypen als Objekten zu arbeiten.

**2. Wofür dienen Wrapper-Klassen in Java?** Wrapper-Klassen haben verschiedene Verwendungszwecke, darunter:
- Konvertierung von primitiven Datentypen in Objekte, um sie in Sammlungen wie Listen oder Sets zu speichern.
- Bereitstellung von Methoden zum Arbeiten mit primitiven Datentypen als Objekten.
- Erlauben von Null-Werten für primitive Datentypen durch Verwendung von `null`.
- Generics in Java funktionieren nur mit Objekten und unterstützen keine primitiven Datentypen.
- Sammlungen (Collections) in Java arbeiten nur mit Objekten. Um primitive Datentypen in einer dieser Klassen zu speichern, musst du den primitiven Datentyp in eine Klasse verpacken..

**3. Was ist Autoboxing in Java?** 
Autoboxing ist ein automatischer Prozess in Java, bei dem primitiven Datentypen automatisch in ihre entsprechenden Wrapper-Klassen umgewandelt werden. Dies ermöglicht es, primitiven Datentypen in Sammlungen wie ArrayLists zu speichern, die normalerweise Objekte erfordern.

**4. Was ist Auto-Unboxing in Java?** 
Auto-Unboxing ist der umgekehrte Prozess von Autoboxing. Hierbei wird ein Objekt einer Wrapper-Klasse automatisch in einen primitiven Datentyp umgewandelt. Dies geschieht, wenn ein Objekt in einem Kontext verwendet wird, in dem ein primitiver Datentyp erwartet wird.

```java
// Autoboxing: primitive int wird automatisch in Integer umgewandelt
Integer zahlObjekt = 42;

// Auto-Unboxing: Wert aus dem Integer-Objekt wird automatisch extrahiert
int zahl = zahlObjekt;

// Beispiel mit ArrayList (Sammlung von Integer-Objekten)
ArrayList<Integer> zahlenListe = new ArrayList<>();
zahlenListe.add(10); // Autoboxing: 10 wird in Integer umgewandelt

int ersterWert = zahlenListe.get(0); // Auto-Unboxing: Wert wird in int umgewandelt

// Auto-Unboxing
Integer i = 10;
if (i == 123) { // Integer == int 
	System.out.println("This is an Integer....");
}
```


##### Primitive Type zu Wrapper Class
Es gibt zwei gängige Möglichkeiten, einen primitiven Datentyp in eine Wrapper-Klasse umzuwandeln: 
- die Verwendung von Konstruktoren 
- die Verwendung von statischen Methoden wie `valueOf()`.

**1. Verwendung von Konstruktoren:** 
Jede Wrapper-Klasse hat einen oder mehrere Konstruktoren, die primitiven Datentypen als Argumente akzeptieren und ein entsprechendes Wrapper-Objekt erstellen.
```java
int primitiveInt = 42;
Integer wrapperInt = new Integer(primitiveInt); // Konstruktor für Integer
```
**2. Verwendung von statischen Methoden wie `valueOf()`:** 
Wrapper-Klassen bieten oft eine statische Methode namens `valueOf()`, die einen primitiven Wert als Argument akzeptiert und ein entsprechendes Wrapper-Objekt zurückgibt.
```java
double primitiveDouble = 3.14;
Double wrapperDouble = Double.valueOf(primitiveDouble); // Verwendung von valueOf für Double
```
Die Verwendung von `valueOf()` wird oft bevorzugt, da sie möglicherweise effizienter ist, da sie möglicherweise wiederverwendete Objekte zurückgibt.
Weitere Beispiele:
```java
int primitiveInt = 42;
Integer wrapperInt = Integer.valueOf(primitiveInt);

float primitiveFloat = 3.14f;
Float wrapperFloat = Float.valueOf(primitiveFloat);

char primitiveChar = 'A';
Character wrapperChar = Character.valueOf(primitiveChar);

boolean primitiveBoolean = true;
Boolean wrapperBoolean = Boolean.valueOf(primitiveBoolean);
```

##### Wrapper-Klasse in primitiven Datentyp umwandeln:
Du kannst eine Wrapper-Klasse in einen primitiven Datentyp umwandeln, indem du entsprechende Methoden aufrufst, die in den Wrapper-Klassen verfügbar sind. Jede Wrapper-Klasse bietet Methoden, um ihren Wert als primitiven Datentyp zurückzugeben.
```java
Integer wrapperInt = Integer.valueOf(42);
int primitiveInt = wrapperInt.intValue(); // Methode intValue() gibt den Wert als int zurück

Double wrapperDouble = Double.valueOf(3.14);
double primitiveDouble = wrapperDouble.doubleValue();

Character wrapperChar = Character.valueOf('A');
char primitiveChar = wrapperChar.charValue();

```


## Methoden
- In Java sind Methoden dafür, bestimmte Aktionen oder Operationen auszuführen.
- Sie sind in Klassen definiert und können aufgerufen werden.
- Methoden ermöglichen die Wiederverwendung von Code und verbessert Lesbarkeit.

Note: **Rückgabetyp in Methoden:** Der Datentyp des Werts, den die Methode zurückgibt. Verwendung von `void`, wenn die Methode keinen Wert zurückgibt.
#### Zugriffsmodifikatoren:** 
Diese Modifikatoren regeln den Zugriff auf Klassen, Methoden und Variablen.
- `public`: Das Element ist von überall aus sichtbar.
- `protected`: Das Element ist in der eigenen Klasse, abgeleiteten Klassen und im selben Paket sichtbar.
- `default` (kein Modifikator angegeben): Das Element ist nur im selben Paket sichtbar.
- `private`: Das Element ist nur in der eigenen Klasse sichtbar.
#### Nichtzugriffsmodifikatoren:** 
Diese Modifikatoren beeinflussen das Verhalten und die Funktionalität von Klassen und Methoden, haben jedoch keinen direkten Einfluss auf den Zugriffsbereich..
- `static`: Das Element gehört zur Klasse und nicht zu einer Instanz. Es kann aufgerufen werden, ohne ein Objekt zu erstellen.
- `final`: Das Element kann nicht erneut zugewiesen oder vererbt werden. Bei Methoden bedeutet `final`, dass die Methode nicht in abgeleiteten Klassen überschrieben werden kann.
- `abstract`: Das Element ist abstrakt und hat keine Implementierung. Es wird in abgeleiteten Klassen implementiert.
- `synchronized`: In Mehrfadenanwendungen stellt sicher, dass nur ein Thread gleichzeitig auf das Element zugreifen kann.
- `volatile`: In Mehrfadenanwendungen stellt sicher, dass Änderungen an dieser Variable sofort von allen Threads sichtbar sind.
- `transient`: Wird für Instanzvariablen verwendet, um anzuzeigen, dass sie nicht in den Zustand eines serialisierten Objekts einbezogen werden sollen.

new keyword -> um Objekte zu erstellen.

```java
public class MethodenBeispiel {

    // Methode zur Addition von zwei Zahlen
    public int addiere(int zahl1, int zahl2) {
        int ergebnis = zahl1 + zahl2;
        return ergebnis;
    }

    public static void main(String[] args) {
        MethodenBeispiel beispiel = new MethodenBeispiel();
        int summe = beispiel.addiere(5, 3);
        System.out.println("Die Summe ist: " + summe);
    }
}

```

Interviewfrage:
- How to achieve reusability in java?
Mithilfe von Methoden kann man die Wiederverwendbarkeit erreichen.


















































