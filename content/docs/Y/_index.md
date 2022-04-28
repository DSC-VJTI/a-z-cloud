---
title: "Y"
linkTitle: "Y"
weight: 4
description: >
  ## YAML
---

> The superset of JSON

YAML is a data-serialization language that is commonly used to define configuration files for Ansible, Kubernetes, GitHub Actions and many more DevOps tools. Originally intended to be called _Yet Another Markup Language_ to reference its purpose as a markup language like HTML, XML in the early 00's, YAML is now repurposed as _YAML Ain't Markup Language_ to indicate its data representation purpose.

### Why YAML?

We usually use JSON for defining configurations for web applications such as a `package.json` for Node.js applications. However, YAML is widely seen in use for defining configurations for larger applications. YAML supports several features that are absent in JSON such as it is more human-readable, supports comments, multiple data types, and multiline strings.

### An Example

The structure of a YAML file is a map or a list. Maps allow you to associate key-value pairs. Each key must be unique, and the order doesn't matter; you can relate to a Python dictionary.

A map in YAML needs to be resolved before it can be closed, and a new map is created. A new map can be created by either increasing the indentation level (usually 2 spaces) or by resolving the previous map and starting an adjacent map.

A list includes values listed in a specific order and may contain any number of items needed. A list sequence starts with a dash (-) and a space, while indentation separates it from the parent. You can think of a sequence as a Python list or an array in Bash. A list can be embedded into a map.

```yaml
# an example YAML
author: "Pankaj Khushalani"
day: Y # strings work without quotes too
number: 25
number-as-hex: 0x19
is-about-yaml: true
sections-array:
  - "Why YAML"
  - "An Example"
  - "Learn More"
sections-array-another-way: ["Why YAML", "An Example", "Learn More"]
dictionary:
  dictionary-key: four
  dictionary-in-dictionary:
    nested-dictionary-key: 1
multiline-string: |
  I can write this string
  across multiple lines :)
```

The following is the corresponding JSON obtained from a [YAML to JSON convertor](https://onlineyamltools.com/convert-yaml-to-json):

```javascript
{
  "author": "Pankaj Khushalani",
  "day": "Y",
  "number": 25,
  "number-as-hex": 25,
  "is-about-yaml": true,
  "sections-array": [
    "Why YAML",
    "An Example",
    "Learn More"
  ],
  "sections-array-another-way": [
    "Why YAML",
    "An Example",
    "Learn More"
  ],
  "dictionary": {
    "dictionary-key": "four",
    "dictionary-in-dictionary": {
      "nested-dictionary-key": 1
    }
  },
  "multiline-string": "I can write this string\nacross multiple lines :)\n"
}
```

As we can see, double quotes were added everywhere, comments were removed, and escape sequences were used for multiline strings. Because of its support for lists and maps in YAML, a JSON file is a valid YAML file.

### Learn More

- The official YAML [website](https://yaml.com/). Do have a peek at the [original YAML website](https://yaml.org/) that is entirely written in YAML!

- A [quick guide](https://learnxinyminutes.com/docs/yaml/) for YAML
