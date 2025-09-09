## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:ab047bfee584456d523d11d5cd0574353166590f6f0e64ccd18db4d3938c0dc5
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:2862622a8a8ef53b03ff819e68bcbefea3bacc1dc50b74850751859d062d33dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0a97e700a0fe139083c238dfe1e8d7d2ec108047bde1dbb5af4732db2d4ff9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e08df0e087c0e4a0faa21567c36510c90cf39bfe10f81d7b92092d2c98ab80`  
		Last Modified: Mon, 08 Sep 2025 22:15:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e4f52d4fbf35f2953bd443407e4d0dd26519968866f69bda668137e6c7748823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5225490970e034abf2a83f28a4c0a91a4422ff69af52d5e59a9171b9c55438d8`

```dockerfile
```

-	Layers:
	-	`sha256:755ea5af6aa33a9e1590de706d4aa3a3d2d827fc6d181a936ad697b3c63e8bda`  
		Last Modified: Tue, 09 Sep 2025 00:24:02 GMT  
		Size: 3.7 MB (3733431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b0d5922fd85b29a66531f89b60603db7f00ac485ff68f056dd53c83d40ab511`  
		Last Modified: Tue, 09 Sep 2025 00:24:04 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:54d162a6f90edfbc51d60b740aaa182228bde999e4286d4862e493adc523373a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46015913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa57ea06a0c0c1ed77b148f406bfb4bbdf93c42cd4915b44a533e9a87547b5db`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cb78550743da54c438514c9643e672e9378df901e1cdbedec41078f3c369313d`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 46.0 MB (46015690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db95218596dbcdfd8eb9ac506b105d12a5eb885c15434dc03a2644697fe3b25c`  
		Last Modified: Mon, 08 Sep 2025 21:27:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:90241c7be599798c8ce042133c18270c6b79b9e0530549150d003a72a109fc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da19ed28e672cc4efd21554482dfe1274a64cb090b33e8e1bb778df0be640350`

```dockerfile
```

-	Layers:
	-	`sha256:063790dfeb90825e689b9d25d2e0f831b069bca6860306b703539a78d29eb78e`  
		Last Modified: Tue, 09 Sep 2025 00:24:09 GMT  
		Size: 3.7 MB (3733632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4fe34da9a407c6d8c4e93cfe313f2eb8a94355f0b398018ee0d218a1c05fc52`  
		Last Modified: Tue, 09 Sep 2025 00:24:11 GMT  
		Size: 5.9 KB (5903 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b1dbf76cd52a91926ce5414ff842dc11409b4ff32aabf0010ef84852700528f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc6c931f83bd13abca48c123eeb1d8733bf0e148d189fe8d5b468b7bb108820`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483f3b951c4080457729741521a2fed62f0b0cf5d105c2b3649d1f53d2f3ed82`  
		Last Modified: Mon, 08 Sep 2025 21:52:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:079c6b6ac3aea3735a73c635cbff8cdcad9b0c91e513afa016cd906236ee4ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b6294d7406eac0138eae99cb6b767f4a46d27f4273ce2dcd91f8324db6484d`

```dockerfile
```

-	Layers:
	-	`sha256:a6edb54f8760cc2d07041625fae99fe143157bb4d60e6982fa7d3f4282b7dce1`  
		Last Modified: Mon, 08 Sep 2025 22:04:29 GMT  
		Size: 3.7 MB (3735610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1789f38e99ecc29062d34f467ef6876cadd5f804879d220e336fb94979a04923`  
		Last Modified: Mon, 08 Sep 2025 22:04:28 GMT  
		Size: 5.9 KB (5903 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1d3aa318646884e44d2a0ca3bbd1f8c45c52ece1c81478f0ed826d5e65c5a644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2ab66a3b78f1303d1b520661b39cdfed4048bd3209a376bc46d23b35b851c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483f3b951c4080457729741521a2fed62f0b0cf5d105c2b3649d1f53d2f3ed82`  
		Last Modified: Mon, 08 Sep 2025 21:52:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2a6e5b64621b4c4a4637482533d1369a0f820ffe5d2f4a5850cfcc67a82ce1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1db8160a39f47c0f98d06514fad14af0a9a8a522dca39d010fca5573b8a77a`

```dockerfile
```

-	Layers:
	-	`sha256:26dfc4404e1201d90525b1451a217bd09d765f021b2857c2a7ebcb9e2d1c1515`  
		Last Modified: Mon, 08 Sep 2025 22:07:45 GMT  
		Size: 3.7 MB (3733646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc2b3751369d51f582fba69d60ebf6988e06ce50a08e491fc9873044cc878779`  
		Last Modified: Mon, 08 Sep 2025 22:07:44 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:f8c51e27f0b39081774ade2c9edd0ef023aa76bc20351b00cad00d1e669c3145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49466908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19097edb82d9da555752b0b7dd593687277186312fce0ffa9dd46b6ef3728969`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207d4db881269eeccb2f9ec4a49034856fcfd293bde12474bc213a92f5ccf7f9`  
		Last Modified: Mon, 08 Sep 2025 22:04:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e78a20498e9b1422d7ba4f7be523bbd59bfb423e3c7f16f9d6f80f5f11c2c544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70efac8cc1e151835137f03f8c433109c4621dd80ae824477e051990d224efc`

```dockerfile
```

-	Layers:
	-	`sha256:425539f54576014a101a38d219b4ee53d7e9697617b619cbc5029f332d4ba12e`  
		Last Modified: Tue, 09 Sep 2025 00:24:23 GMT  
		Size: 3.7 MB (3730628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1249d871facb6a079c654ad07c6d32106837c00ebc9342f106b355a1ad37373`  
		Last Modified: Tue, 09 Sep 2025 00:24:24 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:5f7a9644b5e9d9ff992c66617fb69f2d2cd9934dd0c3e2394f607f474df0205c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b8f33a819a24c8feb9ab3bcdf8caa17254d4e3829a340c186206b07164a0ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:32b0a76df497911c1adc85f7748d78b916d66733f6d0c87cdc6e9eb06317a625`  
		Last Modified: Mon, 08 Sep 2025 21:14:25 GMT  
		Size: 48.8 MB (48760780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181afd3ca5e16571ee5bc18c1ca6661ef640b73b9d5e70a0429578de82a78821`  
		Last Modified: Mon, 08 Sep 2025 21:31:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:75a9a9d08bd478f9a8c0e143f794ed1cb42815408e965a577975f2707a600eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451d4c069120d2b250738420e45b4bebfab2f6a014efd51fd15b34d9ff73bb7d`

```dockerfile
```

-	Layers:
	-	`sha256:bd0391977a19fd83025bc956f5ae6cc93f7c03a396acb0b42bcf8edf55190a11`  
		Last Modified: Tue, 09 Sep 2025 00:24:28 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6519141dbba285e4db7b2cec3d67e0d36caabc6b576c5f7f0ec49bc201238645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1268bb0f90142e0acc8f2b695a35484055967f12e661285b5335e8d9641f18ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972280b1dadb7780fa999dce2a036dde31eb85ab7bee189c49510430c9007bcf`  
		Last Modified: Mon, 08 Sep 2025 21:22:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9114e4721581e9aa4bc647c013fcec99cbd31fe5a97a7bcc7fd121ac4304586d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcc2ca5d2fbbcb326860c4e051cba3f22da6b9ee7bd70b1e6c44c8d2c390c3a`

```dockerfile
```

-	Layers:
	-	`sha256:3c7140f32917d71356b408f4d5c4675d3786fb20a3358ccad259788f97b15bce`  
		Last Modified: Tue, 09 Sep 2025 00:24:32 GMT  
		Size: 3.7 MB (3737787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb878b3664f1b7337d04cf2783bf46e53f6d91d9e708619ed7217a86d8c499d`  
		Last Modified: Tue, 09 Sep 2025 00:24:33 GMT  
		Size: 5.9 KB (5873 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:2ecc6fb302b46f34cb37b8c78ebf7cf2fe2ebd5b3a03236b5adc20991f7a07e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d843c54dc032ad1ddd8fa6eec1d2567156d7307ac0c46612a6b888ceeb0b170`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e1de11bdd6b224ada5f6ebc5b10f5f540a097d4df13fc8b53ba375e7ae7a73`  
		Last Modified: Mon, 08 Sep 2025 21:24:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9033687b08d2ab863f841800071447579e3b11d46c1db2d57fc4ab944a7eafdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46042f5c0ccf01a85ff1f0592fc56dcfe1a607ae41fbc8ceda6154fcc22c9366`

```dockerfile
```

-	Layers:
	-	`sha256:904bcd686f6d4ebb61c898ccb91deafcdf6f27d0dbefd289f265f5282315a42a`  
		Last Modified: Tue, 09 Sep 2025 00:24:38 GMT  
		Size: 3.7 MB (3730269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2ecc8f9c6cc11e51aa3dc827523dad171c4568f135a0ad7aead4951a66134bc`  
		Last Modified: Tue, 09 Sep 2025 00:24:38 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
