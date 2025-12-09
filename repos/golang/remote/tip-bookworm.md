## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:28d3697d7c0601dcd12e4fa50654cd491c0aa9bf05c6bec0c4093614de6c047d
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
$ docker pull golang@sha256:f123f64ef1f320e60a1d238d7b04f2f8b8ad5566cb35ecca5dc563447ebb300e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323704401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4eba76d484e5c87f59c250a4c7bdc113a0d547dadd28f519b0bd84dab32f4d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:30:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 01:30:02 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 01:30:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:30:02 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 01:30:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 01:30:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6058b737bc396c7a239907b60c8da774fef7a07c24a5743dd83d236e71b0aa0`  
		Last Modified: Tue, 09 Dec 2025 01:30:46 GMT  
		Size: 92.4 MB (92410661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949364a36b81a9ad117004649aaa40ca173e0cb5059f62e3ed14f9d09d82b4b7`  
		Last Modified: Mon, 08 Dec 2025 20:07:50 GMT  
		Size: 94.4 MB (94386989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787367e00d0aa697c7ca2809cc60285f45f848a01357b32bc7b75a2c4d685228`  
		Last Modified: Tue, 09 Dec 2025 01:30:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ccd198a1f9bbb510f4a963b55659997f5924fe0f296f50ea3b66be58cab1f2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aee5a8f8c6213648d5b9ec1459ce318ddc78f9c9b33aeeb7d3e91d0a7e2d7e2`

```dockerfile
```

-	Layers:
	-	`sha256:2593eca2bdaf9c3b2834e711704f67b4922aa53dc64ff313d00a49b5f1bffadc`  
		Last Modified: Tue, 09 Dec 2025 03:25:46 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a57ce2d68fd84a2add9be107718d0145953c3a268991e0571f2c23d3fe0144`  
		Last Modified: Tue, 09 Dec 2025 03:25:47 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:bed9fd841bbc4295feb25ecac85c5ddc3b48797058d0cc5e551d5903651b71ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282510867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627c5a8e74755d675a3e2fcf4e720bd6638f68768d3520e9b8883fc9d7e2c59d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:20:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:20:00 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:20:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:20:00 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:20:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:20:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b6eb0fb27a6d99b6b7a2a32ab126d30b16ebd113a3a3e174d37a032cde9bd1`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 59.7 MB (59652137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e7376308ea92e1a058ca3e7c47a500c1843cced4c50253da92dff9e788f22e`  
		Last Modified: Mon, 08 Dec 2025 20:20:40 GMT  
		Size: 66.3 MB (66276486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fa0b6c68e96e333f64da015866d36d22ecf4302421d4e561b2c28faa5b8bbd`  
		Last Modified: Mon, 08 Dec 2025 20:20:43 GMT  
		Size: 90.5 MB (90451274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c2f11237ee7c2d0c5b51877668808dfdb06f11c15e40df120a2ea57a07da63`  
		Last Modified: Mon, 08 Dec 2025 20:20:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:264685037c005ba6c0463562991b852a9404bc6ba504ce349874a333361e24bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5549460d236e9eb3bd94ef562d70f6f1dba1328c4e5eca1792dc1af8c6502b7f`

```dockerfile
```

-	Layers:
	-	`sha256:10f0213fbcbc186cfee1bfe6dde39ff40389b237f22cc52bafe45011185e3be4`  
		Last Modified: Mon, 08 Dec 2025 21:24:55 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71844ca07743aad18366accd7532ee702ff55fe101bb57f82538fb1332f5eb0b`  
		Last Modified: Mon, 08 Dec 2025 21:24:56 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7e8d03d2e4482cf98fd7b60f48b2018c23831836a177ec2e7a8674ff54d47c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312274993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a757e991aaf8b734c673cd97d410e659cd0367c925c1fa8f0bbdc55fc372c4e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:15:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:16:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:16:37 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:16:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:16:37 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:16:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:16:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b302e1a0dadfe9e3484c89806a62acc86abb357dbd3db152e09c7d013b6eeb26`  
		Last Modified: Tue, 09 Dec 2025 02:17:28 GMT  
		Size: 86.5 MB (86491023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2568df0f74d7435ccc404d81d30d0f293c9c2980ac0f029d1100be5d1622d029`  
		Last Modified: Mon, 08 Dec 2025 20:09:47 GMT  
		Size: 89.5 MB (89455005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532983669525748c90a2a7637437bf6005bca5208e69bb8e743f4bcd0396c635`  
		Last Modified: Tue, 09 Dec 2025 02:17:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:cb92cbe95fb63b66d9665bae69e2eb678ae53b1aff2f0818becfdc231d4908fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774063216a396af30cc622efb16c8b1ef7cfe5e126ec0c3123e45a9f453e34cc`

```dockerfile
```

-	Layers:
	-	`sha256:810828866332c78b56e1bb2ce9ffb44c38c44e67dc0809dd188c8ca50cd4e825`  
		Last Modified: Tue, 09 Dec 2025 03:26:00 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b668bdc0a1fae66c39aaf6d511a8a2f535e1f0bb5b082864787dfb4a7afbc0`  
		Last Modified: Tue, 09 Dec 2025 03:26:00 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:506a3aada1cb36b21939f110a5ee8a3caecbb526c9560d0b012ccb6ee31b0da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322682693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b2de6f7db5e59ef941357038267f278243f69fdc48a40002e04843ef2b2172`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:14:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:20:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Dec 2025 02:20:42 GMT
ENV GOPATH=/go
# Tue, 09 Dec 2025 02:20:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:20:42 GMT
COPY /target/ / # buildkit
# Tue, 09 Dec 2025 02:20:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Dec 2025 02:20:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8c9cca3d9f455dde3fab1917d275b029f5f2978fcd1f8f1b757098b58abc9d`  
		Last Modified: Mon, 08 Dec 2025 23:14:28 GMT  
		Size: 24.9 MB (24864339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd442778352104a3bf918f8351b8ac2573f9aa7b0d9136092884f7f79017f9a2`  
		Last Modified: Tue, 09 Dec 2025 00:24:01 GMT  
		Size: 66.2 MB (66233858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922faa1d022c45971265d8530833313ad57043247c7ae65989d536c5cec03053`  
		Last Modified: Tue, 09 Dec 2025 02:21:18 GMT  
		Size: 89.8 MB (89840000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2714e644cc32cbf0646554d2bf879368eb0872b6982a8a69088b6c556adfd2f1`  
		Last Modified: Mon, 08 Dec 2025 20:08:50 GMT  
		Size: 92.3 MB (92277519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5662e039e6313778ae51e94ce7f31a19726ad7c837c575922b07cf070c4b521c`  
		Last Modified: Tue, 09 Dec 2025 02:21:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d3b8b59a62725b9468a2a4ad0a7af739c9cd580b21d98a0c7656ef17cf331bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15faadf3dd929d4d3b954c8df8a9a5fb107e30cf7693eec04521b33e53a459b`

```dockerfile
```

-	Layers:
	-	`sha256:e14c0606abd78759cfc8165a1be517f64b0f44fb4f104170971c50a8d35c6e92`  
		Last Modified: Tue, 09 Dec 2025 03:26:07 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42261d238db4522baab39b96e4bae1662a48805f1aef26c48dffdd97047844cd`  
		Last Modified: Tue, 09 Dec 2025 03:26:08 GMT  
		Size: 28.4 KB (28352 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:72e0b32fbceed0e07c1ca2051f51956309379cddf50cba2c98164b055a6028b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293823601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9580b6249f189b653c3228b749c4739087b807a2a80f8460db83dfdc1933851a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 19:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 23:35:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:25:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:25:36 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:25:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:25:36 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:25:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:25:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bf41c56cb3beefc6b6211c26bdc048d41c337f12bc0bbfcfa89dfb5de99b7`  
		Last Modified: Tue, 18 Nov 2025 19:40:58 GMT  
		Size: 23.6 MB (23614038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a4cb619dbd7fcb3e0be3246f973ccbe692039c1fd01a193751c60045de0d3`  
		Last Modified: Tue, 18 Nov 2025 22:12:34 GMT  
		Size: 63.3 MB (63309296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870c654cc97051b29e543234a565ca86980db6e2499d45b06d4424741a820d98`  
		Last Modified: Tue, 18 Nov 2025 23:38:02 GMT  
		Size: 70.0 MB (70016928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a404c617d98e798d613f962c73f3c77a8a5630f3f06d7b5b8cd7bbe14b9b06`  
		Last Modified: Mon, 08 Dec 2025 20:28:11 GMT  
		Size: 88.1 MB (88122225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53af91a6ee3441aa8e2012a12d7fe6a866ddf69397ab71942ebfead2e40c1df`  
		Last Modified: Mon, 08 Dec 2025 20:28:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fdea7da2984f9e55e966b2d51e3fd03f56d818172503866ae896453cd42bd656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92033242c4c73209b7b5ce0fa8aab67617e9383992ea70dbe65b2af19007f007`

```dockerfile
```

-	Layers:
	-	`sha256:e4f55742fe76afc1464a42b46b369c992ee80159aae9a90c716d40bc2e3f9118`  
		Last Modified: Mon, 08 Dec 2025 21:25:23 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:67901c979efe6bc3ff26debd6ceb51a7f6c38eb8dfb5ecdace626c7331e5e917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.3 MB (329260885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7af88741ce5da7fa885e3b4cf811df87bb23db5f831f4f9cc76769fc15530c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:27:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:23:03 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:23:03 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:23:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:23:03 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:27:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:27:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17787af1df16ce560e48a9be892094ace19b1aecc7f06ca1e97a2e20987822a5`  
		Last Modified: Tue, 18 Nov 2025 04:05:05 GMT  
		Size: 25.7 MB (25672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d717b62eb888bb16cb77af768613d5d676b28f09ab1cb591a5130af4b846f`  
		Last Modified: Tue, 18 Nov 2025 06:52:50 GMT  
		Size: 69.8 MB (69845622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5512ed637996f7ac8314c3bff193637e4e7fe6c3e10a579b4db82c1f79f67c6`  
		Last Modified: Mon, 08 Dec 2025 20:28:54 GMT  
		Size: 90.4 MB (90419795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7f78d7b3fff51dbf03b6fcb119f6f6c12d036239dbfd1e84cb159ba6461fe1`  
		Last Modified: Mon, 08 Dec 2025 20:25:32 GMT  
		Size: 91.0 MB (90996328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6777919a70b74000b69c25d9d14e09453c33be083db66186a3d85bd022aa0b`  
		Last Modified: Mon, 08 Dec 2025 20:28:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ab57e4b93c6582d581f326819d4f3c802f55105df62a4af5c1b2d15e13947a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16dfcd43a8f6d795d9298fff837e37caae96061ffcf45a29e99712a04174ecef`

```dockerfile
```

-	Layers:
	-	`sha256:6daff4f12bbc66fc8852be35e219868007690295cbe44f2952cabe60002e176c`  
		Last Modified: Mon, 08 Dec 2025 21:25:30 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca04a7723215b113e02647e74e4f10e4064e46ff14e2e7d42b3296b6fcd0b7f`  
		Last Modified: Mon, 08 Dec 2025 21:25:31 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:401385aa7bb59099000a554af98d47ccfb1e79b7ff7931e04176211454407829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297230681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b845c902b6817cc7abdfbc28840432346e075ad42341bc826aeb2761ae977cee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:10:20 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:10:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:10:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:10:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f80247bcc58a5a903807561f3aad626158855a07b7817a9ed9975e9775ae2`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 24.0 MB (24027180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099f215b279a7199da193e9e90d7e8e46ea9dfcda3ebe6c6379eb56d436eeae`  
		Last Modified: Tue, 18 Nov 2025 05:57:22 GMT  
		Size: 63.5 MB (63501447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cad7e486e3b479bfad5906ce23c5ec945accd3f3790a3a317e6b77817db8d3`  
		Last Modified: Mon, 08 Dec 2025 20:11:25 GMT  
		Size: 69.0 MB (69011128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d45aee96e59637b1f14b3eb6f81f4f4c64edb3653263ca9a0c489bd88115cb`  
		Last Modified: Mon, 08 Dec 2025 20:11:07 GMT  
		Size: 93.6 MB (93553127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0a9b3be52b9ba44483a8aba4e2a810a72e4a02da8b35a6d004d3aec33a4320`  
		Last Modified: Mon, 08 Dec 2025 20:11:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:adca1e37ca7d880d463b1af7853fb3c1498c30dd5e43aeb70848f3f0e9fcaceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28013ac94f7d65875dc8515af39ed79fc6f656b415e39147021201ea283399a6`

```dockerfile
```

-	Layers:
	-	`sha256:e2cba5b1192036bd2070125b67cf0528a311e06947a21cdedeaae21cb3ac83f8`  
		Last Modified: Mon, 08 Dec 2025 21:25:39 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c29bda3bd5e9b5e55c4bcb2235a140008e9884d76439290f1caee5128790f1c`  
		Last Modified: Mon, 08 Dec 2025 21:25:40 GMT  
		Size: 28.2 KB (28213 bytes)  
		MIME: application/vnd.in-toto+json
