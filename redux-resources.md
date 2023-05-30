# Redux: More Topics...

## RTX (Redux Toolkit)

* What concerns are addressed by Redux Toolkit?
  * Redux Toolkit makes Redux easier to use by reducing the amount of code you need to write. 
  * It makes managing global state and creating actions simpler.

* What does configureStore() do?
  * configureStore() sets up your Redux store with some default settings. 
    * It makes it easier to add middleware and to set up the Redux devtools.

* How would I use createSlice()?
  * createSlice() accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.
    * This means you write less code, because you don't need to write action types and creators by hand.

### References

* <https://redux-toolkit.js.org/introduction/getting-started>
* <https://redux-toolkit.js.org/>
* <https://redux-toolkit.js.org/tutorials/overview>

## MobX

* What is Mobx?
  * MobX is a library for managing and synchronizing application state using observables, actions, and reactions

* How does MobX make it “impossible” to produce an inconsistent state?
  * MobX prevents inconsistent state by tracking changes to observables automatically and using actions to make atomic, deterministic changes to state.

* How would we build a reactive user interface?
  * A reactive UI automatically updates when the state changes. 
  * With MobX, you make your state "observable" and your components automatically re-render when the state they depend on changes.

### References

* <https://mobx.js.org/getting-started.html>
* <https://hookstate.js.org/>
