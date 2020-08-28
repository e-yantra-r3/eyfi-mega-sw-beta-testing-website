<style>
.back{
	position: fixed;
	width: 300px;
	height: 300px;
	top: 50%;
	left: 50%;
    margin-top: auto; 
    margin-left: auto; 
	opacity: 0.15;
	}
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}
</style>



<img src="http://mooc.e-yantra.org/img/eYantra_logo.svg" alt="Paris" class="center">

<img src="http://mooc.e-yantra.org/img/EyantraLogoMini.png" class="back">

# Types of Software Testing

**Author:** Kritka, GeeksforGeeks

### Introduction

Testing is a process of executing a program with the aim of finding  error. To make our software perform well it should be error free. If  testing is done successfully it will remove all the errors from the  software.

### Principles of Testing

(i) All the test should meet the customer requirements 

(ii) To make our software testing should be performed by third party 

(iii) Exhaustive testing is not possible. As we need the optimal  amount of testing based on the risk assessment of the application. (iv)  All the test to be conducted should be planned before implementing it 

v) It follows pareto rule(80/20 rule) which states that 80% of errors comes from 20% of program components. 

(vi) Start testing with small parts and extend it to large parts.

### Types of Testing

### 1. Unit Testing

It focuses on smallest unit of software design. In this we test an individual unit or group of inter related [units.It](http://units.It) is often done by programmer by using sample input and observing its corresponding outputs. Example:

```

a) In a program we are checking if loop, method or 
   function is working fine
b) Misunderstood or incorrect, arithmetic precedence.
c) Incorrect initialization
```

### 2. Integration Testing

The objective is to take unit tested components and build a program  structure that has been dictated by design.Integration testing is  testing in which a group of components are combined to produce output.

Integration testing is of four types: (i) Top down (ii) Bottom up (iii) Sandwich (iv) Big-Bang Example

```

(a) Black Box testing:- It is used for validation. 
In this we ignores internal working mechanism and 
focuses on what is the output?.

(b) White Box testing:- It is used for verification. 
In this we focus on internal mechanism i.e.
how the output is achieved?
```

### 3. Regression Testing

Every time new module is added leads to changes in program. This type of testing make sure that whole component works properly even after  adding components to the complete program. Example

```

In school record suppose we have module staff, students 
and finance combining these modules and checking if on 
integration these module works fine is regression testing
```

### 4. Smoke Testing

This test is done to make sure that software under testing is ready  or stable for further testing It is called smoke test as testing initial pass is done to check if it did not catch the fire or smoked in the  initial switch on. Example:

```

If project has 2 modules so before going to module 
make sure that module 1 works properly
```

### 5. Alpha Testing

This is a type of validation testing. It is a type of  *acceptance testing* which is done before the product is released to customers. It is typically done by QA people. Example:

```

When software testing is performed internally within
the organization
```

### 6. Beta Testing

The beta test is conducted at one or more customer sites by the  end-user of the software. This version is released for the limited  number of users for testing in real time environment Example:

```

When software testing is performed for the limited
number of people
```

### 7. System Testing

In this software is tested such that it works fine for different  operating system. It is covered under the black box testing technique.  In this we just focus on required input and output without focusing on  internal working. In this we have security testing, recovery testing ,  stress testing and performance testing Example:

```

This include functional as well as non functional 
testing
```

### 8. Stress Testing

In this we gives unfavorable conditions to the system and check how they perform in those condition. Example:

```

(a) Test cases that require maximum memory or other
    resources are executed
(b) Test cases that may cause thrashing in a virtual 
    operating system
(c) Test cases that may cause excessive disk requirement
```

### 9. Performance Testing

It is designed to test the run-time performance of software within  the context of an integrated system. It is used to test speed and  effectiveness of program. Example:

```

Checking number of processor cycles.
```

------