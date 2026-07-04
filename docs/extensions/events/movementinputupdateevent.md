# **MovementInputUpdateEvent**

---

This fires before movement input states are updated for your player.

**Cancellable =** `false`

## Parameter

`MovementInputUpdateEvent`

## Example

``` java
@EventTarget
public void onMovementInputUpdate(MovementInputUpdateEvent event) {
    Meowtils.addMessage("Updated movement states.");
}
```