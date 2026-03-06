## `golang:tip-20260301-bookworm`

```console
$ docker pull golang@sha256:e3c788aed0cd341b8c86218c1785a0217ea4a31fd627dbbfe861d33e7569d4a4
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

### `golang:tip-20260301-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:9a1cbc7783afc945188851d243047d58dd7e188012eb754ec8cce52576d3a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.0 MB (322971379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4864d9dd961e375143a771856a91a2ed66147875d4f2a041eccdf6f4a9e28708`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:03:11 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:03:11 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:03:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:03:11 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:03:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:03:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b169dbbe10f5723eeb05522ccf1276a8e0d996c21b31e6251ca7f076ef70ad53`  
		Last Modified: Fri, 06 Mar 2026 02:03:40 GMT  
		Size: 92.4 MB (92444796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689a8c664b692c42c224e696026ec9ec2afa2556b09a298fb5881d3823f0c6dd`  
		Last Modified: Mon, 02 Mar 2026 22:02:43 GMT  
		Size: 93.6 MB (93603346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bda48e9e541cb4aadf451091ff39e8e2ab890eafc175d19e06694b7a2b93ff`  
		Last Modified: Fri, 06 Mar 2026 02:03:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:650be9992eb5fb4ad4b222ab000a334a51b1fbf4e6308e93d4efcc96a7485e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6611ce334a4e166da56648eed5ebbeaf7f25db4592b42e95a3e4427c0b9c0c5b`

```dockerfile
```

-	Layers:
	-	`sha256:cdeae8b61fbe69785e76d5db00bbd65a009bb8fb59bdce56225ff11b9b49ba01`  
		Last Modified: Fri, 06 Mar 2026 02:03:38 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:996917eb91a9174759bfa4454d9e9655d1821683109e96bca1c412c59728cd4b`  
		Last Modified: Fri, 06 Mar 2026 02:03:37 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:df079fa45e22a074900f4147a0ac304179c4b8c3e84439e305c7b007a6ecaac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281809052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9870b40731530b1b0f9655be7a40e7b0dca0efca44de9a1cd135914f9ab0ec87`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 01:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:02:36 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:36 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:36 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:02:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:02:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742857c89c3fff9f983a1595594994ae63f49f2e0dd92faaa9d5886d69aedc6`  
		Last Modified: Tue, 24 Feb 2026 21:34:25 GMT  
		Size: 59.7 MB (59651871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fc96c42a24e91cdea3766c0ce54aa357b9d32ba231696142ffb8a0236b4d4f`  
		Last Modified: Fri, 06 Mar 2026 02:03:03 GMT  
		Size: 66.3 MB (66310458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d47f42e49b5b1824f0c700b4d521593aedaa7278226bf8d2c8c937a0110183`  
		Last Modified: Mon, 02 Mar 2026 22:04:34 GMT  
		Size: 89.7 MB (89696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cd08f7027c0fc10c870ee9810b434478e08c7b1ce8f37ea4b4e4658d80a42a`  
		Last Modified: Fri, 06 Mar 2026 02:03:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8530919ed0f461564edbdd8202359d8ab32656d2c1c46b6e2471408a03029484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa253c5216b8139da234679c5cdd59838b3cb3d9d008245dbf5ccd33cd7660d`

```dockerfile
```

-	Layers:
	-	`sha256:89e5f4ec8d758782e81ff1daeba0104560bdc875280de5fbebf435882edcd1ae`  
		Last Modified: Fri, 06 Mar 2026 02:03:02 GMT  
		Size: 10.3 MB (10303727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95667f4ff14a997010d737eb1eb621c451664728786b46ce275584a0679f9e79`  
		Last Modified: Fri, 06 Mar 2026 02:03:01 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3163c3ccc5b18590b4d95b516269e7369bb81f9a3dc44e8863b7cb8723be8d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 MB (311767710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d7ea1c05ed97a74c57b868be647fcc58f4ada4876e316dc6a624c238b08d2c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:02:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:01:13 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:01:13 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:01:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:01:13 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:03:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:03:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81719af948e0d6931573d27c651c0eaf79ce0227f4a28ca856902980121d770`  
		Last Modified: Fri, 06 Mar 2026 02:04:18 GMT  
		Size: 86.5 MB (86525370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e982fdcb72c3ad1cca7a139b473ea3951042395bd4cf7fbdb4f775c24a9b551`  
		Last Modified: Mon, 02 Mar 2026 22:03:07 GMT  
		Size: 88.8 MB (88784830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f77bc41890c5d2c5e04f31e08dc209ae7a2792bd779812f4ab0d3cd735efd0`  
		Last Modified: Fri, 06 Mar 2026 02:04:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5afcdf48ac088d0d8b894af2397d756e0dfca0aca6c0022d0e146f6cc905e071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77aba415e03196acc029996a27fec9b63e3db49825883612f248c740e379797`

```dockerfile
```

-	Layers:
	-	`sha256:be85719da28f69d6cf6e7a556ff1e51edb3f4ea0776f481f86752d776b467727`  
		Last Modified: Fri, 06 Mar 2026 02:04:17 GMT  
		Size: 10.5 MB (10524855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57cff2df6d885805ce2142a07bb7c59bc08c5d76e70e5110e0f1eed1b24903a`  
		Last Modified: Fri, 06 Mar 2026 02:04:16 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; 386

```console
$ docker pull golang@sha256:063dcb619e789aeeba667e9e135a300764c9092adab4b0a6b66c7a8dd34ef493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321904510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973f1fde7c9cfe50c1c51464c30a4542bd96f76149b6d76b78bf11c32e17b1db`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:01:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:02:52 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:52 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:52 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:02:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:02:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31e1fab6283d72f6ce2de137bc123a8ab89a85f0baa0b6c11c2c6d28c359a32`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 24.9 MB (24872106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383bd8d2ca9c40d67394c0121b8fdb7d7c8f44082342e21f4188fc611c88e9a6`  
		Last Modified: Tue, 24 Feb 2026 19:56:53 GMT  
		Size: 66.2 MB (66234334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ff87a18101ac961a6576f39de4ff650f2a32e80eb763454e097bc6a5cd6796`  
		Last Modified: Fri, 06 Mar 2026 02:03:18 GMT  
		Size: 89.9 MB (89871136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b2140e9f06d205b6b5af3fcc14f26b13013365f22129c2ff99cb48ee34776`  
		Last Modified: Mon, 02 Mar 2026 22:04:44 GMT  
		Size: 91.4 MB (91448922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e1df8b5062b092d874042060a458a59632614a1f374bff24380ece5dbce3ef`  
		Last Modified: Fri, 06 Mar 2026 02:03:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:18e79900708aa57adff95205ca15d364a5bed76f67b2b8ab22e26759dfd885ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba884ac68a6fa8db28be77b436174414b136e3a6aac624ed4a0b58b2aa0c40c`

```dockerfile
```

-	Layers:
	-	`sha256:0fa03d57640774da858f1ae8a7993d5fc6b33978d887f4b20e4f47c5c2655f0f`  
		Last Modified: Fri, 06 Mar 2026 02:03:16 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee7fc33e693e9f75a7467e8c5c9e3643625695d6c3edf000eb4b51a685c98ed0`  
		Last Modified: Fri, 06 Mar 2026 02:03:16 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:8bd3be32aea32a33cd415af73ff6afbf825fca44b2d94ea23be86c3bfab98185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 MB (293186744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326d202f54151bb429fe011d7aa1d85bfceef261b82b283e7285171e8c79c2ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 06:07:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 11:29:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 12:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:22:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:22:37 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:22:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:22:37 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:22:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:21:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6ec71ee94fb878725e70f6a21c20349985b89066361ee1f753b3854cfa2c839a`  
		Last Modified: Tue, 24 Feb 2026 18:41:37 GMT  
		Size: 48.8 MB (48782510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2283ea3597dab73b85bc0ebe9635f3297b9d6d4b8ff5df7913003859ba369`  
		Last Modified: Wed, 25 Feb 2026 06:07:50 GMT  
		Size: 23.6 MB (23615315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372ec86799dac23af2f0ffbced98ecf9eceeaa5ddf68be3af3cc474182e97448`  
		Last Modified: Wed, 25 Feb 2026 11:30:27 GMT  
		Size: 63.3 MB (63310148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8358d10d80c9af8f69fd6083cd0982ee261a68e3865c0f029247660744e146`  
		Last Modified: Wed, 25 Feb 2026 12:20:12 GMT  
		Size: 70.1 MB (70053345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c873d734029e0e4905a401dcf9758b8348160aa0ab7bf1cf0b2f08dfa5025af`  
		Last Modified: Mon, 02 Mar 2026 22:24:43 GMT  
		Size: 87.4 MB (87425268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef0c4dc6bb229ed06c1ac41115700e4ffeba503c4bb5973f9e72ae2fed9dc18`  
		Last Modified: Mon, 02 Mar 2026 22:24:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0b6333ee860dc80a6c20991d1076e280e6fac15d547252b41f18e42d8130f3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3a37903d871065f21135175684cb39163f964757bd3d0a8889c4de0b4d1ede`

```dockerfile
```

-	Layers:
	-	`sha256:07164bc6b29e585d00edf1efabf144e9d1299d81a1cdfb0c0803dfa2bb46ff04`  
		Last Modified: Fri, 06 Mar 2026 02:22:31 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:e0f2064d4b31d57eec52887945b88c8a49b985dce6f1e5685156a81e44fe5a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328621650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529c8da9575db7f77b5bb0e959559ed0b151180595e6c87b433cff80c5e1fd24`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 02:56:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 01:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:02:04 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:04 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:04 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:02:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:02:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba53e63c4e3e4d88f0425bc79a37e364db9aabbff9c13ece5cecc63ec880f3`  
		Last Modified: Tue, 24 Feb 2026 21:19:17 GMT  
		Size: 25.7 MB (25671399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eaeecfe60befcd3d5daac43038587e48eaaea46a2b5f8466018b05c5579686`  
		Last Modified: Wed, 25 Feb 2026 02:57:13 GMT  
		Size: 69.8 MB (69846164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b974129b6c3e3a7e528646be3ae3ea1f40ada540f810b50d02d54c23492805`  
		Last Modified: Fri, 06 Mar 2026 01:12:08 GMT  
		Size: 90.5 MB (90451243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcc3a57b0d1a4c549275152be846eeab1e4bfda9d363982944775991fe15219`  
		Last Modified: Mon, 02 Mar 2026 22:05:31 GMT  
		Size: 90.3 MB (90315888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8e13cee2e6d623c3bc102a2c6265bcaa57f0780480865fcb57823cf3aa1911`  
		Last Modified: Fri, 06 Mar 2026 02:02:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:dc8353eeeb3348e942349e92a50275550c3a8c449ebbcdfb9bbd65ef7a259d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43bb649ff970d0fa4b10b4bb0fb26f6a12e6032e0a0cf41b901ccc7740afd8b`

```dockerfile
```

-	Layers:
	-	`sha256:089648f757bc666c440b0fb588e9cd442dff535bc6299aaab533505721301d9c`  
		Last Modified: Fri, 06 Mar 2026 02:02:57 GMT  
		Size: 10.5 MB (10469516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:186b0d32f34158b576406f7226c55cd6e02d923614010722b55cbd5e11d5d263`  
		Last Modified: Fri, 06 Mar 2026 02:02:56 GMT  
		Size: 28.3 KB (28258 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:5ecaed70e359d2a2719832f90f743b0540af88c5c93d2ecf032bcb88997c539a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296531716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51569b4956b9df958bc95f656bd7a2e85383b89d5cfd31f32fe926429ced8bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:56:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 01:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:01:56 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:01:56 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:01:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:01:56 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:01:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:01:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1490eda04f0dc8144e02f684cac28c2862b3a584dd3e8ad7e22b96b35409c89`  
		Last Modified: Tue, 24 Feb 2026 20:56:37 GMT  
		Size: 24.0 MB (24033874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d60976a172fdc4da11bc00a6a1bd9ac1b17420cd914b41c43278a69a7a6013d`  
		Last Modified: Tue, 24 Feb 2026 23:52:41 GMT  
		Size: 63.5 MB (63501714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57377fd3c0fdaa6f3b6eee9865a1f3021c410d63da5bdf529e0ac5f9e3bdeb28`  
		Last Modified: Fri, 06 Mar 2026 01:11:24 GMT  
		Size: 69.0 MB (69045323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d3098d11b942b930d9b88ef8d2b13e42c10d7ccd12c5e317467f410cfa58`  
		Last Modified: Mon, 02 Mar 2026 22:04:29 GMT  
		Size: 92.8 MB (92802560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7cc7c085d9dc1a6682b8671453f8721b644b7535b62f677fda4c3ec5e3d8d3`  
		Last Modified: Fri, 06 Mar 2026 02:02:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a7a698ff702e0ea360b3785f29b904edbc9b1df87c7a852b0f3904ea143aaef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eef110952516f9d4a3cea9ae49033f12d9660e84c16f5ef04da3dbe27cc8e2e`

```dockerfile
```

-	Layers:
	-	`sha256:c39b74b04a77c030e829857adb3ee4a45d906b49b5f6051a354e8d4057d2e3ce`  
		Last Modified: Fri, 06 Mar 2026 02:02:24 GMT  
		Size: 10.3 MB (10328789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81e27779f5474eda9013b309822dcf98f20ef28aa68f68f4d66267a6f91a25aa`  
		Last Modified: Fri, 06 Mar 2026 02:02:24 GMT  
		Size: 28.4 KB (28384 bytes)  
		MIME: application/vnd.in-toto+json
