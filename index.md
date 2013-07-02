# Benie Hello, World
Genie is a place for you to publish open-source lessons. All of your lessons
will be in simple text files that are easy to maintain and fully owned by you.

## Getting Started
A simple lesson directory looks like the following:

- `index.md` - a text file containing your lesson in markdown format
- `manifest.yml` - a YAML file that describes your lesson

Refer to the [manifest][manifest] of this lesson for an example.

## GitHub Flavored Markdown
Most of the markup can be written in the usual [Markdown][markdown], with a few
GitHub extensions. More information can be obtained from the [GFM documentation][gfm],
but here is a quick preview.

 code                 | output
----------------------|------------------
 `~~strikethrough~~`  | ~~strikethrough~~
`no_intra_emphasis`   | no_intra_emphasis
`http://auto.link`    | http://auto.link/

## Foundation
This template is built using [foundation][foundation], so all of the Foundation
components will still work, if writing HTML if your kind of thing.

## Code
Code is highlighted using Pygments, and it looks like

```ruby
  puts "hello world!"
```

# Problems
Problems may be described using embedded YAML. We currently support three
question types: MCQs, Short Answers, and Tables. Embedded YAML blocks must be
enclosed by three consecutive quotation " marks.

For example, the source for the following question is:

```yaml
format: multi
question: How _tall_ is Mount Everest?
answer: B
options:
  A: 66 inches
  B: 8.85 kilometers
  C: 123400 feet
```

"""
format: multi
question: How _tall_ is Mount Everest?
answer: B
options:
  A: 66 inches
  B: 8.85 kilometers
  C: 123400 feet
"""

"""
format: short
question: What _is_ the most commonly used word in English?
answer: the
"""

"""
format: table
question: Fill in the missing values in the following table.
headings: [A, B, C]
grid:
  - [0, '?',  2]
  - ['?', 4,  5]
answer:
  - [0, 1, 0]
  - [3, 0, 0]
"""

  [manifest]: https://github.com/jimjh/genie-syntax-lesson/blob/master/manifest.yml
  [foundation]: http://foundation.zurb.com/docs/
  [markdown]: http://daringfireball.net/projects/markdown/
  [gfm]: http://github.github.com/github-flavored-markdown/
