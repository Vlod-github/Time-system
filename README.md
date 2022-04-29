# Time system
A system that allows you to subscribe to time events.
## Reasons for use
- Reduce dependence on external APIs (Supposed to integrate with an external timer)
- Emulation and testing
```lua
Time.subscribe(myFunc) -- subscribe to a time event
Time.unsubscribe(myFunc) -- unsubscribe from a time event
-- Next for console
Time.start()
Time.stop()
Time.resume()
```
## Example
```lua
local Time = TimeSystem()
local myFunc = function(time)
	print(time)
end
Time.subscribe(myFunc)
Time.start()
[[ output
0.03125  
0.0625   
0.09375  
0.125    
0.15625  
0.1875   
0.21875  
...
]]
```