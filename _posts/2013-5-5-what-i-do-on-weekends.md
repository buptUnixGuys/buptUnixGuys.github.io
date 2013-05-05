---
layout: post
title: "巧妙实现java默认参数"
tagline: "java技术"
description: ""
tags: ["java"]
---
{% include JB/setup %}

  做为一个C++程序员，我在不知不觉总是比较着C++与java差异。在编程实践中，有时我想利用java中的默认参数，但是不幸地是，java
没有这个特性。好在，我们总是替代技术实现某语言所不具备的特性。利用一个包裹类就是默认参数就是如此。
    public class StudentBuilder{
    private String _name;
    private int _age = 14;      
    private String _motto = ""; 

    public StudentBuilder() { }

      public Student buildStudent()
      {
          return new Student(_name, _age, _motto);
      }
  
      public StudentBuilder name(String _name)
      {
          this._name = _name;
          return this;
      }
  
      public StudentBuilder age(int _age)
      {
          this._age = _age;
          return this;
      }
  
      public StudentBuilder motto(String _motto)
      {
          this._motto = _motto;
          return this;
      }
    }
    Student s1 = new StudentBuilder().name("Eli").buildStudent();
    Student s2 = new StudentBuilder().name("Spicoli").age(16).motto("Aloha, Mr Hand").buildStudent();
  我们写代码，如果采用默认参数，那么留空某些参数即可
