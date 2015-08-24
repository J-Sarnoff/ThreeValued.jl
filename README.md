## ThreeValued.jl
####3-valued logic (False, Maybe, True)

```julia

julia> imp( xor(Maybe,True), True )
True

julia> (Maybe $ True) → True
True
```



-------------------------------------------------
|unary | does             | binary  | infix |
|------|---------------------|--------|-------|
|  not | negates             | and     | &     |
|  unk | True iff Maybe      | or      | \|   |
|  tru | push Maybe to True  | xor     | $     |
|  fal | push Maybe to False | imp     | \rightarrow |


--------------------------------------
|  eql | neq | ltn | lte | gtn | gte |
|-----|-----|------|-----|-----|------|
| == | != | < | <= | > | >= |


```julia
julia> logictable()

("unk","tru","fal","not","and","or","xor","imp",
 "ltn","lte","gte","gtn","eql","neq")


julia> logictable("imp")

    imp   | False  | Maybe  | True 
   -------|--------|--------|------
    False | True   | True   | True   
    Maybe | Maybe  | Maybe  | True   
    True  | False  | Maybe  | True  
    
```    
