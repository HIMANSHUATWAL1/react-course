<---------------01 Lecture Notes -------------------->

1.Making a component give capitalize name (ex-App.jsx)
2.give the .jsx extention for better result ,

3.app.jsx can only return one component at a time we can use (<> </>) for return more than one component.



# <-----------------02 Lecture Notes------------->

1. App.jsx is a functional component which we can also write in main.
2. react use "bundler" for converting or parsing  html code into jsx object(tree like structure ).
3. we can write functional component as function calling (function_name()) syntax because at end it is a function.
4.we cannot directly pass object to it because in react render property have defined arguments and it can not voilate .



/*
const ReactElement={
  type:'a',
  props:{
      href:"https://google.com",
      target:"_blank"
  },
  children:'Click me to visit google'
}
*/

# create using react----------------------->

const reactEle=React.createElement(

  # here in react we have strict guidline for taking parameter.

 # first parameter is any type of tag
 # second is object
 # third is direct text
 # At last our variables are injected 


   'a',
   {href:'http://google.com',target:'_blank'},
    'click me to visit google!',
    variables 
)

# we can write this type also ------------>
const anotherEle=(
  <a href="htttp://google.com" target='_blank'>visit google</a>
)

ReactDOM.createRoot(document.getElementById('root')).render(
  reactEle
)




# how to inject variables in jsx------>

for injecting variable in our jsx we use {} which is called "Evaluated Expression"

# Evaluated Expression means "final outcome"
# we can't add any syntax(if,for etc.) in evaluated Expression block.

# In react when our tree is created than variables are injected in this tree. 

