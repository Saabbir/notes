## Vue Directives:

| Name      | Description |
| --------- | ----------- |
| v-text	  | Updates the element’s textContent. |
| v-html	  | Updates the element’s innerHTML. |
| v-show	  | Toggles the element’s display CSS property based on the truthy-ness of the expression value. |
| v-if	    | Conditionally render the element based on the truthy-ness of the expression value. |
| v-else	  | |
| v-else-if	| |
| v-for	    | Render the element or template block multiple times based on the source data. |
| v-on	    | Attaches an event listener to the element. |
| v-bind	  | Dynamically bind one or more attributes, or a component prop to an expression. |
| v-model	  | Create a two-way binding on a form input element or a component. |
| v-slot	  | Denote named slots or slots that expect to receive props. |
| v-pre	    | Skip compilation for this element and all its children. You can use this for displaying raw mustache tags. Skipping large numbers of nodes with no directives on them can also speed up compilation. |
| v-cloak	  | This directive will remain on the element until the associated Vue instance finishes compilation. |
| v-once	  | Render the element and component once only. |

_More on directives - https://vuejs.org/v2/api/#Directives_

## VUEX Notes:

- Vuex mutation functions mutate the state and can only do synchronous tasks.

- Vuex action functions commit/call the mutation functions and can do asynchronous tasks.

- We can invoke/call a mutation function using store/$store/context.commit() method.

- We can invoke/call a action function using store/$store/context.dispatch() method.

- Both mutation and action functions can take payload.

## VUEX Flow of Data:

1. Vuex action function calls api function (defined in src/services/api directory) which creates http request and returns response. 

2. Then Vuex action function calls appropriate mutation function with that response data. 

3. Then Vuex mutation function mutate the state.

4. Then on state change the DOM gets updated and rerender the view.