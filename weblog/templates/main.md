<!DOCTYPE html>
<html lang="en">
<head>
<title>{weblog-title}{separator}{post-title}</title>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
{feeds}
<style>
@import url('https://static.omg.lol/type/font-honey.css');
@import url('https://static.omg.lol/type/font-lato-regular.css');
@import url('https://static.omg.lol/type/font-lato-bold.css');
@import url('https://static.omg.lol/type/font-lato-italic.css');
@import url('https://static.omg.lol/type/font-md-io.css');
@import url('https://static.omg.lol/type/fontawesome-free/css/all.css');

* {
  box-sizing: border-box;
}

body {
  font-family: 'Lato', sans-serif;
  font-size: 120%;
  color: var(--foreground);
  background: var(--background);
}

header nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

header nav li {
  display: inline-block;
}

header nav li a {
  display: block;
  text-decoration: none;
  margin-right: 1em;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'VC Honey Deck', serif;
  margin: 1rem 0;
}

p,
li {
  line-height: 160%;
}

header,
main,
footer {
  max-width: 60em;
  margin: 2em auto;
  padding: 0 1em;
}

header {
  margin-top: 4em;
}

footer p {
  margin-top: 5em;
  font-size: 90%;
  text-align: center;
}

a:link {
  color: var(--link);
}

a:visited {
  color: var(--link);
}

a:hover {
  color: var(--link);
}

a:active {
  color: var(--link);
}

.post-info,
.post-tags {
  font-size: 85%;
  color: var(--accent);
  text-align: right;
}

.post-info i:nth-child(2) {
  margin-left: .75em;
}

.tag {
  background: var(--accent);
  color: var(--background) !important;
  padding: .3em .4em;
  margin: .8em 0 0 .4em;
  border-radius: .5em;
  text-decoration: none;
  display: inline-block;
}

hr {
  border: 0;
  height: 1px;
  background: var(--accent);
  margin: 2em 0;
}

code {
  padding: .2em .3em;
  border: 1px solid var(--accent);
  white-space: pre-wrap;
  word-wrap: break-word;
}

pre,
code {
  font-family: 'MD IO 0.4';
  font-size: 90%;
}

pre code {
  background: var(--background);
  color: var(--foreground);
  display: inline-block;
  padding: 1em;
  white-space: pre-wrap;
  word-wrap: break-word;
}

img {
  max-width: 100%;
}

table {
  border-collapse: collapse;
}

td,
th {
  padding: .75em;
  text-align: left;
  border: 1px solid var(--accent);
}

.weblog-title a {
  text-decoration: none;
  color: var(--foreground);
}
</style>
<link rel="preload" href="https://cdn.themes.lol/styles/assets/css/styles--vinca-styles.css?05042024" as="style" fetchpriority="high">
</head>

<body>

  <header>
    <h1 class="weblog-title"><a href="{base-path}">{weblog-title}</a></h1>
    {navigation}
  </header>

  <main>

    <article>
      {body}
      <aside class="post-info">
        <i class="fa-solid fa-clock"></i> {date}
      </aside>
      <aside class="post-tags">
        {tags}
      </aside>
    </article>

    <hr>

    <h2>Recent posts</h2>

    {recent-posts}

<h2>Weblog.lol Webring</h2>

<div style="width: fit-content; border: 2px outset; text-align:center">
<p style="margin: 0; padding: 0.1em; border: 2px inset">This site is a member of The Unofficial weblog.lol Webring.</p>
<div style="display: flex">
<a style="flex: 1; margin: 0; padding: 0.1em; border: 2px inset" href="https://webri.ng/webring/webloglol/previous?via=https%3A%2F%2Fblog.darylsun.page%2F">Previous Site</a>
<a style="flex: 1; margin: 0; padding: 0.1em; border: 2px inset" href="https://webri.ng/webring/webloglol/random?via=https%3A%2F%2Fblog.darylsun.page%2F">Random Site</a>
<a style="flex: 1; margin: 0; padding: 0.1em; border: 2px inset" href="https://webri.ng/webring/webloglol/next?via=https%3A%2F%2Fblog.darylsun.page%2F">Next Site</a>
</div>
</div>

</main>

<footer>
<fieldset id="theme-picker" class="theme-picker">
<legend>Theme</legend>
<ul class="u-list--no-marker" role="list">
<li><input id="auto-theme" name="theme" type="radio" value="auto" checked=""><label for="auto-theme" class="u-gap--right">Auto</label></li>
<li><input id="light-theme" name="theme" type="radio" value="light"><label for="light-theme" class="u-gap--right">Light</label></li>
<li><input id="dark-theme" name="theme" type="radio" value="dark"><label for="dark-theme" class="u-gap--right">Dark</label></li>
<li><small><svg aria-hidden="true" class="svg-inline--fa fa-arrow-up u-gap--right" focusable="false" data-prefix="fas" data-icon="arrow-up" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" data-fa-i2svg=""><path fill="currentColor" d="M214.6 41.4c-12.5-12.5-32.8-12.5-45.3 0l-160 160c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L160 141.2V448c0 17.7 14.3 32 32 32s32-14.3 32-32V141.2L329.4 246.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3l-160-160z"></path></svg><!-- <i aria-hidden="true" class="fa-solid fa-arrow-up u-gap--right"></i> Font Awesome fontawesome.com --><a href="#document-top">Back to top</a></small></li>
</ul>
</fieldset>
<p>Made with <a href="https://weblog.lol">weblog.lol</a>.</p>
</footer>

<!-- Discuss on Mastodon -->
<template id="mastodon-post-template">
{discuss-on-mastodon-template}
</template>
<script type="module" src="/mastodon-post.js" defer></script>

</body>

</html>