## `buildpack-deps:plucky-curl`

```console
$ docker pull buildpack-deps@sha256:c47166826c40f5cd35fe81fa376189173a493fa28f7e936637df9ceee8f205e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:plucky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3318ec464e8d40b7abb8f33c56401a9ca5986fa084c7c8a308520c590e495c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49870960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652d55aa42522ed5c61b5416e882295820b7d8fc8e0c078c0f5b0c8c42d8564a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:d17f4a4666630f8b9d15b4dc3923b653110adbab5c7c5d0bd03975e1894a7a36 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a54a536f5c04d9395dbeed64c1972fe7c7df89f5374561b8718bebbfe644fd94`  
		Last Modified: Wed, 10 Sep 2025 15:57:46 GMT  
		Size: 29.7 MB (29715598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b97812ff0ce0ff49ad436d22bb765dc0c078ca9b006fea6b1c05ccb51df32b`  
		Last Modified: Mon, 15 Sep 2025 22:12:34 GMT  
		Size: 20.2 MB (20155362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c7bb7f17be42b11298d22cfa72aa005a060c25941d0a5a1ce61040a3c85e97f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65732bda6ab11e657bf8139facb931e91fbfe0bdaac3277aa29405d0a5b36eb`

```dockerfile
```

-	Layers:
	-	`sha256:e2074127d48739fa1cd67c0dae34556786a65f2e49648169ab888242587b99fb`  
		Last Modified: Tue, 16 Sep 2025 01:20:21 GMT  
		Size: 2.6 MB (2613462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04efc97f390f1a62e1ffc78a4a03bef0cb89afe216ce01fcba2c4be289c86b32`  
		Last Modified: Tue, 16 Sep 2025 01:20:22 GMT  
		Size: 7.0 KB (6968 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5003fd83f175bcb401528aa86e732b2df4824b0ec3b296fda6fb5a06d78ec7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44712856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11484d2adb62645dc1be56a3ebf1b3249b9dd2a59e65a4e616e4ac20e36c6e5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:10114ef0b2a9754f23d7fb435ea61b94bb321445f7265266c66bf4ff069986da in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cbb4155e6c1b850eb4480b08de2a9e6acb90dd08837756bc1647f535d025f8b4`  
		Last Modified: Mon, 15 Sep 2025 21:09:59 GMT  
		Size: 26.8 MB (26843807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec71301aecd896f276835da86ce14239083f765a1e273818df6ebc7eead691a5`  
		Last Modified: Mon, 15 Sep 2025 22:09:57 GMT  
		Size: 17.9 MB (17869049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f601982ccb66c8a0689c9a96fa16a7bb5d8b94901c2d1e67193cf2bd20d5efb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a286618c9bcb6869a46ab056e9d52dd443be2c6e491f8303719bf17aee52c080`

```dockerfile
```

-	Layers:
	-	`sha256:057c94669f8b1d55cbdf87935ff5b3296c918974f9e3e4888d5e1e791642605e`  
		Last Modified: Tue, 16 Sep 2025 01:20:26 GMT  
		Size: 2.6 MB (2614961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ae8caa787798fcec3454a9531b8d5c3e97688780698499966ae0f9df7ae2c8`  
		Last Modified: Tue, 16 Sep 2025 01:20:27 GMT  
		Size: 7.0 KB (7032 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:872d11fc7df89246081506bd2c5451f5ce8d586f66283b6f6abab73a8906f9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47463358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0596608a9141cbd95af39ba1768d571d5ba391ae9d3c5891b2855ad299dd9e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:1d0db44377aa33c495de438dd435408b4391cf11e887ef1a542a8ab49275c67c in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:47429ff9cdd3006afbf0a7a02f144b5a7444e546614a97a12fd567f7a4e3afdb`  
		Last Modified: Wed, 10 Sep 2025 15:57:53 GMT  
		Size: 28.3 MB (28305856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10315f775138ab7163eef3727c6dab9223b7bcb7a298fa6c0bfbded2ea9618ac`  
		Last Modified: Mon, 15 Sep 2025 22:11:59 GMT  
		Size: 19.2 MB (19157502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:604372d2fdaf11dd482f5856b433e79497da4f4d01b1c15c2ad80cdb6013ac85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d004f2a265f49bcfb1a5fc10e63150be85d1875da81e60f4afecbd2327a886`

```dockerfile
```

-	Layers:
	-	`sha256:da8e287ca4a4d092c1aaeae1501953e45943e6ba05aff233abc6409ca46dac95`  
		Last Modified: Tue, 16 Sep 2025 01:20:31 GMT  
		Size: 2.6 MB (2613719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:565ac9aae1302bd93c4d07981ab59c5e041eb107518d3afe3670dcb278a1876e`  
		Last Modified: Tue, 16 Sep 2025 01:20:32 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cd65a01178f8fb9a52aa27f72ce8e4f17f4e81d3fbd23cfc59a533e82bf79c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54519831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d358cc34c35a24a0b9772432a5a4c38d1b0d694523a0e5ddc05aac82f6b5ed1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:6adb4e685c451ab40584158f7419d79aa01d082f4041be632719c7ff546fb9da in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36e9bdbf4fe8f4e0dfc5762cb75e78afcabb8dadbee69af0ee1588b7b3f428a6`  
		Last Modified: Mon, 15 Sep 2025 21:11:04 GMT  
		Size: 32.9 MB (32935846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561cfb699599e82ba24851faa10142412d9beeccaed1347775ba14e86e5da75`  
		Last Modified: Mon, 15 Sep 2025 22:12:34 GMT  
		Size: 21.6 MB (21583985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44f242e4d7e8f3308dbfc61681b22b037f675180173b4f1e349b6e91f2e8eb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb11338ee08346f526fbcb7cfab8e3e752a17b61994a8d25c781d7005764749f`

```dockerfile
```

-	Layers:
	-	`sha256:5953a41dd0003f4c9c39fd68a3478fb0ac5f2b715d44e35de0aba3287fe87670`  
		Last Modified: Tue, 16 Sep 2025 01:20:38 GMT  
		Size: 2.6 MB (2617280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99cd97db40eccfa970aec3f6b95002d65a32f6a4ab2e4d5c8264983c9ab01ec5`  
		Last Modified: Tue, 16 Sep 2025 01:20:40 GMT  
		Size: 7.0 KB (6999 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:27aa7bbf0abab9c137d61377342876c7c3ef73425ae79d7eb668f3769ce13ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49628221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4b68cac59716b051dc48b83488148e090bd06764b620a009529af11d9d79a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:6deeb8ad1cf6cbcbaeadf271398b84360ae1aa44c52589c5a25061070904d259 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4dbb31f8610f9a26c0e0287f94383b3fdd5b82ca5cff6fb36074b179a1a762ea`  
		Last Modified: Mon, 18 Aug 2025 06:51:45 GMT  
		Size: 29.7 MB (29736585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e174fc97d5309e505875653aa9c1975ab84d1b6475850d214ebef84c966dbb8`  
		Last Modified: Mon, 18 Aug 2025 20:07:27 GMT  
		Size: 19.9 MB (19891636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f3efbe51e4602c84aafba68a9041ee0f87d6c0bd0339d02b32d50f162ee41091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f53e84dc134ae2e51fc5876b9938e9eb6479ca6d20c7a79423736c3ec313c5a`

```dockerfile
```

-	Layers:
	-	`sha256:53d9dce9caebccc2a22cec69c74c09efc90618d27ccb1ccc3877ba04eee88a12`  
		Last Modified: Mon, 18 Aug 2025 22:19:39 GMT  
		Size: 2.6 MB (2606574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56b2c60a4a724c2eb70a4234969e8a0c9c9686aaa55f268be938d141451dce81`  
		Last Modified: Mon, 18 Aug 2025 22:19:40 GMT  
		Size: 7.0 KB (7000 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b0fe7aaf64285e8c9d7bf7ab98022d08cfab7aad7112625eec91e16608a13cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50128859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c782695b796ab893542a423a18f44444b9a573b154fceea8ed9eaacad2930b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:887fec0e4d0c972b51a6e86694b1427520a0727885d5bd45dd6f7fd2f5a2b01b in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2fdf3f6e779d3806c424aaa684f699e2b62eaee0ea412f005aab588e71ac9821`  
		Last Modified: Mon, 15 Sep 2025 21:11:50 GMT  
		Size: 28.6 MB (28571164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098110e94bf3ff0cd14b4fd788bb31d467af1ad77ac445ca3a1511fa1e309d44`  
		Last Modified: Mon, 15 Sep 2025 22:13:39 GMT  
		Size: 21.6 MB (21557695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ebe9d2baf4007fa74765c1503221b2e6653f8191621bca269a06c78c94339a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8291a4e55324f0555bf1bffe393f6567e531312375c8cf0cf8a970d8f89fdc17`

```dockerfile
```

-	Layers:
	-	`sha256:3fd82ec306c423b3546f7873500816e757dcbfe83bb032a8ef9f84a1c937f1bd`  
		Last Modified: Tue, 16 Sep 2025 01:21:30 GMT  
		Size: 2.6 MB (2615490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb36f137c39dd83dfcab627c0ffb8458828842b03e8863c675b30fd5bd6cd218`  
		Last Modified: Tue, 16 Sep 2025 01:21:31 GMT  
		Size: 7.0 KB (6968 bytes)  
		MIME: application/vnd.in-toto+json
