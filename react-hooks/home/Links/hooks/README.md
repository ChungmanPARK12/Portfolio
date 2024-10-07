```js
import { useState, useEffect } from 'react';

export const useFetch = (url, initiaValue) => {
    const [result, setResult] = useState(initiaValue);

    useEffect(() => {
        fetch(url)
        //fetch('http://localhost:3005/jokes/random')
         .then(response => response.json())
         .then(json => {
            console.log('joke json', json);
            setResult(json);
        });
    }, []);

    return result;
}
```