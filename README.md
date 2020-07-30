A simple Coordinate class for Java.

# Documentation

com.jdabtieu<br>
**Class Coord**

java.lang.Object<br>
&nbsp;&nbsp;&nbsp;&nbsp;com.jdabtieu.Coord

**All Implemented Interfaces:**<br>
`Cloneable, Comparable<Coord>`
___
```java
public class Coord
extends Object
implements Comparable<Coord>, Cloneable
```
  
The Coord class represents coordinates on a Cartesian plane.<br>It stores coordinates in the form (x,y) where x and y are signed 32-bit integers.<br>This class extends the functionality of the already existing java.awt.point, including but not limited to implementing the Comparable interface.

## Constructor Summary

| Constructor and Description |
| --------------------------- |
| `Coord(int x, int y)`<br>Constructs a new Coord which stores the coordinate (x, y) in the Cartesian plane. |
| `Coord(String x, String y)`<br>Constructs a new Coord which stores the coordinate (x, y) in the Cartesian plane. |

## Method Summary

| Modifier and Type | Method and Description |
| ----------------- | ---------------------- |
| Coord | `clone()`<br>Returns a new Coord with the same coordinates as this. |
| int | `compareTo(Coord arg0)`<br>Compares two Coords using the compareMode. |
| double | `distanceTo(Coord arg0)`<br>Gets the straight-line distance from this to arg0. |
| boolean | `equals(Object obj)`<br>Compares this Coord to the specified object. |
| int | `getX()`<br>Gets the x-coordinate of this Coord. |
| int | `getY()`<br>Gets the y-coordinate of this Coord. |
| int | `hashCode()`<br>Returns a hash code for this Coord. |
| static void | `setCompareMode(String newMode)`<br>Sets a new compareMode. |
| void | `setLocation(int x, int y)`<br>Sets the location of this Coord to (x,y). |
| void | `setLocation(String x, String y)`<br>Sets the location of this Coord to (x,y). |
| void | `setX(int x)`<br>Sets the x-coordinate of this Coord. |
| void | `setY(int y)`<br>Sets the y-coordinate of this Coord. |
| String | `toString()`<br>Converts this Coord into a String in the form (x,y). |
| void | `translate(int dx, int dy)`<br>Move this Coord to (x+dx,y+dy). |
| void | `translate(long dx, long dy)`<br>Move this Coord to (x+dx,y+dy). |
| void | `translate(String dx, String dy)`<br>Move this Coord to (x+dx,y+dy). |

| Methods inherited from java.lang.Object |
| --------------------------------------- |
| [`finalize`](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html#finalize--), [`getClass`](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html#getClass--), [`notify`](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html#notify--), [`notifyAll`](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html#notifyAll--), [`wait`](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html#wait--), [`wait`](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html#wait-long-), [`wait`](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html#wait-long-int-) |
