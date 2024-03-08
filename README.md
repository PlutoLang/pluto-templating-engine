# pluto-templating-engine

A templating engine for Pluto.

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

The templating syntax is the same as Twig's, but the functionality is more akin to PHP — giving you access to all of Pluto. So, any text processed by this is effectively Pluto source code just with a different packaging and different output semantics.
