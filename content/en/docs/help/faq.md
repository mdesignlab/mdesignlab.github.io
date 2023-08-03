---
title: "FAQ"
description: "Answers to frequently asked questions."
lead: "Answers to frequently asked questions."
date: 2020-10-06T08:49:31+00:00
lastmod: 2020-10-06T08:49:31+00:00
draft: false
images: []
menu:
  docs:
    parent: "help"
weight: 630
toc: true
---
<h2>
on the progress
</h2>

<!-- ## Hyas?

Doks is a [Hyas theme](https://gethyas.com/themes/) build by the creator of Hyas.

## Footer notice?

Please keep it in place.

## Keyboard shortcuts for search?

- focus: `Ctrl + /`
- select: `↓` and `↑`
- open: `Enter`
- close: `Esc`

## Other documentation?

- [Netlify](https://docs.netlify.com/)
- [Hugo](https://gohugo.io/documentation/)

## Can I get support?

Create a topic:

- [Netlify Community](https://community.netlify.com/)
- [Hugo Forums](https://discourse.gohugo.io/)
- [Doks Discussions](https://github.com/h-enk/doks/discussions)

## Contact the creator?

Send `h-enk` a message:

- [Netlify Community](https://community.netlify.com/)
- [Hugo Forums](https://discourse.gohugo.io/)
- [Doks Discussions](https://github.com/h-enk/doks/discussions)

<svg xmlns="http://www.w3.org/2000/svg" style="display: none;">
  <symbol id="check-circle-fill" fill="currentColor" viewBox="0 0 16 16">
    <path d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zm-3.97-3.03a.75.75 0 0 0-1.08.022L7.477 9.417 5.384 7.323a.75.75 0 0 0-1.06 1.06L6.97 11.03a.75.75 0 0 0 1.079-.02l3.992-4.99a.75.75 0 0 0-.01-1.05z"/>
  </symbol>
  <symbol id="info-fill" fill="currentColor" viewBox="0 0 16 16">
    <path d="M8 16A8 8 0 1 0 8 0a8 8 0 0 0 0 16zm.93-9.412-1 4.705c-.07.34.029.533.304.533.194 0 .487-.07.686-.246l-.088.416c-.287.346-.92.598-1.465.598-.703 0-1.002-.422-.808-1.319l.738-3.468c.064-.293.006-.399-.287-.47l-.451-.081.082-.381 2.29-.287zM8 5.5a1 1 0 1 1 0-2 1 1 0 0 1 0 2z"/>
  </symbol>
  <symbol id="exclamation-triangle-fill" fill="currentColor" viewBox="0 0 16 16">
    <path d="M8.982 1.566a1.13 1.13 0 0 0-1.96 0L.165 13.233c-.457.778.091 1.767.98 1.767h13.713c.889 0 1.438-.99.98-1.767L8.982 1.566zM8 5c.535 0 .954.462.9.995l-.35 3.507a.552.552 0 0 1-1.1 0L7.1 5.995A.905.905 0 0 1 8 5zm.002 6a1 1 0 1 1 0 2 1 1 0 0 1 0-2z"/>
  </symbol>
</svg>

<div class="alert alert-primary d-flex align-items-center" role="alert">
  <svg class="bi flex-shrink-0 me-2" width="24" height="24" role="img" aria-label="Info:"><use xlink:href="#info-fill"/></svg>
  <div>
    An example alert with an icon
  </div>
</div>
<div class="alert alert-success d-flex align-items-center" role="alert">
  <svg class="bi flex-shrink-0 me-2" width="24" height="24" role="img" aria-label="Success:"><use xlink:href="#check-circle-fill"/></svg>
  <div>
    An example success alert with an icon
  </div>
</div>
<div class="alert alert-warning d-flex align-items-center" role="alert">
  <svg class="bi flex-shrink-0 me-2" width="24" height="24" role="img" aria-label="Warning:"><use xlink:href="#exclamation-triangle-fill"/></svg>
  <div>
    An example warning alert with an icon
  </div>
</div>
<div class="alert alert-danger d-flex align-items-center" role="alert">
  <svg class="bi flex-shrink-0 me-2" width="24" height="24" role="img" aria-label="Danger:"><use xlink:href="#exclamation-triangle-fill"/></svg>
  <div>
    An example danger alert with an icon
  </div>
</div>

<div class="bd-callout bd-callout-info">
<h5 id="conveying-meaning-to-assistive-technologies">Conveying meaning to assistive technologies</h5>
<p>Using color to add meaning only provides a visual indication, which will not be conveyed to users of assistive technologies – such as screen readers. Ensure that information denoted by the color is either obvious from the content itself (e.g. the visible text), or is included through alternative means, such as additional text hidden with the <code>.visually-hidden</code> class.
</div>

<div class="callout">...</div>

<p>For more information and examples on how to modify our Sass maps and variables, please refer to <a href="/docs/5.0/layout/grid/#sass">the Sass section of the Grid documentation</a>.</p>
<h2 id="creating-your-own">Creating your own</h2>
<p>We encourage you to adopt these guidelines when building with Bootstrap to create your own components. We&rsquo;ve extended this approach ourselves to the custom components in our documentation and examples. Components like our callouts are built just like our provided components with base and modifier classes.</p>
<div class="bd-example">
  <div class="bd-callout my-0">
    <strong>This is a callout.</strong> We built it custom for our docs so our messages to you stand out. It has three variants via modifier classes.
  </div>
</div>
<div class="highlight"><pre class="chroma"><code class="language-html" data-lang="html"><span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">&#34;callout&#34;</span><span class="p">&gt;</span>...<span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</code></pre></div><p>In your CSS, you&rsquo;d have something like the following where the bulk of the styling is done via <code>.callout</code>. Then, the unique styles between each variant is controlled via modifier class.</p>
<div class="highlight"><pre class="chroma"><code class="language-scss" data-lang="scss"><span class="c1">// Base class
</span><span class="c1"></span><span class="nc">.callout</span> <span class="p">{}</span>

<span class="c1">// Modifier classes
</span><span class="c1"></span><span class="nc">.callout-info</span> <span class="p">{}</span>
<span class="nc">.callout-warning</span> <span class="p">{}</span>
<span class="nc">.callout-danger</span> <span class="p">{}</span>
</code></pre></div><p>For the callouts, that unique styling is just a <code>border-left-color</code>. When you combine that base class with one of those modifier classes, you get your complete component family:</p>
<div class="callout callout-info">
<strong>This is an info callout.</strong> Example text to show it in action.
</div>

<div class="callout callout-warning">
<strong>This is a warning callout.</strong> Example text to show it in action.
</div>

<div class="callout callout-danger">
<strong>This is a danger callout.</strong> Example text to show it in action.
</div>

      </div>
    </main>
  </div>
 -->
