[![Nightly CI status master][master-ci-badge]][master-ci-link]
[![IRC][irc-badge]][irc-link]

                          ZZZZZZ
                        ZZZZZZZZZZZZ
                      ZZZZZZZZZZZZZZZZ
                     ZZZZZZZ     ZZZZZZ
                    ZZZZZZ        ZZZZZ
                    ZZZZZ          ZZZZ
                    ZZZZ           ZZZZZ
                    ZZZZ           ZZZZ
                    ZZZZ          ZZZZZ
                    ZZZZ        ZZZZZZ
                    ZZZZ     ZZZZZZZZ       777        7777       7777777777
              ZZ    ZZZZ   ZZZZZZZZ         777      77777777    77777777777
          ZZZZZZZ   ZZZZ  ZZZZZZZ           777     7777  7777       777
        ZZZZZZZZZ   ZZZZ    Z               777     777    777       777
       ZZZZZZ       ZZZZ                    777     777    777       777
      ZZZZZ         ZZZZ                    777     777    777       777
     ZZZZZ          ZZZZZ    ZZZZ           777     777    777       777
     ZZZZ           ZZZZZ    ZZZZZ          777     777    777       777
     ZZZZ           ZZZZZ     ZZZZZ         777     777    777       777
     ZZZZ           ZZZZ       ZZZZZ        777     777    777       777
     ZZZZZ         ZZZZZ        ZZZZZ       777     777    777       777
      ZZZZZZ     ZZZZZZ          ZZZZZ      777     7777777777       777
       ZZZZZZZZZZZZZZZ            ZZZZ      777      77777777        777
         ZZZZZZZZZZZ               Z
            ZZZZZ

The friendly Operating System for IoT!

RIOT is a real-time multi-threading operating system that supports a range of
devices that are typically found in the Internet of Things (IoT):
8-bit, 16-bit and 32-bit microcontrollers.

RIOT is based on the following design principles: energy-efficiency, real-time
capabilities, small memory footprint, modularity, and uniform API access,
independent of the underlying hardware (this API offers partial POSIX
compliance).

RIOT is developed by an international open source community which is
independent of specific vendors (e.g. similarly to the Linux community).
RIOT is licensed with LGPLv2.1, a copyleft license which fosters
indirect business models around the free open-source software platform
provided by RIOT, e.g. it is possible to link closed-source code with the
LGPL code.

## FEATURES

RIOT is based on a microkernel architecture, and provides features including,
but not limited to:

* a preemptive, tickless scheduler with priorities
* flexible memory management
* high resolution, long-term timers
* support 100+ boards based on AVR, MSP430, ESP8266, ESP32, MIPS, RISC-V,
  ARM7 and ARM Cortex-M
* the native port allows to run RIOT as-is on Linux, BSD, and MacOS. Multiple
  instances of RIOT running on a single machine can also be interconnected via
  a simple virtual Ethernet bridge
* IPv6
* 6LoWPAN (RFC4944, RFC6282, and RFC6775)
* UDP
* RPL (storing mode, P2P mode)
* CoAP
* CCN-Lite
* Sigfox
* LoRaWAN


## GETTING STARTED
* You want to start the RIOT? Just follow our
[quickstart guide](http://u.720life.cn/g/07cee005d2b43d0f92c3fa236b8c7af13527c6a2c8f06d285eef329515b107389aa679c7b0a96eabc1c40f3cf248bda6d89fb20a3b12a8e12fa999e99e7db5b1)  or
try this
[tutorial](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e98842c4beb27f233819de84405041c6a60eaa8a54d56075893c78a71304d1a90bd64a04f22b569fa206d80369ed2a14 
For specific toolchain installation, follow instructions in the
[getting started](http://u.720life.cn/g/07cee005d2b43d0f92c3fa236b8c7af10f501335a93eda4d115cd59193560f157e4f453355560c7e17415b5e3c6d8e90)  page.
* The RIOT API itself can be built from the code using doxygen. The latest
  version of the documentation is uploaded daily to
  [riot-os.org/api](http://u.720life.cn/g/15a670b61c403fe787cfe7f133e71fde94e77762a9cb96f16bd8c90fddb7d9a2 

### USING THE NATIVE PORT WITH NETWORKING
If you compile RIOT for the native cpu and include the `netdev_tap` module,
you can specify a network interface like this: `PORT=tap0 make term`

#### SETTING UP A TAP NETWORK
There is a shell script in `RIOT/dist/tools/tapsetup` called `tapsetup` which
you can use to create a network of tap interfaces.

*USAGE*

To create a bridge and two (or `count` at your option) tap interfaces:

    ./dist/tools/tapsetup/tapsetup [-c [ ]]

## CONTRIBUTE

To contribute something to RIOT, please refer to our
[contributing document](CONTRIBUTING.md).

## MAILING LISTS
* RIOT OS kernel developers list
 * devel@riot-os.org (http://u.720life.cn/g/e341fb79b7758bb4d22b17c382c3c56f57300db0f652ca8ede73b329e18739c3ecabd7c1b71f24ac584cef98b2cd5d85) 
* RIOT OS users list
 * users@riot-os.org (http://u.720life.cn/g/e341fb79b7758bb4d22b17c382c3c56f57300db0f652ca8ede73b329e18739c35921d2b03c91b4eb1799c870b7b05925) 
* RIOT commits
 * commits@riot-os.org (http://u.720life.cn/g/e341fb79b7758bb4d22b17c382c3c56f57300db0f652ca8ede73b329e18739c3ae62ffa7b565654721a1ac0a10d76f87fbc54b71ff43deae1c8a0f3f7a6bd6d9) 
* Github notifications
 * notifications@riot-os.org
   (http://u.720life.cn/g/e341fb79b7758bb4d22b17c382c3c56f57300db0f652ca8ede73b329e18739c35f2d1a994282fd91f6c6aa24c35fffb81cdb49406f418de65b177171df74c368) 

## LICENSE
* Most of the code developed by the RIOT community is licensed under the GNU
  Lesser General Public License (LGPL) version 2.1 as published by the Free
  Software Foundation.
* Some external sources, especially files developed by SICS are published under
  a separate license.

All code files contain licensing information.

For more information, see the RIOT website:

https://www.riot-os.org


[master-ci-badge]: https://ci.riot-os.org/RIOT-OS/RIOT/master/latest/badge.svg
[master-ci-link]: https://ci.riot-os.org/nightlies.html#master
[irc-badge]: https://img.shields.io/badge/IRC-join%20chat%20%E2%86%92-blue.svg
[irc-link]: https://webchat.freenode.net?channels=%23riot-os



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)