[![alt text][shield-status]][link-repo] [![alt text][shield-production]][link-todo] [![alt text][shield-webc]][link-webc] [![alt text][shield-deps]][link-repo] ![alt text][shield-polymer] [![alt text][shield-license]][link-license]

_[Demo and API docs][link-webc]_

##&lt;signin-button&gt;

A generic sign in button element implementing the [Google Sign-In guidelines](https://developers.google.com/identity/sign-in/web/build-button)

### Usage Instructions

The `signin-button` element creates themed buttons that can be used as login
buttons or as generic similarly-styled buttons.

The `signin-button` can make use of inbuilt providers or can be customized for
others. The element has support for 'short', 'dark theme' and 'tile' (icon only)
variants accessible through properties. The icons used as part of this element
are rendered from SVGs using `iron-icon`.

To customize the element's provider, you can pass in one (or more) of the following:
- attributes such as `provider`, `name`, `icon`, `prefix`, `label`
- an object with the above attributes as properties
- only the `provider` attribute to use one of the inbuilt providers

When you use the `signin-button` element on its own, the inbuilt providers include:
- `anonymous`: For anonymous or demo users
- `email`: For generic email/password sign-in flows
- `facebook`: Facebook
- `github`: GitHub
- `google`: Google
- `twitter`: Twitter
- `unknown`: Unknown provider - this is the fallback when a match cannot be found.

These are the providers used by [Firebase](https://firebase.google.com/) and should
serve majority of users.

It will also import `signin-button/signin-icons.html` containing the following icons:
```
['signin:anonymous', 'signin:email', 'signin:facebook', 'signin:github', 'signin:google', 'signin:twitter', 'signin:unknown']
```

To access more providers, you may also import the `signin-button-more-providers`
element. This element wraps a `signin-button` but adds extra less-common providers.

In the future, you will be able to add providers in a similar fashion to how
[iron-iconset](https://www.webcomponents.org/element/PolymerElements/iron-iconset) adds icons.

### Examples

Using an inbuilt provider:
```
<signin-button provider="google"></signin-button>
```

Configuring a custom provider:
```
<signin-button provider="linkedin" logo-color="#0077B5" name="LinkedIn" icon="my-icons:linkedin"></signin-button>
```

Configuring a custom provider from an object: (as above, but attributes are properties of the object)
```
<signin-button new-provider="[[providerObject]]"></signin-button>
```

## To Do List
This is a brief list of tasks that are yet to be completed. Feel free to open an issue or contribute a pull request if you think you can help.
- Provider addition API akin to `iron-iconset`
- Implement Tests

Demo and API docs: [webcomponents.org][link-webc], [GitHub Pages][link-docs]

[link-docs]: https://samthecodingman.github.io/signin-button/
[link-license]: https://github.com/samthecodingman/signin-button/blob/master/LICENSE
[link-repo]: https://www.github.com/samthecodingman/signin-button
[link-todo]: https://www.github.com/samthecodingman/signin-button#to-do-list
[link-webc]: https://www.webcomponents.org/element/samthecodingman/signin-button
[shield-deps]: https://img.shields.io/badge/dependencies-polymer-green.svg "Dependencies: polymer"
[shield-license]: https://img.shields.io/badge/license-MIT-blue.svg "License: MIT"
[shield-polymer]: https://img.shields.io/badge/polymer%20version-1.0-yellow.svg "Polymer Version: 1.0"
[shield-production]: https://img.shields.io/badge/production--ready-no-red.svg "Production Ready: no"
[shield-status]: https://img.shields.io/badge/status-beta-yellow.svg "Status: beta"
[shield-webc]: https://img.shields.io/badge/webcomponents.org-published-blue.svg "Published on webcomponents.org"
