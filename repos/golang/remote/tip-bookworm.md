## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:73d5fae26866d88e2517b895c38ad4db87d345e42d6daa92c53909cfc68cea29
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:3637fbd0d27123a21acbfa880af3d21732b97b3b58e6291ad88e4f23017f68c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326709101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66686b037a90cecbd9b4c132ced0ccd76446d0fd6ecffa7b2f3e94769351126`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:17:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:19:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:19:42 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:19:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:19:42 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:19:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:19:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcda2b4d7993820b00c5488d173051e76d01ba6b85620617ba77001b0f9e2fa`  
		Last Modified: Wed, 22 Apr 2026 05:12:28 GMT  
		Size: 64.4 MB (64396988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f951608aaa3e89b5f45836e7bb4887d3ae875613678404729d591b3bc67d6a`  
		Last Modified: Tue, 28 Apr 2026 00:20:11 GMT  
		Size: 92.4 MB (92448655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779709856b286b334888c2db50fa75d06845c18a6db8049d9f565750e3ae705d`  
		Last Modified: Tue, 28 Apr 2026 00:19:47 GMT  
		Size: 97.3 MB (97332439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf4799187c39475cb284477f6f5ea2a85e6404a0be5b6439d0412fb986562a`  
		Last Modified: Tue, 28 Apr 2026 00:20:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:22ba89b9cc169343c336599b5a60e9e47f6cd4b331002fa08a2c111f173fb05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1c3a40fd28d5747aadd43fdd28b6516e05f24df1881ff0575b871715f1f641`

```dockerfile
```

-	Layers:
	-	`sha256:15e91196fafe3dbcabe387bd5c0fa2a46e8a9c867ec6b44bac1066438c58943e`  
		Last Modified: Tue, 28 Apr 2026 00:20:09 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc231b6db0555230989e2aa4777a0721237075748ad9454ace73b195a51eecc`  
		Last Modified: Tue, 28 Apr 2026 00:20:09 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:63bb3df47b0f5fae652141d00b0cf76a8da9de620586a139c1fe2f681ae2bdf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285285066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33cb350891efcb2089d09885bb99327176825b634e41b73f0d3876195d7bcb0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:17:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:20:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:20:32 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:20:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:20:32 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:20:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:20:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3960cd47ab70e092f1d1162d4a33a761e2cfa64e09c3ca3118416ced1e6f99de`  
		Last Modified: Wed, 22 Apr 2026 03:52:25 GMT  
		Size: 59.7 MB (59652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453d4ad68e80b9d3f2617dcc0e1675fbc0b0ec9c34a23cffef99f7a44e864b0`  
		Last Modified: Tue, 28 Apr 2026 00:21:00 GMT  
		Size: 66.3 MB (66305588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d73ddf188a2e2e6775fd1105089506e6b38ccd4ec9defa63926d5363c7b9227`  
		Last Modified: Tue, 28 Apr 2026 00:21:01 GMT  
		Size: 93.2 MB (93172464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece3c123880d3b95c58adc2f333dbd6cb243e4c5097d71d1b03cd491b9b2a750`  
		Last Modified: Tue, 28 Apr 2026 00:20:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6278887419dc24b21fa52a655035e18ce8dc309fcec7dc1c0b0fee233fcb08c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3396c1e0a8d0be38c6e2c9004beed9075546b8fd9e9d72a888fcf5063ae2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4a0791f1957b0f141104d426c285d2f814a803dea9f74a87b496f8bf61482101`  
		Last Modified: Tue, 28 Apr 2026 00:20:58 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9e37a554ac9879afcb74d42edfbb5bb8f252fd51a742637b3d32c367f0be4c`  
		Last Modified: Tue, 28 Apr 2026 00:20:57 GMT  
		Size: 28.5 KB (28497 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a8fb9bf329df54e70f2dc6f3ba22e1e8dbe70faa91670f7d5c6ae1c25e295ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (315023368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0196a06788dc4365f6eae783a9668a2d5e325604d2270165935e533f68d58715`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:17:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:19:29 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:19:29 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:19:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:19:29 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:19:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:19:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d218230120636d94b547ba9443df3185b0faa32902a274df3c09b4b7d75f289f`  
		Last Modified: Tue, 28 Apr 2026 00:19:57 GMT  
		Size: 86.5 MB (86521421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324bee5f74040b6510924c3347f3aeb86c3579f67dc47584d6081f70bceb6576`  
		Last Modified: Tue, 28 Apr 2026 00:19:44 GMT  
		Size: 92.0 MB (92039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9ba4b20e4d824d691413c2ee0ebde467016faeae17e55113ad3c58e5f4269e`  
		Last Modified: Tue, 28 Apr 2026 00:19:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:57de39d48af29f588f776e808b1b777e73ba7d730bddf8e51ed2f8f658383724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97019818369b64c7424e4eee15ea4db0dd2aef858271a8bd2bbc345d6077f75f`

```dockerfile
```

-	Layers:
	-	`sha256:7b6a26ec59181fe392a9cb1a98bbc0ef5348034d5b67f3a9edadbdc478913182`  
		Last Modified: Tue, 28 Apr 2026 00:19:56 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98a39b3a9f7a98b02f802c8c0216593ed21dfe439bdf1807c0e492d4c8ca333b`  
		Last Modified: Tue, 28 Apr 2026 00:19:55 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:d2228a5d49a1b75d93a31847c3bfedffffaebf1230a4f814f2afaf6232f1fd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325548008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3856188d04423d388286f008264efde2f6b93e32b97e718f7635f0f23b3ef2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:02:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:20:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:22:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:22:49 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:22:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:22:49 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:22:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:22:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d771f6f5a1356deff0c1540de8894e5249a2f8c97ba7961a41235129f48c60`  
		Last Modified: Wed, 22 Apr 2026 01:42:30 GMT  
		Size: 24.9 MB (24875723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd81f3dc271c0572c6da562bcce13d5c0a8f379729949fde98b0b1e57ca2e4c`  
		Last Modified: Wed, 22 Apr 2026 05:02:53 GMT  
		Size: 66.2 MB (66235084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9879efc874ed51b634054b663c3928e8e648e3a1b26fbda190c327c3584011c`  
		Last Modified: Tue, 28 Apr 2026 00:23:18 GMT  
		Size: 89.9 MB (89871502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d6a9c589b969b9eee8b2fb5a3d53dcb1feacb04a0d56a4902866f913a72511`  
		Last Modified: Tue, 28 Apr 2026 00:22:10 GMT  
		Size: 95.1 MB (95087823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1474c208a86616834fbbb95e88fec23b62af94ad6d4e84a8078437fc8111b6b`  
		Last Modified: Tue, 28 Apr 2026 00:23:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6867c730c7397f122e1959915c8e8f59e31ba2eb064c09adb98b4586fea3f4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab112a7ae7c8624829ce9099bdb5e069cad98f21fa0c54e05cf97666353d320e`

```dockerfile
```

-	Layers:
	-	`sha256:db18d716e962d4d354ad36e4c4288d137a058b64a4fff557dc71bd051c2d0619`  
		Last Modified: Tue, 28 Apr 2026 00:23:16 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17b53782e009aec1c0513226a87e6e39cabf629843eedc7a880382db7cec3ed`  
		Last Modified: Tue, 28 Apr 2026 00:23:15 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:89671d878a23ef0047e86baf11db21b670a9233a74843f3f28119ff5c2694747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296688008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349b87697c2cf65be5847efcd1da88db6a6963c91bd0cec05a9bb7424acdcbfb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 13:38:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 18:49:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 19:35:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:41:56 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:41:56 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:41:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:41:56 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:42:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:42:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d3be957b775aeb19be93537211a85a2a31f49a07f3bbc6044dcea43e1c8ad87b`  
		Last Modified: Wed, 22 Apr 2026 01:25:51 GMT  
		Size: 48.8 MB (48782445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689fafc394c7107b6f97558e80faf7c6aa5a2d625bf130259c59cbe1f85ed9fb`  
		Last Modified: Wed, 22 Apr 2026 13:39:30 GMT  
		Size: 23.6 MB (23615606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451e7b3cb9c9d1c48a12fd45433b4710af87bfecf6744a09df7916580c67c305`  
		Last Modified: Wed, 22 Apr 2026 18:50:27 GMT  
		Size: 63.3 MB (63309466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1d9d3dbe215b8bcf0455f627ea3048e9af9e774f3f36403e2e0c26f0767680`  
		Last Modified: Wed, 22 Apr 2026 19:37:24 GMT  
		Size: 70.1 MB (70051299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6cf4da74aaa87494c6f9ff21c0c2521dbb6fbf104dd0da2009b5220756199b`  
		Last Modified: Tue, 28 Apr 2026 00:44:07 GMT  
		Size: 90.9 MB (90929035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3192f94cef19949c7ef9f6953759b926493f420593e8143ff74695ec295dc35`  
		Last Modified: Tue, 28 Apr 2026 00:43:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8a8aca5818d9f937e48e35072161c8d2b09e09efae6b21a72087f32fa755ff15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82683cb8e4d703cc40ee34254224b8e38525dbc0960b2f0ede33324417bf10c`

```dockerfile
```

-	Layers:
	-	`sha256:bc2da948890f60b1b664530bb43040b8a2d7b13e05c6edd30e428f4800093f7b`  
		Last Modified: Tue, 28 Apr 2026 00:43:57 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:5bd0cd91c9b20bfac2bc2424ff3276584bbe2bd7c78abc924aa89f131de84081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332222499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be8ab6ec867e895ce50743c84dd438916a1054675e607d0f655b5f02694db4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:38:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:21:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:21:51 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:21:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:21:51 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:22:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:22:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c150273f4a5b502fcc97d9a922e79c7bc7d5035fb9eb1142f5adfbcea709a1`  
		Last Modified: Wed, 22 Apr 2026 03:39:23 GMT  
		Size: 25.7 MB (25679369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5543a629afcc86e06f307e20d98c8cdd9f2490908cdef00122fb2daf671594`  
		Last Modified: Wed, 22 Apr 2026 09:37:35 GMT  
		Size: 69.8 MB (69846406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900d09be1892512836e57077e4aaa77f32975bd70115886dfb4ea461e5b3abb3`  
		Last Modified: Tue, 28 Apr 2026 00:23:11 GMT  
		Size: 90.5 MB (90462296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e34165e157d14e975c070ad73c3dbd1767de1fa84e282e6505d64626df00ff3`  
		Last Modified: Tue, 28 Apr 2026 00:23:11 GMT  
		Size: 93.9 MB (93897536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfc9c8416ba6e98df977d0a067a2a965899906cc15d84306e4018a12f15e86`  
		Last Modified: Tue, 28 Apr 2026 00:23:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:38944c5fb455cac3e8ba850b18d49369dd75b645740c618820627057195ee7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de23f06bb2be3091fa9c56c6e6493c53753b5e8442d200de2d8f716787f338a9`

```dockerfile
```

-	Layers:
	-	`sha256:9576901cb49406451be80409254f3cf6f3388e27062b6ae14d9cd9610ee6edf0`  
		Last Modified: Tue, 28 Apr 2026 00:23:08 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea3706984046f429b991cbd3884eb33410b01f7591ee9655344c629bc25a5ea`  
		Last Modified: Tue, 28 Apr 2026 00:23:07 GMT  
		Size: 28.3 KB (28259 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:2b2148ecf5af8b85a4e43e6df4e8952539e4dc132f56bbf91614ac0716fd8787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299622078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ae13461ba49455ff97541ce8dc7c9c60ed2238952e482fee379d9c080ca675`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:20:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:39:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:35:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:35:54 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:35:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:35:54 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:40:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:40:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac385f32c2d6e9209dd9f8ada378863aba00921ac3815f399e84f802ea5ce36e`  
		Last Modified: Wed, 22 Apr 2026 02:32:03 GMT  
		Size: 24.0 MB (24036363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df5494ce4223646f47cc2e95923748571f15dc98fdcd0c46696a358fa2128f`  
		Last Modified: Wed, 22 Apr 2026 04:20:41 GMT  
		Size: 63.5 MB (63500148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ef49d1bd750bbc5150b9412c747688b7df9d5501041dbafc4353c0a3f10e5f`  
		Last Modified: Tue, 28 Apr 2026 00:46:32 GMT  
		Size: 69.1 MB (69055982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c795090f7b3ba987c0e4ca6fd1eb3c889fe964ab0c0eb932bae581f24e4f796`  
		Last Modified: Tue, 28 Apr 2026 00:37:36 GMT  
		Size: 95.9 MB (95881458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5820cecfa8fee7f4ce8cd40bea7a2639d6ed875510c03b16c22ea2339d30213`  
		Last Modified: Tue, 28 Apr 2026 00:46:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c22db1b0e48d6fbc2cc187558a6eae799dd71e1aa8eb8cc5b33b225774f160c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd80b28359b26590a4370fb57bf05bfb06d7e3df7d4bb22d919747c7ea0350`

```dockerfile
```

-	Layers:
	-	`sha256:637ed487c98b773fe6dc8457b3283801a0ab8dd04467f51e4639c192745e1a27`  
		Last Modified: Tue, 28 Apr 2026 00:46:26 GMT  
		Size: 10.3 MB (10329539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae833309b09fff65a13788e9c8994516c12e35a27885532dcd26185ae0db603f`  
		Last Modified: Tue, 28 Apr 2026 00:46:17 GMT  
		Size: 28.2 KB (28212 bytes)  
		MIME: application/vnd.in-toto+json
