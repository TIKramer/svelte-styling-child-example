# svelte-styling-child-example

## Problem: 

A tag component that is used throughout the app could have any background/text color with possible icon.

Two solutions to styling - I'm not sure which is better.

For styling a custom tag component:

<img src="https://github.com/TIKramer/svelte-styling-child-example/blob/main/example.png" width="60%" height="30%">

### Solution 1
Creating a new component for each different tag set, with styles defined inside the component. This approach results in some repeated code across different tag sets.

### Solution 2
Create a tag component that you can pass style values using --color and --background, and then create subcomponents of this component. Minimizes some code repetition
