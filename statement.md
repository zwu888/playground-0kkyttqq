```C++ runnable
#include <iostream>

int foo(int i)
{
  return 2;
}

double foo(double d)
{
  return 4.0;
}

struct Computer
{
  int foo(int i)
  {
    return 8; 
  }
};

struct Gateway : public Computer
{
  double foo(double d)
  {
    return 16.0; 
  }
};

int main(int argc, char** argv)
{
  Gateway g;

  std::cout << foo(1) + foo(1.0) + g.foo(1) + g.foo(1.0) << std::endl;

  return 0;
}
```


