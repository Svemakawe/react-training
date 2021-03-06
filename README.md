# React Monday Training | React Components

## Introduction

The goal of this repository is to create a lot of React components.

To start this project, you can:
- Clone this project
- Go inside `starter-code`
- Run `npm install`
- Run `npm start`


## Components | `IdCard`

Create a `IdCard` component with 6 props:
- `lastName`: A string
- `firstName`:  A string
- `gender`:  A string, `'male'` or `'female'`
- `height`: A number
- `birth`: A date
- `picture`: A string

**Example**
```js
<IdCard 
  lastName='Doe'
  firstName='John'
  gender='male'
  height={178}
  birth={new Date("1992-07-14")}
  picture="https://randomuser.me/api/portraits/men/44.jpg"
/>

<IdCard 
  lastName='Delores '
  firstName='Obrien'
  gender='female'
  height={172}
  birth={new Date("1988-05-11")}
  picture="https://randomuser.me/api/portraits/women/44.jpg"
/>
```

**Output**

![image](https://user-images.githubusercontent.com/5306791/52976030-22b0d200-33c8-11e9-91fe-e3ce0fa14078.png)


## Components | `Greetings`

Create a `Greetings` component with 2 props:
- `lang`: A string that could be ,`"de"`,`"en"`,`"es"`,`"fr"`
- `children`: A text 

**Example**
```js
<Greetings lang="de">Ludwig</Greetings>
<Greetings lang="fr">François</Greetings>
```

**Output**

![image](https://user-images.githubusercontent.com/5306791/52957158-57edfd80-3391-11e9-8726-93c1a3389016.png)


## Components | `Random`

Create a `Random` component with 2 props:
- `min`: A number
- `max`: A number

**Example**
```js
<Random min={1} max={6}/>
<Random min={1} max={100}/>
```

**Output**

![image](https://user-images.githubusercontent.com/5306791/52957202-718f4500-3391-11e9-9b45-d1172067e877.png)



## Components | `BoxColor`

Create a `BoxColor` component that displays a rectangle with a background color based on props. For this, you will need a inline style ([documentation](https://reactjs.org/docs/dom-elements.html#style)). 

It takes 3 props:
- `r`: A number between 0 and 255 representing the amount of red
- `g`: A number between 0 and 255 representing the amount of green
- `b`: A number between 0 and 255 representing the amount of blue

**Example**
```js
<BoxColor r={255} g={0} b={0} />
<BoxColor r={128} g={255} b={0} />
```

**Output**

![image](https://user-images.githubusercontent.com/5306791/52957816-ec0c9480-3392-11e9-9e00-67094fa2b431.png)


As a bonus, you can also display the hex values of the color (ex: `#ff0000` for red).

## Components | `CreditCard`

Create a `CreditCard` component that displays a square with a background color based on props. For this. You will need a styled component. 

It takes 8 props:
- `type`: A string that can be `"Visa"` or `"Master Card"`
- `number`: A string that is number of the credit card. You will only display the 4 last digits for security reasons 😉
- `expirationMonth`: A number that represents the month, between 1 and 12
- `expirationYear`: A number that represents the year
- `bank`: A string that represents the name of the bank
- `owner`: A string the reprensents the name of the owner
- `bgColor`: A string for the background color of the card
- `color`: A string for the text color of the card

Take your time to do as close to the output. You probably have to use flexbox.

**Example**
```js
<CreditCard 
  type="Visa"
  number="0123456789018845"
  expirationMonth={3}
  expirationYear={2021}
  bank="BNP"
  owner="Maxence Bouret"
  bgColor="#11aa99"
  color="white" />
<CreditCard 
  type="Master Card"
  number="0123456789010995"
  expirationMonth={3}
  expirationYear={2021}
  bank="N26"
  owner="Maxence Bouret"
  bgColor="#eeeeee"
  color="#222222" />
<CreditCard 
  type="Visa"
  number="0123456789016984"
  expirationMonth={12}
  expirationYear={2019}
  bank="Name of the Bank"
  owner="Firstname Lastname"
  bgColor="#ddbb55"
  color="white" />
```

**Output**

![image](https://user-images.githubusercontent.com/5306791/52975678-ac5fa000-33c6-11e9-8cbf-7d13a8a0f625.png)



## Components | `Rating`

Create a `Rating` component that displays 5 stars, some of them must be empty (☆), some must be full (★).

It takes 1 props:
- `children`: A number between 0 and 5. Be careful, it can be a float number. If it's 3.9, it will display 4 stars.


**Example**
```js
<Rating>0</Rating>
<Rating>1.49</Rating>
<Rating>1.5</Rating>
<Rating>3</Rating>
<Rating>4</Rating>
<Rating>5</Rating>
```

**Output**

![image](https://user-images.githubusercontent.com/5306791/52972787-39512c00-33bc-11e9-93d8-428d835442fd.png)


## Components | `DriverCard`

**Example**
```js
<DriverCard 
  name="Travis Kalanick"
  rating={4.2}
  img="https://si.wsj.net/public/resources/images/BN-TY647_37gql_OR_20170621052140.jpg?width=620&height=428"
  car={{
    model: "Toyota Corolla Altis",
    licensePlate: "CO42DE"
  }} />
<DriverCard 
  name="Dara Khosrowshahi"
  rating={4.9}
  img="https://ubernewsroomapi.10upcdn.com/wp-content/uploads/2017/09/Dara_ELT_Newsroom_1000px.jpg"
  car={{
    model: "Audi A3",
    licensePlate: "BE33ER"
  }} />
```

**Output**

![image](https://user-images.githubusercontent.com/5306791/52972847-66054380-33bc-11e9-92e0-8e48d1ab0212.png)



## State | `ClickablePicture`

Create a component `ClickablePicture` that displays a picture and toggle to the next picture on click.

**Example**
```js
<ClickablePicture
  img="/img/persons/maxence.png"
  imgClicked="/img/persons/maxence-glasses.png" />
```

**Output before click**

![image](./solution-code/public/img/persons/maxence.png)

**Output after the 1st click**

![image](./solution-code/public/img/persons/maxence-glasses.png)

PS: If you want your own picture instead, you can do it yourself with this picture: http://www.stickpng.com/assets/images/584999937b7d4d76317f5ffd.png 😎


## State | `Dice`

Create a `Dice` component that display a random picture (example: `'/img/dice3.png'`). Then everytime the user clicks on the component:
- An empty picture is displayed (`'/img/dice-empty.png'`) 
- 2 seconds later, a new random picture is displayed (example: `'/img/dice6.png'`).

**Example**
```js
<Dice />
```

**Output before a click**

![image](https://user-images.githubusercontent.com/5306791/52976705-c13e3280-33ca-11e9-8684-f4dbff643b79.png)


**Output 1 millisecond after a click**

![image](https://user-images.githubusercontent.com/5306791/52976790-25f98d00-33cb-11e9-864e-ec14b4ec2a31.png)


**Output 2 seconds after a click**

![image](https://user-images.githubusercontent.com/5306791/52976752-f64a8500-33ca-11e9-98ee-b0b17f5e85b2.png)


## State | `Carousel`

Create a `Carousel` component that displays an image and two buttons ('left' and 'right') and that changes the picture everytime.

**Example**
```js
<Carousel
  imgs={["https://randomuser.me/api/portraits/women/1.jpg", "https://randomuser.me/api/portraits/men/1.jpg","https://randomuser.me/api/portraits/women/2.jpg", "https://randomuser.me/api/portraits/men/2.jpg"]} />
```

## List and Keys | `NumbersTable`

**Example**
```js
<NumbersTable limit={10} />
```

**Output**
```html
<ul>
  <li>1</li>
  <li>2</li>
  <li>3</li>
  <li>4</li>
  <li>5</li>
  <li>6</li>
  <li>7</li>
  <li>8</li>
  <li>9</li>
  <li>10</li>
</ul>
```

If the number is even, display it in red, otherwise in black.


## List and Keys | `FaceBook` | Simple

Create a `FaceBook` component that displays the list of all profiles from `src/data/berlin.json`. You will probably have to write: 

```js
import profiles from './data/berlin.json'
```

**Example**
```js
<FaceBook />
```

**Output** (you should see about 28 profiles)

![image](https://user-images.githubusercontent.com/5306791/53018529-e8d8dd80-3452-11e9-9912-1221eef67be6.png)


## List and Keys | `FaceBook` | Advanced

On your `FaceBook` component, add as many buttons as you have `country`. Then, when the user clicks on one of the button (example: 'USA'), add a blue background to all the profiles where their country is the one selected.

**Example**
```js
<FaceBook />
```

**Output** (you should see more profiles and more countries)

![image](https://user-images.githubusercontent.com/5306791/53018961-f8a4f180-3453-11e9-9c82-1f57a2f66a30.png)



Example of extra iterations:
- By default, only display the picture. Then, when a user clicks on a picture, display more informations
- Add sort buttons
- Add a search input