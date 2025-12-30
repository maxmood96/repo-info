## `debian:rc-buggy`

```console
$ docker pull debian@sha256:96970db2914db19c11a4eae69e3f4301ea768f8d6ff3260295881aca560270ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:1e97db935d3b7600ee0d707ce9ed3b26a18a8a4de2fd7eb3422cdf3c3e93b16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48821344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8e87616f27aa11b022b29fa3c746ed369eba4e54f8274730b3b43aa5bfe9cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:15:17 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:36a4985327850927961426bc6fcb1fb8dc1f9b5e7f69f8061c7daf2f4aee58a7`  
		Last Modified: Mon, 29 Dec 2025 22:29:41 GMT  
		Size: 48.8 MB (48821118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973d22da9497c1f2badbb10b36cedf3d44fc80c99247c2625ed58c849a26fd53`  
		Last Modified: Mon, 29 Dec 2025 23:15:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:9ae732d9ff9b8a82edf3f9388e2742edd481076efc6112ba45b1d4b605bdebe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc45c23c28858f858c82a7393d7c4b309dc308522661cd050bcacf159c132c6`

```dockerfile
```

-	Layers:
	-	`sha256:5e89687daa23eb44b579eb5843944456648b601e1f0bc5b451977f8bb32bc33e`  
		Last Modified: Tue, 30 Dec 2025 04:26:21 GMT  
		Size: 3.1 MB (3142345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3113131cb3803ae38538836690996e497b84f6f957c9cad93be5856a15d303`  
		Last Modified: Tue, 30 Dec 2025 04:26:22 GMT  
		Size: 6.1 KB (6055 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:823c81b59e4abb5c7cecef30c8324314a832a78f87b6d20d233a50e6cda55f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45112722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd20b7912170179fd208aac1fc1a64e95d94035abbf88c9d48ac38d3b38b1cdc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:15:09 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:fa37dcda97874915e8cdcc90ad670632c868d75ea88f3d100f667fda60d8b657`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 45.1 MB (45112498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130abad43695fc19efb693702b8d5579b22a1cf0cc16800231a33e50d9060084`  
		Last Modified: Mon, 29 Dec 2025 23:15:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:1d3d060be875d4df96a65aeca0dcfe25cc6fb0a08ecb9061ccaa7113017273d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886e0eb4178dc19a5949e4464265a6877a05a9f6019fc1da8b6473a7a55056c1`

```dockerfile
```

-	Layers:
	-	`sha256:58015bc35e09839c153cb155fd47343edb7b417a1465d8e1a625b07a2c2e3c86`  
		Last Modified: Tue, 30 Dec 2025 04:26:35 GMT  
		Size: 3.1 MB (3143721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa19ebd14bffcbe173558e384fea120e803f91e59d5d28687aa1546ff4cea9b8`  
		Last Modified: Tue, 30 Dec 2025 04:26:36 GMT  
		Size: 6.1 KB (6120 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5d3c1e33a3d1261c51904901698e980f438bb23cd3a95e67b6cb779c7b89f48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48801255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a397ed4350ea8bea7adc0d42efeb5cb7cb63d35a3080e9e404d9789c0b307ce`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:15:17 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e81a19d37d9900498b0ca8a841e2e3fe3dfde06146f7d10d1e71e1df7a8ae8ab`  
		Last Modified: Mon, 29 Dec 2025 22:29:24 GMT  
		Size: 48.8 MB (48801029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cca365b8b28a768064172d06ca438ae109c629343b6ae8c3675e518251606d`  
		Last Modified: Mon, 29 Dec 2025 23:15:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:c8d83d880d6d9ac3c58d60b391d6dfef4a6d2d6c64c245effd7f9ea8933cde1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d64da27b08b03fdac4ffe6aca8ac6c01cfd513723ce8e028b879f98fc1156f9`

```dockerfile
```

-	Layers:
	-	`sha256:f6e270d1b15ab4eba20597b0ece5802553c037768ecbadbffb93e3bec0c4c618`  
		Last Modified: Tue, 30 Dec 2025 04:26:42 GMT  
		Size: 3.1 MB (3143198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c1f1d39e0515d7eb02df54fbe947fbcd26c30f1a13d91c50b3f4add9b88691`  
		Last Modified: Tue, 30 Dec 2025 04:26:42 GMT  
		Size: 6.1 KB (6135 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:54da1d4da8ed1247485d9ade30e407f38f925c55f16302977612f45279de9296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49939371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d2cddb1e5c152fabd2b41c1b2ef4ea708e57661d97b85c5e08b5ccedc49014`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:15:42 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:f17a69092f61f8d721afcb2893fe3fd9f89bff73ba6442fc317604ef6ed50dce`  
		Last Modified: Mon, 29 Dec 2025 22:26:26 GMT  
		Size: 49.9 MB (49939146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27094b1bb6aae9654c21392cf590dca457f56fcd0b500a859c2b69198afc2234`  
		Last Modified: Mon, 29 Dec 2025 23:15:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:ed584995a8463ffa9cd22a25f8963010d15504e37eb97fae8fc4fd031059cd78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aabadcfa03f3212df52255421cf3bb7d84fb9c1dfd5b0301819c2a4d2a56621`

```dockerfile
```

-	Layers:
	-	`sha256:2c3e5ee928993dd2c10c7530d445a61f7b652abfb940ed26e17a769c328d3068`  
		Last Modified: Tue, 30 Dec 2025 04:26:46 GMT  
		Size: 3.1 MB (3139544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cb0ade6549dc41129c77a390619128fb9402f35081e131945ec8c407670dc5`  
		Last Modified: Tue, 30 Dec 2025 04:26:49 GMT  
		Size: 6.0 KB (6034 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:94755e99c0589965dbec716cf7278d7ce26bea0b02d8148e59938e15cdde67b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53505141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3fe750eb47e947b23f81fe8f7507e91aba8b844ed57986a2e213c123778881`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 16:11:50 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:4751b9b2bc723252279cfc4495d1386aada5bcd65548da744f319db317b21560`  
		Last Modified: Tue, 30 Dec 2025 15:09:27 GMT  
		Size: 53.5 MB (53504917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b19b29b65bd8decbe324c037e0217f7331d15a4409b1305c242ec58ecf35b0`  
		Last Modified: Tue, 30 Dec 2025 16:12:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:d86e8da7840d54a1e90283a2ba6a563a227dec87aae7fc8b3b12d2e398edcde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedeb6623506e493b749ac0daa03b384772649900c91395b0006eccc832a8a8e`

```dockerfile
```

-	Layers:
	-	`sha256:45ae5ed3656168ea18bf73a0ce10335fbeebbbb37df146a04f3943ccc9af628d`  
		Last Modified: Tue, 30 Dec 2025 19:24:33 GMT  
		Size: 3.1 MB (3145854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33be92d588b9e56a38167bb2aa0bc369cb9f51d8ccbd77d3bb8b4d44454b5d3f`  
		Last Modified: Tue, 30 Dec 2025 19:24:34 GMT  
		Size: 6.1 KB (6087 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:fcd0c931bb9bf9caba1eb3e3e02a8f2464c71e61ee990b706bbab9cd68ceed0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46843066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adeac6d3c310a35bf64228acfaadef113903e16fde42a4f51d7dc789306b7ce`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 01:27:49 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:992d8af34d90a1736cf1953fc1b6a42478d3f56705880d255aceac14902fb105`  
		Last Modified: Tue, 30 Dec 2025 00:37:42 GMT  
		Size: 46.8 MB (46842840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1475d25ecfc58efc0331b6cadd66d46d6f56a20cc869adc44ef12f727b0bcef`  
		Last Modified: Tue, 30 Dec 2025 01:28:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:59e00498b3c365391837dae414d3e91f700fab997101cfab21ea9cf64afcf665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a61b05f394a16ea4ce285fb4d423fb30f59853d3789c3488d80f3b32d1616df`

```dockerfile
```

-	Layers:
	-	`sha256:757a5f808c129b46454d9fbbefff7751355d28998bc851585cdc3c4bdd14e028`  
		Last Modified: Tue, 30 Dec 2025 04:26:56 GMT  
		Size: 3.1 MB (3133849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726c69a7de665476fdd2b9a13a5a5a727cde4e0f567dfb6ec8aac4cf07124652`  
		Last Modified: Tue, 30 Dec 2025 04:26:57 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:644cdc3a8c69fa059e22b8c80469864518d22c80773f60a3358f52dbf7943452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2723aab488fac6a7416c80b657ea3f76abe2d0e02caff3cc5ef6cbf7935f7cf0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 04:13:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d1672feb37bf4d7307a6feb7cf62c56febe8495830b9f965806ad0a97fe6efac`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 48.4 MB (48375355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05f4ead931594e4def6e696b33e6d7adc7a8281d5da59c270322aefa2a46118`  
		Last Modified: Tue, 30 Dec 2025 04:13:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:a561453957a818c63c14cb171bb4eec9219f524ce7952d19ba833dde60b29424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27082c3bb9009c7262495b39a49e47897db84fc9335687a88c5f6e3b388103f`

```dockerfile
```

-	Layers:
	-	`sha256:22ecf2d51f57d04675a004fed17a72e2eda70b41880a5ab8b4b4f7b3fcbefd9e`  
		Last Modified: Tue, 30 Dec 2025 07:24:31 GMT  
		Size: 3.1 MB (3143794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07aa768c6dbcc4abc5f677101c30765eb53dcef903206850c0559117e01fb029`  
		Last Modified: Tue, 30 Dec 2025 07:24:32 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json
