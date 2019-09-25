# pantson-cerberusx-fileobject

v0.1

Dynamically loads and saves objects

Currently on flat objects work. Now works with arrays or other objects. Strings, int and floats supported.
Arrays of custom types not supported.

    class test
      field text:string
      field num1:int
      field num2:int
      
      field t:values
    end
  
    class values
      field num1:int
      field test:string
    end
    
## Functions

### DisplayObject(obj:object)

outputs object to screen/log

### SaveObject(filename:string,obj:object)

Save an object to a filename

### LoadObject(filename:string,obj:object)

Loads a file into obj

This is currently BROKEN!!!

## Example

    If KeyHit(KEY_D) Then DisplayObject(test)
    If KeyHit(KEY_S) Then SaveObject("test.txt",test)
    If KeyHit(KEY_L) Then LoadObject("test.txt",test)
 
