---
layout: post
title:      "Jquery Front-End With Rails API"
date:       2018-09-04 21:37:37 +0000
permalink:  jquery_front-end_with_rails_api
---


Wow, who would have thought that we (you, since the beginning, and I ) would be close to the end! It came with a lot of sweat, coffee, dreams of JavaScript, and there's still one more project to do.

But that's for later let us talk about the now. 

While working on my JavaScript project I, came across many challenging scenarios. 

1.  Right of the bat, I can tell you that JS is way more challenging than Ruby, or even Rails.

2. That feeling of making a feature work even if it's just making sure that line of code gets returned while highjacking an event, it is amazingly satisfying. 

Let me tell you about something pretty amazing that I learned throughout my project. 

First, I am one hell of a Googler. Googling be a skill that can be added to your resume for future careers!

Second, Prototypes. 

JavaScript has this neat inheritance construct called `Prototypes`
to have a full understanding on that you should read this [documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain) on it.

Creating a prototype is like adding custom methods to your Ruby class models. (though JS doesn't necessary have 'classes', well they do it was introduced in ES2015 mostly the word 'class') Anyways, I ran into the issue of "Can you iterate an array within a prototype? 

Yes. Yes, You can.

But it is tricky or at least it was for me. In my Models, I had a class of Pet. That pet class has many diets and when associating my back-end class model to my JS version of Class Object which looked like the lines below

```
const clickHandler = () =>{
  $(".js-moreInfo").on('click', function(){
    let id = $(this).data("id")
    $.get("/pets/" + id + ".json", function(pet){
      let newPet = new Pet(pet)
```

When I would envoke `console.log(newPet)` it would log the right instance parsed in by JSON. Now getting the array of `diets` associated with that pet and have it displayed was the issue. So I came up with this.

```
let diet = this.diets.map(d =>
    `<li>
      Diet : ${d.name}
      </li>`
  )
	```

inside the prototype function!! 

Stay tune and I might tell you how I ended up solving my situation.


