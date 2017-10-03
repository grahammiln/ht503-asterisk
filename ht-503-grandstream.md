# HT-503 Settings

See [Making the Phone Vanish – Telephone Calls via an HT-503 and Raspberry Pi](https://theworklife.com/graham-miln/2017/09/24/telephone-calls-via-ht-503-raspberry-pi/) for a discussion of these settings.

## BASIC SETTINGS

- Telnet Server: No
- Device Mode: Bridge
- WAN side HTTP/Telnet access: Yes
- Unconditional Call Forward to VOIP: 2000 / *ip.address.raspberry.pi* / 5060

## FXO PORT

- Account Active: Yes
- Primary SIP Server: ip.address.raspberry.pi
- Outbound Proxy: ip.address.raspberry.pi
- SIP User ID: ht503fxo
- Authenticate ID: ht503fxo
- Authenticate Password: 1234
- SIP Registration: Yes
- FXO Termination > Number of Rings: 2
- FXO Termination > Impedance-based: Yes
- FXO Termination > PSTN Ring Thru FXS: No
- Channel Dialing > Stage Method (1/2): 1

## FXS PORT

- Account Active: Yes
- Primary SIP Server: ip.address.raspberry.pi
- Outbound Proxy: ip.address.raspberry.pi
- SIP User ID: ht503fxs
- Authenticate ID: ht503fxs
- Authenticate Password: 1234
- SIP Registration: Yes

# HT-503 Country Specific Settings

The following settings are specific to **France**.

## BASIC SETTINGS

- Time Zone: GMT+01:00

## ADVANCED SETTINGS

- Dial Tone: `f1=440@-10,f2=0@-10,c=0/0;`
- Ringback Tone: `f1=440@-10,f2=0@-10,c=150/300;`
- Busy Tone: `f1=440@-10,f2=0@-10,c=50/50;`
- Reorder Tone: `f1=440@-10,f2=0@-10,c=50/50;`

See [Operational Bulletin No. 781 (1.II.2003) and Annexed List: Various tones used in national networks](https://www.itu.int/pub/T-SP-OB.781-2003) for tone references.

## FXS PORT

- SLIC Setting: France

## FXO PORT

- FXO Termination > PSTN Disconnect Tone: `f1=440@-30,f2=440@-30,c=50/50;`
- FXO Termination > Country-based: France