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





# <------------------Lecture-3 Note ------------------>


#            *** HOOK in react***

here we learn about hooks--->

1.React on variable update  .
2.react controls the UI update.


# useState Hook--->

Responsible for changing state (do not update value ),this change is propogated in UI(DOM).

useState gives us two things in a form of "Array"

[variable,functionForVariable]=useState(default value)

functionForVariable controls the variable.


functionForVariable(updated value of variable)




# <---------------------Lecture-04--------------------------->


# create root Method------->

Behind the scene React It creates DOM like structure .It compares the actual DOM with its own created DOM and takes the only value that is changing in the UI.



# React-fiber ====> "heart of react"

1. Algorithm used in react DOM is fiber.

2. React fiber is to increase its suitability for areas like animation,layout etc.

3. Incremental rendering is key feature of fiber.

4. Hydration -->When javaScript added in UI/WebLayout.

5. It is not necessary for every update to be applied.We can pause,abort,and assign priority to the different type of update.

 # Reconciliation---> A recursive algorithm that reconsider to who will be update.  (diffrenciation algorithm  between browser tree and react tree )
 behind the scene it is called "virtual DOM".


 # in fiber if we wants to improve performance of list than we should use "keys" ,key should be "stable ,predictable and  unique.
 




# <--------------Lecture-05 (Props(PROPERTIES))------------->

1. Props makes the card "Reusable".
2. props is used in components .
3. props returns object.
4. we can pass the string in component in app.jsx as props.
5. we can't pass the Array and Object in component.

function App() {


  return (
    <>
# it is inlegal --->
    <Card  channel="chai or code" obj={hello:"hii"}   arr=[1,2,3] />
    <Card/> 
   
  </>
  )
}



6. but as a variable we can pass the array or object in component in app.jsx.


#     see here--->


function App() {
 let  myObj={
    name:"hello hem",
    class:21
  }

let arr=[1,2,3,4]
  return (
    <>
#  this is legal--->
    <Card  channel="chai or code" obj={myObj}  myArr={arr}/>
    <Card/> 
   
  </>
  )
}


7. in a card component, it has bydefault access of props in its return 

8. we can use destructered method in component .
function Card({username}) {
    console.log("props:",username);
  return (
  <.></>
  );
}


9. we use props as a variable in our component--> {props}










