# Movie app

React JS

import React from "react";
import PropTypes from "prop-types";

class App extends React.Component{ //state === object
state ={
count:0
};
add = () =>{ //setState : 새로운 state와 함께 render fun을 호출
this.setState(current =>({count: current.count +1}));
};
minus = () =>{
this.setState(current =>({count: current.count -1}))
};
render(){
return <div>
<h1>The number is: {this.state.count}</h1>
<button onClick={this.add}>Add</button>
<button onClick={this.minus}>Minus</button>
</div> //class 이기 때문에 this 붙힘
}

}

export default App;
