## `golang:tip-20260314-bookworm`

```console
$ docker pull golang@sha256:b4a8a4ca5250c7650eba5468b67b528915309568e4dac9941ac76e3d1d58d9ac
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

### `golang:tip-20260314-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:f72828a0b8e48b9c5e10c50ab6a75daef5e65b9fd40632efe7c008e4ba355066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323098837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d1c30223cdc94069736ebf5632b4b73e4f2d305e599f09362c98fc8dbcd430`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:06:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:06:08 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:06:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:06:08 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:06:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:06:11 GMT
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
	-	`sha256:86cb47aa42ef0056634a303e96593da9f0e9c7ddd2c080d02d8e38529935886f`  
		Last Modified: Mon, 16 Mar 2026 18:06:37 GMT  
		Size: 92.4 MB (92448527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4384ef542a16608e9b825ddf3c86dc09e4324c50fc9718c0261655531fdcaac`  
		Last Modified: Mon, 16 Mar 2026 18:05:32 GMT  
		Size: 93.7 MB (93727072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a685eb8e134600d3f059b0dc39d4797848d5a0989243ddebcad4e567a8b553`  
		Last Modified: Mon, 16 Mar 2026 18:06:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:75164f3c9ffa511f44e811bc5e6d28f74a6fec9b242be9751979fd4f16191dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903a75ffcf32204b508c70629922fbb2c9f0f9906d9ecb4c4f3eeee0f3b4233`

```dockerfile
```

-	Layers:
	-	`sha256:ec142cb1cf1bb2c81982a0852f98a731e20c08503a89e2b409bb921f0d273651`  
		Last Modified: Mon, 16 Mar 2026 18:06:35 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b14d35b971b9202dca54c42164ee185ec4e2ede82a1f366c5d7be9f403bfdfb`  
		Last Modified: Mon, 16 Mar 2026 18:06:34 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:59346f4cc2be2c44f9e758c810080e4f0e5ae245dac82f333cc4a2936d7e7294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281945975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb42b05257db54fa6dbb5d866c0a47ea398d0a2029a0a666a8160679e0ce6ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:03:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:05:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:50 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:50 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:05:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:05:53 GMT
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
	-	`sha256:911b5f4e2381bb69f0ce14458c5766b74a48ccb6c7fc0c22c2c77f8638c335f9`  
		Last Modified: Mon, 16 Mar 2026 18:06:18 GMT  
		Size: 66.3 MB (66305277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3549b40c9d6609f7ae376dd04fb2e1ccc5bd7d54b10023e8efe518db570d9`  
		Last Modified: Mon, 16 Mar 2026 18:06:19 GMT  
		Size: 89.8 MB (89838768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223abeecaf2550a6c451df566715e410c84ee7e5f873f3f00e3cf826cefed5fc`  
		Last Modified: Mon, 16 Mar 2026 18:06:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0f6782d611b447c2a7c63cb49e193f2d5a76ae4340d3c26f76e7a6465026eab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236f7530ffd08bcba9b2142a09a9f1d33eff7661732a45648f80de7440671a1d`

```dockerfile
```

-	Layers:
	-	`sha256:94ec9a3ac671762c4b42ee3ba13a7ad2d02148a85fdbbd4656a1feaf4a009182`  
		Last Modified: Mon, 16 Mar 2026 18:06:17 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d76bc6683c40183e7e2504d131a73736c63ded2e38009bd97298add2d9412c6`  
		Last Modified: Mon, 16 Mar 2026 18:06:15 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ec627cc7b3df9bf7a369addc85df3d779c972e615f88f7a39c93cb869c97179f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311892176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f4d19179ceb3cec9b7441e16b36d18d4e7d8453a86fb760a801b4fb71029b4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:03:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:05:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:38 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:38 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:05:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:05:40 GMT
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
	-	`sha256:dfab7338810193a2ec4f4afbbdd50aa26259817ebc86a8f835481ff804eb8eb4`  
		Last Modified: Mon, 16 Mar 2026 18:06:06 GMT  
		Size: 86.5 MB (86521202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad36eab247615030277063307261e70ef31ab1fb10cb9e2a3d5ec600c3c4c21e`  
		Last Modified: Mon, 16 Mar 2026 18:05:21 GMT  
		Size: 88.9 MB (88913464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0b2c01e47a1f757ac12f38a407a6e2b53ff167c52fcb7aa574e4dc4f0d7b24`  
		Last Modified: Mon, 16 Mar 2026 18:06:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ac6f32e498eef32dd674b735faa61e9839e55dc960925327c03025ee1f592076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955b7632af1e83677c910b82fe876b13a832f1bbb28c0f8be339644448e7a043`

```dockerfile
```

-	Layers:
	-	`sha256:48e7903e37e0809b91b0daf0b7f32c085459c514a57227d27b3f5dd4ab42d06c`  
		Last Modified: Mon, 16 Mar 2026 18:06:04 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e7ab67d3fec10bc1b63f645f96e93371a11bdb09a89d31fe674c7952ad9b59`  
		Last Modified: Mon, 16 Mar 2026 18:06:03 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; 386

```console
$ docker pull golang@sha256:9143dce0237f7ac96cefc6ec51a10090519d967ffb52df4b885ad9760de09273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322032407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d3b2283f7c961188ea17dd3c4b537cd29b9d362af31a9e9959e8e66d41684a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:03:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:06:03 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:06:03 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:06:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:06:03 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:06:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:06:05 GMT
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
	-	`sha256:67d93c1b6660c7ae31867fcc7ac329336b79aba0724b6ea54ba958d5b326bf16`  
		Last Modified: Mon, 16 Mar 2026 18:06:31 GMT  
		Size: 89.9 MB (89871447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beadfccec3ab6ced574e10800119a7f79c633318e3fc8b60061f1b218729af5`  
		Last Modified: Mon, 16 Mar 2026 18:05:47 GMT  
		Size: 91.6 MB (91576509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f77f4027bd9dca3b6a39b55bf7927cf2f0c5d028f9fe879eb803f9ec4157080`  
		Last Modified: Mon, 16 Mar 2026 18:06:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4fc826fa2d0328d85693ff843b010f74221a1121bb88b5d4d472c362277ef2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e27236f5a81a04934235a2325dfec6bbce7ce15a123c3d77aaed42cd98f69`

```dockerfile
```

-	Layers:
	-	`sha256:a4ddb190e6f21b9385a8043f0bc2b89c2765fead3dd5ef0654a3795be1275bf7`  
		Last Modified: Mon, 16 Mar 2026 18:06:29 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b25166c0ba65ae801dd4e668ac19eb2b31ab4c2610204192bc184e8b9df36d`  
		Last Modified: Mon, 16 Mar 2026 18:06:29 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:a9e31e14eba1fee28b9aff855e646a979d6fd39915537f161e3df34357bf547b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293326203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7bba2011e9036b378b7d9aa963f0a2757d5edbb2ee39d1a14e4033f69ac6f3`
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
# Mon, 16 Mar 2026 18:24:48 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:24:48 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:24:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:24:48 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:25:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:25:03 GMT
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
	-	`sha256:ff347f6a145f7f93bbfb2eb74f5a1a353cbf6b3881958a27e04c5d6b711e338b`  
		Last Modified: Mon, 16 Mar 2026 18:27:00 GMT  
		Size: 87.6 MB (87564728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b407766a3ae114da28fcc9b1a90384b81c510e9bc6657645365cc48235c14ac6`  
		Last Modified: Mon, 16 Mar 2026 18:26:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:60d950f7a2c9efe6cf0e67744713ccbe84c51b8bf25c1b270ddd4b45f53d34a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d079cfe4f93f19f30ad72a7286e0d017bb8f23a4822a4c66f32a0f6b1dfe9d4`

```dockerfile
```

-	Layers:
	-	`sha256:7eb96918b2aed91f9e0af860166212bede559e527e41add350c0fbe5f78427d8`  
		Last Modified: Mon, 16 Mar 2026 18:26:50 GMT  
		Size: 28.2 KB (28239 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:9aa712cb0306b34532c3df675da465aa71046f3e237834ed1bcfa4e2cb176a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328751726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822ce5f80738beb534881c7a5148b297f2af4f186455fdf51ea6938dcaab9970`
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
# Mon, 16 Mar 2026 18:05:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:42 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:42 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:05:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:05:47 GMT
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
	-	`sha256:fa5ba3f21f31dd88c9cf395edb0e30aca822e3dcde51bd5a6421a6f428d5671b`  
		Last Modified: Mon, 16 Mar 2026 18:06:39 GMT  
		Size: 90.4 MB (90445965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43689c4dbd3be7aaa673816e7cd68a511ac3817adf011cca22445aa40e3b08c5`  
		Last Modified: Mon, 16 Mar 2026 18:06:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9f791df30240ca0042c4513a9fc4aa629c616fef2d054db49130791601a866a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83de60e56901bce3e00473e3b2629fef5284181718e6e72ff5a136c9c514d87a`

```dockerfile
```

-	Layers:
	-	`sha256:d4252dc929a269108fdb2f36c2b96db16d54022bdca59a9e8aaf2b8ec61202cb`  
		Last Modified: Mon, 16 Mar 2026 18:06:37 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a732d836424288a73caa0c85e0d76322f2494273c65c1b5bded64097b0777f`  
		Last Modified: Mon, 16 Mar 2026 18:06:37 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:aa44494a747dd67304adf23326560606a6c1ca8e3f163aec3cae8b23d78f2e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296654509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bc5499e32b137a409c70c666f36d285e78fd5515ad98535a967b98524fa745`
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
# Mon, 16 Mar 2026 18:06:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:06:20 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:06:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:06:20 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:06:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:06:22 GMT
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
	-	`sha256:a9e78b174fccd5298debc49ecb6092c7b356413921318c225406833e6427b55a`  
		Last Modified: Mon, 16 Mar 2026 18:06:51 GMT  
		Size: 92.9 MB (92925352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ee7e0e08703b1a9be8bf38c027e997c34a2f3405463a485514dfeb1db9437`  
		Last Modified: Mon, 16 Mar 2026 18:06:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9a45b37ab4ebe3e89f73bcb67c58d011a73706801a66ea1e308469a21f11bb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f83136b1962d2e99850f95fd3344f7d4d2db3bbfe235f841d7e49684dd2ddc9`

```dockerfile
```

-	Layers:
	-	`sha256:d739e17a0459021547c40b23c77bc828db90877bea897acdfba4a14212352cb5`  
		Last Modified: Mon, 16 Mar 2026 18:06:50 GMT  
		Size: 10.3 MB (10328791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa92e334658dbd48d7c2eecc660d55c0741ed9304b80ba20cc7a41b3b0c67454`  
		Last Modified: Mon, 16 Mar 2026 18:06:49 GMT  
		Size: 28.2 KB (28212 bytes)  
		MIME: application/vnd.in-toto+json
