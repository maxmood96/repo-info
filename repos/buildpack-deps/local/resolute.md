# `buildpack-deps:resolute`

## Docker Metadata

- Image ID: `sha256:9111db4342fa7443dbb506583cfb0bf7555cd9e849a00f12bcd975967b4fa39b`
- Created: `2026-02-17T21:48:32.880666583Z`
- Virtual Size: ~ 819.65 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
- Labels:
  - `org.opencontainers.image.ref.name=ubuntu`
  - `org.opencontainers.image.version=26.04`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.3.2-2`

Binary Packages:

- `libacl1:amd64=2.3.2-2`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.3.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-2.dsc' acl_2.3.2-2.dsc 2604 SHA512:8376928f8a96880edce6e6f1073623ed03bf3da4489807d531c0ecd4c5ff09d19754007e3533922389134aa55a4b64d6f71caa7186133d5a5f559eecf7e33427
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz' acl_2.3.2.orig.tar.xz 371680 SHA512:c2d061dbfd28c00cecbc1ae614d67f3138202bf4d39b383f2df4c6a8b10b830f33acec620fb211f268478737dde4037d338a5823af445253cb088c48a135099b
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2.orig.tar.xz.asc' acl_2.3.2.orig.tar.xz.asc 833 SHA512:a425b385e3ce30e7146cf8b143ca269e3edd78af82a21dea76d10ea68215f9abcfb1ed8be24ce3b6dce24e6640df8d5d5f365a47399e37006a66c6a62a41fe41
'http://archive.ubuntu.com/ubuntu/pool/main/a/acl/acl_2.3.2-2.debian.tar.xz' acl_2.3.2-2.debian.tar.xz 24296 SHA512:58f4f202baa58a6912f85682b967dca282981c1b8d57ffcda1cd67784b5e3f1865ccd1c452d06a50978649d3cb5198d2d5d23004e103b5bd89352a7c1904444f
```

### `dpkg` source package: `adduser=3.153ubuntu1`

Binary Packages:

- `adduser=3.153ubuntu1`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.153ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.153ubuntu1.dsc' adduser_3.153ubuntu1.dsc 1807 SHA512:29c8a19c57ce30211a3facb7ee7cfe03df68dbb0282fb88cc28aa810ca0d60a2caa08228372e8b72ec54508fc96187bbf9f978f127eded41d94b77d0ec7d084c
'http://archive.ubuntu.com/ubuntu/pool/main/a/adduser/adduser_3.153ubuntu1.tar.xz' adduser_3.153ubuntu1.tar.xz 339348 SHA512:d01e1aa88a84afb8cf55e5afbe920e00b5ade6456d59d7a16a092027442fc6de2c2200fec8508ebd5fc09241c2b4409fd437e2d92a0689fb1a2ea4038f0d8223
```

### `dpkg` source package: `aom=3.13.1-2`

Binary Packages:

- `libaom3:amd64=3.13.1-2`

Licenses: (parsed from: `/usr/share/doc/libaom3/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `BSD-3-Clause`
- `BSD-3-clause`
- `Expat`
- `ISC`
- `public-domain-md5`

Source:

```console
$ apt-get source -qq --print-uris aom=3.13.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.13.1-2.dsc' aom_3.13.1-2.dsc 2402 SHA512:cc86258464b3b5eb3a2be500c0f5387b1a93952336b057fade04c9ffa2bf2bec104e6cf6e7b3992458c6d16e26ee809678ea50dc6f483ab9639733986d4d95db
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.13.1.orig.tar.gz' aom_3.13.1.orig.tar.gz 6262920 SHA512:cde7b044131bdf642758948b6ccbcfa1c79d1d698badfc3a82d88f78ef09c55c6ac3a04e3c515af2f89becf94eb48f0af5145e0784628f95676a85e8dd350a7a
'http://archive.ubuntu.com/ubuntu/pool/main/a/aom/aom_3.13.1-2.debian.tar.xz' aom_3.13.1-2.debian.tar.xz 20840 SHA512:082d2e163f7c1d4bcb4c6fe76d88e75c4e11339bef19c32f64a68c952db3cd5f23aee361ac4a726fb2febfe0863a2ec58ef2679df4df11f8e30ac0695e7def5e
```

### `dpkg` source package: `apr-util=1.6.3-3ubuntu3`

Binary Packages:

- `libaprutil1t64:amd64=1.6.3-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libaprutil1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr-util=1.6.3-3ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-3ubuntu3.dsc' apr-util_1.6.3-3ubuntu3.dsc 2647 SHA512:3ebd82905a9f82a3ff57b91e22b3423473c656b4e2b375f9633294de9f55128e9464f4c22ba2e31f253604627ca39e43a41362e95ea6c6568b5fcea2511d4554
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3.orig.tar.bz2' apr-util_1.6.3.orig.tar.bz2 432692 SHA512:8050a481eeda7532ef3751dbd8a5aa6c48354d52904a856ef9709484f4b0cc2e022661c49ddf55ec58253db22708ee0607dfa7705d9270e8fee117ae4f06a0fe
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr-util/apr-util_1.6.3-3ubuntu3.debian.tar.xz' apr-util_1.6.3-3ubuntu3.debian.tar.xz 342676 SHA512:92724a96f75695a81d68f9cf2a9a10bef86ab62965a6d0fc4af05fe78fd17277ce71c01ab9549632011393786e34430756d4b098ed80f14b39964b825cc904f9
```

### `dpkg` source package: `apr=1.7.6-3`

Binary Packages:

- `libapr1t64:amd64=1.7.6-3`

Licenses: (parsed from: `/usr/share/doc/libapr1t64/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris apr=1.7.6-3
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.6-3.dsc' apr_1.7.6-3.dsc 2402 SHA512:4f8e25a2f05c2c0530e832f12b339ec0e44131f04e0d95008f345eba2bac88201e179a85fde6c2f1f86988fd16b2ded3d92bef4a471ef702ebabe8fa66b28cee
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.6.orig.tar.bz2' apr_1.7.6.orig.tar.bz2 899670 SHA512:629b60680d1244641828019db903a1b199e8a19c8f27a5132b93faacb381ce561f88463345ab019258f1f1e8cfdf8aa986ac815153a8e7e04a22b3932f9fedd2
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.6.orig.tar.bz2.asc' apr_1.7.6.orig.tar.bz2.asc 898 SHA512:e20000b14e94f164a37c90c122f6e7469f2b26f62792ced4573a0aebc80d0a53d864f14ecf62c6f30531e5ab42b987ce7faffec1d9207acddfaa21378550e282
'http://archive.ubuntu.com/ubuntu/pool/main/a/apr/apr_1.7.6-3.debian.tar.xz' apr_1.7.6-3.debian.tar.xz 42384 SHA512:64ea438a1601a4e0c91c9da54f91e4bf4237d5b7b426c2bddf9a925f8590fe431c3b63c8f7fe4c7724d2c4b65bd54c50c35670467fe5985d8ef971e1b25853d5
```

### `dpkg` source package: `apt=3.1.12`

Binary Packages:

- `apt=3.1.12`
- `libapt-pkg7.0:amd64=3.1.12`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/3.1.12/


### `dpkg` source package: `architecture-properties=0.2.6build1`

Binary Packages:

- `native-architecture=0.2.6build1`

Licenses: (parsed from: `/usr/share/doc/native-architecture/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris architecture-properties=0.2.6build1
'http://archive.ubuntu.com/ubuntu/pool/main/a/architecture-properties/architecture-properties_0.2.6build1.dsc' architecture-properties_0.2.6build1.dsc 2021 SHA512:0432d55556993abf40b2e8101737b5c34ba505014509ea25eafd20e6959808562bc8cd4bc04d83e230c6905bbeb0c7f9446f2061f2d77518091ffa3b3a9f7099
'http://archive.ubuntu.com/ubuntu/pool/main/a/architecture-properties/architecture-properties_0.2.6build1.tar.xz' architecture-properties_0.2.6build1.tar.xz 5480 SHA512:f62b93a3167457a8c34346a77b4bda40722134f6986a1b7b62e4876261127afc8d4f52f0b9442153ed985f2926eeb5ba2248aa2db9890e96c58e1652a3a6a84e
```

### `dpkg` source package: `attr=1:2.5.2-3build1`

Binary Packages:

- `libattr1:amd64=1:2.5.2-3build1`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `audit=1:4.1.2-1`

Binary Packages:

- `libaudit-common=1:4.1.2-1`
- `libaudit1:amd64=1:4.1.2-1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.1.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.1.2-1.dsc' audit_4.1.2-1.dsc 2546 SHA512:e15a01ca5f2f34698c3e8fdf2d0f3c020c2e3e14efa7df3e9652db7663cf0f2b7c6cdd44abe8c90fa0388f03d6840ea6eef59978debde12782ff1fda630ea9f5
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.1.2.orig.tar.gz' audit_4.1.2.orig.tar.gz 656095 SHA512:a47fec1041e11a76ad57b57bcf6e9b454188d95ec26cabf15e92e114d46c7c8f09ddb251d5aebef8bc7faacc6ccffe44c73543d8234af237548b4ad89a408fc3
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.1.2-1.debian.tar.xz' audit_4.1.2-1.debian.tar.xz 19712 SHA512:517cbcfaad3e2310535c349c74a3173b3fbd30e8ff0828ba844204bab43cc0a69fde1227944bb449a2c7eb2d9e906cdbe08f4e6494014e632d11be14a9ef47c7
```

### `dpkg` source package: `autoconf=2.72-3.1ubuntu2`

Binary Packages:

- `autoconf=2.72-3.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/autoconf/copyright`)

- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `GPL-3+ with Texinfo exception`
- `MIT-X-Consortium`
- `no-modification`
- `other`
- `permissive`
- `permissive-long-disclaimer`
- `permissive-short-disclaimer`
- `permissive-without-disclaimer`
- `permissive-without-notices-or-disclaimer`

Source:

```console
$ apt-get source -qq --print-uris autoconf=2.72-3.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72-3.1ubuntu2.dsc' autoconf_2.72-3.1ubuntu2.dsc 2174 SHA512:2134467f3f8ef02ff7d21b83b3f7948c0421d88f380380b3517e6ffadebb39fcedd4017a381863af865e18bad0f0342680f504fa77282bb9a289fcb4e3c2fa7a
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72.orig.tar.xz' autoconf_2.72.orig.tar.xz 1389680 SHA512:c4e9fbd858666d3e5c3b4fe7f89aa3e8e3a0a00dc7e166f8147d937d911b77ba3ac6a016f9d223ccdd830bc8960b3e60397c0607cc6a1fd2c50c7492839ddd17
'http://archive.ubuntu.com/ubuntu/pool/main/a/autoconf/autoconf_2.72-3.1ubuntu2.debian.tar.xz' autoconf_2.72-3.1ubuntu2.debian.tar.xz 27464 SHA512:d74e44153e643ba63bd0039d3efe2f351e3dfd7a7c92ac4fdbb7934d46c5585e45603e9546c41ec5f8847b8fb9dab1deae301975e7a71d9dfb517e7cd40da287
```

### `dpkg` source package: `automake=1:1.18.1-3build1`

Binary Packages:

- `automake=1:1.18.1-3build1`

Licenses: (parsed from: `/usr/share/doc/automake/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris automake=1:1.18.1-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake/automake_1.18.1-3build1.dsc' automake_1.18.1-3build1.dsc 2507 SHA512:6d57cbd12e802c1813128a78878f7126ef4a98ed4d5bc7950e4e953ebdb649403b5dc5d9732d2ba3089fa8ef59248fa5a2a996d2bcff183590477b690c7a7f81
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake/automake_1.18.1.orig.tar.xz' automake_1.18.1.orig.tar.xz 1652392 SHA512:8baa16831416a953a743f4e3c0f55cea5ebefe0f5a7a0e390581981d4461d02dc9038415124e974b2ec390c40daaa241802cd7d42c6fafb793f87cf355db2a61
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake/automake_1.18.1.orig.tar.xz.asc' automake_1.18.1.orig.tar.xz.asc 488 SHA512:5a1f0e89a8f3826c766aa98617765f4a576dc278abb7a0a4c0fa04d27d15bf670b79853642914db58731eb4dc737f0b9ad65ba9a07b7bb227e763e90e2e54349
'http://archive.ubuntu.com/ubuntu/pool/main/a/automake/automake_1.18.1-3build1.debian.tar.xz' automake_1.18.1-3build1.debian.tar.xz 22812 SHA512:23072852bb6912f012834c1bceff01d3573ae7f536f7ba167f4328c3d08e2887cbb2174f40de8e90f51a3af71afa69a967bcd7f6d496394d5968a490d525e42b
```

### `dpkg` source package: `autotools-dev=20240727.1build1`

Binary Packages:

- `autotools-dev=20240727.1build1`

Licenses: (parsed from: `/usr/share/doc/autotools-dev/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris autotools-dev=20240727.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20240727.1build1.dsc' autotools-dev_20240727.1build1.dsc 1685 SHA512:939ac00c18d45c49a6dadd75c5afbb3ea98eb0a602c344204b234bfd47f2a498b52146d89cad974318762f5a54db3cd8de3dedbe9734d7da71ff03207d9acd30
'http://archive.ubuntu.com/ubuntu/pool/main/a/autotools-dev/autotools-dev_20240727.1build1.tar.xz' autotools-dev_20240727.1build1.tar.xz 99820 SHA512:2db2a06fd868ab043e854c00c7e5e78cee60ec38d83babd84492c5da7da57581fbca64a0d4ef4b4471f77b95b7d11ff4eb811db35f7f699444c5906b50329099
```

### `dpkg` source package: `base-files=14ubuntu5`

Binary Packages:

- `base-files=14ubuntu5`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`
- `GPL-2+`
- `verbatim`

Source:

```console
$ apt-get source -qq --print-uris base-files=14ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_14ubuntu5.dsc' base-files_14ubuntu5.dsc 1727 SHA512:cd864000c1c3b385f8c995899be30e64b653c482abcf74da9f52b8b26275c94fcaf082f48faba584a90b28b29fba19f0ac06db506bef264e7e09e99d5875bd86
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-files/base-files_14ubuntu5.tar.xz' base-files_14ubuntu5.tar.xz 97972 SHA512:73bb888d0691426ea5d9637a00ad82c99907485a6db473ef078596c5705f4882d4d19acc85944cf51badea9c6f0713c95dc60040fa6315370e24afbad04f90a1
```

### `dpkg` source package: `base-passwd=3.6.8`

Binary Packages:

- `base-passwd=3.6.8`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.6.8
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.8.dsc' base-passwd_3.6.8.dsc 2044 SHA512:cacd3929c178191cacd4b08f810e28a76987938db2efd2c3a9a990ad8400f75f69760c21fc9c6b370bd7f181a678ae52a01817776972475f75b6d855dc72afbc
'http://archive.ubuntu.com/ubuntu/pool/main/b/base-passwd/base-passwd_3.6.8.tar.xz' base-passwd_3.6.8.tar.xz 61840 SHA512:f8d58fa5fa7c4242793121f43220012b328d55796af69b2def61630de2a180bff3bc72e816a24d4ab96cc3dd98bb677b68f6d00f9ee54568189822959f8a475e
```

### `dpkg` source package: `bash=5.3-1ubuntu1`

Binary Packages:

- `bash=5.3-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `BSD-4-clause-UC`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `Latex2e`
- `MIT-like`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris bash=5.3-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.3-1ubuntu1.dsc' bash_5.3-1ubuntu1.dsc 2072 SHA512:0e9bf07ed7528c4dc660d44d64942567dd4ea62b05525b78e906a5b2a623051d2c3312c446cd338cda496fb79191bfbe44630d5e9836be2fcefebf4c4028a559
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.3.orig.tar.xz' bash_5.3.orig.tar.xz 5571836 SHA512:79a1800b6b579a1cc4247c67fc2aceed9a7197f2ea91a3528365297eee1b20a860af27d6d8cadc3c4a3c91a9f8ac9e04c34d7a5e80b605e1252adffedd26e932
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.3-1ubuntu1.debian.tar.xz' bash_5.3-1ubuntu1.debian.tar.xz 96008 SHA512:3621ed62eb49c9ba6415003942805ccbdd6c4a0448d59d6a7b569b9ba1c8446babed51e1484821237ebcae81cf8fefd6e202df7a7eaad14fa1ded11e138d96ff
```

### `dpkg` source package: `binutils=2.46-1ubuntu1`

Binary Packages:

- `binutils=2.46-1ubuntu1`
- `binutils-common:amd64=2.46-1ubuntu1`
- `binutils-x86-64-linux-gnu=2.46-1ubuntu1`
- `libbinutils:amd64=2.46-1ubuntu1`
- `libctf-nobfd0:amd64=2.46-1ubuntu1`
- `libctf0:amd64=2.46-1ubuntu1`
- `libgprofng0:amd64=2.46-1ubuntu1`
- `libsframe3:amd64=2.46-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe3/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.46-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.46-1ubuntu1.dsc' binutils_2.46-1ubuntu1.dsc 9064 SHA512:b16aed586fdb141163747dba315c500bb1844e2dd3630150ad7dc8a3b02da5e2bfa5f776d32a9b951be44630f868abfacdcd3faba500ecfb16717fa06dcb4025
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.46.orig.tar.xz' binutils_2.46.orig.tar.xz 29830224 SHA512:20540d217cd57c53bc51151046b3e406ee75b80917c9b0b6c37aafaf61702ea4caec533b5554f4dea12e6e211452a6adbaa02004fec12c56e0ef31028acc427a
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.46-1ubuntu1.debian.tar.xz' binutils_2.46-1ubuntu1.debian.tar.xz 135728 SHA512:4567a3a61e7e40d57c3023adb74946090eeadd5fa358361c73e1adfc8c9945d2963bda0144694449ae0d58aca04d5000c1f232eab869303b81aac29b9a114388
```

### `dpkg` source package: `brotli=1.2.0-3`

Binary Packages:

- `libbrotli-dev:amd64=1.2.0-3`
- `libbrotli1:amd64=1.2.0-3`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.2.0-3
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.2.0-3.dsc' brotli_1.2.0-3.dsc 2282 SHA512:21fe8c94dc028383956dcef999adf20dadecabf870cf300ac5609f6215a138112ab7d023619c620b138ac9c3cea7fdf7844633f952da94f7eb82b01ae54f75fb
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.2.0.orig.tar.gz' brotli_1.2.0.orig.tar.gz 646398 SHA512:ceb2a1a5661296885a2f67bd2d6b02ad467cdc5fb39a82ec8e5fde26633ef4df354ebf7491c8442b090cdd38dc607857c4f9bee8aebb8ff63d44ae7322faceae
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.2.0-3.debian.tar.xz' brotli_1.2.0-3.debian.tar.xz 5896 SHA512:487698ab1f4da26d51788e0a836f801d25dfcde52b313433384a2ee8d40e05eb5190465dd1a14d72e91e8959b509b5d735568ce2cc7a10150eca540c2661a429
```

### `dpkg` source package: `bzip2=1.0.8-6build2`

Binary Packages:

- `bzip2=1.0.8-6build2`
- `libbz2-1.0:amd64=1.0.8-6build2`
- `libbz2-dev:amd64=1.0.8-6build2`

Licenses: (parsed from: `/usr/share/doc/bzip2/copyright`, `/usr/share/doc/libbz2-1.0/copyright`, `/usr/share/doc/libbz2-dev/copyright`)

- `BSD-variant`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.8-6build2
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6build2.dsc' bzip2_1.0.8-6build2.dsc 2205 SHA512:e8422344d455bce7894722f57089c62ca441fec37a69e33c6444b05eb141ad6ed74dc6a86dd8d637d98f31ac2111900a113c29d7062687a4c7db07bb53b9eb7c
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8.orig.tar.gz' bzip2_1.0.8.orig.tar.gz 810029 SHA512:083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3
'http://archive.ubuntu.com/ubuntu/pool/main/b/bzip2/bzip2_1.0.8-6build2.debian.tar.bz2' bzip2_1.0.8-6build2.debian.tar.bz2 27136 SHA512:a7efd355101eb9751a90ad9d0d068a105f5ead3d69faa85074c31bb2ca61e7892270d40c476167814942765e7401b137a580d3eea5f2b67e0f6fefd309eb3072
```

### `dpkg` source package: `ca-certificates=20250419`

Binary Packages:

- `ca-certificates=20250419`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20250419
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20250419.dsc' ca-certificates_20250419.dsc 1766 SHA512:a23a4c3bda0d9d16cf5575044d58b5dcee545e164cf455e31522927738dcf62cbccb8ff0520afdd36d53b22cff824388c492bcf85ebf28a9c5a35e8fcdafd745
'http://archive.ubuntu.com/ubuntu/pool/main/c/ca-certificates/ca-certificates_20250419.tar.xz' ca-certificates_20250419.tar.xz 277504 SHA512:5a66a4aabbc18bce752b9e2d362309812cb685e24c0bb52cbb04cde3284b023034955c0ba8c9a3fa065392ab8372d166e6cb17b82fb336cb485e2b63485e9631
```

### `dpkg` source package: `cairo=1.18.4-3`

Binary Packages:

- `libcairo2:amd64=1.18.4-3`

Licenses: (parsed from: `/usr/share/doc/libcairo2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris cairo=1.18.4-3
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.4-3.dsc' cairo_1.18.4-3.dsc 2784 SHA512:e7812a44247ec018fd06a35ae4743c0f6bf5264823e977d6310546e3b23ba949528b559a5ed0a8fe21432ad7c29251929a2ee63f58a3ff8c1df6cc0b316a7218
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.4.orig.tar.xz' cairo_1.18.4.orig.tar.xz 32578804 SHA512:863679f817ed67dc2c916c035d740916e27e7e69c04fca63936e37d274e7f4c79848d16c8f7c481798864602e8847c489f698df89b785cbc576c925dbd513316
'http://archive.ubuntu.com/ubuntu/pool/main/c/cairo/cairo_1.18.4-3.debian.tar.xz' cairo_1.18.4-3.debian.tar.xz 29988 SHA512:be2227bc8df8de7081e6b2162595d11210629510b6916d405af47a2a90a21882991bfd4e06d061935ef05de213a2c0eaeac2be5ba1560435f05db641d013c441
```

### `dpkg` source package: `cdebconf=0.280ubuntu1`

Binary Packages:

- `libdebconfclient0:amd64=0.280ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdebconfclient0/copyright`)

- `BSD-2-Clause`
- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris cdebconf=0.280ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.280ubuntu1.dsc' cdebconf_0.280ubuntu1.dsc 2873 SHA512:bd0f7dd6a9e3b19040f726c966775955569f29c4f63c1a6680549a42f8bd591a93574346f0dba3fd5f46f60b2cbe75d77422fa09e85e908c1ea6a83b390ef1a9
'http://archive.ubuntu.com/ubuntu/pool/main/c/cdebconf/cdebconf_0.280ubuntu1.tar.xz' cdebconf_0.280ubuntu1.tar.xz 287352 SHA512:24bb2f3083730194bf76ecf9039d92429550e5e3f52aa417ae628b9805433b42227e56941671d7c549f86c0302c43c22e3b62b3d01d609b6f79869e3e2ef53d7
```

### `dpkg` source package: `coreutils-from=0.0.0~ubuntu24`

Binary Packages:

- `coreutils=9.5-1ubuntu2+0.0.0~ubuntu24`
- `coreutils-from-uutils=0.0.0~ubuntu24`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`, `/usr/share/doc/coreutils-from-uutils/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris coreutils-from=0.0.0~ubuntu24
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu24.dsc' coreutils-from_0.0.0~ubuntu24.dsc 1966 SHA512:2e03843c71f35a5e24b63b81f4cf203558d1c59fe7fad42ab13173737281829e9e4cd1b4840349dc2d28726008223655700123c8b0beb490ecdb5028336a6c36
'http://archive.ubuntu.com/ubuntu/pool/main/c/coreutils-from/coreutils-from_0.0.0%7eubuntu24.tar.xz' coreutils-from_0.0.0~ubuntu24.tar.xz 7384 SHA512:2841b9435326c202e040b260ebf067ea13d922ec498adc837a8f33ba50a7b0f0afe8682acebeb534e083f932adb71ac66895db8a3afd2bc72d945d2b81c0a5ac
```

### `dpkg` source package: `coreutils=9.7-3ubuntu1`

Binary Packages:

- `gnu-coreutils=9.7-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gnu-coreutils/copyright`)

- `BSD-4-clause-UC`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-3`
- `GPL-3+`
- `ISC`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `curl=8.18.0-1ubuntu1`

Binary Packages:

- `curl=8.18.0-1ubuntu1`
- `libcurl3t64-gnutls:amd64=8.18.0-1ubuntu1`
- `libcurl4-openssl-dev:amd64=8.18.0-1ubuntu1`
- `libcurl4t64:amd64=8.18.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3t64-gnutls/copyright`, `/usr/share/doc/libcurl4-openssl-dev/copyright`, `/usr/share/doc/libcurl4t64/copyright`)

- `BSD-4-Clause-UC`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+ with Autoconf-data exception`
- `GPL-2+ with Libtool exception`
- `GPL-3+ with Autoconf-data exception`
- `ISC`
- `OLDAP-2.8`
- `X11`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris curl=8.18.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.18.0-1ubuntu1.dsc' curl_8.18.0-1ubuntu1.dsc 3260 SHA512:d3e815903b5eae81212997338133cacbd601a5e7038e99a7405b2d520150fa353d11209ed66b81b1fadc74780a7d8a4257a1e2484197698973ebb8eeecbf71c9
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.18.0.orig.tar.gz' curl_8.18.0.orig.tar.gz 4182005 SHA512:84f193f28369ccb7fba0d8933cfc24f5fbb282b046e7e8c2c1a0da35db8ec13d17e6407c240ce3a12cf4dccac62e5919bd98f3add77065408c6259cfe1071575
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.18.0.orig.tar.gz.asc' curl_8.18.0.orig.tar.gz.asc 488 SHA512:fd31f4ff1dcb6c13f200cc67639b3760e6c47bead73f53f8700d3387792b57c8abe60e23f27d15d3ff9197490aa549e5c9910b271294cc3f75f4b37dc3c9af0c
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.18.0-1ubuntu1.debian.tar.xz' curl_8.18.0-1ubuntu1.debian.tar.xz 55344 SHA512:2c66ace76ac787f40f6f35806558a5b0b6a489e1fed5103158f144d4534f8b66a06eac6cdc7c7c44c5792db70b833b92629cc4ef790b3b1af76442edb0ada23e
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-9ubuntu1`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-9ubuntu1`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-2-clause`
- `BSD-2.2-clause`
- `BSD-3-Clause-Attribution`
- `BSD-3-clause`
- `BSD-3-clause-JANET`
- `BSD-3-clause-PADL`
- `BSD-4-clause-UC`
- `FSFULLR`
- `GPL-3`
- `GPL-3+`
- `IBM-as-is`
- `MIT-CMU`
- `MIT-Export`
- `MIT-OpenVision`
- `OpenLDAP`
- `RSA-MD`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-9ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9ubuntu1.dsc' cyrus-sasl2_2.1.28+dfsg1-9ubuntu1.dsc 3583 SHA512:68941067eed1b29cc03e6d006c93bffc3c22d9e074e78b97dee825b12fef26d52f88c73cf3e52cebefb46942c6151766156f0a9a8c6ad6e654f532fae3808d7e
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA512:e94075d09b38a50138b782323de286deb7b15008064f07df4fa682e94367e829d9bfafef48d5478f730fef8fde536bcc6d54cab0452b76473a3c620b3dc18fa2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9ubuntu1.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-9ubuntu1.debian.tar.xz 99304 SHA512:cf638d3bf7111761818d7abfcbbcd33d5a4214b1a0030b000996052c400d5560690d6b93d0b4502c7bb406d1d83686747600e0a84101ff8bced0740ba8ff3307
```

### `dpkg` source package: `dash=0.5.12-12ubuntu2`

Binary Packages:

- `dash=0.5.12-12ubuntu2`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `db-defaults=1:5.3.21ubuntu4`

Binary Packages:

- `libdb-dev:amd64=1:5.3.21ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libdb-dev/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris db-defaults=1:5.3.21ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu4.dsc' db-defaults_5.3.21ubuntu4.dsc 1619 SHA512:5bfc537d793b41008adef1d964f22d3517c66820d3b007984ad541e8a69235f3250c6f597922127b42ecef450579314f6c8055dbd04ccb509aeb662eb2158a21
'http://archive.ubuntu.com/ubuntu/pool/main/d/db-defaults/db-defaults_5.3.21ubuntu4.tar.xz' db-defaults_5.3.21ubuntu4.tar.xz 2896 SHA512:6314f039a0cd290dc030fc62dbcda70154bf44e60b28e60a3843708aa6806037466c30da165b1c02ac3e371d0e8e1dc6470c1021457ab1e10ffd58014ebff800
```

### `dpkg` source package: `db5.3=5.3.28+dfsg2-10ubuntu1`

Binary Packages:

- `libdb5.3-dev=5.3.28+dfsg2-10ubuntu1`
- `libdb5.3t64:amd64=5.3.28+dfsg2-10ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdb5.3-dev/copyright`, `/usr/share/doc/libdb5.3t64/copyright`)

- `Artistic`
- `BSD-3-clause`
- `BSD-3-clause-fjord`
- `GPL`
- `GPL-3`
- `MIT-old`
- `Ms-PL`
- `Sleepycat`
- `TCL-like`
- `X11`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28+dfsg2-10ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-10ubuntu1.dsc' db5.3_5.3.28+dfsg2-10ubuntu1.dsc 2484 SHA512:3767fbb8ada0b2aa00a107e6b6f2eb06ec9bf0fbb20f7a22645098ec5f52fae5930e359f119c09116ed6eab2f46734ec80ddbbbdd60cf675bf17ed2116a9d81b
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2.orig.tar.xz' db5.3_5.3.28+dfsg2.orig.tar.xz 21287688 SHA512:f9c9d042702ef3fcfdd4b4859583048f3396b161009dc24b6d3a2c53533d58214239fc80e2c42db17e9f092df44d531502737f3b368b956bff49ef057b6b51ef
'http://archive.ubuntu.com/ubuntu/pool/main/d/db5.3/db5.3_5.3.28%2bdfsg2-10ubuntu1.debian.tar.xz' db5.3_5.3.28+dfsg2-10ubuntu1.debian.tar.xz 36572 SHA512:3c8afc4f013a54d163f90c26ba6a616f4e95ce0f3f40d328d6602498adfa6a691e6a44d2f32f5467712a2ee3566b5315a05f44e68792d9d4d5b835bf810114b9
```

### `dpkg` source package: `debconf=1.5.91`

Binary Packages:

- `debconf=1.5.91`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.91
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.91.dsc' debconf_1.5.91.dsc 2035 SHA512:523a2aedd2925d7417f166daf896176225733d4f308959b7dbec80f4d8e9a177fb6b6d282297a7f8da13b50afadeda6210c095dd6cd75dfd41f6ffdef90a1c9f
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.91.tar.xz' debconf_1.5.91.tar.xz 609964 SHA512:3c79aec120e660d0e74ae6a35747818a555172685d1258fff3c6622abe795858779159440f39bcf641955c335a07de8386cf0d0518cdae8193fe4f28d8492df8
```

### `dpkg` source package: `debianutils=5.23.2`

Binary Packages:

- `debianutils=5.23.2`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/debianutils/5.23.2/


### `dpkg` source package: `diffutils=1:3.12-1`

Binary Packages:

- `diffutils=1:3.12-1`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `FSFAP`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with autoconf exception`
- `GPL-3+ with texinfo exception`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3.0+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.12-1
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.12-1.dsc' diffutils_3.12-1.dsc 1875 SHA512:1560e462c0645f104cb7e37e1c6d82d0de0f7cd0a31ea5676d3604dbcdbb4ecd325123057ce96b6da3b7d2218a49fc9392528893321920b81c37f325ed710735
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.12.orig.tar.xz' diffutils_3.12.orig.tar.xz 1938800 SHA512:10b17cf1dcdfa9ca0e5db91d62c4a079ebe9fd7eafa3aaebd4eb7e6206e4d753f348496622aa281e1bd7f7fcde65ce4a886dcc4acbb59332ef980f224197b4e4
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.12.orig.tar.xz.asc' diffutils_3.12.orig.tar.xz.asc 833 SHA512:8eb59b40156741fbfcac947f29f76aa0eefb9c8f819206cab9474da0ffe0154c6aa8b38435eccdd82ceb8c3565a6c548e8d2a0f771f1e8e1af15635854ec9c62
'http://archive.ubuntu.com/ubuntu/pool/main/d/diffutils/diffutils_3.12-1.debian.tar.xz' diffutils_3.12-1.debian.tar.xz 14752 SHA512:e2054eac9f98935f28d8335e2d06ac7ee55bf9d1f0ea0d4ff0eed2efe2e2cb2e717d732f04a6197027a8146e78931cc13bbb96dc3223cbdecb4e259549125515
```

### `dpkg` source package: `djvulibre=3.5.29-1`

Binary Packages:

- `libdjvulibre-dev:amd64=3.5.29-1`
- `libdjvulibre-text=3.5.29-1`
- `libdjvulibre21:amd64=3.5.29-1`

Licenses: (parsed from: `/usr/share/doc/libdjvulibre-dev/copyright`, `/usr/share/doc/libdjvulibre-text/copyright`, `/usr/share/doc/libdjvulibre21/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris djvulibre=3.5.29-1
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.29-1.dsc' djvulibre_3.5.29-1.dsc 2389 SHA512:2addf124bbfc05bcfc21dfae644ac35f38198133c4dec5a00dc572b064d0729c13afb36d7459bdc89af82050af4effb01e3cd698fc46633c16440c093a8f4463
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.29.orig.tar.xz' djvulibre_3.5.29.orig.tar.xz 3214548 SHA512:e8f4631f29ee20fefea7abc92aed09b658a4abea4821d1fad534156679c0fd3736e2bedd26dc5d9360061be9629a76ae00aca57054256edb33afa53dbb13b987
'http://archive.ubuntu.com/ubuntu/pool/main/d/djvulibre/djvulibre_3.5.29-1.debian.tar.xz' djvulibre_3.5.29-1.debian.tar.xz 16780 SHA512:3180f3d9bc8fe344fd94429accd72eb89c151ed8e94ed8fcda7514f121efc84d9235313673b5c2dd8422503a7a36fb97ff74053a8add754591897cf64080741c
```

### `dpkg` source package: `dpkg=1.22.21ubuntu5`

Binary Packages:

- `dpkg=1.22.21ubuntu5`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `dpkg=1.22.21ubuntu9`

Binary Packages:

- `dpkg-dev=1.22.21ubuntu9`
- `libdpkg-perl=1.22.21ubuntu9`

Licenses: (parsed from: `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.22.21ubuntu9
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.21ubuntu9.dsc' dpkg_1.22.21ubuntu9.dsc 3457 SHA512:5df36c1f3e1c3cfbb17cd6c4acca49794ffa7ef8bd3d08960b1a1ceb6209f1f74fe635c51d810d118368f20347015526b79dd645585e604c344ada24532ab8ee
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.22.21ubuntu9.tar.xz' dpkg_1.22.21ubuntu9.tar.xz 5674884 SHA512:515b722132d28807dabdd3cf890d85fdf6931d9139179597e779ef353a682733bfeeb5b7b80652234889503718134a8a4936757b4a31382e0bcc126d3eed5c0c
```

### `dpkg` source package: `e2fsprogs=1.47.2-3ubuntu2`

Binary Packages:

- `comerr-dev:amd64=2.1-1.47.2-3ubuntu2`
- `e2fsprogs=1.47.2-3ubuntu2`
- `libcom-err2:amd64=1.47.2-3ubuntu2`
- `libext2fs2t64:amd64=1.47.2-3ubuntu2`
- `libss2:amd64=1.47.2-3ubuntu2`
- `logsave=1.47.2-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/comerr-dev/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcom-err2/copyright`, `/usr/share/doc/libext2fs2t64/copyright`, `/usr/share/doc/libss2/copyright`, `/usr/share/doc/logsave/copyright`)

- `0BSD`
- `Apache-2`
- `Apache-2.0`
- `BSD-3-Clause`
- `BSD-3-Clause-Variant`
- `BSD-4-Clause-CMU`
- `Expat`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Texinfo exception`
- `ISC`
- `Kazlib`
- `LGPL-2`
- `Latex2e`
- `MIT-US-export`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3ubuntu2.dsc' e2fsprogs_1.47.2-3ubuntu2.dsc 3292 SHA512:8a406035cf48048d701fb111a2b005be8e6a2844f0ab6f45730c992bd69b54039fdfacc6a23254728b0c980215c25cf415e2fdc322416e0767c4d60e5532d905
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA512:dd89139c5e2bf999a22d999686ef06ab42f6ad537c6aeaa3fe68d9734d734b7396fd7ab2fd8002be26860c5653991a666d0df06c804c2f1f07f1274468ec728f
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA512:a22d46cc37497861d5a7e50076b40b8be6f459790f6eaacf0446200776fb74492ca9bfc7abc19edda3c9f7f722c318827b02f9cfbbb2118a8e86bce4d446d56b
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3ubuntu2.debian.tar.xz' e2fsprogs_1.47.2-3ubuntu2.debian.tar.xz 105644 SHA512:8e4ad2ba2648b6a59682a2330e03d08fe60c14bc42ccacd65d433a2d97fdd3a4c17445b93ab262cd760d53820b5c06bd1d16cf682de4a635a7ed787d00e75adf
```

### `dpkg` source package: `elfutils=0.194-1`

Binary Packages:

- `libelf1t64:amd64=0.194-1`

Licenses: (parsed from: `/usr/share/doc/libelf1t64/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris elfutils=0.194-1
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.194-1.dsc' elfutils_0.194-1.dsc 3317 SHA512:4d9877804f434ba81855b4416d8761575f073bef91e971d1558ad1e196fd8552e4ccd11d8100aa25a83c68c8e32f197160d21e4ab8fba893a95f25ae3f180e07
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.194.orig.tar.bz2' elfutils_0.194.orig.tar.bz2 12003321 SHA512:5d00502f61b92643bf61dc61da4ddded36c423466388d992bcd388c5208761b8ed9db1a01492c085cd0984eef30c08f895a8e307e78e0df8df40b56ae35b78a5
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.194-1.debian.tar.xz' elfutils_0.194-1.debian.tar.xz 44252 SHA512:f9313bac391509d3a637e0ac5ed03e466f1818e60c825d0d1052679badb449be7bf690a9f48b13728f4f62e3123244e7ef3a36dc50389514aa3540def4f22db9
```

### `dpkg` source package: `expat=2.7.4-1`

Binary Packages:

- `libexpat1:amd64=2.7.4-1`

Licenses: (parsed from: `/usr/share/doc/libexpat1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris expat=2.7.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.4-1.dsc' expat_2.7.4-1.dsc 1970 SHA512:d91b4c705d09f5b510b69b9694e95fa8d59bcce5e655ea7dc3eaedc5f4b97aa8397f96d3cb7a920123cb3a2c377565872dc55ae441c72b1d06dcbbc64e11ebdb
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.4.orig.tar.gz' expat_2.7.4.orig.tar.gz 8448897 SHA512:0e157ce875ec993b4e495e0cd04979109c1f0f0dbfa707c113d9b4ed243c668fce20e5ef79ff8df2f30587cc182a0254794b2fb9bb53f938da608ace32903820
'http://archive.ubuntu.com/ubuntu/pool/main/e/expat/expat_2.7.4-1.debian.tar.xz' expat_2.7.4-1.debian.tar.xz 13420 SHA512:17f1ac9cb2ddc126bcaeb7b2a9d1051211f13ab094fe83aad1fb2af5fc6988d9fc58a57fba8223221e8981071d24facead83421312206a5b5ed01e6cef369d5f
```

### `dpkg` source package: `fftw3=3.3.10-2fakesync1build3`

Binary Packages:

- `libfftw3-bin=3.3.10-2fakesync1build3`
- `libfftw3-dev:amd64=3.3.10-2fakesync1build3`
- `libfftw3-double3:amd64=3.3.10-2fakesync1build3`
- `libfftw3-long3:amd64=3.3.10-2fakesync1build3`
- `libfftw3-quad3:amd64=3.3.10-2fakesync1build3`
- `libfftw3-single3:amd64=3.3.10-2fakesync1build3`

Licenses: (parsed from: `/usr/share/doc/libfftw3-bin/copyright`, `/usr/share/doc/libfftw3-dev/copyright`, `/usr/share/doc/libfftw3-double3/copyright`, `/usr/share/doc/libfftw3-long3/copyright`, `/usr/share/doc/libfftw3-quad3/copyright`, `/usr/share/doc/libfftw3-single3/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris fftw3=3.3.10-2fakesync1build3
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-2fakesync1build3.dsc' fftw3_3.3.10-2fakesync1build3.dsc 2893 SHA512:7e435e30ad81b9b202b80eb229dd70f3ab5749ccff3fa67ceac4e1ff91f06f28f8cf856ff8c6283245703752244a6e6cea11d48062135ec7dcb3f01dda19f1f0
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10.orig.tar.gz' fftw3_3.3.10.orig.tar.gz 4262403 SHA512:fa2ea740449fd06c833a82e1fff82bacd554188d500cbedff5a0bc185551799ef9ef9b8b1c227283abdbbdd185424d19df9c0f06ed88d5fe3d9c001d6fab6109
'http://archive.ubuntu.com/ubuntu/pool/main/f/fftw3/fftw3_3.3.10-2fakesync1build3.debian.tar.xz' fftw3_3.3.10-2fakesync1build3.debian.tar.xz 14896 SHA512:20b6c10041a0ce1fbe4306c00250c262674eb93c519c4cf22117fe5363355cbc684137240fdb961c8eb0b29773fe128bdd6cc0c7193f2a88a379c736c32f7669
```

### `dpkg` source package: `file=1:5.46-5build1`

Binary Packages:

- `file=1:5.46-5build1`
- `libmagic-mgc=1:5.46-5build1`
- `libmagic1t64:amd64=1:5.46-5build1`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1t64/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris file=1:5.46-5build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46-5build1.dsc' file_5.46-5build1.dsc 2292 SHA512:3a7c29f9b78adda5049a56ec26f03679a51ba974bc36be0f7de8ff3eee33b933584840203b6923a79ab3a92a3d0e8eb17a64d6ea46c9d8991472c50c13291e7e
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46.orig.tar.gz' file_5.46.orig.tar.gz 1312892 SHA512:a6cb7325c49fd4af159b7555bdd38149e48a5097207acbe5e36deb5b7493ad6ea94d703da6e0edece5bb32959581741f4213707e5cb0528cd46d75a97a5242dc
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46.orig.tar.gz.asc' file_5.46.orig.tar.gz.asc 201 SHA512:a6e6fe92d909a9b153c88828942c2963b3b683cda5f6d7ae281e4ca42b30a582e82094b182976515ee85689200b8f6512d34b7f39291cbf9623d583ce688530a
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46-5build1.debian.tar.xz' file_5.46-5build1.debian.tar.xz 37088 SHA512:16a41aec0f608438508a9d3ddb67eef430e3bd8ed874b0dc8e03b07c84d15d2653a21b9a450f872b70b9925383ca8897e7eccbbdd5bd0a5dae87c3700e57cfe2
```

### `dpkg` source package: `findutils=4.10.0-3build1`

Binary Packages:

- `findutils=4.10.0-3build1`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `BSD-3-clause`
- `FSFAP`
- `FSFULLR`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL`
- `GPL with automake exception`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf-data exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-data exception`
- `GPL-3+ with Bison-2.2 exception`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `fontconfig=2.17.1-3ubuntu1`

Binary Packages:

- `fontconfig=2.17.1-3ubuntu1`
- `fontconfig-config=2.17.1-3ubuntu1`
- `libfontconfig1:amd64=2.17.1-3ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris fontconfig=2.17.1-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.17.1-3ubuntu1.dsc' fontconfig_2.17.1-3ubuntu1.dsc 2751 SHA512:146870db67e2fccd3ba24c359d78b941c02eb18e43e043f58c1c091f8c336a470c9dc861de92f6288a74817c91572f06bc04310155d4eab300f7c4268d0f274d
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.17.1.orig.tar.gz' fontconfig_2.17.1.orig.tar.gz 622045 SHA512:2a2df9b28cbb4952db7b2dab28ac969435afa7d162b6f888169a3908a41b4134bb9710fc08984fb8a30c39314fb813e1598f002e1efa207b5d5b19d37bed9d3c
'http://archive.ubuntu.com/ubuntu/pool/main/f/fontconfig/fontconfig_2.17.1-3ubuntu1.debian.tar.xz' fontconfig_2.17.1-3ubuntu1.debian.tar.xz 31920 SHA512:78e51f228ee3060df8685824c36c1276ff0019247ea9b33b28c251c3a84c7125e2ab78b93d229dc256b6368f09012e9155a940dd08a1befb869d2dba2aab08d1
```

### `dpkg` source package: `fonts-dejavu=2.37-8build1`

Binary Packages:

- `fonts-dejavu-core=2.37-8build1`
- `fonts-dejavu-mono=2.37-8build1`

Licenses: (parsed from: `/usr/share/doc/fonts-dejavu-core/copyright`, `/usr/share/doc/fonts-dejavu-mono/copyright`)

- `GPL-2`
- `GPL-2+`
- `bitstream-vera`

Source:

```console
$ apt-get source -qq --print-uris fonts-dejavu=2.37-8build1
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8build1.dsc' fonts-dejavu_2.37-8build1.dsc 2525 SHA512:523808cab1406990639689414f663eeea764764c225e753212a2e171d747bb6e2d3312b50bd5a7e5e6cb1f2a979327f07e487b356638656ba24cfa135da2ea79
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37.orig.tar.bz2' fonts-dejavu_2.37.orig.tar.bz2 12050109 SHA512:e61fc8c675ef76edb49dd9a8caee62087280929bb8144b52aca2f8def30025c56246589ad8a6a806b9574e6876eedd16d57c70a6ce9c86817a2dfe39d8a2bb2b
'http://archive.ubuntu.com/ubuntu/pool/main/f/fonts-dejavu/fonts-dejavu_2.37-8build1.debian.tar.xz' fonts-dejavu_2.37-8build1.debian.tar.xz 13244 SHA512:dd31959839baff4aedc0696a7d5bd72c9476896bd5badec0fcac5ac6a3924a6abc122c023122bf63036b7ca0ba62026366b89bcab9d325679f800463dfab4fef
```

### `dpkg` source package: `freetype=2.14.1+dfsg-2`

Binary Packages:

- `libfreetype-dev:amd64=2.14.1+dfsg-2`
- `libfreetype6:amd64=2.14.1+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libfreetype-dev/copyright`, `/usr/share/doc/libfreetype6/copyright`)

- `BSD-3-Clause`
- `BSL-1.0`
- `Expat`
- `FSFAP`
- `FTL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `MIT-Modern-Variant`
- `MIT-SMC`
- `OpenGroup-MIT`
- `Public-Domain`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris freetype=2.14.1+dfsg-2
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.1%2bdfsg-2.dsc' freetype_2.14.1+dfsg-2.dsc 3732 SHA512:3958aaa31e17fa564edbcfb57241c1ceea45eb6b4cbecdcf6d830452f803cfcf566c294e7711e532d60ebfff081c45e663cc6dda9cbfae2dc1c47910e5e6b51f
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.1%2bdfsg.orig-ft2demos.tar.xz' freetype_2.14.1+dfsg.orig-ft2demos.tar.xz 344228 SHA512:a6240e888807c6171f8ee5d14578f83902cb495e6e911e5fd7c17628025310a60b0dfe5cd6c6e8803d3460eacd534d7f21c6c598081934d609575e182a312877
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.1%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.14.1+dfsg.orig-ft2demos.tar.xz.asc 833 SHA512:86ba1530f510fcf9c088f598d5c038b537844dfa5faa5a8b69ece497b1ced61bd56af566b2563f63c74af56229db9e1357b924697b8a6cf77a5f88e5f98912f4
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.1%2bdfsg.orig-ft2docs.tar.xz' freetype_2.14.1+dfsg.orig-ft2docs.tar.xz 2175972 SHA512:a2e0901863d59c59ff4d1ded1c2000ddaa5cf21c3ea5fdf74e8bfecee56f8cf954628d0abd7440e9c1a3ebe23801138737e297809f403574304c41231f0fb962
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.1%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.14.1+dfsg.orig-ft2docs.tar.xz.asc 833 SHA512:15ad91d610b19823a1a379f86632a0d42764a49082aaef0eee15fa9e2df70e26b8c48e2f812eadda54ef2b5b3a4f795a979c1534ced7d6b29974335d14daab98
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.1%2bdfsg.orig.tar.xz' freetype_2.14.1+dfsg.orig.tar.xz 2247228 SHA512:df9ae0bb4804cf57b343e69621f253c5e0bb55ad3ba329ca82d7b13f8cc0310459d702d9d6706e8e619543be12f2f56c0367ccaaf3858faf4d13d2a5f33364c9
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.1%2bdfsg-2.debian.tar.xz' freetype_2.14.1+dfsg-2.debian.tar.xz 43904 SHA512:d4636223f6f5ad482ecee290f766d1fc939b4ea868e82b39a5e13fd818a0b4f56c823bb5b232d845067bf42930ed1ca1f19a38b4249611510b4b2b32c43f03e8
```

### `dpkg` source package: `fribidi=1.0.16-5`

Binary Packages:

- `libfribidi0:amd64=1.0.16-5`

Licenses: (parsed from: `/usr/share/doc/libfribidi0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris fribidi=1.0.16-5
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.16-5.dsc' fribidi_1.0.16-5.dsc 2014 SHA512:1a2442a7a3a9366e50de61af99e22a9e083537ac769e874d2feb41c955dd4b1a3203d2415353c0f2b55aa1d816f1fd58a18a9c1cc216a982617ece221a66a50b
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.16.orig.tar.xz' fribidi_1.0.16.orig.tar.xz 1098260 SHA512:e3a56f36155f6813e3609473639fc533de742309f561c463012dc90b412a1ac7694b765d92669b2cbfaee973ca0e92fa5e926e68a1a078921f26ef17d82ab651
'http://archive.ubuntu.com/ubuntu/pool/main/f/fribidi/fribidi_1.0.16-5.debian.tar.xz' fribidi_1.0.16-5.debian.tar.xz 9052 SHA512:de65575306f5f72a052e1276a06ed1dda56b192b3a8e141abc8730e3bc59a140b68134f09911ea665d838bb04d7a58d4a492472ba7cf4c967df9aa9748a1e3c6
```

### `dpkg` source package: `gcc-15=15.2.0-12ubuntu1`

Binary Packages:

- `cpp-15=15.2.0-12ubuntu1`
- `cpp-15-x86-64-linux-gnu=15.2.0-12ubuntu1`
- `g++-15=15.2.0-12ubuntu1`
- `g++-15-x86-64-linux-gnu=15.2.0-12ubuntu1`
- `gcc-15=15.2.0-12ubuntu1`
- `gcc-15-base:amd64=15.2.0-12ubuntu1`
- `gcc-15-x86-64-linux-gnu=15.2.0-12ubuntu1`
- `libgcc-15-dev:amd64=15.2.0-12ubuntu1`
- `libstdc++-15-dev:amd64=15.2.0-12ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp-15/copyright`, `/usr/share/doc/cpp-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-15/copyright`, `/usr/share/doc/g++-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-15/copyright`, `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/gcc-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/libgcc-15-dev/copyright`, `/usr/share/doc/libstdc++-15-dev/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-15=15.2.0-12ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0-12ubuntu1.dsc' gcc-15_15.2.0-12ubuntu1.dsc 52487 SHA512:d2013902f805431de3b03f00fc1bab420cb014b03a7f46f24b3b58f86df786c3e47c684f78b29cb296af15e20e8e75d02fac10788f0e397434b50f18a7d7d88c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0.orig.tar.gz' gcc-15_15.2.0.orig.tar.gz 105962230 SHA512:83887af5c7798105d1ad85f0e9c794daa3cf030638bf40b3bff48771b8325d95c9a0d99d7d2c86c8e45499ff87f975e1914d00b72482862357645cc7ec330d38
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0-12ubuntu1.debian.tar.xz' gcc-15_15.2.0-12ubuntu1.debian.tar.xz 2876412 SHA512:ac55144a2f32a4f78b02be81000aed89a2d9a184f2ac93b5e22694456333c57590a7e87f7f90d43df4acc0cb0cfe0e5a672d57c539c2597daf1d60ef0e6c40b3
```

### `dpkg` source package: `gcc-16=16-20260210-0ubuntu1`

Binary Packages:

- `gcc-16-base:amd64=16-20260210-0ubuntu1`
- `libasan8:amd64=16-20260210-0ubuntu1`
- `libatomic1:amd64=16-20260210-0ubuntu1`
- `libcc1-0:amd64=16-20260210-0ubuntu1`
- `libgcc-s1:amd64=16-20260210-0ubuntu1`
- `libgomp1:amd64=16-20260210-0ubuntu1`
- `libhwasan0:amd64=16-20260210-0ubuntu1`
- `libitm1:amd64=16-20260210-0ubuntu1`
- `liblsan0:amd64=16-20260210-0ubuntu1`
- `libquadmath0:amd64=16-20260210-0ubuntu1`
- `libstdc++6:amd64=16-20260210-0ubuntu1`
- `libtsan2:amd64=16-20260210-0ubuntu1`
- `libubsan1:amd64=16-20260210-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-16-base/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-16=16-20260210-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-16/gcc-16_16-20260210-0ubuntu1.dsc' gcc-16_16-20260210-0ubuntu1.dsc 52875 SHA512:c87be65defccbad06d869df7b1773cc9673ec082fea72eaab43d38289f7c81696497790f45a27f031136ddb149585f911446aebda34ee35434acc52a32c0df52
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-16/gcc-16_16-20260210.orig.tar.gz' gcc-16_16-20260210.orig.tar.gz 101390900 SHA512:58beec008e62ee103ce034adb5b520ea37ffd4ac4735b5d5d331ec3b9ae5e52bda2011a90a59eb32ec8d6e34d16ae4b36dbc16f59c33169ae5d72ff683e2f7e8
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-16/gcc-16_16-20260210-0ubuntu1.debian.tar.xz' gcc-16_16-20260210-0ubuntu1.debian.tar.xz 626964 SHA512:e1b6f152d6c9fae41e32e295273f84479feaebfd4004aed437be21acf4dcf55b0d2b10b5cf32c74332e108d7670c56292a1749c2c660c18bb3f78d0c1498a073
```

### `dpkg` source package: `gcc-defaults=1.229ubuntu1`

Binary Packages:

- `cpp=4:15.2.0-4ubuntu1`
- `cpp-x86-64-linux-gnu=4:15.2.0-4ubuntu1`
- `g++=4:15.2.0-4ubuntu1`
- `g++-x86-64-linux-gnu=4:15.2.0-4ubuntu1`
- `gcc=4:15.2.0-4ubuntu1`
- `gcc-x86-64-linux-gnu=4:15.2.0-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.229ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.229ubuntu1.dsc' gcc-defaults_1.229ubuntu1.dsc 38342 SHA512:814e39c4bb9a562e5c87b2c111c2b5af1ec641c0e5bfe84929c83bca9045859b73c900baa40ffc350515b6653142ba7e035cf0269a360adf163c2d8cbb3b9318
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.229ubuntu1.tar.xz' gcc-defaults_1.229ubuntu1.tar.xz 58296 SHA512:01038a0c30fd0fa724e08ec397361c2bf5b42040761508ff6297dc92ebe7b29eb8a0f8679b9e20128aebea78df77d325f2927343a4b7089dc49a3c8e92e5d892
```

### `dpkg` source package: `gdbm=1.26-1build1`

Binary Packages:

- `libgdbm-compat4t64:amd64=1.26-1build1`
- `libgdbm-dev:amd64=1.26-1build1`
- `libgdbm6t64:amd64=1.26-1build1`

Licenses: (parsed from: `/usr/share/doc/libgdbm-compat4t64/copyright`, `/usr/share/doc/libgdbm-dev/copyright`, `/usr/share/doc/libgdbm6t64/copyright`)

- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gdbm=1.26-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.26-1build1.dsc' gdbm_1.26-1build1.dsc 2258 SHA512:09891ef94fd16d1bd253657afd2a78811524a7b42a54ca50befa0500444c4c9c643aaa29ec9f6152265c35fc0cb8671fb2fd375b83291b50e78fc0509ea235a2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.26.orig.tar.gz' gdbm_1.26.orig.tar.gz 1226591 SHA512:44aafe254f0950a8f5215d8f1337674f07b19f2a375f6eb19a7e39690028c80c3774b705c2b76b470ae74042b21f2ca77d02f6f57aa2ee50296db801220a3352
'http://archive.ubuntu.com/ubuntu/pool/main/g/gdbm/gdbm_1.26-1build1.debian.tar.xz' gdbm_1.26-1build1.debian.tar.xz 16896 SHA512:81c243f1e1d6fcf4c8abdcc6f1c294863021a9c6ce8ff360c45ecc18357a1e21b6b3d89e530f7ba8c0e40aa9d85eb05d819941593ab3baffb3087c06a574bdee
```

### `dpkg` source package: `git=1:2.51.0-1ubuntu1`

Binary Packages:

- `git=1:2.51.0-1ubuntu1`
- `git-man=1:2.51.0-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/git/copyright`, `/usr/share/doc/git-man/copyright`)

- `Apache-2.0`
- `Artistic`
- `Artistic-1`
- `BSD-3-clause`
- `Boost`
- `EDL-1.0`
- `Expat`
- `GPL`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `dlmalloc`
- `mingw-runtime`

Source:

```console
$ apt-get source -qq --print-uris git=1:2.51.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.51.0-1ubuntu1.dsc' git_2.51.0-1ubuntu1.dsc 2656 SHA512:995c8ac6af4331625936708fb1f4309bf7349dfc8b5037566c6a54238131a95c52dc7518ac6c4628a1ad8dbeb078b4bb9e8c5c3585afbb6a37dc6eea9f89acfe
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.51.0.orig.tar.xz' git_2.51.0.orig.tar.xz 7857228 SHA512:2b8c59589266c0c9e58a9f4fda4a970a8a492e2e0ecbafc414fcfacac4a04251f0115b3676f4599a415b53906f1dea312b18a42e9bde455286abd62ec327beaf
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.51.0-1ubuntu1.debian.tar.xz' git_2.51.0-1ubuntu1.debian.tar.xz 821848 SHA512:e5f8451664c213ba067010d0fca4121da7a813be833fdc0606fc99306c4aade63784db63162f5bd167312d247778a4393a24a82cd850fd93b18ecade75382511
```

### `dpkg` source package: `glib2.0=2.87.2-3`

Binary Packages:

- `girepository-tools:amd64=2.87.2-3`
- `libgio-2.0-dev:amd64=2.87.2-3`
- `libgio-2.0-dev-bin=2.87.2-3`
- `libgirepository-2.0-0:amd64=2.87.2-3`
- `libglib2.0-0t64:amd64=2.87.2-3`
- `libglib2.0-bin=2.87.2-3`
- `libglib2.0-data=2.87.2-3`
- `libglib2.0-dev:amd64=2.87.2-3`
- `libglib2.0-dev-bin=2.87.2-3`

Licenses: (parsed from: `/usr/share/doc/girepository-tools/copyright`, `/usr/share/doc/libgio-2.0-dev/copyright`, `/usr/share/doc/libgio-2.0-dev-bin/copyright`, `/usr/share/doc/libgirepository-2.0-0/copyright`, `/usr/share/doc/libglib2.0-0t64/copyright`, `/usr/share/doc/libglib2.0-bin/copyright`, `/usr/share/doc/libglib2.0-data/copyright`, `/usr/share/doc/libglib2.0-dev/copyright`, `/usr/share/doc/libglib2.0-dev-bin/copyright`)

- `AFL-2.0`
- `Apache-2.0`
- `Apache-2.0 with LLVM exception`
- `CC-BY-SA-3.0`
- `CC0-1.0`
- `Expat`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `Iconv-PD`
- `Janik-permissive`
- `Kuchling-PD`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MPL-1.1`
- `Mingw-PD`
- `Plumb-PD`
- `Unicode-DFS-2016`
- `bzip2-1.0.6`
- `cmph`
- `old-glib-tests`

Source:

```console
$ apt-get source -qq --print-uris glib2.0=2.87.2-3
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.87.2-3.dsc' glib2.0_2.87.2-3.dsc 4684 SHA512:dda0b0752a67e22d93dc42d8b48b3c290b951a8f1fcb81d1bfb1cc8d787637a4e76ea811a7b483702c2e927283c676fb2d3cc20ee728840343f224081d32728e
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.87.2.orig-unicode-data.tar.xz' glib2.0_2.87.2.orig-unicode-data.tar.xz 666552 SHA512:32c5e2303868cd80b85f83e94e3f1418ea050fde2f892db0463a41040db2ff0e6db7b29b0af5d0a7bd355976765d1f23ad947230d8c46696a6fd249fc465de6c
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.87.2.orig.tar.xz' glib2.0_2.87.2.orig.tar.xz 5747156 SHA512:6156cdf2cf88672ba23c0ffb133af0dedd65b18df318ba3a99a691678c514af8a30680082ffc86f15c25050f49668382ea81aef9642cb28a4227a3e35aacbde8
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.87.2-3.debian.tar.xz' glib2.0_2.87.2-3.debian.tar.xz 148168 SHA512:a7ed17411052b0bb8ed8179c4a6c20388c84692d2dc3de6fc79b3a2e271be41a065743fb5d4af5b7409291b27fe9625f86a5d653bed158cc8adbdac588c7e628
```

### `dpkg` source package: `glibc=2.42-2ubuntu2`

Binary Packages:

- `libc-bin=2.42-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`)

- `BSD-2-clause`
- `BSD-3-clause-Berkeley`
- `BSD-3-clause-Carnegie`
- `BSD-3-clause-Oracle`
- `BSD-3-clause-WIDE`
- `BSD-like-Spencer`
- `BSL-1.0`
- `CORE-MATH`
- `Carnegie`
- `DEC`
- `FSFAP`
- `GFDL-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-2+-with-link-exception`
- `GPL-3`
- `GPL-3+`
- `IBM`
- `ISC`
- `Inner-Net`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-2.1+-with-link-exception`
- `LGPL-3`
- `LGPL-3+`
- `MIT-like-Lord`
- `PCRE`
- `SunPro`
- `Unicode-DFS-2016`
- `Univ-Coimbra`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `glibc=2.42-2ubuntu5`

Binary Packages:

- `libc-dev-bin=2.42-2ubuntu5`
- `libc-gconv-modules-extra:amd64=2.42-2ubuntu5`
- `libc6:amd64=2.42-2ubuntu5`
- `libc6-dev:amd64=2.42-2ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc-gconv-modules-extra/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

- `BSD-2-clause`
- `BSD-3-clause-Berkeley`
- `BSD-3-clause-Carnegie`
- `BSD-3-clause-Oracle`
- `BSD-3-clause-WIDE`
- `BSD-like-Spencer`
- `BSL-1.0`
- `CORE-MATH`
- `Carnegie`
- `DEC`
- `FSFAP`
- `GFDL-1.3`
- `GPL-2`
- `GPL-2+`
- `GPL-2+-with-link-exception`
- `GPL-3`
- `GPL-3+`
- `IBM`
- `ISC`
- `Inner-Net`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-2.1+-with-link-exception`
- `LGPL-3`
- `LGPL-3+`
- `MIT-like-Lord`
- `PCRE`
- `SunPro`
- `Unicode-DFS-2016`
- `Univ-Coimbra`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.42-2ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42-2ubuntu5.dsc' glibc_2.42-2ubuntu5.dsc 8040 SHA512:cf032ae56884483712e22d6ff2d7b189af611bdd17b05603ff5a3932530bab67626fd5cebe604d6d2ea0e66d2b7fdcbd87fbaa9cea239f28a7a5e4f11b10a3d5
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42.orig.tar.xz' glibc_2.42.orig.tar.xz 19930508 SHA512:73a617db8e0f0958c0575f7a1c5a35b72b7e070b6cbdd02a9bb134995ca7ca0909f1e50d7362c53d2572d72f1879bb201a61d5275bac16136895d9a34ef0c068
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42.orig.tar.xz.asc' glibc_2.42.orig.tar.xz.asc 981 SHA512:d868220778e98d24aead10a585e6a903892e4d043cd96a404634c8aa03d001d624a46a5c0fe13c86f83f66396a1f360a10990966fe377e98a722914b5087575d
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.42-2ubuntu5.debian.tar.xz' glibc_2.42-2ubuntu5.debian.tar.xz 451836 SHA512:e66a53d1e2f5b63b16e0c70d5170ae94396d031cb192c318505764d9382ca447d2716acafd6ba16961cde67c666186b5c64d4e6c8b93b7f585fcac240ca5f9ee
```

### `dpkg` source package: `gmp=2:6.3.0+dfsg-5ubuntu2`

Binary Packages:

- `libgmp-dev:amd64=2:6.3.0+dfsg-5ubuntu2`
- `libgmp10:amd64=2:6.3.0+dfsg-5ubuntu2`
- `libgmpxx4ldbl:amd64=2:6.3.0+dfsg-5ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libgmp-dev/copyright`, `/usr/share/doc/libgmp10/copyright`, `/usr/share/doc/libgmpxx4ldbl/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.3.0+dfsg-5ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-5ubuntu2.dsc' gmp_6.3.0+dfsg-5ubuntu2.dsc 2337 SHA512:746af799ad3fe14fe718ac03bf66ac806307218e89c191b97357772276803ee5c6e4c8a85286e0574e097046f81c0ad2fdc41ef52d28a8c42b1ca6ef2e50ed8d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg.orig.tar.xz' gmp_6.3.0+dfsg.orig.tar.xz 1870556 SHA512:a422b29024464aeb26c69f64be1bc37407d74e0290f44f67fc040fe38b97f3eb7aa6ba8380722ef36cac39816d1c4f24b771159fb86d5979ef0791dcdef708bc
'http://archive.ubuntu.com/ubuntu/pool/main/g/gmp/gmp_6.3.0%2bdfsg-5ubuntu2.debian.tar.xz' gmp_6.3.0+dfsg-5ubuntu2.debian.tar.xz 40328 SHA512:3fb43e01cea284935bfd5b7334a5273b5b342561e651665010215e172a989b1840f0185cb1615c4e3bbba19c6ba1544d964de8b2cee32252ed3952644bb2efcb
```

### `dpkg` source package: `gnupg2=2.4.8-4ubuntu1`

Binary Packages:

- `gpgv=2.4.8-4ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gpgv/copyright`)

- `BSD-3-clause`
- `CC0-1.0`
- `Expat`
- `GPL-2+`
- `GPL-2.0`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `RFC-Reference`
- `TinySCHEME`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `gnupg2=2.4.8-4ubuntu3`

Binary Packages:

- `dirmngr=2.4.8-4ubuntu3`
- `gnupg=2.4.8-4ubuntu3`
- `gpg=2.4.8-4ubuntu3`
- `gpg-agent=2.4.8-4ubuntu3`
- `gpgconf=2.4.8-4ubuntu3`
- `gpgsm=2.4.8-4ubuntu3`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`)

- `BSD-3-clause`
- `CC0-1.0`
- `Expat`
- `GPL-2+`
- `GPL-2.0`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `RFC-Reference`
- `TinySCHEME`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris gnupg2=2.4.8-4ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8-4ubuntu3.dsc' gnupg2_2.4.8-4ubuntu3.dsc 4565 SHA512:b721fcaea7a86d26c5fed553d4956f76d74eaef24628e8bee88966373b141b526c2abd2e4aa22d94d5f4156bb557442d76a63d00c27f9251cbec28d0bdd731e1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8.orig.tar.bz2' gnupg2_2.4.8.orig.tar.bz2 8017685 SHA512:d7f07a258141a583bc8be18c0984d7dfe8508f12c624c053881ee63dfee11adcda8de216bcaaef9f5d24a1e217de70bf69ee2e3cc43b0da66a0e571ce9c4b436
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8.orig.tar.bz2.asc' gnupg2_2.4.8.orig.tar.bz2.asc 228 SHA512:f739eb41481149e145724969e94907ac55e082da0456e1343da24488958ecd020225b45e1d5dc4c93abc06fe89d942e892b488a460f3278f9f2bcff5f51c8ca0
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnupg2/gnupg2_2.4.8-4ubuntu3.debian.tar.xz' gnupg2_2.4.8-4ubuntu3.debian.tar.xz 122928 SHA512:ea071fe3a1c6184eaaf7bbc8f1a4760d88e5430087b9346c0eff8850f3189e49e59a296f089a5affdf8ef5d6c7b97880d0448e003c921f394ed6b29ef291aaee
```

### `dpkg` source package: `gnutls28=3.8.10-3ubuntu1`

Binary Packages:

- `libgnutls-dane0t64:amd64=3.8.10-3ubuntu1`
- `libgnutls-openssl27t64:amd64=3.8.10-3ubuntu1`
- `libgnutls28-dev:amd64=3.8.10-3ubuntu1`
- `libgnutls30t64:amd64=3.8.10-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgnutls-dane0t64/copyright`, `/usr/share/doc/libgnutls-openssl27t64/copyright`, `/usr/share/doc/libgnutls28-dev/copyright`, `/usr/share/doc/libgnutls30t64/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`
- `CC0 license`
- `Expat`
- `FSFAP`
- `GFDL-1.3`
- `GPL`
- `GPL-3`
- `GPLv3+`
- `LGPL`
- `LGPL-3`
- `LGPLv2.1+`
- `LGPLv3+_or_GPLv2+`
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.8.10-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.10-3ubuntu1.dsc' gnutls28_3.8.10-3ubuntu1.dsc 3356 SHA512:7348f62fd6d994dd015c823a05f15a5672fec80c42865c19eb4e97ea243eefc0b66d5d0b5f43661c815cb84fb645dd8e131516761639cd6fed6276ce0f9d3343
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.10.orig.tar.xz' gnutls28_3.8.10.orig.tar.xz 6909856 SHA512:d453bd4527af95cb3905ce8753ceafd969e3f442ad1d148544a233ebf13285b999930553a805a0511293cc25390bb6a040260df5544a7c55019640f920ad3d92
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.10.orig.tar.xz.asc' gnutls28_3.8.10.orig.tar.xz.asc 833 SHA512:8f79f17db7c1d38f2e96daeb8fc709faa34216e56fcc7f724b875692437126ecbc91544bf53f16f6e9f65ad64436cc61ba4c1c4aed057a0acc373be102fd5945
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.10-3ubuntu1.debian.tar.xz' gnutls28_3.8.10-3ubuntu1.debian.tar.xz 177332 SHA512:4ebe267faa0e30cbec597ae38953d82516e6ab428f9990bb97e0a5728048a721501fd2ec93162d7a37d49a835df61d4f326f196b463c611f150fc8a43a5355e3
```

### `dpkg` source package: `graphite2=1.3.14-11ubuntu1`

Binary Packages:

- `libgraphite2-3:amd64=1.3.14-11ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libgraphite2-3/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `MPL-1.1`
- `custom-sil-open-font-license`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris graphite2=1.3.14-11ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-11ubuntu1.dsc' graphite2_1.3.14-11ubuntu1.dsc 2653 SHA512:65798e19d15b81683da58df6b2106cfdc5e7dcdf90d290a4fcbbcf0b450fbaf14939d7ee01d5c8b7b51488d46d9173a3ae1e7f2e3d30d07f2f84af65a0309677
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14.orig.tar.gz' graphite2_1.3.14.orig.tar.gz 6629829 SHA512:49d127964d3f5c9403c7aecbfb5b18f32f25fe4919a81c49e0534e7123fe845423e16b0b8c8baaae21162b1150ab3e0f1c22c344e07d4364b6b8473c40a0822c
'http://archive.ubuntu.com/ubuntu/pool/main/g/graphite2/graphite2_1.3.14-11ubuntu1.debian.tar.xz' graphite2_1.3.14-11ubuntu1.debian.tar.xz 15984 SHA512:dbdd8fd63b23ffa9ae1aec0709d6c4f9f8622d488c8683214c8ad95290791878d212c23ae99589fd266f85a5deddd37a59c2587f7b41268e1cb25b0e0a078e62
```

### `dpkg` source package: `grep=3.12-1`

Binary Packages:

- `grep=3.12-1`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `BSD-3-clause`
- `FSFAP`
- `FSFUL`
- `FSFULLR`
- `FSFULLR and/or GPL and/or LGPL`
- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris grep=3.12-1
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.12-1.dsc' grep_3.12-1.dsc 1647 SHA512:267043711608634df53a28221afeacb510ebeb85c10bb69257f3860552704651852097f2c447c14728f1c0c4212bfdc42f9ad69cfd11faf4232d702da717fae6
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.12.orig.tar.xz' grep_3.12.orig.tar.xz 1918448 SHA512:c54b4db5a8b9afe098c088decd94977746305284d716666a60bac82b4edc0fae4acf828970b5b6fc7d58ecd549f638e17e6958f33a71fedcc7d7415b9228b161
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.12.orig.tar.xz.asc' grep_3.12.orig.tar.xz.asc 833 SHA512:333755fd9e5879436789a19e9593667d6fb96c2d1b876a1c391eb9cd75d10bb7fbc10215db9838280e6006790c818ef4583b1ae22318a833a5b69264ca15dbf1
'http://archive.ubuntu.com/ubuntu/pool/main/g/grep/grep_3.12-1.debian.tar.xz' grep_3.12-1.debian.tar.xz 24160 SHA512:b7e3aed1874a943a8fcef27e55040f64304c3ecd505b20e6dbec4ce9b5ec658de1b5434c21afe4f4cde31115cab5532ed728311b19c4ee99537697cd7ddb6ba0
```

### `dpkg` source package: `gzip=1.13-1ubuntu4`

Binary Packages:

- `gzip=1.13-1ubuntu4`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3+-no-invariant`
- `GFDL-3`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.13-1ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13-1ubuntu4.dsc' gzip_1.13-1ubuntu4.dsc 1933 SHA512:28e928fb761398aed1e66355c6cdba4042842bcd4f8288f89f2f711675ddfb310afc5fd84319a95360b9d532d18a059055f8b0915d834313cf51c5e627c4c85c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13.orig.tar.xz' gzip_1.13.orig.tar.xz 838248 SHA512:e3d4d4aa4b2e53fdad980620307257c91dfbbc40bcec9baa8d4e85e8327f55e2ece552c9baf209df7b66a07103ab92d4954ac53c86c57fbde5e1dd461143f94c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.13-1ubuntu4.debian.tar.xz' gzip_1.13-1ubuntu4.debian.tar.xz 21444 SHA512:0fe5f34300df6de43d296bf03a4dc1a73c744b46b091afe4fab273efd1cc2abb50ad471b7b999399cf2c5405c128ec0b8df58dc4d4b0a2ec75913e57687e06f5
```

### `dpkg` source package: `harfbuzz=12.3.2-1`

Binary Packages:

- `libharfbuzz0b:amd64=12.3.2-1`

Licenses: (parsed from: `/usr/share/doc/libharfbuzz0b/copyright`)

- `Apache-2.0`
- `CC0-1.0`
- `GPL-2`
- `GPL-2+ with Font exception`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `MIT`
- `Monotype`
- `OFL-1.1`
- `UFL-1.0`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris harfbuzz=12.3.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_12.3.2-1.dsc' harfbuzz_12.3.2-1.dsc 2573 SHA512:3605b6db30587f08293fa5b6e23b30056a55850bfc5b904a1d30a2e0720b2bb50a3605949337c2a3766b1bc2b41fe38846ce8b0ee4968656f26292f605318542
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_12.3.2.orig.tar.xz' harfbuzz_12.3.2.orig.tar.xz 19282952 SHA512:2bb907d206edb93a9fb0856dc2e767d491f79f20cd8e8eeeb65f284f10b67ca9ae16b6a8e72ebbfedfeaa0199af7c12dbe675eb08b7c1fb61d2f5ca1fa406782
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_12.3.2-1.debian.tar.xz' harfbuzz_12.3.2-1.debian.tar.xz 19772 SHA512:688eb5afb3aa98af1d32c565dc40d8992f90a2ca51bbf8c12c5eb1386b337b2a5f85664dd690f3c740ad93f4a63512872a0d35e6d0f78420c4e0435d228b5e78
```

### `dpkg` source package: `hicolor-icon-theme=0.18-2build1`

Binary Packages:

- `hicolor-icon-theme=0.18-2build1`

Licenses: (parsed from: `/usr/share/doc/hicolor-icon-theme/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris hicolor-icon-theme=0.18-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-2build1.dsc' hicolor-icon-theme_0.18-2build1.dsc 2349 SHA512:2be146bc8fbf91d145f24532d63d3d91d48e9929269435390906a72a66d3b7ddfa225d93bcf05db51b6e90ca17296dae9b41874712ca7d4fe89dbba22dd29d01
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz' hicolor-icon-theme_0.18.orig.tar.xz 29624 SHA512:07db44fb6bec797445740832fa2b3ba56f5f335834161a26a4e5f767a8c45c0885ef1189e887b56752bd20c4b1aac101c5d4a395df4177cd3817ee5105db0d37
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18.orig.tar.xz.asc' hicolor-icon-theme_0.18.orig.tar.xz.asc 833 SHA512:e00447c8918250978622a9465ac16181206deed977743d71faa068341f3aab4a1e98e70aed9f03e62806f2b3d8e1df20ff3b09332d0feda70d4532496154f0c2
'http://archive.ubuntu.com/ubuntu/pool/main/h/hicolor-icon-theme/hicolor-icon-theme_0.18-2build1.debian.tar.xz' hicolor-icon-theme_0.18-2build1.debian.tar.xz 9232 SHA512:640788eb0f80d3e67c707b4d2136e92c5a753af4920c03da4998bf442d99b5fa84897dd15bb88f4e99e8554ee81ada4820965265390c032823cc3ae85fdf1da9
```

### `dpkg` source package: `hostname=3.25build1`

Binary Packages:

- `hostname=3.25build1`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.25build1
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.25build1.dsc' hostname_3.25build1.dsc 1543 SHA512:f9f180a2b477d4e3d5e08714d8978c961558f289086a0f221d0483d223fc9201512ba554c5e356102c438216ffaadcda6d21e9db9e644dce41652388878c454e
'http://archive.ubuntu.com/ubuntu/pool/main/h/hostname/hostname_3.25build1.tar.xz' hostname_3.25build1.tar.xz 12896 SHA512:b99c6e870198c1be17e5a4e68cecfe40e1f28b1e43595ab960c79afdd94877f0e34903dbb33d845060fa76e9ed64298c250bd27a03446ba6e0b61d135ed97e11
```

### `dpkg` source package: `imagemagick=8:7.1.2.13+dfsg1-1`

Binary Packages:

- `imagemagick=8:7.1.2.13+dfsg1-1`
- `imagemagick-7-common=8:7.1.2.13+dfsg1-1`
- `imagemagick-7.q16=8:7.1.2.13+dfsg1-1`
- `libmagickcore-7-arch-config:amd64=8:7.1.2.13+dfsg1-1`
- `libmagickcore-7-headers=8:7.1.2.13+dfsg1-1`
- `libmagickcore-7.q16-10:amd64=8:7.1.2.13+dfsg1-1`
- `libmagickcore-7.q16-10-extra:amd64=8:7.1.2.13+dfsg1-1`
- `libmagickcore-7.q16-dev:amd64=8:7.1.2.13+dfsg1-1`
- `libmagickcore-dev=8:7.1.2.13+dfsg1-1`
- `libmagickwand-7-headers=8:7.1.2.13+dfsg1-1`
- `libmagickwand-7.q16-10:amd64=8:7.1.2.13+dfsg1-1`
- `libmagickwand-7.q16-dev:amd64=8:7.1.2.13+dfsg1-1`
- `libmagickwand-dev=8:7.1.2.13+dfsg1-1`

Licenses: (parsed from: `/usr/share/doc/imagemagick/copyright`, `/usr/share/doc/imagemagick-7-common/copyright`, `/usr/share/doc/imagemagick-7.q16/copyright`, `/usr/share/doc/libmagickcore-7-arch-config/copyright`, `/usr/share/doc/libmagickcore-7-headers/copyright`, `/usr/share/doc/libmagickcore-7.q16-10/copyright`, `/usr/share/doc/libmagickcore-7.q16-10-extra/copyright`, `/usr/share/doc/libmagickcore-7.q16-dev/copyright`, `/usr/share/doc/libmagickcore-dev/copyright`, `/usr/share/doc/libmagickwand-7-headers/copyright`, `/usr/share/doc/libmagickwand-7.q16-10/copyright`, `/usr/share/doc/libmagickwand-7.q16-dev/copyright`, `/usr/share/doc/libmagickwand-dev/copyright`)

- `Artistic`
- `BSD-with-FSF-change-public-domain`
- `GNU-All-Permissive-License`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL2+-with-Autoconf-Macros-exception`
- `GPL3+-with-Autoconf-Macros-exception`
- `GPL3+-with-Autoconf-Macros-exception-GNU`
- `ImageMagick`
- `ImageMagickLicensePartEZXML`
- `ImageMagickLicensePartFIG`
- `ImageMagickLicensePartGsview`
- `ImageMagickLicensePartOpenSSH`
- `ImageMagickPartGraphicsMagick`
- `ImageMagickPartlibjpeg`
- `ImageMagickPartlibsquish`
- `Imagemagick`
- `LGPL-3`
- `LGPL-3+`
- `Magick++`
- `Makefile-in`
- `Perllikelicence`
- `aclocal`

Source:

```console
$ apt-get source -qq --print-uris imagemagick=8:7.1.2.13+dfsg1-1
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.2.13%2bdfsg1-1.dsc' imagemagick_7.1.2.13+dfsg1-1.dsc 5202 SHA512:ed994df5b85f961161de2cf81af00c39a0aa2ca3676e4b5298c812b3db2069d18903a47bca42bd2d874d5116f6bc9edaf2973263cfd51c46bbae85fd1de2c8d6
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.2.13%2bdfsg1.orig.tar.xz' imagemagick_7.1.2.13+dfsg1.orig.tar.xz 10524452 SHA512:bcde9957c77c224839b897fba7b18aa0d640cf76d95c8eccf9775720ba998c2da2e31b2e750b168cd62a9fa1dc6ab9bb4af482f3e6f22eed8a89d85ec70a8e4d
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.2.13%2bdfsg1-1.debian.tar.xz' imagemagick_7.1.2.13+dfsg1-1.debian.tar.xz 268004 SHA512:6195126a74f01f040ec9abd3a8095c26a1392d43e45198858f75cc3d57d5afa87a933dfd50a40b729c2455ac927da587422333c521768b82471e00e9d0f25f95
```

### `dpkg` source package: `imath=3.1.12-1ubuntu3`

Binary Packages:

- `libimath-3-1-29t64:amd64=3.1.12-1ubuntu3`
- `libimath-dev:amd64=3.1.12-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29t64/copyright`, `/usr/share/doc/libimath-dev/copyright`)

- `imath`

Source:

```console
$ apt-get source -qq --print-uris imath=3.1.12-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12-1ubuntu3.dsc' imath_3.1.12-1ubuntu3.dsc 2728 SHA512:d63dc15bf0401348cf5b8f3b931d2ef070651076bc092343d9599754c8f5392b7e4ea801db890b7e6176a11de3537dcf825cc10db230feeed34473dce95b1f8a
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12.orig.tar.gz' imath_3.1.12.orig.tar.gz 604232 SHA512:32628dfcacb610310b81ffe017a66215cf5fb84c2e0a6ac8c94a68c048be3d2b97eb57965dd253770184d5824cce1e5440b8eefb2834666b273b3193ff108343
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12.orig.tar.gz.asc' imath_3.1.12.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12-1ubuntu3.debian.tar.xz' imath_3.1.12-1ubuntu3.debian.tar.xz 10224 SHA512:a17231679aec8877a0c301068ea46b6c314d61a25c562ef4956f9957a209c72a58cb511733faa6faa204a9f91ff063a5c504df40f820244666fc22ada5e12c3f
```

### `dpkg` source package: `init-system-helpers=1.69`

Binary Packages:

- `init-system-helpers=1.69`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.69
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.69.dsc' init-system-helpers_1.69.dsc 2234 SHA512:f8055fa3cf3eaefff9178c737845464de128a3f4682c421c5a65b6e2a45d615e166bfbdb4326dedc98ea2426f243b1b24b51f59d0bf78b968b1558b44b90ccd5
'http://archive.ubuntu.com/ubuntu/pool/main/i/init-system-helpers/init-system-helpers_1.69.tar.xz' init-system-helpers_1.69.tar.xz 45648 SHA512:3b08b93194523af989177616a5e8cfa1ffa9ba31650a09325a98e704f7e4e8291febcaeea8e66e32784ce45e286d136091d3d83a8416859368ae59b8897f3d9d
```

### `dpkg` source package: `isl=0.27-1build1`

Binary Packages:

- `libisl23:amd64=0.27-1build1`

Licenses: (parsed from: `/usr/share/doc/libisl23/copyright`)

- `BSD-2-clause`
- `LGPL-2`
- `LGPL-2.1+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris isl=0.27-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27-1build1.dsc' isl_0.27-1build1.dsc 1829 SHA512:849400d7fca9bef18e41156fa87a6ca2837d279da0b57973de6431a946e9eb02f44bd3861ae3ecf308efc26e4233bd7f2d10cd90a2c10deebfad8b3d41ac96a1
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27.orig.tar.xz' isl_0.27.orig.tar.xz 2056436 SHA512:6d6f50c3f6f26e0d3f67586dee6427d87999c426c94069a6f3012ec3c9a41adeebd50f43b5d2705db6abc12e38eb01c19f55dba113c0799da5f667eef46b2be0
'http://archive.ubuntu.com/ubuntu/pool/main/i/isl/isl_0.27-1build1.debian.tar.xz' isl_0.27-1build1.debian.tar.xz 24944 SHA512:986c512a6bb89a1b85c25a44f66b51c91df106f9027ea71fa5ab051a574a4f19d73284c2f65139ac49f1a226e3fc3282c690c7ab53560ece18e6375779a9c328
```

### `dpkg` source package: `jansson=2.14-2build4`

Binary Packages:

- `libjansson4:amd64=2.14-2build4`

Licenses: (parsed from: `/usr/share/doc/libjansson4/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris jansson=2.14-2build4
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build4.dsc' jansson_2.14-2build4.dsc 2083 SHA512:4dc57c6e48c6d8278a47f34a8590706389ebf58fe3fe025b9e6fdbcb5e23e101e5cab118604b498a31d7d5b3d8520f8e8022c21bb96ef84a1e6a0e87c3e96999
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14.orig.tar.gz' jansson_2.14.orig.tar.gz 141500 SHA512:c56e2e8d18819e3f5caa46edd4819694a240aeb3524a6f9d9f4465edf65b183d1870bd5d256cdd378d411a52979121369b951406fdf7bf323db5c30001fa1bc4
'http://archive.ubuntu.com/ubuntu/pool/main/j/jansson/jansson_2.14-2build4.debian.tar.xz' jansson_2.14-2build4.debian.tar.xz 5688 SHA512:50fd608db5883b3b78bb5551b453d0fe57d9a86eda5b92744c5a49cdd65d9d6628230b36217bd1a28c151ea0ad35c3991bcc0c729668c428fd9987eaefea58bf
```

### `dpkg` source package: `jbigkit=2.1-6.1ubuntu3`

Binary Packages:

- `libjbig-dev:amd64=2.1-6.1ubuntu3`
- `libjbig0:amd64=2.1-6.1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libjbig-dev/copyright`, `/usr/share/doc/libjbig0/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris jbigkit=2.1-6.1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-6.1ubuntu3.dsc' jbigkit_2.1-6.1ubuntu3.dsc 2170 SHA512:7d718da05ee327cb9b2aa866be99129b82f63249bc6125e206ab689763672951ceead170decb268565a320b8a8fa86abe5a27b916cbbbb9793c06582ad7c2c71
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1.orig.tar.gz' jbigkit_2.1.orig.tar.gz 438710 SHA512:c4127480470ef90db1ef3bd2caa444df10b50ed8df0bc9997db7612cb48b49278baf44965028f1807a21028eb965d677e015466306b44683c4ec75a23e1922cf
'http://archive.ubuntu.com/ubuntu/pool/main/j/jbigkit/jbigkit_2.1-6.1ubuntu3.debian.tar.xz' jbigkit_2.1-6.1ubuntu3.debian.tar.xz 11240 SHA512:b7f74359529b23e83c075769e953f5348ecfc310d1a56af9b483303ef7f23c2e0ce6faffd1ec97674836ea110b742958d2108ed5b816952cdfab9e0d1e97ed74
```

### `dpkg` source package: `keyutils=1.6.3-6ubuntu3`

Binary Packages:

- `libkeyutils1:amd64=1.6.3-6ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.6.3-6ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-6ubuntu3.dsc' keyutils_1.6.3-6ubuntu3.dsc 2186 SHA512:8fa833d4b7cb7f9c2fa66b8f5d8367c7dc2c0f006bdc8d142deee558cc72e2bc927b2d866273f4098799812baa7eb06bad6ad09214849acc8ca8346d18003dbb
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3.orig.tar.gz' keyutils_1.6.3.orig.tar.gz 137022 SHA512:f65965b8566037078b8eeffa66c6fdbe121c8c2bea7fa5bce04cf7ba5ccc50d5b48e51f4a67ca91e4d5d9a12469e7e3eb3036c920ab25e3feba6e93b4c149cf9
'http://archive.ubuntu.com/ubuntu/pool/main/k/keyutils/keyutils_1.6.3-6ubuntu3.debian.tar.xz' keyutils_1.6.3-6ubuntu3.debian.tar.xz 17552 SHA512:8a6752c41e5646e5cc6754d9c9a068710eab9a5197f81094b5534dec56f39e0422ee7127310180ddb812921492e9fe3a3d47a66ec4c6540bd3ca6e2f4204976e
```

### `dpkg` source package: `krb5=1.22.1-2`

Binary Packages:

- `krb5-multidev:amd64=1.22.1-2`
- `libgssapi-krb5-2:amd64=1.22.1-2`
- `libgssrpc4t64:amd64=1.22.1-2`
- `libk5crypto3:amd64=1.22.1-2`
- `libkadm5clnt-mit12:amd64=1.22.1-2`
- `libkadm5srv-mit12:amd64=1.22.1-2`
- `libkdb5-10t64:amd64=1.22.1-2`
- `libkrb5-3:amd64=1.22.1-2`
- `libkrb5-dev:amd64=1.22.1-2`
- `libkrb5support0:amd64=1.22.1-2`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4t64/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit12/copyright`, `/usr/share/doc/libkadm5srv-mit12/copyright`, `/usr/share/doc/libkdb5-10t64/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.22.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1-2.dsc' krb5_1.22.1-2.dsc 3378 SHA512:41e045d9b0ef3d793c32c26c2b4995a197e9dfd6e820e6d9c7edd85f102f9ea825f7af9ff3f69acfa830a9ea91a090055f90d8126c135772f53d83f8bb855bc1
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1.orig.tar.gz' krb5_1.22.1.orig.tar.gz 8747101 SHA512:c33bfada5e0c035133436031d9818ad97b0ff08578691c832b743c55751a2cf9460501d3cc658ab79655ed7a0f9f4795ba94b363d6b616795d9bdca668825c52
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1.orig.tar.gz.asc' krb5_1.22.1.orig.tar.gz.asc 833 SHA512:83354b1e4f71cfb52ba8b921740c5abd4941563f4f8ed880f1feacb173aec2d1b6efbe94d21b062418a73b47d81e2e734fdd47805a07278dbc4945975b9f1267
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1-2.debian.tar.xz' krb5_1.22.1-2.debian.tar.xz 102864 SHA512:e345b670cb39866f7f7d3ba2495b28fd0470795feb5405a4ce781971beccfb94fb739d9e93ac716b086ea6c01dae96c9dc7091f60511f7d756d0c785f9436ee3
```

### `dpkg` source package: `lcms2=2.17-1`

Binary Packages:

- `liblcms2-2:amd64=2.17-1`
- `liblcms2-dev:amd64=2.17-1`

Licenses: (parsed from: `/usr/share/doc/liblcms2-2/copyright`, `/usr/share/doc/liblcms2-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `IJG`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris lcms2=2.17-1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.17-1.dsc' lcms2_2.17-1.dsc 2043 SHA512:26fca49377c6526ab563d8b44254912e97ae5384baa199fbf510c98b48a7260a72df0bed0aebe0da9a56f4491bd94fc76e72b0bf7f54fbcc76e7e554c05c0aa1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.17.orig.tar.gz' lcms2_2.17.orig.tar.gz 5245319 SHA512:81885c70fb26a9b7d37a398f43ccb0d1d3ab8f43de7da8f760b26d053a0d7e0543e7d3b0cdcaf9b3b681a1b88f032134c5a3c1a6774a9abc66a8a3f10ba64398
'http://archive.ubuntu.com/ubuntu/pool/main/l/lcms2/lcms2_2.17-1.debian.tar.xz' lcms2_2.17-1.debian.tar.xz 11760 SHA512:b049a28f64da638728ca788e3acbf9983a51626fe1de3316cb16d550842c1c54d49aeb7be5bab44e18821434229d2dae1b86a2bd9d47114a5a20d55aaaf3dd0d
```

### `dpkg` source package: `lerc=4.0.0+ds-5ubuntu2`

Binary Packages:

- `liblerc-dev:amd64=4.0.0+ds-5ubuntu2`
- `liblerc4:amd64=4.0.0+ds-5ubuntu2`

Licenses: (parsed from: `/usr/share/doc/liblerc-dev/copyright`, `/usr/share/doc/liblerc4/copyright`)

- `Apache-2.0`

Source:

```console
$ apt-get source -qq --print-uris lerc=4.0.0+ds-5ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-5ubuntu2.dsc' lerc_4.0.0+ds-5ubuntu2.dsc 2739 SHA512:9e75c46439d01176626787abd05cf161e052bb12e5b44d5abae6015814b2972453b0ef18818f0fe8dc4da0a7b706d1c671ad4c40b4647b81ae3225942dc8487a
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds.orig.tar.xz' lerc_4.0.0+ds.orig.tar.xz 348140 SHA512:d5539360fa92f40319466fea73a66d0d03aedff886fb75985bfcaeeb77ef516b9fa24b8d83da09c114bf6090bbd68e64d9ac2649a19315895134fa86023478e1
'http://archive.ubuntu.com/ubuntu/pool/main/l/lerc/lerc_4.0.0%2bds-5ubuntu2.debian.tar.xz' lerc_4.0.0+ds-5ubuntu2.debian.tar.xz 8808 SHA512:d17a28ee92e21398ff4fa3e88c45a11d19de0979a960fc978326392810de8fd4d9118724f436a5689d755c950b05d7eedcf584c2a5e8426364ca1eacd2a2695e
```

### `dpkg` source package: `libassuan=3.0.2-2build1`

Binary Packages:

- `libassuan9:amd64=3.0.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libassuan9/copyright`)

- `FSFULLR`
- `FSFULLRWD`
- `GPL-2`
- `GPL-2+ with Autoconf-data exception`
- `GPL-2+ with Libtool exception`
- `GPL-2.with.nonstandard.Autoconf-data.exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf-2.0~Archive exception`
- `GPL-3+ with Autoconf-data exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris libassuan=3.0.2-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2-2build1.dsc' libassuan_3.0.2-2build1.dsc 2705 SHA512:7efac2cb818028a1f44fa6239fcae17774bf52a772518cdb936e780491e1c63e99a8c684051a71673d7f4e040fe24ea945903f7621d9a5a40e543b57de9560b8
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2' libassuan_3.0.2.orig.tar.bz2 593917 SHA512:a591eda350ecbf4fe8568b5087f69830df31f36ec67e2a50672aacea9bee16020f374a0bface459aeac1897c048072415ab5962a97034ce6fa413100b2a427fb
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2.orig.tar.bz2.asc' libassuan_3.0.2.orig.tar.bz2.asc 228 SHA512:56e0a8288e498bbba504fdaa84060ef6dd30c72efd691d6d0e39069113a394f2da407d83adfd14f7ae25b8e8531f8e9dee859b52471261653dc2ed5f44ef22dc
'http://archive.ubuntu.com/ubuntu/pool/main/liba/libassuan/libassuan_3.0.2-2build1.debian.tar.xz' libassuan_3.0.2-2build1.debian.tar.xz 17596 SHA512:b4fc08de67862598c8440001b427ef8ce30e9bfcd15d91788ba8dc962a87711b36cd25006feda8a32121a43da385d3df5a4b19b0c4bc96799446403aeb2b0dcb
```

### `dpkg` source package: `libbsd=0.12.2-2build1`

Binary Packages:

- `libbsd0:amd64=0.12.2-2build1`

Licenses: (parsed from: `/usr/share/doc/libbsd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-2-clause-author`
- `BSD-2-clause-verbatim`
- `BSD-3-clause`
- `BSD-3-clause-John-Birrell`
- `BSD-3-clause-Regents`
- `BSD-3-clause-author`
- `BSD-5-clause-Peter-Wemm`
- `Beerware`
- `Expat`
- `ISC`
- `ISC-Original`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcap-ng=0.8.5-4build3`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4build3`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcap2=1:2.75-10ubuntu1`

Binary Packages:

- `libcap2:amd64=1:2.75-10ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libcap2=1:2.75-10ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75-10ubuntu1.dsc' libcap2_2.75-10ubuntu1.dsc 2789 SHA512:6585867897ab6b136b319376f7269ea1a0d04c46b865a633515ef34c3326f6683d0830d0c7c60201161dd2dab2300ab91fbb21636e5bb235f144109efdb502d9
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz' libcap2_2.75.orig.tar.xz 197868 SHA512:229e9b62a1d54024107cbf321fffcb152c0071154554a3fcee6e09e19cc47fd1fd862575135a4fc589b79a043f760bf40d26ea9fd58638f26e809533c017d65f
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75.orig.tar.xz.asc' libcap2_2.75.orig.tar.xz.asc 833 SHA512:6a6af52ef3a48356d8c205827aa039ed852ec4a1cfea44f00613457380478ebd4946caf933a8ebdf98899b14340b9a7ef9b7151c4659329e2fd80590667d59d9
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap2/libcap2_2.75-10ubuntu1.debian.tar.xz' libcap2_2.75-10ubuntu1.debian.tar.xz 23640 SHA512:deddc0d08ad985e22cbefa63f65c8c29731af8eb9d5c7d34a4597d2609fe29900b4354337c8ef7ce5a99c808c481d46572136448268742bdc3505e0bb1ba75cb
```

### `dpkg` source package: `libcbor=0.10.2-2ubuntu2`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libcbor=0.10.2-2ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-2ubuntu2.dsc' libcbor_0.10.2-2ubuntu2.dsc 2238 SHA512:13dfefa6219a21743816cdff9a1fff1ef7c41ef70f276c6759090dd82a5972cb5bd9b2d84f3a5a045b2ff727aa5a8404981f3e3d67123f48e290ecf641bdeae6
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2.orig.tar.gz' libcbor_0.10.2.orig.tar.gz 289450 SHA512:23c6177443778d4b4833ec7ed0d0e639a0d4863372e3a38d772fdce2673eae6d5cb2a31a2a021d1a699082ea53494977c907fd0e94149b97cb23a4b6d039228a
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcbor/libcbor_0.10.2-2ubuntu2.debian.tar.xz' libcbor_0.10.2-2ubuntu2.debian.tar.xz 7392 SHA512:cb259804ef47078f998955a3534148fe7c96aea3f619a999e7c4d479b837b50138899abb8a22db6e5ef70b5acbd8b0aae6aa010cab8751e6c6f4b8da50dcacab
```

### `dpkg` source package: `libdatrie=0.2.14-1`

Binary Packages:

- `libdatrie1:amd64=0.2.14-1`

Licenses: (parsed from: `/usr/share/doc/libdatrie1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libdatrie=0.2.14-1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.14-1.dsc' libdatrie_0.2.14-1.dsc 2236 SHA512:0a6f8de2aa0130603f5bf89f0b5c8a2cf2e885c57f127015bca536d4ac15e43c0dc5f241ba787626f835fcad20c2a4a3fbc9da95f42a88b5e6c0a09b40d394cf
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.14.orig.tar.xz' libdatrie_0.2.14.orig.tar.xz 325696 SHA512:c5df387a1c9b5fae65eff69102651f4f054d873194d97faa8e329282353156fa4fb41a1ea771b24ade3f0ad2a548d85d7950a4aa6ed4e5c356bc504720e792d1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdatrie/libdatrie_0.2.14-1.debian.tar.xz' libdatrie_0.2.14-1.debian.tar.xz 9792 SHA512:00b2feadcd0efebc96d9c97282cc769e546bcabd659e675cf39428965540da6939e9596100c97d912af38bf0c73e9bb3a160bf1ad803e2053a62ae2add924877
```

### `dpkg` source package: `libde265=1.0.16-1build1`

Binary Packages:

- `libde265-0:amd64=1.0.16-1build1`

Licenses: (parsed from: `/usr/share/doc/libde265-0/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `other-1`
- `public-domain-1`

Source:

```console
$ apt-get source -qq --print-uris libde265=1.0.16-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.16-1build1.dsc' libde265_1.0.16-1build1.dsc 2345 SHA512:c24fc258ad785e5a5e4def68fa89df16a3bb3787ce0c171a8d716544376bb187f55435392b2a3804b27bc87ffb9e0b90ef7e2d7242e0dce99398721f31e63579
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.16.orig.tar.gz' libde265_1.0.16.orig.tar.gz 835657 SHA512:07f4dd75238030ed86f1b86d990a5a1c31866d5217db2aa23757432da214a19c5f4094a6c2f8fe3453c64d36ee745ca4f1e22a19a80b2685b6530431a35eb4e1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libde265/libde265_1.0.16-1build1.debian.tar.xz' libde265_1.0.16-1build1.debian.tar.xz 136956 SHA512:2c2b78426e709abeafaf7bf15b48eb3ed55630562b148e37c1ab412846aa5572d3593f7b22a144a5f4d9a94b09986e096846d73b608af5e74f857f23816b8338
```

### `dpkg` source package: `libdeflate=1.23-2build1`

Binary Packages:

- `libdeflate-dev:amd64=1.23-2build1`
- `libdeflate0:amd64=1.23-2build1`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.23-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23-2build1.dsc' libdeflate_1.23-2build1.dsc 2257 SHA512:ae4f6624fad59f7dbc01cd8e8ea4c84a0417fc5075edf0b7bc6f8b1164a22862004f283b794546a2c13eeabb010837533fab26fe63147c30d5ba1b8c511d9f0b
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23.orig.tar.gz' libdeflate_1.23.orig.tar.gz 197519 SHA512:c1effb9c5ee8d65bc12ae3d0669a4a394acace13cc146300ed24a7f12a0ec058f66729e1ffbae268711bdcc4151143752ab2d56a099dd6394b2735e8e2f1b671
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23-2build1.debian.tar.xz' libdeflate_1.23-2build1.debian.tar.xz 5696 SHA512:8f371affa26c020b4b7555c2f28f0b7f2b075ed072f25bc022e1a267dace5e0bc6886729b0920a0bb69166ea3c2c2df308c24e575e6f88b991d24fe1a47570ac
```

### `dpkg` source package: `libedit=3.1-20251016-1`

Binary Packages:

- `libedit2:amd64=3.1-20251016-1`

Licenses: (parsed from: `/usr/share/doc/libedit2/copyright`)

- `BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libedit=3.1-20251016-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20251016-1.dsc' libedit_3.1-20251016-1.dsc 2264 SHA512:6bcd222ac7cf37173bbe651d17d87d47cc48c26c6ed25de85ff34dc7324221c83ceb1fdc4289c91c75bd3589907c3ad4722487b6624b95774f3012d986fe1cff
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20251016.orig.tar.gz' libedit_3.1-20251016.orig.tar.gz 549005 SHA512:a084895f92d7b373eb5aff7d4497d395fb141343fdce86de5387fedd5f77b0695ea68f061e461e35d248e66cf4cc0c62a364309f908a42db27e4fa70b530e2cf
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libedit/libedit_3.1-20251016-1.debian.tar.xz' libedit_3.1-20251016-1.debian.tar.xz 16716 SHA512:8248a63a1f95b382ad2f436e24b18ab048b47db357043303c772f7f9a8e4e99ac333c8504d1b96dc84df1c28740d6ec559b1b93385df1995d374ea4964aedeae
```

### `dpkg` source package: `liberror-perl=0.17030-1`

Binary Packages:

- `liberror-perl=0.17030-1`

Licenses: (parsed from: `/usr/share/doc/liberror-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`
- `MIT/X11`

Source:

```console
$ apt-get source -qq --print-uris liberror-perl=0.17030-1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17030-1.dsc' liberror-perl_0.17030-1.dsc 2337 SHA512:1c039478eb6721fb61ac62f0daedf0e32e935f40625564a1dbc6f240776bb9bfaa05a2f0176296f08fcf939e7d967fd31274aca9d7522b05809bd32c97e511ec
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17030.orig.tar.gz' liberror-perl_0.17030.orig.tar.gz 33488 SHA512:842e33fbc2f2bd6eaf03459263070311fde9ae06105438baf8920826ca26d3f46c18d0d49bfe85a3eb25dfe94e671db0e7d1f30a143b8d82bea47410bfbf7f01
'http://archive.ubuntu.com/ubuntu/pool/main/libe/liberror-perl/liberror-perl_0.17030-1.debian.tar.xz' liberror-perl_0.17030-1.debian.tar.xz 4660 SHA512:7a7d03e838840c466c34bcea97b43a1cc12f4baa87ed260164a04c01ca2aeec50286104b98ac074e5af44e8e68fac36823ba0ad04729fb2d8046487b42a2553b
```

### `dpkg` source package: `libevent=2.1.12-stable-10build2`

Binary Packages:

- `libevent-2.1-7t64:amd64=2.1.12-stable-10build2`
- `libevent-core-2.1-7t64:amd64=2.1.12-stable-10build2`
- `libevent-dev=2.1.12-stable-10build2`
- `libevent-extra-2.1-7t64:amd64=2.1.12-stable-10build2`
- `libevent-openssl-2.1-7t64:amd64=2.1.12-stable-10build2`
- `libevent-pthreads-2.1-7t64:amd64=2.1.12-stable-10build2`

Licenses: (parsed from: `/usr/share/doc/libevent-2.1-7t64/copyright`, `/usr/share/doc/libevent-core-2.1-7t64/copyright`, `/usr/share/doc/libevent-dev/copyright`, `/usr/share/doc/libevent-extra-2.1-7t64/copyright`, `/usr/share/doc/libevent-openssl-2.1-7t64/copyright`, `/usr/share/doc/libevent-pthreads-2.1-7t64/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSL`
- `Expat`
- `FSFUL`
- `FSFULLR`
- `FSFULLR-No-Warranty`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `curl`

Source:

```console
$ apt-get source -qq --print-uris libevent=2.1.12-stable-10build2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-10build2.dsc' libevent_2.1.12-stable-10build2.dsc 2436 SHA512:bc7c961f9858e8212f8822104accd902d64477ab18a7db6b896bfe5f4f7b4f400ae5aa944570e6fc9da932446b9171b1f133e62081037383a5c7256db157e672
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable.orig.tar.gz' libevent_2.1.12-stable.orig.tar.gz 1100847 SHA512:88d8944cd75cbe78bc4e56a6741ca67c017a3686d5349100f1c74f8a68ac0b6410ce64dff160be4a4ba0696ee29540dfed59aaf3c9a02f0c164b00307fcfe84f
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libevent/libevent_2.1.12-stable-10build2.debian.tar.xz' libevent_2.1.12-stable-10build2.debian.tar.xz 18060 SHA512:22c896807ecd0b651e7228e6a59c0a9b968221db1e3633d479ce7719632bf6cefc82546337a90a3bc7e839e80813d03b19ef6431cd6dec841dd027f08b0635b5
```

### `dpkg` source package: `libexif=0.6.25-1build1`

Binary Packages:

- `libexif-dev:amd64=0.6.25-1build1`
- `libexif12:amd64=0.6.25-1build1`

Licenses: (parsed from: `/usr/share/doc/libexif-dev/copyright`, `/usr/share/doc/libexif12/copyright`)

- `BSD-3-Clause`
- `CC0-1.0`
- `GPL-2`
- `GPL-2.0`
- `LGPL-2.1`
- `LGPL-2.1-or-later`
- `LicenseRef-Wrobel`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libexif=0.6.25-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25-1build1.dsc' libexif_0.6.25-1build1.dsc 2094 SHA512:35e396413081168b646e53e9eacedd53348b15a36000d0c94ab14a2e3d5484b1880f1537a171965f8e9b6275af983ec6f56f1f6954707f17cc205891640ceba7
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25.orig.tar.gz' libexif_0.6.25.orig.tar.gz 1253324 SHA512:9e42af0d898a9d832d7b146a2085fb08eafdbb5ae476184aee1b495632172749d910f581246d22a0c68382ea9d969de54bd9539d4d877ad4dd6ca989e1b6d8db
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25-1build1.debian.tar.xz' libexif_0.6.25-1build1.debian.tar.xz 12168 SHA512:91b9f12dba5a963cd7e2a5cfff225a287835fdb3460a5c22738d20f701c004efa5898b2c4e39210aebaf9af6420b795ac6122e7a9d334f56ad073e15c7847df3
```

### `dpkg` source package: `libffi=3.5.2-3`

Binary Packages:

- `libffi-dev:amd64=3.5.2-3`
- `libffi8:amd64=3.5.2-3`

Licenses: (parsed from: `/usr/share/doc/libffi-dev/copyright`, `/usr/share/doc/libffi8/copyright`)

- `Expat`
- `GPL`
- `GPL-2+`
- `GPL-3+`
- `LGPL-2.1+`
- `MPL-1.1`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libffi=3.5.2-3
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2-3.dsc' libffi_3.5.2-3.dsc 1954 SHA512:52348c55c957433105c47137fab4d787071580bea2199949b5982be59ba46d81fd43639e23e906bbe362706371e6bae8fe5cd08a6f68a6bc8f2fe2e611bae91a
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2.orig.tar.gz' libffi_3.5.2.orig.tar.gz 598870 SHA512:4579932becbe33b2cb3c7a6327a9b47fee67f225ebb4677870ed4402bb7c186966a5b8645dc8a09128af51dcba27c23537e6a34567dbea4e3dc3728cfb51e038
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libffi/libffi_3.5.2-3.debian.tar.xz' libffi_3.5.2-3.debian.tar.xz 10928 SHA512:ee5ecb07a2b656c2c269a2e906792e2eac86cb167e2be9012a4bada201b47072fa5bfe4e55769927e2490b7b7859e821712b4a15ab0af8a73e1faaa7d23943dd
```

### `dpkg` source package: `libfido2=1.16.0-2build1`

Binary Packages:

- `libfido2-1:amd64=1.16.0-2build1`

Licenses: (parsed from: `/usr/share/doc/libfido2-1/copyright`)

- `BSD-2-clause`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libfido2=1.16.0-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.16.0-2build1.dsc' libfido2_1.16.0-2build1.dsc 2246 SHA512:9a11874aec83568ca3af3dea8acbdf91c700b684b2f08b62209bea851ee255c7516b841078fcc2a7b3ab577968ad08b35ba817ba625e9edd912a1e3a3acd3813
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.16.0.orig.tar.xz' libfido2_1.16.0.orig.tar.xz 599884 SHA512:f85b5f8bb8c85a4371035f2875eb70f0e8dc8450279020d853cc19e200e4e68bddf93829b7c7675ac078e3b04c267e8cc6fb044302b9080913e2ba89e877cc38
'http://archive.ubuntu.com/ubuntu/pool/main/libf/libfido2/libfido2_1.16.0-2build1.debian.tar.xz' libfido2_1.16.0-2build1.debian.tar.xz 65876 SHA512:a9be47e2be7fa51b964e8e9e3af9f542fb8cca342e52c3bbeff3bb30748eeeaa3a89ed70512d44c327c3a82745a7fb4fbf0ecad32b7b75c5252ecee0b849f229
```

### `dpkg` source package: `libgcrypt20=1.11.2-3`

Binary Packages:

- `libgcrypt20:amd64=1.11.2-3`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.11.2-3
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.2-3.dsc' libgcrypt20_1.11.2-3.dsc 2945 SHA512:a68caae63f6f21910bf0794ea9826930bc4e712e53669a2e670b8b2fb05e4ee13cacf9d3a46b15bcd730f636bc89bd65c00547f34dfce1e61aae64349eb4c410
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.2.orig.tar.bz2' libgcrypt20_1.11.2.orig.tar.bz2 4237802 SHA512:b706cea602cc8f0896e57ce979643bf78974b05faec27c1b053b773c57d8b04250e30e95a4ef5899e1df981d01d8d08f0a36e10b5820a5ec4183e74c02e5f1f0
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.2.orig.tar.bz2.asc' libgcrypt20_1.11.2.orig.tar.bz2.asc 265 SHA512:236edbd12f904a75497eba1b04fd79826a9553406a4301f90e91c5598d4b6ae9f20b894027ae8f5e821d776fbaef3c8203b9ee6e077e5659782ce750aecd5e57
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.11.2-3.debian.tar.xz' libgcrypt20_1.11.2-3.debian.tar.xz 43012 SHA512:bf95402293c26873a8a29996b66d16e657c322073b54ad3e72a4eb1b69807e1fdf2b48b296b4427191a4466d06afdcc6e60c1c292c83a93fca42380beba7f474
```

### `dpkg` source package: `libgpg-error=1.58-1`

Binary Packages:

- `libgpg-error0:amd64=1.58-1`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libgpg-error/1.58-1/


### `dpkg` source package: `libheif=1.21.2-1`

Binary Packages:

- `libheif-plugin-aomdec:amd64=1.21.2-1`
- `libheif-plugin-libde265:amd64=1.21.2-1`
- `libheif1:amd64=1.21.2-1`

Licenses: (parsed from: `/usr/share/doc/libheif-plugin-aomdec/copyright`, `/usr/share/doc/libheif-plugin-libde265/copyright`, `/usr/share/doc/libheif1/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-Clause-UC`
- `BSL-1.0`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libheif=1.21.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.21.2-1.dsc' libheif_1.21.2-1.dsc 3713 SHA512:c189b7577c51382aa72e1c18670bde351480a10fffd9af978f1ce12c093d049a841377215d30332217f097dbbe907597af8ee2f65ff5c10772cbaf2596877098
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.21.2.orig.tar.gz' libheif_1.21.2.orig.tar.gz 1859435 SHA512:ec7cf3a1ceafc6df01fa57b488c763da8b88971f01b71385d377036e4301d1145d743af942654e5b741468fd9d0c8ab520a9bf205c5a7d3cdd60767cec4df232
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.21.2-1.debian.tar.xz' libheif_1.21.2-1.debian.tar.xz 13144 SHA512:afb5c7df0c0892d323da7f2975efac2a1a99164f25f1520d9b2830efb5037ffbad519270c6ebdd96da16e59a2c5a1dbca9756260ec91f322662be44f4205d151
```

### `dpkg` source package: `libice=2:1.1.1-1build1`

Binary Packages:

- `libice-dev:amd64=2:1.1.1-1build1`
- `libice6:amd64=2:1.1.1-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libice=2:1.1.1-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.1.1-1build1.dsc' libice_1.1.1-1build1.dsc 2016 SHA512:1ef7154cfc349ddc73424d9c552e8d9fa879ace62ba21049e102c973bfa8a041162ac4490783c9ca242da7b3b19ca24c7e48cff86ce97fe26f41e777e6527492
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.1.1.orig.tar.gz' libice_1.1.1.orig.tar.gz 489944 SHA512:e39fc7f76c19c4edc3e520b7cef16f9f65c4723f4d3603f7e664c54a5fe8fdd756f9a8bb2dc3b0ccf6646a8d1d202cba1cfa220e160b32e233a37c2cc7d13f1d
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libice/libice_1.1.1-1build1.diff.gz' libice_1.1.1-1build1.diff.gz 7407 SHA512:d23aff3f69b2f8435bdf6f960777c0cae9e006ffe561683011ead538eb5b2a1f6fe42ec9d7f91fe06ea822ac4b609f817d1006bed045688d2c30636057060347
```

### `dpkg` source package: `libidn2=2.3.8-4build1`

Binary Packages:

- `libidn2-0:amd64=2.3.8-4build1`
- `libidn2-dev:amd64=2.3.8-4build1`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`, `/usr/share/doc/libidn2-dev/copyright`)

- `Expat`
- `FSFAP`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.3.8-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8-4build1.dsc' libidn2_2.3.8-4build1.dsc 2566 SHA512:d4bf0877b73ac25260322cfc2bc08de753fab0ec9dcb6b058023f5e1fcae5859e8473b880c9aae23564e9363fc7b84de749626d5b4b971787d217064daaac09b
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz' libidn2_2.3.8.orig.tar.gz 718637 SHA512:e3f4ec5113f531d2b1827a11d7292318fdc49032c013b0076911b075b0e879428db9b45fe137aa37bf9c60e672b6883c035f9f45b2b42625031534965d518bc1
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8.orig.tar.gz.asc' libidn2_2.3.8.orig.tar.gz.asc 1223 SHA512:f5c7f1676018b1cd362e250dd8ad59150c34b11ede9a21dbaf6f2e88fa943c881db6e59bf3e9180567379173cb21c4c893d835db99f4ed9e94bd80f84fb8ee2c
'http://archive.ubuntu.com/ubuntu/pool/main/libi/libidn2/libidn2_2.3.8-4build1.debian.tar.xz' libidn2_2.3.8-4build1.debian.tar.xz 18192 SHA512:6994c4e028b02b383268101f0274940bb2bbc9067c33948095c5275e906add9570500f8cbc91974e8de85f2db0d4f6853f68b2586bf2fd2baa9e72c2925e75d8
```

### `dpkg` source package: `libjpeg-turbo=2.1.5-4ubuntu3`

Binary Packages:

- `libjpeg-turbo8:amd64=2.1.5-4ubuntu3`
- `libjpeg-turbo8-dev:amd64=2.1.5-4ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libjpeg-turbo8/copyright`, `/usr/share/doc/libjpeg-turbo8-dev/copyright`)

- `BSD-3-clause`
- `BSD-BY-LC-NE`
- `Expat`
- `NTP`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libjpeg-turbo=2.1.5-4ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-4ubuntu3.dsc' libjpeg-turbo_2.1.5-4ubuntu3.dsc 2523 SHA512:7d0041cc84e48250f0ea1258e8ff8ac24a0afb3f440c69845fe939038574df6311fc24bbeafd2b894de137c44d9f6129278b45e92a0967b0970723d1f90edf20
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5.orig.tar.gz' libjpeg-turbo_2.1.5.orig.tar.gz 2264471 SHA512:20036303fbe5703a5742dc3778cc5deb2eb98d00a9852e7e80ba73c195bba011ec206c090589c482f1153f74505c3fe06d96af00f6beaa65a7fcf7ffaf626fc2
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg-turbo/libjpeg-turbo_2.1.5-4ubuntu3.debian.tar.xz' libjpeg-turbo_2.1.5-4ubuntu3.debian.tar.xz 109132 SHA512:9d9d1e2fd2194b3551f0e00441360371c3eb6ce6719803b288271bed32e014421267f0ca61977234ca9e6c7e9d31fe5a3d41bc91662555b27c7b4961c04ad9c6
```

### `dpkg` source package: `libjpeg8-empty=8c-2ubuntu12`

Binary Packages:

- `libjpeg-dev:amd64=8c-2ubuntu12`
- `libjpeg8:amd64=8c-2ubuntu12`
- `libjpeg8-dev:amd64=8c-2ubuntu12`

Licenses: (parsed from: `/usr/share/doc/libjpeg-dev/copyright`, `/usr/share/doc/libjpeg8/copyright`, `/usr/share/doc/libjpeg8-dev/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libjpeg8-empty=8c-2ubuntu12
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu12.dsc' libjpeg8-empty_8c-2ubuntu12.dsc 1579 SHA512:6e58a6aafe3537c18e1757666c02b4e397979c336ec5bfc8fa1dde30e5e468aa2bb81172887bb12dd669e41eda2b1e0fbc94008218a673c5fa0c541183a2de48
'http://archive.ubuntu.com/ubuntu/pool/main/libj/libjpeg8-empty/libjpeg8-empty_8c-2ubuntu12.tar.gz' libjpeg8-empty_8c-2ubuntu12.tar.gz 2021 SHA512:a0c6674b02abc13ce3e420d99c13f099fb854fb4ea2c29380d3446064bb13e837f452a81e85f2db655f6f5b0d52efdd02c0a0ad7caa31adfa1ce8ab0b1645aed
```

### `dpkg` source package: `libksba=1.6.7-2build1`

Binary Packages:

- `libksba8:amd64=1.6.7-2build1`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `FSFUL`
- `GPL-3`
- `LGPL-2.1-or-later`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.6.7-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7-2build1.dsc' libksba_1.6.7-2build1.dsc 2506 SHA512:46a2817fba077f8e55afa5f251b64f46c63a5afa8638eaf1481ca2456a93f83c6117d26d74a634b3b9e29de07f252eac9b7deb839f67dc6770524b2a3a3a249b
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2' libksba_1.6.7.orig.tar.bz2 706437 SHA512:60cb9df9f502ca479818f45b78c4bc2b78f6f359be2b8da489ea98f8896a43ab2c20cf97526b79a3220fb32f1701e62a6481fe61e91e567186ecf4f33d8e64d3
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7.orig.tar.bz2.asc' libksba_1.6.7.orig.tar.bz2.asc 228 SHA512:66208b8e4fe76a753943f13a0e65b765eb496013f7f9aeb0b66a454dfb8c67794d1b70841a4014ef0c7ac4642d7b56c38b35cb34be9d8ee8ea6820cc13db53aa
'http://archive.ubuntu.com/ubuntu/pool/main/libk/libksba/libksba_1.6.7-2build1.debian.tar.xz' libksba_1.6.7-2build1.debian.tar.xz 14928 SHA512:dc92b03ca9390333cb728f8b2f82c1916d57645f49cec39104c99013df57cdcdb57956bb26c35a9925ae49ac0170b8c6b43004694b6c99bc459cbb73f1c932c5
```

### `dpkg` source package: `liblqr=0.4.2-2.2`

Binary Packages:

- `liblqr-1-0:amd64=0.4.2-2.2`
- `liblqr-1-0-dev:amd64=0.4.2-2.2`

Licenses: (parsed from: `/usr/share/doc/liblqr-1-0/copyright`, `/usr/share/doc/liblqr-1-0-dev/copyright`)

- `GPL-3`
- `GPLv3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris liblqr=0.4.2-2.2
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.2.dsc' liblqr_0.4.2-2.2.dsc 1953 SHA512:30fa17af4256ed8c49bd2a89750500c8c8ffcf52b15573b598dc880e94f7145ce3f501b96485d540d6f1971065c53b2d76fca22180176414c719b6651934661d
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2.orig.tar.gz' liblqr_0.4.2.orig.tar.gz 439884 SHA512:acfa5868c41ea145092711e84d6c9eb62cb725b3d7531917b0d91b7d4af2a9912b18a96edc2594a826f09dabe0a0a82936ceea7d1f31301a23d558b1450d2547
'http://archive.ubuntu.com/ubuntu/pool/universe/libl/liblqr/liblqr_0.4.2-2.2.debian.tar.xz' liblqr_0.4.2-2.2.debian.tar.xz 5788 SHA512:d3388db0d00e34b5d638772f9925571a954e5648ba5000355cde35e37dfd058a665f2944960b2b155c2083c0e417e4bd3baeaf293a6941160c506a9137e23985
```

### `dpkg` source package: `libmaxminddb=1.12.2-1build2`

Binary Packages:

- `libmaxminddb-dev:amd64=1.12.2-1build2`
- `libmaxminddb0:amd64=1.12.2-1build2`

Licenses: (parsed from: `/usr/share/doc/libmaxminddb-dev/copyright`, `/usr/share/doc/libmaxminddb0/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`
- `LGPL-3`
- `LGPL-3.0+`

Source:

```console
$ apt-get source -qq --print-uris libmaxminddb=1.12.2-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2-1build2.dsc' libmaxminddb_1.12.2-1build2.dsc 2259 SHA512:9c638235f8932844154f683d71a4c0fc95bdda68c1cde77b09bfc178fda4c92bb2abd6d384013f7122594ebeaba5b90678eb515c6f13ce39f920a34b212784d4
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2.orig.tar.gz' libmaxminddb_1.12.2.orig.tar.gz 369848 SHA512:88cbccecba2025128babcfb0102f7688982194601974bd3ceaa45ec1bd535e5b6a50c2ce2f214ba5774959987cc64e7f686f76e11672555c690b57a51b1575fa
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmaxminddb/libmaxminddb_1.12.2-1build2.debian.tar.xz' libmaxminddb_1.12.2-1build2.debian.tar.xz 7056 SHA512:12a870767fb24ba54402ed976b7a9a7f9a04e33b7af34b17a31a4fd2fd8bc21b274ef845f2fc0460ed5b852f2072694b16ec4550c7d42558b6bed98208eb1285
```

### `dpkg` source package: `libmd=1.1.0-2build3`

Binary Packages:

- `libmd0:amd64=1.1.0-2build3`

Licenses: (parsed from: `/usr/share/doc/libmd0/copyright`)

- `BSD-2-clause`
- `BSD-2-clause-NetBSD`
- `BSD-3-clause`
- `BSD-3-clause-Aaron-D-Gifford`
- `Beerware`
- `ISC`
- `public-domain-md4`
- `public-domain-md5`
- `public-domain-sha1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libpng1.6=1.6.55-1`

Binary Packages:

- `libpng-dev:amd64=1.6.55-1`
- `libpng16-16t64:amd64=1.6.55-1`

Licenses: (parsed from: `/usr/share/doc/libpng-dev/copyright`, `/usr/share/doc/libpng16-16t64/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `BSD-like-with-advertising-clause`
- `GPL-2`
- `GPL-2+`
- `expat`
- `libpng`
- `libpng OR Apache-2.0 OR BSD-3-clause`

Source:

```console
$ apt-get source -qq --print-uris libpng1.6=1.6.55-1
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.55-1.dsc' libpng1.6_1.6.55-1.dsc 2254 SHA512:157b278d6940ad74f9963b8da1ab56f54f2d669cbfac45112e2305bc6e17d8d9092c86f119088be04026eac8462482fc2220108124ee8893bc2ff98ee4d51f0f
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.55.orig.tar.gz' libpng1.6_1.6.55.orig.tar.gz 1586616 SHA512:98ce4acef95ab92ec03039fa0b60b229c0ca607bf1bbe4295f92c638940ecd2d03aba63186ee837b063c09f8176de4987853df96549436c90f588d69f9061a3c
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpng1.6/libpng1.6_1.6.55-1.debian.tar.xz' libpng1.6_1.6.55-1.debian.tar.xz 33544 SHA512:9877b447142441e40712d119b7b09f3fe46035256f30d6db31e68b598f686803645a09e512e900de1a37633178bc3a69434100c0e4431488a26e7957c72223b4
```

### `dpkg` source package: `libpsl=0.21.2-1.1build2`

Binary Packages:

- `libpsl-dev:amd64=0.21.2-1.1build2`
- `libpsl5t64:amd64=0.21.2-1.1build2`

Licenses: (parsed from: `/usr/share/doc/libpsl-dev/copyright`, `/usr/share/doc/libpsl5t64/copyright`)

- `Chromium`
- `MIT`
- `gnulib`

Source:

```console
$ apt-get source -qq --print-uris libpsl=0.21.2-1.1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build2.dsc' libpsl_0.21.2-1.1build2.dsc 2388 SHA512:9736ca1e4a00bbb2ce19eaf7a7e04e98fb5dfcc51f8ecfc2ce0eb6785708f34aabfea67ee63f01a4af5eca9d17b4941b16a0a803f2b79021f2d87fb8895e97b8
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2.orig.tar.xz' libpsl_0.21.2.orig.tar.xz 1870352 SHA512:5308feee863b84705246ce303c093e0c9fecd948ab382fd7480e9ea1ca5f72de42fc2c8f70472a97603580a3fd1eb2b552b093d79756e9fe93effba9f25b6aa4
'http://archive.ubuntu.com/ubuntu/pool/main/libp/libpsl/libpsl_0.21.2-1.1build2.debian.tar.xz' libpsl_0.21.2-1.1build2.debian.tar.xz 12292 SHA512:7b9235d134029f52920c657e163738c1dd319ea5e9862a3d3e8f7619a6d6b72c23ba0130a454201a52ed943b117d6be770ac2ab11cae59d6679a7da01872398f
```

### `dpkg` source package: `libraw=0.21.4-2`

Binary Packages:

- `libraw23t64:amd64=0.21.4-2`

Licenses: (parsed from: `/usr/share/doc/libraw23t64/copyright`)

- `CC-BY-SA-3.0`
- `CDDL-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libraw=0.21.4-2
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.4-2.dsc' libraw_0.21.4-2.dsc 2187 SHA512:fa920e02921a34543f86a5433821165f324f84e58293121da452ca7db48a21739f84a46f5581d0e300e35d8475c88a132384b0345659759dfa71b4d093aef5d7
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.4.orig.tar.gz' libraw_0.21.4.orig.tar.gz 566327 SHA512:d8366d62f32f02466128ecfedf9a9b39289834a73d89d57004cf7df63919e66808ba283cddf5843b25fe903d72eb988ac5b490525083e2b5d84a05c7679b4014
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.4-2.debian.tar.xz' libraw_0.21.4-2.debian.tar.xz 24312 SHA512:baa743a17360c6acf002d628e1b7a8c8fea3c6d6aaaa160e991f7fbc9252217ac1e0c0d642062b200f2a0e1b27f31bde1fa9a40c915a6a515594fd71f04fb1e6
```

### `dpkg` source package: `libseccomp=2.6.0-2ubuntu3`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libselinux=3.9-4`

Binary Packages:

- `libselinux-dev:amd64=3.9-4`
- `libselinux1:amd64=3.9-4`

Licenses: (parsed from: `/usr/share/doc/libselinux-dev/copyright`, `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.9-4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.9-4.dsc' libselinux_3.9-4.dsc 2905 SHA512:690e8bd153b1f9bb81620e47c69a68953b38fad796478a202a9888746eeeef42709588a78bdc105f09c6c07578268e45d263a1171e3d03a103efbd5eb773b0c0
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.9.orig.tar.gz' libselinux_3.9.orig.tar.gz 205334 SHA512:a91942e7d16673396610d969f2471173989995a048edacf6076f6df3200a0d541a1c9932a7632d70aa7c728de7e7d3c62712e5aab6c0b763826e7ffef808cadb
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.9.orig.tar.gz.asc' libselinux_3.9.orig.tar.gz.asc 833 SHA512:20bd4eaa75c0830b10fa8116ab787ca9d5099330c270e2e620220144b9fd239e1e2ca1ddc7ea79c1c3c6863b672530b4f875d6e68043de0da44e035b42d7d132
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.9-4.debian.tar.xz' libselinux_3.9-4.debian.tar.xz 38096 SHA512:862f74bbb23bcfadf517c5a669d65d3242fd28c9bd35090b0195231d3ac9042450b1d8248f0dc02c409de6ad85c6183dbcc2ae4ff913b4f33515b97936a0c5e8
```

### `dpkg` source package: `libsemanage=3.8.1-1build1`

Binary Packages:

- `libsemanage-common=3.8.1-1build1`
- `libsemanage2:amd64=3.8.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libsepol=3.9-2`

Binary Packages:

- `libsepol-dev:amd64=3.9-2`
- `libsepol2:amd64=3.9-2`

Licenses: (parsed from: `/usr/share/doc/libsepol-dev/copyright`, `/usr/share/doc/libsepol2/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris libsepol=3.9-2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.9-2.dsc' libsepol_3.9-2.dsc 2326 SHA512:8402a41b450fc815c37dd8163905ff9f04ae692372dd0ff7ed1aacd2d22144e2096ad69bb49685b0853317d7d11f870e2fecc30c76a4f6297407e6b2207d4e74
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.9.orig.tar.gz' libsepol_3.9.orig.tar.gz 515726 SHA512:9a198fb0b7f4981939e6556ba690892bda77446785c2015cdf4178fa303095186f255dfbebe04e6749a139379718a012349aa7a70fac94a860a3745c0536afe9
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.9.orig.tar.gz.asc' libsepol_3.9.orig.tar.gz.asc 833 SHA512:a84d39be1ab744d70c6df7f170f429f6625218e304c748317188670202de6bc2175a88b4b006c451aa3874c28881fbe09f6dfcc13022f3cbbef2acd4a886a992
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsepol/libsepol_3.9-2.debian.tar.xz' libsepol_3.9-2.debian.tar.xz 21416 SHA512:f5c99799993c4950352f43c7e5fdae4383eb8f8ecabb50b51812ccdad8250cc31090348eef26da2ac9f6c4a66b4313607514249edd7eafd17ea1f6adfb047a97
```

### `dpkg` source package: `libsm=2:1.2.6-1build1`

Binary Packages:

- `libsm-dev:amd64=2:1.2.6-1build1`
- `libsm6:amd64=2:1.2.6-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libsm=2:1.2.6-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6-1build1.dsc' libsm_1.2.6-1build1.dsc 2326 SHA512:6f74042e720c5f5266682b71e586652599e0c14080732e37dd58c7bcb686723cbc1ce9230ace07f64b366a1e747cc34575843c5fa79f509fd569e8986234a597
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz' libsm_1.2.6.orig.tar.gz 467497 SHA512:316df49f1573ace0bccbfcdf2b1d22c91ec7a1ceb5b320d142fd33cca81e0e0582a0256764aef594f9b31ac5f63d8823dc04c8a6113019ec54ee26eb9323ded4
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6.orig.tar.gz.asc' libsm_1.2.6.orig.tar.gz.asc 833 SHA512:b7a617bc09cdc9e4298576f014932165f6b3cc2dd3f96d35db92f46b7f93260705b37f501fbdefb5810eb8f64f64d9260c39cc5ad7660d226b292804798711ee
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsm/libsm_1.2.6-1build1.diff.gz' libsm_1.2.6-1build1.diff.gz 13398 SHA512:91da35c944e1bac99cf78fa935fbf6618ce2d5738e9181a4423a279ea5ce26f8b9b98b81985f21ee6e803d424b49887ef3dd265396f2f9d2661531019f7833db
```

### `dpkg` source package: `libssh2=1.11.1-1build1`

Binary Packages:

- `libssh2-1-dev:amd64=1.11.1-1build1`
- `libssh2-1t64:amd64=1.11.1-1build1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1-dev/copyright`, `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.1-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1-1build1.dsc' libssh2_1.11.1-1build1.dsc 2343 SHA512:b8255d13b5f547f6ea8d438b7a147c88467decfd2f08b432bfde885f3e03a294c8471b38c62bb17985706a8fa67a29208d5432189ad1c8f655089df9662ebdd1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz' libssh2_1.11.1.orig.tar.gz 1093012 SHA512:8703636fc28f0b12c8171712f3d605e0466a5bb9ba06e136c3203548fc3408ab07defd71dc801d7009a337e1e02fd60e8933a2a526d5ef0ce53153058d201233
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz.asc' libssh2_1.11.1.orig.tar.gz.asc 488 SHA512:83e600ddd676013932297c4f3d2cf2e65b5308f7700d818b34f30d760c7495180e6d8dae70579c8bea95ea2d7ccb12fc42641e545e11ec4b6630a0e6b350b282
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1-1build1.debian.tar.xz' libssh2_1.11.1-1build1.debian.tar.xz 17220 SHA512:a294d9e0354ddeff5656511853924f785d98eb9052f7a9c8c550f3e3b14cfde1a9bd38c2ed299472b67df54a49171793657fa836e084df2f4539ddfe08b5058e
```

### `dpkg` source package: `libtasn1-6=4.21.0-2`

Binary Packages:

- `libtasn1-6:amd64=4.21.0-2`
- `libtasn1-6-dev:amd64=4.21.0-2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`, `/usr/share/doc/libtasn1-6-dev/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.21.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.21.0-2.dsc' libtasn1-6_4.21.0-2.dsc 2665 SHA512:d83f16d2fbc66bb6bfa26f17efa2f910a9e5e4db86c6fde245782806c6a3819c1b7210d3375a6adc9615549d0f0ddee3e0935fabd39df14bd8a70e2608412ad2
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.21.0.orig.tar.gz' libtasn1-6_4.21.0.orig.tar.gz 1816537 SHA512:6a581c4c072b168bf29a0dec7e59a9329a798e392b7d1033791d0e3166a5d1164e2a7065373a84018d500a01563657900c318b1fd437c227c3174b754f9998d3
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.21.0.orig.tar.gz.asc' libtasn1-6_4.21.0.orig.tar.gz.asc 1223 SHA512:2347e04e9214b295fd20490a237ae394f02cb26950a07456364311437c23324728fa9547f83ceba2ba829a5473c004e129cf72a891e50a2f4f96f16ee37a0bb9
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtasn1-6/libtasn1-6_4.21.0-2.debian.tar.xz' libtasn1-6_4.21.0-2.debian.tar.xz 19408 SHA512:4350fffbed87dae2a7919bf02857f2094a03a5f64555c04c0ff78819ac3899139f0fc8028ee2ffc9750d8488f37f8db68e5eb8a0e9d4bd36369da681fa942a44
```

### `dpkg` source package: `libtext-charwidth-perl=0.04-11build4`

Binary Packages:

- `libtext-charwidth-perl:amd64=0.04-11build4`

Licenses: (parsed from: `/usr/share/doc/libtext-charwidth-perl/copyright`)

- `Artistic`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-charwidth-perl=0.04-11build4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11build4.dsc' libtext-charwidth-perl_0.04-11build4.dsc 2265 SHA512:0fe85b9e64a3837989d81ace4214eb550cb80d6a7895f572c8e043021bca9f44cc43c32965ed66bf018dbb034aa0cc7ac2800e9782a9b64ce4c3589e1db1ac9f
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04.orig.tar.bz2' libtext-charwidth-perl_0.04.orig.tar.bz2 8327 SHA512:37e47e23557a14fac3d1471017a2a9b637fa2c8a0b11d3feedfa40a2f2fdf48dbb7f1d9d855f5e56733e3da09436fd7e73360b105aa24194f31aabd8e87dddb4
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-charwidth-perl/libtext-charwidth-perl_0.04-11build4.debian.tar.xz' libtext-charwidth-perl_0.04-11build4.debian.tar.xz 3228 SHA512:cc89f58b8bc90cada87a10519f99aa344436eaa631b2fe5f09b817c9df8bf1ee761c35096d88329b9e4c52b8fd091ac68bbac258d86d4bd0a0a653f7b39b52ef
```

### `dpkg` source package: `libtext-wrapi18n-perl=0.06-10`

Binary Packages:

- `libtext-wrapi18n-perl=0.06-10`

Licenses: (parsed from: `/usr/share/doc/libtext-wrapi18n-perl/copyright`)

- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris libtext-wrapi18n-perl=0.06-10
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.dsc' libtext-wrapi18n-perl_0.06-10.dsc 1829 SHA512:77c1d3d64cd6e31939367f8a5d5d8d5d1b0c4d3a9b2fd8edaf834b687ba9f212b6f33bfd708bb5983a51c7eb2f8e9058a26e3416526d681e6a9d87006399aa60
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06.orig.tar.gz' libtext-wrapi18n-perl_0.06.orig.tar.gz 3797 SHA512:08b26bae38eea906ced417f88b494862e5485fe8d8ddf8bc69582b57d3d427393ba6bec9320e79541ccd7d63b20c6c7e5194ccd649cf79ef7caf9892c757ad96
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtext-wrapi18n-perl/libtext-wrapi18n-perl_0.06-10.debian.tar.xz' libtext-wrapi18n-perl_0.06-10.debian.tar.xz 3452 SHA512:490da004cdfe1b1ff967deef2846de80e8868b8aa0faef501097509c5d0bf8c814defb3d760be9ffae782e8fe3f4a5640ddfe222e59ab733aec4bc3b9d15ced7
```

### `dpkg` source package: `libthai=0.1.30-1`

Binary Packages:

- `libthai-data=0.1.30-1`
- `libthai0:amd64=0.1.30-1`

Licenses: (parsed from: `/usr/share/doc/libthai-data/copyright`, `/usr/share/doc/libthai0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libthai=0.1.30-1
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.30-1.dsc' libthai_0.1.30-1.dsc 2301 SHA512:043b70b803d06f3a472c724f5e43832691da022f992c0ee47b0afededd522100a22f884e9d4caf16ee0c822645044e46c8e089531b42aac5da40e3eee8f92d4b
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.30.orig.tar.xz' libthai_0.1.30.orig.tar.xz 436044 SHA512:c84d575b6855d54b1ea1d9878a94153ba7807cc736f7bf01327d17a6444c6fd4b18deae2ab5a2612847892c9d94ed4ceb54fbf25244aa6eb88a3605260ad328e
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libthai/libthai_0.1.30-1.debian.tar.xz' libthai_0.1.30-1.debian.tar.xz 12652 SHA512:ec2c7bb9d9ed9bb870c45fe19a7bd643077e01164c414f846248c9d8b10099f86195c1f530997e0735a8db7e0cc525623702e5b8b2e2f4013a9db3a450b8f9fd
```

### `dpkg` source package: `libtool=2.5.4-9`

Binary Packages:

- `libltdl-dev:amd64=2.5.4-9`
- `libltdl7:amd64=2.5.4-9`
- `libtool=2.5.4-9`

Licenses: (parsed from: `/usr/share/doc/libltdl-dev/copyright`, `/usr/share/doc/libltdl7/copyright`, `/usr/share/doc/libtool/copyright`)

- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris libtool=2.5.4-9
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.5.4-9.dsc' libtool_2.5.4-9.dsc 2240 SHA512:1b4e549bcc6a9ca2320f924e3f037e38d4baf0d1931625508e19890b1364d1af3c551cf8868ad997cdc394678cf667358b4b82b704f4bd1c7c7662fc3cbd1eae
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.5.4.orig.tar.xz' libtool_2.5.4.orig.tar.xz 1069572 SHA512:c8ff1fc71373313185ecfff8d282bf3547b8a2d2e102aa4475d7db4945d4f4bfd45cd0d79a8e00a1c1394246908e586f8ccfd9f1cf86ff837b5c6ad7cc57a750
'http://archive.ubuntu.com/ubuntu/pool/main/libt/libtool/libtool_2.5.4-9.debian.tar.xz' libtool_2.5.4-9.debian.tar.xz 41704 SHA512:9804cec0963da794b3afed53a426a9ba836404ef3cb9f91f532129ef3c65636d93c17f4a014d5fdbf3da9b33f467752814cec5887c16253baef0b79f168655b5
```

### `dpkg` source package: `libunistring=1.3-2`

Binary Packages:

- `libunistring5:amd64=1.3-2`

Licenses: (parsed from: `/usr/share/doc/libunistring5/copyright`)

- `BSD-3-clause`
- `FreeSoftware`
- `GFDL-1.2+`
- `GFDL-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-2+ with distribution exception, Expat`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode-DFS-2016`
- `X11`
- `bsd-3-clause`
- `gfdl-1.2+`
- `gfdl-1.3+`
- `isc`
- `public-domain`
- `unicode-dfs-2016`

Source:

```console
$ apt-get source -qq --print-uris libunistring=1.3-2
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-2.dsc' libunistring_1.3-2.dsc 2215 SHA512:b5f352f94a03ff54581afe4cd88b1e5ffac6ae7fd45c95bc55f2cc3de24090a0c18d948a43405443388d42e537488c36d4638e33b81061f45f5c591d472148f9
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz' libunistring_1.3.orig.tar.xz 2753448 SHA512:864d42b1d4ae4941fe5c8327d6726ab8e3a35d2d5f9d25ce4859a72ab2f549a7b68f58638cf8767d863f58161d1a4053495d185860964a942d6750e42facf931
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz.asc' libunistring_1.3.orig.tar.xz.asc 833 SHA512:829229528acc8f9d13de4c43fea6caddacaf1f1cc201a7927b2c140d7ac5a81e213a1a20ba67766d6867fbe301ddddf78685f5af54e67906160807d6e8028b5a
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-2.debian.tar.xz' libunistring_1.3-2.debian.tar.xz 28480 SHA512:31079e73da30c7e0eab7bf1fa81936d2655df6f7d216fdfae418c54b8c168828d467af9cde17c2f9102a4479260c74a63cb50701ede8652097efbe47eb6086e5
```

### `dpkg` source package: `libwebp=1.5.0-0.1build1`

Binary Packages:

- `libsharpyuv-dev:amd64=1.5.0-0.1build1`
- `libsharpyuv0:amd64=1.5.0-0.1build1`
- `libwebp-dev:amd64=1.5.0-0.1build1`
- `libwebp7:amd64=1.5.0-0.1build1`
- `libwebpdecoder3:amd64=1.5.0-0.1build1`
- `libwebpdemux2:amd64=1.5.0-0.1build1`
- `libwebpmux3:amd64=1.5.0-0.1build1`

Licenses: (parsed from: `/usr/share/doc/libsharpyuv-dev/copyright`, `/usr/share/doc/libsharpyuv0/copyright`, `/usr/share/doc/libwebp-dev/copyright`, `/usr/share/doc/libwebp7/copyright`, `/usr/share/doc/libwebpdecoder3/copyright`, `/usr/share/doc/libwebpdemux2/copyright`, `/usr/share/doc/libwebpmux3/copyright`)

- `Apache-2.0`
- `BSD-3-Clause`

Source:

```console
$ apt-get source -qq --print-uris libwebp=1.5.0-0.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0-0.1build1.dsc' libwebp_1.5.0-0.1build1.dsc 2889 SHA512:085f6790e762ec35b9e9821085fd38d7788f5c7ab8d503f56d3b5d374f678b3cdcce147969a91ddd0e54bf8eaeafe9ffe331cf7b6ac3ed1cdc9fd5b0a5fb2a53
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz' libwebp_1.5.0.orig.tar.gz 4267494 SHA512:7a39594cf5585428f82d555b05e78aa63758a56841a313c0b74dfb4996afe37dddf92498d6123ff2a949a7209fb9097927f10ee75b5a38b481f110c892e5302b
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0.orig.tar.gz.asc' libwebp_1.5.0.orig.tar.gz.asc 833 SHA512:892e6240b767d7b47fc4faa337aa78f1426359e155c94305377510b0a0c8a24830597b261ebb458f6310338afde487616bd6cca3347b624d8f46500487a3c067
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwebp/libwebp_1.5.0-0.1build1.debian.tar.xz' libwebp_1.5.0-0.1build1.debian.tar.xz 11356 SHA512:c27b0795a00e022d91a881f438a6166fe7ea080bf6e758db487a6f033e81615a3061790a505a95f2baa9f7bc7fc07f80f3ce5f4435ef9e7f121039b95699cf02
```

### `dpkg` source package: `libwmf=0.2.13-2`

Binary Packages:

- `libwmf-0.2-7:amd64=0.2.13-2`
- `libwmf-dev=0.2.13-2`
- `libwmflite-0.2-7:amd64=0.2.13-2`

Licenses: (parsed from: `/usr/share/doc/libwmf-0.2-7/copyright`, `/usr/share/doc/libwmf-dev/copyright`, `/usr/share/doc/libwmflite-0.2-7/copyright`)

- `AGPL-3 with Font exception`
- `GD`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libwmf=0.2.13-2
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-2.dsc' libwmf_0.2.13-2.dsc 2368 SHA512:b683d69f0921cd71b1583dc5e275bc7617c4921dbf0cd5dc07516d097daa7feaeee136a1290c55ebf40b2afd5a116fcd1089b56c2045579c1a415fec55a5b0bd
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13.orig.tar.gz' libwmf_0.2.13.orig.tar.gz 3044235 SHA512:f45a936c9bc98fc1a5f2b0808b497119e4dcd3c132615fdddb7583e5719c7d1d7f85c16ebf313cad453e5b7ae3508bf6b80c4ed2b42322b7dec295d8f4eb86ce
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.13-2.debian.tar.xz' libwmf_0.2.13-2.debian.tar.xz 25572 SHA512:d8b7a3bd1ca33896637f45eabcea4e58d2ce3ecd6397ab1b6b32507c5d268e54be304178943c701bdd8d799962597e0d50d275f3a5c82649a116a0037c4bd099
```

### `dpkg` source package: `libx11=2:1.8.12-1build2`

Binary Packages:

- `libx11-6:amd64=2:1.8.12-1build2`
- `libx11-data=2:1.8.12-1build2`
- `libx11-dev:amd64=2:1.8.12-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.12-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12-1build2.dsc' libx11_1.8.12-1build2.dsc 2514 SHA512:3a3dd0be3e053666ab587cdbd9a966f0c59196dd8f84b82c65cda6c7c8059ff11d8c33e0f27b2251e517d279be9d38bb3984738392eb1a692ab98feee89f6218
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz' libx11_1.8.12.orig.tar.gz 3215077 SHA512:82d62d01176bbb8ee225f6dba741dcbccded62486ae4c70bc7158aa2a19dcf4a795ee9d475a875ed8843a4ae185eb4899d06dac4000b5fe8b5bbb5e13b450153
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12.orig.tar.gz.asc' libx11_1.8.12.orig.tar.gz.asc 833 SHA512:37b5f57a55cb75cb218937175ad06752ab85391c23ac91006a19fe32b82fc86f4b5eca11dba9b38c7d38efbf98aba3eeadcf3cf7bddf11175334ebe8e4d94d23
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.12-1build2.diff.gz' libx11_1.8.12-1build2.diff.gz 74635 SHA512:9407683de20881202f88d2b14ef905170a6ac074a0d123bb5165b481bf4743620eb949d267f1d62a88ca762faa24e657014a889fa7df5f7fbebc885731dd50bb
```

### `dpkg` source package: `libxau=1:1.0.11-1build2`

Binary Packages:

- `libxau-dev:amd64=1:1.0.11-1build2`
- `libxau6:amd64=1:1.0.11-1build2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxau=1:1.0.11-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11-1build2.dsc' libxau_1.0.11-1build2.dsc 2208 SHA512:29aadc79e789fb71f89c5335bd19b99311b1c9f63354ec8a67b4ed8155b01f34412a57cc3599b0d56eb5b436f6779af5c2186a28ab44a97fc0aa8b06e186b507
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz' libxau_1.0.11.orig.tar.gz 404973 SHA512:315625ae6657e817c09c83da53029488bd5140bc1048eef1072b12958457fdec6c41f79b190cf10885559d2e4c7d47110cd08369b438ca47749790c51edd8492
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11.orig.tar.gz.asc' libxau_1.0.11.orig.tar.gz.asc 358 SHA512:97e4425f90e720800cf91f45cf3dcb92b88017cba0db6fa4e39978ad8871b7312a048f4b51622176488edfb5b620ba0d6f0ffd087f0b177f9abfe3d8854fab30
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxau/libxau_1.0.11-1build2.diff.gz' libxau_1.0.11-1build2.diff.gz 22840 SHA512:2084201315eabcc07672ee0d46ca89034f76e157aad0763b0bb01b10ee5fb2b52e6ed1c9f57d4dd7d037d6c45f9249ce93b8117a763617e83ee187965b8c84f7
```

### `dpkg` source package: `libxcb=1.17.0-2ubuntu1`

Binary Packages:

- `libxcb-render0:amd64=1.17.0-2ubuntu1`
- `libxcb-shm0:amd64=1.17.0-2ubuntu1`
- `libxcb1:amd64=1.17.0-2ubuntu1`
- `libxcb1-dev:amd64=1.17.0-2ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcb=1.17.0-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0-2ubuntu1.dsc' libxcb_1.17.0-2ubuntu1.dsc 5425 SHA512:827e6431f4bd4301b15d5a080abc5a2f83d603586b3305dafcad17f29b45d0d5ee22e145be20d8e38840b4e6a0501d2504d348abe8872d7be5d2035a4cc3804a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0.orig.tar.gz' libxcb_1.17.0.orig.tar.gz 661593 SHA512:58624a33d39371a7ff58368ed5a09c1c31bea3abd040173db1d41018de4208bc52d2fb8cfd7382ff34d01b98d01a3e314a71a808533880564cd51cd96624a7bb
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcb/libxcb_1.17.0-2ubuntu1.diff.gz' libxcb_1.17.0-2ubuntu1.diff.gz 28420 SHA512:fbb3b8d42de598e210c083e6655a7c7ae827ec16be508e2f45a6662f2fd7c23455b485501199b168ebb874a97211748fb3dffcd5193747ab5e0efe37f1803ce6
```

### `dpkg` source package: `libxcrypt=1:4.5.1-1`

Binary Packages:

- `libcrypt-dev:amd64=1:4.5.1-1`
- `libcrypt1:amd64=1:4.5.1-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxcrypt=1:4.5.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.5.1-1.dsc' libxcrypt_4.5.1-1.dsc 2434 SHA512:3564b82caebdf85b4a85384ea44e532578e9a6f22f36b92bd048483f489226a1ea3587a10e0703ae206898c886fa6040c73a1fb6e1e4c864afd6442573020f2c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.5.1.orig.tar.xz' libxcrypt_4.5.1.orig.tar.xz 433264 SHA512:857e42b9680dbeb09d80316446738704d841ced7e0d1ae2148edb45bd1996fcc646e59ac26ec2dd79e9d765f5c151b89f970fd7d9ad4415223e022c3d5f384aa
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxcrypt/libxcrypt_4.5.1-1.debian.tar.xz' libxcrypt_4.5.1-1.debian.tar.xz 8684 SHA512:b3a5a0ecc7594f403975cd0c04648c0fc59c0418f4ce35eceff765d49fffd1f9ff49d97dd48a107e5db646bf388827e6beeb5eef234c9a1853ad7cec0580e969
```

### `dpkg` source package: `libxdmcp=1:1.1.5-2`

Binary Packages:

- `libxdmcp-dev:amd64=1:1.1.5-2`
- `libxdmcp6:amd64=1:1.1.5-2`

Licenses: (parsed from: `/usr/share/doc/libxdmcp-dev/copyright`, `/usr/share/doc/libxdmcp6/copyright`)

- `OpenGroup-MIT`

Source:

```console
$ apt-get source -qq --print-uris libxdmcp=1:1.1.5-2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5-2.dsc' libxdmcp_1.1.5-2.dsc 2269 SHA512:6e7ee900e8636a82589087d372ae48d11ca608307fd42a97d4354d11cdf73eced939b0bc4f11922b08996b005f12c68f7e63836920e61848bfce3eae74163d64
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz' libxdmcp_1.1.5.orig.tar.gz 442597 SHA512:400add8f47c28fe9cb80d6159a7268e7f5029d13a6219f3e07087455d99f807aa5b372242be9c14fbb7164b3c8180b8dc5edfeb620412bcbee246162f53c61d3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5.orig.tar.gz.asc' libxdmcp_1.1.5.orig.tar.gz.asc 833 SHA512:e44c62904e5680ede9c3188c2fcf8e453c09d5f89e2958be34196e6f1130177f2e7bbd324337b5ee1902817c09357be0144dd91c2b6fd4e943edebe532c5193c
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxdmcp/libxdmcp_1.1.5-2.diff.gz' libxdmcp_1.1.5-2.diff.gz 10201 SHA512:ee0b681b8333842665b248757caa26e765ca8dc687bff6bc4b52bc0e4374cfed0fd2596b6d4ec821c59137aa17196cd25b34a5c84a8a9fa187efba2362d6078b
```

### `dpkg` source package: `libxext=2:1.3.4-1build3`

Binary Packages:

- `libxext-dev:amd64=2:1.3.4-1build3`
- `libxext6:amd64=2:1.3.4-1build3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxext=2:1.3.4-1build3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build3.dsc' libxext_1.3.4-1build3.dsc 2221 SHA512:43d31f2d3bf3e9935014f332d801e6940ae1e439a7d7a951112716688cb1a9602e2dab3a818b57ada0bd476ce4d4d00e7384665444799cddd9a41c068b8375ed
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4.orig.tar.gz' libxext_1.3.4.orig.tar.gz 494434 SHA512:4eebd639fd57cb9b84a1e17e368f82fbf3d9f021eef5ad3fe31dd128500db57862a82c1e0d214d447cb7641b2be3fd7e949ee1196f2a482793c6628fb1e5cd70
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxext/libxext_1.3.4-1build3.diff.gz' libxext_1.3.4-1build3.diff.gz 12746 SHA512:4919396ef6da409a3941abd772f3bb6839897c96cde3c55b488d09332a2f08a9044d9fcaa1b34087f25acb4e4826d0a6b578d6aad67cdeb9f6347927a64c0fc7
```

### `dpkg` source package: `libxml2=2.15.1+dfsg-2ubuntu1`

Binary Packages:

- `libxml2-16:amd64=2.15.1+dfsg-2ubuntu1`
- `libxml2-dev:amd64=2.15.1+dfsg-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libxml2-16/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.15.1+dfsg-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.15.1%2bdfsg-2ubuntu1.dsc' libxml2_2.15.1+dfsg-2ubuntu1.dsc 3190 SHA512:13d2c4ce5a307a630f0f5bd237dca110a6397f2b5e5f66efd3dec9d11ee12294255479150a4cc87a90f8404c1966193493b004bfdb6dd2ec71e1d1797d498b9a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.15.1%2bdfsg.orig.tar.xz' libxml2_2.15.1+dfsg.orig.tar.xz 1185240 SHA512:206308977f923d6a6d17a8ea843cfca5b1d6e00a9c2a3efe7d96551bcdf89a943bf53671404de619974edba0556816dc707ac44b8b9eb147445d697bec46d96e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.15.1%2bdfsg-2ubuntu1.debian.tar.xz' libxml2_2.15.1+dfsg-2ubuntu1.debian.tar.xz 39376 SHA512:6b52395cd36b57949bfa61818f01aa2e73408f5295cab74b7b02340e9026a74d76aa926a77255638f0ba6966d8dc4eb7fc4e7cbcbb6b12ee075e1ac08b080b97
```

### `dpkg` source package: `libxrender=1:0.9.12-1build1`

Binary Packages:

- `libxrender1:amd64=1:0.9.12-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxrender=1:0.9.12-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12-1build1.dsc' libxrender_0.9.12-1build1.dsc 2282 SHA512:57c55abb028d6903795e7b6b5cdd3f4b00e104d658fd9837bf64f365b37568cb90672d90713fc7bf51fa5008c46426985ed154143e329f08248c9449619b0c0d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz' libxrender_0.9.12.orig.tar.gz 450034 SHA512:b7cbe8ead3a4eeb7c42acede8569361cf11818d98d05ede75a5f0c48c3fb6b1c0b3b62bb2ba6aea19b4804938512e63ebed127928b1a553b518e3ab974bd089d
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12.orig.tar.gz.asc' libxrender_0.9.12.orig.tar.gz.asc 833 SHA512:299b2654f2bd2b51033072a225a42f75b5e16aff65f6ff171defe9f692f95f69fbcda0b121caf7f4706ee0dd5f9ecef9b2d2ff50a729d40b280fbdeb80ff17cf
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxrender/libxrender_0.9.12-1build1.diff.gz' libxrender_0.9.12-1build1.diff.gz 21468 SHA512:ede29895285be98ca7841741d375fe32d170cac2464b2f6909e09c7cfc04c04a870f1ca8024956dc918052b2751bdaba4145ee4f0dda9c7e21f4feea6a9610a3
```

### `dpkg` source package: `libxslt=1.1.43-0.3`

Binary Packages:

- `libxslt1-dev:amd64=1.1.43-0.3`
- `libxslt1.1:amd64=1.1.43-0.3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.43-0.3
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.43-0.3.dsc' libxslt_1.1.43-0.3.dsc 2183 SHA512:988e63062b3b0ccfa76e5c54b87256da9a5cf5fcec2d024dd4765d429600e7b198045e5c2804c4c2128d60de4f2e72a4ad59b1d89888efe50eef190753546609
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.43.orig.tar.xz' libxslt_1.1.43.orig.tar.xz 1518364 SHA512:96110b0397a8f5791f489127574e2143845feb61bea0581d7b7e3c1101fd0718483bae81a7ce417b971bd678293bfd95daddad0dadd3e256c87d41a69faed85a
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.43-0.3.debian.tar.xz' libxslt_1.1.43-0.3.debian.tar.xz 27452 SHA512:644ae78884010fd2cf29505c9a3f5c45bc0b6800b2ab04be3e60ef9862e150c6dfa8af5955abaedfc3b6078d306a1773514c38c6afe206ccf0ddbbe3d00295b1
```

### `dpkg` source package: `libxt=1:1.2.1-1.3build1`

Binary Packages:

- `libxt-dev:amd64=1:1.2.1-1.3build1`
- `libxt6t64:amd64=1:1.2.1-1.3build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxt=1:1.2.1-1.3build1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.3build1.dsc' libxt_1.2.1-1.3build1.dsc 2383 SHA512:2622d3f65cce40bbd92c31ffdf36961be4a36c66428e35a6a4c66bdaa0713c1cbd210ed8fce5ba60fc4fb3cbe1d66f3e24379f749db75b591c30b080db4c1e56
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz' libxt_1.2.1.orig.tar.gz 1024473 SHA512:73c2fd8a6590ab5ee93cf646e4f41fb71d424961ecbf9bc13c68abdf539c63ab0c59a4d3b22195ba21859523f4cf0e937648424532794a1350a5891061096503
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1.orig.tar.gz.asc' libxt_1.2.1.orig.tar.gz.asc 358 SHA512:135e01b8a79beac9530087dee1a5458c359b4f1ae8346e2502f72f4fc24be400477fda90944315c585e3416e80cb74d1a140d5dfec81e854a4996199a8b221dc
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxt/libxt_1.2.1-1.3build1.diff.gz' libxt_1.2.1-1.3build1.diff.gz 46528 SHA512:655250528961eed8992a9da2bc1e1f1476e876a68859680df1418bb9b758e5c7959b7be7b955aa3ee940a413ac723f2cd7cfaa5d633392e917e7931bf9b36eee
```

### `dpkg` source package: `libyaml=0.2.5-2build3`

Binary Packages:

- `libyaml-0-2:amd64=0.2.5-2build3`
- `libyaml-dev:amd64=0.2.5-2build3`

Licenses: (parsed from: `/usr/share/doc/libyaml-0-2/copyright`, `/usr/share/doc/libyaml-dev/copyright`)

- `Expat`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris libyaml=0.2.5-2build3
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-2build3.dsc' libyaml_0.2.5-2build3.dsc 2064 SHA512:0b5b3bbb06f6c0ea26229a7d42da83f9ad36975829b2fa19ab563534ffc7af1439fb31b61517768cb49bdd007029874ae705fb4a38af7afcf158d0a2c1bd713d
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5.orig.tar.gz' libyaml_0.2.5.orig.tar.gz 85055 SHA512:a0f01e3fc616b65b18a4aa17692ee8ea1a84dc6387d1cf02ac7ef7ab7f46b9744c2aac0a047ff69d6c2da1d2a2d7b355c877da0db57e34d95cd4f37213ab6e7e
'http://archive.ubuntu.com/ubuntu/pool/main/liby/libyaml/libyaml_0.2.5-2build3.debian.tar.xz' libyaml_0.2.5-2build3.debian.tar.xz 5860 SHA512:d771e1430913635319897c47ecce02202f97d0882ffbb73f2908660b4ce7f358fbb09fae5f0a092d77bacb2da5fa3aa259f2e2fa656bdafd347e5e651c873c83
```

### `dpkg` source package: `libzstd=1.5.7+dfsg-3`

Binary Packages:

- `libzstd-dev:amd64=1.5.7+dfsg-3`
- `libzstd1:amd64=1.5.7+dfsg-3`

Licenses: (parsed from: `/usr/share/doc/libzstd-dev/copyright`, `/usr/share/doc/libzstd1/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `zlib`

Source:

```console
$ apt-get source -qq --print-uris libzstd=1.5.7+dfsg-3
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-3.dsc' libzstd_1.5.7+dfsg-3.dsc 2490 SHA512:cb5c666134428bf00d66dbf888863fffc2b0e480d30de5da0e3525cf5869a16ab69c8a3032e4d90072a3a3d6a3b901ed7c1c75a26a106d3c1e83fe49345a3176
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg.orig.tar.xz' libzstd_1.5.7+dfsg.orig.tar.xz 1834780 SHA512:74604a877f899df6a47e88b895334c0fe35af9d096d472f535e772b156bf61e5529833173ea766dbf5e58fc20ce40a2e47ff1cbed8ff7f2bbd506c6634ae5145
'http://archive.ubuntu.com/ubuntu/pool/main/libz/libzstd/libzstd_1.5.7%2bdfsg-3.debian.tar.xz' libzstd_1.5.7+dfsg-3.debian.tar.xz 23164 SHA512:c96d7ca533284c04a1c74362b206eface7460f24ce8cea18c6ebe6109d0d264ccd57ad23a3d11684a0810c5f879de455f197f3f8d88941ac420d0b6e25dfe388
```

### `dpkg` source package: `linux=6.19.0-5.5`

Binary Packages:

- `linux-libc-dev:amd64=6.19.0-5.5`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lto-disabled-list=77`

Binary Packages:

- `lto-disabled-list=77`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lto-disabled-list=77
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_77.dsc' lto-disabled-list_77.dsc 1441 SHA512:dcf480fffebc2123b107038c31434ce5c2c95c14f16a685f1f9e3ae6ab4d979f2636118e580b2591b65a545659f37a7245e7ffdfb27bcda2703020b7d6e2a5cf
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_77.tar.xz' lto-disabled-list_77.tar.xz 14512 SHA512:03c5a47b31fe3e2af140b73b9800120f49f625fd5cc59ed25078e4703ca411df76b44bbf6ebee5862fc010e6d5edaee714af6d995d76e185520eecb162a31d1f
```

### `dpkg` source package: `lz4=1.10.0-6`

Binary Packages:

- `liblz4-1:amd64=1.10.0-6`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.10.0-6
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-6.dsc' lz4_1.10.0-6.dsc 1941 SHA512:39bbc7ecc070543781a46a8a1dd8fce7d2f1458aad8b01d391dff05f1047686053196a4079427b5d647f18a436032900fcdf4f981b32aa1793c8f23f2e8303d8
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA512:8c4ceb217e6dc8e7e0beba99adc736aca8963867bcf9f970d621978ba11ce92855912f8b66138037a1d2ae171e8e17beb7be99281fea840106aa60373c455b28
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-6.debian.tar.xz' lz4_1.10.0-6.debian.tar.xz 9236 SHA512:ba2bac25a9bdb688132e28eed6712de0c087f2f031c6a8b72fb3a6d0b1e8a7e0052e861d5fe4506109ab5ff536c9a3d3f7d00a152253e81c937d433cfe2ad11d
```

### `dpkg` source package: `m4=1.4.21-1`

Binary Packages:

- `m4=1.4.21-1`

Licenses: (parsed from: `/usr/share/doc/m4/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris m4=1.4.21-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.21-1.dsc' m4_1.4.21-1.dsc 1783 SHA512:100cd6a459d97844e59b35ddc216fc320374bd838984e5e7e98783570953984186ceeb5a545534be76f5c515d8edc848a13b57cc68aa89552bf76819d2e178bf
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.21.orig.tar.xz' m4_1.4.21.orig.tar.xz 2080016 SHA512:efe5ec212f6431129a79667f098b2efe2e824122112f73a675deccb9c0d8c9b0bc9e3bf50c9cd5c0b894dc0af1b3f02253e5e67893fb9548a6a9d3bed7c829f7
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.21.orig.tar.xz.asc' m4_1.4.21.orig.tar.xz.asc 488 SHA512:033c1481a1629bcc6ae1cb3437630b00a6b04a4f1aecc26db33b475aff088d50aa7dd15f053cad5a7014ce1b197e8533b8fc5f8f555a952ddb334a9d6e1af059
'http://archive.ubuntu.com/ubuntu/pool/main/m/m4/m4_1.4.21-1.debian.tar.xz' m4_1.4.21-1.debian.tar.xz 17296 SHA512:c8bc8ad5377917aa65f8d5c6debd33a505612d9cef9199302d8b1c65b6b45e6952ff284dcc0122ca84437ea731be744c13fe5dc06950dacba1e3ad5a78ac01c7
```

### `dpkg` source package: `make-dfsg=4.4.1-2`

Binary Packages:

- `make=4.4.1-2`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.4.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1-2.dsc' make-dfsg_4.4.1-2.dsc 1976 SHA512:7b9ea0aeda776b1724c74b0aa2857d3effda31b029a7b47a9d77a509ef33185d72d61827eb2e2bc81170f2172bd961e60379e30b5d1382859aee8181339f0685
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1.orig.tar.xz' make-dfsg_4.4.1.orig.tar.xz 1125180 SHA512:7efa533e7c85e0f394d2a9c422c1cf854f304871f0c692ff74eac18597fa53d1a79b41ba1c56b88d8c79f2e6dfb8c3c3ba8640af15756f455167d62e7ed7b04c
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1-2.debian.tar.xz' make-dfsg_4.4.1-2.debian.tar.xz 44088 SHA512:dd9442a94e3cd75ec0f2cc3f2f349fd34c25a0ba1dd5e24a62f5778b5002d9b7a4768578b9f814266fceb51b69726c9d37d33f66f3d7f3effca9d1ec786e187f
```

### `dpkg` source package: `mawk=1.3.4.20250131-2`

Binary Packages:

- `mawk=1.3.4.20250131-2`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mawk/1.3.4.20250131-2/


### `dpkg` source package: `media-types=14.0.0build1`

Binary Packages:

- `media-types=14.0.0build1`

Licenses: (parsed from: `/usr/share/doc/media-types/copyright`)

- `ad-hoc`

Source:

```console
$ apt-get source -qq --print-uris media-types=14.0.0build1
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_14.0.0build1.dsc' media-types_14.0.0build1.dsc 1671 SHA512:fda7b5f6767b4628e94319e891b6e8110572ac12b8d10f30a7aabaad1abddba4e468dc8830365b0058c9a44fb5917f5c8fc80eca4df9c13f445ec5ffbb999e29
'http://archive.ubuntu.com/ubuntu/pool/main/m/media-types/media-types_14.0.0build1.tar.xz' media-types_14.0.0build1.tar.xz 65280 SHA512:a4362a1aa1c07f9d3f514a8d5138de4d82cc4172fcad13ecb691a1ba38dbeaec9389838207f3ef80ded8346e4fccae31e0034e0613e6f81e9bbe1a5ae7faee04
```

### `dpkg` source package: `mercurial=7.1.1-1ubuntu1`

Binary Packages:

- `mercurial=7.1.1-1ubuntu1`
- `mercurial-common=7.1.1-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `mpclib3=1.3.1-2`

Binary Packages:

- `libmpc3:amd64=1.3.1-2`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpclib3=1.3.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-2.dsc' mpclib3_1.3.1-2.dsc 1919 SHA512:72c0899f4380c63f7e00a94d7a3a018bd865775de903c9f7fc604d468563950338babba7675bb83a6b29bb02344616c83907b110985b3b68c299c4e912195b5f
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1.orig.tar.gz' mpclib3_1.3.1.orig.tar.gz 773573 SHA512:4bab4ef6076f8c5dfdc99d810b51108ced61ea2942ba0c1c932d624360a5473df20d32b300fc76f2ba4aa2a97e1f275c9fd494a1ba9f07c4cb2ad7ceaeb1ae97
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpclib3/mpclib3_1.3.1-2.debian.tar.xz' mpclib3_1.3.1-2.debian.tar.xz 4628 SHA512:4cdefaa458efdbde8b48d42754446e348600f8320b2c0ade917441fabd46b01ac0872be18b7823e1326c4d9e2eee6a94a5338b14dee91862ec93076335bda42c
```

### `dpkg` source package: `mpfr4=4.2.2-2`

Binary Packages:

- `libmpfr6:amd64=4.2.2-2`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris mpfr4=4.2.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.2-2.dsc' mpfr4_4.2.2-2.dsc 2007 SHA512:8c723709afc9dc8c5f6f15c390c2e2abf9c76a269425b78360c2821db8719f5cfb7b768f1e51be7e6e6919e8f8531caeea3deb53ceb4f0c3383860b8b8fc7b32
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.2.orig.tar.xz' mpfr4_4.2.2.orig.tar.xz 1505596 SHA512:eb9e7f51b5385fb349cc4fba3a45ffdf0dd53be6dfc74932dc01258158a10514667960c530c47dd9dfc5aa18be2bd94859d80499844c5713710581e6ac6259a9
'http://archive.ubuntu.com/ubuntu/pool/main/m/mpfr4/mpfr4_4.2.2-2.debian.tar.xz' mpfr4_4.2.2-2.debian.tar.xz 12616 SHA512:753266814daf020c393b4a40e2225c482855e21a49427622c9b785a8bbc0cb4e6408ab8d66c78427fa5c1ff953f7883a7aee8e156cd1fae6f69ae6fcf15c36f3
```

### `dpkg` source package: `mysql-8.4=8.4.8-0ubuntu1`

Binary Packages:

- `libmysqlclient-dev=8.4.8-0ubuntu1`
- `libmysqlclient24:amd64=8.4.8-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libmysqlclient-dev/copyright`, `/usr/share/doc/libmysqlclient24/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Boost-1.0`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `public-domain`
- `zlib/libpng`

Source:

```console
$ apt-get source -qq --print-uris mysql-8.4=8.4.8-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.8-0ubuntu1.dsc' mysql-8.4_8.4.8-0ubuntu1.dsc 3801 SHA512:2ed154f71c914fe62768d1327a7deba85e11da1499f01a2dc871d6004e750b6fadd1897bebdc98a9f8fd99f3f50e86d3c69804aae038dc5b9aa79f7ccd99d2d4
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.8.orig.tar.gz' mysql-8.4_8.4.8.orig.tar.gz 479002191 SHA512:4e95db1a1c2bf99240d846e690784616b15fb3137b4512072ad71a40911c5bb72c0b0354cc588aab7cd5d396e1d1c709a63d9cd09ae664d8fe6ed0f7683e4cf6
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.8.orig.tar.gz.asc' mysql-8.4_8.4.8.orig.tar.gz.asc 833 SHA512:62fcf0be950f5f9bcec0670bba921d556218a33776f524395ab0d0710c54060192e40e52e1307ed10516cb0553f994ba00dc10342cc9620f5ff20e5705eaf28b
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-8.4/mysql-8.4_8.4.8-0ubuntu1.debian.tar.xz' mysql-8.4_8.4.8-0ubuntu1.debian.tar.xz 135760 SHA512:60b0bd9e793611fb1b0bf085586693c47b950aabb2bd2575f180b3114a3c37648eb6634c23cd7db6535ada227ca5b4aeeda367622cddd837c73af985dcccaac6
```

### `dpkg` source package: `mysql-defaults=1.1.1ubuntu2`

Binary Packages:

- `default-libmysqlclient-dev:amd64=1.1.1ubuntu2`
- `mysql-common=5.8+1.1.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/default-libmysqlclient-dev/copyright`, `/usr/share/doc/mysql-common/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris mysql-defaults=1.1.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.1ubuntu2.dsc' mysql-defaults_1.1.1ubuntu2.dsc 2309 SHA512:527d0eacb21cc020ba22d589cb98c0599de44fe9db40ebbda73e02a081f0ff29dce6b07ca9524467469edad15f45923a4b78b6657f2aeb2975f650ca203e1a00
'http://archive.ubuntu.com/ubuntu/pool/main/m/mysql-defaults/mysql-defaults_1.1.1ubuntu2.tar.xz' mysql-defaults_1.1.1ubuntu2.tar.xz 7628 SHA512:288f877f8e15fb60be9d2748cfadb5153ef65b42072ea5a61456649e626f57da97f93e4d789003fabb27866af0a8559a99732fb9b48aee85a8b6a621b4373d4a
```

### `dpkg` source package: `ncurses=6.6+20251231-1`

Binary Packages:

- `libncurses-dev:amd64=6.6+20251231-1`
- `libncurses6:amd64=6.6+20251231-1`
- `libncursesw6:amd64=6.6+20251231-1`
- `libtinfo6:amd64=6.6+20251231-1`
- `ncurses-base=6.6+20251231-1`
- `ncurses-bin=6.6+20251231-1`

Licenses: (parsed from: `/usr/share/doc/libncurses-dev/copyright`, `/usr/share/doc/libncurses6/copyright`, `/usr/share/doc/libncursesw6/copyright`, `/usr/share/doc/libtinfo6/copyright`, `/usr/share/doc/ncurses-base/copyright`, `/usr/share/doc/ncurses-bin/copyright`)

- `BSD-3-clause`
- `MIT/X11`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris ncurses=6.6+20251231-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.6%2b20251231-1.dsc' ncurses_6.6+20251231-1.dsc 4163 SHA512:2dbb2716c022c91ae15c1de5aa31844ee39d34c9e0e61f54365adb53c818d217eb8425e485b45c6b0de3541f8090974f77bc6bd41fd129ae9def1e8906154499
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.6%2b20251231.orig.tar.gz' ncurses_6.6+20251231.orig.tar.gz 3789898 SHA512:bb95db59e1a4ea5371efe77806af601460a9a4447fb5c98931d2e911aa5b1b760f1627c2ff8377d13128db5f11b1c20db89c52c5c4584adeed5622e909eef16f
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.6%2b20251231.orig.tar.gz.asc' ncurses_6.6+20251231.orig.tar.gz.asc 729 SHA512:3228642bd563bad6b920e883921e61dab4e42b3a53c8dc02112726fd63964484aff3b13ec666b4f253bc58edb666a8aa4fca8bafc23db0e6405c8f6a07a662fd
'http://archive.ubuntu.com/ubuntu/pool/main/n/ncurses/ncurses_6.6%2b20251231-1.debian.tar.xz' ncurses_6.6+20251231-1.debian.tar.xz 50852 SHA512:fd0acff5a48336ba877a3bf2122eb889461fca98e2eae0ead561c027f442e6984852a1c3414f8439fbcb414f75f83ae20468f5196eeaa51d335065173c2bbbf8
```

### `dpkg` source package: `netbase=6.5`

Binary Packages:

- `netbase=6.5`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.5
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.5.dsc' netbase_6.5.dsc 899 SHA512:1092aa10f8b59cbd88bd382fcd3042fdc1b1344af98de75b7cf2cfdaa005e164fcea2ea604652936dfdaeb0d79430b083782794a0f79d1cab5dec615e7acda26
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.5.tar.xz' netbase_6.5.tar.xz 32544 SHA512:d64a5dc98bfa3ecef65cb061888fb8a948e853692fd56b523409304df9b5426369ec3c9b61731cacaadab5876ec24bb63631fece935641b533a8763792311fb3
```

### `dpkg` source package: `nettle=3.10.2-1`

Binary Packages:

- `libhogweed6t64:amd64=3.10.2-1`
- `libnettle8t64:amd64=3.10.2-1`
- `nettle-dev:amd64=3.10.2-1`

Licenses: (parsed from: `/usr/share/doc/libhogweed6t64/copyright`, `/usr/share/doc/libnettle8t64/copyright`, `/usr/share/doc/nettle-dev/copyright`)

- `Expat`
- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-3+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-3+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nettle=3.10.2-1
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.2-1.dsc' nettle_3.10.2-1.dsc 2297 SHA512:2429234b8b6d02c98245acb4ff246213e77682d2618c45436fd44ffd2e7dd1052e07a0d92bf3143c2cd36bf8f846d3ef65c10f834f1914f93da66149d5c6ce4b
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.2.orig.tar.gz' nettle_3.10.2.orig.tar.gz 2644644 SHA512:bf37ddd7dca8e78488da2a5286dcf16761d527d620572b42f2ad27bb8ee8c12999d92b0272e06f53766e7155a3f4a1ab7ad9c4b1c3caec47c031878b6b1772fb
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.2.orig.tar.gz.asc' nettle_3.10.2.orig.tar.gz.asc 573 SHA512:a998bb2e565ef4e36d8783cb78d5cb74dc3cd499d7706f381a75210194bff93e9ccd9102f6f6eca5a061e1172aaf9970c9ea109670027fbda23f299e78ba6c55
'http://archive.ubuntu.com/ubuntu/pool/main/n/nettle/nettle_3.10.2-1.debian.tar.xz' nettle_3.10.2-1.debian.tar.xz 25052 SHA512:45739e3af9c2ec00a1f7b9c0998e87bcf0a0803dd1aa52c6eae1a536e637435800aafee5aed570c7b8e9515d2838a445f74c0e648a944417de9298561c90bdd6
```

### `dpkg` source package: `nghttp2=1.64.0-1.1ubuntu2`

Binary Packages:

- `libnghttp2-14:amd64=1.64.0-1.1ubuntu2`
- `libnghttp2-dev:amd64=1.64.0-1.1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`, `/usr/share/doc/libnghttp2-dev/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.64.0-1.1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0-1.1ubuntu2.dsc' nghttp2_1.64.0-1.1ubuntu2.dsc 2621 SHA512:b9b4dcdc9387b85020d46d939f27a907a0c143b3e09318332a71acce536c9268a248147c3e40d2e5a9e54a66b20272e0f4316dac89ae2fdd08457d002bde369e
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0.orig.tar.gz' nghttp2_1.64.0.orig.tar.gz 1069782 SHA512:35f8230a0fa2825f0bc400d4852d8e8b484f659c67b00639ccd074a0029088f016e967db2f62b6b64af1f8ef684f5809a833e7f922e38b9405f7cc7756bcfb75
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.64.0-1.1ubuntu2.debian.tar.xz' nghttp2_1.64.0-1.1ubuntu2.debian.tar.xz 39976 SHA512:fe37794628ba6cec920fbdfd2f00979c4bd2ed0cda096e0ebccf5f9b7648f68cc4da5028d1d9726e7ee0ed044f2099ec2e9ba6f96ef4bb1b5b62e3ae62835e32
```

### `dpkg` source package: `npth=1.8-3build1`

Binary Packages:

- `libnpth0t64:amd64=1.8-3build1`

Licenses: (parsed from: `/usr/share/doc/libnpth0t64/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.8-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8-3build1.dsc' npth_1.8-3build1.dsc 2212 SHA512:3f8e58740736464a74a97012dee0f7141ae9ffbcf315d3f388aa5fc52031ef4c0e3abad39fad258b6732e21df31878b6d20598ea88e7e719d9a001a99d86e845
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8.orig.tar.bz2' npth_1.8.orig.tar.bz2 317739 SHA512:34fdeea3d8a7a594d8fdbcc6d5d389b5c8e282e8e84c1491b1e51960c0fa007df6a1d62543f0107f0772f3215557d4b25c2a9c7067cb0ae2f8de7b4d63d09fb4
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8.orig.tar.bz2.asc' npth_1.8.orig.tar.bz2.asc 390 SHA512:2d2d26d2bde77997187792f724b89b6c1ba7ad845c0087d78d7bd2eef688136df8fa8ea02c5199c0a3ad602bf228af0fadf82ecd3ff4b9ed35c71d009bb2e1a5
'http://archive.ubuntu.com/ubuntu/pool/main/n/npth/npth_1.8-3build1.debian.tar.xz' npth_1.8-3build1.debian.tar.xz 8752 SHA512:b834fb1ce6f2d4d267fd2263a66e210ac07fb66be29a7fd396997437e33f0e3b1f89b9a093cf400a112a40ae7e62b4ec5ea3dda63861e52a4832d63bbda812cd
```

### `dpkg` source package: `openexr=3.1.13-2build1`

Binary Packages:

- `libopenexr-3-1-30:amd64=3.1.13-2build1`
- `libopenexr-dev=3.1.13-2build1`

Licenses: (parsed from: `/usr/share/doc/libopenexr-3-1-30/copyright`, `/usr/share/doc/libopenexr-dev/copyright`)

- `BSD-3-clause`
- `openexr`

Source:

```console
$ apt-get source -qq --print-uris openexr=3.1.13-2build1
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.13-2build1.dsc' openexr_3.1.13-2build1.dsc 2317 SHA512:6f1501224ed06553624b09f7b382b7ab4f7fc6aecd27edd0b5c60e1df2aa45e00ce25041d45ec350b87900a9604c0245273fe877958b3c5f7e2649942cb68505
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.13.orig.tar.gz' openexr_3.1.13.orig.tar.gz 20542408 SHA512:662ebfce32bc56e3b5140e7d1813b8c117ac6e806fe30c996b956465ce20ee43f1f535b97868a87a26d1d7909d7f59acbe383f335ab8d72ad1484408cbabf77b
'http://archive.ubuntu.com/ubuntu/pool/universe/o/openexr/openexr_3.1.13-2build1.debian.tar.xz' openexr_3.1.13-2build1.debian.tar.xz 19348 SHA512:e1ff157b6c89174396287e4cb3814925712efed4460b2e24defe0e004a86db108f27ace4e0eb511943582f9bc04ec9b2bb71e6b18412021e473d320d19994959
```

### `dpkg` source package: `openjpeg2=2.5.4-1`

Binary Packages:

- `libopenjp2-7:amd64=2.5.4-1`
- `libopenjp2-7-dev:amd64=2.5.4-1`

Licenses: (parsed from: `/usr/share/doc/libopenjp2-7/copyright`, `/usr/share/doc/libopenjp2-7-dev/copyright`)

- `BSD-2`
- `BSD-3`
- `LIBPNG`
- `LIBTIFF`
- `LIBTIFF-GLARSON`
- `LIBTIFF-PIXAR`
- `MIT`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris openjpeg2=2.5.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.4-1.dsc' openjpeg2_2.5.4-1.dsc 2563 SHA512:d00d1ac0db1b81a0f5b7b02091ed9a0c0bfe9adc041cfb358cdf7bae97770ad04ccf8b206010309f83685620922534cc7830d1364ebc08a7f1f3b3349ad245d2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.4.orig.tar.xz' openjpeg2_2.5.4.orig.tar.xz 1395184 SHA512:343594a672429833389e2826456dd9800bb0118618ec9e84ea10f3846736bb32b46baa95a702e69b84c93cff70ddc7fa1baec78ae6a801c01b9cc723f072233b
'http://archive.ubuntu.com/ubuntu/pool/main/o/openjpeg2/openjpeg2_2.5.4-1.debian.tar.xz' openjpeg2_2.5.4-1.debian.tar.xz 15588 SHA512:9985e4806dfa36508b45aa6a5ef72dbf238a16918246f01ac63535d3bf8a745a5d463f99571829dc8c5fd16cbe749e6e5a016f326cd550c7e2fc9f41feb94fe5
```

### `dpkg` source package: `openldap=2.6.10+dfsg-1ubuntu5`

Binary Packages:

- `libldap-common=2.6.10+dfsg-1ubuntu5`
- `libldap-dev:amd64=2.6.10+dfsg-1ubuntu5`
- `libldap2:amd64=2.6.10+dfsg-1ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libldap-common/copyright`, `/usr/share/doc/libldap-dev/copyright`, `/usr/share/doc/libldap2/copyright`)

- `BSD-3-clause`
- `BSD-3-clause-California`
- `BSD-3-clause-variant`
- `BSD-4-clause-California`
- `Beerware`
- `Expat`
- `Expat-ISC`
- `Expat-UNM`
- `F5`
- `FSF-unlimited`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `GPL-2+ with Libtool exception`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Autoconf exception`
- `GPL-3+ with Libtool exception`
- `JCG`
- `MIT-XC`
- `NeoSoft-permissive`
- `OpenLDAP-2.8`
- `UMich`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openldap=2.6.10+dfsg-1ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1ubuntu5.dsc' openldap_2.6.10+dfsg-1ubuntu5.dsc 3426 SHA512:addfc27c84e83b2cce4c2efe398641eb87192f42d35ab6e25eaca4021b347f8070fef08d3f4a95e3d1e1999b7d9f1d666f535c6f54eb8c071808f4199b21d185
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg.orig.tar.xz' openldap_2.6.10+dfsg.orig.tar.xz 3754560 SHA512:9c24cab12ea4002560670d1a6053c00582aea1713e3db262bbf5aae7666c6d50ef28e7b59ca4dbe5c5b5903e56268911a935a58ef852239c259830458e804f62
'http://archive.ubuntu.com/ubuntu/pool/main/o/openldap/openldap_2.6.10%2bdfsg-1ubuntu5.debian.tar.xz' openldap_2.6.10+dfsg-1ubuntu5.debian.tar.xz 189056 SHA512:6955829975b20a8c45b6f958fcb7c0f88408df8c4befe6d407ef2020c0dbcfb8f5e147cc405db676922ffa2061d4cc700d12ce15bd3b7f79c40822be0bf091b4
```

### `dpkg` source package: `openssh=1:10.2p1-2ubuntu1`

Binary Packages:

- `openssh-client=1:10.2p1-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/openssh-client/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `Expat-with-advertising-restriction`
- `Mazieres-BSD-style`
- `OpenSSH`
- `Powell-BSD-style`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris openssh=1:10.2p1-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1-2ubuntu1.dsc' openssh_10.2p1-2ubuntu1.dsc 3499 SHA512:08eb87a6f300981e2ee35541582747b093d9d7bb9f9f45ae1c1b250df8c92e67972fd84b7267c1fd25bc6bcf2f32eec243e9da0735c6cfebea5a1686b03cbac2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1.orig.tar.gz' openssh_10.2p1.orig.tar.gz 1974519 SHA512:66f3dd646179e71aaf41c33b6f14a207dc873d71d24f11c130a89dee317ee45398b818e5b94887b5913240964a38630d7bca3e481e0f1eff2e41d9e1cfdbdfc5
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1.orig.tar.gz.asc' openssh_10.2p1.orig.tar.gz.asc 833 SHA512:f1f71700b1b0b2117aed505488b98b7ebb51ce26e53184b08df0b07aa2c5a1e54dc4d3cbcbe871b5ad849a2a0e22b02af318ff22a68c980ab53b04be03c9bf3c
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1-2ubuntu1.debian.tar.xz' openssh_10.2p1-2ubuntu1.debian.tar.xz 214552 SHA512:337a353a47f03a0acd9e4c3391cdd1d3a3e84b729620c5f30713623340a955403e1efbda18edf79ae782a15dfce7e3af1628181e73eec674366462cbd633f400
```

### `dpkg` source package: `openssl=3.5.3-1ubuntu2`

Binary Packages:

- `libssl-dev:amd64=3.5.3-1ubuntu2`
- `libssl3t64:amd64=3.5.3-1ubuntu2`
- `openssl=3.5.3-1ubuntu2`
- `openssl-provider-legacy=3.5.3-1ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libssl-dev/copyright`, `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

Source:

```console
$ apt-get source -qq --print-uris openssl=3.5.3-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.5.3-1ubuntu2.dsc' openssl_3.5.3-1ubuntu2.dsc 2600 SHA512:3ab238c4502490f90ea7d5227302d43baa1a8ae5b0b8536eaac6d387bdf11a75914d40c4ba0e0452113f50cac310788462c9ed34aa0fb280faa368d9dfa321c7
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.5.3.orig.tar.gz' openssl_3.5.3.orig.tar.gz 53183370 SHA512:58265c05d208a269418d4928d3127d22738e696d5d080ab8f1c0cbd2cd30e4e1e07e244a1d81c9b40f1a7f972fe835f4f122c098a7b2177ac48492881416aa78
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/openssl_3.5.3-1ubuntu2.debian.tar.xz' openssl_3.5.3-1ubuntu2.debian.tar.xz 67424 SHA512:8288788e75092aacd0789284f95a08707b131a37b5f1b31cec134f82debac4a6af63ed6a65dc6025e45bfe584e8ec63ed99037ef95ae02739479014c65a5f189
```

### `dpkg` source package: `p11-kit=0.25.10-1`

Binary Packages:

- `libp11-kit-dev:amd64=0.25.10-1`
- `libp11-kit0:amd64=0.25.10-1`

Licenses: (parsed from: `/usr/share/doc/libp11-kit-dev/copyright`, `/usr/share/doc/libp11-kit0/copyright`)

- `Apache-2.0`
- `BSD-3-clause`
- `FSFAP`
- `FSFULLR`
- `GPL-2+ with Autoconf-data exception`
- `GPL-3+ with Autoconf-data exception`
- `ISC`
- `LGPL-2.1`
- `LGPL-2.1+`
- `X11`
- `customFSFULLRWD`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.25.10-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.10-1.dsc' p11-kit_0.25.10-1.dsc 2548 SHA512:31ae5779fcac1bae34128de7618597d2b2281ce48dd23cb9e3c96c7b77b103945f563249707735856f3e370ba14695664a7b00abbcb4b494bb8f973420618d38
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.10.orig.tar.xz' p11-kit_0.25.10.orig.tar.xz 1053532 SHA512:c5a5dfb6bd46e8964a70f2fc601bd5b61bf88f79d1011c70e6f37a62130c4aad692d8bac83aff2fd2728543274e198d2946ded7a53636835aefb13b9a3155527
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.10.orig.tar.xz.asc' p11-kit_0.25.10.orig.tar.xz.asc 228 SHA512:5c0e711fa1ef619bfd8ea479c45a6c76d22721549eb2a802f18644411fab6983fc09854677fac22b228e323a505e20036a9cfe4007f504567c5dd2bb1a3e6976
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.25.10-1.debian.tar.xz' p11-kit_0.25.10-1.debian.tar.xz 24308 SHA512:e23a1108fb9d994d514b11ee7872a769207d70b9b8a7a9b566215249ce43d404e4ad8930cd34354c2189642e2a05b47497d888357892ff50628e638b0b6e9755
```

### `dpkg` source package: `pam=1.7.0-5ubuntu2`

Binary Packages:

- `libpam-modules:amd64=1.7.0-5ubuntu2`
- `libpam-modules-bin=1.7.0-5ubuntu2`
- `libpam-runtime=1.7.0-5ubuntu2`
- `libpam0g:amd64=1.7.0-5ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `BSD-3-clause`
- `BSD-tcp_wrappers`
- `Beerware`
- `GPL`
- `GPL-1`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `pango1.0=1.57.0-1`

Binary Packages:

- `libpango-1.0-0:amd64=1.57.0-1`
- `libpangocairo-1.0-0:amd64=1.57.0-1`
- `libpangoft2-1.0-0:amd64=1.57.0-1`

Licenses: (parsed from: `/usr/share/doc/libpango-1.0-0/copyright`, `/usr/share/doc/libpangocairo-1.0-0/copyright`, `/usr/share/doc/libpangoft2-1.0-0/copyright`)

- `Apache-2`
- `Apache-2.0`
- `Bitstream-Vera`
- `Chromium-BSD-style`
- `Example`
- `ICU`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `OFL-1.1`
- `TCL`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris pango1.0=1.57.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.57.0-1.dsc' pango1.0_1.57.0-1.dsc 3704 SHA512:d441f21f4bbf6d9cdca2d9c0ba56b7045d20fa29d03989fcc0171675f9577f8d1b9cd5c6201a6c97a8b10bc47442a028ec60116c3a951f91c6fc9d64a0af29f4
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.57.0.orig.tar.xz' pango1.0_1.57.0.orig.tar.xz 2566400 SHA512:e3d251e0c2d5cb7f2e9d26e675aa2fae0c3cedce9e73b77f92a4abbeff55eaa819811e4c064ca036d3964a3ee4592f596ebfa7c0a760189b9d8c38a5f3a4ea3a
'http://archive.ubuntu.com/ubuntu/pool/main/p/pango1.0/pango1.0_1.57.0-1.debian.tar.xz' pango1.0_1.57.0-1.debian.tar.xz 44172 SHA512:a76fd38853d86ce1c9a3061bd7479325f7353bc07951f1bf5bb3a1bdb46d849e447ed39cfbfdf1624238ba25f7fcd6594c787984d7da4433a765b07b9bf300d3
```

### `dpkg` source package: `patch=2.8-2build1`

Binary Packages:

- `patch=2.8-2build1`

Licenses: (parsed from: `/usr/share/doc/patch/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris patch=2.8-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8-2build1.dsc' patch_2.8-2build1.dsc 1713 SHA512:bf3355a5e92a37ee77ead1b6741c6d5dbb9739b201c4a9e3ca3e50ebe79d5272909297a48eda29ed91236ce72528ac37541108269bb2d8591f1ee8be146aa5b8
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8.orig.tar.xz' patch_2.8.orig.tar.xz 907208 SHA512:d689d696660a662753e8660792733c3be0a94c76abfe7a28b0f9f70300c3a42d6437d081553a59bfde6e1b0d5ee13ed89be48d0b00b6da2cadbfc14a15ada603
'http://archive.ubuntu.com/ubuntu/pool/main/p/patch/patch_2.8-2build1.debian.tar.xz' patch_2.8-2build1.debian.tar.xz 9512 SHA512:e19f158ba106992bd9bbf23ceec57f58b85f4817a839d829ef00ddc6752394002f123a1575b2cab94649117eb1b96463fb3dd45c59c731d571621b23fb2fc484
```

### `dpkg` source package: `pcre2=10.46-1build1`

Binary Packages:

- `libpcre2-16-0:amd64=10.46-1build1`
- `libpcre2-32-0:amd64=10.46-1build1`
- `libpcre2-8-0:amd64=10.46-1build1`
- `libpcre2-dev:amd64=10.46-1build1`
- `libpcre2-posix3:amd64=10.46-1build1`

Licenses: (parsed from: `/usr/share/doc/libpcre2-16-0/copyright`, `/usr/share/doc/libpcre2-32-0/copyright`, `/usr/share/doc/libpcre2-8-0/copyright`, `/usr/share/doc/libpcre2-dev/copyright`, `/usr/share/doc/libpcre2-posix3/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-3-clause-Cambridge with BINARY LIBRARY-LIKE PACKAGES exception`
- `X11`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris pcre2=10.46-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.46-1build1.dsc' pcre2_10.46-1build1.dsc 2221 SHA512:5454744ec42c17a8153fc479577f6cfb2be961e5588e02828908b4f1d618878d9f5c783f4bdccf6f1f62303b8e4b52a31f62e2dbe37dff1cad08907726a418e1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.46.orig.tar.gz' pcre2_10.46.orig.tar.gz 2718545 SHA512:8bc85f1e47633f4cab07e00b65e9f94a38bb8db56d7ea0a3068774a5ccfe5b777e6645c0a345dd265a06aa6672448ad51c9e56636c48ec87dae9f884a998e00b
'http://archive.ubuntu.com/ubuntu/pool/main/p/pcre2/pcre2_10.46-1build1.diff.gz' pcre2_10.46-1build1.diff.gz 8804 SHA512:b430153c7e3b41f0ddfa526ed816d66111b27415c8d0863d8c516c27f84e0370d517911048db6ec1ad0ce45e08c4c5afec369b7d64b68b200e2cc5c20251049a
```

### `dpkg` source package: `perl=5.40.1-6build1`

Binary Packages:

- `libperl5.40:amd64=5.40.1-6build1`
- `perl=5.40.1-6build1`
- `perl-base=5.40.1-6build1`
- `perl-modules-5.40=5.40.1-6build1`

Licenses: (parsed from: `/usr/share/doc/libperl5.40/copyright`, `/usr/share/doc/perl/copyright`, `/usr/share/doc/perl-base/copyright`, `/usr/share/doc/perl-modules-5.40/copyright`)

- `Artistic`
- `Artistic,`
- `Artistic-2`
- `Artistic-dist`
- `BSD-3-clause`
- `BSD-3-clause-GENERIC`
- `BSD-3-clause-with-weird-numbering`
- `BSD-4-clause-POWERDOG`
- `BZIP`
- `CC0-1.0`
- `DONT-CHANGE-THE-GPL`
- `Expat`
- `FSFAP`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3+-WITH-BISON-EXCEPTION`
- `LGPL-2.1`
- `REGCOMP`
- `REGCOMP,`
- `SDBM-PUBLIC-DOMAIN`
- `TEXT-TABS`
- `Unicode`
- `ZLIB`

Source:

```console
$ apt-get source -qq --print-uris perl=5.40.1-6build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-6build1.dsc' perl_5.40.1-6build1.dsc 2932 SHA512:249bedfe2613348fd33408c66d957102ac235c7d94473e90641bf60bdf7db600ac0300208b843145c5494f82988bfb6284018554bc78a84173e16884bc07a426
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA512:933261779f476b0edda581270949c92e8e7dbe4bcaf1417398e708a321cdb748fe329acb703b2e74446cdfb03c20cefcab1eb972b852418ed3ea9b870db1fa86
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA512:3ff16b3462ce43ff38dab21b3dfc20f81772b8c9eac19ab96ba2d5e6cbb390e2302fa76c4879f915249357cd11c7ec0d548bcbf3ab2c156df1b9fca95da3f545
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-6build1.debian.tar.xz' perl_5.40.1-6build1.debian.tar.xz 172908 SHA512:c8a4135968ee5a462f853a2651b570e9c9bff5305f4f6dc8dd5356904aa97d4f148eca8ce32cb12515e284f4067b8a4408cdb47f2675b43183017721c41b6dd3
```

### `dpkg` source package: `pinentry=1.3.2-3ubuntu1`

Binary Packages:

- `pinentry-curses=1.3.2-3ubuntu1`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.3.2-3ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.2-3ubuntu1.dsc' pinentry_1.3.2-3ubuntu1.dsc 3373 SHA512:684e98947af437d702eae06d2ea2cd99a207a2c5736a3a5cc137ad95463a847f88176a61824829e84ea52ce9fedd5d03a400e2eba86b083be7670e20227304a2
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.2.orig.tar.bz2' pinentry_1.3.2.orig.tar.bz2 612858 SHA512:3b4d50a42d412d649a7830f7378aa966342c2bc0157d03b0ad79cf0aed29d6698d48c734e23b1dccada5f6ef81d0c09d3ead6cd703eadfc8082987e6bea0aafc
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.2.orig.tar.bz2.asc' pinentry_1.3.2.orig.tar.bz2.asc 427 SHA512:645e0bc78001dd1883f03437594588d2be8b0d1a32521c13d4ceea437652ca5675bd15977bdccdcfdabf96bc4edbaa567f547b46d7725d48c28e65be13654098
'http://archive.ubuntu.com/ubuntu/pool/main/p/pinentry/pinentry_1.3.2-3ubuntu1.debian.tar.xz' pinentry_1.3.2-3ubuntu1.debian.tar.xz 20348 SHA512:f8bb460c7411bca6c5fb69653f7ae2386ecbcd4f8fd641508cfaf8053820c2c0dda052c1f2a051bc648094721b2a0f3ca698206a56ba98dc1c8f6cbf75e510d2
```

### `dpkg` source package: `pixman=0.46.4-1`

Binary Packages:

- `libpixman-1-0:amd64=0.46.4-1`

Licenses: (parsed from: `/usr/share/doc/libpixman-1-0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris pixman=0.46.4-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.46.4-1.dsc' pixman_0.46.4-1.dsc 2019 SHA512:9c059227bf84e62d4f6419406f7ea1c6b5e8a0a2dc9ace4c8ecbbc272b568ea9965c402508a7356747645bd98758fbd51488481fbd2151265e46eb20dd621fd7
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.46.4.orig.tar.gz' pixman_0.46.4.orig.tar.gz 827198 SHA512:10ddb88b51f5456c440d77a7b4230600b099e818378a9b55f715bbe5ec3d9f1e9da2124d28a2bd3377f1ab20af87e0ec4fa9dadaa20a2f1f880dd2dc7f27ca6c
'http://archive.ubuntu.com/ubuntu/pool/main/p/pixman/pixman_0.46.4-1.diff.gz' pixman_0.46.4-1.diff.gz 9639 SHA512:df40dca4e3663782f5431f1dfb4087fa659003bdf0ba3daa7fc527acf9bff03dabdb37cc7498e0b920c318714f1c42c2791b6281af8f2b3fac21cfd8602d2eae
```

### `dpkg` source package: `pkgconf=1.8.1-4build1`

Binary Packages:

- `libpkgconf3:amd64=1.8.1-4build1`
- `pkgconf:amd64=1.8.1-4build1`
- `pkgconf-bin=1.8.1-4build1`

Licenses: (parsed from: `/usr/share/doc/libpkgconf3/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=1.8.1-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-4build1.dsc' pkgconf_1.8.1-4build1.dsc 2154 SHA512:9ef1f0bd26e6f3b8d1dc30d8709a96c25edc0c4f38979d33c5dfb769929f923eba53901ab87236510b3b355696c3291ac66e1305b3234f71a5b18d25a9fc4b83
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1.orig.tar.xz' pkgconf_1.8.1.orig.tar.xz 302372 SHA512:7a7d5204c1c9bfb6578bda56f299d1fa0300e69a133a65730b10ad77aefbf26fceb74ae77cecda326b3ed5db5736f27fcce94764b3a56d40f4bb99fecdc80bba
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_1.8.1-4build1.debian.tar.xz' pkgconf_1.8.1-4build1.debian.tar.xz 17804 SHA512:72ed87055ac67f5dc74547cee6a81a3f3f19a498dbe17b0c5b744060723ed5f00963f56e088176449fbca4f003531596edfc8bfd9fadf2bc380c5e9400e84b6c
```

### `dpkg` source package: `postgresql-18=18.1-2`

Binary Packages:

- `libpq-dev=18.1-2`
- `libpq5:amd64=18.1-2`

Licenses: (parsed from: `/usr/share/doc/libpq-dev/copyright`, `/usr/share/doc/libpq5/copyright`)

- `Artistic`
- `BSD-2-clause`
- `BSD-3-Clause`
- `BSD-3-clause`
- `Custom-Unicode`
- `Custom-pg_dump`
- `Custom-regex`
- `GPL-1`
- `PostgreSQL`
- `Tcl`
- `double-metaphone`
- `nagaysau-ishii`

Source:

```console
$ apt-get source -qq --print-uris postgresql-18=18.1-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-18/postgresql-18_18.1-2.dsc' postgresql-18_18.1-2.dsc 4443 SHA512:e3d90f581698ba0e6a97eca5df32bb14d3c5b1c62582fbb4fbb7221c3a62b09a343132cc838ed12b17ea65707ab2a554ff60d82e2d2b15ae01e0106065cc2470
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-18/postgresql-18_18.1.orig.tar.bz2' postgresql-18_18.1.orig.tar.bz2 22423920 SHA512:bac8a9bfb12c0c70b5870d92c6f322edbfd559e9ac939e841f16d8271b5c2bc4fb2628e053b407aed71b4032e9f4cba55f1e0a8dc6a3bd4933c2b701fe69ec08
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-18/postgresql-18_18.1-2.debian.tar.xz' postgresql-18_18.1-2.debian.tar.xz 24444 SHA512:95038efc414e1400cffc26f47ec77725715b3fb6e14daf4b18704be9c4b0813832b39d926ddab1d38136ad995ca7b2b88af8c3d28abd55d2aa0978d353a44fe8
```

### `dpkg` source package: `procps=2:4.0.4-9ubuntu1`

Binary Packages:

- `libproc2-0:amd64=2:4.0.4-9ubuntu1`
- `procps=2:4.0.4-9ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libproc2-0/copyright`, `/usr/share/doc/procps/copyright`)

- `GPL-2`
- `GPL-2.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris procps=2:4.0.4-9ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-9ubuntu1.dsc' procps_4.0.4-9ubuntu1.dsc 2247 SHA512:8b1abfba83a6d8ddbea36ec5bc5629769c73774cd02766dd2fb738c6c9ea7b333b51ce69905aca0d8aeb9cb8fe380bf3d1f28db8d32507efe65c34bf87951d50
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4.orig.tar.xz' procps_4.0.4.orig.tar.xz 1401540 SHA512:94375544e2422fefc23d7634063c49ef1be62394c46039444f85e6d2e87e45cfadc33accba5ca43c96897b4295bfb0f88d55a30204598ddb26ef66f0420cefb4
'http://archive.ubuntu.com/ubuntu/pool/main/p/procps/procps_4.0.4-9ubuntu1.debian.tar.xz' procps_4.0.4-9ubuntu1.debian.tar.xz 62072 SHA512:e7991c0546e67c6fe6db5c81f11dbb402999800b4665709da03eea8283e7b268845e460f78dbb7af4219b1708315c84dd0f080c8e834288ab95a8df4bf1b6976
```

### `dpkg` source package: `python-packaging=25.0-2`

Binary Packages:

- `python3-packaging=25.0-2`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-packaging=25.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_25.0-2.dsc' python-packaging_25.0-2.dsc 2526 SHA512:22457ef62aa9ce166c985cff25365c718c7d819cb7f3ff4407fa9ec456e5e7233f910af613da423538eec451b85f1c05f753580cd05fbbcd56c441c31ca9558f
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_25.0.orig.tar.gz' python-packaging_25.0.orig.tar.gz 165727 SHA512:0672602d2e18c3aee71b3e567b0de572bc8613ee3d24a79a655ded23ac08ec4582193225bc0c0ea390ed81cf5efbb46e8afbe0798d14f2235f811f263c25728c
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_25.0-2.debian.tar.xz' python-packaging_25.0-2.debian.tar.xz 4232 SHA512:d371d29f343af2486a5e66563992566b08048b0e6a3ad8a0afc0d3a8438be0efc4f2ebea7ca9a2bacdf697cbfcf89925472ac3c02de95da92ed1f75ab4193808
```

### `dpkg` source package: `python3-defaults=3.13.9-3`

Binary Packages:

- `libpython3-stdlib:amd64=3.13.9-3`
- `python3=3.13.9-3`
- `python3-minimal=3.13.9-3`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris python3-defaults=3.13.9-3
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.13.9-3.dsc' python3-defaults_3.13.9-3.dsc 2479 SHA512:d6a7959844c4a787e3c6641fdc33fcbf9ab6b63631a8535b008b99ee5aa9914a4c7d366345667372246673010cc6d00091171694ebdb1d7491efa387c3260d92
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3-defaults/python3-defaults_3.13.9-3.tar.gz' python3-defaults_3.13.9-3.tar.gz 146945 SHA512:587863d8775c25a9dab05461517e48ef65e921836fb3429c2c30c8e89de2e98f1770f6a58fc61f37fec69e943033cc1bfc112ce68aa8fc2a4ca7716c93c46242
```

### `dpkg` source package: `python3.13=3.13.12-1`

Binary Packages:

- `libpython3.13-minimal:amd64=3.13.12-1`
- `libpython3.13-stdlib:amd64=3.13.12-1`
- `python3.13=3.13.12-1`
- `python3.13-minimal=3.13.12-1`

Licenses: (parsed from: `/usr/share/doc/libpython3.13-minimal/copyright`, `/usr/share/doc/libpython3.13-stdlib/copyright`, `/usr/share/doc/python3.13/copyright`, `/usr/share/doc/python3.13-minimal/copyright`)

- `* Permission to use this software in any way is granted without`
- `By obtaining, using, and/or copying this software and/or its`
- `GPL-2`
- `Permission  is  hereby granted,  free  of charge,  to  any person`
- `Permission is hereby granted, free of charge, to any person obtaining`
- `Permission to use, copy, modify,`
- `Redistribution`
- `This software is provided 'as-is', without any express`
- `This software is provided as-is, without express`
- `binary forms, with`
- `distribute this software`
- `distribute this software and`
- `distribute this software for any`
- `implied`
- `its`
- `use in source`
- `without`

Source:

```console
$ apt-get source -qq --print-uris python3.13=3.13.12-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.12-1.dsc' python3.13_3.13.12-1.dsc 3699 SHA512:f341ec9abf3729a9ca1b69bc26662f7d9666bb9e15576f6a2598ba0b9a55d3abdfa93af2a56349c8e8912eb8a036e7012582f4e77a5577e9c7f74650fc0b8a57
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.12.orig.tar.xz' python3.13_3.13.12.orig.tar.xz 22926488 SHA512:5edecdf13999d8629f31543dffdcba521dbb5633577e481ee49275e377509a2f6d700624c26f95b57a8ff9501378d10d7c07c1d0e7e19be0d6c88f05b6315a13
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.12.orig.tar.xz.asc' python3.13_3.13.12.orig.tar.xz.asc 963 SHA512:6d42bc51b3658e1b092e7ab44306f6fc968646a7a9aeb63a3c443d1f75e27153a2138e88c15cebf8d559ce6d7744acecd4e6026c6d0be6fde070f804042d4aea
'http://archive.ubuntu.com/ubuntu/pool/main/p/python3.13/python3.13_3.13.12-1.debian.tar.xz' python3.13_3.13.12-1.debian.tar.xz 261232 SHA512:f6fb4632f19742918e197a7837fd08ff67041527c1d7a4e3ccb19455981e66f41d4c1fb4643bcb787f305104e54cb4f2e47c0ccccd6053288d1c995692ef473a
```

### `dpkg` source package: `readline=8.3-3`

Binary Packages:

- `libreadline-dev:amd64=8.3-3`
- `libreadline8t64:amd64=8.3-3`
- `readline-common=8.3-3`

Licenses: (parsed from: `/usr/share/doc/libreadline-dev/copyright`, `/usr/share/doc/libreadline8t64/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GFDL-NIV-1.3+`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC-no-attribution`

Source:

```console
$ apt-get source -qq --print-uris readline=8.3-3
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3-3.dsc' readline_8.3-3.dsc 2817 SHA512:da2062b49605d9fec2bec460bd724b333b52464506013086d5912b27a0c429753d463830f58223a718c620cc3c47249b715360374f57ed299373b9fa1dee508a
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3.orig.tar.gz' readline_8.3.orig.tar.gz 3419642 SHA512:513002753dcf5db9213dbbb61d51217245f6a40d33b1dd45238e8062dfa8eef0c890b87a5548e11db959e842724fb572c4d3d7fb433773762a63c30efe808344
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3-3.debian.tar.xz' readline_8.3-3.debian.tar.xz 34188 SHA512:3296406f695d9828dccbc8ed6dde856951fc96a625e31cbf43e59986cefb48267514062c76818914b7402fda4f95016ce2ef7cc6ab62f0a7440b91a6edc49f58
```

### `dpkg` source package: `rpcsvc-proto=1.4.3-1build1`

Binary Packages:

- `rpcsvc-proto=1.4.3-1build1`

Licenses: (parsed from: `/usr/share/doc/rpcsvc-proto/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+-autoconf-exception`
- `GPL-3`
- `GPL-3+-autoconf-exception`
- `MIT`
- `permissive-autoconf-m4`
- `permissive-autoconf-m4-no-warranty`
- `permissive-configure`
- `permissive-fsf`
- `permissive-makefile-in`

Source:

```console
$ apt-get source -qq --print-uris rpcsvc-proto=1.4.3-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1build1.dsc' rpcsvc-proto_1.4.3-1build1.dsc 2023 SHA512:b91a16587a6a6815d1ae5457f3264b7d7351b84951a2e91bca1b0be9211dd7aa945b1324ddc4865c9ee92c0c887e77aed5f8ddce544d4aa1ababe45822d95368
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3.orig.tar.xz' rpcsvc-proto_1.4.3.orig.tar.xz 167964 SHA512:e46ba9ccdd6c520128bf3a154db90742f288a4d593b094a630141cdc5aeb834ffebf9b0eb6d5d0aad9faef3c445c75e2355cbc3e1382b50d29f4d2799441c6e9
'http://archive.ubuntu.com/ubuntu/pool/main/r/rpcsvc-proto/rpcsvc-proto_1.4.3-1build1.debian.tar.xz' rpcsvc-proto_1.4.3-1build1.debian.tar.xz 4320 SHA512:e68d5150fb7dbf38e5feb38dc387301e57f5cba7348467e1d9e5763d7a8e56c5473f30e75a1551fb8fea8e8d96dbbf9a3455e67ceaf1c786adcc4b10b0f35ad2
```

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-3`

Binary Packages:

- `librtmp-dev:amd64=2.4+20151223.gitfa8646d.1-3`
- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-3`

Licenses: (parsed from: `/usr/share/doc/librtmp-dev/copyright`, `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-3
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-3.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-3.dsc 2295 SHA512:b670257b456696972739f21b9306ad38a0a36c6962dac67dac66b1091548990acd765e76a450ea57bdba30f623026487b34d6d3b5ba674abf0c009f4955ec2e4
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA512:bdfcbab73179d614a295a7b136ea4c9d0ce4620883b493f298362784d245608cd6ad4b0ad30f94ed73a086b4555399521ae9e95b6375fce75e455ae68c055e7b
'http://archive.ubuntu.com/ubuntu/pool/main/r/rtmpdump/rtmpdump_2.4%2b20151223.gitfa8646d.1-3.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-3.debian.tar.xz 8180 SHA512:63735f2e10b667d4aaa4258b581444f2e7b54ab8d223eb530acf42f4fc635e3163a00cb323aeb41ceeabf4ce94d8ec065e58c01d71efe4f71f376a9fbd66eb74
```

### `dpkg` source package: `rust-coreutils=0.6.0-0ubuntu1`

Binary Packages:

- `rust-coreutils=0.6.0-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/rust-coreutils/copyright`)

- `Apache-2.0`
- `MIT`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris rust-coreutils=0.6.0-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.6.0-0ubuntu1.dsc' rust-coreutils_0.6.0-0ubuntu1.dsc 8887 SHA512:2fe727d490049812fab52fc1e76ada442a62e47a265fb154caa3e8de6c0888979c77cffcdc04cad0059a261c9d46246f53e24ee06efb8f593532f9c70e990c68
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.6.0.orig-l10n.tar.gz' rust-coreutils_0.6.0.orig-l10n.tar.gz 620925 SHA512:4882bfa22355781052d5c85a442537d0a18e305994d32fc5f8ea4b2ec5628eed69a9d2c03d7cf0a45d3ea97266aef4790aecf6f84fcc46271ddcbbfbf60e73dc
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.6.0.orig-rust-vendor.tar.xz' rust-coreutils_0.6.0.orig-rust-vendor.tar.xz 12755792 SHA512:ded0b334233d7ab2dd72e59615c63f27926069623fbc7fb8fa016749805e7791b7c835bbe9b8b2ed5b919b025b21e1337de697f4f69cb1103142b57b378fe40f
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.6.0.orig.tar.gz' rust-coreutils_0.6.0.orig.tar.gz 3080080 SHA512:5c5aad87104d55bbb77d030f6024a5f55010971a8c4026784a2f60e89df34b7a281809cf8bd989e3fe7d08baf0fb7e04a72dd4edecd203af7ce67266a22de69b
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.6.0-0ubuntu1.debian.tar.xz' rust-coreutils_0.6.0-0ubuntu1.debian.tar.xz 19248 SHA512:ac310ace36b34b907040b0a730235887ade6d60521a92d0c3da4c0953bdc616b3be20b8abd0d7556c214002b801be164098948859611c36e7f079ccb94b4baf7
```

### `dpkg` source package: `rust-sequoia-sq=1.3.1-6`

Binary Packages:

- `sq=1.3.1-6`

Licenses: (parsed from: `/usr/share/doc/sq/copyright`)

- `GPL-2`
- `GPL-2.0-or-later`
- `LGPL-2`
- `LGPL-2.0-or-later`

Source:

```console
$ apt-get source -qq --print-uris rust-sequoia-sq=1.3.1-6
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-6.dsc' rust-sequoia-sq_1.3.1-6.dsc 4451 SHA512:20dc5deef07b7f7fc1feba1aa9386fa8229caf5c711010ff418a2791d282bf9aab4831afcca08581c2219b03cc652f6c4117011aca8043beebe15dcf3b96052c
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1.orig.tar.gz' rust-sequoia-sq_1.3.1.orig.tar.gz 740320 SHA512:3aa4468b7bcb27532907ce759852e6b92b394a2fc91953b9f3723b9deaab3661c84fb298d79ef3332467aa7a5ca1158d6a8bd65dd961d30aafdcfb34a867c880
'http://archive.ubuntu.com/ubuntu/pool/universe/r/rust-sequoia-sq/rust-sequoia-sq_1.3.1-6.debian.tar.xz' rust-sequoia-sq_1.3.1-6.debian.tar.xz 5480 SHA512:514724c31df2eee0bbe2a9726cbd90bbaaab0b8a10db1196aaff1329e5f29ecbc2ffb8f32a13d20b057edad960f5755c9a18bbc971f2933cde8d55b61c2e2612
```

### `dpkg` source package: `sed=4.9-2build2`

Binary Packages:

- `sed=4.9-2build2`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `BSD-4-clause-UC`
- `BSL-1`
- `GFDL-1.3`
- `GFDL-NIV-1.3+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `X11`
- `pcre`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sensible-utils=0.0.26build1`

Binary Packages:

- `sensible-utils=0.0.26build1`

Licenses: (parsed from: `/usr/share/doc/sensible-utils/copyright`)

- `All-permissive`
- `GPL-2`
- `GPL-2+`
- `configure`
- `installsh`

Source:

```console
$ apt-get source -qq --print-uris sensible-utils=0.0.26build1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.26build1.dsc' sensible-utils_0.0.26build1.dsc 1730 SHA512:94ebf17d5aaa6c4ce36c6ebbe2dbce8d53d8724432a42971f6faf485ed1f7a855bbbeafbb0b9343227dbd34cfaaa3e0ed4cbe19d8f77eb3e7e43e7a2ab8893df
'http://archive.ubuntu.com/ubuntu/pool/main/s/sensible-utils/sensible-utils_0.0.26build1.tar.xz' sensible-utils_0.0.26build1.tar.xz 76808 SHA512:e07fb2499d79d7fb8d50e9fb6b3f8be0cfd71722fc3275159395e4aa6d13fd5f95034454b8a669aa6f59f6997c7ebf3410739afd0700f26796bcd85f8dece713
```

### `dpkg` source package: `serf=1.3.10-3ubuntu2`

Binary Packages:

- `libserf-1-1:amd64=1.3.10-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libserf-1-1/copyright`)

- `Apache`
- `Apache-2.0`
- `Zlib`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `shadow=1:4.17.4-2ubuntu2`

Binary Packages:

- `login.defs=1:4.17.4-2ubuntu2`
- `passwd=1:4.17.4-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sqlite3=3.46.1-9`

Binary Packages:

- `libsqlite3-0:amd64=3.46.1-9`
- `libsqlite3-dev:amd64=3.46.1-9`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`, `/usr/share/doc/libsqlite3-dev/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.46.1-9
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1-9.dsc' sqlite3_3.46.1-9.dsc 2641 SHA512:be933217438ad743e42d815a8f373a561ac27377037766c4c067bd6e6e193212cb809e200d522a8472049cf01f268b8ac77be1cf5710fdcf95655c0f6e52dfb8
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1.orig-www.tar.xz' sqlite3_3.46.1.orig-www.tar.xz 5861820 SHA512:a5ec0f57d014b2f33d679cfbae0ca1935eb84871376b29216ffcc286a92a363a823ca0ec729a000d702054ee90b2fcc1887c1fb4bebfabcd14894f8ef91b7ad6
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1.orig.tar.xz' sqlite3_3.46.1.orig.tar.xz 8456776 SHA512:47d3c900d95641c89d5d807881e20e97f3b7889cf44c76d48715066ba5c1860defcd17498440d79bcc49b15c2ea28e81ed4b5b159f9e947941e5c1ee27de06ba
'http://archive.ubuntu.com/ubuntu/pool/main/s/sqlite3/sqlite3_3.46.1-9.debian.tar.xz' sqlite3_3.46.1-9.debian.tar.xz 35848 SHA512:56337376f7ae87bf33076b8c4f732ece42483339febfb68b7500922e1a5a85c93bfd0c9ec105643aab3f6995444bde06f528c50986948819dbd20c92dffd59bd
```

### `dpkg` source package: `subversion=1.14.5-6`

Binary Packages:

- `libsvn1:amd64=1.14.5-6`
- `subversion=1.14.5-6`

Licenses: (parsed from: `/usr/share/doc/libsvn1/copyright`, `/usr/share/doc/subversion/copyright`)

- `AFL-3`
- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `BoostAcMacros`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `Svnwrap`
- `Unicode`
- `Utfwidth`

Source:

```console
$ apt-get source -qq --print-uris subversion=1.14.5-6
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5-6.dsc' subversion_1.14.5-6.dsc 3976 SHA512:010f1fae3d096cc60f8ef652ecfd86bba6eeba55c14910d603c4ba3dce95055e87d8d666163dae2deb2333d7c2d5f576a1e4b3c3b563b98fa13facbb9c5c2138
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5.orig.tar.gz' subversion_1.14.5.orig.tar.gz 11645728 SHA512:a8e9f5bf9f32e4fa9a5873544c9228a392af0b4ec1126389a98cd8830c0644fc9d4b88bcb800c0e2c40bd58517cfaba23d79164c774d2cb3267a897c1d599634
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5.orig.tar.gz.asc' subversion_1.14.5.orig.tar.gz.asc 2382 SHA512:b85c4d6e77194b5edff12e3e57c7d673226253048ddf3b622bb4dee6a8aed9153d3c69477876a7caae9eebe2ff5930e42993e34c8fc33d9fa65f9a57bc005d24
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5-6.debian.tar.xz' subversion_1.14.5-6.debian.tar.xz 300584 SHA512:fa67d398bf1c8a4b3d17ee5830893597411bbac3d51fcc54cb878c009d0340b6ac30697a6b7355840fb39c3cd5083c41146d9a421f929683ad20e0954d66ff06
```

### `dpkg` source package: `sysprof=50~beta-1`

Binary Packages:

- `libsysprof-capture-4-dev:amd64=50~beta-1`

Licenses: (parsed from: `/usr/share/doc/libsysprof-capture-4-dev/copyright`)

- `BSD-2-Clause-Patent`
- `BSD-3-Clause`
- `GPL-2`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0+`
- `LGPL-2`
- `LGPL-2.0+`
- `LGPL-3`
- `LGPL-3.0+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sysprof=50~beta-1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_50%7ebeta-1.dsc' sysprof_50~beta-1.dsc 3582 SHA512:14a44b6210d3d6565cae40f257cf3f6064e40ccd18c2136c0d5d2cd9cea5d77a79c752146501a9524b38b27508679bd02b324342512c8f2e3c7afae2b68e920c
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_50%7ebeta.orig.tar.xz' sysprof_50~beta.orig.tar.xz 1275596 SHA512:2a87a3641b9f68c9b01f1097282cc2a318e675df56a3c16c48ba1cef21e04458d21b651b162a9a8960234cb6407e9528915474e86464e803665ff95a548f32ad
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_50%7ebeta-1.debian.tar.xz' sysprof_50~beta-1.debian.tar.xz 16940 SHA512:ec3b9ac7f2cf2c3cd7b4638529266190ee0dc42197c2bac06cfe43a716b8f9d56813a879b67316319535b6284b5164471ad020ebbb63a586405b4fc5d65aa9db
```

### `dpkg` source package: `systemd=257.9-0ubuntu2`

Binary Packages:

- `libsystemd0:amd64=257.9-0ubuntu2`
- `libudev1:amd64=257.9-0ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0-1.0`
- `Expat`
- `GPL-2`
- `GPL-2 with Linux-syscall-note exception`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `sysvinit=3.15-5ubuntu1`

Binary Packages:

- `sysvinit-utils=3.15-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`
- `GPL-2.0`
- `GPL-2.0+`
- `GPL-3`
- `GPL-3.0`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=3.15-5ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.15-5ubuntu1.dsc' sysvinit_3.15-5ubuntu1.dsc 2489 SHA512:1a2e3989915b6098334168ecbb5a259d0a8a528c57b3ca51a40de78b935942276901b3f01f431adce77651512859af0bfd462813312832dea973073efda91839
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.15.orig.tar.gz' sysvinit_3.15.orig.tar.gz 516469 SHA512:94613deefc08f2fe8191d08cfdd05e0ed569b9ffac40795acf6b3bddfc412ff13aeb546b279641c2b1722f505d34830e1f71cfb433c4ab94a343342a8d0f9d1b
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysvinit/sysvinit_3.15-5ubuntu1.debian.tar.xz' sysvinit_3.15-5ubuntu1.debian.tar.xz 124244 SHA512:4235cc11519557f7988a3ca93014dbd2bd43b3f72c7247e38c1ab844f8ef1b766d04643f29d307aeb187c07292e64b1677197242b9f093f474e1e9f0b15970f5
```

### `dpkg` source package: `tar=1.35+dfsg-3.1build1`

Binary Packages:

- `tar=1.35+dfsg-3.1build1`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `GPL-3+ with Bison exception`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `tiff=4.7.0-3ubuntu3`

Binary Packages:

- `libtiff-dev:amd64=4.7.0-3ubuntu3`
- `libtiff6:amd64=4.7.0-3ubuntu3`
- `libtiffxx6:amd64=4.7.0-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.7.0-3ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0-3ubuntu3.dsc' tiff_4.7.0-3ubuntu3.dsc 2368 SHA512:db14ba26d5bd5342e5e649b7ad4e47844141a4d3a0cea2ccd2b9159eae9508c58872c9c58b28ab1fe2e4224c3f370adb412dabd0ff64df344154f68e51a6025a
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0.orig.tar.bz2' tiff_4.7.0.orig.tar.bz2 2111254 SHA512:6d6f39727a4403ffaae390d54f1d7a6ff926085480422cbc4e2168e8e6490bf283e69361860d0ca0d7951543f48be550641b76d814c24a1b4e4bff1da9e27c6d
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0-3ubuntu3.debian.tar.xz' tiff_4.7.0-3ubuntu3.debian.tar.xz 27588 SHA512:d09eb851e20849139ad3069057dae7a1fc30db88c71deefb1c7927bbb5f90fecf86c86262d6984b79291bd399a844fe844199c4ecfdb32d649b8d1968890f865
```

### `dpkg` source package: `tzdata=2025c-3ubuntu3`

Binary Packages:

- `tzdata=2025c-3ubuntu3`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris tzdata=2025c-3ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025c-3ubuntu3.dsc' tzdata_2025c-3ubuntu3.dsc 2680 SHA512:6a38c833dc0c5fa7d4360e1ae65ec16bda33adc309e5f147734469f28bcea48d7d98eed180581fafefaca8e66067b2a8192eac8777a1286686308d5636604c85
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025c.orig.tar.gz' tzdata_2025c.orig.tar.gz 469363 SHA512:1e33f7212fd0ae2ad3c16e68f0c1fc7a6ad26a126b8406c379a5768d79604c6a816054bd0fe3a63228d70cd6a1fc2b1bae2a9f8014e102d3727eb9d21affa1f1
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025c.orig.tar.gz.asc' tzdata_2025c.orig.tar.gz.asc 833 SHA512:a3c734604cf77dda62eafe9148bcd846d39789d4761c7b0459151094b916df84136d4e73c914aac200c71065d4ed7f3d36cf5ee90bedbf972345de54881109ce
'http://archive.ubuntu.com/ubuntu/pool/main/t/tzdata/tzdata_2025c-3ubuntu3.debian.tar.xz' tzdata_2025c-3ubuntu3.debian.tar.xz 189384 SHA512:62f8011e9c555b79f11974b7d502b4177594a718c2424a1d6d095e7677036aec344449415a5d9da41526ec0e10e659d1755e3794809c48a0418949f85668e02e
```

### `dpkg` source package: `ubuntu-keyring=2023.11.28.1build1`

Binary Packages:

- `ubuntu-keyring=2023.11.28.1build1`

Licenses: (parsed from: `/usr/share/doc/ubuntu-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris ubuntu-keyring=2023.11.28.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1build1.dsc' ubuntu-keyring_2023.11.28.1build1.dsc 1896 SHA512:07c3c2cfb1eb230ed745245d069a4c41c8ae3f9bb82d9aeed9d1823f7c398f13b996b4708e8ccdb509347ae2764982735cdfa5927d58b4e7fa8508068148293e
'http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/ubuntu-keyring_2023.11.28.1build1.tar.xz' ubuntu-keyring_2023.11.28.1build1.tar.xz 20300 SHA512:5f6d23d46b4f6d0b0e894ca54509aa4cc6fcd3904ab58ed275111d7a5612b05ddc07664e30e516c5315f73ac28a3d81c23618fcef185cde8599131f5775b64e5
```

### `dpkg` source package: `ucf=3.0052`

Binary Packages:

- `ucf=3.0052`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0052
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0052.dsc' ucf_3.0052.dsc 1512 SHA512:04b2579fe93e2d7275325e229a045012e90535b2d795285403faf25096ec813c8895eef29733638e615f651950e591fe6fc68f0e47710b2c958edbab2254e112
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0052.tar.xz' ucf_3.0052.tar.xz 71488 SHA512:388c59769867d510eb1583dd98168b3bd6cb678bf753cde781b09ad3ebc8d38a1811293253c15dad272cfa529967474dc629f1d27b00fc4473eea6745fdc0b42
```

### `dpkg` source package: `unbound=1.24.2-1ubuntu1`

Binary Packages:

- `libunbound8:amd64=1.24.2-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libunbound8/copyright`)

- `BSD-2-VUT`
- `BSD-3-ADG`
- `BSD-3-CZ.NIC`
- `BSD-3-Farsight`
- `BSD-3-NLnetLabs`
- `BSD-3-NLnetLabs-Mekking`
- `BSD-3-Regents-DEC`
- `BSD-3-Todd-Miller`
- `BSD-3-VUT`
- `BSD-3-Viagénie`
- `BSD-3-WIDE`
- `GPL-3`
- `GPL-3+ with Bison exception`
- `ISC`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris unbound=1.24.2-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.24.2-1ubuntu1.dsc' unbound_1.24.2-1ubuntu1.dsc 3037 SHA512:a7ca49f341cb7f987ef3067b9c62075668a759f5454075e2628818e137aa32e5ed9886e911e59d5b5d048079cb1edda52ae695ac4f56794907f457713641ea31
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.24.2.orig.tar.gz' unbound_1.24.2.orig.tar.gz 6905018 SHA512:655d63ec5305323e84d82691425d74d98c332d0028517bd729d191e5f968ce9481b49ec7447d4c4906dce7997a998a115db36e911a59d2d877da5840c2080261
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.24.2-1ubuntu1.debian.tar.xz' unbound_1.24.2-1ubuntu1.debian.tar.xz 37036 SHA512:598c8da14428479dea634d793890223091f940b2b0ba343b0d70376da67e6a2619a4f2b42ba0c145798d75084f09dc189150981ade2a3a906a6e6f1fc95985f9
```

### `dpkg` source package: `unzip=6.0-29ubuntu1`

Binary Packages:

- `unzip=6.0-29ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris unzip=6.0-29ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-29ubuntu1.dsc' unzip_6.0-29ubuntu1.dsc 1987 SHA512:5b5293681b1e4be9bb115d9e9060f247a0f3c55effcfe84376e28ce01261441ffc2d3b5c69367a64972d085cb23f98a266ae663a3c4837ee233afeefe67caada
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0.orig.tar.gz' unzip_6.0.orig.tar.gz 1376845 SHA512:0694e403ebc57b37218e00ec1a406cae5cc9c5b52b6798e0d4590840b6cdbf9ddc0d9471f67af783e960f8fa2e620394d51384257dca23d06bcd90224a80ce5d
'http://archive.ubuntu.com/ubuntu/pool/main/u/unzip/unzip_6.0-29ubuntu1.debian.tar.xz' unzip_6.0-29ubuntu1.debian.tar.xz 48040 SHA512:02812bd6b96694ef3c13986651e599f0cc70af9ffae09b68cfec989dfb172636bebc93eee2b95604ed554697f4d88997c8b777b3f02d74e37d4b0d415a6a7e87
```

### `dpkg` source package: `utf8proc=2.10.0-2`

Binary Packages:

- `libutf8proc3:amd64=2.10.0-2`

Licenses: (parsed from: `/usr/share/doc/libutf8proc3/copyright`)

- `Expat`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris utf8proc=2.10.0-2
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.10.0-2.dsc' utf8proc_2.10.0-2.dsc 1404 SHA512:022121ffe94a575224be0eb4a05260720bd9cf46548f0ca08720dff7d98f4afdb9a85c1b7ad8541accdb6d95b9726ec2b798762266735f7b8d4d2e8c99edd0a5
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.10.0.orig.tar.gz' utf8proc_2.10.0.orig.tar.gz 199045 SHA512:92a771606bcbecbb86c8d101931bc042dc7035938a665a7a449c2d8a7d3255df9df9c77c5cab0fc9dcaecb04be970149f60bfff463fc813e96727b7035ca9bb4
'http://archive.ubuntu.com/ubuntu/pool/universe/u/utf8proc/utf8proc_2.10.0-2.debian.tar.xz' utf8proc_2.10.0-2.debian.tar.xz 6088 SHA512:0193f58f08b2c3cf82afb24ee4e26047bcecee16d5bdfbe24f81b564ad03642e162a6a7ceda6b0950ff18cf7d3b30cb4e8321493dfe66d3e926a867fb9a7fdf5
```

### `dpkg` source package: `util-linux=2.41.2-4ubuntu2`

Binary Packages:

- `bsdutils=1:2.41.2-4ubuntu2`
- `login=1:4.16.0-2+really2.41.2-4ubuntu2`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/login/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `BSLA`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `util-linux=2.41.2-4ubuntu3`

Binary Packages:

- `libblkid-dev:amd64=2.41.2-4ubuntu3`
- `libblkid1:amd64=2.41.2-4ubuntu3`
- `libmount-dev:amd64=2.41.2-4ubuntu3`
- `libmount1:amd64=2.41.2-4ubuntu3`
- `libsmartcols1:amd64=2.41.2-4ubuntu3`
- `libuuid1:amd64=2.41.2-4ubuntu3`
- `mount=2.41.2-4ubuntu3`
- `util-linux=2.41.2-4ubuntu3`
- `uuid-dev:amd64=2.41.2-4ubuntu3`

Licenses: (parsed from: `/usr/share/doc/libblkid-dev/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount-dev/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `BSLA`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `ISC`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris util-linux=2.41.2-4ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.2-4ubuntu3.dsc' util-linux_2.41.2-4ubuntu3.dsc 5035 SHA512:bb203bfd7ad6f76d5f2fc13a70e88f0e10f61248d3e0a204040a885b9e97437aaa8bbba7f91a3f065ff11af854aa155f43d57e5012a8235bb5913487abe87b5c
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.2.orig.tar.xz' util-linux_2.41.2.orig.tar.xz 9612488 SHA512:696c87e7cf185acc9b4b969ddade6155ea2945ae494eaecfd7b1f35d9607166cb09be79878fb793dd31b4d4dcac8c9be4be76af3886185db7ae8b58c303fb0cf
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.2-4ubuntu3.debian.tar.xz' util-linux_2.41.2-4ubuntu3.debian.tar.xz 113324 SHA512:5a6d6c20c92437737c5bc01f4e598774f54cf371e3439f88f49fb07179bdd643df87cd3941f383a3e0a3c142b700074c7c26d0c585e3965970793ed4de74309a
```

### `dpkg` source package: `wget=1.25.0-2ubuntu4`

Binary Packages:

- `wget=1.25.0-2ubuntu4`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.25.0-2ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.25.0-2ubuntu4.dsc' wget_1.25.0-2ubuntu4.dsc 2120 SHA512:c1214251f5679cf1e9d9902fb09844dbcde7f8795b4f0117f67520838d08828316e64b3eee3fdd28f53dec056c3dab8d1aef918d0de08272e6f4cff693b894ca
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.25.0.orig.tar.gz' wget_1.25.0.orig.tar.gz 5263736 SHA512:a7ce33c07a1a206a8574b6e9ea7cc5292315df0914edbcf05a014d35ae9e3d24699a46818b409b884ada57428cf30502f4bbb3767cae2c6934e4e7fb2d0c5036
'http://archive.ubuntu.com/ubuntu/pool/main/w/wget/wget_1.25.0-2ubuntu4.debian.tar.xz' wget_1.25.0-2ubuntu4.debian.tar.xz 32036 SHA512:f702ea730ab59819c3b0c3d4cc8c9c4f8b0b329b4a458ea26e74d02bab27d4011d5ac80fb2ebf86f2caa0c69415007ac3d3dca6df9d1a742f561fa2359e83809
```

### `dpkg` source package: `xorg-sgml-doctools=1:1.11-1.1build1`

Binary Packages:

- `xorg-sgml-doctools=1:1.11-1.1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xorg-sgml-doctools=1:1.11-1.1build1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1build1.dsc' xorg-sgml-doctools_1.11-1.1build1.dsc 2011 SHA512:41fe8517b833cecf40e30d7587a2ddaa8722be486f5c85746cfa87f773451eab1b507a1928b47419ae4eed74d48768710720f3e350f1ec7552b1be58ed22f99a
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11.orig.tar.gz' xorg-sgml-doctools_1.11.orig.tar.gz 150367 SHA512:a2386e41a8e2f7deaded61e00eaeab922647c0d0f4e36268c4337dc71d2412b0ec433140d080a0fd118b6112ed0a4f960280f932fe8d4a90ea9dc8bedf1eb75e
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg-sgml-doctools/xorg-sgml-doctools_1.11-1.1build1.diff.gz' xorg-sgml-doctools_1.11-1.1build1.diff.gz 3420 SHA512:a8745546eb0667dab5fe09bd17ca39da21cf1d728dafbacb568e74e264ec813950ad6cb83b231f473e572df91c47ad523e6964161b961cff5820fcdab17b4984
```

### `dpkg` source package: `xorg=1:7.7+24ubuntu2`

Binary Packages:

- `x11-common=1:7.7+24ubuntu2`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+24ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b24ubuntu2.dsc' xorg_7.7+24ubuntu2.dsc 2061 SHA512:86ddfe02615fe8205d2e5549b9a3c07a820d8acdc8432a840e99298e7affb42a85560f94b53795b67cbadbe564f196299e977ecf252c0226ca07dc176168c2aa
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b24ubuntu2.tar.xz' xorg_7.7+24ubuntu2.tar.xz 241656 SHA512:47805cbd512ebb7e522134736efb224f7ad53c6f9a306f6643f3ad79928f1137afa7b3b677d0e193c91308058667cbf982bb1ac0b5f9a400078f7e3b68ed8ae6
```

### `dpkg` source package: `xorgproto=2025.1-1`

Binary Packages:

- `x11proto-dev=2025.1-1`

Licenses: (parsed from: `/usr/share/doc/x11proto-dev/copyright`)

- `MIT`
- `SGI`

Source:

```console
$ apt-get source -qq --print-uris xorgproto=2025.1-1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2025.1-1.dsc' xorgproto_2025.1-1.dsc 3336 SHA512:f22d44559d37fbb5b2f0a687550221aa12d9bb7debee0aacc1e6519ae95c221184aa6145b9d656f59b19c742ab4e7fa72eca99b9b52d65db250c567c645b52c5
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2025.1.orig.tar.gz' xorgproto_2025.1.orig.tar.gz 1127613 SHA512:053504c8fbaf952825c4c179e8de8c3502d816b961bc483b5d4f968a41a89802c71932d8073e7b3e4ffea61bf42596e98599c6ea5c750bb48ee5514916e7e387
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2025.1.orig.tar.gz.asc' xorgproto_2025.1.orig.tar.gz.asc 195 SHA512:a71137a374c5bf5786ad9a164c75fb9ae7b5910cb5bd059816721f05bac095bf1e9ae4b075e3d8097b1d95b49120e177fa92e4776f10224ff766217ff2fff591
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorgproto/xorgproto_2025.1-1.diff.gz' xorgproto_2025.1-1.diff.gz 25174 SHA512:1d17a13e4659af704579de2368e952ce8c6bde6bf781335046935bf4d3f6c45de5e37cba4fa576ec02d7e139629b81f25324c0d5ba63c4d4e21e1a9e297c6a78
```

### `dpkg` source package: `xtrans=1.6.0-1build1`

Binary Packages:

- `xtrans-dev=1.6.0-1build1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris xtrans=1.6.0-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.6.0-1build1.dsc' xtrans_1.6.0-1build1.dsc 1907 SHA512:bd554110effa9c5047fc48e219b4500ddda9aefcd6a9f62742a7af2a68e4bd20bba2e86de81aa846f8ad97c60f56cf6109a15fbfd71954ff1b24f04cd4fa0f02
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.6.0.orig.tar.gz' xtrans_1.6.0.orig.tar.gz 239113 SHA512:1165faf7e62ba3a1eb449867b7e626d21f4191a8980ab411ef4bae3875d60333739bb843559b9a1c7e01f7175e18fc9590cd340608d2939a7588989063cecb5f
'http://archive.ubuntu.com/ubuntu/pool/main/x/xtrans/xtrans_1.6.0-1build1.diff.gz' xtrans_1.6.0-1build1.diff.gz 18591 SHA512:0fa8aaa1ef714ea8695e9d1a8e2e5608935d2a8137927422286e395f598d78ef31cfd3eb75e1d38bd8a2f9901d18d0ca1b5d9a599cbcefdb93d2ea6cb4befd1b
```

### `dpkg` source package: `xxhash=0.8.3-2build1`

Binary Packages:

- `libxxhash0:amd64=0.8.3-2build1`

Licenses: (parsed from: `/usr/share/doc/libxxhash0/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris xxhash=0.8.3-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3-2build1.dsc' xxhash_0.8.3-2build1.dsc 1968 SHA512:c0724343c725447e14dcb6478eeb56db152fa4bb8e86cdd4f2764eaee7acb9682b165c74ce8f177047305ef33249d110436865840118e703f740c58eec0115d6
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3.orig.tar.gz' xxhash_0.8.3.orig.tar.gz 1147630 SHA512:8b5c8b9aad4e869f28310b12cc314037feda81d92f26c23eaecdb35dc65042ca2e65f2e9606033e62a31bcc737a9a950500ffcbdb8677d6ab20e820ea14f2b79
'http://archive.ubuntu.com/ubuntu/pool/main/x/xxhash/xxhash_0.8.3-2build1.debian.tar.xz' xxhash_0.8.3-2build1.debian.tar.xz 5224 SHA512:ac6d91fa86c5273eaf27200b3f57ee716e8d54d346bfd950f3d2bc76a716e5765ebf1d0d1380b2bddacafa445ca7209a8ee78e2e1351b201bbe6d5c934b98390
```

### `dpkg` source package: `xz-utils=5.8.2-2`

Binary Packages:

- `liblzma-dev:amd64=5.8.2-2`
- `liblzma5:amd64=5.8.2-2`
- `xz-utils=5.8.2-2`

Licenses: (parsed from: `/usr/share/doc/liblzma-dev/copyright`, `/usr/share/doc/liblzma5/copyright`, `/usr/share/doc/xz-utils/copyright`)

- `0BSD`
- `FSFUL`
- `FSFULLR`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3.0-or-later-WITH-Autoconf-exception-macro`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PD`
- `PD-debian`
- `none`
- `permissive-nowarranty`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.8.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.2-2.dsc' xz-utils_5.8.2-2.dsc 2496 SHA512:0b55e6daf3d3f5b582452f5d062c6f06f7a918a4dd64be3eebd327827dda2677ce67c87bed746f0674f2abd8c3badff0a535334fbbede9dc51c1728fde38bb2d
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.2.orig.tar.xz' xz-utils_5.8.2.orig.tar.xz 1511132 SHA512:9cb422456d51df4261c16bcd68b188d64b778f43c875188cb140372dab9793c873111f5608c3dfe3dffe5dd6da9ba7ba96d7154d3d4fae26cb1cc22b6b66910e
'http://archive.ubuntu.com/ubuntu/pool/main/x/xz-utils/xz-utils_5.8.2-2.debian.tar.xz' xz-utils_5.8.2-2.debian.tar.xz 27228 SHA512:7b26b6c5661c2d9a8bb5912f2c8f917edaba973ddb3842b489ca7498a5627233ae7c56316c37f1d79c2ebc4d214958e0c1c92301533d9466db796df009fa2e62
```

### `dpkg` source package: `zlib=1:1.3.dfsg+really1.3.1-1ubuntu3`

Binary Packages:

- `zlib1g:amd64=1:1.3.dfsg+really1.3.1-1ubuntu3`
- `zlib1g-dev:amd64=1:1.3.dfsg+really1.3.1-1ubuntu3`

Licenses: (parsed from: `/usr/share/doc/zlib1g/copyright`, `/usr/share/doc/zlib1g-dev/copyright`)

- `Zlib`

Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.3.dfsg+really1.3.1-1ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu3.dsc' zlib_1.3.dfsg+really1.3.1-1ubuntu3.dsc 3167 SHA512:e1999f7fbd8c10fa5d277a698b679ba9c5713aeda5b97ab32f67d74c6844fdef29e3248a48797090a2dfc2b641b2c6d8ec3ad634523c10f45b2c1c699dd7a66f
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1.orig.tar.gz' zlib_1.3.dfsg+really1.3.1.orig.tar.gz 1325737 SHA512:068cb731e400cfc435db292839737938199d05d77b3010c7b9b87c9d0a127c7545198cea2a620da124ea3dfdde02ab63672aa01fc6cfd1e1ab5a2d6f9ca454c8
'http://archive.ubuntu.com/ubuntu/pool/main/z/zlib/zlib_1.3.dfsg%2breally1.3.1-1ubuntu3.debian.tar.xz' zlib_1.3.dfsg+really1.3.1-1ubuntu3.debian.tar.xz 59872 SHA512:b34ebf6afde26eccf0dc3b4e7f43c67b49763337f61a1bb66cb826e02e6d0558e72dacf35ac7365321299bea2f514c0cb3b8c53b01daf21069c57f062ea591f5
```
