<!DOCTYPE html>
<html lang="en">
<head>
  <title>{weblog-title}{separator}{post-title}</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  {feeds}
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
<p>Made with <a href="https://weblog.lol">weblog.lol</a>.</p>
</footer>

<!-- Discuss on Mastodon -->
<!-- <template id="mastodon-post-template">
{discuss-on-mastodon-template}
</template>
<script type="module" src="/mastodon-post.js" defer></script> -->

</body>

</html>