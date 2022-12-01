# Astro Gap

Astro doesn't have a generic way of creating gaps between html elements. There are times where two elements need to be separated with different spaces. Astro Gap solves that problem. It works depending on the parent element's flex, inline  or grid positioning. It also works depending on the axis for both flex and grid. It uses a spacing system that is calculated based on the root font size of the element multiplied by the amount of spacing that you want. This makes it so that you are free to use what ever base font size you want. The script for each gap will only run once.

## Usage

```js
npm i astro-gap
```

## Props 

The `<AstroGap/>` has two props  `spaces=` and `color=`. These props are used to make it do It's job and figure out where one is from another. 

`spaces=` : a number that is based on how many spaces that you want to consume.  

**The number will be multiplied by the parent's font size to determine the total amount of pixels used**

`color=` : the color of the gap it should only be used to see where the gap is and how it is influencing your layout 

**The only colors you can use are red green blue purple black indigo orange yellow brown white**


## Mental Map

The way gap works it that the parent's display property is taken into account then if it's a flexbox or a grid then the gap will change it's width or height accordingly. The table below represents how the `<AstroGap />` will change it's height or width in response to it's parent's properties.   

| Parent Properties                      | Property Changed | 
| -------------------------------------- | ---------------- |
| display: inline                        | width            |
| display: block                         | height           |
| display: grid / grid-auto-flow: row    | height           |
| display: grid / grid-auto-flow: column | width            |
| display: flex / flex-direction: row    | width            |
| display: flex / flex-direction: column | height           |








