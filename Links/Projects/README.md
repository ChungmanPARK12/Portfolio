```js
import React from "react";
import PROJECTS from "../data/projects";

const Project = props => {
        const {title, image, description, link} = props.project;

        return(
            <div style={{ display: 'inline-block', width: 300, margin:30}}>
              <h3>{title}</h3>
              <img src={image} alt='profile' style={{width: 200, height: 120}}/>
              <p>{description}</p>
              <button  
                    onClick={() => window.open(link, '_blank')}
                    style={{
                        padding: '10px 20px',
                        backgroundColor: '#d3d3d3',
                        color: 'black',
                        borderRadius: '5px',
                        cursor: 'pointer',
                        marginTop: '10px'
                    }}>Visit Project
                </button>
            </div>
        )   
}

const Projects = () => (   
    <div>
        <h2>Achievement</h2>
        <div>
            {
             PROJECTS.map(PROJECT => (
                
                     <Project key={PROJECT.id} project={PROJECT}/>
                    )
                )
            }
        </div>
    </div>
)
    


export default Projects;
```