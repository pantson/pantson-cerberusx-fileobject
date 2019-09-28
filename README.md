# pantson-cerberusx-fileobject

v0.4b

Dynamically convers objects into text.
Also contains functions for loading and saving objects. 

## Compatibility

Currently works with flat objects and objects with arrays and other objects. Strings, int and floats supported.
Arrays of custom types not supported.

### working classes

    class test
      field text:string
      field num1:int
      field num2:int
      field num3:int[10]
      
      field t:values
    end
  
    class values
      field num1:int
      field test:string
    end

### non working classes
    
    class test      
      field t:values[10]
    end
  
    class values
      field num1:int
    end

## Functions

### Object2String:String\[\](obj:Object)

Converts an object to text. Use this text to add to your gamestate or other files.

### String2Object(text:String\[\],obj:Objec)

Convert some text to an object.

### DisplayObject(obj:object)

outputs object to screen/log

### SaveObject(filename:string,obj:object)

Save an object to a filename

### LoadObject(filename:string,obj:object)

Loads a file into obj

## Example

    If KeyHit(KEY_D) Then DisplayObject(test)
    If KeyHit(KEY_S) Then SaveObject("test.txt",test)
    If KeyHit(KEY_L) Then LoadObject("test.txt",test)
    text:String[] = Object2Text(test)
    String2Object(["num1=45","num2=72"],test)
