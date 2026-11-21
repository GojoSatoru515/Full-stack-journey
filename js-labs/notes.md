# Week 4: Functions, scope, Math/Dates, closures

## Functions
- return gives a value back; console.log only shows it → returns undefined
- arrow with { } needs return; without { } it returns automatically
- default param applies ONLY for undefined ("" and 0 are real values)
- pure = same input → same output + no side effects

## Scope
- inside sees outside; outside never sees inside (→ ReferenceError)
- let/const inside = NEW variable (outer untouched)
- no keyword inside = CHANGES the outer variable
- const/let used before their line → TDZ error, and the whole script stops

## Math & Dates
- toFixed → STRING (display only); roundMoney = Math.round(x*100)/100 → number
- floor = always smaller (-3.2 → -4); ceil = always bigger (-3.2 → -3)
- Math.max(x, 500) = AT LEAST 500 · Math.min(x, 0.3) = AT MOST 0.3
- months are 0-based (10 = November); getDate = day of month, getDay = weekday
- setDate mutates → copy first with new Date(date)

## Functions as values
- fn = the function itself · fn() = its result
- callback = a function you GIVE to another function
- factory = (setting) => (input) => ...  (returns a new function)
- closure = a function that remembers variables from where it was created 🎒
- private state: let inside the factory, the inner function updates + returns it