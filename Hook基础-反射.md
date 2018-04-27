### Hook基础-反射

#### 反射变量

定义Test类如下


    package com.example.lib;

    public class Test {

        private String username;
        private String password;

        public Test(){
        }

        public int showInfo(String name,String pwd){
            MyClass.print("name = " + name);
            MyClass.print("pwd = " + pwd);
            return 2;
        }

        @Override
        public String toString() {
            return "Test{" +
                    "username='" + username + '\'' +
                    ", password='" + password + '\'' +
                    '}';
        }
    }


首先Class.forName静态方法可以根据类绝对路径拿到某个类的实例

	public static void main(String[] args){
    	Class<?> cls = Class.forName("com.example.lib.Test");
        //
        Object object = cls.newInstance();
    }


