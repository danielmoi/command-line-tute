# `ifconfig`

## Name
Interface Configuration

----
## Usage

```
$ ifconfig [options] [interface] [options]
```


----
## Description
`ifconfig` is a utility used to assign an address to a network interface, and/or configure network interface parameters




---
## Examples
If no arguments are given, ifconfig displays the status of the currently active interfaces.
```
$ ifconfig

lo0: <interface configuration for lo0>
  ...
  ... <other interfaces>
  ...
```

----
If a single interface argument is given, it displays the status of the given interface only.
```
$ ifconfig en0

en0: <interface configuration for en0>
```


----
If a single -a argument is given, it displays the status of all interfaces, even those that are down.
```
$ ifconfig -a

lo0: <interface configuration for lo0>
  ...
  ... <ALL other interfaces>
  ...
```

---
We can get the IP address of our machine by doing this:
```
$ ifconfig | grep inet

inet <details>
inet6 <details>
inet6 <details>
inet6 <details>
inet 111.111.1.1 netmask 0xffffff00 broadcast 222.222.2.222
inet6 ... <details>
inet6 ... <details>
```
Where 111.111.1.1 is the IP address of our machine.

----
We can also be more specific, so only one line is printed to standard output:
```
$ ifconfig | rg 'inet .* broadcast'

inet 111.111.1.1 netmask 0xffffff00 broadcast 222.222.2.222
```


---
Used otherwise, it CONFIGURES an interface.
