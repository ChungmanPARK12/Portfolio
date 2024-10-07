```js
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);

// function createObject() {
//     return {
//         arrowFunction: () => {
//             console.log('arrowFunction this', this);
//         },
//         functionKeywordFunction: function () {
//             console.log('functionKeyword this', this);
//         }
//     }
// }
// const obj = createObject();
// console.log('obj', obj);
// obj.arrowFunction();
// obj.functionKeywordFunction();



```