# Change Log

## [1.3.3] 2025-03-31

- Implement react-photoswipe-gallery:
  - Replace deprecated PhotoSwipeGallery component with modern Gallery and Item components
  - Update gallery layout with responsive grid styling
  - Fix CSS import issues for PhotoSwipe by importing directly in components
  - Create reusable MyGallery component to simplify usage

## [1.3.2] 2023-05-25

- Fix issues
- Update dependencies

## [1.3.1] 2022-08-19

- Update the dependencies
- Migration to React 18
- Migration to sass from node-sass

## [1.3.0] 2021-03-24

### Bug fixing

- https://github.com/creativetimofficial/ct-paper-kit-pro-react/issues/9
- https://github.com/creativetimofficial/ct-paper-kit-pro-react/issues/7 (added more info in docs)
- https://github.com/creativetimofficial/ct-paper-kit-pro-react/issues/4
- Changed the way we import images
  - Old way: `require("path/to/imgae")`
  - New way: `require("path/to/imgae").default`

### Major style changes

### Deleted components

### Added components

### Deleted dependencies

- `react-photoswipe` (replaced by `react-photoswipe-gallery`)
- `react-bootstrap-switch` (replaced by the simple Bootstrap Switch: https://reactstrap.github.io/components/form/#Custom-Inputs)
- `react-tagsinput` (replaced by inner component - but the docs for this plugins still apply)
- `react-google-maps` (replaced by simple Google Maps API)
- `@types/googlemaps` (replaced by simple Google Maps API)
- `@types/markerclustererplus` (replaced by simple Google Maps API)
- `@types/react` (replaced by simple Google Maps API)

### Added dependencies

- `bootstrap@4.6.0`
- `jquery@3.6.0` (Only to stop warnings from Bootstrap)
- `react-photoswipe-gallery@1.3.4`
- `photoswipe@4.1.3`

### Updated dependencies

```
headroom.js       0.11.0   →   0.12.0
moment            2.26.0   →   2.29.1
node-sass         4.14.1   →    5.0.0
nouislider        14.5.0   →   14.6.4
react            16.13.1   →   17.0.2
react-datetime    2.16.3   →    3.0.4
react-dom        16.13.1   →   17.0.2
react-scripts      3.4.1   →    4.0.3
react-select       3.1.0   →    4.3.0
reactstrap         8.4.1   →    8.9.0
typescript         3.9.5   →    4.2.3
```

### Warning

_When doing a clean install, you might have some warnings, those come from `node_modules` and do not affect the project in any way._
_The following two error might occur while doing a clean install - They do not affect the product in any way:_
_npm WARN react-datetime@3.0.4 requires a peer of react@^16.5.0 but none is installed. You must install peer dependencies yourself._
_npm WARN @babel/plugin-bugfix-v8-spread-parameters-in-optional-chaining@7.13.12 requires a peer of @babel/core@^7.13.0 but none is installed. You must install peer dependencies yourself._

## [1.2.0] 2020-06-12

### Bug fixing

- https://github.com/creativetimofficial/ct-paper-kit-pro-react/issues/2
- https://github.com/creativetimofficial/ct-paper-kit-pro-react/issues/1
- Other Paper React products issues solved here as well
  - https://github.com/creativetimofficial/paper-kit-react/issues/2
  - https://github.com/creativetimofficial/paper-dashboard-react/issues/15
  - https://github.com/creativetimofficial/paper-dashboard-react/issues/8
  - https://github.com/creativetimofficial/ct-paper-dashboard-pro-react/issues/8
  - https://github.com/creativetimofficial/ct-paper-dashboard-pro-react/issues/6 - solution to this is to change the usage of the ModalHeader from reactstrap to simple Bootstrap ones:
    So, instead of:

```
<ModalHeader className="justify-content-center" toggle={this.toggleModalDemo}>
    Modal Title
</ModalHeader>
```

You should use

```
<div className="modal-header justify-content-center">
  <button type="button" className="close" data-dismiss="modal" aria-label="Close" onClick={this.toggleModalDemo}>
    <span aria-hidden="true">×</span>
  </button>
  <h5 className="modal-title">Modal Title</h5>
</div>
```

### Major style changes

- `src/assets/scss/paper-kit/_nucleo-outline.scss` (changed the fonts import to `~assets/fonts` and also added assets path inside `jsconfig.json` file)
- `src/assets/scss/paper-kit/_nucleo-icons.scss` (changed the fonts import to `~assets/fonts` and also added assets path inside `jsconfig.json` file)
- `src/assets/scss/paper-kit/plugins/photo-swipe/_main-settings.scss` (changed the images import to `~assets/img` and also added assets path inside `jsconfig.json` file)
- `src/assets/scss/react/paper-kit/_responsive.scss` (solution for https://github.com/creativetimofficial/ct-paper-kit-pro-react/issues/1)

### Deleted components

### Added components

### Deleted dependencies

### Added dependencies

- gulp@4.0.2 (for Creative Tim copyrights)
- gulp-append-prepend@1.0.8 (for Creative Tim copyrights)

### Updated dependencies

```
headroom.js           0.9.4   →    0.11.0
moment               2.24.0   →    2.26.0
node-sass            4.12.0   →    4.14.1
nouislider           14.0.2   →    14.5.0
react                16.8.6   →   16.13.1
react-dom            16.8.6   →   16.13.1
react-router-dom      5.0.1   →     5.2.0
react-scripts         3.0.1   →     3.4.1
react-select          3.0.4   →     3.1.0
reactstrap            8.0.0   →     8.4.1
@types/googlemaps    3.36.6   →    3.39.6
@types/react        16.8.23   →   16.9.35
typescript            3.5.2   →     3.9.5
```

### Warning

_All the following products: Paper Kit React, Paper Dashboard React, Paper Kit PRO React and Paper Dashboard PRO React have been updated together, and thus, we've added to all of them the same version of 1.2.0 - we may have skipped some versions for some of the above products, we've done so, since we want all Paper & React products to share the same versions._
_While in development some of the plugins that were used for this product will throw some warnings - note, this only happens in development, the UI or the functionality of the product is not affected, also, if the issues will persist in React 17, we'll drop usage of those plugins, and replace them with other ones._
_Warnings might appear while doing an npm install - they do not affect the UI or the functionality of the product, and they appear because of NodeJS and not from the product itself._

## [1.0.0] 2019-07-15

### Original Release

- Added Reactstrap as base framework
- Added React and React Hooks
- Added design from Paper Kit 2 PRO by Creative Tim
