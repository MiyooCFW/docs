# Configuration Pack

HYJiNX187's PCSX-Rearmed Config Library v1.0

Download [here](assets/PCSX_Rearmed_CFG_2.zip)

```
v1.1 Release Notes

- Added 25 PSX CFGs (Total 125)
- Update Gmenu2x Entry to support *.cue files and hide *.bin

v1.0 Release Notes

- Added 100 PSX CFGs
- Added Gmenu2x Custom Entry
- Added pcsx.dge wrapper script for loading cfg
```

## Introduction

This package was created to improve PSX support beyond default setup

## Pre-Requisites

Because I used many different BIOS to create these custom
configs, it is recommended that you provide the following PSX
BIOS. I cannot provide these to you, you will need to locate
them and ensure that they are placed in `\emus\pcsx_rearmed\bios`
- PSXONPSP660.BIN
- SCPH1001.BIN
- scph5500.bin
- scph5501.bin
- scph5502.bin
- scph7001.bin
- scph7502.bin

The 100 cfg files provided by this package expect NTSC PBP "roms"
to be named the same and reside in `/roms/PS1/*.PBP`

You will need to source your own PBP files and you should rename 
them to match the names of the cfg files located in 
`\emus\pcsx_rearmed\.pcsx\cfg\*.cfg`

If your PBP files are not named exactly like their corresponding 
CFG they will not load.

Example:

`\roms\PS1\Alien_Resurrection_(USA).PBP`

`\emus\pcsx_rearmed\.pcsx\cfg\Alien_Resurrection_(USA).cfg`

NOTE: The PBPs I used to test were official PBPs provided by PSN 
Servers. PSX ROMs available across the internet are of many
different formats, regions and versions. I cannot help you find
these and your mileage may vary if you use ROMs that are not
official NTSC PBPs of the games supported in this release.

Sharing of BIOS or PBPs is illegal and you should not ask for
help in obtaining these. Officially, you should be purchasing
these games and scraping them off of your devices.

## Installation
Unzip the contents of the zip file into the "Main" partition of
you Miyoo 1.3.3 CFW SD Card.



## Additional Information

This package provides configs for the top 100 games as defined by
the GameFAQs community and was created using the following thread

https://gamefaqs.gamespot.com/boards/916392-playstation/73165050

My package is based on Miyoo CFW 1.3.3 which can be found here:

https://github.com/TriForceX/MiyooCFW

PCSX-Rearmed was original ported by "Sauce" aka "GameBlaBla"
https://github.com/gameblabla/pcsx_rearmed/

The pcsx.dge and accompanying Gmenu2x entry are a work around for
the following known issue (fixed in latest PCSX-ReARMed):

https://github.com/notaz/pcsx_rearmed/issues/163

The -cfg flag does not allow you to directly pass a custom cfg to
PCSX. My DGE script will copy and overwrite the global pcsx.cfg
file for every game you launch under the Gmenu2x folder. When/if
this bug is resolved, the cfg files should be able to be passed
with a -cfg parameter file, but you will need to use my script
until the bug is resolved.

_Don't you dare ask for PBPs or BIOS files!_

<details><summary><b>View Hash List here</b></summary>

---

| Filename                                              | MD5                              | SHA1                                     | CRC32    | SHA-256                                                          | SHA-512                                                                                                                          | SHA-384                                                                                          | Full Path                                                                        | Modified Time         | Created Time        | Entry Modified Time  | File Size   | File Version  | Product Version  | Identical  | Extension  | File Attributes  |
|-------------------------------------------------------|----------------------------------|------------------------------------------|----------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------|---------------------|----------------------|-------------|---------------|------------------|------------|------------|------------------|
| Chocobo_Racing_(USA).PBP                              | ff8d30c1cfb0f572032918b6903003fb | d0d77feabe5a56e317adf5926faf5af6c0d73fae | 05602c74 | 7cfc2d7192aa9a710b3a45c8e528a43ea37d90df86cf1218112322453ef3f2e6 | cd2a3653359efa8a384feff0c38469452261ba4ca11569d72533806330e0ac7126e231c7cca99f54b45bea6e35efaa782b8faea45ec1e70635599b96be4b9a97 | eeb141727b29b2089755e3709ef97471dbbf1ba9bfe3caffca5a1b70c3ebe9ec8a21da121fafdbd89cd3caea47d1f0c0 | C:\Users\Kyle\Desktop\psx2\Chocobo_Racing_(USA).PBP                              | 2/18/2017 6:16:59 PM  | 3/5/2021 9:22:26 PM | 3/6/2021 11:22:55 AM | 243,383,841 |               |                  |            | PBP        | A                |
| Chocobos_Dungeon_2_(USA).PBP                          | bd812e532b3a1bc956720c2668fe5e09 | 0ed150e9795c93e07c9eb014f60ca9564e536206 | 2227e1ad | 2c2c240a28b984ea7ad62ca5480966dd9e4fccc8f84977b248e0f08226e2e37d | 27f177333ac7904b2b7c22be406212b65ffec70bc2e6882cb7d822962c7498d7ba85d581e5755fd80f37a57b545da29b3b40cade9069f51967af7add80de6972 | 4ea0954990cdb13c97c0a856d105a3e35a668329de3bad702130b49dbef0515932541d376dc1ce3874202c72cbc4002a | C:\Users\Kyle\Desktop\psx2\Chocobos_Dungeon_2_(USA).PBP                          | 2/19/2017 8:47:43 AM  | 3/5/2021 9:22:46 PM | 3/6/2021 11:23:09 AM | 329,151,025 |               |                  |            | PBP        | A                |
| Civilization_II_(USA).PBP                             | ce6acbd20d82a73cdb672a30fa86864f | e985202bfa9e887c92b7bd633927b7519c72d9c5 | 3629f040 | 8f6422e6834f2cbce9e72ed5d3feca4f3e2d4893b449d7301bcb977449eb5e08 | c9aa061cb72fb25c6757cdcb0d0d15814fecd57814e8d9c0796a1e6cf97e64cc5039c19384fc7dbed3ec8ecef70059d53adc8424a0a4e1545cca1ac13cbcc66d | 406a18705507b9a4ec3124a2ae6096791003087fc8e1fe5b82f84591f215dc2ce83e2d033380833c4f361ae311fbc4ba | C:\Users\Kyle\Desktop\psx2\Civilization_II_(USA).PBP                             | 2/15/2017 11:18:51 PM | 3/5/2021 9:23:02 PM | 3/6/2021 11:23:38 AM | 325,361,553 |               |                  |            | PBP        | A                |
| Disney-Pixar_Toy_Story_Racer_(USA).PBP                | becbd19d7123d9e8da2b2586486c05be | 419da99abbf2ae35043b0dc86569793905c852fa | 03fb4020 | 18253c9a74bbc6783cda578327a6e3eb0f950be0244e5ba7de228562b8ab42db | 82051526a7fba0c17f46567e39d0edf4741a5e62651cde68db0d556afba4b8f3bb1b4b2db518ba2f30516c3f73a3c68ed3f3143ad23f95118e95dbfe1d2f4ef3 | eb38a8bdb9e2c9a0732814b21fe378fb73b46f2e808a0b6197c1554211e4d20a014a8edd2dc7d912c4089ab15f53d2c8 | C:\Users\Kyle\Desktop\psx2\Disney-Pixar_Toy_Story_Racer_(USA).PBP                | 2/19/2017 2:20:24 AM  | 3/5/2021 9:23:48 PM | 3/6/2021 11:23:52 AM | 141,900,865 |               |                  |            | PBP        | A                |
| Duke_Nukem_Time_to_Kill_(USA).PBP                     | 5f34bdabea7afc3dfcceb0169788765a | 1ab20c931fac1fc2754c1110b67e4755d73af689 | 81af108a | 61cacbaa0e1ec874c558cbfd746fb66bb1670cf9dc0f727c4cab04f591c56977 | 26df6127668d24ad6b5c31404d117af0d38a16a90d9823c5edbbe05903c463d8dc436ea7174a8b0443e7625e01703b59fe43448afa96f0e7c555508b4930acc6 | c384b26309bc57372486a96bac9f176071cec83501380406e6565f9fd9f299146ed2c63d60e51aa1db67b5f19acdf014 | C:\Users\Kyle\Desktop\psx2\Duke_Nukem_Time_to_Kill_(USA).PBP                     | 2/19/2017 1:31:11 AM  | 3/5/2021 9:23:33 PM | 3/6/2021 11:24:36 AM | 230,698,721 |               |                  |            | PBP        | A                |
| Frogger_(USA).PBP                                     | c4b5240f2f43300af99959373ea1a948 | 734fb484f029b7117532872b8c45de684a4bb7f1 | ef4e82a8 | 974d42f1b5aab8ade09bcb94a487f834b9cfc256108f6b8388ab4f8255a8e54e | 382f9356e57503c705ab69912069396257d3345faeb1e3b0a40c0eccddcaafc9f2d7f4c8cbe0a88fbb9ac95d649ce3ba99b8d9fb705667200c368b8a0a7fdd9b | a9b827e3a977bd41fa1da43230ae0c5dade0eb0ea061e123b3e7227e6002d960f91270493d207e1432fd81b50ef1c279 | C:\Users\Kyle\Desktop\psx2\Frogger_(USA).PBP                                     | 2/19/2017 1:40:03 AM  | 3/5/2021 9:24:00 PM | 3/6/2021 11:25:01 AM | 159,242,145 |               |                  |            | PBP        | A                |
| Galaga_Destination_Earth_(USA).PBP                    | 1474b53fa9d9383daf188078395b0d46 | fcbe450be8511391c6d1f028138b021dc2593bb1 | ce5fac74 | f09a24ee18ee6a35e4906cc081f5f3a91ba05573ed6df349381b5d86e75dfe63 | 9000048e6d01c584759364f7fded63318eba2769b643d3b566f1667d617a1332288cd4e25d2d2684b02341ee2453ef12d4daa0288b0cc47339d64498c5c13e4b | 7c764f9a51ad94891625a2a85cf8e196289959b9c4d8f72d009d4d64543738fa04eaa53fda09a794a17d514bcc00d496 | C:\Users\Kyle\Desktop\psx2\Galaga_Destination_Earth_(USA).PBP                    | 2/19/2017 12:28:50 AM | 3/5/2021 9:25:00 PM | 3/6/2021 11:25:20 AM | 347,023,665 |               |                  |            | PBP        | A                |
| Kings_Field_(USA).PBP                                 | 2afee2e98591434ad988b4e5b9ce8414 | 17a51af8a187e1de6922c2352b32dd2d23cc68f3 | 6187a6af | 628b358249e317549cb4356d7c6f686882ecce02f8cf8b1555a7203bba1d83ef | d5f4c946a1994a8ef491dac4f941442547bd963403c03f84e8cdff5931145ab4e8248e225cd1ae4903deda498d21ba6c9c27504725cf3072b546b68d21804951 | 506353625f3d72ad680b650d2b7615331f9d311a0f52b36c1ba5586f2fb5abcb1e49089868940a54b6ef3e727d00bd7e | C:\Users\Kyle\Desktop\psx2\Kings_Field_(USA).PBP                                 | 2/18/2017 9:47:55 AM  | 3/5/2021 9:26:01 PM | 3/6/2021 11:25:42 AM | 154,985,761 |               |                  |            | PBP        | A                |
| Micro_Machines_V3_(USA).PBP                           | e86fb48676ca6a6c85ba294acbafd281 | 626afdadc8754d1e88f80341bc3ee6a1c7eacb7e | 4840d220 | 6dcb77bb56ef51b4fe77dde8a41fcdf88eba727100afc852658fcad79266311e | 1f2d7ff5b2ded87cb1092ac130780653413ccbb748d3917ef725842591003fde82ef359b8c9c77dd7b77a7325a134973035e1e2d961e22ae2d056677efb19bb2 | 6d291f008ac72754df939d419e30cdef50d13b627a18bc0b803fba28b5c433cf1ea2324ce8419f2f48899b2b5edd962d | C:\Users\Kyle\Desktop\psx2\Micro_Machines_V3_(USA).PBP                           | 2/19/2017 1:42:05 AM  | 3/5/2021 9:26:41 PM | 3/6/2021 11:25:53 AM | 238,944,433 |               |                  |            | PBP        | A                |
| Missile_Command_(USA).PBP                             | 43c9bd929ba6817e431a25531ee5fa8d | 948b4d071034cd674f1d093042d16731e3cacb7c | 90e9c50c | cecece99a600eeaf9bb3ec80bdc8f882c55ac2d5997e5b1077ba37685f4313cb | 8b0578fa5b55a5bf528d132ae4976afe37b6cd60de4552c024ac9be24709ccc3734f3920c3d3cbb7d2650ee0bec4baf5f9635d963e2c3c2bdd09445123e24561 | 5acc1198bdcdf1ecbe831d56ec2ba6021d41c5fb778f6a559b26673ae9b982ba4db7102a7e692ffdf190d7a479756da1 | C:\Users\Kyle\Desktop\psx2\Missile_Command_(USA).PBP                             | 2/19/2017 5:09:18 AM  | 3/5/2021 9:26:36 PM | 3/6/2021 11:26:01 AM | 211,668,353 |               |                  |            | PBP        | A                |
| Q-bert_(USA).PBP                                      | 614888349240ada6411a1c102e9ce7bf | 6ddb47d517825edf10245c8fc49378649eb8772b | bcb9ad3b | 845ddf4bd0dc0fb3643e066d7d472c89517397b648a295074d04679b45fc008d | 7ef3669d3cbdaf5c84ecfd05459bba32373d3f062e465a1bf6be66e51ed75c71bb15f95cd33419d21f93e2c051f17531ff65b4761675aef00e2dc4b574a396ab | 84bda6e2300d54d71cffa9e8ecd388f9e4a23ffdf7e6ef660cd3fd68239304b1813bd294b009e60d666a4aae6b6d9c7b | C:\Users\Kyle\Desktop\psx2\Q-bert_(USA).PBP                                      | 2/18/2017 11:21:23 PM | 3/5/2021 9:27:55 PM | 3/6/2021 11:26:06 AM | 142,300,385 |               |                  |            | PBP        | A                |
| Qix_Neo_(USA).PBP                                     | 879e02da0f9a1233583ef93e300fc343 | 1741db32b510b1e2f1913e113a7fd33df5d255e5 | 230b4497 | 4445236899a0581f015a0fa5a76d6c96cce88173727510f1b5adf376dc39758e | 90e66310374cb34b8ab5f2a9e947f168c0cc175e19c8f8b1c036d3f83a5a81a613b5e3b3bc4c80dfe6761f8f38340a46b95872e091963ab38304f4eb08261e84 | 9cc82f9f22feba1aee8a1832208ba256e6051c27143b7190470fe46a7de4cdfa5efb8bdffe3bc01ff377343c67c2fd82 | C:\Users\Kyle\Desktop\psx2\Qix_Neo_(USA).PBP                                     | 2/13/2017 1:24:15 AM  | 3/5/2021 9:27:59 PM | 3/6/2021 11:26:14 AM | 32,544,337  |               |                  |            | PBP        | A                |
| Rayman_(USA).PBP                                      | 22cd1aa497319dd08bef44ca56dcd2fd | 7f9ef6bf87df81332b3c2286eb4809ce0e365957 | 68fe04f9 | bd0923ca4ad4e2f99f6b80ac05002e28d645fe66f086c7a5f0797702decd1099 | b7ed6580aa799fb919e6d1a2aa5a430c90d9efef22c36b380c4e80e5fbe5ebee5d3ae9e92961aaa2a2650fc05f00e117def8631bb6c9dfc2a8b653d4ac05b1cf | 2834dd0bf629463b98f568c8dcf91238bb398a40ad9c86a3094af4ce25e3bb280519b1a58e4938531e7a3e3032a50a0f | C:\Users\Kyle\Desktop\psx2\Rayman_(USA).PBP                                      | 2/16/2017 1:22:47 AM  | 3/5/2021 9:28:31 PM | 3/6/2021 11:26:19 AM | 508,566,977 |               |                  |            | PBP        | A                |
| Rayman_2_The Great_Escape_(USA).PBP                   | dcb046d8a70c254af2af4f78a775926b | 74dd09946f4758b6997b24ec5d33dbd58c91d79e | 40faea6b | 9d0aa155a02e00c68074b5bff851c56a57ef9810e2283a7ba96b61aac7a22abc | 392b9a7448d9fe72692e22406116feba6c358064f510ca6f59109b91177a6e000626dc93a9f483c911c4cc5ed5a6715ba7ad60bc487824b53bfc1fc54b57f216 | cf611fd0df716b4842982e0da6e8072609b183c42fb13a0b2308257c79e6c1eb0a8af4891f3dcb96d5a5f7d37a878847 | C:\Users\Kyle\Desktop\psx2\Rayman_2_The Great_Escape_(USA).PBP                   | 2/16/2017 12:25:51 AM | 3/5/2021 9:28:43 PM | 3/6/2021 11:26:36 AM | 494,471,489 |               |                  |            | PBP        | A                |
| Robotron_X_(USA).PBP                                  | 9af6b13f345fb032a77c96bd4ce36f2e | 0d762d1c7eefe26c766f85bcab2afbf9a0df5986 | 88b4c5af | 213d888a30edc17a9a7d68978292919a29ee049dc078ff45f5e6747aef497101 | 9aceeecf1a484cc762daad364dba372f46af50117f4152ed0d6bee31fdd0068e7fa2caa291a730f0738c37c781fd8be6bf4d6ace7cd1ddf2eba7ae496b582709 | da769f26e68f05fd4c2a0e2e959eaaeea51b59d9388e4380f9c5b519f33b7020c09a4d2d1dc5aecdfd32c54176641354 | C:\Users\Kyle\Desktop\psx2\Robotron_X_(USA).PBP                                  | 2/19/2017 7:30:30 AM  | 3/5/2021 9:28:43 PM | 3/6/2021 11:26:45 AM | 654,347,665 |               |                  |            | PBP        | A                |
| SimCity_2000_(USA).PBP                                | 9b5f719aabdd82b337629c5f3f26930a | 88e853a682d2450d83cd19b98f467979054bd02d | b2bcc755 | 4e5ff9eda034dba1912b0acf3c9a5488d67bc934a22f5e76d1e2c0a3545d3f4e | da9e955652c51dbf148269900243b308b2e131ba47af3aecd599b2faa5c22bfc02fb25e9037d940f3c6160bf08568c8d33b4e6ce7a232fb60190c4ca6c886d82 | e56180af9ea75333f29e9de3b1384f9be743b316c58558b3104f7325a1f17983fa2c357d9fac421fbc8fce768d26a4f9 | C:\Users\Kyle\Desktop\psx2\SimCity_2000_(USA).PBP                                | 2/15/2017 1:56:26 AM  | 3/5/2021 9:29:48 PM | 3/6/2021 11:26:53 AM | 42,989,057  |               |                  |            | PBP        | A                |
| Space_Invaders_(USA).PBP                              | 35aea34bebba0235336f2a792e12916a | fd86f451676d317e41b343b359e9e94f3d8a78b0 | 0c00da46 | 3b761f9ba859e5599b6b1e7f48bdf95b0fbb792674fbc0e3cb2cc66776281fc2 | 77180fc4d5e39865ac4812ce030d6d5680166dafeb6efdedc93f9259694357594301541d4f8e54761d26ee93a5058d2750c0a76d39126a5e2ec708b41354f5c1 | b8a2b430be4454936e216ded094d2923abbda5c513c5de3b089687f22329c826a262976ee36c3fdc5c7bc4328ec834c6 | C:\Users\Kyle\Desktop\psx2\Space_Invaders_(USA).PBP                              | 2/19/2017 8:40:11 AM  | 3/5/2021 9:29:23 PM | 3/6/2021 11:27:04 AM | 136,956,385 |               |                  |            | PBP        | A                |
| Speed_Punks_(USA).PBP                                 | 432a47a9e105fe3e651b48b07a0da8cd | 1094f02020823086681f20192e620c6b82d41d37 | 7a51d60b | d1115b2155d4a57025bf6ce54bab861249111c8d029892ae1f72eff52e2ef65b | 80a2bb64d24f797d1cbb0fe756f0ea6c63f4e6e033ac6bb33bdff4359925c99fcb7e7ade62dd3a1a9d6f0d17e9ce083416a406d8b7a5626a431d33088b124ff0 | 372c3299ba486f54ba571bf316af2318e4c1d4bc3d30e61115abc852c303856c837170b52ba2af668533a789697062fd | C:\Users\Kyle\Desktop\psx2\Speed_Punks_(USA).PBP                                 | 2/19/2017 7:41:49 AM  | 3/5/2021 9:30:22 PM | 3/6/2021 11:27:13 AM | 478,377,937 |               |                  |            | PBP        | A                |
| Spider-Man_(USA).PBP                                  | 4cf220e38accc6a1d4f050c4a18529dc | 8134b74ec6fc13c2c47325775dba650d81efa62f | 95aa8c70 | 59e777cc1763bdd259e6915551c2b635077f19195ff0925534048c324f8e1d12 | 65e532f1f5351ceace8e56e60426c6424d199b58579b2dd717554f9d35d06d6ddc9110444e6d5a36da5a63e56c8ec58abcd11aab3fa84c18a5305f41c14220d9 | ae4698684bff431ad25e96c87dcde1fc0cfe2b867f2a9733f9a311043aea3ce64e5d1d93a521a0c666cf7328a0c16d1a | C:\Users\Kyle\Desktop\psx2\Spider-Man_(USA).PBP                                  | 2/19/2017 2:58:19 AM  | 3/5/2021 9:31:01 PM | 3/6/2021 11:27:20 AM | 439,647,457 |               |                  |            | PBP        | A                |
| Spider-Man_2_Enter_Electro_(USA).PBP                  | 4cc3969f5e147f9f6be2b507b1d9f132 | 37cfc23aa78a92b6f52024e783c62732134d6358 | dd9a4c4f | 8b5bb73af618cb8fceece387fb3980ea74f34027aaf373f52b172c4d5ba0a8c3 | 76c3ccba98dd51c5412a803b2bb21c843e17969fcba66a667c0a60e5054dba2e1cf03cd8affc7b37a4efaafbe27d09ecf82637f05fc65e6f0c638045eec5384e | 0d8d3bec3c4d87830855444cbaad8fa5832036e7962995aaa124aee37111dee0b7c0e2401a3993cae030f0deb2676d7d | C:\Users\Kyle\Desktop\psx2\Spider-Man_2_Enter_Electro_(USA).PBP                  | 2/19/2017 8:44:32 AM  | 3/5/2021 9:29:51 PM | 3/6/2021 11:27:36 AM | 378,939,169 |               |                  |            | PBP        | A                |
| Tempest_X3_(USA).PBP                                  | 88bd65b2ad498dcbb22214c1b2197c40 | f20ddf4f5622930f8f9451386b2246243e6d3be6 | b91e77cb | 037cdd2eebc7ffbfacc1f6e95a8829c6abb69c2991f38651824a9dddd62fc219 | 1d7e0d52d50c840f237e75db140f4c52983e4d1289aa598dad7129eb996aa0a9dcefb39e6699c2d99257f96a41ecb7ce8b93d807191f4b2640592c2891461e7d | 0318954807463c0e0098d5f082233b79d390779cae005923733d12b96b1f2fbdb303feb344e5f6ffba5d6d821dd5a162 | C:\Users\Kyle\Desktop\psx2\Tempest_X3_(USA).PBP                                  | 2/18/2017 4:05:42 PM  | 3/5/2021 9:32:15 PM | 3/6/2021 11:27:45 AM | 248,803,841 |               |                  |            | PBP        | A                |
| Test_Drive_Off-Road_2_(USA).PBP                       | 77f41385cdaeead01822ad13f22356c7 | 5700d69de9ade2aa924d1dc0db6390df6f99c627 | 525fe73c | d450c2d118fa30fe1d25221c3fa23aeea6592f06c1189479cfa8ce5f1069c1c8 | 3f02af8b82c77b10a74459fb58b2db776b70d854bf095953ad741b800aa394c59f760aa4ed1d3b1af4f5f58e7a7cc1182bf76816c0e5611de65228a06e3418e8 | 78e332a12cfa784e693636e0c2b747fa14fdc5fa3ab94632089826766123156c865f22de038a148ba0f71ebbd6fabcf8 | C:\Users\Kyle\Desktop\psx2\Test_Drive_Off-Road_2_(USA).PBP                       | 2/17/2017 11:40:04 PM | 3/5/2021 9:32:35 PM | 3/6/2021 11:27:59 AM | 140,132,065 |               |                  |            | PBP        | A                |
| Twisted_Metal_III_(USA).PBP                           | 1ab2035fdf6fec9bc5971e1c2e9f1de9 | 77fae3dd9b1082250a305e47a998139fdeb056da | 47bd2c48 | 43f1883f834b8faa65ed526470f4328dc3fa525d1130f8120c7533061e564f3f | f91098de37870f9ce0ba1a1b657d5e5dc6b145541cbf38beac5e412410d199939f4f817f20d738fd2c26fd601c13f0d348f177d06fcde4b63d1dcc7e24edba98 | ffa94f657d345e78441f7bfa0d3a713b6600d761b284b4b0790b45ba679f2abe7b2a1aec26ce1de50d6f2b2bbdf331b7 | C:\Users\Kyle\Desktop\psx2\Twisted_Metal_III_(USA).PBP                           | 2/19/2017 7:16:31 AM  | 3/5/2021 9:32:42 PM | 3/6/2021 11:28:10 AM | 564,892,817 |               |                  |            | PBP        | A                |
| Um_Jammer_Lammy_(USA).PBP                             | 8b39018b89e8af9b6893e0970927f6a8 | 8e5d1daec95a28535ebb85e755386e79a9447308 | 21d3a6e3 | 07594a3213994e1afa6ddec8aff1028e984d4187f931e1cd4fc144e3b8e6817e | c8b18cb14e0f2cf5440d54bd9d477bb3afe6326d9bb37aa8f5eb566c458e6e29843bf413e92f56a871e182d7d717d64f887f4e6cdd4a1a4797fb1b33b8cb0f68 | b18838bddf8eff656a941ed7fd2d53088a404f88613a0d9268e4bee1ccdc3623bd0736fe4651d9078028fbe2f407c8da | C:\Users\Kyle\Desktop\psx2\Um_Jammer_Lammy_(USA).PBP                             | 2/19/2017 6:47:52 AM  | 3/5/2021 9:33:24 PM | 3/6/2021 11:28:20 AM | 576,296,993 |               |                  |            | PBP        | A                |
| Walt_Disney_World_Quest_Magical_Racing_Tour_(USA).PBP | 69b19f033ae947385bafdf73b8a38021 | 1a77a1b78e9613730aa624513b5fc938604df294 | 450e774e | e214aed91f5a35bdd4b3f1e81ffe520f1ffb25e5b790791e53fe977abdd3b4c1 | c91a06f5a9df976d22136d8c251cc9466688883602aff4fd4124c734b459848d7b59c2c161954d210f99afd65ed9c3e11eca4fc6178cf2da67e02ee0b3f3eda7 | ae38a451c1054b3f9c1a94df1615473d0169a8beddf3e3f7faf6c4438ba0d68210dbd5d57510a9aa83e7f0c97fd20d9f | C:\Users\Kyle\Desktop\psx2\Walt_Disney_World_Quest_Magical_Racing_Tour_(USA).PBP | 2/19/2017 4:55:12 AM  | 3/5/2021 9:34:13 PM | 3/6/2021 11:28:43 AM | 206,896,129 |               |                  |            | PBP        | A                |

---

</details>

# Compatibility List
Thanks to $Lud for this guide

Warning! This compatibility list is for the optimized PCSX ReARMed version on this page, see more here.

| Game Title                    | Region       | Compatibility          | Device    | Average FPS | Comments                                                                                                                                                     |
|-------------------------------|--------------|------------------------|-----------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crash Bandicoot               | Europe (PAL) | Graphical/Audio Issues | Pocket Go | 20-45       | Some FPS drop down in some parts of levels, audio can be heard, with some issues.                                                                            |
| Driver - You Are the Wheelman | USA (NTSC-U) | Graphical/Audio Issues | Pocket Go | 28-35       | Can be played, but with lag, audio is a bit choppy, but you can understand what the narrator says.                                                           |
| Gran Turismo                  | Europe (PAL) | Playable               | Pocket Go | 29-40       | At start and in menu selector, screen is bigger than the console screen, in-game can be playable decently, you can hear the background music in mid quality. |
| Gran Turismo 2                | Europe (PAL) | Graphical/Audio Issues | Pocket Go | 36-44       | You can heard in-game audio in good quality very often.                                                                                                      |
| Klonoa - Door to Phantomile   | Europe (PAL) | Graphical/Audio Issues | Pocket Go | 28-35       | Choppy audio, uncomfortable.                                                                                                                                 |
| Rayman                        | Europe (PAL) | Playable               | Pocket Go | 50-52       | Audio can be heard in good quality (2D game).                                                                                                                |
| Resident Evil                 | Europe (PAL) | Playable               | Pocket Go | 46-50       | Choppy audio with lag spikes sometimes, fast when playing and moving the player.                                                                             |
| Spider-Man                    | Europe (PAL) | Graphical/Audio Issues | Pocket Go | 28-30       | Choppy audio with uncomfortable noise in the background, but can be played at mid quality. Needs a tweak with configuration for L2-R2 triggers.              |
| Tekken 3                      | Europe (PAL) | Graphical/Audio Issues | Pocket Go | 27-33       | Very uncomfortable when playing, choppy audio.                                                                                                               |
| Tony Hawk's Pro Skater 3      | Europe (PAL) | Graphical/Audio Issues | Pocket Go | 28-37       | Can be heard background music, in-game music is very choppy and uncomfortable.                                                                               |

# Compatibility List (Old)
Thanks to Pifen for this guide

Notice all of this testing is for anyone wondering if the game they want to play works.
The emulator for pocketgo is still infant with what it can do.
Don't expect things to run on first try and what i consider good frames may not be to your liking.
I will not be testing out your liked games so don't ask me to download x or y game.

All tests done with PocketGo CFW 1.1
- Bios 1001
- GPU UNAI
- Default sound
- EBOOT format is .PBP
- PS1 format is .cue/.bin

Some games choosen to use PSP EBOOT mostly for space reasons
Great example is the 10+ files in PS1 Ace Combat
Easier to use PSP format

For control schemes to original games use PSX database.

| ﻿FORMAT | NAME                        | STATUS         | FRAME SKIP | FRAME STATUS                                          | NOTES                                                                                                             |
|--------|-----------------------------|----------------|------------|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| PSP    | ALIEN TRILOGY               | WORKING        | AUTO FS    | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PSP    | ACE COMBAT                  | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PS1    | ACE COMBAT 2                | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PS1    | ACE COMBAT 3                | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PS1    | BATTLE TANX GLOBAL ASSAULT  | WORKING        | FS 1       | HEAVY FRAME DROP                                      | NOTICEABLE NEAR TANK EXPLOSIONS                                                                                   |
| PSP    | BLOOD OMEN LEGACY OF KAIN   | WORKING        | FS 1       | MENU ISSUES BUT VERY PLAYABLE                         |                                                                                                                   |
| PS1    | C&C RETALIATION             | WORKING        | AUTO FS    | SLIGHT FRAME DROP                                     | NORMALLY WHEN MOVING MANY UNITS                                                                                   |
| PS1    | C&C RED ALERT               | WORKING        | AUTO FS    | SLIGHT FRAME DROP                                     | NORMALLY WHEN MOVING MANY UNITS                                                                                   |
| PS1    | C&C                         | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | NORMALLY WHEN MOVING MANY UNITS                                                                                   |
| PSP    | CASTLEVANIA SYMPHONY NIGHT  | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | COLONY WARS                 | WORKING        | FS 1       | NOTICEABLE DROPS NEAR LARGE SHIPS                     | DON'T DO THIRD PERSON                                                                                             |
| PSP    | COLONY WARS VENGEANCE       | WORKING        | FS 1       | NOTICEABLE DROPS NEAR LARGE SHIPS                     | DON'T DO THIRD PERSON                                                                                             |
| PSP    | COLONY WARS 3 RED SUN       | WORKING        | FS 1       | NOTICEABLE DROPS NEAR LARGE SHIPS                     | DON'T DO THIRD PERSON                                                                                             |
| PSP    | DIGIMON WORLD 1             | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PSP    | DIGIMON WORLD 2             | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PS1    | DIGIMON WORLD 3             | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PS1    | DINO CRISIS                 | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PSP    | DINO CRISIS 2               | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | SOME ISSUES WITH IN GAME CUTSCENES                                                                                |
| PS1    | DINO CRISIS 2               | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | SOME ISSUES WITH IN GAME CUTSCENES                                                                                |
| PSP    | DUNE 2000                   | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PS1    | DUNE 2000                   | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PS1    | MEGAMAN LEGENDS             | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | AIMING IS A PAIN BUT ALLIVIATED WITH AUTO AIM                                                                     |
| PSP    | MEGAMAN LEGENDS             | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | AIMING IS A PAIN BUT ALLIVIATED WITH AUTO AIM                                                                     |
| PS1    | MEGAMAN LEGENDS 2           | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | AIMING IS A PAIN BUT ALLIVIATED WITH AUTO AIM                                                                     |
| PSP    | MEGAMAN LEGENDS 2           | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | AIMING IS A PAIN BUT ALLIVIATED WITH AUTO AIM                                                                     |
| PS1    | FRONT MISSION 3             | WORKING        | FS 1       | BARELY ANY DROP                                       | MAIN MENU AT START IS BLACK BUT JUST CLICK X TO START GAME AND IT PLAYS PERFECTLY                                 |
| PS1    | FINAL FANTASY 7             | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | ON HEAVY DUTY SPELLS                                                                                              |
| PS1    | HYDRO THUNDER               | WORKING        | FS 1       | ALMOST UNPLAYABLE                                     | NEEDS BETTER GPU SUPPORT                                                                                          |
| PS1    | GAMESHARK V2                | SOUNDS ONLY    |            |                                                       |                                                                                                                   |
| PS1    | GAMESHARK V4 (UNL)          | NOTHING        |            |                                                       |                                                                                                                   |
| PSP    | GEX                         | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | GEX 2                       | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PSP    | GEX 3                       | WORKING        | FS 2       | SLIGHT FRAME DROP                                     | RECOMMEND FS 2 FOR THIS GAME THEY WENT ALL OUT WITH THE DETAIL                                                    |
| PSP    | GRAN TURISMO                | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | MAIN MENU IS WIDE BUT DOESN'T AFFECT GAMEPLAY                                                                     |
| PSP    | GRAND THEFT AUTO            | WORKING        | FS 1       | BARELY ANY DROP                                       | THE GAME IS TINY SO EXPECT TO DIE FROM GUNSHOTS YOU BARELY SEE                                                    |
| PSP    | GTA LONDON                  | WORKING        | FS 1       | BARELY ANY DROP                                       | THE GAME IS TINY SO EXPECT TO DIE FROM GUNSHOTS YOU BARELY SEE                                                    |
| PSP    | IN THE HUNT                 | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PSP    | INTELLIGENT QUBE            | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | LEGO ROCK RAIDERS           | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | NEAR MANY PLACED BUILDINGS                                                                                        |
| PSP    | MARVEL VS STREET FIGHTER    | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | MDK                         | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PS1    | METAL GEAR SOLID            | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PS1    | NEED FOR SPEED 3            | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | DUE TO JUST OVERALL SPEED AND TRACKS                                                                              |
| PSP    | PANDEMONIUM!                | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PSP    | PANDEMONIUM! 2              | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PS1    | PANZER FRONT                | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | PARASITE EVE                | CRASH          |            |                                                       |                                                                                                                   |
| PSP    | PARASITE EVE 2              | CRASH          |            |                                                       |                                                                                                                   |
| PS1    | PARASITE EVE 1              | WORKING        | FS 1       | SLIGHT FRAME DROP                                     | GPU STRUGGLES WITH TEXT AND AYA MODEL BUT STILL PLAYABLE                                                          |
| PS1    | PARASITE EVE 2              | INTRO          |            |                                                       | GAME SHOWS INTRO BUT DOESN'T REACH MAIN MENU                                                                      |
| PSP    | RESIDENT EVIL 1             | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | RESIDENT EVIL 2             | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | RESIDENT EVIL 3             | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PS1    | SILENT HILL                 | WORKING        | FS 1       | VERY HEAVY FRAME DROPS                                | NEEDS BETTER GPU SUPPORT                                                                                          |
| PSP    | SILENT HILL                 | CRASH          |            |                                                       |                                                                                                                   |
| PSP    | SPYRO 3                     | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PSP    | STEEL REIGN                 | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PSP    | SUIKODEN                    | CRASH ON START |            |                                                       |                                                                                                                   |
| PS1    | SUIKODEN                    | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PS1    | SUIKODEN 2 BUGFIXED PATCHED | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | SYPHON FILTER               | WORKING        | FS 1       | BAD FRAME DROPS ON SOME LEVELS                        | WOULD SUGGEST PATIENCE WITH THIS ONE                                                                              |
| PSP    | TEKKEN 3                    | WORKING        | FS 1       | HEAVY FRAME DROP                                      | STILL PLAYABLE BUT SOME MOVES GO INVISIBLE DUE TO FRAME DROP                                                      |
| PSP    | TOMB RAIDER                 | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | TOMB RAIDER 2               | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | TONY HAWK                   | WORKING        | FS 1       | SLIGHT FRAME DROP                                     |                                                                                                                   |
| PSP    | TONY HAWK 2                 | WORKING        | FS 1       | BAD FRAMES GAME IS PLAYABLE BUT YOU WILL DESPAIR      |                                                                                                                   |
| PSP    | VIGILANTE 8                 | WORKING        | FS 1       | FRAME DROPS ON MANY TERRAIN OBJECTS BUT VERY PLAYABLE | SUGGEST L2 AS TRIANGLE AND R2 AS CROSS FOR WEAPON FIRING, YOU MAY NEED TO PUT CROSS AS START BUTTON ALSO FOR MENU |
| PSP    | VIGILANTE 8 2ND OFFENSE     | WORKING        | FS 1       | FRAME DROPS ON MANY TERRAIN OBJECTS BUT VERY PLAYABLE | SUGGEST L2 AS TRIANGLE AND R2 AS CROSS FOR WEAPON FIRING, YOU MAY NEED TO PUT CROSS AS START BUTTON ALSO FOR MENU |
| PSP    | WARCRAFT 2                  | WORKING        | FS 1       | BARELY ANY DROP                                       | NOTICE TEXT IS SMALL, IT'S ALL VOICED SO LISTEN TO GAME                                                           |
| PS1    | WILD ARMS                   | WORKING        | FS 1       | BARELY ANY DROP                                       | MAIN MENU FRAMES ARE BAD                                                                                          |
| PS1    | WILD ARMS 2                 | WORKING        | FS 1       | BARELY ANY DROP                                       | PERFECT MAIN MENU                                                                                                 |
| PSP    | WIPEOUT 3                   | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |
| PSP    | WORMS                       | WORKING        | FS 1       | BARELY ANY DROP                                       | WORMS ARE VERY TINY MEMORIZE WHO YOUR TOONS ARE                                                                   |
| PSP    | XENOGEARS 1.0               | STUCK BOOTING  |            |                                                       |                                                                                                                   |
| PSP    | XENOGEARS 2.0               | WORKING        | FS 1       | BARELY ANY DROP                                       | MAIN MENU IS STRETCHED BUT EASY TO SELECT NEW GAME                                                                |
| PS1    | YU-GI-OH! FORBIDDEN         | WORKING        | FS 1       | BARELY ANY DROP                                       |                                                                                                                   |