# vue add nativescript-vue-preset
Fixes most errors caused by installing &lt;nativescript-vue> plugin. 

**IMPORTANT:** run \"vue invoke nativescript-vue-preset\" twice after adding. 

What does it do:
* ✅ Adds support for platform-tagged CSS lines: e.g. adding `[web]` will keep that line for `web`, but not in native. Multiple tags per line can be added e.g. `[web][android]` will only keep that line in `web` & `android`, but will remove it for iOS builds etc.
    * Supported platform tags are:
        ```
        * web: ['web', 'w', 'cross']
        * ios: ['native', 'n', 'ios', 'apple', 'cross']
        * android: ['native', 'n', 'android', 'cross']
        ```
* ✅ Adds .eslint.js, with support for fixed module-require resolving + disables unreasonable rules `(you can always edit .eslintrc.js to suit your style)`
* ✅ Replaces `~/` tilde with `@/`at paths: fixes `Unable to resolve path to module` `import/no-unresolved` &amp; `import/extensions`
