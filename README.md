# snack oggetti

🏆 Code Question 1

const hamburger = { name: "Cheese Burger", weight: 250 };

const secondBurger = hamburger;

secondBurger.name = 'Double Cheese Burger';

secondBurger.weight = 500;

​

console.log(hamburger.name); // ?

console.log(secondBurger.name ); // ?

    Senza lanciare il codice, riesci a prevedere cosa viene stampato in console?

    i 2 console log stamperanno double cheese burger

    Quanti oggetti sono stati creati in memoria durante l'esecuzione di questo codice?

    solo il name
    -----------------------------

🏆 Code Question 2

const hamburger = {

    name: "Cheese Burger",

    weight: 250,

    ingredients: ["Cheese", "Meat", "Bread", "Tomato"]

};

​

const secondBurger = {...hamburger};

secondBurger.ingredients[0] = "Salad";

​

console.log(hamburger.ingredients[0]); // ?

console.log(secondBurger.ingredients[0]); // ?

P.S.: Ricordati che gli Array, come gli oggetti, sono dei Reference Type (Tipi di Riferimento)!

    Senza lanciare il codice, riesci a prevedere cosa viene stampato in console?

    in tutti e 2 i log sarà con "Salad"

    Quanti oggetti sono stati creati in memoria durante l'esecuzione di questo codice?

    sono stati creati in memoria 3 oggetti, hamburger, ingredients, secondBurger
    ------------------------------------------------------

🏆 Code Question 3

const hamburger = {

    name: "Cheese Burger",

    weight: 250,

    maker: {

        name: "Anonymous Chef",

        restaurant: {

            name: "Hyur's Burgers",

            address: "Main Street, 123",

            isOpen: true,

        },

        age: 29

    }

};

​

const secondBurger = structuredClone(hamburger);

const thirdBurger = structuredClone(hamburger);

    Quanti oggetti sono stati creati in memoria durante l'esecuzione di questo codice?

    vengono creati in memoria 12 oggetti, perchè hamburger ha l'oggetto principale: hamburger, maker e restaurant(dentro maker), se applichiamo la deep copy tutto il blocco viene creato in memoria

---

🏆 Code Question 4

const chef = {

    name: "Chef Hyur",

    age: 29,

    makeBurger: (num = 1) => {

        console.log(`Ecco ${num} hamburger per te!`);

    },

}

​

const restaurant = {

    name: "Hyur's Burgers",

    address: {

        street: 'Main Street',

        number: 123,

    },

    openingDate: new Date(2025, 3, 11),

    isOpen: false,

};

    Qual è il metodo migliore per clonare l’oggetto chef, e perché?
    userei lo spread operator, perchè non ha proprietà annidate

    Qual è il metodo migliore per clonare l’oggetto restaurant, e perché?
    per clonare restaurant userei la deep copy(structured), per oggetti complessi come opening date oppure isOpen

🎯 Code Question 5 (Bonus)

const hamburger = {

    name: "Cheese Burger",

    weight: 250,

    maker: {

        name: "Anonymous Chef",

        restaurant: {

            name: "Hyur's Burgers",

            address: "Main Street, 123",

            isOpen: true,

        },

        age: 29

    }

};

​

const newRestaurant = {...hamburger.maker.restaurant};

newRestaurant.name = "Hyur's II";

newRestaurant.address = "Second Street, 12";

const secondBurger = {...hamburger};

secondBurger.maker.restaurant = newRestaurant;

secondBurger.maker.name = "Chef Hyur";

​

console.log(hamburger.maker.name); // ?

console.log(secondBurger.maker.name); // ?

console.log(hamburger.maker.restaurant.name); // ?

console.log(secondBurger.maker.restaurant.name); // ?

    Senza lanciare il codice, riesci a prevedere cosa viene stampato in console?
    Quanti oggetti sono stati creati in memoria durante l'esecuzione di questo codice?
