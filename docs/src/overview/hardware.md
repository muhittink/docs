# Hardware Support

In order to keep the automation and maintenance overhead small, we strongly advise against building highly heterogeneous environments with metal-stack. Having a lot of different vendors and server models in your partitions will heavily increase the time and effort for introducing metal-stack in your infrastructure. From experience we can tell that the interfaces for automating hardware provisioning are usually inconsistent between vendors and even between server models of the same vendor. Therefore, we encourage adopters to start off with only a small amount of machine types. If you want to be on the safe side, you should consider buying the hardware that we officially support.

We came up with a repository called [go-hal](https://github.com/metal-stack/go-hal), which includes the interface required for metal-stack to support a machine vendor. If you plan to implement support for new vendors, please check out this repository and contribute back your efforts in order to make the community benefit from extended vendor support as well.

## Servers

At the moment we support the following server types:

| Vendor     | Series      | Model            |
| :--------- | :---------- | :--------------- |
| Supermicro | Big-Twin    | SYS-2029BT-HNR   |
| Supermicro | SuperServer | SSG-5019D8-TR12P |

## Switches

At the moment we support the following switch types:

| Vendor    | Series        | Model      |
| :-------- | :------------ | :--------- |
| Edge-Core | AS7700 Series | AS7712-32X |

!!! warning

    On our switches we run [Cumulus Linux](https://cumulusnetworks.com/products/cumulus-linux/). The metal-core writes network configuration specifically implemented for this operating system. Please also consider running Cumulus Linux on your switches if you do not want to run into any issues with networking.

    Of course, contributions for supporting other switch vendors and operating systems are highly appreciated.
