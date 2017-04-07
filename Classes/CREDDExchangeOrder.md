CREDDExchangeOrder
==================

### Prefix: crd

### Description

Individual orders on the CREDD Exchange.

Table of Content
---------------- 

<!-- toc -->

------------------------------------------------------------------------

`Function`

is(oVariable)
-------------

### Description

Checks if the variable that was passed in is a CREDDExchangeOrder.

### Params

-   **oVariable** **(Variable)** - The variable that this function will
    check.

### Return Value

-   **Boolean** - Whether the variable that was passed in is a
    CREDDExchangeOrder or not.

------------------------------------------------------------------------

`Function`

newBuyOrder()
-------------

### Description

Creates a new CREDDExchangeOrder that is a buy order.

### Return Value

-   **[CREDDExchangeOrder](../Classes/CREDDExchangeOrder.html)** - A new
    CREDD Exchange buy order.

### Usage/Example

```lua
    This is largely unused since CREDDExchangeOrders are created using the ActionConfirmButton.
```

------------------------------------------------------------------------

`Function`

newSellOrder()
--------------

### Description

Creates a new CREDDExchangeOrder that is a sell order.

### Return Value

-   **[CREDDExchangeOrder](../Classes/CREDDExchangeOrder.html)** - A new
    sell order for the CREDD Exchange.

### Usage/Example

```lua
    This is largely unused since CREDDExchangeOrders are created using the ActionConfirmButton.
```

------------------------------------------------------------------------

`Method`

\_\_eq(crdCompare) (Deprecated)
-------------------------------

### Description

Determines if another CREDDExchangeOrder is the same as this one.

### Params

-   **crdCompare**
    **([CREDDExchangeOrder](../Classes/CREDDExchangeOrder.html))** - The
    CREDDExchangeOrder that is being compared to the one calling this
    function.

### Return Value

-   **Boolean** - Whether the two CREDDExchangeOrders are the same order
    or not.

------------------------------------------------------------------------

`Method`

\_\_gc() (Deprecated)
---------------------

### Description

Forces the garbage collector to be called on the CREDDExchangeOrder that
called the function.

------------------------------------------------------------------------

`Method`

Cancel()
--------

### Description

Removes the order from the CREDD Exchange.

------------------------------------------------------------------------

`Method`

CanPost()
---------

### Description

Validates that the order is set for a valid number ( &gt; 0 ) of credits
and is not currently posted on the CREDD Exchange.

### Return Value

-   **Boolean** - Whether the order can be posted on the CREDD Exchange
    or not.

------------------------------------------------------------------------

`Method`

GetExpirationTime()
-------------------

### Description

Gets the amount of time that the order will remain on the CREDD
Exchange.

### Return Value

-   **[Time](../Classes/Time.html)** - A Time object that states when the
    order will expire.

### Usage/Example

```lua
    The full date/time can be converted to a string using the Time object's _tostring function:

    local crdNewOrder = CCExchangeOrder.newBuyOrder()
    local monPrice = Money.new()
    monPrice:SetAmount(1)

    crdNewOrder:SetPrice(monPrice)
    crdNewOrder:Post()

    local timeExpiration = crdNewOrder:GetExpirationTime()
    Print(timeExpiration:_tostring())
```

------------------------------------------------------------------------

`Method`

GetListTime()
-------------

### Description

Gets the time that the order was posted.

### Return Value

-   **[Time](../Classes/Time.html)** - A time object for when the order
    was posted.

### Usage/Example

```lua
    The full date/time can be converted to a string using the Time object's _tostring function:

    local crdNewOrder = CCExchangeOrder.newBuyOrder()
    local monPrice = Money.new()
    monPrice:SetAmount(1)

    crdNewOrder:SetPrice(monPrice)
    crdNewOrder:Post()

    local timeExpiration = crdNewOrder:GetListTime()
    Print(timeExpiration:_tostring())
```

------------------------------------------------------------------------

`Method`

GetPrice()
----------

### Description

Gets the price that the order was set for.

### Return Value

-   **[Money](../Classes/Money.html)** - The amount and type of money
    that the order is requesting or offering for a CREDD.

------------------------------------------------------------------------

`Method`

IsBuy()
-------

### Description

Determines if the order is a buy order.

### Return Value

-   **Boolean** - Whether the order is a buy order or not.

------------------------------------------------------------------------

`Method`

IsPosted()
----------

### Description

Checks if the order is posted on the CREDD Exchange.

### Return Value

-   **Boolean** - Whether the order is posted on the CREDD Exchange or
    not.

------------------------------------------------------------------------

`Method`

Post()
------

### Description

Posts the order on the CREDD Exchange.

------------------------------------------------------------------------

`Method`

SetPrice(monPrice)
------------------

### Description

Sets the price that the order asks for once it is posted on the CREDD
Exchange.

### Params

-   **monPrice** **([Money](../Classes/Money.html))** - The amount of
    money that the order will pay for / accept for CREDD.

### Return Value

-   **Boolean** - Whether the price was set successfully or not.

### Usage/Example

    Note that the Money has to be in credits and the amount has to be greater than 0.