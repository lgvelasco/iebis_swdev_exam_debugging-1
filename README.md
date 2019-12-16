# iebis_swdev_exam_debugging

## Bugs Found
### 1) _emailAddress.replaceAll(".", "/");_
The program was replacing all the characters in the string due to the _.replaceAll_ method. To fix it we just change the parameters to _("\\.", "/")

### 2) _random.nextInt(2)_
The parameter bound in _random.nextInt(2)_ does not include 2, to fix we change the bound to 3 _random.nextInt(3)_

### 3) _word = new StringBuffer('Y');_
The StringBuffer was adding a character instead of a string, this is due to the use of single quotes instead of double

### 4) _switch{}_
There are no breaks within the switch, so the program will go to the next case "T". To solve this one must add _break;_ after each case. 
```java
switch (random.nextInt(3)) {
            case 0:
                word = new StringBuffer("Y");
                break;
            case 1:
                word = new StringBuffer("F");
                break;
            case 2:
                word = new StringBuffer("T");
                break;
        }
```  
