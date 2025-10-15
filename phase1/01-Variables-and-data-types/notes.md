# Reflection

Answer these 4 questions in your own words:

1.  What’s the difference between primitive and reference data types?
    Ans: Primitive is like a New Toy, & Reference Data is like a Toy Box shared among 2 People.
2.  Why is understanding copy by value vs reference essential for debugging?
    Ans: Copy by Value has a Term that both parties have individual objects, while Reference is you have a same box with the same ball inside shared between the Two.
3.  When would you use let vs const?
    Ans. let will be used when the value can be changed, const is basically a constant value which cannot be changed.
4.  What surprised you in this lesson?
    Ans: primitive & Reference Data types

       <!DOCTYPE html>
    <html lang="en">
      <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Mini Challenge</title>
      </head>
      <body>
        <script>
          let x = 5;
          let y = x;
          y = 10;
          //   What will be the value of x and y?
          // 5, 10
          console.log(x, y);
          //   why?
          //   because value of let can be assigned again & both are different values.

          let car = { brand: "Honda", color: "Red" };
          let newCar = car;
          newCar.color = "black";
          console.log(car);
          //   What happens to car.color?
          // //   Why does it happen?
          //     car.color will become Black. It happens because
          //     we only have one car which color was changed to black

          const fruits = ["apple", "banana"];
          fruits.push("mango");
          console.log(fruits);

          /* 🧠 Challenge 5: Real-World Analogy

            You’re designing a system for a café:

            Each customer’s order is a primitive value (total bill).

            Each customer’s profile is a reference value (object).

            If two systems accidentally share the same customer profile object, what kind of bug could appear?
            Describe the issue in plain English, using your own analogy. */

          let order = 100;
          const profile = { id: 1, name: "Rohan", phone: 8077777777 };

          console.log(profile);
          // if accidentally share the same profile data, it will overlap over the other value

          //   🧠 Challenge 6: Tricky Type Detection

          //   Without running code — predict the output of:

          typeof null; // object
          typeof []; // object
          typeof {}; // object
          typeof NaN; //number
          typeof undefined; //undefined

          //🧠 Challenge 7: Mutation Chain Reaction

          let person = { name: "Rohan" };
          let team = [person];

          person.name = "Rohan Rawat";
          console.log(team[0].name);
          //   What will team[0].name show?
          // Rohan Rawat

        </script>

      </body>
    </html>
