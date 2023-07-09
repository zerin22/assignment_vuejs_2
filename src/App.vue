<template>
  <h2><span>Exercise 1:</span> {{ result }}</h2>
  <h2><span>Exercise 2:</span> {{ result2 }}</h2>
  <h2><span>Exercise 3:</span> {{ greeting }}</h2>
  <h2><span>Exercise 4:</span> {{ number }}</h2>
  <h2><span>Exercise 5:</span> {{ results }}</h2>
  <h2><span>Exercise 6:</span> {{ largeNumber }}</h2>
  <h2><span>Exercise 7:</span> {{ getAddressCity(address) }}</h2>
  <h2><span>Exercise 8:</span> {{ doubleNumbers([1, 2, 3, 4, 5]) }}</h2>
  <h2><span>Exercise 9:</span> {{ filterEvenNumbers([1, 2, 3, 4, 5]) }}</h2>
  <h2><span>Exercise 10:</span> {{ sumArray([1, 2, 3, 4, 5]) }}</h2>
  <h2><span>Exercise 11:</span> {{ sortNumbers([5, 2, 8, 1, 4]) }}</h2>
</template>

<script setup>
//Start Exercise 1
  const destructureExample = (obj, arr) => {
    const { name, age } = obj;
    const [value1, , value2] = arr;

    return { name, age };
  }

  const obj = { 
    name: 'John', 
    age: 30, 
    city: 'New York' 
  };
  const arr = [10, 20, 30, 40];

  const result = destructureExample(obj, arr);


  //End Exercise 1

  //Start Exercise 2
  const sumNumbers = (...numbers) => {
    return numbers.reduce((sum, number) => sum + number, 0);
  }

  const result2 = sumNumbers(1, 2, 3, 4, 5);
  //End Exercise 2


  //Start Exercise 3
  const createGreeting = (name) => {
    return `Hello, ${name}! Welcome to our website.`;
  }

  const greeting = createGreeting('Alice');
  //End Exercise 3


  //Start Exercise 4

  function isEven(number){
    return (number % 2 == 0 ? "Even" : "Odd");
  }

  const number = isEven(7);

  //End Exercise 4

  //Start Exercise 5

  const multidata = (a,b) => a * b;
  
  const results = multidata(2,3);

  //End Exercise 5

  //Start Exercise 6

  function getLargestNumber(number1, number2){
    return (number1 > number2 ? number1 : number2 || number2 > number1 ? number2 : number1);
  }
  const largeNumber = getLargestNumber(10, 5);

  //End Exercise 6

  //Start Exercise 7

  function getAddressCity(address){
    return address.city ?? "Unknown"
  }

  const address = { street: '123 Main St', country: 'USA' };

  //End Exercise 7

  //Start Exercise 8

  function doubleNumbers(arr){
    return arr.map((element) => element *2 );
  }

  //End Exercise 8

  //Start Exercise 9

  function filterEvenNumbers(arr){
    return arr.filter((element) => element % 2 == 0 );
  }

  //End Exercise 9

  //Start Exercise 10

  function sumArray(arr){
    return arr.reduce((sum, num) => sum + num, 0 );
  }

  //End Exercise 10

  //Start Exercise 11

  function sortNumbers(arr){
    return arr.sort();
  }

  //End Exercise 11
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,300;1,500&display=swap');

  h2 {
    margin-left: 20px;
    font-size: 18px;
    color:rgb(171, 82, 254);
    font-family: 'Poppins', sans-serif;
    font-weight: 300;
    
  }

  span{
    font-size: 25px;
    color: rgb(105, 9, 153);
    font-weight: 500;
    font-style: italic;
  }
</style>
