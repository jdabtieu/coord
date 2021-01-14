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
| double | `distanceTo(Coord arg0)`<br>**Deprecated - use eucDist instead**<br>Gets the straight-line distance from this to arg0. |
| boolean | `equals(Object obj)`<br>Compares this Coord to the specified object. |
| double | `eucDist(Coord arg0)`<br>Gets the straight-line (Euclidean) distance from this to arg0. |
| int | `getX()`<br>Gets the x-coordinate of this Coord. |
| int | `getY()`<br>Gets the y-coordinate of this Coord. |
| int | `hashCode()`<br>Returns a hash code for this Coord. |
| long | `manDist(Coord arg0)`<br>Gets the Manhattan distance from this to arg0. |
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

## Constructor Detail
| Coord |
| ----- |
| `public Coord(int x, int y)`<br>Initializes a newly created `Coord` object so that it represents the point (x,y) on the Cartesian plane.<br><b>Parameters:</b><br>`x` - The x-coordinate<br>`y` - The y-coordinate<br><b>See also:</b><br>`setLocation(int, int)` |

| Coord |
| ----- |
| `public Coord(String x, String y)`<br>Initializes a newly created `Coord` object so that it represents the point (x,y) on the Cartesian plane. Strings x and y must be integers, once trimmed of any leading or trailing whitespace.<br><b>Parameters:</b><br>`x` - The x-coordinate<br>`y` - The y-coordinate<br><b>Throws:</b><br>`NullPointerException`  - if one or both arguments are `null`<br>`NumberFormatException` - if one or both arguments are not integers, are larger than `Integer.MAX_VALUE`, or less than `Integer.MIN_VALUE`<br><b>See Also:</b><br>`setLocation(String, String)` |

## Method Detail
| clone |
| ----- |
| `public Coord clone()`<br>Returns a copy of this Coord. The copy has the same x- and y-coordinates as this Coord.<br><b>Overrides:</b><br>`clone` in class `Object`<br><b>Returns:</b><br>copy of this Coord |

| compareTo |
| --------- |
| `public int compareTo(Coord arg0)`<br>Compares the location of this Coord to another Coord arg0 based on compareMode. By default, a Coord is larger if its x-coordinate is larger than another Coord's x-coordinate, or if both are equal and the y-coordinate is greater. `compareTo` should never throw an exception unless the value of `compareMode` has been modified using a debugger.<br><b>Specified by:</b><br>`compareTo` in interface `Comparable<String>`<br><b>Parameters:</b><br>`arg0` - the Coord to be compared<br><b>Returns:</b><br>the value 0 if both Coords are equal; the value -1 if `arg0` is greater than `this`; the value 1 if `this` is greater than `arg0`<br><b>Throws:</b><br>`NullPointerException` if `compareMode` is `null`<br>`IllegalStateException` if `compareMode` is not valid<br><b>See Also:</b><br>`setCompareMode(String)` |

| distanceTo |
| ---------- |
| `public double distanceTo(Coord arg0)`<br>**Deprecated - use eucDist instead**<br>Calculates the straight-line distance to another Coord `arg0`. The returned distance will always be zero or positive.<br><b>Parameters:</b><br>`arg0` the Coord to calculate distance to<br><b>Returns:</b><br>the straight-line distance to `arg0` |

| equals |
| ------ |
| `public boolean equals (Object obj)`<br>Compares this Coord to the specified object. The result is true if the argument is not `null` and is a Coord representing the same point on the Cartesian plane as this Coord.<br><b>Overrides:</b><br>`equals` in class `Object`<br><b>Parameters:</b><br>`true` if the given object is equivalent to this Coord, `false` otherwise<br><b>See Also:</b><br>`compareTo(Coord)` |

| eucDist |
| ------- |
| `public double eucDist(Coord arg0)`<br>Calculates the straight-line (Euclidean) distance to another Coord `arg0`. The returned distance will always be zero or positive.<br><b>Parameters:</b><br>`arg0` the Coord to calculate distance to<br><b>Returns:</b><br>the straight-line (Euclidean) distance to `arg0` |

| getX |
| ---- |
| `public int getX()`<br>Returns the x-coordinate of this Coord.<br><b>Returns:</b><br>x-coordinate of this Coord |

| getY |
| ---- |
| `public int getY()`<br>Returns the y-coordinate of this Coord.<br><b>Returns:</b><br>y-coordinate of this Coord |

| hashCode |
| -------- |
| `public int hashCode()`<br>Returns a hash code for this Coord. The hash code for a `Coord` object is computed as `(1 * 31 + x) * 31 + y`. The hash code for the Coord representing the origin is 961.<br><b>Overrides:</b><br>`hashCode` in class `Object`<br><b>Returns:</b><br>a hash code for this Coord |

| manDist |
| ------- |
| `public long manDist(Coord arg0)`<br>Calculates the Manhattan distance to another Coord `arg0`. The returned distance will always be zero or positive.<br><b>Parameters:</b><br>`arg0` the Coord to calculate distance to<br><b>Returns:</b><br>the Manhattan distance to `arg0` |

| setCompareMode |
| -------------- |
| `public static void setCompareMode(String newMode)`<br>Sets a new `compareMode` for use in `compareTo(Coord arg0`. The default is `XY`, in which the Coord with the larger x-coordinate, or if both are equal, the larger y-coordinate, is larger. Also available are:<br>`YX`, in which the Coord with the larger y-coordinate, or if both are equal, the larger x-coordinate, is larger<br>`X`, in which the Coord with the larger x-coordinate is larger<br>`Y`, in which the Coord with the larger y-coordinate is larger<br>`DIST`, in which the Coord furthest from the origin is larger<br><b>Parameteres:</b><br>`newMode` - the new compareMode<br><b>Throws:</b><br>`NullPointerException` if `compareMode` is `null`<br>`IllegalArgumentException` if `compareMode` is not valid<br><b>See Also:</b><br>`compareTo(Coord)` |


| setLocation |
| ----------- |
| `public void setLocation(int x, int y)`<br>Sets the location of this Coord to (x,y). This method is used by the constructor `Coord(int x, int y)`<br><b>Parameters:</b><br>`x` - The x-coordinate<br>`y` - The y-coordinate |

| setLocation |
| ----------- |
| `public void setLocation(String x, String y)`<br>Sets the location of this Coord to (x,y). Strings x and y must be integers, once trimmed of any leading or trailing whitespace. This method is used by the constructor `Coord(String x, String y)`<br><b>Parameters:</b><br>`x` - The x-coordinate<br>`y` - The y-coordinate<br><b>Throws:</b><br>`NullPointerException`  - if one or both arguments are `null`<br>`NumberFormatException` - if one or both arguments are not integers, are larger than `Integer.MAX_VALUE`, or less than `Integer.MIN_VALUE` |

| setX |
| ---- |
| `public void setX(int x)`<br>Sets the x-coordinate of this Coord to x.<br><b>Parameters:</b><br>`x` - the new x-coordinate for this Coord |

| setY |
| ---- |
| `public void setY(int y)`<br>Sets the y-coordinate of this Coord to x.<br><b>Parameters:</b><br>`y` - the new y-coordinate for this Coord |

| toString |
| -------- |
| `public String toString()`<br>Returns a String representation for this Coord. The String returned will be in the form of (`x`,`y`). For example, the Coord representing the origin would be `(0,0)`.<br><b>Overrides:</b><br>`toString` in class `Object`<br><b>Returns:</b><br>a String representation of this Coord |

| translate |
| --------- |
| `public void translate(int dx, int dy)`<br>Move this Coord to (x+dx,y+dy), if x+dx and y+dy are within the bounds of the 32-bit int.<br><b>Parameters:</b><br>`dx` - The amount to change the x-coordinate by<br>`dy` - The amount to change the y-coordinate by<br><b>Throws:</b><br>`ArithmeticException` - if one or both arguments cause x or y to become larger than `Integer.MAX_VALUE`, or less than `Integer.MIN_VALUE`<br><b>See Also:</b><br>`translate(long, long)` |

| translate |
| --------- |
| `public void translate(long dx, long dy)`<br>Move this Coord to (x+dx,y+dy), if x+dx and y+dy are within the bounds of the 32-bit int.<br><b>Parameters:</b><br>`dx` - The amount to change the x-coordinate by<br>`dy` - The amount to change the y-coordinate by<br><b>Throws:</b><br>`ArithmeticException` - if one or both arguments cause x or y to become larger than `Integer.MAX_VALUE`, or less than `Integer.MIN_VALUE` |

| translate |
| --------- |
| `public void translate(String dx, String dy)`<br>Move this Coord to (x+dx,y+dy), if dx and dy are integers once they are trimmed of leading and trailing whitespace, and if x+dx and y+dy are within the bounds of the 32-bit int.<br><b>Parameters:</b><br>`dx` - The amount to change the x-coordinate by<br>`dy` - The amount to change the y-coordinate by<br><b>Throws:</b><br>`NullPointerException` - if one or both arguments are `null`<br>`NumberFormatException` - if one or both arguments are not an integer of if they are greater than `Long.MAX_VALUE` or less than `Long.MIN_VALUE`<br>`ArithmeticException`  - if one or both arguments cause x or y to become larger than `Integer.MAX_VALUE`, or less than `Integer.MIN_VALUE`<br><b>See Also:</b><br>`translate(long, long)` |
