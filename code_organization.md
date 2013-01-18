## CSS Code Organization

Jonathan Snook offers a stucture for CSS organization in his book SMACSS, in which he presents his view on DRY and maintainable CSS. The structure he proposes is organized in 5 levels of specificity:

1. **Base** - Global Styles en resets
2. **Layout** - Positionering van de pagina-elementen (``.l-header``, ``.l-sidebar``)
3. **Modules** - De verschillende modules welke worden gebruikt
4. **State** - Defines the appearance of the current state a module/component is in. These states should indicate a temporary styling based on a specific temporary ruleset. (``.is-active``, ``.is-clicked``, ``.is-invalid``). These are different from extentions in the sense that extentions differ based on context, not states.
5. **Themes** - Especially used in very large projects which need to be able to switch between different 'themes' depending on for example the season or user-settings.

This structure can also be applied to the organization of the files in a project.

One specific css file (which is referenced in the index.html) imports  base.css, layout.css and modules.css. Modules.css in itself imports the seperate modules, which are defined in their own file for easy lookup and maintenance.

    --css/
     | --app.css
     | --base.css
     | --base/
       | --general.css
       | --reset.css
     | --layout.css
     | --modules.css
     | --modules/
       | --module-1.css
       | --module-2.css
       | --module-3.css
       | --module-4.css


These files should be further optimized trough concatination and compression in order to reduce HTTP-requests and filesize. This can be done trough [GruntJS](www.grunt.com) or the [r.js optimizer](www.requirejs.com) of RequireJS. Otherwise a CSS-preprocessor like [Sass](www.sass.com) can help with the optimization process, as well as add several other benefits.
