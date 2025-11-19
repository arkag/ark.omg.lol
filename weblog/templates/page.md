Type: Template
Title: Page Template

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
      box-sizing: border-box;
    }

    body {
      font-family: 'Source Sans 3', sans-serif;
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

      .navbar li:nth-child(even) {
        display: none;
        /* Hide separators on mobile */
      }
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
      line-height: 170%;
    }

    .container {
      max-width: 60em;
      width: 100%;
      margin: 2em auto;
      padding: 4em 2em 2em;
      box-sizing: border-box;
      background: var(--container-bg);
      border-radius: 1em;
    }

    header,
    main,
    footer {
      max-width: 100%;
      width: 100%;
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    header {
      margin-bottom: 2em;
    }

    main {
      flex: 1;
    }

    footer {
      margin-top: 2em;
    }

    footer p {
      font-size: 90%;
      margin: 0;
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
      text-align: center;
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

    .weblog-title {
      text-align: center;
      font-family: 'Source Sans 3', sans-serif;
      font-weight: 700;
      font-size: 2em;
      margin-top: 0;
      margin-bottom: 0.25em;
    }

    .weblog-title a {
      text-decoration: none;
      color: var(--foreground);
    }

    .navbar a {
      color: var(--foreground);
    }

    main ul {
      list-style: none;
      padding: 0;
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
          <li><a rel="me" href="https://alex.kagno.com/resume">Resume</a></li>
        </ul>
      </div>
    </header>

    <main>

{body}

<hr>

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

</body>
</html>