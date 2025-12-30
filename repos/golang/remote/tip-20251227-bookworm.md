## `golang:tip-20251227-bookworm`

```console
$ docker pull golang@sha256:e9dfc58a75d6caf86b3450339a2bc1d0d2ac9921f50b6684725fe991946d1127
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
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20251227-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:ea0c4c2d2301a0905606bc2c3d3cccbba3567968b8592f3288139f2ec3754d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324361487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43801ecf5cc0265d42c9d7b423dee54e888b465d5d1abcc0616d9bacb1599bfc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:22:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 03:22:22 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 03:22:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 03:22:22 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 03:22:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 03:22:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858b7813255a9cb57d05f02b50978e5b5965b0cfc040288fa29905cdc65ad9a`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 64.4 MB (64396090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d175d4e900867ba3e10389f4d6c61b039c96ec1a4997c2ed011d6506422357`  
		Last Modified: Tue, 30 Dec 2025 03:23:05 GMT  
		Size: 92.4 MB (92410487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c54e75f0355977f49fd303fcd47e9c421e5cb4ce0639b9b1710d2f526d135`  
		Last Modified: Mon, 29 Dec 2025 22:17:03 GMT  
		Size: 95.0 MB (95044613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a98a6e4c71ac9319b99b18a57da6c5576366812f48711233c4ae462f8369fa6`  
		Last Modified: Tue, 30 Dec 2025 03:22:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1f9425b358d7df2ef55bffaa87e80c0d445a84f769c5c49e9700eb7dd1e86174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b295bed167d35f025eb40eff164b7d68680c8415e39c8b6504ca3b6baf1ebf37`

```dockerfile
```

-	Layers:
	-	`sha256:e28546615058a7a403b31f9278edbf9e421acc4bb720d2cdb8dd64f22f4b119a`  
		Last Modified: Tue, 30 Dec 2025 06:25:39 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0527d4cb52ee80633044cb332178571fef823186b558e57dec8163ebfcedf7`  
		Last Modified: Tue, 30 Dec 2025 06:25:40 GMT  
		Size: 28.4 KB (28385 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:8f5a01c2d6671f5d2b8af67132dba59cd53e6b9ef1c38e6c11d9efbee1bee0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283174435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af758a61229a2e67cbb37bcf96249309bb5c3ea6211a60f9d518f93d8875e3d0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:19:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 03:19:39 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 03:19:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 03:19:39 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 03:19:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 03:19:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7f06489595662b32227ed4939431e5099ae83a2661a5770c752a389e68e400`  
		Last Modified: Tue, 30 Dec 2025 02:06:44 GMT  
		Size: 59.7 MB (59652384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66e3c7e2994f9b3c82e01b8d4ae75d62d4fbd0cce592804325fc6258fad3320`  
		Last Modified: Tue, 30 Dec 2025 03:20:15 GMT  
		Size: 66.3 MB (66276468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a592f218adec4eba0bdf6f4ba76e47643fbd079be331ecdb85fd7600664dc026`  
		Last Modified: Mon, 29 Dec 2025 22:16:40 GMT  
		Size: 91.1 MB (91114533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21325f1d8f5edcad890f471e17f372f229d72a8acd80fc9acaecc395f14808f9`  
		Last Modified: Tue, 30 Dec 2025 03:20:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:90d7bc8f95c1c25cd90a9acace2d2af30a7347f9091447790cb9887efe10c01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f2e0a20257e95761841f93ad903600c4a26b7d1a478e726eb44f696dee52b`

```dockerfile
```

-	Layers:
	-	`sha256:59fad2fc58d3443bf307f533d025a60d21f1235abc6c9d7d38fe3eda4df17985`  
		Last Modified: Tue, 30 Dec 2025 06:25:47 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38e520869b19e898c9e39d56faeaffcc3aa569f8188e96ae1bcb0d4d988173a`  
		Last Modified: Tue, 30 Dec 2025 06:25:48 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:fddc3e3fafa2a6240074c414cd27badf6b6d3d45fd6b0e556705d054bf1ccf66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312944833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cdbb27baf852b2fbfce367b81a8375a62b660c2b8ac18bd2ec9a2c540eda27`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:21:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 03:21:57 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 03:21:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 03:21:57 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 03:22:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 03:22:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2bdfee63f0c6b24c94412dbdb19fb6c50fe6706af6bfbace9fbcb434612db`  
		Last Modified: Tue, 30 Dec 2025 03:22:37 GMT  
		Size: 86.5 MB (86490997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff2a18ac08f0eac3e3d9e16d67bcab1f49cd95a40840a22cede89724436815`  
		Last Modified: Mon, 29 Dec 2025 22:16:45 GMT  
		Size: 90.1 MB (90124983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30de4cc044aa33b3d973409089a99ee554b38177b914080f1c5c8ee728f862`  
		Last Modified: Tue, 30 Dec 2025 03:22:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ac0f0050ed94fa50a03d642de1a10c00f961ef7dff3d9f10c7ae6312012f4354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d49c75c7ae7d3a741ff9c94d95389ebc607b330a6beb332d1e4c62b1091b29`

```dockerfile
```

-	Layers:
	-	`sha256:4d65e4bb24fd20399a38fad2fc66fd5ce39d59fb3e6cefb0ed5610334758a459`  
		Last Modified: Tue, 30 Dec 2025 06:25:56 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4130b70bf574edd937429ffe200b80edd26594f161bc2753236a59a59fda85c`  
		Last Modified: Tue, 30 Dec 2025 06:25:57 GMT  
		Size: 28.5 KB (28521 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-bookworm` - linux; 386

```console
$ docker pull golang@sha256:90b6300a978db20b518692780b8c46945238398eb7fb3e0e45bd314943a203ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323343427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e5c5b19d4b7a3246ef21e4a4c1b1b0ad409c72f8f863008b6f943b406b8743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:32:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:19:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:21:29 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 02:21:29 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 02:21:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:21:29 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 02:21:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 02:21:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d27cc9ffb7903d292157edf3b1fb57175a2a59b66ae4855d328a6a97d9b4a6e9`  
		Last Modified: Mon, 29 Dec 2025 22:24:49 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63bb42155eb2fe3cb6496304c20382db95885b672da0e34a3fffa188861a6ec`  
		Last Modified: Mon, 29 Dec 2025 23:47:31 GMT  
		Size: 24.9 MB (24864466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10eedb7d741cb151d52259302acf62c6c98590a9a4168d4370619e890f15715`  
		Last Modified: Tue, 30 Dec 2025 00:32:36 GMT  
		Size: 66.2 MB (66233282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e295f8252ca90e89f51c1363170a6376ce4095e7645eaba61a98042c65f425ae`  
		Last Modified: Tue, 30 Dec 2025 02:22:14 GMT  
		Size: 89.8 MB (89839937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b6f0074455116012c1ba771d20edb2ec10d2462257d60366f8ccb9b9224a99`  
		Last Modified: Mon, 29 Dec 2025 22:17:35 GMT  
		Size: 92.9 MB (92938705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575dbe2fb45e9468db32a096a5c32074522972f62ce95c55407ebe75f1465a51`  
		Last Modified: Tue, 30 Dec 2025 02:22:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c543ca285f12d47013a6e570d44c6c1bbe57eb915eaa09084c67b57d0c4fee8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1393781d7623e4fcf8ab599d8591e32ede8f54ff2476af17600821c1310acc0`

```dockerfile
```

-	Layers:
	-	`sha256:4418ac70f1828e832a87b372b6c622992d41da35cee387eba1e6315d909595d4`  
		Last Modified: Tue, 30 Dec 2025 03:26:00 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c83effd6df77e320910a28d105e949a1b9f1de1679ae8284bf2831492a73cc4`  
		Last Modified: Tue, 30 Dec 2025 03:26:01 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:f12758c0329d9f1d55b404698ceae7e7c8bd52bfdf0485812261881d5d818877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329922682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aa59026bd8f866bdce623c96258866ac9f8290ce6ac9922db7c767537b1e3c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:30:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:16:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 08:41:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 22:16:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:29 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:29 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 10:29:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 10:29:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7517c515ac5fd6799cec288b72512b8ea3fc54d2d37de5af54d06ba0ea2f21bf`  
		Last Modified: Tue, 30 Dec 2025 01:31:20 GMT  
		Size: 25.7 MB (25672165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ff2cfb691fedcba1692cb13fd0632001d1a876833f4cd2aa52eba87257a8f`  
		Last Modified: Tue, 30 Dec 2025 03:17:48 GMT  
		Size: 69.8 MB (69845530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb3fd09a1e6774e533a42b26351be92003f5bdea475b8caa70173ad58b79d9f`  
		Last Modified: Tue, 30 Dec 2025 08:43:16 GMT  
		Size: 90.4 MB (90419830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d98e6a9db6f27c232427cc65a14243d3dc0a9f5145a0455e78bccfb2bf7249c`  
		Last Modified: Mon, 29 Dec 2025 22:17:47 GMT  
		Size: 91.7 MB (91658002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7785ac6f814e946243f18d76b5755d85e5be2e965a7ae9ae33a34584cd794ee0`  
		Last Modified: Tue, 30 Dec 2025 10:30:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9c627314caad68fd995090f686e9833ff7a1c2adf152d5e6fa00da92c5263671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13644cb49cfefad1e8da6fd0bc9390c829d661419ca37ab1b43f514f67cc27ec`

```dockerfile
```

-	Layers:
	-	`sha256:5e910bcf5676c4bddcf9036131a120ea7cd986bc1a8763b131fe5fd4e723bd87`  
		Last Modified: Tue, 30 Dec 2025 12:24:51 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be8e5a7f536f0f59dc5cf8d86296c10d3fcee971fb8191da8ac6076c833434e`  
		Last Modified: Tue, 30 Dec 2025 12:24:52 GMT  
		Size: 28.4 KB (28431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:cbb4e5a8a9cb97fdd114e69a5f845cca23c16e3047ef393f2b799eb3eee437ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297881163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e4459cfef43768f9e35d8a05ec1e177b1a1c30cd5b2a3d3362cf946c0a59df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:19:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 22:16:41 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:41 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:41 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 04:23:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 04:23:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ce8a6983b315f7ccc96b582192afffde7bfdc0a45f357f2cd098b4f88aab2be4`  
		Last Modified: Mon, 29 Dec 2025 22:25:37 GMT  
		Size: 47.1 MB (47137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acc4c1479120c6249296b3550670caa7738ba389b23a7ca3973f7732c12c0ab`  
		Last Modified: Tue, 30 Dec 2025 00:42:34 GMT  
		Size: 24.0 MB (24027124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013d337299523414af9c112b1b1a1d201a2c6eaec2baa26798cdadeeaf575ed2`  
		Last Modified: Tue, 30 Dec 2025 02:20:20 GMT  
		Size: 63.5 MB (63501425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a50104ac36e31bee7580bfdf7cf8ba0d5d569364966c5b8ab2d26fe49e2a97`  
		Last Modified: Tue, 30 Dec 2025 03:25:31 GMT  
		Size: 69.0 MB (69010871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ce8a7fa174e9abbfa1259cfd0fba44c900e27f7f4a5ae1c83f6fe0801a275`  
		Last Modified: Mon, 29 Dec 2025 22:17:17 GMT  
		Size: 94.2 MB (94203858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ab8877dd30ebb7b237399097cb5459172e77e1594003aa42f69e35422adcf8`  
		Last Modified: Tue, 30 Dec 2025 04:23:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d0ed90d9a18478f132e6d6d0439ea4ec144e0381eb136e76c4c6330550817704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b154d0343b5de012f973dff41a9e56ee301b55abeb74f12c692aaf6d1e1a2526`

```dockerfile
```

-	Layers:
	-	`sha256:ce102109909be4e0cfead83b5007be36cece5b3f5945f6f0e6c9a34cbec2b529`  
		Last Modified: Tue, 30 Dec 2025 06:26:10 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665626ebfe749f8bd985f3d8ce6b3beec500968f04be26a41722fad9ae9b454a`  
		Last Modified: Tue, 30 Dec 2025 06:26:11 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
