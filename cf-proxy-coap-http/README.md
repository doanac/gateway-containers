Eclipse Californium is a Java implementation of RFC7252 - Constrained Application Protocol for IoT Cloud services. Thus, the focus is on scalability and usability instead of resource-efficiency like for embedded devices. Yet Californium is also suitable for embedded JVMs.

More information can be found at http://www.eclipse.org/californium/ and http://coap.technology/.

NOTE: The cf-proxy .jar in this folder has been customized with patches to fix handling of multiple file processing

## Build your own version of cf-proxy

  * git clone https://github.com/eclipse/californium -b 2.0.x
  * cd californium
  * git am *.patch
  * mvn clean install
  * cp demo-apps/run/cf-proxy-*.jar [this folder]

## How to use this image

```
docker run -p 5682:5682/udp hub.foundries.io/cf-proxy-coap-http
```
