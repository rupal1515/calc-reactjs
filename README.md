import React from 'react';
import ReactDOM from 'react-dom';
import App from '.App';

ReactDOM.render(<App />,
  document.getElementBYId('root')
);


import {add,sub,multi,div} from './Cal';

function App(){
  return (
    <>
    <ul>
       <li>{add(40,4)}</li>
       <li>{sub(40,4)}</li>
       <li>{multi(40,4)}</li>
       <li>{div(40,4)}</li>
    </ul>
   </>,
  );
}

export default App;

function add(a,b){
    let sum = a+b;
    return sum;
}

function sub(a,b){
    let sub = a-b;
    return sub;
}
function multi(a,b){
    let multi =a*b;
    return multi;
}
function div(a,b){
    let div = a/b;
    div = div.tofixed(2)
    return div;
}


export {add,sub,multi,div};
