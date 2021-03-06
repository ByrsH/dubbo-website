# stickiness

Sticky connections are used for stateful services, as much as possible so that clients always make calls to the same provider, unless the provider hangs up and connects to the other one.

Sticky connections will automatically open [Delayed Connections](./lazy-connect.md) to reduce the number of long connections.

```xml
<dubbo:reference id="xxxService" interface="com.xxx.XxxService" sticky="true" />
```

Dubbo supports method-level sticky connection, and if you want more granular control, you can also configure as follow.

```xml
<dubbo:reference id="xxxService" interface="com.xxx.XxxService">
    <dubbo:mothod name="sayHello" sticky="true" />
</dubbo:reference>
```
