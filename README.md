### Task №1(8 kyu)

Consider an array/list of sheep where some sheep may be missing from their place. We need a function that counts the number of sheep present in the array (true means present).
Hint: Don't forget to check for bad values like null/undefined

[Task_link](https://www.codewars.com/kata/54edbc7200b811e956000556)

#### Solution
~~~ Java
public class Counter {
  public int countSheeps(Boolean[] arrayOfSheeps) {
    int count = 0;
    //Iterate through the Sheep array
    for(int i = 0; i < arrayOfSheeps.length; i++) {
    //If not null and true, increment count
      if(arrayOfSheeps[i] != null && arrayOfSheeps[i])
       count++;
    }
    return count;
  }
}
~~~

#### Fav Solution
~~~ Java
public class Counter {
  public int countSheeps(Boolean[] arrayOfSheeps) {
    int counter = 0;
    for (Boolean present : arrayOfSheeps) {
      if (present != null && present) {
        counter += 1;
      }
    }
    return counter;
  }
}
~~~


### Task №2(7kyu)

Count the number of divisors of a positive integer n.

Random tests go up to n = 500000.

[Task_link](https://www.codewars.com/kata/542c0f198e077084c0000c2e)

#### Solution

~~~ Java
public class FindDivisor {

    public long numberOfDivisors(int n) {
        int count = 0;
        for (int i = 1; i <= n; i++) {
            if (n % i == 0) {
                count++;
            }
        }
        return count;
    }

}
~~~

#### Fav Solution

~~~ Java
public class FindDivisor {

  public long numberOfDivisors(int n) {
    int cntr = 0;
    for (int i = 1; i <= n/2; i++)
      if (n % i == 0) cntr++;
    return (n == 0)? 0 : ++cntr;
  }

}
~~~
