# header

```html
<section class="hero is-primary">
  <div class="hero-body">
    <div class="container">
      <h1 class="title">
        <a href="/">Marvelex</a>
      </h1>
      <h2 class="subtitle">
        The Marvel Codex
      </h2>
    </div>
  </div>
</section>
```

# list

```html
<section class="section">
  <div class="container">
    <!-- data -->
  </div>
</section>
```

# item

```html
<div class="box">
  <a href="">
    <article class="media">
      <div class="media-left">
        <figure class="image">
          <img src="" style="max-width: 72px;">
        </figure>
      </div>
      <div class="media-content">
        <div class="content">
          <p>
            <!-- data -->
          </p>
        </div>
      </div>
    </article>
  </a>
</div>
```

# search

```html
<section class="section">
  <div class="container">
    <form class="search-form">
      <p class="control has-icon">
        <input class="input search" type="text" placeholder="Search for a comic" />
        <i class="fa fa-search"></i>
      </p>
    </form>
  </div>
</section>
```

# comic detail

```html
<article class="media">
  <div class="media-left">
    <figure class="image">
      <img src="${src}" style="max-width: 150px;">
    </figure>
  </div>
  <div class="media-content">
    <div class="content">
      <h1>${comic.title}</h1>
      <p>
        ${comic.description}
      </p>
      <hr>
      <h2>Creators</h2>
      <table class="table">
        <thead>
          <tr>
            <th>Name</th>
            <th>Role</th>
          </tr>
        </thead>
        <tbody>
          ${comic.creators.items.map((item) => authorRow(item))}
        </tbody>
      </table>
    </div>
  </div>
</article>
```

```html
<tr>
  <td>${author.name}</td>
  <td>${author.role}</td>
</tr>
```

# error

```html
<article class="message is-danger">
  <div class="message-body">
    <i class="fa fa-meh-o"></i> Sorry... ${msg}
  </div>
</article>
```

# empty

```html
<article class="message is-info">
  <div class="message-body">
    <i class="fa fa-frown-o"></i> Could not find anything matching your search terms
  </div>
</article>
```