
# Java Fundamentals Cheat Sheet





## Java Data Types
    byte / short / int / long -123, 10
    float / double 235.13
    char 'U'
    boolean true, false
    String "Greetings from earth"
 
 ##Java Statements

    If Statement
    if ( expression ) {
    statements
    } else if ( expression ) {
    statements
    } else {
    statements
    }
    While Loop
    while ( expression ) {
    statements
    }
    Do-While Loop
    do {
    statements
    } while ( expression );
    For Loop
    for ( int i = 0; i < max; ++i) {
    statements
    }
    For Each Loop
    for ( var : collection ) {
    statements
    }
    Switch Statement


##Java Statements (cont)


    switch ( expression ) {
    case value:
    statements
    break;
    case value2:
    statements
    break;
    default:
    statements
    }
    Exception Handling
    try {
    statements;
    } catch (ExceptionType e1) {
    statements;
    } catch (Exception e2) {
    catch-all statements;
    } finally {
    statements;
    }
##Java Data Conversions

    String to Number
    int i = Integer.parseInt(str);
    double d = Double.parseDouble(str);
    Any Type to String
    String s = String.valueOf(value);
    Numeric Conversions
    int i = (int) numeric expression;


##Java String Methods


    s.length() length of s
    s.charAt(i) extract ith character
    s.substring(start,
    end)
    substring from start to
    end-1
    s.toUpperCase() returns copy of s in ALL
    CAPS
    s.toLowerCase() returns copy of s in
    lowercase
    s.indexOf(x) index of first occurence of
    x
    s.replace(old,
    new)
    search and replace
    s.split(regex) splits string into tokens
    s.trim() trims surrounding
    whitespace
    s.equals(s2) true if s equals s2
    s.compareTo(s2) 0 if equal/+ if s > s2/- if s
    < s2
    See

##java.util.ArrayList Methods

    add(itm)  Add itm to list

    get(i)   Return ith item

    size()   Return number of items

    remove(i)  Remove ith item

    set(i, val)  Put val at position i

    ArrayList<String>  names =
    new ArrayList<String>();


##java.util.HashMap Methods

    m.put(key,value) Inserts value with key
    m.get(key) Retrieves value with key
    m.containsKey(key
    )
    true if contains key
    HashMap<StÂrinÂg,String> names =
    new HashMap<StÂrinÂg, String>();
    HashMap.html for more.ava Hello World
    import java.util.Date;
    public class Hello {
    public static void main(String[] args) {
    System.out.println("Hello, world!");
    Date now = new Date();
    System.out.println("Time: " + now);
    }
    }
    * Save in Hello.java
    * Compile: javac Hello.java
    Java Arithmetic Operators
    x + y add x - y subtract
    x * y multiply x / y divide
    x % y modulus ++x / x++ increment
    --x / x-- decrement
    Assignment shortcuts: x op= y
    Example: x += 1 increments x
    Java Comparison Operators
    x < y Less x <= y Less or eq
    x > y Greater x >= y Greater or eq
    x == y Equal x != y Not equal


##ava Boolean Operators
    
    ! x (not) x && y (and) x || y (or)


##Java Text Formatting



**printf style formatting**

    System.out.printf("Count is %d\n", count);
    s = String.format("Count is %d", count);
    
**MessageFormat style formatting**

    s = MessageFormat.format(
    "At {1,time}, {0} eggs hatched.",
    25, new Date());

**Individual Numbers and Dates**

    s = NumberFormat.getCurrencyInstance()
    .format(x);
    s = new SimpleDateFormat(""h:mm a"")
    .format(new Date());
    s = new DecimalFormat("#,##0.00")
    .format(125.32);




