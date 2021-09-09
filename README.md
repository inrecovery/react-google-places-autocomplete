# React Google Places Autocomplete hook

This is the Fork of <a href="https://github.com/tintef/react-google-places-autocomplete">tintef/react-google-places-autocomplete</a>


## Getting started

Install the latest version:
```sh
npm install --save @erslee/react-google-places-autocomplete-hook
  or
yarn add @erslee/react-google-places-autocomplete-hook
```

Use the hook in the component!
```js
import React from 'react';
import useGooglePlacesAutocomplete from '@erslee/react-google-places-autocomplete-hook';

const Component = () => (
  const [ autocompleteData, setAutocompleteData ] = useState([]);
  const [ autocomplete ] = useGooglePlacesAutocomplete({
		apiKey: "***",
		debounce: 300,
		minLengthAutocomplete: 3
	});

  const handleChange = (event) => {
    const value = event.target.value;

    autocomplete(value, (data) => {
      setAutocompleteData(data);
    })
  }

  <div>
    <input onChange={handleChange} />
    {autocompleteData && autocompleteData.map(item => <li>item.label</li>)}
  </div>
);
```

## Original Documentation

Use the component!
```js
import React from 'react';
import GooglePlacesAutocomplete from 'react-google-places-autocomplete';

const Component = () => (
  
  <div>
    <GooglePlacesAutocomplete
      apiKey="****"
    />
  </div>
);

export default Component;
```

**Coming from v2? Check the [migration guide](https://tintef.github.io/react-google-places-autocomplete/docs/v2-to-v3)**

## Documentation

[**Read The Docs**](https://tintef.github.io/react-google-places-autocomplete)

## How to contribute?

1. Fork this repo
2. Clone your fork
3. Code 🤓
4. Test your changes

    For this, I like to use [yalc](https://github.com/whitecolor/yalc), as it allows to emulate the process of using npm/yarn.

    1. Install [yalc](https://github.com/whitecolor/yalc)
    2. Build project with `yarn build` or `npm run build`
    3. Publish the package with yalc: `yalc publish`
    4. Add the package to your test project `yalc add react-google-places-automocomplete`
    5. If needed, to update the package on your test project: `yalc update react-google-places-autocomplete`


5. Submit a PR!


<br />
<br />
<p align="center">
  Icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a>
</p>