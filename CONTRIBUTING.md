This site is generated using the Zola static site generator.

## Checking and publishing biographies

Pick a biography in the `raw_files` directory.
Each file will have front matter in the following format: 

```toml
+++
title = "Lastname Firstname"
date = "YYYY-MM-DD"
authors = ["xxx"]
[taxonomies]
surname_initial = ["x"]
tags = ["xxx"]
sex = ["xxx"]
[extra]
birth = xxx
death = xxx
sources = ["xxx"]
aka = "xxx"
+++
```

### Data model

<dl>
<dt>title</dt>
<dd>The title of the biography. You will usually find this in the form Lastname Firstname, and you should switch this around to Firstname(s) Lastname. The only reason this hasn't been changed automatically is because of people with middle names.</dd>

<dt>date</dt>
<dd>The date the post was originally published; should already be present.</dd>

<dt>authors</dt>
<dd>You might find Michael Walker's name at the bottom of some of these, in which case you can add his name here. Otherwise, Graham Stevenson is assumed to be the default author so you can delete this field.</dd>

<dt>surname_initial</dt>
<dd>The first letter of the person's last name, used for categorisation.</dd>

<dt>tags</dt>
<dd>Any keywords associated with the person. These are optional and it's up to you what you put here.</dd>

<dt>sex</dt>
<dd>The sex of the person. Can be either man or woman.</dd>

<dt>birth</dt>
<dd>Year of birth, optional.</dd>

<dt>death</dt>
<dd>Year of death, optional.</dd>

<dt>sources</dt>
<dd>Any sources referenced in the article. These are not structured in any consistent way.</dd>

<dt>aka</dt>
<dd>Alternative names for the person, if they were known by a pseudonym or a common nickname.</dd>
</dl>

Read through the article and fill in any details in the front matter. 

## Style editing

You can use markdown for some text formatting, eg. lists and block quotes. Zola uses ??? version of markdown.

Some extra HTML markup is fine, for example casting quotes as `<q>` tags, or tagging abbreviations with `<abbr>`.

The raw files are converted markdown from a database export of a Wordpress site, which was itself migrated from an earlier website.

### Things to watch out for

#### Quotes surrounded by slashes

For example:

```
`/
```

Replace these with single quotes as appropriate.

#### Images

Images from the original site, for example:

```
![](http://79.170.40.183/grahamstevenson.me.uk/images/stories/barnsby%20george%20_socialism.jpg)
```

These links are no longer valid.
We do have many (most?) of the image files saved, but sorting these out is another project.
Remove the links and any associated captions.

### Other

You might prefer to add line breaks after sentences.
This is conventional, but not a hard style rule.

Graham occasionally put inline notes or references between square brackets.
We don't really have a common way to format these references.
Maybe we should use footnotes?

## Web design

One goal of this project is to keep the biographies online as long as possible, and failing that make sure they're in a good position to be archived in some offline format.

In order to achieve this we need to adhere to a few structural constraints. The content is essentially text-only. There are no images, no JavaScript, and no CSS pre-processing step. The build is as simple as possible, and there are no moving parts at the end of it.

The site design is still very basic and could be improved, within the constraints listed above. Good print layouts would be useful. Please open an issue if you have any mockups, proposals, or ideas to consider.
