# pluto-templating-engine

A Twig-like templating engine for Pluto.

```lua
local TE = require "templating-engine"

local data = [[{% if user then %}
Hello, {{ user.name }}!
{% else %}
You're not logged in.
{% end %}]]

io.write(TE.render(data)) --> You're not logged in.

user = { name = "TheLegend27" }

io.write(TE.render(data)) --> Hello, TheLegend27!
```
