## Running Local Dev

```
hugo --watch server --buildFuture --buildDrafts
```

## generate new blog post

## shortcode info


### table of content
```

{{</* toc */>}}
```

### pdf reader

```
In your Hugo website place the following shortcode in any of the markdown pages.
```
{{< embed-pdf url="./path/to/pdf/file/example.pdf" >}}

```

To hide pagination
```
{{< embed-pdf url="./path/to/pdf/file/example.pdf" hidePaginator="true" >}}
```


To render a selected page number
```
{{< embed-pdf url="./path/to/pdf/file/example.pdf" renderPageNum="5" >}}
```

To hide loading spinner
```
{{< embed-pdf url="./path/to/pdf/file/example.pdf" hideLoader="true" >}}
```

```
