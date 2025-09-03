## `golang:tip-20250831-trixie`

```console
$ docker pull golang@sha256:65cbe8274b831dd6e75023a0c8c9f6696ea90299afa791bda7bd17445a2a8e21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `golang:tip-20250831-trixie` - linux; amd64

```console
$ docker pull golang@sha256:56cc755a3afa8cd5a20894073044e71a257c6d966da017adfe5743d6af0394c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328178406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c7599e406495dbcc7ea62ff86d49eeacb8e939d76e441e3099d8123496857`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea45766c6449310ca2fc621a7e00bedb4b9b803a7fbfe2607efce6d2e07e435`  
		Last Modified: Tue, 12 Aug 2025 22:15:03 GMT  
		Size: 67.8 MB (67777316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b519d207fe34ed7b1f2622990bb05cdc9442bdfddc83cbaf1fea876734bd33d7`  
		Last Modified: Tue, 02 Sep 2025 17:25:59 GMT  
		Size: 102.1 MB (102055368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3dff0c88890d852f1b6000c60fab1e5090230eba3301a46159a26dd4149cf4`  
		Last Modified: Tue, 02 Sep 2025 17:26:01 GMT  
		Size: 83.5 MB (83454344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c2adf530c181d6ccc239f75b96844f9935ea71a73d5847ec5d663538dc0686`  
		Last Modified: Tue, 02 Sep 2025 17:25:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:bdcf28b3c9e4e0342da713ca7061d2e7bfb874becdb1d3a66e3a9578eb3f1d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10807322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851e47f25e4d2544b6653c23987158ed1068b67311231c99b55053a35cecac3`

```dockerfile
```

-	Layers:
	-	`sha256:8025ae36d23c40834dc04e8a61835fd684a50955f063a86249167fb3ded78b98`  
		Last Modified: Tue, 02 Sep 2025 20:23:36 GMT  
		Size: 10.8 MB (10778310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab0dfa055bb026ba5230d25cf85502ac98d80503f41750ef3b95267439f336d`  
		Last Modified: Tue, 02 Sep 2025 20:23:37 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:f2f374b17ead9383ab3ce63890fc04dc4b55bb24e9d5783518a43ef40f935c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285255706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff4a7e4bc2ea2d17662b48385b74b6d21e79a22a20d1abc63057231fc43a82c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72873bc1bfa1e9338237d9573d1640f6647f61a1636bbd71d8128d16503087`  
		Last Modified: Wed, 13 Aug 2025 00:16:54 GMT  
		Size: 23.6 MB (23613045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe0a58e6c2887b271354fa2e1067ff7e829f063163f76c4a3d4f1da179eb22e`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 62.7 MB (62718501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983e43eed239a19cf297a7ce2beb2041dbb4789440168f810815da1dfa6cf3c8`  
		Last Modified: Fri, 22 Aug 2025 17:33:19 GMT  
		Size: 72.7 MB (72699083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8183d7d02c47a9b085b3d0bc6d67309b7fa4b7ef97cac1694dc0b5ea8b6ce9c`  
		Last Modified: Tue, 02 Sep 2025 17:26:14 GMT  
		Size: 80.5 MB (80512289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb66d9008f9a76950a9ccfbe90f3fb0d7ce9b75d3b9cb197dd869f061e91f2d`  
		Last Modified: Tue, 02 Sep 2025 17:26:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:a75555e228e44692d26660332ea9d9bb4eafa5a4264c239e947f8e5797accbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25543966b2573c0003eef5816e3af86f01b1d8bda2f02498c3e13afeb5b94195`

```dockerfile
```

-	Layers:
	-	`sha256:653f6bf109d16c1282a6a3d1ba8a3847fcba0725396064e78600657eec50d1e2`  
		Last Modified: Tue, 02 Sep 2025 20:23:48 GMT  
		Size: 10.6 MB (10574199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:228a634f2b34bd080730abb77d58e06ea2d46bc92100ff46d11034a4fe679d68`  
		Last Modified: Tue, 02 Sep 2025 20:23:49 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:55433ebadc6fe79e2633310fb865180e49613d2810ff1746787c4b612241cb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319913644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475af52a5a7e74fbde0fce18578c9270d8b971ac8105833dda8c76b1c11d35c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1ac401574f911479ede74ac51bf6b97a3e9068a260cb14b2cb133e3cf3eb58`  
		Last Modified: Tue, 02 Sep 2025 17:24:12 GMT  
		Size: 98.2 MB (98200183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948ccd09d5c498d3bdd3015babafec64e8e01106fe6a739f268b131403fa7cbb`  
		Last Modified: Tue, 02 Sep 2025 17:24:20 GMT  
		Size: 79.5 MB (79463464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79007f8d2ad39915608c909cf5ee90fd0d4ac82557885aa4608653d9e1183acb`  
		Last Modified: Tue, 02 Sep 2025 17:24:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f7392159340312e13410d86debcfabf3daca5ec041d91f136bf89310433e887a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10927932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883ee0aee6a3e3cb47287a538e975223b4d4c1824b69a732d523a58013fed5a2`

```dockerfile
```

-	Layers:
	-	`sha256:2e6e32bb4c896aceae709e806acd7c877cc11f58f1c6af6384f4a2eb47831674`  
		Last Modified: Tue, 02 Sep 2025 20:23:58 GMT  
		Size: 10.9 MB (10898765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1733cada262a8f0f296af0024ca87bc7ee2b0315065cd6e3713508a42b50606`  
		Last Modified: Tue, 02 Sep 2025 20:23:59 GMT  
		Size: 29.2 KB (29167 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-trixie` - linux; 386

```console
$ docker pull golang@sha256:cca23b3270658a14c4e576f56237d6d8cd0354ee1c2993b4707c5585e6d8a363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (329992914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166a1377a77d9b24283cafdb6fdbfb96c2f4b6e022e9d16fcfc0f9e98466dd9e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d9f8c7ff550056ffe2cca57d7110ae0306e74220a891574e97ddc10ba49823d`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 50.8 MB (50794258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde29e7bc69fcf496b5e5df92d7d82da6ff9f4877784085c4dcba73f6ee6a1ea`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26772559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9904337df106e0852d247e06047929e66d5097f2d2c13861e2e31ecc63f4b`  
		Last Modified: Tue, 12 Aug 2025 22:15:57 GMT  
		Size: 69.8 MB (69794753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c067f6363895081ef7a3553f2bf88434306aea7190a66b83b0280bef482d73e`  
		Last Modified: Tue, 02 Sep 2025 17:27:13 GMT  
		Size: 100.5 MB (100498418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc969e7a30537f064821c7c82ed2000b4f696dfb82f12bececa0caf74f9469a`  
		Last Modified: Tue, 02 Sep 2025 17:27:09 GMT  
		Size: 82.1 MB (82132767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eaaa1be8a8e99519f2034291209e414e4ee9cce2b140acabc450fcf4017864`  
		Last Modified: Tue, 02 Sep 2025 17:26:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:eed18e96f213a7654e959012c4f656d6b1e853446887902aea2739519838f6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10778544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84463cee0f881659e2cd7ba08f99a19d4816254d8846305cb2a07ef37834c9eb`

```dockerfile
```

-	Layers:
	-	`sha256:b1bdeff40b0a354c3e54011cc8b24e75895b8b7e0a3a3f0ed7a50b2dbe27183b`  
		Last Modified: Tue, 02 Sep 2025 20:24:08 GMT  
		Size: 10.7 MB (10749576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f78b044ef2a62ed62a75439dbc33074ffb79939cbb3664d2b2dfc573b84192c4`  
		Last Modified: Tue, 02 Sep 2025 20:24:09 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:a42a3355309e30b71d4070c64566b55ab8f3f3168bea66c54d43a9171f857756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326692471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9201ecd9dc3728d9d2ccba9a213a06fc669af7888044b7005d869229631f1cc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf20d9e1e5f16d7552d637dd4a12484b22e52928311f81dd13c82b6838c2ae7`  
		Last Modified: Wed, 13 Aug 2025 21:23:59 GMT  
		Size: 73.0 MB (73018659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c109f1eaaa6062f2aff79b79857ba42623f33aab83075f001a97de36d13c1403`  
		Last Modified: Tue, 02 Sep 2025 17:28:09 GMT  
		Size: 92.8 MB (92761484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65adef97a585f4d6f34375efc6b453ef50bc737c051ef6eb9403cedd2e831eb9`  
		Last Modified: Tue, 02 Sep 2025 17:28:09 GMT  
		Size: 80.8 MB (80815917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4f938eb650cdd055cb3206ba4313b09ffb5169fa8d8b6747c466578679e443`  
		Last Modified: Tue, 02 Sep 2025 17:28:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ab0195f70887f29ab25541db60b3fafb5a10a0522b1b4a19ecc0d0180c94f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10803159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7944408ab746332f471ad7dcbc8fd3aa76f367893edd92e5863a2ba243bcfff4`

```dockerfile
```

-	Layers:
	-	`sha256:074ae22c7828d6602f748525bc18d7f49cc1d6dc71121bbccc3e5455e957cd7f`  
		Last Modified: Tue, 02 Sep 2025 20:24:18 GMT  
		Size: 10.8 MB (10774094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c893861013b6930c78e9c53151ca6c0cb394c8408e0f372da24a8178c0a8a19d`  
		Last Modified: Tue, 02 Sep 2025 20:24:19 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:4ea11b5fe699cb5fd148f11e6c687d59f1718368fef00df6bdb363cf6116d7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351806425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7169822cd522d76403008e9c1eee45e885ec9b15d4baf49b818ac2dd3e50d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e41821bc74a26f64d4f81be6785aac1d7f09df07149a206784ae23523e36a`  
		Last Modified: Thu, 14 Aug 2025 14:47:51 GMT  
		Size: 25.0 MB (24950584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0b64daccd6b787f78c1a1622c08097763f53e2dee005bedbf3141bbaa8af2`  
		Last Modified: Sun, 17 Aug 2025 07:49:06 GMT  
		Size: 66.7 MB (66658307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633618253f092f4a4acbf99fa7a220a8363959887159df8b8feac3518e23d810`  
		Last Modified: Mon, 25 Aug 2025 01:07:47 GMT  
		Size: 131.5 MB (131541938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293eb689539c18522b5644ece27c44567aa0a4ab5ae7b74edd76c1cea9f0f71c`  
		Last Modified: Wed, 03 Sep 2025 05:13:46 GMT  
		Size: 80.9 MB (80891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fe1353d17ab68f294e17de00736dfed8838e5854d8e23bf806821af406411f`  
		Last Modified: Wed, 03 Sep 2025 05:13:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b36ff1ba2a6d7df8aa3d56f7eca36de2c24cd1b70ec0fc3db1d1185a21657101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10876997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5f889010980c6ae5fabcc8a3385d51c8ab32f37e0c55c6de728b6b305f5012`

```dockerfile
```

-	Layers:
	-	`sha256:2cc2fec55a13d079dab8c719b219932eb20b81a13b2deacb9acd5fc8db7cc5ad`  
		Last Modified: Wed, 03 Sep 2025 08:23:44 GMT  
		Size: 10.8 MB (10847927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee85351ebf43c295c6a1baf8c55b6b40455f21e0923eef66bd04719dd14b69ea`  
		Last Modified: Wed, 03 Sep 2025 08:23:45 GMT  
		Size: 29.1 KB (29070 bytes)  
		MIME: application/vnd.in-toto+json
