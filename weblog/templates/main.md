<!DOCTYPE html>
<html lang="en">
<head>
  <title>{weblog-title}{separator}{post-title}</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  {feeds}
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Source+Sans+3:ital,wght@0,300;0,400;0,600;0,700;1,400&display=swap');
    @import url('https://static.omg.lol/type/font-honey.css');
    @import url('https://static.omg.lol/type/font-mint-grotesk-regular.css');
    @import url('https://static.omg.lol/type/font-md-io.css');
    @import url('https://static.omg.lol/type/fontawesome-free/css/all.css');
    @import url('https://static.omg.lol/css/style.css');

    :root {
      --foreground: #4c4f69;
      /* Catppuccin Latte: Text */
      --background: #eff1f5;
      /* Catppuccin Latte: Base */
      --container-bg: #dce0e8;
      /* Catppuccin Latte: Mantle (darker than base) */
      --link: #1e66f5;
      /* Catppuccin Latte: Blue */
      --accent: #9ca0b0;
      /* Catppuccin Latte: Overlay1 */
    }

    @media (prefers-color-scheme: dark) {
      :root {
        --foreground: #cdd6f4;
        /* Catppuccin Mocha: Text */
        --background: #1e1e2e;
        /* Catppuccin Mocha: Base */
        --container-bg: #181825;
        /* Catppuccin Mocha: Mantle (darker than base) */
        --link: #89b4fa;
        /* Catppuccin Mocha: Blue */
        --accent: #7f849c;
        /* Catppuccin Mocha: Overlay1 */
      }
    }

    * {
      font-family: 'Source Sans 3', sans-serif;
    }

    body {
      font-size: 120%;
      color: var(--foreground);
      background: var(--background);
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    /* Cute lil' Navbar */
    .navbar {
      width: 100%;
      margin-bottom: 1rem;
    }

    .navbar ul {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      list-style: none;
      margin: 0;
      padding: 0;
      gap: 0.5rem;
    }

    .navbar li {
      display: flex;
      align-items: center;
    }

    .navbar a {
      text-decoration: none;
      padding: 0.5rem 1rem;
      border-radius: 4px;
      transition: background-color 0.2s ease;
    }

    .navbar a:hover {
      background-color: rgba(0, 0, 0, 0.1);
    }

    @media (max-width: 600px) {
      .navbar ul {
        flex-direction: column;
        gap: 0.25rem;
      }
    }
  </style>
</head>

<body>

  <div class="container">
    <header>
      <h1 class="weblog-title"><a href="{base-path}">{weblog-title}</a></h1>
      <div class="navbar">
        <ul>
          <li><a rel="me" href="https://alex.kagno.com/">Home</a></li>
          <li> | </li>
          <li><a rel="me" href="https://alex.kagno.com/blog">Blog</a></li>
          <li> | </li>
          <li><a rel="me" href="https://resume.alex.kagno.com">Resume</a></li>
        </ul>
      </div>
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
  <p>Made with <a href="https://weblog.lol">weblog.lol</a>.</p>
</footer>
</div>

<!-- Discuss on Mastodon -->
<template id="mastodon-post-template">
{discuss-on-mastodon-template}
</template>
<script type="module" src="/mastodon-post.js" defer></script>

</body>

</html>