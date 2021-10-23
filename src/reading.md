---
layout: pages.njk
title: 2021 Books
---
Books I read in 2021. See [here for 2019]({{ '/posts/2019-books' | url }}), [here for 2020]({{ '/posts/2020-books' | url }}).

<h3 id="book-shelf">2021 Shelf</h2>

<div class="book-shelf-container">
  {%- for book in current_books -%}
  <div class="book">
    <a href="{{ book.GoodreadsURL }}">
      <img src="{{ book.CoverURL }}">
    </a>
  </div>
  {%- endfor -%}
</div>

<h3 id="book-shelf">2021 List</h2>

<div class="book-list-container">
  <table>
    <thead>
      <tr>
        <th>No.</th><th>Title</th><th>Author</th><th>Read</th><th>Category</th><th>Pages</th>
      </tr>
    </thead>
    <tbody>
      {%- for book in current_books -%}
      <tr>
        <td class="table-row-number"></td><td><a href="{{ book.GoodreadsURL }}">{{ book.Title }}</a></td><td>{{ book.Author }}</td><td>{{ book.Read }}</td><td>{{ book.Category }} <span class="meta-text">{{ book.SubCategory }}</span></td><td class="center">{{ book.Pages }}</td>
      </tr>
      {%- endfor -%}
    </tbody>
  </table>
</div>