```js
import React, {Component} from 'react';

const Joke = ({joke:{setup, punchline}}) => (
  <p style={{margine:20}}>{setup} <em>{punchline}</em></p>
)

class Jokes extends Component {
    state = {joke: {}, jokes: []};
    componentDidMount() {
        fetch('https://official-joke-api.appspot.com/random_joke')
         .then(response => response.json())
         .then(json=> this.setState({joke: json}))
         .catch(error => alert(error.message));
    }
    fetchJokes = () => {
        fetch('https://official-joke-api.appspot.com/random_ten')
         .then(response => response.json())
         .then(json => this.setState({ jokes: json}))
         .catch(error => alert(error.message));
    }
    render() {
        return (
            <div>
                
                <h2>Highlight Joke</h2>
                <Joke joke={this.state.joke} />
                <hr />
                <h3>Want ten more jokes?</h3>
                <button onClick={this.fetchJokes}
                   style={{
                    padding: '10px 10px',
                    borderRadius: '5px'
                   }}>Click me!</button>
                {
                    this.state.jokes.map(joke => {
                        return <Joke key={joke.id} joke={joke} />
                    })
                }
            </div>
        )
    }
}

export default Jokes;
```