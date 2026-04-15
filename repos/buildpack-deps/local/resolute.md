# `buildpack-deps:resolute`

## Docker Metadata

- Image ID: `sha256:c7732c3a432edc4489e3fd488c9028d39998fc8c5e4abaa8cb1b7b822ebb547e`
- Created: `2026-04-07T03:23:48.648497652Z`
- Virtual Size: ~ 795.78 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["/bin/bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
- Labels:
  - `org.opencontainers.image.created=2026-04-04T04:05:33.447700+00:00`
  - `org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.
`
  - `org.opencontainers.image.title=ubuntu`
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

### `dpkg` source package: `apt=3.1.16`

Binary Packages:

- `apt=3.1.16`
- `libapt-pkg7.0:amd64=3.1.16`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg7.0/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `curl`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/3.1.16/


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

### `dpkg` source package: `attr=1:2.5.2-4`

Binary Packages:

- `libattr1:amd64=1:2.5.2-4`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.5.2-4
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-4.dsc' attr_2.5.2-4.dsc 2614 SHA512:41318867cdf78e342e4b559e5b4a275ec2c4317a2387e24f00f510cee2eaa0a4f324c2e76609063205d190a966fe1fcf86ec44779cbffa009a3218772cf7c93b
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz' attr_2.5.2.orig.tar.xz 334180 SHA512:f587ea544effb7cfed63b3027bf14baba2c2dbe3a9b6c0c45fc559f7e8cb477b3e9a4a826eae30f929409468c50d11f3e7dc6d2500f41e1af8662a7e96a30ef3
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2.orig.tar.xz.asc' attr_2.5.2.orig.tar.xz.asc 833 SHA512:16362013313d055dec307bcf755a9846f5153a78309a499f8cac4ff57a2154de2bc8f3b1400e81dba7a0bf0c67aa02a5d464898ed6e4aa721b64ec95fd313968
'http://archive.ubuntu.com/ubuntu/pool/main/a/attr/attr_2.5.2-4.debian.tar.xz' attr_2.5.2-4.debian.tar.xz 32372 SHA512:bbad8871fb1edfe17e5d0ca12f0b6eb5fa944dc8676b5180a2f4d6c6f18231eb8ec64230d0efb43c61fc33969c0aebcab7699ae381f0b6c8147fc87614a10bac
```

### `dpkg` source package: `audit=1:4.1.2-1build1`

Binary Packages:

- `libaudit-common=1:4.1.2-1build1`
- `libaudit1:amd64=1:4.1.2-1build1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:4.1.2-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.1.2-1build1.dsc' audit_4.1.2-1build1.dsc 2891 SHA512:d74e9ee61b3c7cd1efaf93146b8772ce415f306f2ef6eabb0bcfe5fd0ba428ffc538b914be284c96052703747c8c57cb157313ddd83a5d6e995e7b1220a297fb
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.1.2.orig.tar.gz' audit_4.1.2.orig.tar.gz 656095 SHA512:a47fec1041e11a76ad57b57bcf6e9b454188d95ec26cabf15e92e114d46c7c8f09ddb251d5aebef8bc7faacc6ccffe44c73543d8234af237548b4ad89a408fc3
'http://archive.ubuntu.com/ubuntu/pool/main/a/audit/audit_4.1.2-1build1.debian.tar.xz' audit_4.1.2-1build1.debian.tar.xz 19800 SHA512:9567431f963f3a6f63bfe37682f6cc5d7a3b49b047b41bf7267df4c9736b9939eeb2c4d762b93828b1c0a3cc223c30d7361075211ee90552341e52dede5d3692
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

### `dpkg` source package: `bash=5.3-2ubuntu1`

Binary Packages:

- `bash=5.3-2ubuntu1`

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
$ apt-get source -qq --print-uris bash=5.3-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.3-2ubuntu1.dsc' bash_5.3-2ubuntu1.dsc 2246 SHA512:fa2d5895397e0907326385ed7aa93339a0a53524393d288af4a91eee75632408a13868ae5edadf6dbb55c617745978c0271803184025d8071723a9af2b108b5b
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.3.orig.tar.xz' bash_5.3.orig.tar.xz 5571836 SHA512:79a1800b6b579a1cc4247c67fc2aceed9a7197f2ea91a3528365297eee1b20a860af27d6d8cadc3c4a3c91a9f8ac9e04c34d7a5e80b605e1252adffedd26e932
'http://archive.ubuntu.com/ubuntu/pool/main/b/bash/bash_5.3-2ubuntu1.debian.tar.xz' bash_5.3-2ubuntu1.debian.tar.xz 98872 SHA512:1952501498230c9e42a8cf579d53597ec814fdee5bbd3d371b79dd673d4405debebb2400a6fc9d79e44bf4ac6cea18e6de2c24b1be6a7e14edad006e7c119f5f
```

### `dpkg` source package: `binutils=2.46-3ubuntu2`

Binary Packages:

- `binutils=2.46-3ubuntu2`
- `binutils-common:amd64=2.46-3ubuntu2`
- `binutils-x86-64-linux-gnu=2.46-3ubuntu2`
- `libbinutils:amd64=2.46-3ubuntu2`
- `libctf-nobfd0:amd64=2.46-3ubuntu2`
- `libctf0:amd64=2.46-3ubuntu2`
- `libgprofng0:amd64=2.46-3ubuntu2`
- `libsframe3:amd64=2.46-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/binutils/copyright`, `/usr/share/doc/binutils-common/copyright`, `/usr/share/doc/binutils-x86-64-linux-gnu/copyright`, `/usr/share/doc/libbinutils/copyright`, `/usr/share/doc/libctf-nobfd0/copyright`, `/usr/share/doc/libctf0/copyright`, `/usr/share/doc/libgprofng0/copyright`, `/usr/share/doc/libsframe3/copyright`)

- `GFDL`
- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris binutils=2.46-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.46-3ubuntu2.dsc' binutils_2.46-3ubuntu2.dsc 9064 SHA512:099842d2ab52e64ba8eaa053bd7b6581bc7c4f4d69e0d5bc6a0eca4fbb25957ac60b668d0d227706752ca41ec99721eb8c0603318334289a3046eff1a0c137a0
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.46.orig.tar.xz' binutils_2.46.orig.tar.xz 29830224 SHA512:20540d217cd57c53bc51151046b3e406ee75b80917c9b0b6c37aafaf61702ea4caec533b5554f4dea12e6e211452a6adbaa02004fec12c56e0ef31028acc427a
'http://archive.ubuntu.com/ubuntu/pool/main/b/binutils/binutils_2.46-3ubuntu2.debian.tar.xz' binutils_2.46-3ubuntu2.debian.tar.xz 136556 SHA512:88b31d97912a41f77549d5fa1fc378b23e0269157d5d0483f2d59dcfab3921f233a8eb25623bd288e0cd706ce072e4242346c42129cfd04464e90b9f92ab2043
```

### `dpkg` source package: `brotli=1.2.0-3build1`

Binary Packages:

- `libbrotli-dev:amd64=1.2.0-3build1`
- `libbrotli1:amd64=1.2.0-3build1`

Licenses: (parsed from: `/usr/share/doc/libbrotli-dev/copyright`, `/usr/share/doc/libbrotli1/copyright`)

- `MIT`

Source:

```console
$ apt-get source -qq --print-uris brotli=1.2.0-3build1
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.2.0-3build1.dsc' brotli_1.2.0-3build1.dsc 2281 SHA512:8a47d671763614d0413611bc14733fd75f116cb22d5d7530edc87a19c7de0d5a83c8723389b9800628f17e00099158e23987e77a5d35b55c11f63248a1d3b5f1
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.2.0.orig.tar.gz' brotli_1.2.0.orig.tar.gz 646398 SHA512:ceb2a1a5661296885a2f67bd2d6b02ad467cdc5fb39a82ec8e5fde26633ef4df354ebf7491c8442b090cdd38dc607857c4f9bee8aebb8ff63d44ae7322faceae
'http://archive.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.2.0-3build1.debian.tar.xz' brotli_1.2.0-3build1.debian.tar.xz 5976 SHA512:5ba45f6142daccab0f2dc71da08ecc8f8ecec5370923db06450ef0628b4c1eb5e5f805ba5d02b57b6ad14884f0cb89bb6895a9290e83e5e249ad3fe16cdccf86
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

### `dpkg` source package: `ca-certificates=20250419build1`

Binary Packages:

- `ca-certificates=20250419build1`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `coreutils=9.7-3ubuntu2`

Binary Packages:

- `gnu-coreutils=9.7-3ubuntu2`

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


### `dpkg` source package: `curl=8.18.0-1ubuntu2`

Binary Packages:

- `curl=8.18.0-1ubuntu2`
- `libcurl3t64-gnutls:amd64=8.18.0-1ubuntu2`
- `libcurl4-openssl-dev:amd64=8.18.0-1ubuntu2`
- `libcurl4t64:amd64=8.18.0-1ubuntu2`

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
$ apt-get source -qq --print-uris curl=8.18.0-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.18.0-1ubuntu2.dsc' curl_8.18.0-1ubuntu2.dsc 3259 SHA512:567ba46efd7039b451f96d8ed1ee8bfd1bd66a79c8366ef7595d404a1e55b2db92fe19591094bbaeb1c935797446c0edee16251215b71b9c3482be829760389a
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.18.0.orig.tar.gz' curl_8.18.0.orig.tar.gz 4182005 SHA512:84f193f28369ccb7fba0d8933cfc24f5fbb282b046e7e8c2c1a0da35db8ec13d17e6407c240ce3a12cf4dccac62e5919bd98f3add77065408c6259cfe1071575
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.18.0.orig.tar.gz.asc' curl_8.18.0.orig.tar.gz.asc 488 SHA512:fd31f4ff1dcb6c13f200cc67639b3760e6c47bead73f53f8700d3387792b57c8abe60e23f27d15d3ff9197490aa549e5c9910b271294cc3f75f4b37dc3c9af0c
'http://archive.ubuntu.com/ubuntu/pool/main/c/curl/curl_8.18.0-1ubuntu2.debian.tar.xz' curl_8.18.0-1ubuntu2.debian.tar.xz 60024 SHA512:978eae7396ef896b64a9ba9f76f547043a9401e4fc917fdd73e23f63e934376d08b5e8fe119220c220c2f62a362445ac450e44a9799e16a841b044af69762d1a
```

### `dpkg` source package: `cyrus-sasl2=2.1.28+dfsg1-9ubuntu3`

Binary Packages:

- `libsasl2-2:amd64=2.1.28+dfsg1-9ubuntu3`
- `libsasl2-modules-db:amd64=2.1.28+dfsg1-9ubuntu3`

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
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.28+dfsg1-9ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9ubuntu3.dsc' cyrus-sasl2_2.1.28+dfsg1-9ubuntu3.dsc 3668 SHA512:d25138154061c047834bf4c3e5959fd98351a35b1030e435d0b66c99926a7a6ce640b2ad3114feb7276613ae5c272b4adf20eaad405e7450ce8df820f142ae6e
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1.orig.tar.xz' cyrus-sasl2_2.1.28+dfsg1.orig.tar.xz 794540 SHA512:e94075d09b38a50138b782323de286deb7b15008064f07df4fa682e94367e829d9bfafef48d5478f730fef8fde536bcc6d54cab0452b76473a3c620b3dc18fa2
'http://archive.ubuntu.com/ubuntu/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.28%2bdfsg1-9ubuntu3.debian.tar.xz' cyrus-sasl2_2.1.28+dfsg1-9ubuntu3.debian.tar.xz 99600 SHA512:a1ff9e73fc72c4c31b6c11368218f069e7210b22bc19a608a2a40103809aafd9221dc3f1251dd621c2cf187247e45715141c47600e14ced9186ad96956550c51
```

### `dpkg` source package: `dash=0.5.12-12ubuntu3`

Binary Packages:

- `dash=0.5.12-12ubuntu3`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `BSD-3-Clause`
- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.12-12ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-12ubuntu3.dsc' dash_0.5.12-12ubuntu3.dsc 2060 SHA512:ebf6df8d5cf0b0a64bb1661f63608968fb80a0e422d1b7cd923a37c781da3b7f07c6c2ddf18b84980210604e74dd39915e9d3affb1697c7501c0ee5c85b40088
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12.orig.tar.gz' dash_0.5.12.orig.tar.gz 246054 SHA512:13bd262be0089260cbd13530a9cf34690c0abeb2f1920eb5e61be7951b716f9f335b86279d425dbfae56cbd49231a8fdffdff70601a5177da3d543be6fc5eb17
'http://archive.ubuntu.com/ubuntu/pool/main/d/dash/dash_0.5.12-12ubuntu3.debian.tar.xz' dash_0.5.12-12ubuntu3.debian.tar.xz 48112 SHA512:6a115502740d976493edeaa38cb8b2c64ba38c71d44494f5a70502de7493e61402826f452a39bd405005e6feaa3b58a7f1f86d20a0034a81d9c00a943e398e3e
```

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

### `dpkg` source package: `debconf=1.5.92`

Binary Packages:

- `debconf=1.5.92`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

Source:

```console
$ apt-get source -qq --print-uris debconf=1.5.92
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.92.dsc' debconf_1.5.92.dsc 2202 SHA512:d476203835f48e83eab16254520708e4283388869743fdc90d3aafe3a20e5db0b6a2575f512ae5e99144ada6b0527638c7a118ed99843d16a8a610ffeac90377
'http://archive.ubuntu.com/ubuntu/pool/main/d/debconf/debconf_1.5.92.tar.xz' debconf_1.5.92.tar.xz 610068 SHA512:7813912769918b5fe52902a09dce6747f9a81cd3f3c6388323e29d33381f48902ec2cccdab6d6f8bc92b06996ba760141155e2ddb948ac06b757bb25a70d2e42
```

### `dpkg` source package: `debianutils=5.23.2build1`

Binary Packages:

- `debianutils=5.23.2build1`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL-2`
- `GPL-2+`
- `SMAIL-GPL`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris debianutils=5.23.2build1
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.23.2build1.dsc' debianutils_5.23.2build1.dsc 1663 SHA512:4ea904c7e8aa597bc1ed9330674d0fa7948172088db543124b789e2affc03e2678e02af700370833806b13665edcf7cb775857239f4cb2d7f7d0680a325f110a
'http://archive.ubuntu.com/ubuntu/pool/main/d/debianutils/debianutils_5.23.2build1.tar.xz' debianutils_5.23.2build1.tar.xz 82192 SHA512:e238f1a9f18bf41fbc35300ad0e712a7c7980c7386fa369faa6e389c703b70e22c3753c689f4690d9084903ea4de5026e98bcaa0592ae73628178eaae43f7971
```

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

### `dpkg` source package: `dpkg=1.23.7ubuntu1`

Binary Packages:

- `dpkg=1.23.7ubuntu1`
- `dpkg-dev=1.23.7ubuntu1`
- `libdpkg-perl=1.23.7ubuntu1`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`, `/usr/share/doc/dpkg-dev/copyright`, `/usr/share/doc/libdpkg-perl/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.23.7ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.23.7ubuntu1.dsc' dpkg_1.23.7ubuntu1.dsc 3482 SHA512:b8af1554884f9057bfca85a0dc20a7c18f6ef1773b4ab423148360b069b99bed9624c8fdbbf9c0cc0626df9ea993b3f833ba7c2112c12157fd4d7696b3e8dc3a
'http://archive.ubuntu.com/ubuntu/pool/main/d/dpkg/dpkg_1.23.7ubuntu1.tar.xz' dpkg_1.23.7ubuntu1.tar.xz 5773036 SHA512:94489c924b7d8588ea156fc9593fb576c1fce1b6e159d5095aacbea33c257459af523f77a5c471bbf54f3fb7787c554e90705e40d048db28c00d2e756525c6df
```

### `dpkg` source package: `e2fsprogs=1.47.2-3ubuntu4`

Binary Packages:

- `comerr-dev:amd64=2.1-1.47.2-3ubuntu4`
- `e2fsprogs=1.47.2-3ubuntu4`
- `libcom-err2:amd64=1.47.2-3ubuntu4`
- `libext2fs2t64:amd64=1.47.2-3ubuntu4`
- `libss2:amd64=1.47.2-3ubuntu4`
- `logsave=1.47.2-3ubuntu4`

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
$ apt-get source -qq --print-uris e2fsprogs=1.47.2-3ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3ubuntu4.dsc' e2fsprogs_1.47.2-3ubuntu4.dsc 3044 SHA512:74b3266f98b98aa298447d1878550b989160180934ccb33416ba6807aad072d24333612c7e2cee976c9dc19a6182d5c08b383495aba36f7ece30af7f0f72be19
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz' e2fsprogs_1.47.2.orig.tar.gz 9996725 SHA512:dd89139c5e2bf999a22d999686ef06ab42f6ad537c6aeaa3fe68d9734d734b7396fd7ab2fd8002be26860c5653991a666d0df06c804c2f1f07f1274468ec728f
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2.orig.tar.gz.asc' e2fsprogs_1.47.2.orig.tar.gz.asc 488 SHA512:a22d46cc37497861d5a7e50076b40b8be6f459790f6eaacf0446200776fb74492ca9bfc7abc19edda3c9f7f722c318827b02f9cfbbb2118a8e86bce4d446d56b
'http://archive.ubuntu.com/ubuntu/pool/main/e/e2fsprogs/e2fsprogs_1.47.2-3ubuntu4.debian.tar.xz' e2fsprogs_1.47.2-3ubuntu4.debian.tar.xz 105780 SHA512:fdecd918d182126504e1e474d2dca96416d52b1b7bb7a492ec97b4ecb293fe4ce9e3cba22de0faa6cc541031becaf01054237352bbde8f92d411ff82b4011636
```

### `dpkg` source package: `elfutils=0.194-4`

Binary Packages:

- `libelf1t64:amd64=0.194-4`

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
$ apt-get source -qq --print-uris elfutils=0.194-4
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.194-4.dsc' elfutils_0.194-4.dsc 3416 SHA512:e606a50d9279abd318973ce3d39901c5ba831b77f33eb0543fdc8b281c3da2c83dc38f59d59af490654cd2b4a8e2f88a6a125e60d13b7971d389f5d9126473b7
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.194.orig.tar.bz2' elfutils_0.194.orig.tar.bz2 12003321 SHA512:5d00502f61b92643bf61dc61da4ddded36c423466388d992bcd388c5208761b8ed9db1a01492c085cd0984eef30c08f895a8e307e78e0df8df40b56ae35b78a5
'http://archive.ubuntu.com/ubuntu/pool/main/e/elfutils/elfutils_0.194-4.debian.tar.xz' elfutils_0.194-4.debian.tar.xz 51088 SHA512:e48c93ebfd3b84df5621cb68da9f49281804197e5d07054f39ecbf1f8afc2a042e998a5c9c1e979b65c8d3d8a71b4a94fcc4c0100ea216c2b4934127334fba43
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

### `dpkg` source package: `file=1:5.46-5build2`

Binary Packages:

- `file=1:5.46-5build2`
- `libmagic-mgc=1:5.46-5build2`
- `libmagic1t64:amd64=1:5.46-5build2`

Licenses: (parsed from: `/usr/share/doc/file/copyright`, `/usr/share/doc/libmagic-mgc/copyright`, `/usr/share/doc/libmagic1t64/copyright`)

- `BSD-2-Clause-alike`
- `BSD-2-Clause-netbsd`
- `BSD-2-Clause-regents`
- `MIT-Old-Style-with-legal-disclaimer-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris file=1:5.46-5build2
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46-5build2.dsc' file_5.46-5build2.dsc 2292 SHA512:35628d74689b13d42d7adb81cdcf0839c5b34b629204a52ed38f9e1b3c76c635411b7b216b70a0be913c637a6fafd840791b07cd9c7099dc06e7cae280d530ca
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46.orig.tar.gz' file_5.46.orig.tar.gz 1312892 SHA512:a6cb7325c49fd4af159b7555bdd38149e48a5097207acbe5e36deb5b7493ad6ea94d703da6e0edece5bb32959581741f4213707e5cb0528cd46d75a97a5242dc
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46.orig.tar.gz.asc' file_5.46.orig.tar.gz.asc 201 SHA512:a6e6fe92d909a9b153c88828942c2963b3b683cda5f6d7ae281e4ca42b30a582e82094b182976515ee85689200b8f6512d34b7f39291cbf9623d583ce688530a
'http://archive.ubuntu.com/ubuntu/pool/main/f/file/file_5.46-5build2.debian.tar.xz' file_5.46-5build2.debian.tar.xz 37172 SHA512:dadecf7ff0698f084b5d3699c3d68ac022d9670a03e6aec82346fb85e538e152b9a94d4960ad1cbaa3448cac679b1afe558dbaf5778d98c696472f56f3727b40
```

### `dpkg` source package: `findutils=4.10.0-3build2`

Binary Packages:

- `findutils=4.10.0-3build2`

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

Source:

```console
$ apt-get source -qq --print-uris findutils=4.10.0-3build2
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0-3build2.dsc' findutils_4.10.0-3build2.dsc 2315 SHA512:33cf1d1f641a7a5acbdb3e4baf10b47cfece9dc6003d53862617b58b7e897f9edaac1855206a364e1c5361274b86cbca6018b161d1333e4bff498c6e6a240746
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz' findutils_4.10.0.orig.tar.xz 2240712 SHA512:b8b683d21cd26c6da4f41c56e83cadbda4780f8610a2bbd4b4e34bb1f339c3209721974b03e076d5eef0331fd876d947b398197aad37c29bbcc2e0405c641b34
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0.orig.tar.xz.asc' findutils_4.10.0.orig.tar.xz.asc 488 SHA512:a835153a0671309021be187bf78afee58d9682acb40545aaa9dd187f0ebdea0cfa5583bd03f363243633ea056ddb0a7a6603987ab5e34a608426cb4265ac6d8f
'http://archive.ubuntu.com/ubuntu/pool/main/f/findutils/findutils_4.10.0-3build2.debian.tar.xz' findutils_4.10.0-3build2.debian.tar.xz 33524 SHA512:86b74eecc87a345390b0300d03318ca8844eab42d920f769ad5ee5ea481ca61130866342e3ba2e3debd7113e768b8cb863982ed5522991ee19923ef71c905ff9
```

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

### `dpkg` source package: `freetype=2.14.2+dfsg-1`

Binary Packages:

- `libfreetype-dev:amd64=2.14.2+dfsg-1`
- `libfreetype6:amd64=2.14.2+dfsg-1`

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
$ apt-get source -qq --print-uris freetype=2.14.2+dfsg-1
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.2%2bdfsg-1.dsc' freetype_2.14.2+dfsg-1.dsc 4011 SHA512:c47334e1119f3e819c2493e296db16c98a21971ed48d9ac66fa89171c8e5c3a02042d393634de25dd9eb83ed7a52707859c6bf23b6b3b59d2428bae33ccaeecb
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.2%2bdfsg.orig-ft2demos.tar.xz' freetype_2.14.2+dfsg.orig-ft2demos.tar.xz 347364 SHA512:efef4187b3d9cc747daad26cef6700051388435480c60e96e371eb04be3baae1e09ac932183c3a72b7bb4db1889d2bda89a70bfb058193c73bc5a602e53a3553
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.2%2bdfsg.orig-ft2demos.tar.xz.asc' freetype_2.14.2+dfsg.orig-ft2demos.tar.xz.asc 833 SHA512:569d05266c430b7fb361a5c74198e0047f44ba24fd723d13e89de8974a6ce3fc5837bbd551e2e404926e14da5db68bd50011c6fa6fa01d92460bd3eeaacdc0f2
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.2%2bdfsg.orig-ft2docs.tar.xz' freetype_2.14.2+dfsg.orig-ft2docs.tar.xz 2176140 SHA512:f2794dee78a00f91ea4241722deff64e03e7c42cbd26073ed0d7a6e0ecca14c5f87cb1dbd520ccc94311a6b0f510b4462eee3f8765e8d77841176e78d8c45837
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.2%2bdfsg.orig-ft2docs.tar.xz.asc' freetype_2.14.2+dfsg.orig-ft2docs.tar.xz.asc 833 SHA512:9a42b83c2237cd04e5cea7e5389078a985d6e22f48c030d225c32b5da9230b0c1b8ae6dd213bef4ac572fec74c5d05b9acfc011c199f0db5995293800575514a
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.2%2bdfsg.orig.tar.xz' freetype_2.14.2+dfsg.orig.tar.xz 2246044 SHA512:fa16e901edee4b578cf920eb357ec5f8aea38fe1152e7ad8562201e7edde4d763a457dfdcf69bb1b5792c0b1ba0253e6dea2b8928141e77ab53e366be1b9af65
'http://archive.ubuntu.com/ubuntu/pool/main/f/freetype/freetype_2.14.2%2bdfsg-1.debian.tar.xz' freetype_2.14.2+dfsg-1.debian.tar.xz 44108 SHA512:a5fa0b1e8a4efac56619322fe36ca23cb1ebdf7f00c516734ecd35366c5eeb1d8c3b34429cce66928a87f6fd8eb7f4fd8a18d9da332685efe8100d7eebf5cbdb
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

### `dpkg` source package: `gcc-15=15.2.0-16ubuntu1`

Binary Packages:

- `cpp-15=15.2.0-16ubuntu1`
- `cpp-15-x86-64-linux-gnu=15.2.0-16ubuntu1`
- `g++-15=15.2.0-16ubuntu1`
- `g++-15-x86-64-linux-gnu=15.2.0-16ubuntu1`
- `gcc-15=15.2.0-16ubuntu1`
- `gcc-15-base:amd64=15.2.0-16ubuntu1`
- `gcc-15-x86-64-linux-gnu=15.2.0-16ubuntu1`
- `libgcc-15-dev:amd64=15.2.0-16ubuntu1`
- `libstdc++-15-dev:amd64=15.2.0-16ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp-15/copyright`, `/usr/share/doc/cpp-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++-15/copyright`, `/usr/share/doc/g++-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc-15/copyright`, `/usr/share/doc/gcc-15-base/copyright`, `/usr/share/doc/gcc-15-x86-64-linux-gnu/copyright`, `/usr/share/doc/libgcc-15-dev/copyright`, `/usr/share/doc/libstdc++-15-dev/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-15=15.2.0-16ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0-16ubuntu1.dsc' gcc-15_15.2.0-16ubuntu1.dsc 47488 SHA512:002d375433e6e48a8658c33d9e636acd6e44810085a35c2a801dbbbdef1d99528b26ca470b47cc92647d18900a51ad4753f8372901c852acbca1e7d0532cff5d
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0.orig.tar.gz' gcc-15_15.2.0.orig.tar.gz 105962230 SHA512:83887af5c7798105d1ad85f0e9c794daa3cf030638bf40b3bff48771b8325d95c9a0d99d7d2c86c8e45499ff87f975e1914d00b72482862357645cc7ec330d38
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-15/gcc-15_15.2.0-16ubuntu1.debian.tar.xz' gcc-15_15.2.0-16ubuntu1.debian.tar.xz 3015048 SHA512:54c234377f333a360827adf4c854b8ede6c953a773f9fb96270db0333581ebc0e1ba96e19adf8a4459e6bde3cb90f728232284ff04a37c7c6e1e079bc18c473b
```

### `dpkg` source package: `gcc-16=16-20260322-1ubuntu1`

Binary Packages:

- `gcc-16-base:amd64=16-20260322-1ubuntu1`
- `libasan8:amd64=16-20260322-1ubuntu1`
- `libatomic1:amd64=16-20260322-1ubuntu1`
- `libcc1-0:amd64=16-20260322-1ubuntu1`
- `libgcc-s1:amd64=16-20260322-1ubuntu1`
- `libgomp1:amd64=16-20260322-1ubuntu1`
- `libhwasan0:amd64=16-20260322-1ubuntu1`
- `libitm1:amd64=16-20260322-1ubuntu1`
- `liblsan0:amd64=16-20260322-1ubuntu1`
- `libquadmath0:amd64=16-20260322-1ubuntu1`
- `libstdc++6:amd64=16-20260322-1ubuntu1`
- `libtsan2:amd64=16-20260322-1ubuntu1`
- `libubsan1:amd64=16-20260322-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gcc-16-base/copyright`, `/usr/share/doc/libasan8/copyright`, `/usr/share/doc/libatomic1/copyright`, `/usr/share/doc/libcc1-0/copyright`, `/usr/share/doc/libgcc-s1/copyright`, `/usr/share/doc/libgomp1/copyright`, `/usr/share/doc/libhwasan0/copyright`, `/usr/share/doc/libitm1/copyright`, `/usr/share/doc/liblsan0/copyright`, `/usr/share/doc/libquadmath0/copyright`, `/usr/share/doc/libstdc++6/copyright`, `/usr/share/doc/libtsan2/copyright`, `/usr/share/doc/libubsan1/copyright`)

- `Apache-2.0`
- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-16=16-20260322-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-16/gcc-16_16-20260322-1ubuntu1.dsc' gcc-16_16-20260322-1ubuntu1.dsc 52875 SHA512:3307ee01caeb1f7b51030e36bb1cf37ec598f8435469a7f1ed0c1c80f5ecf541602055ec058cdfdc689944cf0d9ccb7d8b02905d2026531a942e1199b3a85cf1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-16/gcc-16_16-20260322.orig.tar.gz' gcc-16_16-20260322.orig.tar.gz 101830903 SHA512:cd77ff79376e6ede6d5d3eff82204aa1df437f1d4e73e05f11676e684a2b9619722144d8eb61ef53f966364e4167592bec78f05ba5c8ed54b6e5121fa50e1bfa
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-16/gcc-16_16-20260322-1ubuntu1.debian.tar.xz' gcc-16_16-20260322-1ubuntu1.debian.tar.xz 629144 SHA512:51e9135a520ae072953bf09d714f298d5f52d0126cf944d64471f3b54db752219c51341e3beb66f3e6263a5c30f5730af0cc7429925998b8bb2eaec669b5f582
```

### `dpkg` source package: `gcc-defaults=1.230ubuntu1`

Binary Packages:

- `cpp=4:15.2.0-5ubuntu1`
- `cpp-x86-64-linux-gnu=4:15.2.0-5ubuntu1`
- `g++=4:15.2.0-5ubuntu1`
- `g++-x86-64-linux-gnu=4:15.2.0-5ubuntu1`
- `gcc=4:15.2.0-5ubuntu1`
- `gcc-x86-64-linux-gnu=4:15.2.0-5ubuntu1`

Licenses: (parsed from: `/usr/share/doc/cpp/copyright`, `/usr/share/doc/cpp-x86-64-linux-gnu/copyright`, `/usr/share/doc/g++/copyright`, `/usr/share/doc/g++-x86-64-linux-gnu/copyright`, `/usr/share/doc/gcc/copyright`, `/usr/share/doc/gcc-x86-64-linux-gnu/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris gcc-defaults=1.230ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.230ubuntu1.dsc' gcc-defaults_1.230ubuntu1.dsc 38421 SHA512:71a160af405b437ecae8498677116f48f0457d0f4fc9ad53d825e9de41d7f2a99b0b3488650d9ec90f48149eb8db34bd7b79d0db827c36132de110a8715866f9
'http://archive.ubuntu.com/ubuntu/pool/main/g/gcc-defaults/gcc-defaults_1.230ubuntu1.tar.xz' gcc-defaults_1.230ubuntu1.tar.xz 58212 SHA512:0e5b7e8dff26799cd388a5f7e608f54053891dfc970de570fed556a059606a87f5a26447ba967990f4e4650f3a68303b65ec15c5c88a8fffb36c560d96209d32
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

### `dpkg` source package: `git=1:2.53.0-1ubuntu1`

Binary Packages:

- `git=1:2.53.0-1ubuntu1`
- `git-man=1:2.53.0-1ubuntu1`

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
$ apt-get source -qq --print-uris git=1:2.53.0-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.53.0-1ubuntu1.dsc' git_2.53.0-1ubuntu1.dsc 2656 SHA512:c9ba8fba03da566978a8a0fca023f6e35a77469e7faf8b987475d84d70807e1af9ed33ab16379dfcad9d96b03cd1a430318f57e1ece4d4db9adaa8f0f2b108bd
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.53.0.orig.tar.xz' git_2.53.0.orig.tar.xz 7993096 SHA512:f9c0c0f527e10fe3eb524e368b1a24088bfd41097d8cac7854dae7ff21ab8ab2a1716384be53ea6174023ca5a2af3eeddca1d9feb57e447713f82e061df55c8d
'http://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.53.0-1ubuntu1.debian.tar.xz' git_2.53.0-1ubuntu1.debian.tar.xz 835760 SHA512:b950624dce3daf0833392c3918f9705ee7aa809432fad55cfd6d0db6c63be61d17ff186f148612607253608bd5cd142b0fe7ecf20a5e326ab0a25d155d33fd0c
```

### `dpkg` source package: `glib2.0=2.88.0-1`

Binary Packages:

- `girepository-tools:amd64=2.88.0-1`
- `libgio-2.0-dev:amd64=2.88.0-1`
- `libgio-2.0-dev-bin=2.88.0-1`
- `libgirepository-2.0-0:amd64=2.88.0-1`
- `libglib2.0-0t64:amd64=2.88.0-1`
- `libglib2.0-bin=2.88.0-1`
- `libglib2.0-data=2.88.0-1`
- `libglib2.0-dev:amd64=2.88.0-1`
- `libglib2.0-dev-bin=2.88.0-1`

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
$ apt-get source -qq --print-uris glib2.0=2.88.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.88.0-1.dsc' glib2.0_2.88.0-1.dsc 4935 SHA512:f4bd9c90ed03d14f8b507f76a955add2491bedaaad3b0240122c5c42a5969bcda5008589be03c69eabaf40822ad5ed4faa4d03ccd49f12b53698f6d0fe9d8fca
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.88.0.orig-unicode-data.tar.xz' glib2.0_2.88.0.orig-unicode-data.tar.xz 666552 SHA512:32c5e2303868cd80b85f83e94e3f1418ea050fde2f892db0463a41040db2ff0e6db7b29b0af5d0a7bd355976765d1f23ad947230d8c46696a6fd249fc465de6c
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.88.0.orig.tar.xz' glib2.0_2.88.0.orig.tar.xz 5788396 SHA512:ceead8d88720db17dc6bbff7aff14f261f90afc5e8261448aae0657f89b5fcc616cf62f4b049be88a4ddd3f50a869bbcdb66b29777da4969a47987828ecac280
'http://archive.ubuntu.com/ubuntu/pool/main/g/glib2.0/glib2.0_2.88.0-1.debian.tar.xz' glib2.0_2.88.0-1.debian.tar.xz 142452 SHA512:8130fbdad064fac9013a34845a3c00df3386d0d379267e0bfeed40f9a06a4305c5ff12342a75ece415355a23628eb35d9b568c86886074deab8fb31f6d648e8e
```

### `dpkg` source package: `glibc=2.43-2ubuntu1`

Binary Packages:

- `libc-bin=2.43-2ubuntu1`
- `libc-dev-bin=2.43-2ubuntu1`
- `libc-gconv-modules-extra:amd64=2.43-2ubuntu1`
- `libc6:amd64=2.43-2ubuntu1`
- `libc6-dev:amd64=2.43-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc-dev-bin/copyright`, `/usr/share/doc/libc-gconv-modules-extra/copyright`, `/usr/share/doc/libc6/copyright`, `/usr/share/doc/libc6-dev/copyright`)

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
$ apt-get source -qq --print-uris glibc=2.43-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.43-2ubuntu1.dsc' glibc_2.43-2ubuntu1.dsc 8169 SHA512:d03fb684cf8a16484290b1692b3e3fb8a4efbfab89d95b3c496a8157e3647e28837dd1d99267754c2f71daedb17a41c8451e863e682c0ddf16fa53b3b657211a
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.43.orig.tar.xz' glibc_2.43.orig.tar.xz 20297012 SHA512:25765f86bf54a22fc69dd13023ec9be59bd7e1f9d6ea1630cf21851898df2043bb8a01538c4b5fdd06495d0163289362b0768b391b0617f709b89a777168291c
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.43.orig.tar.xz.asc' glibc_2.43.orig.tar.xz.asc 1018 SHA512:6e26f0edee146710bcb73c3890c455e8b479009f99d284c43ea695b73bfe45e4ba47d1460300ce8c7496689b0c21a1c77e6359e005957973648b86755160c8f5
'http://archive.ubuntu.com/ubuntu/pool/main/g/glibc/glibc_2.43-2ubuntu1.debian.tar.xz' glibc_2.43-2ubuntu1.debian.tar.xz 492240 SHA512:c00cd2a038c9ec0fc85b49687193033f21070b1bc3c1416a0309c42dab78fb13ee8ca75d090e3d42845009c70deef6aca04d4b2b35781522a31fcd6a3c6d7012
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

### `dpkg` source package: `gnupg2=2.4.8-4ubuntu3`

Binary Packages:

- `dirmngr=2.4.8-4ubuntu3`
- `gnupg=2.4.8-4ubuntu3`
- `gpg=2.4.8-4ubuntu3`
- `gpg-agent=2.4.8-4ubuntu3`
- `gpgconf=2.4.8-4ubuntu3`
- `gpgsm=2.4.8-4ubuntu3`
- `gpgv=2.4.8-4ubuntu3`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

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

### `dpkg` source package: `gnutls28=3.8.12-2ubuntu1`

Binary Packages:

- `libgnutls-dane0t64:amd64=3.8.12-2ubuntu1`
- `libgnutls-openssl27t64:amd64=3.8.12-2ubuntu1`
- `libgnutls28-dev:amd64=3.8.12-2ubuntu1`
- `libgnutls30t64:amd64=3.8.12-2ubuntu1`

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
- `MIT OR Unlicense`
- `The main library is licensed under GNU Lesser`

Source:

```console
$ apt-get source -qq --print-uris gnutls28=3.8.12-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.12-2ubuntu1.dsc' gnutls28_3.8.12-2ubuntu1.dsc 3377 SHA512:6f5e89bccf9b70c4b9d1af56f7654e11cf8a15acc1b33d999dc4900d8976c8625b7e82f9ec4b4b9418148f601ec50bae5702f9167d206e46ad1b1b71300af344
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.12.orig.tar.xz' gnutls28_3.8.12.orig.tar.xz 6949604 SHA512:332a8e5200461517c7f08515e3aaab0bec6222747422e33e9e7d25d35613e3d0695a803fce226bd6a83f723054f551328bd99dcf0573e142be777dcf358e1a3b
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.12.orig.tar.xz.asc' gnutls28_3.8.12.orig.tar.xz.asc 996 SHA512:a2cb8c797b1acbcc54c6249bd503a1395bc13d878048f6fff9eca54f38472cf55e04864291a49b6c649038a318d403b5a97ae7bf4ae5a3670e542557ca248a65
'http://archive.ubuntu.com/ubuntu/pool/main/g/gnutls28/gnutls28_3.8.12-2ubuntu1.debian.tar.xz' gnutls28_3.8.12-2ubuntu1.debian.tar.xz 178684 SHA512:3567b8cc36546ead054300d21b4d82b3b4d4fe80e2c27565881f6182130af8beb349d6c12a525508d38a2955c816d62a223591cdd2a6bb372b31d673b52904e7
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

### `dpkg` source package: `gzip=1.14-1~exp2ubuntu1`

Binary Packages:

- `gzip=1.14-1~exp2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `FSF-manpages`
- `GFDL-1.3`
- `GFDL-1.3+-no-invariant`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.14-1~exp2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.14-1%7eexp2ubuntu1.dsc' gzip_1.14-1~exp2ubuntu1.dsc 1953 SHA512:1a449a403beed1e0dd07d19bcb495b936393f57c422a7ec655365322f7887cc8d889483ca346779cfca3ac7da6b9128c912bf4f5d00c5cbd235118a1f3d0b68c
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.14.orig.tar.xz' gzip_1.14.orig.tar.xz 885748 SHA512:82aef53188b3e69b51b7ddab5b8c44a11a5b73c0039b22a315a0c7d244694feab0146748add4265901eb1b4c0cee8a9eb69594995f098830d964091af97079c5
'http://archive.ubuntu.com/ubuntu/pool/main/g/gzip/gzip_1.14-1%7eexp2ubuntu1.debian.tar.xz' gzip_1.14-1~exp2ubuntu1.debian.tar.xz 21312 SHA512:d3722962561a406bf426ec36b8973cf6c072cfe6a3f02e54df951f4c21706ff235aa97c15948ca737c853d5fd46c632b573b785a83b5abb49ae0e38312e91bba
```

### `dpkg` source package: `harfbuzz=12.3.2-2`

Binary Packages:

- `libharfbuzz0b:amd64=12.3.2-2`

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
$ apt-get source -qq --print-uris harfbuzz=12.3.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_12.3.2-2.dsc' harfbuzz_12.3.2-2.dsc 2573 SHA512:6b71f1ada98e889e9af23ce1dd1208cdf0d1410d5989e9449e5e6cc0cb98d621ae1b1f209d34806f8a25c283352ed40cdeb7c20941d8c1701bb25268bbfac4a7
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_12.3.2.orig.tar.xz' harfbuzz_12.3.2.orig.tar.xz 19282952 SHA512:2bb907d206edb93a9fb0856dc2e767d491f79f20cd8e8eeeb65f284f10b67ca9ae16b6a8e72ebbfedfeaa0199af7c12dbe675eb08b7c1fb61d2f5ca1fa406782
'http://archive.ubuntu.com/ubuntu/pool/main/h/harfbuzz/harfbuzz_12.3.2-2.debian.tar.xz' harfbuzz_12.3.2-2.debian.tar.xz 19848 SHA512:3ffa4dcc11a31be67b2bd95a0b93b0a0dd337db61db9c84ece55734de26f1fbce4412493fffba6d246f19a2dcd005101167a10b02011ddc972b97eebbcb2bbe3
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

### `dpkg` source package: `imagemagick=8:7.1.2.18+dfsg1-1`

Binary Packages:

- `imagemagick=8:7.1.2.18+dfsg1-1`
- `imagemagick-7-common=8:7.1.2.18+dfsg1-1`
- `imagemagick-7.q16=8:7.1.2.18+dfsg1-1`
- `libmagickcore-7-arch-config:amd64=8:7.1.2.18+dfsg1-1`
- `libmagickcore-7-headers=8:7.1.2.18+dfsg1-1`
- `libmagickcore-7.q16-10:amd64=8:7.1.2.18+dfsg1-1`
- `libmagickcore-7.q16-10-extra:amd64=8:7.1.2.18+dfsg1-1`
- `libmagickcore-7.q16-dev:amd64=8:7.1.2.18+dfsg1-1`
- `libmagickcore-dev=8:7.1.2.18+dfsg1-1`
- `libmagickwand-7-headers=8:7.1.2.18+dfsg1-1`
- `libmagickwand-7.q16-10:amd64=8:7.1.2.18+dfsg1-1`
- `libmagickwand-7.q16-dev:amd64=8:7.1.2.18+dfsg1-1`
- `libmagickwand-dev=8:7.1.2.18+dfsg1-1`

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
$ apt-get source -qq --print-uris imagemagick=8:7.1.2.18+dfsg1-1
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.2.18%2bdfsg1-1.dsc' imagemagick_7.1.2.18+dfsg1-1.dsc 5202 SHA512:4b028784fb63e6680bc1e9c4edac26ad5d4431b5297465731e5244d26888c2a048d58f37fcd6bfc29c34035189fc5e2e33eaa7f3ed99bade73709e62bb37d06f
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.2.18%2bdfsg1.orig.tar.xz' imagemagick_7.1.2.18+dfsg1.orig.tar.xz 10531512 SHA512:e25e6783e110a84aa5a0f2fdbc4837dc8d449f36efa4125f9d49ff50fb029221ea90812e78eef75cdd512596c9bc793dbdbec2c6b76e799e686ec9a7dfbb977c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imagemagick/imagemagick_7.1.2.18%2bdfsg1-1.debian.tar.xz' imagemagick_7.1.2.18+dfsg1-1.debian.tar.xz 271492 SHA512:971e8c86e48453f24b4496daf137c839cf1c87068ea64e3faa705fb2dece12fb0e6672cc2c131026e72c4f2b4d7b14a1b5ae1bc55317f435002cc91db338372e
```

### `dpkg` source package: `imath=3.1.12-1ubuntu5`

Binary Packages:

- `libimath-3-1-29t64:amd64=3.1.12-1ubuntu5`
- `libimath-dev:amd64=3.1.12-1ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libimath-3-1-29t64/copyright`, `/usr/share/doc/libimath-dev/copyright`)

- `imath`

Source:

```console
$ apt-get source -qq --print-uris imath=3.1.12-1ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12-1ubuntu5.dsc' imath_3.1.12-1ubuntu5.dsc 2728 SHA512:fd692cc21a80dc915e837aa29b77c17b9c6757c88c8f82ca0f2288df477311791f93ed1aa322ed407bf953a3111dab007b19095042368191f1d52deea2a686a3
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12.orig.tar.gz' imath_3.1.12.orig.tar.gz 604232 SHA512:32628dfcacb610310b81ffe017a66215cf5fb84c2e0a6ac8c94a68c048be3d2b97eb57965dd253770184d5824cce1e5440b8eefb2834666b273b3193ff108343
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12.orig.tar.gz.asc' imath_3.1.12.orig.tar.gz.asc 287 SHA512:9b3978e44b531429aba42b9cc4969a470898d9d74652e3809edb0273ba9b127c471aec6570b5d352be738f59810091c0df2c70d39c16d2c32833d173b270f72c
'http://archive.ubuntu.com/ubuntu/pool/universe/i/imath/imath_3.1.12-1ubuntu5.debian.tar.xz' imath_3.1.12-1ubuntu5.debian.tar.xz 10260 SHA512:fef9caa05b4f9fda1888f20b1db00cac67b84de9cf9861bf9f43616c2f1f1fff89242898f90115d95fed9320296c600bae37feb009600d4b108d661ab1c2ea79
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

### `dpkg` source package: `krb5=1.22.1-2ubuntu4`

Binary Packages:

- `krb5-multidev:amd64=1.22.1-2ubuntu4`
- `libgssapi-krb5-2:amd64=1.22.1-2ubuntu4`
- `libgssrpc4t64:amd64=1.22.1-2ubuntu4`
- `libk5crypto3:amd64=1.22.1-2ubuntu4`
- `libkadm5clnt-mit12:amd64=1.22.1-2ubuntu4`
- `libkadm5srv-mit12:amd64=1.22.1-2ubuntu4`
- `libkdb5-10t64:amd64=1.22.1-2ubuntu4`
- `libkrb5-3:amd64=1.22.1-2ubuntu4`
- `libkrb5-dev:amd64=1.22.1-2ubuntu4`
- `libkrb5support0:amd64=1.22.1-2ubuntu4`

Licenses: (parsed from: `/usr/share/doc/krb5-multidev/copyright`, `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libgssrpc4t64/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkadm5clnt-mit12/copyright`, `/usr/share/doc/libkadm5srv-mit12/copyright`, `/usr/share/doc/libkdb5-10t64/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5-dev/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.22.1-2ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1-2ubuntu4.dsc' krb5_1.22.1-2ubuntu4.dsc 3896 SHA512:7b99a360edf6222d10785b26f050c4686eba1a3305db68ce7259c0282110c13d36efc23d8447e1f7e09e3cd71247dbd6eed443fdc1b4e2083423c946fdc8ca02
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1.orig.tar.gz' krb5_1.22.1.orig.tar.gz 8747101 SHA512:c33bfada5e0c035133436031d9818ad97b0ff08578691c832b743c55751a2cf9460501d3cc658ab79655ed7a0f9f4795ba94b363d6b616795d9bdca668825c52
'http://archive.ubuntu.com/ubuntu/pool/main/k/krb5/krb5_1.22.1-2ubuntu4.debian.tar.xz' krb5_1.22.1-2ubuntu4.debian.tar.xz 107916 SHA512:8bae60bd13db75f8c7355cedc12371e8c6c771245e259207c9ed288ed948bd73aba1d82c0d62214c0c2d56e99159cee98ab408a658805477588dc2d29f64e7e8
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

### `dpkg` source package: `libbsd=0.12.2-2build2`

Binary Packages:

- `libbsd0:amd64=0.12.2-2build2`

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

Source:

```console
$ apt-get source -qq --print-uris libbsd=0.12.2-2build2
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-2build2.dsc' libbsd_0.12.2-2build2.dsc 2371 SHA512:ca82674b3fbb54deca59e6d67fee3aa0ef4aabda2ae62cc18580e8c7f4862c2bc60a73d1604a5859a281b627a1708c076036e132e1ef1a0719c0fe8ff838b57a
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz' libbsd_0.12.2.orig.tar.xz 446032 SHA512:ce43e4f0486d5f00d4a8119ee863eaaa2f968cae4aa3d622976bb31ad601dfc565afacef7ebade5eba33fff1c329b5296c6387c008d1e1805d878431038f8b21
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2.orig.tar.xz.asc' libbsd_0.12.2.orig.tar.xz.asc 833 SHA512:c2e56aa572ce50d6342c0e45622958eba40319e09d45dc3cff6296cb10eebc0c4154d6f758dd2470a1794251fc0273d05ac2d735698eae83183769df5f7d44c3
'http://archive.ubuntu.com/ubuntu/pool/main/libb/libbsd/libbsd_0.12.2-2build2.debian.tar.xz' libbsd_0.12.2-2build2.debian.tar.xz 18852 SHA512:4e5ef3f62ec045953030948ad421c728beccb423b5dbd2fbe5ff538dafda0a3eb49f8241e3e7aa7d653c8dec81bcb12e9d33ccd2d2fb95376566ede835576959
```

### `dpkg` source package: `libcap-ng=0.8.5-4build5`

Binary Packages:

- `libcap-ng0:amd64=0.8.5-4build5`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.8.5-4build5
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4build5.dsc' libcap-ng_0.8.5-4build5.dsc 2307 SHA512:65ba0c4011fd1d102b74ef9d107c8d278c8e1fd60606066c9c159e483b26b20f429fa59f4b9a7b169c76b391c065d3208120bf109874744c27b4ad1f001468ae
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5.orig.tar.gz' libcap-ng_0.8.5.orig.tar.gz 59265 SHA512:3bd868c7f263b77edd2feda831470b407f1086b434618e54336fb78bbf8bf3bad53f4c006a2118fb594b16554f8f7ec2acb76e08be5586d0261684e9ba139231
'http://archive.ubuntu.com/ubuntu/pool/main/libc/libcap-ng/libcap-ng_0.8.5-4build5.debian.tar.xz' libcap-ng_0.8.5-4build5.debian.tar.xz 8044 SHA512:d74b7540e236fbf4e92aa1762b0c85b6fcd3356d7d44d14716a03df5020b55fc0a922f22edc8f815e964df1e1c604744702b81af0b99bfd149ad1de186d4119d
```

### `dpkg` source package: `libcap2=1:2.75-10ubuntu1`

Binary Packages:

- `libcap2:amd64=1:2.75-10ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libcap2/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `libcbor=0.10.2-2ubuntu2`

Binary Packages:

- `libcbor0.10:amd64=0.10.2-2ubuntu2`

Licenses: (parsed from: `/usr/share/doc/libcbor0.10/copyright`)

- `Expat`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `libdeflate=1.23-2ubuntu1`

Binary Packages:

- `libdeflate-dev:amd64=1.23-2ubuntu1`
- `libdeflate0:amd64=1.23-2ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libdeflate-dev/copyright`, `/usr/share/doc/libdeflate0/copyright`)

- `Expat`

Source:

```console
$ apt-get source -qq --print-uris libdeflate=1.23-2ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23-2ubuntu1.dsc' libdeflate_1.23-2ubuntu1.dsc 2340 SHA512:d6d24fea4b6e03de723b3e8cf3159109f26cd57774ef2663c2243f69d07d6c94f7e876f1271da6a7b2eb405ff297e73fed98925b11b05f1c8d47188790bea78e
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23.orig.tar.gz' libdeflate_1.23.orig.tar.gz 197519 SHA512:c1effb9c5ee8d65bc12ae3d0669a4a394acace13cc146300ed24a7f12a0ec058f66729e1ffbae268711bdcc4151143752ab2d56a099dd6394b2735e8e2f1b671
'http://archive.ubuntu.com/ubuntu/pool/main/libd/libdeflate/libdeflate_1.23-2ubuntu1.debian.tar.xz' libdeflate_1.23-2ubuntu1.debian.tar.xz 6276 SHA512:6f9005ff6a4422435b8401a684670c5881c92cfff39728712c9e70763d4f2b64dcda5c0012a3edf6ce94a84cc382d156fe14ebe8031cf4be37d9a1184c1cf541
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

### `dpkg` source package: `libexif=0.6.25-2`

Binary Packages:

- `libexif-dev:amd64=0.6.25-2`
- `libexif12:amd64=0.6.25-2`

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
$ apt-get source -qq --print-uris libexif=0.6.25-2
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25-2.dsc' libexif_0.6.25-2.dsc 2338 SHA512:5c5bb787ab46d67494fa5a3367509c297859da357c9cf7b86df183fbea8651f8021dd1a8e886ad630710fab512421e6bcb0d8c2121358fa6336ccc7b4a94e473
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25.orig.tar.gz' libexif_0.6.25.orig.tar.gz 1253324 SHA512:9e42af0d898a9d832d7b146a2085fb08eafdbb5ae476184aee1b495632172749d910f581246d22a0c68382ea9d969de54bd9539d4d877ad4dd6ca989e1b6d8db
'http://archive.ubuntu.com/ubuntu/pool/main/libe/libexif/libexif_0.6.25-2.debian.tar.xz' libexif_0.6.25-2.debian.tar.xz 12732 SHA512:44bf081a3f98e1aca767d86cb67254ac5a0d5432dd0dda6d00d3b1b7f0ed3218da4492131e2c9923ba41346f93773993cfd47d2fa5ccb304661753245d273ef4
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libffi/3.5.2-3/


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

### `dpkg` source package: `libgcrypt20=1.12.0-2`

Binary Packages:

- `libgcrypt20:amd64=1.12.0-2`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.12.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.12.0-2.dsc' libgcrypt20_1.12.0-2.dsc 2962 SHA512:a4d9ade6f3b2ec38f12d65f450753c718a197b0720d52238cd63b4c6572a2ad95b37fe75775328b84830c1e757e6d7c6832d610d39dc676430a029682f9c4567
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.12.0.orig.tar.bz2' libgcrypt20_1.12.0.orig.tar.bz2 4438947 SHA512:9421461297bd79b14f94d1ab275c3ed93b5d433531915c5cc7a718a94d32978a46feccb7a33fe63a60780ff00d465fbe1fe9ada5c250cf6d10a525c246c63d1c
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.12.0.orig.tar.bz2.asc' libgcrypt20_1.12.0.orig.tar.bz2.asc 265 SHA512:9861910a5a955e37b5c90dbb01e1fcf35cd573801004d3cf762fc33180b9bfed1db229827395b54fdb1c499004daece4b6201ec83e9ca214fff79855b691e9a9
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgcrypt20/libgcrypt20_1.12.0-2.debian.tar.xz' libgcrypt20_1.12.0-2.debian.tar.xz 42220 SHA512:d3107357361b54ec6fec6b810a7cfb90cde6496abcd551f252b6f8c760cc3834480aa5a693a277ac8c70c087404de570c87b384d9f95f81ac5e3a1e9bd3aad64
```

### `dpkg` source package: `libgpg-error=1.58-2`

Binary Packages:

- `libgpg-error0:amd64=1.58-2`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.58-2
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.58-2.dsc' libgpg-error_1.58-2.dsc 2961 SHA512:68055f98b039c86966f74d45bc80f7964ba974f0c3a3d42b961a93ec83ebadb6b92aea3edefcd3c10d8043a0f1ceb02c252712fb93c0a975f113b3474debd3ab
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.58.orig.tar.bz2' libgpg-error_1.58.orig.tar.bz2 1123899 SHA512:4f4cb7f24e6cf4266c30da3985b9e62d4ab6012d8f43e9969d6edfd344d2a08f6277ab10610627597f6c58d064b3127fd286ae678381b84610d611645db5bbb4
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.58.orig.tar.bz2.asc' libgpg-error_1.58.orig.tar.bz2.asc 265 SHA512:9836a8f5a8805529b371219f6608fdd505d1ece2bc09719f27cb79cbee9c324e635fd393341b862f6e74e3d92d6640ae24234172e64ccb09a0066fbc7c3a6d5d
'http://archive.ubuntu.com/ubuntu/pool/main/libg/libgpg-error/libgpg-error_1.58-2.debian.tar.xz' libgpg-error_1.58-2.debian.tar.xz 19792 SHA512:4688f44641aae43bc23209a120fff7f91d11652445438e111b23f62afafb15ed4d97785ce6f434b8913bfca19f29396781e5cc416b162cbcd059a947d3aa87e7
```

### `dpkg` source package: `libheif=1.21.2-3`

Binary Packages:

- `libheif-plugin-aomdec:amd64=1.21.2-3`
- `libheif1:amd64=1.21.2-3`

Licenses: (parsed from: `/usr/share/doc/libheif-plugin-aomdec/copyright`, `/usr/share/doc/libheif1/copyright`)

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
$ apt-get source -qq --print-uris libheif=1.21.2-3
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.21.2-3.dsc' libheif_1.21.2-3.dsc 3838 SHA512:65293689676d9d2ea7734485cf8c0473e8a8af5bcba28599370a72b048b540f3f0861a9408d9ea869f4164deb7d28a2ac97b1b7aeab669bbae956453825cd5bd
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.21.2.orig.tar.gz' libheif_1.21.2.orig.tar.gz 1859435 SHA512:ec7cf3a1ceafc6df01fa57b488c763da8b88971f01b71385d377036e4301d1145d743af942654e5b741468fd9d0c8ab520a9bf205c5a7d3cdd60767cec4df232
'http://archive.ubuntu.com/ubuntu/pool/main/libh/libheif/libheif_1.21.2-3.debian.tar.xz' libheif_1.21.2-3.debian.tar.xz 13400 SHA512:93a97a0d71ca16c4441d50bd939b4fc893dc6b61dbaf384d829cc9378e8b15f2961ba824aa8e6db1484d8e1710905cf0cd704b191f9122dfb270c1ab7f623b64
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `libmd=1.1.0-2build4`

Binary Packages:

- `libmd0:amd64=1.1.0-2build4`

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

Source:

```console
$ apt-get source -qq --print-uris libmd=1.1.0-2build4
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build4.dsc' libmd_1.1.0-2build4.dsc 2383 SHA512:6be3d5382e37e043339d389e06982203eb7fa852c69bbb04d5ee895891c28ebab3ebbb38cc62c470ca8d9acd59814edecac02478f3f7cbc29a7f0ba9044d3452
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz' libmd_1.1.0.orig.tar.xz 271228 SHA512:5d0da3337038e474fae7377bbc646d17214e72dc848a7aadc157f49333ce7b5ac1456e45d13674bd410ea08477c6115fc4282fed6c8e6a0bf63537a418c0df96
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0.orig.tar.xz.asc' libmd_1.1.0.orig.tar.xz.asc 833 SHA512:b0ff3baa7eedc205ee6f8b844859145fa6922c39e8f62f1e997851a65b2881649b438a37baa5800d140541da6f4dacc9f92a370f945d7461937b8cdedeca1cef
'http://archive.ubuntu.com/ubuntu/pool/main/libm/libmd/libmd_1.1.0-2build4.debian.tar.xz' libmd_1.1.0-2build4.debian.tar.xz 8584 SHA512:2953ea175c8c9ba0613dea96b751f1cf493120e3741a9efc1b2b3e571f02081705c4ca1afc0f6d190ce786ec88024cb16acf726b3aec925593dc76c6794839d6
```

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libpng1.6/1.6.55-1/


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

### `dpkg` source package: `libraw=0.21.5b-1ubuntu1`

Binary Packages:

- `libraw23t64:amd64=0.21.5b-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libraw23t64/copyright`)

- `CC-BY-SA-3.0`
- `CDDL-1.0`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libraw=0.21.5b-1ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.5b-1ubuntu1.dsc' libraw_0.21.5b-1ubuntu1.dsc 2335 SHA512:665bec1ca153054483c06effa641a8253ad03133b0b9824f8c38f32c22e12f642c4342aefbed3a8e9214854fbcda0fa26a7e33dcbc0e91d7fb06fff11d5b307c
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.5b.orig.tar.gz' libraw_0.21.5b.orig.tar.gz 566951 SHA512:09168e2ed9e5e0edff1371758433ad492a0ad50d62157b2b12cf78295f5653658b660248e0cad235c3a8bbe4fd733c0133592745d0cb1b7b6397735853fd6e9c
'http://archive.ubuntu.com/ubuntu/pool/main/libr/libraw/libraw_0.21.5b-1ubuntu1.debian.tar.xz' libraw_0.21.5b-1ubuntu1.debian.tar.xz 19072 SHA512:22c90183431fa9428dd748af96942b0f7ee0d6c0ec55b57e4038048d4a3fa8646bd63d6f2c70f89f0a84981c663ceb500f4657f09b8a390c18635744d922fec0
```

### `dpkg` source package: `libseccomp=2.6.0-2ubuntu5`

Binary Packages:

- `libseccomp2:amd64=2.6.0-2ubuntu5`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.6.0-2ubuntu5
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0-2ubuntu5.dsc' libseccomp_2.6.0-2ubuntu5.dsc 2745 SHA512:f2775de1859a890df14ff2bac09546c3d8ccff62fe5e708e06f97b4c24ea58e58968424406ef5c80555865f7ce148ece43a50bf6a3167db1b52e113c2a0f827a
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz' libseccomp_2.6.0.orig.tar.gz 685655 SHA512:9039478656d9b670af2ff4cb67b6b1fa315821e59d2f82ba6247e988859ddc7e3d15fea159eccca161bf2890828bb62aa6ab4d6b7ff55f27a9d6bd9532eeee1b
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0.orig.tar.gz.asc' libseccomp_2.6.0.orig.tar.gz.asc 833 SHA512:973b69c58085a1567f860e621e3a197be02c0ca71dad664234418cf5c00c39767efd37a7c4016f1be5bd588262617b6603855262db2ee6f31bc16061bc130e0f
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libseccomp/libseccomp_2.6.0-2ubuntu5.debian.tar.xz' libseccomp_2.6.0-2ubuntu5.debian.tar.xz 27908 SHA512:71c657e86df1e6155afefc220c0d8aecf8c250e9ab3d60c667b0032cb67caa8714dc976baf44bbd71eadc5e64364d4f07e2e365ba4fb6357630085b027fa4f45
```

### `dpkg` source package: `libselinux=3.9-4build1`

Binary Packages:

- `libselinux-dev:amd64=3.9-4build1`
- `libselinux1:amd64=3.9-4build1`

Licenses: (parsed from: `/usr/share/doc/libselinux-dev/copyright`, `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libselinux=3.9-4build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.9-4build1.dsc' libselinux_3.9-4build1.dsc 3079 SHA512:dd789c358292d8e41a5e178c6292c5d97c156447960363d5926d2c38f0bd46cfe88d3bd2eb2d256ba8a3cdbc3e22ddbd49275751b3296583b6f014b8993a93bb
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.9.orig.tar.gz' libselinux_3.9.orig.tar.gz 205334 SHA512:a91942e7d16673396610d969f2471173989995a048edacf6076f6df3200a0d541a1c9932a7632d70aa7c728de7e7d3c62712e5aab6c0b763826e7ffef808cadb
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.9.orig.tar.gz.asc' libselinux_3.9.orig.tar.gz.asc 833 SHA512:20bd4eaa75c0830b10fa8116ab787ca9d5099330c270e2e620220144b9fd239e1e2ca1ddc7ea79c1c3c6863b672530b4f875d6e68043de0da44e035b42d7d132
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libselinux/libselinux_3.9-4build1.debian.tar.xz' libselinux_3.9-4build1.debian.tar.xz 38172 SHA512:97d37f655390bfe9a9417944aae0aed83a6d8e0fe69b9e2993566b36f51175543d6e9aca017eb04b20745301b153203a93ce204aadc5b99f76dbdd2c440e79ae
```

### `dpkg` source package: `libsemanage=3.9-1build1`

Binary Packages:

- `libsemanage-common=3.9-1build1`
- `libsemanage2:amd64=3.9-1build1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage2/copyright`)

- `GPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=3.9-1build1
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.9-1build1.dsc' libsemanage_3.9-1build1.dsc 2989 SHA512:373e47000fc3aa4004328f8199af190723fc09499e0065308771b3df63d2a7df25bed4218dbfc99bc3684e17566af217361bc80f0d14f1a279648d1affb17569
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.9.orig.tar.gz' libsemanage_3.9.orig.tar.gz 185278 SHA512:a859e8d9313c922942a9be0477b387775b19c41bd108f80992112dcd2696701f40a890f5e6fc3087e7bfe69b382a1bcffa3e02c8996a719e763fbe2f6787c61c
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.9.orig.tar.gz.asc' libsemanage_3.9.orig.tar.gz.asc 833 SHA512:d01aa5d26c88c66f3f283aba9a4abf8df059180d96f557b4abc20f9d5d9a80fdf868767fb29d631d420febeb17453369d5c50fe92749c39cb5dca8a0fe5ba2b2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libsemanage/libsemanage_3.9-1build1.debian.tar.xz' libsemanage_3.9-1build1.debian.tar.xz 38084 SHA512:54acfde9a072e4b2f90e30d15604e81420460199ce2468d54b0ae69cf04b70513201dd641468e4cee4771935465844e21caa90909bd2aae157f84e91118d98df
```

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

### `dpkg` source package: `libssh2=1.11.1-1build2`

Binary Packages:

- `libssh2-1-dev:amd64=1.11.1-1build2`
- `libssh2-1t64:amd64=1.11.1-1build2`

Licenses: (parsed from: `/usr/share/doc/libssh2-1-dev/copyright`, `/usr/share/doc/libssh2-1t64/copyright`)

- `BSD3`
- `ISC`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.11.1-1build2
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1-1build2.dsc' libssh2_1.11.1-1build2.dsc 2343 SHA512:ed8c8aee475a1bfb7154e58406de9bdf3a6732c5fffd711a1e45c1c18cfed53defd81464f1d61e7865f2df11e3dcd6177470c0c03f5a18eef6249cb1f70445e8
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz' libssh2_1.11.1.orig.tar.gz 1093012 SHA512:8703636fc28f0b12c8171712f3d605e0466a5bb9ba06e136c3203548fc3408ab07defd71dc801d7009a337e1e02fd60e8933a2a526d5ef0ce53153058d201233
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1.orig.tar.gz.asc' libssh2_1.11.1.orig.tar.gz.asc 488 SHA512:83e600ddd676013932297c4f3d2cf2e65b5308f7700d818b34f30d760c7495180e6d8dae70579c8bea95ea2d7ccb12fc42641e545e11ec4b6630a0e6b350b282
'http://archive.ubuntu.com/ubuntu/pool/main/libs/libssh2/libssh2_1.11.1-1build2.debian.tar.xz' libssh2_1.11.1-1build2.debian.tar.xz 17304 SHA512:ca810a09e67a43c027ffa6d1876a3f72de2a284cead2b61cfa25f723f485448149f4d4ec248475e325b694f3071fbd0a344347aa6484966a36dea9c4ebacab35
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

### `dpkg` source package: `libunistring=1.3-2build1`

Binary Packages:

- `libunistring5:amd64=1.3-2build1`

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
$ apt-get source -qq --print-uris libunistring=1.3-2build1
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-2build1.dsc' libunistring_1.3-2build1.dsc 2210 SHA512:8de54cdbe01d9184df54c9fa9aeeaf7b09d01464721bc2769c4a4d3eef023e723166328dd77d4ab7240a4cde8e36d31d780e35fd160f05c67dbe8417f1ec6495
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz' libunistring_1.3.orig.tar.xz 2753448 SHA512:864d42b1d4ae4941fe5c8327d6726ab8e3a35d2d5f9d25ce4859a72ab2f549a7b68f58638cf8767d863f58161d1a4053495d185860964a942d6750e42facf931
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3.orig.tar.xz.asc' libunistring_1.3.orig.tar.xz.asc 833 SHA512:829229528acc8f9d13de4c43fea6caddacaf1f1cc201a7927b2c140d7ac5a81e213a1a20ba67766d6867fbe301ddddf78685f5af54e67906160807d6e8028b5a
'http://archive.ubuntu.com/ubuntu/pool/main/libu/libunistring/libunistring_1.3-2build1.debian.tar.xz' libunistring_1.3-2build1.debian.tar.xz 28548 SHA512:7dcc88d4114d94f4691e1d8bcb8ddd1417cf2d28befa8e2820ea1fd92adbcc787d8f6d2ccb18d70a8d42d5183af38e0706e763c098a7965bd4f534e7702d0b57
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

### `dpkg` source package: `libwmf=0.2.14-1`

Binary Packages:

- `libwmf-0.2-7:amd64=0.2.14-1`
- `libwmf-dev=0.2.14-1`
- `libwmflite-0.2-7:amd64=0.2.14-1`

Licenses: (parsed from: `/usr/share/doc/libwmf-0.2-7/copyright`, `/usr/share/doc/libwmf-dev/copyright`, `/usr/share/doc/libwmflite-0.2-7/copyright`)

- `AGPL-3 with Font exception`
- `GD`
- `ISC`
- `LGPL-2`
- `LGPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris libwmf=0.2.14-1
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.14-1.dsc' libwmf_0.2.14-1.dsc 2368 SHA512:fb5b8cb06d63f217b9f0d2287d3ec650c120e56ec340b848f80e373f78fca346af6e670d9582e78e850d52ae86a4470467846f649e4d500fd3603848d7bbdb2e
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.14.orig.tar.gz' libwmf_0.2.14.orig.tar.gz 2628359 SHA512:ab8b1540a4e97e8dc3e28c44749ec75279fd5ce770b081d3f436418f46891a3a5636470ea4e9ac545d25ccdba69b1f98d4c91b415ab13458aafe4a56779b0d6c
'http://archive.ubuntu.com/ubuntu/pool/main/libw/libwmf/libwmf_0.2.14-1.debian.tar.xz' libwmf_0.2.14-1.debian.tar.xz 25496 SHA512:c100f71897df9d2a9da976ee9236b603bcc2a35698e84b49460f4e028dbe5f22b385f3d5e1eeb11edafacf913bb836f2085251c6b94d5f7cbf5637e1309526f2
```

### `dpkg` source package: `libx11=2:1.8.13-1`

Binary Packages:

- `libx11-6:amd64=2:1.8.13-1`
- `libx11-data=2:1.8.13-1`
- `libx11-dev:amd64=2:1.8.13-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libx11=2:1.8.13-1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.13-1.dsc' libx11_1.8.13-1.dsc 2490 SHA512:7406dd42a4d48c81f7d197014d76e572aa0a5aac9bb39921fe544c1b40068789616969a73dd4cf9f343bc3de82de078da17edc52f9753bde101975693213119b
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.13.orig.tar.gz' libx11_1.8.13.orig.tar.gz 3217264 SHA512:3dbcb261bbf56e8613b61e84af5d6924bf804a5fb90fe84f3bde46e4bec3b0c8c496d9e2a9b6717511fd37544fe84350092a744aa98640612f653640693d791e
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.13.orig.tar.gz.asc' libx11_1.8.13.orig.tar.gz.asc 833 SHA512:172a116ff7070e1b9729f1f76b2d8dda460885c307f9a410233f49c12abbc59ad374a0b34e2c56b34a62ecb38143c1369e5ac39acd5ed3c8218840522356e4f7
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libx11/libx11_1.8.13-1.diff.gz' libx11_1.8.13-1.diff.gz 76915 SHA512:e7a8fd3953bccf97b764022740c03f70088364f15cf578436a3d5c412b9b51f4aed88d753d6ddea9cd2e6123917b5fbf60e20505edbb47574293f70c51e1573b
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

### `dpkg` source package: `libxml2=2.15.2+dfsg-0.1`

Binary Packages:

- `libxml2-16:amd64=2.15.2+dfsg-0.1`
- `libxml2-dev:amd64=2.15.2+dfsg-0.1`

Licenses: (parsed from: `/usr/share/doc/libxml2-16/copyright`, `/usr/share/doc/libxml2-dev/copyright`)

- `ISC`
- `MIT-1`

Source:

```console
$ apt-get source -qq --print-uris libxml2=2.15.2+dfsg-0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.15.2%2bdfsg-0.1.dsc' libxml2_2.15.2+dfsg-0.1.dsc 3135 SHA512:3c752ab4f83c74945187c651f5ce3571086cfbec089153990e584efb4d0dc913acbd7efc83e6975bd2437a123c1cae113505130d292e41d038fedbfc5d0457b2
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.15.2%2bdfsg.orig.tar.xz' libxml2_2.15.2+dfsg.orig.tar.xz 2154608 SHA512:d7f79a6c9435477a6b8b85e7eab8d5c69b253e2a7fbec073418ecbbd721a2feb4ebf8e04bd21ccde499d3620238fb343789cacaa6b175d9ca64a031ae07be933
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxml2/libxml2_2.15.2%2bdfsg-0.1.debian.tar.xz' libxml2_2.15.2+dfsg-0.1.debian.tar.xz 36120 SHA512:5e4fd0190b422ec5869870855357582846fa7663653922b684679805a8e80cb86555cb65b70373a6566b879f3117f627d458093c5de2b6d150d4fa28bc440eaf
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

### `dpkg` source package: `libxslt=1.1.45-0.1`

Binary Packages:

- `libxslt1-dev:amd64=1.1.45-0.1`
- `libxslt1.1:amd64=1.1.45-0.1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris libxslt=1.1.45-0.1
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.45-0.1.dsc' libxslt_1.1.45-0.1.dsc 2181 SHA512:bac9f532d885ef4101aaaf15ee0ce0cd166e5e6283ac5cb52173354e220b807e845b55927205ceeaec5ea68849a84fe0d2405b4e391738185a3ba4f950f9afdb
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.45.orig.tar.xz' libxslt_1.1.45.orig.tar.xz 1519992 SHA512:8f0608aad7250ccfe62808169d464a1641535b41a73b4fbbc1eeec9c9e785bbd8f4860d571eb567ee1e7abbd89ac3d707a5f3e3a9e836ecaf38155793ce47d78
'http://archive.ubuntu.com/ubuntu/pool/main/libx/libxslt/libxslt_1.1.45-0.1.debian.tar.xz' libxslt_1.1.45-0.1.debian.tar.xz 26428 SHA512:8390e67c46f90db424ef252cbe058bdc7bbadb5fdd7bece316f308f5c3130638e24fa63c5efd2d9a9849072bf784580efb14dce74eaa3c28d7552abceee8a53f
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

### `dpkg` source package: `linux=7.0.0-12.12`

Binary Packages:

- `linux-libc-dev:amd64=7.0.0-12.12`

Licenses: (parsed from: `/usr/share/doc/linux-libc-dev/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `lto-disabled-list=79`

Binary Packages:

- `lto-disabled-list=79`

Licenses: (parsed from: `/usr/share/doc/lto-disabled-list/copyright`)

- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lto-disabled-list=79
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_79.dsc' lto-disabled-list_79.dsc 1441 SHA512:e116038a4f5c85e0234c86d8b6d1e7b595cd9607a77cda60bbcbb6babf8f0d3b00fb76e3c0da5671e1a8f19c8896e69249a15adb36e05ce7f70f128027231f29
'http://archive.ubuntu.com/ubuntu/pool/main/l/lto-disabled-list/lto-disabled-list_79.tar.xz' lto-disabled-list_79.tar.xz 14576 SHA512:c5c0090d27777df78ce4217be67e960068ca020b59fa5a156408131436a2732e16ff3cbfd53653e3c6867bb53bada009dfc6b6f17d6dbbf81310fd8488d7ad01
```

### `dpkg` source package: `lz4=1.10.0-8`

Binary Packages:

- `liblz4-1:amd64=1.10.0-8`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=1.10.0-8
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-8.dsc' lz4_1.10.0-8.dsc 2062 SHA512:69b04e49d5d0d9bd8c5041c935f401e3dea226021c7ff9ebf200484ab59b556b0af9a4c072b2a1fa3412b838802c16f4b285176af00bb377f499a2f020708e4e
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0.orig.tar.gz' lz4_1.10.0.orig.tar.gz 387114 SHA512:8c4ceb217e6dc8e7e0beba99adc736aca8963867bcf9f970d621978ba11ce92855912f8b66138037a1d2ae171e8e17beb7be99281fea840106aa60373c455b28
'http://archive.ubuntu.com/ubuntu/pool/main/l/lz4/lz4_1.10.0-8.debian.tar.xz' lz4_1.10.0-8.debian.tar.xz 9676 SHA512:dd40a08d4b15ffdcec2137540bab7d35d1a5ac853ccb364838f9823ec18642d9e30aaea5cab31a6c858a7f5a75b8b019698aa4b6a60be12059928bd007d85b1d
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

### `dpkg` source package: `make-dfsg=4.4.1-3`

Binary Packages:

- `make=4.4.1-3`

Licenses: (parsed from: `/usr/share/doc/make/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris make-dfsg=4.4.1-3
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1-3.dsc' make-dfsg_4.4.1-3.dsc 1976 SHA512:38bdcdebb057ef98a07a7de65a76f2f5780f70fad4dc99835fb0a6ab001c68c30e54d831f64247802885aaa06db3fd2ae3b58fe950bc0804510d5413511f90fd
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1.orig.tar.xz' make-dfsg_4.4.1.orig.tar.xz 1125180 SHA512:7efa533e7c85e0f394d2a9c422c1cf854f304871f0c692ff74eac18597fa53d1a79b41ba1c56b88d8c79f2e6dfb8c3c3ba8640af15756f455167d62e7ed7b04c
'http://archive.ubuntu.com/ubuntu/pool/main/m/make-dfsg/make-dfsg_4.4.1-3.debian.tar.xz' make-dfsg_4.4.1-3.debian.tar.xz 44236 SHA512:7236506f2d13ad33ca2eb3a078243eba2b707cc1a75f5a42252f0e1219e5dad708e37bcf0dcd3b1f5c3620e7c2e678b717a87533a7d715d6da9a12df15b758e2
```

### `dpkg` source package: `mawk=1.3.4.20260129-1`

Binary Packages:

- `mawk=1.3.4.20260129-1`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `CC-BY-3.0`
- `GPL-2`
- `GPL-2.0-only`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.4.20260129-1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20260129-1.dsc' mawk_1.3.4.20260129-1.dsc 2969 SHA512:25b8713930c50d45408d357a34ea6ebfd633f0a4a756b9e27bebcfbaede98bc15fd0787ffd4dc91f4cb2b056ddf97845243b61d60447c6b30fb8a623fe924dc1
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20260129.orig.tar.gz' mawk_1.3.4.20260129.orig.tar.gz 436702 SHA512:90debb7eefc5e6b9895d74f971c87b8e1e33562d7d991d9ae07d3396322e5bb86188faef7a721cdc688f0d4e42c1bba2641d23ddb9527e2df41f9b5ca9d59724
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20260129.orig.tar.gz.asc' mawk_1.3.4.20260129.orig.tar.gz.asc 729 SHA512:4606000d69f5421d04edee6c7c8e7dea450ff86b43911fc635975267673279be564370ae7445529ed39d57342964c6424b1c86e8f764bd3cc82b38799edc8883
'http://archive.ubuntu.com/ubuntu/pool/main/m/mawk/mawk_1.3.4.20260129-1.debian.tar.xz' mawk_1.3.4.20260129-1.debian.tar.xz 16116 SHA512:aa2c8eb292241703a20a5c871ba81f98050e54d7cb6b345d40077141c592974c2f6f664c410e544e434df581e452657c60c1b9c904635f90175c20515591008c
```

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

### `dpkg` source package: `mercurial=7.2-3build1`

Binary Packages:

- `mercurial=7.2-3build1`
- `mercurial-common=7.2-3build1`

Licenses: (parsed from: `/usr/share/doc/mercurial/copyright`, `/usr/share/doc/mercurial-common/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris mercurial=7.2-3build1
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.2-3build1.dsc' mercurial_7.2-3build1.dsc 2856 SHA512:f6f0f4b12f88c1dd3dedf03a58f058fafaf1524946b2c27ac14308744ce7c602b1f2a668d963769fd4f63099a665a14851868eeef17fbec1a6e07a8f499de445
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.2.orig.tar.gz' mercurial_7.2.orig.tar.gz 9244423 SHA512:716203e038959e6641fdd8ed4bbcff8774f0d525f1709a20f51fe4faf0545bdbef1c567b382378b7bc07a3f08c620ea6a600ada2bb5a99d8da69be0155be1f7e
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.2.orig.tar.gz.asc' mercurial_7.2.orig.tar.gz.asc 659 SHA512:03aae2720cc4b9e130e8e2d9ab0a3551192e466416811dbd2f6f239f1de51161ad0421f9ee37c40e434f15a1b5c3969558b8d185c0cf1412a12823106b122a36
'http://archive.ubuntu.com/ubuntu/pool/universe/m/mercurial/mercurial_7.2-3build1.debian.tar.xz' mercurial_7.2-3build1.debian.tar.xz 54944 SHA512:34ea2cfb365fba8ecf12a5e745904f17baff2c0e5eeb981506127f5a998909d9cb7a1199420e74008866e3b2db90e1c5b7a860b323811b6991a2dcb9fc627771
```

### `dpkg` source package: `mpclib3=1.3.1-2`

Binary Packages:

- `libmpc3:amd64=1.3.1-2`

Licenses: (parsed from: `/usr/share/doc/libmpc3/copyright`)

- `LGPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mpclib3/1.3.1-2/


### `dpkg` source package: `mpfr4=4.2.2-2`

Binary Packages:

- `libmpfr6:amd64=4.2.2-2`

Licenses: (parsed from: `/usr/share/doc/libmpfr6/copyright`)

- `GFDL-1.2`
- `LGPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/mpfr4/4.2.2-2/


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

### `dpkg` source package: `netbase=6.5build1`

Binary Packages:

- `netbase=6.5build1`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=6.5build1
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.5build1.dsc' netbase_6.5build1.dsc 1527 SHA512:cbb9d44680c56f483aaefaff5cf76c6384115fa0883ae8cdeba87c41c3f9cdd54727075eeb230f63686cff07ee419a9cf455f6d1687bc52bb46f2ba847cfe9cd
'http://archive.ubuntu.com/ubuntu/pool/main/n/netbase/netbase_6.5build1.tar.xz' netbase_6.5build1.tar.xz 32620 SHA512:03132bb9c84ec4d5536dc2b7072e020584244d1adf5e9d1fffb50269a6b6d973233453e869eb672e7ed671c2e46660f510f67ec04d079fdaeab64f5019272443
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

### `dpkg` source package: `nghttp2=1.68.0-2`

Binary Packages:

- `libnghttp2-14:amd64=1.68.0-2`
- `libnghttp2-dev:amd64=1.68.0-2`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`, `/usr/share/doc/libnghttp2-dev/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `all-permissive`

Source:

```console
$ apt-get source -qq --print-uris nghttp2=1.68.0-2
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.68.0-2.dsc' nghttp2_1.68.0-2.dsc 2753 SHA512:d8be225592b6fcbeefa8ebf045431c8a167cfb5c45e18d8567c7aaa9075c50e643ba98ceb424aad0b98f9aa2a32d4de7ce2f548f690669fd06928dd582369edd
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.68.0.orig.tar.gz' nghttp2_1.68.0.orig.tar.gz 2638098 SHA512:5f9204463b7a97060ff8ca2edbb1576ec194cb8c545bd4b90a3a35d72eb2a1c39bb588f85f7e21bfb31396552e90a47c5c8ecada5273d49b7e81b23d08eb0fa5
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.68.0.orig.tar.gz.asc' nghttp2_1.68.0.orig.tar.gz.asc 833 SHA512:93eba11415c29789dac80874b2cb4f6341195f52d2b43ab9a00542bf7bf8c96d4ed776a0f91c8803998e6dea337a0635bc0a93835a5284e921867f6de1fa2581
'http://archive.ubuntu.com/ubuntu/pool/main/n/nghttp2/nghttp2_1.68.0-2.debian.tar.xz' nghttp2_1.68.0-2.debian.tar.xz 14976 SHA512:f1a5633a8e8cc6e582a7bf0915d0fa3b43696579f666d1d520751d4c5b3cd5a4b813f4d5147c1f762ac457cd8439638cdff9af5dfa254107f1cdf2570b7f3338
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

### `dpkg` source package: `openssh=1:10.2p1-2ubuntu3`

Binary Packages:

- `openssh-client=1:10.2p1-2ubuntu3`

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
$ apt-get source -qq --print-uris openssh=1:10.2p1-2ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1-2ubuntu3.dsc' openssh_10.2p1-2ubuntu3.dsc 3345 SHA512:d660734d1c75cb24fd5f57f6eccc941b1eca77ec4efd54e00ac6fd91d1467d7aa1f7e7889ad971ec269f716cfed886ab2d8a1714c34e6c87fa2241f53676b783
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1.orig.tar.gz' openssh_10.2p1.orig.tar.gz 1974519 SHA512:66f3dd646179e71aaf41c33b6f14a207dc873d71d24f11c130a89dee317ee45398b818e5b94887b5913240964a38630d7bca3e481e0f1eff2e41d9e1cfdbdfc5
'http://archive.ubuntu.com/ubuntu/pool/main/o/openssh/openssh_10.2p1-2ubuntu3.debian.tar.xz' openssh_10.2p1-2ubuntu3.debian.tar.xz 214244 SHA512:a30c4ae00fdd42b9e52e93e2a2184c0930dcb5e083b22fb9218672b81bcaf38485a1034ded964b8e249b97ecd9f09ad34a69f33f0fd2a620a648fa3bf6bacef1
```

### `dpkg` source package: `openssl=3.5.5-1ubuntu1`

Binary Packages:

- `libssl-dev:amd64=3.5.5-1ubuntu1`
- `libssl3t64:amd64=3.5.5-1ubuntu1`
- `openssl=3.5.5-1ubuntu1`
- `openssl-provider-legacy=3.5.5-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/libssl-dev/copyright`, `/usr/share/doc/libssl3t64/copyright`, `/usr/share/doc/openssl/copyright`, `/usr/share/doc/openssl-provider-legacy/copyright`)

- `Apache-2.0`
- `Artistic`
- `GPL-1`
- `GPL-1+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `p11-kit=0.26.2-2`

Binary Packages:

- `libp11-kit-dev:amd64=0.26.2-2`
- `libp11-kit0:amd64=0.26.2-2`

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
$ apt-get source -qq --print-uris p11-kit=0.26.2-2
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.26.2-2.dsc' p11-kit_0.26.2-2.dsc 2541 SHA512:eb079e1a8acc0998aa5a835e3f83e418c50cf509a760c31a896dcf4ea9067623a1994de595ff86408ce487a7e334e28317c8f92ba31bc1252c1412ca290ded58
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.26.2.orig.tar.xz' p11-kit_0.26.2.orig.tar.xz 1069216 SHA512:662c77e3133a9ee00f155fc2c1f12fdb16492920f992ab6e9de587c8abf76f990d442643bf8464cc08ad4d1c584f4d6f8d3a006aa7fc791010fa9cb7acaf6b7b
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.26.2.orig.tar.xz.asc' p11-kit_0.26.2.orig.tar.xz.asc 228 SHA512:86c518b609da5d48dfc816d70a17910b430d4ecf4315de77944c2d4250c00fe941f79b1055705630388df25924333460a4f65e1713f4d1ce141fe1f598cf658c
'http://archive.ubuntu.com/ubuntu/pool/main/p/p11-kit/p11-kit_0.26.2-2.debian.tar.xz' p11-kit_0.26.2-2.debian.tar.xz 24392 SHA512:ebd641ff88341f9e62a79d0b54bb0be653de6d2e3e34c2f49d52f3f4e5250316cc7506c6c40713e7799187c61e5e3096e0fe804be677ab79331af03c8efd8eee
```

### `dpkg` source package: `pam=1.7.0-5ubuntu3`

Binary Packages:

- `libpam-modules:amd64=1.7.0-5ubuntu3`
- `libpam-modules-bin=1.7.0-5ubuntu3`
- `libpam-runtime=1.7.0-5ubuntu3`
- `libpam0g:amd64=1.7.0-5ubuntu3`

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

Source:

```console
$ apt-get source -qq --print-uris pam=1.7.0-5ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0-5ubuntu3.dsc' pam_1.7.0-5ubuntu3.dsc 2908 SHA512:1c74137e64054a7aeb23bae5fe58f3a2797b2fa780d8d41b26afc2b8a93c25f2171b4418ac4efc40466a02b1808bab075086f19dc296a12085a310ea1b0807a8
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0.orig.tar.xz' pam_1.7.0.orig.tar.xz 507824 SHA512:ab5cadb0eb5e95e36146fdbbc77eef4e5e0f38aeee4e819b080a1316f69969c3c33e4a2daf3246ded4c2e58ce517d7f1acb0d8de02a4898ff753f4c3aeec51cf
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0.orig.tar.xz.asc' pam_1.7.0.orig.tar.xz.asc 801 SHA512:573bef1d63c0ce4efb5d1efd71a582f6ff679f2e278c326f66e142175cf67e42404453d41b92c5ce201b7d41db7b0617695f0d0972a812f0ab19553dec37192e
'http://archive.ubuntu.com/ubuntu/pool/main/p/pam/pam_1.7.0-5ubuntu3.debian.tar.xz' pam_1.7.0-5ubuntu3.debian.tar.xz 194108 SHA512:0cdc2295f7490523bd9947884546257e7b610ed1c5fada24a8be20572c0e8e8311765228630747f891a02466f92811c49bf64dd38e786a992485959f5f2b10c3
```

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

### `dpkg` source package: `perl=5.40.1-7build1`

Binary Packages:

- `libperl5.40:amd64=5.40.1-7build1`
- `perl=5.40.1-7build1`
- `perl-base=5.40.1-7build1`
- `perl-modules-5.40=5.40.1-7build1`

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
$ apt-get source -qq --print-uris perl=5.40.1-7build1
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-7build1.dsc' perl_5.40.1-7build1.dsc 2932 SHA512:94e432af9a72a7c6b45da42d7b7bc9d9b29460110e8391e72fe2562e4805e0a3450f790978677ed3dac43951f9224b9f194ffa9c3979a30e908d68e5275587bd
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig-regen-configure.tar.xz' perl_5.40.1.orig-regen-configure.tar.xz 421056 SHA512:933261779f476b0edda581270949c92e8e7dbe4bcaf1417398e708a321cdb748fe329acb703b2e74446cdfb03c20cefcab1eb972b852418ed3ea9b870db1fa86
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1.orig.tar.xz' perl_5.40.1.orig.tar.xz 13930924 SHA512:3ff16b3462ce43ff38dab21b3dfc20f81772b8c9eac19ab96ba2d5e6cbb390e2302fa76c4879f915249357cd11c7ec0d548bcbf3ab2c156df1b9fca95da3f545
'http://archive.ubuntu.com/ubuntu/pool/main/p/perl/perl_5.40.1-7build1.debian.tar.xz' perl_5.40.1-7build1.debian.tar.xz 172948 SHA512:6d47c24cd22eb767614a4780aa44a792fdc14f7d63cce15ec8adb2ea678be0ccba3f9c60e7ce3dfbbea5d22a8a64becba56a92dd657956902b1885414a45d5dd
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

### `dpkg` source package: `pkgconf=2.5.1-4`

Binary Packages:

- `libpkgconf7:amd64=2.5.1-4`
- `pkgconf:amd64=2.5.1-4`
- `pkgconf-bin=2.5.1-4`

Licenses: (parsed from: `/usr/share/doc/libpkgconf7/copyright`, `/usr/share/doc/pkgconf/copyright`, `/usr/share/doc/pkgconf-bin/copyright`)

- `BSD-2`
- `BSD-4`
- `GPL-2`
- `GPL-2+`
- `ISC`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pkgconf=2.5.1-4
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_2.5.1-4.dsc' pkgconf_2.5.1-4.dsc 1772 SHA512:679cb2e432f999848fd2a582687a72b6731bf8929037a5f7b4d9fcfb23159cd01a476314fba4099fc8f8979e7eab5660b97ec383edebee5783e664bbd26b1336
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_2.5.1.orig.tar.xz' pkgconf_2.5.1.orig.tar.xz 328064 SHA512:e654c3a460e5f0f801e8ac43ad9086f397d1da0553186ff05f5f0e18ffdac99fb652fd9b6c0379db4bc8307699699d69bc66d13cc85a4a6b0cd36462f5948a1d
'http://archive.ubuntu.com/ubuntu/pool/main/p/pkgconf/pkgconf_2.5.1-4.debian.tar.xz' pkgconf_2.5.1-4.debian.tar.xz 11116 SHA512:34fe74306fa44a22a2a3a65220195bbee57c3827376c58123486f2b50ea6aae48aa9a5d93ed0623154d373cb6d2ec1f984a1a1eae2d0b2e9c9a7225671e71c10
```

### `dpkg` source package: `postgresql-18=18.3-1`

Binary Packages:

- `libpq-dev=18.3-1`
- `libpq5:amd64=18.3-1`

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
$ apt-get source -qq --print-uris postgresql-18=18.3-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-18/postgresql-18_18.3-1.dsc' postgresql-18_18.3-1.dsc 4752 SHA512:4eca1ccb629f975343d14aedfd271ec7bffb1d859cae4050f4f09837396e4e939683774299816384ed4a79b83cf30dc16e956161bbb79b954d4dbb29cd5abe81
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-18/postgresql-18_18.3.orig.tar.bz2' postgresql-18_18.3.orig.tar.bz2 22497924 SHA512:fdbe6d726f46738cf14acab96e5c05f7d65aefe78563281b416bb14a27c7c42e4df921e26b32816a5030ddbe506b95767e2c74a35afc589916504df38d1cb11c
'http://archive.ubuntu.com/ubuntu/pool/main/p/postgresql-18/postgresql-18_18.3-1.debian.tar.xz' postgresql-18_18.3-1.debian.tar.xz 25136 SHA512:0c006e605839d8ebfb132f6507edf96d88e0fb4d8e6519847bfd90c1a8d993fde59c3f69a252712dc609fecf80a33a1a96f6390de5188ca414be859ecbb34d1c
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

### `dpkg` source package: `python-packaging=26.0-1`

Binary Packages:

- `python3-packaging=26.0-1`

Licenses: (parsed from: `/usr/share/doc/python3-packaging/copyright`)

- `Apache-2.0`
- `BSD-2-clause`
- `BSD-3-clause`
- `Expat`

Source:

```console
$ apt-get source -qq --print-uris python-packaging=26.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_26.0-1.dsc' python-packaging_26.0-1.dsc 2372 SHA512:03f00a6ac85957b915e07a204adba7b1b557f9e4698705fc7a306c40d54243a8230c8f165b002369d5265113f7e872bf103e0298db40759ba36f6297fa72e101
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_26.0.orig.tar.gz' python-packaging_26.0.orig.tar.gz 143416 SHA512:27a066a7d65ba76189212973b6a0d162f3d361848b1b0c34a82865cf180b3284a837cc34206c297f002a73feae414e25a26c5960bb884a74ea337f582585f1d2
'http://archive.ubuntu.com/ubuntu/pool/main/p/python-packaging/python-packaging_26.0-1.debian.tar.xz' python-packaging_26.0-1.debian.tar.xz 4264 SHA512:eb51c0b293e846a46d9c17806f364b6d3380ff50a93dcbd12f5e0659f463676616e5e62ebedb37106472c935dfa05515c74351353cafd3ca52c0e3ec58732742
```

### `dpkg` source package: `python3-defaults=3.14.3-0ubuntu1`

Binary Packages:

- `libpython3-stdlib:amd64=3.14.3-0ubuntu1`
- `python3=3.14.3-0ubuntu1`
- `python3-minimal=3.14.3-0ubuntu1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


### `dpkg` source package: `python3.14=3.14.3-5`

Binary Packages:

- `libpython3.14-minimal:amd64=3.14.3-5`
- `libpython3.14-stdlib:amd64=3.14.3-5`
- `python3.14=3.14.3-5`
- `python3.14-minimal=3.14.3-5`

Licenses: (parsed from: `/usr/share/doc/libpython3.14-minimal/copyright`, `/usr/share/doc/libpython3.14-stdlib/copyright`, `/usr/share/doc/python3.14/copyright`, `/usr/share/doc/python3.14-minimal/copyright`)

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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/python3.14/3.14.3-5/


### `dpkg` source package: `readline=8.3-4`

Binary Packages:

- `libreadline-dev:amd64=8.3-4`
- `libreadline8t64:amd64=8.3-4`
- `readline-common=8.3-4`

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
$ apt-get source -qq --print-uris readline=8.3-4
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3-4.dsc' readline_8.3-4.dsc 2957 SHA512:e219a8f03f3e6997de23c9291441102267ef27703839a6c6d3511afe63004ed4a3fc3d878f5848427a3856075c5b0dfd6b3f06f547b8e8d534ac31588b03e9a4
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3.orig.tar.gz' readline_8.3.orig.tar.gz 3419642 SHA512:513002753dcf5db9213dbbb61d51217245f6a40d33b1dd45238e8062dfa8eef0c890b87a5548e11db959e842724fb572c4d3d7fb433773762a63c30efe808344
'http://archive.ubuntu.com/ubuntu/pool/main/r/readline/readline_8.3-4.debian.tar.xz' readline_8.3-4.debian.tar.xz 28644 SHA512:de3d049df477623a50dd423ecb6e7bc4eaa081c502b28aaefe4e5528c1a1997403a81a1f6afeec417b4c5358374c5bbfb08f0d0eda8f29ee2a73649a232fb4f0
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

### `dpkg` source package: `rust-coreutils=0.7.0-0ubuntu1`

Binary Packages:

- `rust-coreutils=0.7.0-0ubuntu1`

Licenses: (parsed from: `/usr/share/doc/rust-coreutils/copyright`)

- `Apache-2.0`
- `MIT`
- `permissive`

Source:

```console
$ apt-get source -qq --print-uris rust-coreutils=0.7.0-0ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.7.0-0ubuntu1.dsc' rust-coreutils_0.7.0-0ubuntu1.dsc 8743 SHA512:49159f31f8f27e3ae42e6d41688da13d7e53eed1baf0b005241de81cb482fb43bd917504bb2a437206b42917daf52c9436507c4c334ac539c3d388dd9dc05cee
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.7.0.orig-l10n.tar.gz' rust-coreutils_0.7.0.orig-l10n.tar.gz 717302 SHA512:104cc87dc1949f9f890684d9c09275f942b02010d01f9d0d0069cb88ab2a084544731863c80b477668fb13735b45c20c128fa0a074f40df8d567cad62f78c9e3
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.7.0.orig-rust-vendor.tar.xz' rust-coreutils_0.7.0.orig-rust-vendor.tar.xz 12950648 SHA512:7fae7a242d08171baeb04961706d95f851c7a5f8b32d2afb09feb28eb8d5073fcf2e50b1aed6c532a0f8c857b8074488f501dc6dc3f1cb5aa0ce4443c26bb336
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.7.0.orig.tar.gz' rust-coreutils_0.7.0.orig.tar.gz 3138285 SHA512:c2d92758b28c3e61510452280046bd1d4519d810115f104006d93d909c86d0a0562ea485f8482ed18456414ebf7f9150bcef569d6cc77107a819a11686438ad7
'http://archive.ubuntu.com/ubuntu/pool/main/r/rust-coreutils/rust-coreutils_0.7.0-0ubuntu1.debian.tar.xz' rust-coreutils_0.7.0-0ubuntu1.debian.tar.xz 19612 SHA512:52b2251a6b075e62c4e6c7fe70eba3c0c0d930157a47f815e9b109a46ccc9592af931e8117e71749a680c5b55f43781f91db93e0797241f60b5f1f828fc2ee78
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

### `dpkg` source package: `sed=4.9-2build3`

Binary Packages:

- `sed=4.9-2build3`

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

Source:

```console
$ apt-get source -qq --print-uris sed=4.9-2build3
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build3.dsc' sed_4.9-2build3.dsc 1963 SHA512:4ec29eaf520175f9778cd7047e6327344aad160fd06feecb4661cace99170676fb555836ce9f10177d4082e2c001608d0fc486840a2fb4f5a0f06a395397478e
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9.orig.tar.xz' sed_4.9.orig.tar.xz 1397092 SHA512:36157a4b4a2430cf421b7bd07f1675d680d9f1616be96cf6ad6ee74a9ec0fe695f8d0b1e1f0b008bbb33cc7fcde5e1c456359bbbc63f8aebdd4fedc3982cf6dc
'http://archive.ubuntu.com/ubuntu/pool/main/s/sed/sed_4.9-2build3.debian.tar.xz' sed_4.9-2build3.debian.tar.xz 63000 SHA512:4a91097e9b63233026892caa98d907158cc6fb8fc8f35de2bc6ec4833364d1f6bb60ebae58f4cb0ba667df0728f3fed8de36e68acdc2bfc9111e2664a2a05802
```

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


### `dpkg` source package: `shadow=1:4.17.4-2ubuntu3`

Binary Packages:

- `login.defs=1:4.17.4-2ubuntu3`
- `passwd=1:4.17.4-2ubuntu3`

Licenses: (parsed from: `/usr/share/doc/login.defs/copyright`, `/usr/share/doc/passwd/copyright`)

- `BSD-3-clause`
- `GPL-1`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.17.4-2ubuntu3
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4-2ubuntu3.dsc' shadow_4.17.4-2ubuntu3.dsc 2991 SHA512:7f33c32998b04495e429129d9bad0cb963b19e9813373d983cf40ace75a2e643fc182cef9d125320190344e86d0a13e2bcf40680f10ac00da64cc07ce7063a73
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4.orig.tar.xz' shadow_4.17.4.orig.tar.xz 2326584 SHA512:06830f654650312a79ccd6d729a51808b324d594abf1c05d56a2d0880936df292ec5c9fd6c7f4ad59a6d0f2bf5be0af42afe6386c24c2c087fd64fff301bade3
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4.orig.tar.xz.asc' shadow_4.17.4.orig.tar.xz.asc 488 SHA512:24f14397a975e4b09be087705a96544ff8ad76e0aa8c708ed4a53db3a295ad0a33fd0797fc570dcbb2446d4e103a3e43922a93168f65012eba5d3fe31549ebdd
'http://archive.ubuntu.com/ubuntu/pool/main/s/shadow/shadow_4.17.4-2ubuntu3.debian.tar.xz' shadow_4.17.4-2ubuntu3.debian.tar.xz 181748 SHA512:2400077447e1fdf88777a9a9069b1329569be0cc747cf4b6b962a10ca7309f04c0f0cf430ea58149689ab05afb65a874cb5ebbe538122702b88921d0edcf3664
```

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

### `dpkg` source package: `subversion=1.14.5-6build1`

Binary Packages:

- `libsvn1:amd64=1.14.5-6build1`
- `subversion=1.14.5-6build1`

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
$ apt-get source -qq --print-uris subversion=1.14.5-6build1
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5-6build1.dsc' subversion_1.14.5-6build1.dsc 3720 SHA512:c978f8c1b2b03436cf06b4217dd2432a4f51211704792f78bdc05d76e17c6985903fa21c9aa5d7235e578534c9a802d58baf9ab3d2209bf8ce94be229661e7f2
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5.orig.tar.gz' subversion_1.14.5.orig.tar.gz 11645728 SHA512:a8e9f5bf9f32e4fa9a5873544c9228a392af0b4ec1126389a98cd8830c0644fc9d4b88bcb800c0e2c40bd58517cfaba23d79164c774d2cb3267a897c1d599634
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5.orig.tar.gz.asc' subversion_1.14.5.orig.tar.gz.asc 2382 SHA512:b85c4d6e77194b5edff12e3e57c7d673226253048ddf3b622bb4dee6a8aed9153d3c69477876a7caae9eebe2ff5930e42993e34c8fc33d9fa65f9a57bc005d24
'http://archive.ubuntu.com/ubuntu/pool/universe/s/subversion/subversion_1.14.5-6build1.debian.tar.xz' subversion_1.14.5-6build1.debian.tar.xz 300712 SHA512:a42abad66e34fbdb768c6408d058f331ba8473d52c502175b5e859b055e38287ce1e8cfe65e47c5610d11ad26787c5e7318733c1dcaa3d7abf4f42ac095a1af2
```

### `dpkg` source package: `sysprof=50.0-1`

Binary Packages:

- `libsysprof-capture-4-dev:amd64=50.0-1`

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
$ apt-get source -qq --print-uris sysprof=50.0-1
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_50.0-1.dsc' sysprof_50.0-1.dsc 3561 SHA512:7d0fedfecda0b6525c086af384117ff07fb155a292db52e5a625bbf5600301a7187613fe082292fa6ce0883860ab6b0d7f90ba0382febd1d83452d27347f4c04
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_50.0.orig.tar.xz' sysprof_50.0.orig.tar.xz 1289588 SHA512:da07515df722b59550b45c70a2f4c323defa6e561701091e33924499c9ee512ba4584cb3700936ec9a152b64dc0048811671cf37b1093b217c285c22c35d30e5
'http://archive.ubuntu.com/ubuntu/pool/main/s/sysprof/sysprof_50.0-1.debian.tar.xz' sysprof_50.0-1.debian.tar.xz 16956 SHA512:4cf222d1ca28b3cbd648d4bb47a6d257d6c1274cc3c268b5ad3353f69bc0c443581ba073dcd4b1f328ca3e029d9b97736f1f9d9accb6b3376eb8815c7da6d49c
```

### `dpkg` source package: `systemd=259.5-0ubuntu1`

Binary Packages:

- `libsystemd0:amd64=259.5-0ubuntu1`
- `libudev1:amd64=259.5-0ubuntu1`

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

### `dpkg` source package: `tar=1.35+dfsg-4`

Binary Packages:

- `tar=1.35+dfsg-4`

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

Source:

```console
$ apt-get source -qq --print-uris tar=1.35+dfsg-4
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-4.dsc' tar_1.35+dfsg-4.dsc 2034 SHA512:3035eeb3b2e6d10a8a086f615b8e8cf1a1de75ece40eca7695434c31ffdab6ee175eceb0065ccf8b9b9b3659332f5fff80833dbdd593fd78e1a4f569b6e2be02
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg.orig.tar.xz' tar_1.35+dfsg.orig.tar.xz 2111608 SHA512:3aea32b5c8de229131308420d8a7aa57f7fd1b376980456dd1aa66f97509572750c3833ab9cc2edc6fdea51f802033598c83a0d6e7f18680b1638996f0acaae7
'http://archive.ubuntu.com/ubuntu/pool/main/t/tar/tar_1.35%2bdfsg-4.debian.tar.xz' tar_1.35+dfsg-4.debian.tar.xz 21640 SHA512:8f15f5738bde72e4c234d105fbd8c088eda7c01a3b88e60c3d6b71fce80079440b8bb6a4350a7650a13f8c727e6ed9bc99b849299be5e8ec0b9fb379cea729e9
```

### `dpkg` source package: `tiff=4.7.0-3ubuntu4`

Binary Packages:

- `libtiff-dev:amd64=4.7.0-3ubuntu4`
- `libtiff6:amd64=4.7.0-3ubuntu4`
- `libtiffxx6:amd64=4.7.0-3ubuntu4`

Licenses: (parsed from: `/usr/share/doc/libtiff-dev/copyright`, `/usr/share/doc/libtiff6/copyright`, `/usr/share/doc/libtiffxx6/copyright`)

- `Hylafax`

Source:

```console
$ apt-get source -qq --print-uris tiff=4.7.0-3ubuntu4
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0-3ubuntu4.dsc' tiff_4.7.0-3ubuntu4.dsc 2368 SHA512:fd3bee1a6228adb02f34a44b83e31ec94796ff26d3ada239889cf85cf456170f82d8606e55051d08e327a2bd4a51b7b90f3ab7b319ea7b1143c44ab077f0a538
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0.orig.tar.bz2' tiff_4.7.0.orig.tar.bz2 2111254 SHA512:6d6f39727a4403ffaae390d54f1d7a6ff926085480422cbc4e2168e8e6490bf283e69361860d0ca0d7951543f48be550641b76d814c24a1b4e4bff1da9e27c6d
'http://archive.ubuntu.com/ubuntu/pool/main/t/tiff/tiff_4.7.0-3ubuntu4.debian.tar.xz' tiff_4.7.0-3ubuntu4.debian.tar.xz 27680 SHA512:3578dfad714830ded3f0c2505748167ef77c189546c6232eb698c7f835db3a3fa6db137cef9e3952d35e154fe54f4e9efe12c62d9e4a1dd786c8b0574d7bde02
```

### `dpkg` source package: `tzdata=2026a-1ubuntu1`

Binary Packages:

- `tzdata=2026a-1ubuntu1`

Licenses: (parsed from: `/usr/share/doc/tzdata/copyright`)

- `ICU`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.


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

### `dpkg` source package: `ucf=3.0052ubuntu1`

Binary Packages:

- `ucf=3.0052ubuntu1`

Licenses: (parsed from: `/usr/share/doc/ucf/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris ucf=3.0052ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0052ubuntu1.dsc' ucf_3.0052ubuntu1.dsc 1619 SHA512:48d088d41eee2fbd4945aa56ccf4deb50930f92f7d6074875f6261ebb55b00bb0527b63b1d9d98be52e39d9311a5a55888ecfbc82426ac26d16f74edf0ecd972
'http://archive.ubuntu.com/ubuntu/pool/main/u/ucf/ucf_3.0052ubuntu1.tar.xz' ucf_3.0052ubuntu1.tar.xz 71700 SHA512:9527efa31392d165cae80677a79695cf0b12eafe168eeadeed0de470494acd974a6947c0497db76047596149f11937fde092294a7af7f1cf143a7d6f40a105a4
```

### `dpkg` source package: `unbound=1.24.2-1ubuntu2`

Binary Packages:

- `libunbound8:amd64=1.24.2-1ubuntu2`

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
$ apt-get source -qq --print-uris unbound=1.24.2-1ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.24.2-1ubuntu2.dsc' unbound_1.24.2-1ubuntu2.dsc 3037 SHA512:119fadaa8db3e6e958dc4f4ed6e4ef7a387999aad741cb81c29a50c87aa967cce45954577c7e5694d2d6f067ac20c8217a85bbf9730cf89d34ea394a2e248d70
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.24.2.orig.tar.gz' unbound_1.24.2.orig.tar.gz 6905018 SHA512:655d63ec5305323e84d82691425d74d98c332d0028517bd729d191e5f968ce9481b49ec7447d4c4906dce7997a998a115db36e911a59d2d877da5840c2080261
'http://archive.ubuntu.com/ubuntu/pool/main/u/unbound/unbound_1.24.2-1ubuntu2.debian.tar.xz' unbound_1.24.2-1ubuntu2.debian.tar.xz 37084 SHA512:70c0e8c2122301dc211e0d27a03030863ec6428164ce1a824ee2feef4b0f142dd5072a4ef7a9329708627722a3337deb76d5ecb7f23d2944adeb3ff283c123c5
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

### `dpkg` source package: `util-linux=2.41.3-3ubuntu2`

Binary Packages:

- `bsdutils=1:2.41.3-3ubuntu2`
- `libblkid-dev:amd64=2.41.3-3ubuntu2`
- `libblkid1:amd64=2.41.3-3ubuntu2`
- `libmount-dev:amd64=2.41.3-3ubuntu2`
- `libmount1:amd64=2.41.3-3ubuntu2`
- `libsmartcols1:amd64=2.41.3-3ubuntu2`
- `libuuid1:amd64=2.41.3-3ubuntu2`
- `login=1:4.16.0-2+really2.41.3-3ubuntu2`
- `mount=2.41.3-3ubuntu2`
- `util-linux=2.41.3-3ubuntu2`
- `uuid-dev:amd64=2.41.3-3ubuntu2`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/libblkid-dev/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libmount-dev/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/login/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`, `/usr/share/doc/uuid-dev/copyright`)

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
$ apt-get source -qq --print-uris util-linux=2.41.3-3ubuntu2
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.3-3ubuntu2.dsc' util-linux_2.41.3-3ubuntu2.dsc 5439 SHA512:a7b05b69289a99de9a9f6f015af3392c385ab2e6e0927ed65bfa13faf546438e436c459edbcb0f2525481deb83b27964815416a5a3acc341c63abd046434163f
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.3.orig.tar.xz' util-linux_2.41.3.orig.tar.xz 9467224 SHA512:3d299f0e05a4c982a04dbcbaaeff1222152feedf51c56c5dbdeb75999c68269d652a994f5cdf4c1ee42bb7b28475dd0792192c299fd9bc3b45198c5b153dad00
'http://archive.ubuntu.com/ubuntu/pool/main/u/util-linux/util-linux_2.41.3-3ubuntu2.debian.tar.xz' util-linux_2.41.3-3ubuntu2.debian.tar.xz 116776 SHA512:0b0099e529b9a07814ff8d835e810c54082ff2101838277043faaaa994a57122e9fdd1591d17bc1f206a906113f66fc07ff8f33d1108c3442e36a0063880b21c
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

### `dpkg` source package: `xorg=1:7.7+26ubuntu1`

Binary Packages:

- `x11-common=1:7.7+26ubuntu1`

Licenses: (parsed from: `/usr/share/doc/x11-common/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris xorg=1:7.7+26ubuntu1
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b26ubuntu1.dsc' xorg_7.7+26ubuntu1.dsc 2047 SHA512:afeb81755bfb109c9f4bcf35bc40d6d33b167c18db3e0773a058c09ab42598c0ef791838b29cec17de88a2a6a20388aa52bbba9fd0a225ed52991752005842d9
'http://archive.ubuntu.com/ubuntu/pool/main/x/xorg/xorg_7.7%2b26ubuntu1.tar.xz' xorg_7.7+26ubuntu1.tar.xz 241928 SHA512:ed2ef9d9ead2055f4970d0ed435c6fce784789852d72802208dfd12e54a811e2d957c4f0769f0900ba16100ee876c24806d20e0624a860dafce99b196239cf75
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

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/xz-utils/5.8.2-2/


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
