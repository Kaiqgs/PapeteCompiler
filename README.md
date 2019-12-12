# PapeteCompiler
Papete is the name of my compiler. Written in python using ANTLR4.
A project that started as a Compilers course assignment and turned out to be really fun.


The name Papete doesn't really have a meaning aside for inside jokes, but since this is computer science we're talking about, let it be an acronym:
- P.ython3'n
- A.ntlr4
- P.owered
- E.nvironment
- T.ranslation
- E.ngine


## Involved in this project
Kaique Alan Gualter dos Santos(me)


Bruno Mendonça dos Santos [github page](https://github.com/mendonca-bruno/)

## Installation
You're going to need [python3](https://www.python.org/download/releases/3.0/), the only other dependency needed is [antlr4](https://github.com/antlr/antlr4). 
You can install antlr4 using the following command
```
  pip install antlr4-python3-runtime
```
on linux you might want to:
```
  pip3 install antlr4-python3-runtime
```
Make sure to check [their page at pypi.com](https://pypi.org/project/antlr4-python3-runtime/) for further instructions.

## Running
Once you have python3 and antlr4. Git clone this project and open a terminal. 
You can use the following command to execute a fibonacci code sample.
```
python -m App.main SampleCode/fib.ppte
```
on linux you might want to:
```
python3 -m App.main SampleCode/fib.ppte
```

## Syntax Example

``` c++
! Inner function example;
! Function assignment example;
! Function passed as return example;
func foo(){
    func bar(){
        print("Hello World!");
    };
    return bar;
};

func globalScopeBar = foo();
globalScopeBar();
! [outputs]: Hello World!
```
``` c++
! Function as argument example;
! If and else stament example;
func getOne(int a, int b, func selector){
    bool pickVarA = selector(a, b);
    if(pickVarA){
        return a;
    }else{
        return b;
    };
};

! Selector function will be used to determine which
! value to pick;
func selector(int a, int b){
    return a > b;
};

print("Picking between numbers using custom selector: picked = " + getOne(10, 20, selector));
! [outputs]: Picking between numbers using custom selector: picked = 20
```
More samples can be found on the CodeSamples folder.
