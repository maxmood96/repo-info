## `debian:stable-backports`

```console
$ docker pull debian@sha256:a1b892ad837cfe5f87e323a63e523bfbf273823009fdc8b6591d280f1bc3d6f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:b1d48c795995eecc99a5acb476f9d301d02e0a16661cc8aedac0a01b42c4d900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48491422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca989295c390fcfeea051fd1809dcb2d2307b72bd04bd8552550c896b91bfe3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:03aa13039ade077a5f450c72b9578c25fa5ee5a69e6cd263319496355a3379ce`  
		Last Modified: Thu, 08 May 2025 17:05:44 GMT  
		Size: 48.5 MB (48491200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5df09c66c06d8346c14426a1e2dc189ab40b8230e4c75002ceccf06a8f32bd`  
		Last Modified: Thu, 08 May 2025 17:51:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:241e2f60883a1d574642089f2a1f10abecc2dc6f4f7ce6c685e720f41183ea93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489d688275e29fce246a1006ab76a55325f08e1f2b6e60f7ea14b839c9644bd7`

```dockerfile
```

-	Layers:
	-	`sha256:6bc3c3686eeb3afd7fe2f87432d37696cdb7d04fabf1a0bfa8a9ea071d4fed6c`  
		Last Modified: Mon, 28 Apr 2025 21:41:52 GMT  
		Size: 3.6 MB (3620568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c74de3bbf5e8395fba8b710da93d1e207392343478ac4b60d120acb5b88fa8`  
		Last Modified: Mon, 28 Apr 2025 21:41:52 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9867b669e3648a88ea4dbe84379e4c10027edff96b91b9ed236ee95457674658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46027021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc9e68a2d9d860c859a9763de9f474df7a31f5a004be2b30bcd15daf629243c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:92d509ed822678d9588999f6e2d95bb0637ce3bc59491955f14a63873e677bc8`  
		Last Modified: Mon, 28 Apr 2025 21:09:01 GMT  
		Size: 46.0 MB (46026799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e53257b5f7536c8eb1739ff0e5f6c28225411f10ad357b156d1e30f1e385954`  
		Last Modified: Mon, 28 Apr 2025 21:42:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4a04ef187b547ace0e77e2c20f29c4d79cea055e30a99baebdfb3088a0d28202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dfa2b1afbc06d43a410c83b842c098430ae7c79889e7541529ffe41cbe4f14`

```dockerfile
```

-	Layers:
	-	`sha256:8a622e235071a8b1668fb51f5f32a1f7580581ccb46c405add1d748b5bd2a338`  
		Last Modified: Mon, 28 Apr 2025 21:42:11 GMT  
		Size: 3.6 MB (3620769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfd85ce6b836e8e24e1ed38507b75e4b791622f3c15182d57fff1e0c88ce454c`  
		Last Modified: Mon, 28 Apr 2025 21:42:10 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0af6542802cf9d1785a89b812fc2881e5bf6260179cd60435c1a3b41a9b20336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44197297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432ed9a4f391c1e56b04a9af1eda22cd25afd31d26b857352635eedc35c7f5d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b2981e37e4c65722a660bca9163e0a4ec7b5f1d01f62fff33f5abdcf6bf161b3`  
		Last Modified: Mon, 28 Apr 2025 21:17:54 GMT  
		Size: 44.2 MB (44197077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2aff421936fff3c6df0a6b7f4b8c227c5c7ebb6e5b9a106a9bb15d168af27`  
		Last Modified: Mon, 28 Apr 2025 21:44:04 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d07a7ac557cc268e55e3c09b05f080276783c33485f3cea23ade1c71ab9d2aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21bfd4722ff448a20e4e6e999e5bbae98449455c8bb8dcdec661df344bb0d4a`

```dockerfile
```

-	Layers:
	-	`sha256:d338581017c1491da42de00d02f7c2d3e85353a56227bd181dae4e1b60c44041`  
		Last Modified: Mon, 28 Apr 2025 21:44:04 GMT  
		Size: 3.6 MB (3622747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7615020cee2eb50ac661de206dfb6ae3f7f19068bf38495f21c70f51579667b9`  
		Last Modified: Mon, 28 Apr 2025 21:44:04 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:51b0da72340be694b2d27ac48812feb37b909caf9a218f9618ba27fcac0bd91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48327869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cad8ee6159ddad5e79dfa42b83d938fd5839fa3e4fe70a08c75aeaa8b7ea53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4e7f2f8f5c4b6053ae2b47d14774a1bc36f052f245a327fe8abc0d0334fe7bb9`  
		Last Modified: Thu, 08 May 2025 17:15:27 GMT  
		Size: 48.3 MB (48327646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a29b0f4d4ab890f9e501a1754df52c87a73e522f7448007e868ed15f868ebca`  
		Last Modified: Thu, 08 May 2025 18:56:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:901f8adc483b589125a8d7c159140cc393e13e6278dc4214285ae672abc39359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf7f5bb35a9584c69e2a47936bff02f53f81bd7d195f08430799e6108c7a1a3`

```dockerfile
```

-	Layers:
	-	`sha256:a15a73b9b493ef66306982f62b6ec4d40c1d325e66080ae41642de187b9c8d5e`  
		Last Modified: Mon, 28 Apr 2025 21:42:37 GMT  
		Size: 3.6 MB (3620783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d5949d1c60d07b825df971970f41602070fbafa8e7ae5cd7501900f0e381e2`  
		Last Modified: Mon, 28 Apr 2025 21:42:37 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:0438ab151da95c31dd5f5b68763fbf1b6958793ec2b9a19e4d4888e790054b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15556b5bfbdb668ee6d6e053b43ca35ae5a7c407cccba9398f4837865f5c0571`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:553c999fbf9e647c6ae27b137c6ea4451c3911c99606030b429dfec7a7a76a4c`  
		Last Modified: Mon, 28 Apr 2025 21:08:28 GMT  
		Size: 49.5 MB (49478573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99bd0c4ca62d4d5ded37e59779505d25625ebd18a9c27989bbe237c7e532c06`  
		Last Modified: Mon, 28 Apr 2025 21:42:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3a2f0188c95e0f594810f94a0d65bd17c4712ffc6460a8b9ce4dce4a1feca2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad503d31e4685e8c180810f46592a1226078a0c55ef79b65c0b0e185b0b23908`

```dockerfile
```

-	Layers:
	-	`sha256:1823ab740ecca54bb355a25db80bbe7719ef5a7ce592bea8ea1610854c9330ed`  
		Last Modified: Mon, 28 Apr 2025 21:42:19 GMT  
		Size: 3.6 MB (3617729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8168cd3d5562bb81a005a50d2f8947175753080706c75bf38bd453b6ecae3708`  
		Last Modified: Mon, 28 Apr 2025 21:42:18 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:92373cfe94496e17916b158fc8eccabef52bfb240e673684f6993d8c61997aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48775662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cbdbe4f33cc69ef7749ebb6de4a1b89f71ebeab70721b4fb0c393a1c470d98`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5ec1a698d2ca822d27566657a787d0a204ab71d215fa7337df01c287ba6f1cd6`  
		Last Modified: Mon, 28 Apr 2025 21:12:20 GMT  
		Size: 48.8 MB (48775440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61370ba72320e1d8726b38817711fdf434172f3fe81a843d9acdf039493a76ce`  
		Last Modified: Mon, 28 Apr 2025 21:43:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b8f6729ff730f1de5d5ad7f5025ade4d0534cd58ede6439aa6eef73b0c7469a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dfb1ee6154067cef28cb10a9deb087b63974c704b7be7ba3b380f923179d5d`

```dockerfile
```

-	Layers:
	-	`sha256:f727eca421b245c841f9b8e3cc7c153b87b77ae9a1ebe33add4b8910b59c6778`  
		Last Modified: Mon, 28 Apr 2025 21:43:46 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ecd8cdf7ece242b275bbc5fd3f9afe3d116b2a8cf5069056082b941ea35feeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52332352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8713018b79bad69c1a74775d1fa5c69aaab6d60375e4ddf1d2bee00e6cfffad0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:255d57fa318c3a40056713f2b47bf60ffa35dcb72d7d71894b2c1bf1d12d3ba1`  
		Last Modified: Mon, 28 Apr 2025 21:23:31 GMT  
		Size: 52.3 MB (52332130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61370ba72320e1d8726b38817711fdf434172f3fe81a843d9acdf039493a76ce`  
		Last Modified: Mon, 28 Apr 2025 21:43:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b87126213877ce772d1916869ee9e126bf7aa9b68e9733a72fac7188aafd635e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912cdaf9e1b5c701ef36213d75686343b73b83292f66631cd9a8c3878083ef25`

```dockerfile
```

-	Layers:
	-	`sha256:9be8c735f0c69bb550908415f6a16a2207cb1c23b059cd698027be478a4125d5`  
		Last Modified: Mon, 28 Apr 2025 21:43:40 GMT  
		Size: 3.6 MB (3624828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280af4f4bf0bc42b5e88bb64dcecd505de075e4ba9d109aff95b22a21b461342`  
		Last Modified: Mon, 28 Apr 2025 21:43:39 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:8169a8395be43eee1aa3942ccab351038dfbda39352fddadb6a5885180dd32df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47151553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82236e69be750513f966b32997915083a0b3db94e4a7adc1cd909270e29d4fca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c8dde55758e9540cb3e26521e181522d73a945c40f1823837b115cfcd954a306`  
		Last Modified: Mon, 28 Apr 2025 21:09:34 GMT  
		Size: 47.2 MB (47151330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e0ead25422281f131116995572cd69c68a48a1c848b054159c62cf8b3ce7ce`  
		Last Modified: Mon, 28 Apr 2025 21:42:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:256015a8f0121eed39d0af492d7982dfb2013e143947e8a56e7af01d7cefda6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5866953580ab9c4b210479ea86c7d8f2fe3a9993803a345b5a0ec89355d073`

```dockerfile
```

-	Layers:
	-	`sha256:f4b4c92d733666f1e76ab5db357924aa00a20506a53996ee55cca06c74ec6ab9`  
		Last Modified: Mon, 28 Apr 2025 21:42:14 GMT  
		Size: 3.6 MB (3620298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5825f6e7bc91f863432d1621ab44894859143296bfd2bfecfaa42b5fc99efcb8`  
		Last Modified: Mon, 28 Apr 2025 21:42:14 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
