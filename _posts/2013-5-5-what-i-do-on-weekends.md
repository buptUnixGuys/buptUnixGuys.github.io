---
layout: post
title: "java默认参数的trick"
tagline: "java技术"
description: ""
tags: ["java"]
---
{% include JB/setup %}

  有时我想利用java中的默认参数，但是不幸地是，java没有这个特性。利用一个包裹类可以实现。

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
