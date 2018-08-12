>两个复数的加法运算
```cpp
#include <iostream>
#include <windows.h>

class complex{
public:
	complex() {
		sb = 0;
		xb = 0;
	}
	complex(double x, double y) {
		sb = x;
		xb = y;
	}
	complex(double x) {
		sb = x;
		xb = 0;
	}
	friend complex operator+(const complex& a,const complex& b) {
		complex c;
		c.sb = a.sb + b.sb;
		c.xb = a.xb + b.xb;
		return c;
	}
	void display() {
		if (sb == 0 && xb != 0)
			std::cout << xb << "i" << std::endl;
		if (sb != 0 && xb == 0)
			std::cout << sb << std::endl;
		if (sb == 0 && xb == 0)
			std::cout << 0 << std::endl;
		else {
			if (xb > 0)
				std::cout << sb << " + " << xb << "i" << std::endl;
			if (xb < 0)
				std::cout << sb << " - " << -xb << "i" << std::endl;

		}
	}
	void set(double& a, double b) {
		sb = a;
		xb = b;
	}
private:
	double sb;
	double xb;
};

int main() {

	double a, b, c, d;
	complex c1, c2, c3;
	
	while (1) {
		std::cout << "两个复数:  ";
		std::cin >> a >> b >> c >> d;

		c2.set(a, b);
		c3.set(c, d);
		c1 = c2 + c3;

		std::cout << "=========================" << std::endl;
		std::cout << "C1 = ";
		c2.display();
		std::cout << "C2 = ";
		c3.display();
		std::cout << std::endl;
		std::cout << "C1 + C2 = ";
		c1.display();
		
		std::cout << "=========================" << std::endl;
	}
	
	return 0;
}
```
