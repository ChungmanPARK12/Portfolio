```js
import React from 'react';
import SOCIAL_PROFILES from '../data/socialProfiles';

const SocialProfile = props => {
    const {link, image} = props.socialProfile;

    const openInNewWindow = () => {
        window.open(link, '_blank', 'noopener,noreferrer');
    }

    return (
        <span onClick={openInNewWindow} style={{cursor: 'pointer'}}>
            <img src={image} alt='social-profile' style={{width: 35, height: 35, margin:10}}/>
        </span>
    )  
}

const SocialProfiles = () => (
    <div>
        <h2>Connect with me!</h2>
        <div>
            {
                 SOCIAL_PROFILES.map(SOCIAL_PROFILE => {
                 return <SocialProfile key={SOCIAL_PROFILE.id} socialProfile={SOCIAL_PROFILE}/>;
                    
                })
            }
        </div>
    </div>
)
 
export default SocialProfiles;
```