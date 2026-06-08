# **SendPacketEvent**

---

This fires each time your client sends a packet to the server.

## Parameter

`SendPacketEvent`

## Methods

### Packet

``` java
getPacket()
```

Returns current **Packet**.

## Example

``` java
/*
Cancels item release packets, also known as NoItemRelease.
*/
@EventTarget
public void onSendPacket(SendPacketEvent event) {
    if (event.getPacket() instanceof C07PacketPlayerDigging) {
        final C07PacketPlayerDigging packet = (C07PacketPlayerDigging) event.getPacket();

        if (packet.getStatus() == C07PacketPlayerDigging.Action.RELEASE_USE_ITEM) {
            event.setCancelled(true);
        }
    }
}
```