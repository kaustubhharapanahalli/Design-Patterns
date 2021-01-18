# Class Diagram to implement Strategy Pattern

```plantuml
@startuml
class ShippingCost {
    + shipping_cost()
    + __init__(Strategy)
}

interface AbsStrategy{
    + calculate()
}

class FedexStrategy{
    + calculate()
}

class PostalStrategy{
    + calculate()
}

class UPSStrategy{
    + calculate()
}

ShippingCost "Context" o--> "Strategy" AbsStrategy : 1
AbsStrategy <|.. PostalStrategy
AbsStrategy <|.. FedexStrategy
AbsStrategy <|.. UPSStrategy

@enduml
```
