// Weblog Configuration

;; About your weblog
;; -----------------

Weblog title: A Piece of the Void
Weblog description: Thoughts, rants, etc. from yours truly.
Author: Alex Kagno
Canonical domain: alex.kagno.com
Landing page: /
Landing page template: Landing Page Template


;; General config stuff
;; --------------------

Separator:  · 
Navigation: [Home](https://alex.kagno.com), [Blog](https://alex.kagno.com/blog), [Resume](https://resume.alex.kagno.com)
Files path: /files/
Landing page post count: 1
// Landing page post length: 45 words
Post template: Post Template

;; Pagination
;; ----------

Pagination path: /page/
Previous page template: <span class="previous-page"><a href="$previous_page">← Previous Page</a></span>
Next page template: <span class="next-page"><a href="$next_page">Next Page →</a></span>


;; Time stuff
;; ----------

; You can use a timezone value from the "TZ database name" column on this 
; web page: https://en.wikipedia.org/wiki/List_of_tz_database_time_zones

Timezone: MST
Date format: F j, Y g:i A


;; Feeds
;; -----

Feed post count: 25
// Feed post appendix: <p><em>Published with weblog.lol!</em></p>


;; Posts
;; -----

Post path format: /\b\l\o\g/
Default post: <<[---
Title: Your new post
Summary: A short description of your post for those on other platforms
Tags: blogging, another-tag, a-third-tag
Date: $date
---

]>>

Titleless title length: 15 words
// Truncation appendix:  […]
// Title format: <h1><a href="$permalink">$title</a></h1>

Multiple posts count: 10
Multiple posts format: <<[
[post:begin]
<article>
  {body}
  <aside class="post-info">
    <i class="fa-solid fa-clock"></i> {date}
  </aside>
  <aside class="post-tags">
    {tags}
  </aside>
</article>
[post:end]
]>>

;; Recent posts {recent-posts}
;; ---------------------------

Recent posts count: 5
Recent posts format: <<[
<ul>
[post:begin]<li><a href="$location">$title</a></li>[post:end]
</ul>]>>


;; Post list {post-list}
;; ---------------------

Post list format: <<[
<ul>
[post:begin]<li><a href="$location">$title</a></li>[post:end]
</ul>]>>


;; Page list {page-list}
;; ---------------------

Page list format: <<[
<ul>
[page:begin]<li><a href="$location">$title</a></li>[page:end]
</ul>]>>


;; Search
;; ------

Search status: enabled
Search template: Page Template
Search results success message: There [is|are] $count [result|results] for your search:
Search results failure message: There were no results found for your search.
Search results format: <<[
<h2>Results for “$search”</h2>
<p>$search_results_message</p>
[post:begin]<h3><a href="$location">$title</a></h3>
<p>$date</p>
<p>$snippet</p>[post:end]
]>>


;; Tags {tags}
;; -----------

Tag path: /tag/
// Tag page template: Tag Template
Tags format: <<[
[tag:begin]<a class="tag" href="$tag_location">$tag</a>[tag:end]
]>>
Tag page format: <<[
<h2>Posts tagged with “$tag”</h2>
<ul>
[tag:begin]<li><a href="$location">$title</a></li>[tag:end]
</ul>
]>>

Tag listing path: /tags
// Tag listing template: Tag Listing Template
// Note: tag listing order can be "alphabetical", "ascending", or "descending" where alphabetical sorts by the tag name and ascending/descending sorts by the count of entries with that tag
Tag listing order: alphabetical
Tag listing format: <<[
<h2>Tags</h2>
<ul>
[tag:begin]<li><a href="$location">$tag</a> ($count)</li>[tag:end]
</ul>
]>>

;; Custom config
;; -------------

Custom lol theme: <meta name="theme-color" media="(prefers-color-scheme: light)" content="#472A49"> <meta name="theme-color" media="(prefers-color-scheme: dark)" content="#C1C1F7"> <meta name="color-scheme" content="light dark">

Preload nebula sans: <link rel="preload" href="https://cdn.kagno.com/fonts/NebulaSans-Bold.ttf" as="font" type="font/ttf" fetchpriority="high" crossorigin><link rel="preload" href="https://cdn.kagno.com/fonts/NebulaSans-Regular.ttf" as="font" type="font/ttf" fetchpriority="high" crossorigin><link rel="preload" href="https://cdn.kagno.com/fonts/NebulaSans-Light.ttf" as="font" type="font/ttf" crossorigin>

Use nebula sans: <style>font-family: NebulaSans;</style>

Custom lol theme picker: <script>(function(){const Theme={AUTO:'auto',LIGHT:'light',DARK:'dark'};const THEME_STORAGE_KEY='theme';const THEME_OWNER=document.documentElement;const cachedTheme=localStorage.getItem(THEME_STORAGE_KEY);if(cachedTheme){THEME_OWNER.dataset[THEME_STORAGE_KEY]=cachedTheme}document.addEventListener('DOMContentLoaded',()=>{const themePicker=document.getElementById('theme-picker');if(!themePicker){return}themePicker.addEventListener('change',(e)=>{const theme=e.target.value;if(theme===Theme.AUTO){delete THEME_OWNER.dataset[THEME_STORAGE_KEY];localStorage.removeItem(THEME_STORAGE_KEY)}else{THEME_OWNER.dataset[THEME_STORAGE_KEY]=theme;localStorage.setItem(THEME_STORAGE_KEY,theme)}});const initialTheme=cachedTheme??Theme.AUTO;themePicker.querySelector('input[checked]').removeAttribute('checked');themePicker.querySelector(`input[value="${ initialTheme }"]`).setAttribute('checked','')})})();</script>

Discuss on mastodon: <mastodon-post><h3 class="u-spacing--top"><i class="fa-brands fa-mastodon"></i><a href="$postURL" rel="me">Discuss on Mastodon</a></h3></mastodon-post>


; Custom template (advanced) variables
;; -----------------------------------

Discuss on mastodon template: <figure class="mastodon-post"><blockquote class="mastodon-post__quote" data-key="content"></blockquote><figcaption class="mastodon-post__caption"><cite> — <a data-key="url" rel="me"><span data-key="username"></span>@<span data-key="hostname"></span></a></cite><dl class="mastodon-post__stats"><div class="mastodon-post__stat"><dt><i class="fa-solid fa-retweet u-color--purple u-gap--right"></i>Reposts</dt><dd data-key="reblogs_count"></dd></div><div class="mastodon-post__stat"><dt><i class="fa-solid fa-comment u-color--purple u-gap--right"></i>Replies</dt><dd data-key="replies_count"></dd></div><div class="mastodon-post__stat"><dt><i class="fa-solid fa-star u-color--purple u-gap--right"></i>Favorites</dt><dd data-key="favourites_count"></dd></div></dl></figcaption></figure>