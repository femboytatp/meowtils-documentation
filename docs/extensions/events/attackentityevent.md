# **AttackEntityEvent**

---

This event fires each time you attempt to attack any entity.

## Parameter

`AttackEntityEvent`

## Methods

### Player

``` java
getPlayer()
```

Returns **EntityPlayer**.

### Target

``` java
getTarget()
```

Returns the target **Entity**.

## Example

``` java
@EventTarget
public void onAttackEntity(AttackEntityEvent event) {
    if (event.getTarget() == null) return;
    Meowtils.addMessage("Attacked: " + event.getTarget());
}
```