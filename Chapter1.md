```cpp
#include <iostream>

class complex{
public:
  complex(){
    this.sb = 0;
    this.xb = 0;
  }
  complex(x, y){
    this.sb = x;
    this.xb = y;
  }
  complex(x){
    this.sb = x;
    this.xb = 0;
  }
  complex operator + (complex& a, complex& b){
    complex c;
    c.sb = a.sb + b.sb;
    c.xb = a.xb + b.xb;
    return c;
  }
  display(){
    if(xb != 0)
      std::cout << sb << " + " << xb << "i"; 
    else
      std::cout << sb;
  }
private:
  double sb;
  double xb;
}

int main(){

  std::cout << "Hello Woeld!" << std::endl;
  
  complex x, y(10, 7), z(2, 9);
  
  x = y + z;
  std::cout << x.display() << std::endl;
  return 0;
}
```
