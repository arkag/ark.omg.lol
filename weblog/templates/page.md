Type: Template
Title: Page Template

<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" type="text/css" href="https://csshake.surge.sh/csshake.min.css">
  <link rel="stylesheet" type="text/css" href="https://static.omg.lol/css/style.css">
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

    * {
      font-family: 'Source Sans 3', sans-serif;
    }

    /* Cute lil' Navbar */
    .navbar {
      width: 100%;
      margin-bottom: 1rem;
    }

    .navbar ul {
      display: flex;
      flex-wrap: wrap;
      list-style: none;
      margin: 0;
      padding: 0;
      gap: 0.5rem;
    }

    .navbar li {
      display: flex;
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
  </style>
</head>

<body>

  <div class="container">
    <header>
      <h1 class="weblog-title"><a href="{base-path}">{weblog-title}</a></h1>
      <div class="navbar">
        <ul>
          <li><a rel="me" href="https://alex.kagno.com/">Home</a></li>
          <li><a rel="me" href="https://alex.kagno.com/blog">Blog</a></li>
          <li><a rel="me" href="https://resume.alex.kagno.com">Resume</a></li>
        </ul>
      </div>
    </header>

    <main>

{body}

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

</body>

</html>