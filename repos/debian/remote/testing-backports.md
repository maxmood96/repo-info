## `debian:testing-backports`

```console
$ docker pull debian@sha256:bffa7a8d29866513efcd3b98d63ba62f5933d5f169d92e5ec349875f08317502
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:94b6e0d26c44358048c8af911594253d022a01aa0e516bca663152001c6e56ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17744753e28db6eb9f6bf85f8acc320217ed68c708d28678f899b73f81a22694`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1779062400'
# Tue, 19 May 2026 22:58:26 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8848ceea1cb0274f75338eab275781012b794ca9263ff09f61506e7f592bd47c`  
		Last Modified: Tue, 19 May 2026 22:36:56 GMT  
		Size: 48.7 MB (48697209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5da04af465ed31a89de7c7ab4cfefa17a19a0f53195b624becca43dfae30aac`  
		Last Modified: Tue, 19 May 2026 22:58:32 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fb2af5ca8e0a2ab325fedde0445fdf4a28d60eff47e472229f44cb59f49c1989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd13f9b8561ffd73fe631a2972fa9765364682f84534ffd3d5674aed58a066c`

```dockerfile
```

-	Layers:
	-	`sha256:5d74c25bae0f23c41a6f8949760263e80cca35c49c465ba3abb31952d3dbff1d`  
		Last Modified: Tue, 19 May 2026 22:58:32 GMT  
		Size: 3.1 MB (3146246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:159d8773ac9b30007732ea2d3d8b62585b54f2a511209f87936be1575a5e3059`  
		Last Modified: Tue, 19 May 2026 22:58:32 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:91de9a9cf9ab7a44a7cebf86ac2241d80488ee87a30a540ff8947082dc2c66a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45603409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f046cfa919d2f606b1ce9843f3919083cc91b78f9f69fc62a7c60f5e1c2edf39`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1779062400'
# Tue, 19 May 2026 22:57:19 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:014f68b20aa968dbe35a42bac52e99fbe9c65adcc6b04d96d492e1940fd0987c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 45.6 MB (45603188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4faf840ed8278d0b67a1687151acb16105b750ce4b7952cb60eb981d95584e1`  
		Last Modified: Tue, 19 May 2026 22:57:25 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:73ec085cb71bee26cf057d0ea9c4cb853f667c54de2ac21083a129302c2e0dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868a70884f66b7306f7213cdd8672debcc47ec8965262b57434313460298b92a`

```dockerfile
```

-	Layers:
	-	`sha256:b53eebd07f931bb6dd6c6fb60461737692258eb3bbf0b204b5e02b916cad5dff`  
		Last Modified: Tue, 19 May 2026 22:57:25 GMT  
		Size: 3.1 MB (3147608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fb6fd386fc6321484977d7e119ecb430ca16e0da1144580745a9d8a96081991`  
		Last Modified: Tue, 19 May 2026 22:57:25 GMT  
		Size: 5.8 KB (5849 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6192717865f6e1468943d79c1073c7e5b430839ece31e2a79838d46987073cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48720256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dfe43b77c905ce42542d196c541506bfc2d3052243d1661526042fb1b1d66f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1779062400'
# Tue, 19 May 2026 22:55:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:58a56138a5196d2f12616e5144d893fa2645adf308a9ba2fded1afee18c2af1f`  
		Last Modified: Tue, 19 May 2026 22:36:57 GMT  
		Size: 48.7 MB (48720033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614a896de1ce4a07fb0beb97c4a3c32480c29fc507f2ccccb6219d024c7322db`  
		Last Modified: Tue, 19 May 2026 22:55:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:358f36c290bbb233c1d70529eae4784c927f4ec130941a05d833333569cc2451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7e70d1abbb223fb0ce9e2a083671cf12a4511fd513c8cc1930fc77ca665835`

```dockerfile
```

-	Layers:
	-	`sha256:bed0cd05f50fb5c8b28ba7b0cfbb81c69c66c0f38667bc811f7c50a73e7e9d43`  
		Last Modified: Tue, 19 May 2026 22:55:58 GMT  
		Size: 3.2 MB (3150916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07cf756b2c78240b4328803b36ce1d05889fb4ae8861c527baac75fa2c5d94ef`  
		Last Modified: Tue, 19 May 2026 22:55:57 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:3309a5843cb0871dc379d0f7fefc6c3581f806caafe611a8630cd82053d426e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5339b757f401f56038213471a2732b887d9b6b3e316b5da83d7a9f217a917d8b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1779062400'
# Tue, 19 May 2026 22:57:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bcae8321b98d973381a954483f7030da000db4d4da9085f33ebe73a77d4c869b`  
		Last Modified: Tue, 19 May 2026 22:37:15 GMT  
		Size: 50.0 MB (50001947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701c6ba3bc508c0a078c76ef8fa09a545ddd8dd4145fefd6454267d5b935c9af`  
		Last Modified: Tue, 19 May 2026 22:57:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0d701b6d5998185e78c9de0c0b03c6c3c04d507447c6ca0a268dc4d0c4371568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efecf68f5af9344dc15e358884788b4c4a10b057803492759e42d7f8744b285a`

```dockerfile
```

-	Layers:
	-	`sha256:1e956a85dff88e267f438dd834a9a9df4fafb0abf9cac846c21b8921713e3680`  
		Last Modified: Tue, 19 May 2026 22:57:58 GMT  
		Size: 3.1 MB (3143443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656fea181ecd7079d818b77deb3be3d0ed8aa256c13a79a3521a9002bc7b8c1e`  
		Last Modified: Tue, 19 May 2026 22:57:57 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3fde66df63546a91aa4d5cb648603c74aa675dc31be34d4084187a2bf1932112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54021507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f1d92d8a9979c09874901f7f95b12f2e557d3cf34c6e9e7bd197cc8ded2e43`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1779062400'
# Tue, 19 May 2026 22:56:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a896bf8623032a9b4075e6319b6f84fd18fb93674032660f124004714d68a5b6`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 54.0 MB (54021284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b278cbc22a5f8684efa93c350e845bf08327018f8b49f6229f125feb53650e`  
		Last Modified: Tue, 19 May 2026 22:56:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:76708087c34a3308018c73d4c54b246d2d0d73c6101590eb2978f75b6ecacad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aca9df18bc19a6eb62ca640926047e3e1452605fae4a46be197360241e550ac`

```dockerfile
```

-	Layers:
	-	`sha256:6220a69e5301243265b563005ea4c144e7836fec417f085085a04b19f37ad5fc`  
		Last Modified: Tue, 19 May 2026 22:56:51 GMT  
		Size: 3.1 MB (3149757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9cc8a70d449878780459b973584c4ad4139ee3aa172e080adcb6fb6763c5134`  
		Last Modified: Tue, 19 May 2026 22:56:50 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:10b163ee4dc3445dbaf1f897ed6be4118d041d68084e2523c610cc601e4a03ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46833413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fb27768cdf51ac6e555788e318a150a5915421b66773b4ac3842bf41a547b3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1779062400'
# Wed, 20 May 2026 01:47:56 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:612adadf0063fc0d0780b5c5f6efeac492aac518a4614c14f4ea5ff21a649186`  
		Last Modified: Tue, 19 May 2026 23:46:24 GMT  
		Size: 46.8 MB (46833190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea72aa88b01894b72ff8f06103c02b7afdd03799ddd7758cb0216504afb02d8c`  
		Last Modified: Wed, 20 May 2026 01:48:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4c687d2baac3dfe208550edb6f8cf827405042940af6a5b43055b1be684c5789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9980a7039deaf8aae3c56f8a9c164c6b5644ad7f065a60a7a5df16d43c34f6`

```dockerfile
```

-	Layers:
	-	`sha256:c78026ed543f9b62b01e99abe7bd59028bf8c6091faa155e445f36edecd0c4da`  
		Last Modified: Wed, 20 May 2026 01:48:51 GMT  
		Size: 3.1 MB (3137760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11bb1c911d37e0f34cd7cfa176e1b7f8ec2b450bce124e2a95c375d974a7c949`  
		Last Modified: Wed, 20 May 2026 01:48:49 GMT  
		Size: 5.8 KB (5819 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:981d1819a41ad33396e110fc6b261e546f749a485538a7d4c8c348db4b65149c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48440752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee1d0a40e78d0796d4216e1f61346a5c56df54d0992f81e7ab16d580032eb7d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1779062400'
# Tue, 19 May 2026 22:56:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0c3a4ef462181c965f3e9bcb96017afe28ad32a832bcfe94c1e0abaccfa05df0`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 48.4 MB (48440529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9a6575683b242ea3318e14d7eeadf3da606c73045ddf0e0240e2190cce434`  
		Last Modified: Tue, 19 May 2026 22:56:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:35933e94c0a9eea5de6c4013c517ea7db1faea80e8929db9b9e1b60d52ab2e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58caf092036a49721908f6fa9bceba4f74a4be02d4264cb8c3b4fd977ab93683`

```dockerfile
```

-	Layers:
	-	`sha256:3777bbe5523b111e52de132afc11972f7ccf3f385194c6fce91ddabdd5fe6e3e`  
		Last Modified: Tue, 19 May 2026 22:56:49 GMT  
		Size: 3.1 MB (3147697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:621ffb9903ef28e0b16c5374bfdcbc54efa4679f78a0f4275811de29ea77e67b`  
		Last Modified: Tue, 19 May 2026 22:56:49 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json
