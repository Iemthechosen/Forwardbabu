The application `tgcf` is configured using a simple `YAML` file. If you are new to the `YAML` syntax, don't worry, it's easy, and you will learn it.

## Introducing YAML

Tutorials on YAML syntax:
- [Article by Tutorial Point](https://www.tutorialspoint.com/yaml/yaml_basics.htm) 
- [Article by W3 Schools](https://www.w3schools.io/file/yaml-cheatsheet-syntax) 
- [YouTube video by Nana](https://youtu.be/1uFVr15xDGg?t=73)


## Example Configuration

Below is an example configuration. Don't copy-paste this. Understand what each part does.

```yaml
forwards:
  - source: -1001412118156
    dest: [-1001461332656,-1001457230530]


show_forwarded_from: false

plugins:
  filter:
    text:
      blacklist: ["nope"]
  replace:
    text:
      god: devil
      tokyo: delhi
      
```

## Schema

Here is the complete schema for the configuration file.

- `forwards` (a list of forward objects)
- forward ( contains a `source` (integer), a `dest` (list of integers) and an `offset`(optional integer) )
- `show_forwarded_from` (boolean: true/false)
- `plugins` contain the name of the plugin and the data to be passed to that plugin.
   - What data to pass to plugins? is defined in the documentation for that plugin. Here is the [list of all plugins](https://github.com/aahnik/tgcf/wiki/Plugins).

