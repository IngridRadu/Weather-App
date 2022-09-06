# Weather React App
A React application with login interface, where users can search for weather in a city or multiple cities.
The cities can then be sorted by temperature or by city name, also a city can be deleted when the user wants.

## Install
npm install

### Run
npm start

# Download the code
https://github.com/IngridRadu/Weather-App.git

# Quick look

Search Component

```
import react, { useEffect } from "react";

const SearchComponent = (props) => {
  return (
    <div className="search-box">
      <input
        type="text"
        className="search"
        placeholder="City..."
        onChange={(event) => props.setCity(event.target.value)}
        onKeyDown={props.handleKeyDown}
        value={props.city}
      />
      <button type="button" className="btn" onClick={props.getWeather}>
        Search
      </button>
      <button type="button" className="btn" onClick={props.sortByTemp}>
        Sort by Temp
      </button>
      <button type="button" className="btn" onClick={() => props.sortByName()}>
        Sort by Name
      </button>
    </div>
  );
};

export default SearchComponent;
```
