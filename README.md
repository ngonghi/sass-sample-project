# sass-sample-project

Sass architecture and style organization.

## 7-1 pattern

There are seven folders and one main.scss file for output.

- base/ – contains global styles, such as resets, typography, colors, etc.
- components/ – contains each self-contained component in its own .scss partial
- layout/ – contains styling for larger layout components; e.g. nav, header, footer, etc.
- pages/ – contains page-specific styling, if necessary
- themes/ – contains styling for different themes
- utils/ – contains global mixins, functions, helper selectors, etc.
- vendors/ – contains 3rd-party styles, mixins, etc.
- main.scss – output file that brings together all of the above parts


Each folder should have a single .scss partial file that collects the other files in the same directory – such as _module.scss (my preference) or _glob.scss
Then, you can reference each of these in the main.scss file:

```
// main.scss
@import 'base/module';
@import 'components/module';
@import 'layout/module';
@import 'pages/module';
@import 'themes/module';
@import 'utils/module';
@import 'vendors/module';

```
