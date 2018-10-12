---
layout: post
title:      "React - Props Vs. State"
date:       2018-10-12 17:22:56 +0000
permalink:  react_-_props_vs_state
---


***Props v. State ***

In React there are many ways to define a component. There's the `class`  that normally extends from `React. Component`  and the regular JavaScript function method. They are very similar, but they have something that differs from both `State` and `Props`

***Props:***
	Props short for properties, give you access to modify your component when it's being created. The most important take away is that it can be passed down by a parent component allowing us to create a customizable component everytime we pass new props to it.
	
```
import React, { Component } from 'react'

export default ParentComponent extends Component {
	render(){
		return(
			<div>
			 	<ChildComponent name={Props}/>
			</div>
		)
	}
}
```

When we want to use data that we know is going to change over time we want to use State.

***State: ***

A state is a component’s local state. It strickly belongs to that single component. State allows React Components to dynamically change output over time in response to an event. To give some examples: The like button on FB, the number of retweets going up on Tweeter, and the hearts of Instagram. 

State is normally initialized inside of a constructor. 

```
import React, { Component } from 'react'

export default StateExample extends Component {
	constructor(props){
	super(props)
	this.state = {
		count: 0
	}
};

handleClickEvent = () => {
	this.setState({
		count: this.state.count += 1
	})
};

render(){
		return(
				<div>
<p>Count: {this.state.count}</p>
<button 
onClick={this.handleClickEvent}>Click to add the count</button>
				</div>
		);


    }
}
```
	

***Conclusion: ***

We saw what state and props are, and some examples of them both. Props being close to State besides the fact that `state` is local to that specific component. While Props is mostly a 'read-only' case.
