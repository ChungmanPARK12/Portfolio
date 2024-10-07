```js
import React, {Component} from 'react';
import Projects from './Projects';
import SocialProfiles from './SocialProfiles';
import profile from '../assets/profile1.jpg';
import Title from './Title';

class App extends Component {

    state = {displayBio: false};
    toggleDisplayBio= () => {
        // this.state.displayBio = !this.state.displayBio;
        this.setState({ displayBio: !this.state.displayBio});
    }

    render(){
        return(
            <div>
                
                <img src={profile} alt='profile' className='profile' />
                <h1>Hello!</h1>
                <p>My name is Chungman Park</p>
                <Title /> 
               
                {
                 this.state.displayBio ? (
                    <div>
                       <p>Passionate junior developer</p>
                       <p>Committed to continuoust learning and growth in tech</p>
                      <button onClick={this.toggleDisplayBio}>Close</button>
                    </div>
                 ) : (
                    <div>
                        <button onClick={this.toggleDisplayBio}>Read more</button>
                    </div>
                 )
                }
                <hr />
                <Projects />
                <hr />
                <SocialProfiles />
              
            </div>
        )
    }
}
export default App;

```