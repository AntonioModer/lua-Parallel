lua-Parallel
============

##Status

I can change anything.

##Usage

```Lua
local T = string.dump

Parallel.For(1, 100, T(function(thread_no)
  TASK(function(i) print(thread_no .. " :" .. i) end)
end))

Parallel.For(1, 100, T(function(thread_no)
  TASK(function(i) return thread_no, math.pow(i, 2), math.sqrt(i) end)
end), print)
```

[Parallel hash calculation](/examples/hash.lua)

[Parallel ping hosts in network](/examples/pingnet.lua)
