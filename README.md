# accordion
A simple CSS3, HTML5, and ECMA base (Javascript) Accordion style menu, infinitly Nestable


# what is unique about this code base?

I have come to appreciate, in some cases, the need for very default, simple code that gets a particular job done, visually and functionally speaking, when approaching modern markup that may or may not be supported by an intuitive use of Javascript. This particular bit of code accomplishes what many seek in terms of an accordion style menu and often find trouble accomplishing in easyily extensible, or should I say, compliant code.

The Javascript checks for parents and siblings, constantly expanding the parent container DIV/element as needed when child elements are expanded, based on the height alone of it's total number of nested elements. At the time I wrote this it was loosely based off a CSS3 example I found online. But this examples, relying on transitions as mine does, failed to check the height, and effective state of expansion for the total number of nested elements. Many examples of Javascript code for accordion menus suffer from this problem, and do not provide true recursions therein.

# what are the benefits of recursion?

In the simplest sense recursion for an accordion style menu relying on CSS transitions is really, necessary. But by providing the extra for loop where the parent's maxHeight is appropriately set we ensure that no extra nested elements have their contents shown. I found that many examples using this approach, even using recursion, failed to consider this and when a certain level of nested elements was required, would mistakingly collapse nested containers that were expanded if the parent was collapsed. My function will not do that, using maxHeight of the containing parent element, and takes into account all elements using the loop and variable acc, to effectively remember nested elements state.
