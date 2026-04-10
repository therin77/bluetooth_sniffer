# bluetooth_sniffer

Notes 04/10/26:

https://www.bluetooth.com/wp-content/uploads/Files/Specification/HTML/Core-54/out/en/low-energy-controller/physical-layer-specification.html
 -The LE system uses 40 RF channels with center frequencies at a 2 MHz spacing from 2402 MHz to 2480 MHz.
 -radiative transmit power level at the maximum power setting shall be between 0.01 mW (-20 dBm) and 100 mW (+20 dBm)
 -The modulation is Gaussian Frequency Shift Keying (GFSK) with a bandwidth-bit period product BT=0.5. The modulation index shall be between 0.45 and 0.55. A binary one shall be represented by a positive frequency deviation, and a binary zero shall be represented by a negative frequency deviation.

https://www.bluetooth.com/wp-content/uploads/Files/Specification/HTML/Core-54/out/en/low-energy-controller/link-layer-specification.html
- public and random device addresses
- 40 total RF channels:
  - 3 RF advertisting channels, 37 general channels
- each transmission on a physical channel starts with an Access Address that is used as a correlation code by devices tuned to the physical channel.
- advertising: 2402 MHz, 2426 MHz, 2480 MHz
- The mandatory fields are Preamble, Access Address, PDU, and CRC. The optional field is Constant Tone Extension.
    - The preamble is 1 octet when transmitting or receiving on the LE 1M PHY and 2 octets when transmitting or receiving on the LE 2M PHY. The Access Address is 4 octets. The PDU range is from 2 to 258 octets. The CRC is 3 octets.
    - The preamble is a fixed sequence of alternating 0 and 1 bits, see standard for actual sequences

https://chatgpt.com/share/69d937fd-c3a4-8326-9d38-9d20dc38df5c
- changes channel every "connection event"
- same during packet
- 

TODO:
- sdr good quals for probem
- antenna good quals for problem
- python GFSK demod example
