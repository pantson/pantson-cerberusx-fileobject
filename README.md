# pantson-cerberusx-fileobject

v0.1

Dynamically loads and saves objects

Currently on flat objects work. No arrays or other objects. Strings, int and floats supported.

    class test
      field text:string
      field num1:int
      field num2:int
    end
  
## Functions

### SaveObject(filename:string,obj:object,name:String)

Save an object to a filename

### LoadObject(filename:string,obj:object,name:string)

Loads a file into obj

## Example

    If KeyHit(KEY_S) Then SaveObject("test.txt",test,"test_obj")
    If KeyHit(KEY_L) Then LoadObject("test.txt",test,"test_obj")
 
