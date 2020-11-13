# Spdif
## S/PDIF = Sony/Philips Digital Interface

S/PDIF (Sony/Philips Digital Interface)[1][2] is a type of digital audio interconnect used in consumer audio equipment to output audio over reasonably short distances. The signal is transmitted over either a coaxial cable with RCA connectors or a fiber optic cable with TOSLINK connectors. S/PDIF interconnects components in home theaters and other digital high-fidelity systems.

### Looks like
<figure>
  <img src ="../image/spdif.jpg" />
</figure>

### On Android
- Starting with API level 16 (Jellybean) there's the MediaRouter API which allows you to get some information about the current audio/video routing.
To get routing info you'd use the getSelectedRoute method, with the ROUTE_TYPE_LIVE_AUDIO or ROUTE_TYPE_LIVE_VIDEO flag. This gives you a RouteInfo object, through which you can get the name of the route using the getName method.

```java
MediaRouter mr = (MediaRouter)getSystemService(Context.MEDIA_ROUTER_SERVICE);
RouteInfo ri = mr.getSelectedRoute(MediaRouter.ROUTE_TYPE_LIVE_AUDIO);
if ("HDMI".equals(ri.getName().toString()) {
    // do something...
}
```
