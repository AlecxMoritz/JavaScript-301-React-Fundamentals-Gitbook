# 2.0 - Concept List

Our next app will be a little twist on a typical to do list application, with a focus on keeping track of your progress of understanding React components.

## What We're Going to Build & Learn

* A list app where you can add items and cross them off when they're done
* More about state and life cycle methods. 
* More about functional components and ES6

## Getting Started

To get started, we need to set up our routing to be able to access the application and our folder structure.bbInside of `Sidebar.js` insert the following link:

```javascript
<li><Link to="/reactconceptlist">React Concepts Checklist</Link></li>
```

In `_routes.js` add the following route:

```javascript
    {
      path: '/reactconceptlist',
      exact: true,
      main: () => <ReactConceptsApp />
    },
```

Don't forget to add the import for the component!

```javascript
import ReactConceptsApp from '../apps/concept-list-app/ReactConceptsApp';
```

## Folder structure

Now, in our folder structure we need to create a folder for our app. Underneath \(and outside of\) your timer-apps folder, create a new folder called `concept-list-app`.

```text
    └── src
        └── assets
        └── components
                └── apps
                    └── concept-list-app
                         └── Concept.js
                         └── ConceptList.js
                         └── concepts.js
                         └── NewConcept.js
                         └── ReactConceptsApp.js
                    └── timer-apps
```

Inside of this folder, we're going to start with creating our parent component for our app called `ReactConceptsApp.js`.

## Basic Component

Set up the basic component by typing out the following code:

```javascript
import React, { Component }  from 'react';

export default class ReactConceptsApp extends Component {
    render() {
        return (
            <div className="main">
                <div className="mainDiv">
                    <h1>Concept List App</h1>
                    <p>Use the list below to toggle concepts that you do or do not understand. Note that this will update when you refresh the page.</p>
                </div>
            </div>
        );
    }
}
```

Next, we're going to set up the data for the concepts that we want to include in our app!

[Concept Data](2.1-concept-data.md)

