# angular-styleguide
This guide is heavily biased towards large enterprises with many software projects with team members highly cross cut among projects. For this reason, we will set the stage with a fictitious company and its products. It is an opinionated guide but will often provide more than one way to follow for a specific style.

*This guide is heavily influenced by John Papa's Angular Style Guide and can be thought of as extending it. Where something is not specifically mentioned here, you can fall back to the John Papa Style Guide style(s) mentioned there.*

Come up with a short acronym for the name of your company  
Company: Rusty Parts Inc.  
Acronym: RP

Come up with a short and company unique acronym for the name of your product  
Software Product: Part Scanner  
Acronym: PS

## Modules

### Naming

With a long company name and products names that can be just as lengthy, it makes more sense to come up with some acronyms to use in your company for naming angular modules. Prefix all module names like `companynameacronym.productnameacronym`. Then, add one dot-delimited segment for each folder.

A project with a folder structure like part-scanner/app/scanner containing an angular module would be defined like so

```javascript
angular.module('rp.ps.scanner');
```

## Services*, factories and providers*

### Naming

*coming*

## Functions and class methods

### Naming

Functions and class method names should be descriptive and specific following the lower camel case convention.

```javascript
performAlgorithmA() {
}
```

**Async Promise returning functions**

If a function returns a promise, it should be suffixed with `Async`. This is a good convention that portrays intent especially when used with the upcoming version of ECMAScript that includes the `async` and `await` keywords.

```javascript
createPartAsync(part) {
  return $http.post('/parts', part);
}
```
