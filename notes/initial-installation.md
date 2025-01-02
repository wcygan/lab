# Initial Installation

I had *plenty* of trouble following the instructions until I figured out that my router / gateway (`bootstrap_node_default_gateway`) was running on `192.168.1.254` and *not* `192.168.1.1`:

```yaml
# (OPTIONAL) The default gateway for the nodes
#   Leave blank if your default gateway is the same as the first IP in the network (.1)
bootstrap_node_default_gateway: "192.168.1.254"
```

Basically, this said OPTIONAL and I didn't know any better, so I skipped that!

Essentially, this caused issues so:

1. No node could reach the other nodes
2. No node could reach the internet

It was terrible! Luckily, it boiled down to a stupid mistake :)
