```css
@font-face{
    font-family: RobotoCondensed;
    src: url(assets/roboto-condensed.light.ttf);
    font-weight: 1000;
}

@font-face{
    font-family: EocnomicaBold;
    src: url(assets/economica-bold.ttf);
    
}

body {
    text-align: center;
    font-size: 20px;
    padding: 2.5%;
    font-family: 'RobotoCondensed';
}

h1, h2, h3, h4, h5 {
    font-family: 'EconomicaBold';
}

.track {
    width: 250px;
    height: 250px;
    position: relative;
    display: inline-block;
    margin: 20px;
    cursor: pointer;
     
}
.track-image {
    width: 250px;
    height: 250px;
    vertical-align: bottom; 
}
.track-text {
    background-color: black;
    color: white;
    padding: 5px;
    margin: 0px;   
}
.track-icon {
    position: absolute;
    bottom: 80px;
    left: 105px;
    color: white;
    background-color: black;
    width: 25px;
    height: 30px;
    border-radius: 25px;
    padding: 8px;
    opacity: 0.8;
}

/* .track-text {
    position: absolute;
    width: 250px;
    bottom: 0px;
    background-color: black;
    color: white;
    padding: 5px;
} */
```