# Rasterfari - Easy peasy grid system, ya man

## Default Settings

Feel free to overwrite them with your prefered values.

```css
@import "path/to/rasterfari.scss";

/* some styles */

$rasterfari__cols: 12 !default;         /* Use 16 if you want bigger Grid, Just rename it 16 */
$rasterfari__gutter: 20px !default;     /* You can make the Gutter bigger or smaller when you change the value */
$rasterfari__namespace: '' !default;    /* You can add a Name to the Grid */
$rasterfari__breakpoints: (             /* Grid breakpoints */
    'medium': '(min-width: 40em)',      /* You can change the breakpoints naming too, but don't forget to rename it everywhere */
    'large': '(min-width: 64em)'        /* Add a new breakpoint to the Grid if you need */
) !default;

/* some more styles */
```
## Basic usage

```html
<section class="grid">
    <div class="grid__col">
        <div class="example-col">12 cols</div>
    </div>
    <div class="grid__col  grid__col--11@medium">
        <div class="example-col">11 cols</div>
    </div>
    <div class="grid__col  grid__col--1@medium">
        <div class="example-col">1 col</div>
    </div>
    <div class="grid__col  grid__col--10@medium">
        <div class="example-col">10 cols</div>
    </div>
    <div class="grid__col  grid__col--2@medium">
        <div class="example-col">2 cols</div>
    </div>
    <div class="grid__col  grid__col--6@medium">
        <div class="example-col">6 cols</div>
    </div>
    <div class="grid__col  grid__col--6@medium">
        <div class="example-col">6 cols</div>
    </div>
</section>
```
## Responsive Grid

```html
<section class="grid">
    <aside class="grid__col  grid__col--4@medium  grid__col--2@large">
        <div class="example-col">Aside</div>
    </aside>
    <main class="grid__col  grid__col--8@medium  grid__col--10@large">
        <div class="example-col">Main</div>
    </main>
</section>
```

## Nested Grid

```html
<section class="grid">
    <aside class="grid__col  grid__col--4@medium  grid__col--2@large">
        <div class="example-col">Aside</div>
    </aside>
    <main class="grid__col  grid__col--8@medium  grid__col--10@large">
        <div class="example-col">
            <p>Main</p>
            <div class="grid">
                <div class="grid__col  grid__col--6@medium">
                    <div class="example-nested-col">Nested Grid 1</div>
                </div>
                <div class="grid__col  grid__col--6@medium">
                    <div class="example-nested-col">Nested Grid 2</div>
                </div>
                <div class="grid__col  grid__col--4@medium">
                    <div class="example-nested-col">Nested Grid 3</div>
                </div>
                <div class="grid__col  grid__col--8@medium">
                    <div class="example-nested-col">Nested Grid 4</div>
                </div>
            </div>
        </div>
    </main>
</section>
```

## Push & Pull

```html
<section class="grid">
    <div class="grid__col  grid__col--8@medium  is-pushed-by-4@large">
        <div class="example-col">Main Content</div>
    </div>
    <div class="grid__col  grid__col--4@medium  is-pulled-by-8@large">
        <div class="example-col">Aside</div>
    </div>
    <div class="grid__col  grid__col--6@medium  grid__col--8@large  is-pushed-by-3@medium  is-pushed-by-2@large">
        <div class="example-col">Main Content</div>
    </div>
    <div class="grid__col  grid__col--3@medium  grid__col--2@large  is-pulled-by-6@medium  is-pulled-by-8@large">
        <div class="example-col">Aside Left</div>
    </div>
    <div class="grid__col  grid__col--3@medium  grid__col--2@large">
        <div class="example-col">Aside Right</div>
    </div>
</section>
```

## Grid without Gutter

```html
<section class="grid  has-no-gutter">
    <aside class="grid__col  grid__col--4@medium  grid__col--2@large">
        <div class="example-col">Aside</div>
    </aside>
    <main class="grid__col  grid__col--8@medium  grid__col--10@large">
        <div class="example-col  example-col--has-no-gutter">Main</div>
    </main>
</section>
```

## Middle aligned Grid System

```html
<section class="grid  is-middle">
        <div class="grid__col  grid__col--6@medium">
            <div class="example-col">6 cols</div>
        </div>
        <div class="grid__col  grid__col--6@medium">
            <div class="example-col">6 cols <br>More Content <br>More Content... <br>More...</div>
        </div>
</section>
```

## Bottom aligned Grid System

```html
<section class="grid  is-bottom">
    <div class="grid__col  grid__col--6@medium">
        <div class="example-col">6 cols</div>
    </div>
    <div class="grid__col  grid__col--6@medium">
        <div class="example-col">6 cols <br>More Content <br>More Content... <br>More...</div>
    </div>
</section>
```