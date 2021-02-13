# SMACSS

**Smacss** _(Scalable and Modular Architecture for **CSS**)_ is a style guide that follows five simple categories. **SMACSS** is a way to examine your design process and to fit those rigid frameworks into a flexible thought process. It is an attempt to document a consistent approach to site development when using **CSS**. And really, who isn’t building a site with **CSS** these days?!

#### Which are these categories?

- Base
- Layout
- Module
- State
- Theme

The idea of this architecture is to not mix code of several categories on a single file because it can be very complicated to find a simple line of code to change. Most of the purpose of this categorization is to codify patterns —things that repeat themselves within our design. Repetition results in less code, easier maintenance, and greater consistency in the user experience.

**Base:** _are the defaults values. They are like the padding, `margin`, `border`, `font` and other properties, this values are used on the entire web site and all elements._

**Layout:** _divides a page into sections with elements like `header`, `footer`, `main` page, etc. Layouts hold one or more modules together. Often developers show layout elements by **prefixing the class with l-, e.g. l-header, l-footer**._

**Modules:** _are the reusable, modular parts of our design like `navbar`, `sidebar` and some elements that are repeated in the site._

**State:** _are ways to describe how our modules or layouts will look when they are into a particular state (e.g. active, inactive, expanded, hidden). **These are prefixed with is-, e.g. is-active, is-inactive, is-expanded, is-hidden**._

**Theme:** _Theme rules are similar to state rules in that they describe how modules or layouts might look. It is more applicable for larger sites with shared elements that look different throughout._
