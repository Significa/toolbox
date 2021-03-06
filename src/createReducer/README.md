# createReducer

This function allows to express the reducers as an object mapping from action types to handlers.

- Redux
- Reducer

## Usage

```js
const initialState = [];

export const todos = createReducer(initialState, {
  [types.ADD_TODO]: (state, action) => {
    const text = action.text.trim();
    return [...state, text];
  },

  [types.REMOVE_TODO]: (state, action) => {
    return state.filter((_, i) => i !== action.index);
  }

})
```
