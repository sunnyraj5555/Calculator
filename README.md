# Calculator version1.0

## The calculator is made using pure javascript,html and css

- Let Me Explain
- First List out our requirements

## The user story Cotains:
- A display Screen 
- 10 Buttons for Numbers ```0,1,2,3,4,5,6,7,8,9``` 
- 7 buttons for ```+,-,*,/,(,),=``` 
- One Button to Clean i.e. ```CLEAR ALL```
- One hrading to Display ```$r calculator $r```

## Designing Phase:
Here we will deciede the User interface of the Calculator
- The heading ```$r Calculator $r``` will be Yellow (To give rich look like gold)with a white supportive background.
- The calculator will be in middle 
- it will contain 6 layers

### Layer 1: 
- Only Screen with grey backgroung

### Layer 2:
- Three Numbers ``` |1|2|3|``` & one Addition ```+``` operator.

### Layer 3:
- Three Numbers ``` |4|5|6|``` & one Substraction ```-``` operator.

### Layer 4:
- Three Numbers ``` |7|8|9|``` & one Multiplicatin ```*``` operator.

### Layer 5:
- Three Operator ``` |(|)|/|``` & one Number ```0```.

### Layer 6:
- One Equal to ``` =``` Operator & one Button for ```CLEAR ALL```.

## Development Phase:
- For accepting the the input we need a form ```<form name="forms"> </form>``` as well as input tag ```<input>```

- Layer 1: For display the answers we will take a input tag with type "text" the id is given for designing using css and the name is given to provide access the layer.
```html
    <input type="text" name="answer" id="answerstyle">
```
_ One braek tag after each layer to come on next line 
```<br></br>```

- Layer 2: Here we will use input type "button" and the pass the value which we want to print.
```html
    <input type="button" value=" 1 " onclick="form.answer.value += '1' ">
    <input type="button" value=" 2 " onclick="form.answer.value += '2' ">
    <input type="button" value=" 3 " onclick="form.answer.value += '3' ">
    <input type="button" value=" + " onclick="form.answer.value += '+' ">
```

- Layer 3: same as previous
```html
    <input type="button" value=" 4 " onclick="form.answer.value += '4' ">
    <input type="button" value=" 5 " onclick="form.answer.value += '5' ">
    <input type="button" value=" 6 " onclick="form.answer.value += '6' ">
    <input type="button" value=" - " onclick="form.answer.value += '-' ">
    <br></br>
```

- Layer 4: same as previous
```html
    <input type="button" value=" 7 " onclick="form.answer.value += '7' ">
    <input type="button" value=" 8 " onclick="form.answer.value += '8' ">
    <input type="button" value=" 9 " onclick="form.answer.value += '9' ">
    <input type="button" value=" * " onclick="form.answer.value += '*' ">
    <br></br>
```

- Layer 5: same as previous
```html
    <input type="button" value=" 0 " onclick="form.answer.value += '0' ">
    <input type="button" value=" ( " onclick="form.answer.value += '(' ">
    <input type="button" value=" ) " onclick="form.answer.value += ')' ">
    <input type="button" value=" / " onclick="form.answer.value += '/' ">
    <br></br>
```

- Layer 6: Here there will be 2 buttons
```html
    <input type="button" value=" = " onclick="form.answer.value = eval(form.answer.value)">
    <input type="button" value=" CLEAR ALL " onclick="form.answer.value = '' " id="clear">
```

The main Catch in the program is at two Place.
1. What is the need for ```onclick="form.answer.value += '1'``` ?
- using Onclick function when user will enter let say ```1``` the 1 (i.e value) should be dispalyed in layer 1 screen ```Having name ="answer"``` for that we would have to give the path to 1 (i.e value) i.e ```form.answer.value``` and ```+= '1'``` is nothing but ```value = value + '1'``` here '1' is character added with the number.
2. What is form.answer.value assigned to '' ```value=" CLEAR ALL " onclick="form.answer.value = '' ``` ?

