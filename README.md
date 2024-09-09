# Korona-project
Pretty simple and well developed console application that was written in Java and Maven build tool. This project has been created for "Золотая корона" courses.

## Main functionality  
  * sorting various types from 1 and more input files into 3 output files (integers, floats, strings)
  * provide full and short statistic about sorted values
  * possibility to set the path and prefix for output files
  * support parallel writing into output files

## Options
  * -o: set the path for output files
  * -p: set the prefix for output files
  * -a: append text into output files
  * -s: short statistic
  * -f: full statistic
  
  Example: -o some/path/to -p myprefix_  
  Output files: ../some/path/to/myprefix_integers.txt ../some/path/to/myprefix_floats.txt ../some/path/to/myprefix_strings.txt

## Example of work
### Input file in1.txt:  
Lorem ipsum dolor sit amet  
45  
Пример  
3.1415  
consectetur adipiscing  
-0.001  
тестовое задание  
100500  

### Input file in2.txt:  
Нормальная форма числа с плавающей запятой  
1.528535047E-25  
Long  
123456789

### Util start up:  
java -jar util.jar -s -a -p sample- in.txt in2.txt  

### sample-integers.txt:  
45  
100500  
123456789  

### sample-floats.txt:  
3.1415  
-0.001  
1.528535047E-25  

### sample-strings.txt  
Lorem ipsum dolor sit amet  
Пример  
consectetur adipiscing  
тестовое задание  
Нормальная форма числа с плавающей запятой  
Long

### Short statistic:  
sample-integers.txt short statistic: elements = 3  
sample-floats.txt short statistic: elements = 3  
sample-strings.txt short statistic: elements = 6

## Full statistic:  
sample-integers.txt full statistic: elements = 3; min: 45; max: 123456789; sum: 123557334, average: 41185778  
sample-floats.txt full statistic: elements = 3; min: -0.001; max: 3.1415; sum: 3.1405, average: 1.0468334  
sample-strings.txt full statistic: elements = 6; min length: 5; max length: 42
