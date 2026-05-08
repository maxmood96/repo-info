<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.4`](#spiped164)
-	[`spiped:1.6.4-alpine`](#spiped164-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:3b6ac3e45f172915009c7662a28b4462f14812bdaa14d3256155618d0262ca50
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:3697a0c4441ffdebbc45026e68caef4b180d0435c04825aea8683826608b6a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36830248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7651265801ee07aaa82006e38d9ac3f69a351f0133ed076c95fac3c4070b5869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:34:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 01:34:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 01:34:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 01:34:47 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 01:34:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:34:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9b6c12ee3ac5c9fd735735d76164bc3226971d664e3cf1cde43f281aac222f`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c82eb68b5775c3e49cf91b695f5b281d5635a64d68a48d315ad05b5c25c423a`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6541376dd96a6fc09591396c5ee3d29921d988f4bf5c8ce27b07276d38546423`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 7.0 MB (7047707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffaa1a14fd226e56da74302eab175251416360e90c228fd94dade206c9d78c9`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5303c4f9d1890510b3fa6ddd08d126352bdc1920a3c7c4ce5f8238ef9f18db`  
		Last Modified: Wed, 22 Apr 2026 01:34:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:d0c6471bc8d160d5788eb73aea715f40a47deb73ce301ef156c476a711c3efd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce174c86dade55ce31b891e3eb31393c052de868272c4047ea5f570c54a06c6d`

```dockerfile
```

-	Layers:
	-	`sha256:4cb9cddb67663afe5f2c1f31b7b70b74b000c8330a998fe3c01e31047495cea6`  
		Last Modified: Wed, 22 Apr 2026 01:34:54 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b2345e28b73fe57e118cead927bed244d50e3bd5ce1d6cec6d4134ab93184f`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:58a9096e9da905bf9e7530a00b0386ae545910541ba7636134b7f325a3dabccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d21b5f45c11b35928dffe02224e155b54d9ab4a072b30193e228c96092ef243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:15:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:16:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:16:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:16:28 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:16:28 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:16:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4794e1957b3cf639e20aa4a0d33a68c0170d04be31dfa0d1e3032edec682050`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506884dd4194f6c16e334d33decb7e25face9b3cf73131bf09e3a676569f278c`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ddf0bad83cb62e304347253656f7c58364f61c63151f32241919af173cab8d`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 5.8 MB (5789064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e465e59da14247ef0cbca66c2a5502e3a48bce76072d98ea60321006753a2b20`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cd1db1a45425ed24b69890f937f29324664c3ad90bbd4a1103a1e5c7a59527`  
		Last Modified: Wed, 22 Apr 2026 02:16:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:9710231581fc8bd5e10a24a668c5f93c84658a05f2489c9e329561f21aef8ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f876370a99391838ecfc8b380afcf44edfdb92b7866cc035577e33d97017db`

```dockerfile
```

-	Layers:
	-	`sha256:0fc5644cca517238d76d5f7971f9b147255edf3e7f6eda96e7449b4d72ecbe70`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bffcc7d5d03f329eed1cbe5f2ef5ae347e4005ac12647f80dff37b77315c0b8`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:c4e99b1c150ce516a4f8bfd06f5ce36db9619da989d63041e2e3ed867e16d9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31801768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eee37b96c47b6d13903255f49ebefb808aad92497750349796120f32c768530`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:17:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:17:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:17:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:17:41 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:17:41 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:17:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac891b940103b402884a868ba78e5b89adc92b82368d5cde3f77372c4d9389ba`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ca0590d621a8fd0bb16855593ec7aa1a43dd3f5cbeab09fc15524c20ed2a4f`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c42837a740b33ee79a0dce997a8890719b42fb8983d80880b7dc711c26b63d`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 5.6 MB (5584567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c84840421fc2932ed7fc419b920bb76552acdc93cf1f503f5de9ecdc6933750`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad350f0e865bb8da2f7a450f0b57ff622e290ac3621cff158b4fa2c0c2de22c`  
		Last Modified: Wed, 22 Apr 2026 02:17:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:ee0717b32090e6ea950cc06ea270b71a8c63f09983c60bbee4b7585f217e6a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41537f87b8289ede8bd21a4a0bc0e3582af61d1aa3ca9207aab388dd397eda3a`

```dockerfile
```

-	Layers:
	-	`sha256:d1540387f53a59551e2a390fe3f53e3c532260ee888cedba47ad3cfaeabfd8b1`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acba014320a761b4346330d8f6d015a8b553e0d6fffb49bf6ee42f168f8db01f`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f4d2c7ba22fbdd4c39d643fc06400642b6d479a7dfc684a3939b41bd69392c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36379770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b678a615cd6adb58ebf5f146ff8d89909b5200fed70f6093a1252adb559d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:36:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:37:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:37:14 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:37:14 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:37:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:37:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68b1d288c6fda5c3d291b76142d35c7ec90bba49f2f7e249984ab5030b2a8a`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72258c478f2f0cacc665dd483d41ad5142247c03f899d55173f931b7e1127ccd`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff059afbb00a8d0c47938a8cd83a2cb69138df7c613c1ff73877639d5839980`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 6.2 MB (6233755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3566292154189efcb23707ad78ae15514dc0e956d1fb5b4f10ca4fe927840`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290e4c2f5ef9aaf2f014d15a44512a40b25b7bc0cac6db9b8ae073550aadfd21`  
		Last Modified: Fri, 08 May 2026 19:37:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b8025f0910028dd9817f393058197a8d68cf5196c0a4e130126c5b48c10cb344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ab8802b871f6dee336412a2abb98089de33fd8aaab9762c3cda2637371d0f2`

```dockerfile
```

-	Layers:
	-	`sha256:1778e062fea4855a339744af921af7d4db3810975c7e16ccd96cf39b1c6b1c2c`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5180c5ea69da7069bfd3b17dcadb7c91742ce10c5bb6bedca95126234abc14a7`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:a5a42b31c5133e64d03f5a1b023ee8d27a65307ee447e6c38d72f9cc58a69dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37740931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517dcd55889daad945724e78840508a57f4309eb60f7ac48ae3e1fd811ded477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 01:42:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 01:42:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 01:42:38 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 01:42:38 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aca6cb7748c68cb25492fc9f24d7346509f08daab07852187997f5ec83a17`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac35082291b9c1a69c7516c860296f3f63b00268d97bb3318b375aa7c6e218`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c774ae6d18e11f6370e728ab01c1d87ca3d68bc6588743766f2b410cb763d96`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 6.4 MB (6442237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfb397ca7fc0085e5a145933ae46d485e5ce1ccb26ddbd354479221999788d3`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8607271c493cf7697bd03deb4ca4dbfcc0bf3ac55d61e8713977ef73d03df5`  
		Last Modified: Wed, 22 Apr 2026 01:42:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:3baf1644c67233842338f1d079882c89f34e0e2f0f8f84b79cdc47157827753e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d28367327b2843b2ec92143d178c6a8a51fa102072a88cb902f253539f42bb`

```dockerfile
```

-	Layers:
	-	`sha256:5c6cf5a178a57a0b0343af5d1335e683c16678501f7d68da3537e480e6791951`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0617f04db6a5465841cac97c304341518b612bb2fb1a516a809a02e779d9994a`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:fb2e82a303c6437dde676fa9c556b3600b2cdc7a5e46e19f152e81e5dcc0f36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1897646fdd9349183d12ff126cdfff37d385745dbc739a89f6192070bb64c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:36:47 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 03:36:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:37:49 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 03:37:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 03:37:49 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 03:37:49 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 03:37:50 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 03:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 03:37:50 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7133018187518174bce13421d93aab7d9276fdbb69c490faa8b0ae4dd915be69`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69ca05c79ecee8f52da5603e09290cc97f59f47547a0118206125ada7ffb118`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f362f773d738a0f6c8a9577379a42baa3a6a6ec4e705aa022b87cbe05ec796d`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 6.8 MB (6840643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce985e16ab67f426410c46f9b52b9521c468c6920d27e53c9149213439e7fa5f`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0dcef50dd0fbf39b2d4d37449d8581150d42d9007f0786e4391b4e8f1ef447`  
		Last Modified: Wed, 22 Apr 2026 03:38:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:de14cc2fcdb7dd56234b4b059a2ebac8ab8098ee3f63a2116aa8807058d5f44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e1dc9be890f0321945d897b84572fa1cf0fdfa3c0fcef100e6932f69fb14fc`

```dockerfile
```

-	Layers:
	-	`sha256:e38d24758f530ffb8b0e868d26eb42289904324921b249a7a4130a3b1fe4ed16`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f376bdb6254bdd4e959421b91495c5b0cdbe2185b945455eeec0fdb3994221`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:4b71cf53987a9707a16131c1318e249b3fd3d6ce9a82cb42cc7f49e072e18fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37638423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a4b86552c1e9439f4f551a02d1d47a8a09b1564576e2077689ea60ed92ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 16:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 23 Apr 2026 16:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 23 Apr 2026 16:12:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
VOLUME [/spiped]
# Thu, 23 Apr 2026 16:12:07 GMT
WORKDIR /spiped
# Thu, 23 Apr 2026 16:12:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 16:12:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 16:12:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3fe48b86e812e3913e5d13d1a9629869d202426b9c61e1715fa21c49eefb0`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34a84840c5fe62bd145180a478a04eb839e8ebc46151483b24496cb9f4a91f`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d24129e4ff9e3418ef7a713edd9546c25c9b66ed26f8d5aa09e53f0c443a147`  
		Last Modified: Thu, 23 Apr 2026 16:13:23 GMT  
		Size: 9.4 MB (9355868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9de411851378c843f1fa5367128062cec83a39214793d042c62249d045708d`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45064277bc4d512497c03c09b867eecba1e9f36520600b1b7cf50ccf931c314`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:8f1fdb09a20e86779bcd22247e4e7dc45779eadf380ed22541529e1f7c49f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30611531e32494ce7228fad7644d17d3b521a5eb65e2cab640541ec507a3ccff`

```dockerfile
```

-	Layers:
	-	`sha256:28e7945cedc25231eedc0925db8b02ae1dfc5c3c41f66ebd1d3a8ef39e217551`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3f06dd63e825c9c98e9b4bfdc4f7087ec431640aee8976c15796ae26a216eb`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:019df0384f80e6004366c1482c1a614e1840ece9ddd6e99f1d6bb7ce37049ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35964050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2664081e57843cec9f0abdb42b2f77fbcff9c6301724ad452dfb66ef5c07b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:31:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:31:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:31:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:31:27 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:31:27 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:31:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c273de4662c09d441d0991d3d1cad27add170f42a58b680c85262c0783bdb0b3`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819848a163b2883ddd6e28cee23ce28b8e14b9b83d1e88475875d55c72185cde`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173a50efe24c4e4255e01d86628f8813bed0b1f4dea66438798d4c154ca4af00`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 6.1 MB (6121383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358262f84455a81b0386d68dfa7aaf68b3631255c9bcacc7d9a9391c7ef41e6`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367fe4dffeb063a80c231a46e76b12ba5555c5ca56bff7bd52e453ad07e0a15`  
		Last Modified: Wed, 22 Apr 2026 02:31:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:d96cd204f455c5dc272e462fd8e316e5a97c0504452f2c27d6ac7530e72a0ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b22090b5ebb684acefa119a6124cb7ae2cba0c11749e40e357bc7e2091a88a`

```dockerfile
```

-	Layers:
	-	`sha256:0b1762ce516402255cd017adeca5b00cc772560a4f5608adf1b1827327879424`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07989d6af49ab13c5428e2cd294f3458939a021ba915616b8dd5dfc2fdcd4d8c`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:10785aa58079387363e472d7e20eb96bd01f12b9850476a066e124d57be1a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:6a78a135961dde77e0a3e9171928717694804d7cfb3d6aedbebfadb42bf4f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f599634d068048f3fcd01d27356e8cc57fb8937f8bbf03cfccaebddd3b1e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:35 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:14:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:14:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:14:45 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:14:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09629d4032ef7ab1ef9db974170b9cf0e98f6c5d68cb9f3d0e21a37889d50030`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad68e6c6d9b805cb5d27e526a335f55ae1e22e51fb78ed5cd842984966ec752`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097cdb4e276728ffaa69c00b45edf54d761118176e68ef12d68092b7417f986`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 107.6 KB (107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc806c3d4f80593516df4d73efec6cd1cf16dfd200d5fd6adda41910072975`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d250500ebc740f642b6509ef0a3f0576fe4b93cb687a514ceede64292cd717f`  
		Last Modified: Fri, 17 Apr 2026 00:14:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dcf1f88cd35b0648a36b53371be8057efc788150c247273946f22f226c8922f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695771cd59164f79af4e3d51a194af63f71274fa2ca45642700481f66706680`

```dockerfile
```

-	Layers:
	-	`sha256:9047c6064b6fcd9efa90aa0c959722cd5d0677dd3e15d576484c71664c66a025`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ebf9604f23105cb6660c6767d301a937a4b9d6d85433f32e35ffb2ba1e86d8`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:e61a3952e5718375c379136684659c21136328808a6c3f88e9585943251e9a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c576e8f7269c2ef4826f92b4a22494225a6cd470d17d9f30f01d9cc229e696f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:28:10 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:28:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:28:20 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:28:20 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28595f303e8390d8534900bd78b38647a907732d3d3e842c7b3a9caf747dfa`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2d882259c543692d98198b2c8f098f64b95d9b8018fbe3daf4bce16ccdea8`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 7.9 KB (7941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750bf6b03a38c9f5493952dd7c83dba844fa70e86926b54303c228f996e864fb`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 89.2 KB (89153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0b56fb727ea9f7a3dad23a396c81b60139284396a263e6658329c844b5dad`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6b266845306bbbcbee6801a12889b7c152b510808934deb45a090cedc3a06`  
		Last Modified: Fri, 17 Apr 2026 00:28:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e8ab0469cf1a0658dd7f777f120002189b116eedc60e2d13004809373539fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbd38bcf39cf976d74f4ea0d61a864e9b890815035438f477a99caff10eae99`

```dockerfile
```

-	Layers:
	-	`sha256:acf29d68d1e7fa30dc5742c4211ffe81430df68660be1f3d0207d5a94d98bc39`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:147fe0124aa237fa168a69becb6a2db57f4a9ad7144beb44a52a7735a75ed88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3316848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fac8ff5e55f7bb423942ebc9a0dcfe62ab45560df8acbf81f20fce40adfb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:13:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:13:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:13:54 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:13:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48112adbff0844ea29be59655ce36bdc68db268960b43349a213160861be5b`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b71c7a3ae36749950f95514df7064116e47fac5d0e8f2b2a7465a08ec730b1`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc42fa35611c27c8478a77677c7599958f859178a2ae432cdeea23ff283fe`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 81.7 KB (81682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17f9759dca0bc64327214acbd9fd3deb78375c7afd7010e30d54ffe9eafdb6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eff9de0017984f4c4aceb50f22ba5600d01062af116b4a3d8666f104982e79`  
		Last Modified: Fri, 17 Apr 2026 00:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:87b16d20b49f4fd531d2a7882ebf70ab433c78455a68ecb63229df2b111b80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db1828da7718e04747ebb0f602b5974b0a7a0da76481d2a933ecbb6b1869fd9`

```dockerfile
```

-	Layers:
	-	`sha256:32fd82b374cd8966ecaddf73d35913d341f1bf089acec4758b0eddc9ae15bf6c`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451cb443bac28fadec04af355b08de89c30845228bcead9735b3be6a627381f6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1fd688a89197aa9ec5aa2ecf456f856d56b46639e5d0733ee167c8e1f1f67c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e3a3494482e2c117fe69680a253048739b96db6b666e0ba693d69f12f3cffa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:30 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:23:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:23:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:23:40 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:23:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b70cf46309ade34c5a66991fc83a20e95c2a2ca7662393d07532b98169b897`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5fdf2c2bb57fb12d420f1ebc379b73a6a07a076dd649edbdfb2ec65e9b52f`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bde94e8b5d108bfaf26624adc0087452e38a2a8176cc98ece876fe2117fc72`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 100.6 KB (100601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b88c8155b1bdcaf3ceb67be1cd60eac4d053dbde4189b58b41e709ce71a5d`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb330bcfc9ca5ba0cfa2155b2866b977ad2c3ce1d9ae151d07e639bbada8ed2`  
		Last Modified: Fri, 17 Apr 2026 00:23:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fc73de67fe7f5bcda008d343140166980bf4176b3096a535d83f3dcd2d534e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a18fe2b2319a581866e1c86ace119888f0e7b9a60b55a3ce6b779f28fe92710`

```dockerfile
```

-	Layers:
	-	`sha256:a96c2085f2ac76644e77254bfa9bf6d1b56c67d9d9405eaa8416f74fcba97701`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d5f7f4737f85a0e24460592078844c64dafe02803bdf87581c20f597e952bb`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:60c2f83afdec0385615a7286994daa8f205766ef71d83fa8ddc2e700ac81936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc7573391c8c621e1b2f987722ca168aebbe555b0499e62e86738da10c96e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:54:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 05:54:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 05:55:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 05:55:09 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 05:55:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 05:55:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f934ad8efa54d7383ed1d7daf8f07d69a316c785b55e29d855f59724767ac5`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad6a50d64bebedb5b11ecc9dbad14debf2baa30235c5ed093775151dd20c5f`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9ad205a738e9a190290cb841b91a7516b90d39ccefc8a464803a80e5d3bf2`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 120.1 KB (120105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13bce07410da4d5d2d2271580461ed3ae19008e5249df3c1003a06c213c180b`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d30a682d686a1255ac7f31b311acf6f01b819da6af05a18bb59cf9285441247`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:499b7ec7b9c4e4eec426321c8934ac7fac003aeff1b6247ccf002c546cd6a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072722cf70bdbdd1bd5420a6744bc8ca176440a12571a40e33ce18862067a55`

```dockerfile
```

-	Layers:
	-	`sha256:dd1f08b2c21c938da19a9533a1b9dcb5f15e078dab41c9a4bd4ab244cd979858`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517f76f905b9dca96e65eec9ad79a6211e1b541723537e827a226d4839aa2649`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:cd9ed7a248ccd86ed221ed62ccb5fccc85d88f92bb07eacf32a54aa285d3baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b17425a87a9b3f6cf310b87ae46b1234772bd0b80ea164489da909a148229e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 01:13:49 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 01:14:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 01:14:15 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 01:14:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4eb2b31b373fa4117e61ee4973c717af31bc2e3376684ddf64780f6a0cfbf2`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5bc892fe10dffc5824aa6f02e4a3fd2d8872fcc548dc32d8271fbeda871d54`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f69169c64986eaf44f560100f0ace1b79586cff5d1f517fcf6f2810fcf476`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 112.7 KB (112676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc1153f644e2e26a00aa90bf9b03917ab7f9ec331b32bd9bc295281cee7151`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94785087e434424ecd2b2a79b34d04d7aa53bdc943265138216cadd6badf5495`  
		Last Modified: Fri, 17 Apr 2026 01:14:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:42b060f58ef29347aa95f2a95a49a750c85e6dc1283a7429bdbd08cbb35d8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeddc4f5e06133647f4d77b87d5471240c741e9ac4581ee0469cd5e684bde41`

```dockerfile
```

-	Layers:
	-	`sha256:8054970ddb854b9dbe87ad8cc6cb52f8ac69bae6393895a2cc0ec179d9890648`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf789792086c7df442c741fa726e1c634b400a002527085dcc36c87a5bdd724`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eaf86ffaae6edde3dcb5bc958a07fa09bfe7cf9bcd05be9ace676e83efe5f761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508a25834d52056b9c731fc2100ea35e54d563c093104a90eef8c05cb0cd1cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 03:43:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Apr 2026 03:43:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 19 Apr 2026 03:45:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
VOLUME [/spiped]
# Sun, 19 Apr 2026 03:45:16 GMT
WORKDIR /spiped
# Sun, 19 Apr 2026 03:45:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Apr 2026 03:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Apr 2026 03:45:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6ee73726995fef9f6ea4faf4767bcea48e04bfd71f1eea0bd05f9534d43f8`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dd3bcf1d4c6316b374da1b2790b7de4b60cf8e6512e5f30f8d7b2d7a3b38`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e66ca15c2a84ed0ad5aac95f1257383ec006115c07282942c1fd6f06bc2b26`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a854d7ad8f0e7a7a6274e5c362b1a896bd76e462c14408778ba02dff83d37b`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff5f61469b0ef7c1c8bf56662d9b762181e909bc3c749eacbaaecf7bb475ab`  
		Last Modified: Sun, 19 Apr 2026 03:45:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f21b45950838bc0c80c8410cc4f2814b68f96ecad1e19be90b06994c99afbf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abe71f567ae68daf6e6dfeaafd74f8104d7a6958082dd986f64838b44c12b9f`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4f6fe1bacdcf68608f4eb99bf2115bae97f39b1056b72d36c08b63e32ef42`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e5c1e0a1d68c8bdb360c97f9072a3c973409b2f9afe7ff5795d523cae5119b`  
		Last Modified: Sun, 19 Apr 2026 03:45:38 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:d63a333156f14c550016968b48b61e03d6ffa7cdadeb4dc11994993be83c667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f883e0aba651c328e78b42abc6210940d11022f1ee5d1ff5258ebca42e51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:11 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:41:12 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:41:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:41:19 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:41:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:41:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5658f716398e67bcdf451aa62d9268badc01207fb2761dde286827e782131`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d837fc0069a0ae8449bb0adb9f65b43fff5ff059948bf845ea728a30d3eaca0`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f2f936af1acb505aa131fbad0547df0d36ff3dc9c4f8c3a396c9877b87798`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.9 KB (96930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33930e4a86d8157d355b84eecf720d4f20b38ee3502ab3baa6329d6c6acac811`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27970db5cca98e64b9bdffc3b4445e18a503e3e0dc858c6ae91eff10bccd50bd`  
		Last Modified: Fri, 17 Apr 2026 00:41:29 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3a63421a60ad516e8ae99df7c008ce97158220da99f3e592d9090f762eb254c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ae27771b3c7505fb78b0f0546a7416b11e879220de4dc6090bf643dedf8614`

```dockerfile
```

-	Layers:
	-	`sha256:c6abf9efd631a7212221f0b771ec35e734885be3d3a6755a004bba8bd46cc068`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033e56e9f47fa0453060710502d5ab3daddcba0cc4e51e5e138a57faf3e873d6`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:3b6ac3e45f172915009c7662a28b4462f14812bdaa14d3256155618d0262ca50
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:3697a0c4441ffdebbc45026e68caef4b180d0435c04825aea8683826608b6a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36830248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7651265801ee07aaa82006e38d9ac3f69a351f0133ed076c95fac3c4070b5869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:34:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 01:34:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 01:34:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 01:34:47 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 01:34:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:34:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9b6c12ee3ac5c9fd735735d76164bc3226971d664e3cf1cde43f281aac222f`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c82eb68b5775c3e49cf91b695f5b281d5635a64d68a48d315ad05b5c25c423a`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6541376dd96a6fc09591396c5ee3d29921d988f4bf5c8ce27b07276d38546423`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 7.0 MB (7047707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffaa1a14fd226e56da74302eab175251416360e90c228fd94dade206c9d78c9`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5303c4f9d1890510b3fa6ddd08d126352bdc1920a3c7c4ce5f8238ef9f18db`  
		Last Modified: Wed, 22 Apr 2026 01:34:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:d0c6471bc8d160d5788eb73aea715f40a47deb73ce301ef156c476a711c3efd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce174c86dade55ce31b891e3eb31393c052de868272c4047ea5f570c54a06c6d`

```dockerfile
```

-	Layers:
	-	`sha256:4cb9cddb67663afe5f2c1f31b7b70b74b000c8330a998fe3c01e31047495cea6`  
		Last Modified: Wed, 22 Apr 2026 01:34:54 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b2345e28b73fe57e118cead927bed244d50e3bd5ce1d6cec6d4134ab93184f`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:58a9096e9da905bf9e7530a00b0386ae545910541ba7636134b7f325a3dabccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d21b5f45c11b35928dffe02224e155b54d9ab4a072b30193e228c96092ef243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:15:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:16:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:16:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:16:28 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:16:28 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:16:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4794e1957b3cf639e20aa4a0d33a68c0170d04be31dfa0d1e3032edec682050`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506884dd4194f6c16e334d33decb7e25face9b3cf73131bf09e3a676569f278c`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ddf0bad83cb62e304347253656f7c58364f61c63151f32241919af173cab8d`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 5.8 MB (5789064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e465e59da14247ef0cbca66c2a5502e3a48bce76072d98ea60321006753a2b20`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cd1db1a45425ed24b69890f937f29324664c3ad90bbd4a1103a1e5c7a59527`  
		Last Modified: Wed, 22 Apr 2026 02:16:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:9710231581fc8bd5e10a24a668c5f93c84658a05f2489c9e329561f21aef8ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f876370a99391838ecfc8b380afcf44edfdb92b7866cc035577e33d97017db`

```dockerfile
```

-	Layers:
	-	`sha256:0fc5644cca517238d76d5f7971f9b147255edf3e7f6eda96e7449b4d72ecbe70`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bffcc7d5d03f329eed1cbe5f2ef5ae347e4005ac12647f80dff37b77315c0b8`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:c4e99b1c150ce516a4f8bfd06f5ce36db9619da989d63041e2e3ed867e16d9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31801768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eee37b96c47b6d13903255f49ebefb808aad92497750349796120f32c768530`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:17:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:17:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:17:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:17:41 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:17:41 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:17:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac891b940103b402884a868ba78e5b89adc92b82368d5cde3f77372c4d9389ba`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ca0590d621a8fd0bb16855593ec7aa1a43dd3f5cbeab09fc15524c20ed2a4f`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c42837a740b33ee79a0dce997a8890719b42fb8983d80880b7dc711c26b63d`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 5.6 MB (5584567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c84840421fc2932ed7fc419b920bb76552acdc93cf1f503f5de9ecdc6933750`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad350f0e865bb8da2f7a450f0b57ff622e290ac3621cff158b4fa2c0c2de22c`  
		Last Modified: Wed, 22 Apr 2026 02:17:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:ee0717b32090e6ea950cc06ea270b71a8c63f09983c60bbee4b7585f217e6a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41537f87b8289ede8bd21a4a0bc0e3582af61d1aa3ca9207aab388dd397eda3a`

```dockerfile
```

-	Layers:
	-	`sha256:d1540387f53a59551e2a390fe3f53e3c532260ee888cedba47ad3cfaeabfd8b1`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acba014320a761b4346330d8f6d015a8b553e0d6fffb49bf6ee42f168f8db01f`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f4d2c7ba22fbdd4c39d643fc06400642b6d479a7dfc684a3939b41bd69392c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36379770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b678a615cd6adb58ebf5f146ff8d89909b5200fed70f6093a1252adb559d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:36:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:37:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:37:14 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:37:14 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:37:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:37:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68b1d288c6fda5c3d291b76142d35c7ec90bba49f2f7e249984ab5030b2a8a`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72258c478f2f0cacc665dd483d41ad5142247c03f899d55173f931b7e1127ccd`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff059afbb00a8d0c47938a8cd83a2cb69138df7c613c1ff73877639d5839980`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 6.2 MB (6233755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3566292154189efcb23707ad78ae15514dc0e956d1fb5b4f10ca4fe927840`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290e4c2f5ef9aaf2f014d15a44512a40b25b7bc0cac6db9b8ae073550aadfd21`  
		Last Modified: Fri, 08 May 2026 19:37:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b8025f0910028dd9817f393058197a8d68cf5196c0a4e130126c5b48c10cb344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ab8802b871f6dee336412a2abb98089de33fd8aaab9762c3cda2637371d0f2`

```dockerfile
```

-	Layers:
	-	`sha256:1778e062fea4855a339744af921af7d4db3810975c7e16ccd96cf39b1c6b1c2c`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5180c5ea69da7069bfd3b17dcadb7c91742ce10c5bb6bedca95126234abc14a7`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:a5a42b31c5133e64d03f5a1b023ee8d27a65307ee447e6c38d72f9cc58a69dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37740931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517dcd55889daad945724e78840508a57f4309eb60f7ac48ae3e1fd811ded477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 01:42:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 01:42:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 01:42:38 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 01:42:38 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aca6cb7748c68cb25492fc9f24d7346509f08daab07852187997f5ec83a17`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac35082291b9c1a69c7516c860296f3f63b00268d97bb3318b375aa7c6e218`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c774ae6d18e11f6370e728ab01c1d87ca3d68bc6588743766f2b410cb763d96`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 6.4 MB (6442237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfb397ca7fc0085e5a145933ae46d485e5ce1ccb26ddbd354479221999788d3`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8607271c493cf7697bd03deb4ca4dbfcc0bf3ac55d61e8713977ef73d03df5`  
		Last Modified: Wed, 22 Apr 2026 01:42:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:3baf1644c67233842338f1d079882c89f34e0e2f0f8f84b79cdc47157827753e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d28367327b2843b2ec92143d178c6a8a51fa102072a88cb902f253539f42bb`

```dockerfile
```

-	Layers:
	-	`sha256:5c6cf5a178a57a0b0343af5d1335e683c16678501f7d68da3537e480e6791951`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0617f04db6a5465841cac97c304341518b612bb2fb1a516a809a02e779d9994a`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:fb2e82a303c6437dde676fa9c556b3600b2cdc7a5e46e19f152e81e5dcc0f36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1897646fdd9349183d12ff126cdfff37d385745dbc739a89f6192070bb64c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:36:47 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 03:36:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:37:49 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 03:37:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 03:37:49 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 03:37:49 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 03:37:50 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 03:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 03:37:50 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7133018187518174bce13421d93aab7d9276fdbb69c490faa8b0ae4dd915be69`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69ca05c79ecee8f52da5603e09290cc97f59f47547a0118206125ada7ffb118`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f362f773d738a0f6c8a9577379a42baa3a6a6ec4e705aa022b87cbe05ec796d`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 6.8 MB (6840643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce985e16ab67f426410c46f9b52b9521c468c6920d27e53c9149213439e7fa5f`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0dcef50dd0fbf39b2d4d37449d8581150d42d9007f0786e4391b4e8f1ef447`  
		Last Modified: Wed, 22 Apr 2026 03:38:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:de14cc2fcdb7dd56234b4b059a2ebac8ab8098ee3f63a2116aa8807058d5f44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e1dc9be890f0321945d897b84572fa1cf0fdfa3c0fcef100e6932f69fb14fc`

```dockerfile
```

-	Layers:
	-	`sha256:e38d24758f530ffb8b0e868d26eb42289904324921b249a7a4130a3b1fe4ed16`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f376bdb6254bdd4e959421b91495c5b0cdbe2185b945455eeec0fdb3994221`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:4b71cf53987a9707a16131c1318e249b3fd3d6ce9a82cb42cc7f49e072e18fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37638423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a4b86552c1e9439f4f551a02d1d47a8a09b1564576e2077689ea60ed92ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 16:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 23 Apr 2026 16:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 23 Apr 2026 16:12:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
VOLUME [/spiped]
# Thu, 23 Apr 2026 16:12:07 GMT
WORKDIR /spiped
# Thu, 23 Apr 2026 16:12:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 16:12:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 16:12:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3fe48b86e812e3913e5d13d1a9629869d202426b9c61e1715fa21c49eefb0`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34a84840c5fe62bd145180a478a04eb839e8ebc46151483b24496cb9f4a91f`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d24129e4ff9e3418ef7a713edd9546c25c9b66ed26f8d5aa09e53f0c443a147`  
		Last Modified: Thu, 23 Apr 2026 16:13:23 GMT  
		Size: 9.4 MB (9355868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9de411851378c843f1fa5367128062cec83a39214793d042c62249d045708d`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45064277bc4d512497c03c09b867eecba1e9f36520600b1b7cf50ccf931c314`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:8f1fdb09a20e86779bcd22247e4e7dc45779eadf380ed22541529e1f7c49f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30611531e32494ce7228fad7644d17d3b521a5eb65e2cab640541ec507a3ccff`

```dockerfile
```

-	Layers:
	-	`sha256:28e7945cedc25231eedc0925db8b02ae1dfc5c3c41f66ebd1d3a8ef39e217551`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3f06dd63e825c9c98e9b4bfdc4f7087ec431640aee8976c15796ae26a216eb`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:019df0384f80e6004366c1482c1a614e1840ece9ddd6e99f1d6bb7ce37049ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35964050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2664081e57843cec9f0abdb42b2f77fbcff9c6301724ad452dfb66ef5c07b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:31:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:31:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:31:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:31:27 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:31:27 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:31:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c273de4662c09d441d0991d3d1cad27add170f42a58b680c85262c0783bdb0b3`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819848a163b2883ddd6e28cee23ce28b8e14b9b83d1e88475875d55c72185cde`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173a50efe24c4e4255e01d86628f8813bed0b1f4dea66438798d4c154ca4af00`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 6.1 MB (6121383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358262f84455a81b0386d68dfa7aaf68b3631255c9bcacc7d9a9391c7ef41e6`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367fe4dffeb063a80c231a46e76b12ba5555c5ca56bff7bd52e453ad07e0a15`  
		Last Modified: Wed, 22 Apr 2026 02:31:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:d96cd204f455c5dc272e462fd8e316e5a97c0504452f2c27d6ac7530e72a0ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b22090b5ebb684acefa119a6124cb7ae2cba0c11749e40e357bc7e2091a88a`

```dockerfile
```

-	Layers:
	-	`sha256:0b1762ce516402255cd017adeca5b00cc772560a4f5608adf1b1827327879424`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07989d6af49ab13c5428e2cd294f3458939a021ba915616b8dd5dfc2fdcd4d8c`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:10785aa58079387363e472d7e20eb96bd01f12b9850476a066e124d57be1a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:6a78a135961dde77e0a3e9171928717694804d7cfb3d6aedbebfadb42bf4f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f599634d068048f3fcd01d27356e8cc57fb8937f8bbf03cfccaebddd3b1e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:35 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:14:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:14:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:14:45 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:14:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09629d4032ef7ab1ef9db974170b9cf0e98f6c5d68cb9f3d0e21a37889d50030`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad68e6c6d9b805cb5d27e526a335f55ae1e22e51fb78ed5cd842984966ec752`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097cdb4e276728ffaa69c00b45edf54d761118176e68ef12d68092b7417f986`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 107.6 KB (107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc806c3d4f80593516df4d73efec6cd1cf16dfd200d5fd6adda41910072975`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d250500ebc740f642b6509ef0a3f0576fe4b93cb687a514ceede64292cd717f`  
		Last Modified: Fri, 17 Apr 2026 00:14:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dcf1f88cd35b0648a36b53371be8057efc788150c247273946f22f226c8922f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695771cd59164f79af4e3d51a194af63f71274fa2ca45642700481f66706680`

```dockerfile
```

-	Layers:
	-	`sha256:9047c6064b6fcd9efa90aa0c959722cd5d0677dd3e15d576484c71664c66a025`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ebf9604f23105cb6660c6767d301a937a4b9d6d85433f32e35ffb2ba1e86d8`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:e61a3952e5718375c379136684659c21136328808a6c3f88e9585943251e9a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c576e8f7269c2ef4826f92b4a22494225a6cd470d17d9f30f01d9cc229e696f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:28:10 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:28:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:28:20 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:28:20 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28595f303e8390d8534900bd78b38647a907732d3d3e842c7b3a9caf747dfa`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2d882259c543692d98198b2c8f098f64b95d9b8018fbe3daf4bce16ccdea8`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 7.9 KB (7941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750bf6b03a38c9f5493952dd7c83dba844fa70e86926b54303c228f996e864fb`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 89.2 KB (89153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0b56fb727ea9f7a3dad23a396c81b60139284396a263e6658329c844b5dad`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6b266845306bbbcbee6801a12889b7c152b510808934deb45a090cedc3a06`  
		Last Modified: Fri, 17 Apr 2026 00:28:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e8ab0469cf1a0658dd7f777f120002189b116eedc60e2d13004809373539fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbd38bcf39cf976d74f4ea0d61a864e9b890815035438f477a99caff10eae99`

```dockerfile
```

-	Layers:
	-	`sha256:acf29d68d1e7fa30dc5742c4211ffe81430df68660be1f3d0207d5a94d98bc39`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:147fe0124aa237fa168a69becb6a2db57f4a9ad7144beb44a52a7735a75ed88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3316848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fac8ff5e55f7bb423942ebc9a0dcfe62ab45560df8acbf81f20fce40adfb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:13:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:13:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:13:54 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:13:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48112adbff0844ea29be59655ce36bdc68db268960b43349a213160861be5b`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b71c7a3ae36749950f95514df7064116e47fac5d0e8f2b2a7465a08ec730b1`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc42fa35611c27c8478a77677c7599958f859178a2ae432cdeea23ff283fe`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 81.7 KB (81682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17f9759dca0bc64327214acbd9fd3deb78375c7afd7010e30d54ffe9eafdb6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eff9de0017984f4c4aceb50f22ba5600d01062af116b4a3d8666f104982e79`  
		Last Modified: Fri, 17 Apr 2026 00:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:87b16d20b49f4fd531d2a7882ebf70ab433c78455a68ecb63229df2b111b80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db1828da7718e04747ebb0f602b5974b0a7a0da76481d2a933ecbb6b1869fd9`

```dockerfile
```

-	Layers:
	-	`sha256:32fd82b374cd8966ecaddf73d35913d341f1bf089acec4758b0eddc9ae15bf6c`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451cb443bac28fadec04af355b08de89c30845228bcead9735b3be6a627381f6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1fd688a89197aa9ec5aa2ecf456f856d56b46639e5d0733ee167c8e1f1f67c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e3a3494482e2c117fe69680a253048739b96db6b666e0ba693d69f12f3cffa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:30 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:23:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:23:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:23:40 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:23:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b70cf46309ade34c5a66991fc83a20e95c2a2ca7662393d07532b98169b897`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5fdf2c2bb57fb12d420f1ebc379b73a6a07a076dd649edbdfb2ec65e9b52f`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bde94e8b5d108bfaf26624adc0087452e38a2a8176cc98ece876fe2117fc72`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 100.6 KB (100601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b88c8155b1bdcaf3ceb67be1cd60eac4d053dbde4189b58b41e709ce71a5d`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb330bcfc9ca5ba0cfa2155b2866b977ad2c3ce1d9ae151d07e639bbada8ed2`  
		Last Modified: Fri, 17 Apr 2026 00:23:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fc73de67fe7f5bcda008d343140166980bf4176b3096a535d83f3dcd2d534e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a18fe2b2319a581866e1c86ace119888f0e7b9a60b55a3ce6b779f28fe92710`

```dockerfile
```

-	Layers:
	-	`sha256:a96c2085f2ac76644e77254bfa9bf6d1b56c67d9d9405eaa8416f74fcba97701`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d5f7f4737f85a0e24460592078844c64dafe02803bdf87581c20f597e952bb`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:60c2f83afdec0385615a7286994daa8f205766ef71d83fa8ddc2e700ac81936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc7573391c8c621e1b2f987722ca168aebbe555b0499e62e86738da10c96e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:54:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 05:54:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 05:55:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 05:55:09 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 05:55:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 05:55:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f934ad8efa54d7383ed1d7daf8f07d69a316c785b55e29d855f59724767ac5`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad6a50d64bebedb5b11ecc9dbad14debf2baa30235c5ed093775151dd20c5f`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9ad205a738e9a190290cb841b91a7516b90d39ccefc8a464803a80e5d3bf2`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 120.1 KB (120105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13bce07410da4d5d2d2271580461ed3ae19008e5249df3c1003a06c213c180b`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d30a682d686a1255ac7f31b311acf6f01b819da6af05a18bb59cf9285441247`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:499b7ec7b9c4e4eec426321c8934ac7fac003aeff1b6247ccf002c546cd6a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072722cf70bdbdd1bd5420a6744bc8ca176440a12571a40e33ce18862067a55`

```dockerfile
```

-	Layers:
	-	`sha256:dd1f08b2c21c938da19a9533a1b9dcb5f15e078dab41c9a4bd4ab244cd979858`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517f76f905b9dca96e65eec9ad79a6211e1b541723537e827a226d4839aa2649`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:cd9ed7a248ccd86ed221ed62ccb5fccc85d88f92bb07eacf32a54aa285d3baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b17425a87a9b3f6cf310b87ae46b1234772bd0b80ea164489da909a148229e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 01:13:49 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 01:14:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 01:14:15 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 01:14:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4eb2b31b373fa4117e61ee4973c717af31bc2e3376684ddf64780f6a0cfbf2`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5bc892fe10dffc5824aa6f02e4a3fd2d8872fcc548dc32d8271fbeda871d54`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f69169c64986eaf44f560100f0ace1b79586cff5d1f517fcf6f2810fcf476`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 112.7 KB (112676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc1153f644e2e26a00aa90bf9b03917ab7f9ec331b32bd9bc295281cee7151`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94785087e434424ecd2b2a79b34d04d7aa53bdc943265138216cadd6badf5495`  
		Last Modified: Fri, 17 Apr 2026 01:14:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:42b060f58ef29347aa95f2a95a49a750c85e6dc1283a7429bdbd08cbb35d8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeddc4f5e06133647f4d77b87d5471240c741e9ac4581ee0469cd5e684bde41`

```dockerfile
```

-	Layers:
	-	`sha256:8054970ddb854b9dbe87ad8cc6cb52f8ac69bae6393895a2cc0ec179d9890648`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf789792086c7df442c741fa726e1c634b400a002527085dcc36c87a5bdd724`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eaf86ffaae6edde3dcb5bc958a07fa09bfe7cf9bcd05be9ace676e83efe5f761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508a25834d52056b9c731fc2100ea35e54d563c093104a90eef8c05cb0cd1cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 03:43:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Apr 2026 03:43:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 19 Apr 2026 03:45:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
VOLUME [/spiped]
# Sun, 19 Apr 2026 03:45:16 GMT
WORKDIR /spiped
# Sun, 19 Apr 2026 03:45:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Apr 2026 03:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Apr 2026 03:45:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6ee73726995fef9f6ea4faf4767bcea48e04bfd71f1eea0bd05f9534d43f8`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dd3bcf1d4c6316b374da1b2790b7de4b60cf8e6512e5f30f8d7b2d7a3b38`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e66ca15c2a84ed0ad5aac95f1257383ec006115c07282942c1fd6f06bc2b26`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a854d7ad8f0e7a7a6274e5c362b1a896bd76e462c14408778ba02dff83d37b`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff5f61469b0ef7c1c8bf56662d9b762181e909bc3c749eacbaaecf7bb475ab`  
		Last Modified: Sun, 19 Apr 2026 03:45:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f21b45950838bc0c80c8410cc4f2814b68f96ecad1e19be90b06994c99afbf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abe71f567ae68daf6e6dfeaafd74f8104d7a6958082dd986f64838b44c12b9f`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4f6fe1bacdcf68608f4eb99bf2115bae97f39b1056b72d36c08b63e32ef42`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e5c1e0a1d68c8bdb360c97f9072a3c973409b2f9afe7ff5795d523cae5119b`  
		Last Modified: Sun, 19 Apr 2026 03:45:38 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:d63a333156f14c550016968b48b61e03d6ffa7cdadeb4dc11994993be83c667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f883e0aba651c328e78b42abc6210940d11022f1ee5d1ff5258ebca42e51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:11 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:41:12 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:41:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:41:19 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:41:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:41:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5658f716398e67bcdf451aa62d9268badc01207fb2761dde286827e782131`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d837fc0069a0ae8449bb0adb9f65b43fff5ff059948bf845ea728a30d3eaca0`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f2f936af1acb505aa131fbad0547df0d36ff3dc9c4f8c3a396c9877b87798`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.9 KB (96930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33930e4a86d8157d355b84eecf720d4f20b38ee3502ab3baa6329d6c6acac811`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27970db5cca98e64b9bdffc3b4445e18a503e3e0dc858c6ae91eff10bccd50bd`  
		Last Modified: Fri, 17 Apr 2026 00:41:29 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3a63421a60ad516e8ae99df7c008ce97158220da99f3e592d9090f762eb254c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ae27771b3c7505fb78b0f0546a7416b11e879220de4dc6090bf643dedf8614`

```dockerfile
```

-	Layers:
	-	`sha256:c6abf9efd631a7212221f0b771ec35e734885be3d3a6755a004bba8bd46cc068`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033e56e9f47fa0453060710502d5ab3daddcba0cc4e51e5e138a57faf3e873d6`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:3b6ac3e45f172915009c7662a28b4462f14812bdaa14d3256155618d0262ca50
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.4` - linux; amd64

```console
$ docker pull spiped@sha256:3697a0c4441ffdebbc45026e68caef4b180d0435c04825aea8683826608b6a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36830248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7651265801ee07aaa82006e38d9ac3f69a351f0133ed076c95fac3c4070b5869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:34:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 01:34:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 01:34:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 01:34:47 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 01:34:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:34:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9b6c12ee3ac5c9fd735735d76164bc3226971d664e3cf1cde43f281aac222f`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c82eb68b5775c3e49cf91b695f5b281d5635a64d68a48d315ad05b5c25c423a`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6541376dd96a6fc09591396c5ee3d29921d988f4bf5c8ce27b07276d38546423`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 7.0 MB (7047707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffaa1a14fd226e56da74302eab175251416360e90c228fd94dade206c9d78c9`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5303c4f9d1890510b3fa6ddd08d126352bdc1920a3c7c4ce5f8238ef9f18db`  
		Last Modified: Wed, 22 Apr 2026 01:34:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:d0c6471bc8d160d5788eb73aea715f40a47deb73ce301ef156c476a711c3efd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce174c86dade55ce31b891e3eb31393c052de868272c4047ea5f570c54a06c6d`

```dockerfile
```

-	Layers:
	-	`sha256:4cb9cddb67663afe5f2c1f31b7b70b74b000c8330a998fe3c01e31047495cea6`  
		Last Modified: Wed, 22 Apr 2026 01:34:54 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b2345e28b73fe57e118cead927bed244d50e3bd5ce1d6cec6d4134ab93184f`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:58a9096e9da905bf9e7530a00b0386ae545910541ba7636134b7f325a3dabccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d21b5f45c11b35928dffe02224e155b54d9ab4a072b30193e228c96092ef243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:15:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:16:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:16:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:16:28 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:16:28 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:16:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4794e1957b3cf639e20aa4a0d33a68c0170d04be31dfa0d1e3032edec682050`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506884dd4194f6c16e334d33decb7e25face9b3cf73131bf09e3a676569f278c`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ddf0bad83cb62e304347253656f7c58364f61c63151f32241919af173cab8d`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 5.8 MB (5789064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e465e59da14247ef0cbca66c2a5502e3a48bce76072d98ea60321006753a2b20`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cd1db1a45425ed24b69890f937f29324664c3ad90bbd4a1103a1e5c7a59527`  
		Last Modified: Wed, 22 Apr 2026 02:16:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:9710231581fc8bd5e10a24a668c5f93c84658a05f2489c9e329561f21aef8ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f876370a99391838ecfc8b380afcf44edfdb92b7866cc035577e33d97017db`

```dockerfile
```

-	Layers:
	-	`sha256:0fc5644cca517238d76d5f7971f9b147255edf3e7f6eda96e7449b4d72ecbe70`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bffcc7d5d03f329eed1cbe5f2ef5ae347e4005ac12647f80dff37b77315c0b8`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:c4e99b1c150ce516a4f8bfd06f5ce36db9619da989d63041e2e3ed867e16d9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31801768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eee37b96c47b6d13903255f49ebefb808aad92497750349796120f32c768530`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:17:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:17:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:17:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:17:41 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:17:41 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:17:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac891b940103b402884a868ba78e5b89adc92b82368d5cde3f77372c4d9389ba`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ca0590d621a8fd0bb16855593ec7aa1a43dd3f5cbeab09fc15524c20ed2a4f`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c42837a740b33ee79a0dce997a8890719b42fb8983d80880b7dc711c26b63d`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 5.6 MB (5584567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c84840421fc2932ed7fc419b920bb76552acdc93cf1f503f5de9ecdc6933750`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad350f0e865bb8da2f7a450f0b57ff622e290ac3621cff158b4fa2c0c2de22c`  
		Last Modified: Wed, 22 Apr 2026 02:17:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:ee0717b32090e6ea950cc06ea270b71a8c63f09983c60bbee4b7585f217e6a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41537f87b8289ede8bd21a4a0bc0e3582af61d1aa3ca9207aab388dd397eda3a`

```dockerfile
```

-	Layers:
	-	`sha256:d1540387f53a59551e2a390fe3f53e3c532260ee888cedba47ad3cfaeabfd8b1`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acba014320a761b4346330d8f6d015a8b553e0d6fffb49bf6ee42f168f8db01f`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f4d2c7ba22fbdd4c39d643fc06400642b6d479a7dfc684a3939b41bd69392c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36379770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b678a615cd6adb58ebf5f146ff8d89909b5200fed70f6093a1252adb559d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:36:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:37:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:37:14 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:37:14 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:37:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:37:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68b1d288c6fda5c3d291b76142d35c7ec90bba49f2f7e249984ab5030b2a8a`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72258c478f2f0cacc665dd483d41ad5142247c03f899d55173f931b7e1127ccd`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff059afbb00a8d0c47938a8cd83a2cb69138df7c613c1ff73877639d5839980`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 6.2 MB (6233755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3566292154189efcb23707ad78ae15514dc0e956d1fb5b4f10ca4fe927840`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290e4c2f5ef9aaf2f014d15a44512a40b25b7bc0cac6db9b8ae073550aadfd21`  
		Last Modified: Fri, 08 May 2026 19:37:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b8025f0910028dd9817f393058197a8d68cf5196c0a4e130126c5b48c10cb344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ab8802b871f6dee336412a2abb98089de33fd8aaab9762c3cda2637371d0f2`

```dockerfile
```

-	Layers:
	-	`sha256:1778e062fea4855a339744af921af7d4db3810975c7e16ccd96cf39b1c6b1c2c`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5180c5ea69da7069bfd3b17dcadb7c91742ce10c5bb6bedca95126234abc14a7`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:a5a42b31c5133e64d03f5a1b023ee8d27a65307ee447e6c38d72f9cc58a69dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37740931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517dcd55889daad945724e78840508a57f4309eb60f7ac48ae3e1fd811ded477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 01:42:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 01:42:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 01:42:38 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 01:42:38 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aca6cb7748c68cb25492fc9f24d7346509f08daab07852187997f5ec83a17`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac35082291b9c1a69c7516c860296f3f63b00268d97bb3318b375aa7c6e218`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c774ae6d18e11f6370e728ab01c1d87ca3d68bc6588743766f2b410cb763d96`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 6.4 MB (6442237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfb397ca7fc0085e5a145933ae46d485e5ce1ccb26ddbd354479221999788d3`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8607271c493cf7697bd03deb4ca4dbfcc0bf3ac55d61e8713977ef73d03df5`  
		Last Modified: Wed, 22 Apr 2026 01:42:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:3baf1644c67233842338f1d079882c89f34e0e2f0f8f84b79cdc47157827753e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d28367327b2843b2ec92143d178c6a8a51fa102072a88cb902f253539f42bb`

```dockerfile
```

-	Layers:
	-	`sha256:5c6cf5a178a57a0b0343af5d1335e683c16678501f7d68da3537e480e6791951`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0617f04db6a5465841cac97c304341518b612bb2fb1a516a809a02e779d9994a`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:fb2e82a303c6437dde676fa9c556b3600b2cdc7a5e46e19f152e81e5dcc0f36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1897646fdd9349183d12ff126cdfff37d385745dbc739a89f6192070bb64c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:36:47 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 03:36:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:37:49 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 03:37:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 03:37:49 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 03:37:49 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 03:37:50 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 03:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 03:37:50 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7133018187518174bce13421d93aab7d9276fdbb69c490faa8b0ae4dd915be69`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69ca05c79ecee8f52da5603e09290cc97f59f47547a0118206125ada7ffb118`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f362f773d738a0f6c8a9577379a42baa3a6a6ec4e705aa022b87cbe05ec796d`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 6.8 MB (6840643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce985e16ab67f426410c46f9b52b9521c468c6920d27e53c9149213439e7fa5f`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0dcef50dd0fbf39b2d4d37449d8581150d42d9007f0786e4391b4e8f1ef447`  
		Last Modified: Wed, 22 Apr 2026 03:38:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:de14cc2fcdb7dd56234b4b059a2ebac8ab8098ee3f63a2116aa8807058d5f44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e1dc9be890f0321945d897b84572fa1cf0fdfa3c0fcef100e6932f69fb14fc`

```dockerfile
```

-	Layers:
	-	`sha256:e38d24758f530ffb8b0e868d26eb42289904324921b249a7a4130a3b1fe4ed16`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f376bdb6254bdd4e959421b91495c5b0cdbe2185b945455eeec0fdb3994221`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:4b71cf53987a9707a16131c1318e249b3fd3d6ce9a82cb42cc7f49e072e18fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37638423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a4b86552c1e9439f4f551a02d1d47a8a09b1564576e2077689ea60ed92ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 16:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 23 Apr 2026 16:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 23 Apr 2026 16:12:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
VOLUME [/spiped]
# Thu, 23 Apr 2026 16:12:07 GMT
WORKDIR /spiped
# Thu, 23 Apr 2026 16:12:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 16:12:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 16:12:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3fe48b86e812e3913e5d13d1a9629869d202426b9c61e1715fa21c49eefb0`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34a84840c5fe62bd145180a478a04eb839e8ebc46151483b24496cb9f4a91f`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d24129e4ff9e3418ef7a713edd9546c25c9b66ed26f8d5aa09e53f0c443a147`  
		Last Modified: Thu, 23 Apr 2026 16:13:23 GMT  
		Size: 9.4 MB (9355868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9de411851378c843f1fa5367128062cec83a39214793d042c62249d045708d`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45064277bc4d512497c03c09b867eecba1e9f36520600b1b7cf50ccf931c314`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:8f1fdb09a20e86779bcd22247e4e7dc45779eadf380ed22541529e1f7c49f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30611531e32494ce7228fad7644d17d3b521a5eb65e2cab640541ec507a3ccff`

```dockerfile
```

-	Layers:
	-	`sha256:28e7945cedc25231eedc0925db8b02ae1dfc5c3c41f66ebd1d3a8ef39e217551`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3f06dd63e825c9c98e9b4bfdc4f7087ec431640aee8976c15796ae26a216eb`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:019df0384f80e6004366c1482c1a614e1840ece9ddd6e99f1d6bb7ce37049ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35964050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2664081e57843cec9f0abdb42b2f77fbcff9c6301724ad452dfb66ef5c07b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:31:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:31:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:31:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:31:27 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:31:27 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:31:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c273de4662c09d441d0991d3d1cad27add170f42a58b680c85262c0783bdb0b3`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819848a163b2883ddd6e28cee23ce28b8e14b9b83d1e88475875d55c72185cde`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173a50efe24c4e4255e01d86628f8813bed0b1f4dea66438798d4c154ca4af00`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 6.1 MB (6121383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358262f84455a81b0386d68dfa7aaf68b3631255c9bcacc7d9a9391c7ef41e6`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367fe4dffeb063a80c231a46e76b12ba5555c5ca56bff7bd52e453ad07e0a15`  
		Last Modified: Wed, 22 Apr 2026 02:31:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:d96cd204f455c5dc272e462fd8e316e5a97c0504452f2c27d6ac7530e72a0ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b22090b5ebb684acefa119a6124cb7ae2cba0c11749e40e357bc7e2091a88a`

```dockerfile
```

-	Layers:
	-	`sha256:0b1762ce516402255cd017adeca5b00cc772560a4f5608adf1b1827327879424`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07989d6af49ab13c5428e2cd294f3458939a021ba915616b8dd5dfc2fdcd4d8c`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:10785aa58079387363e472d7e20eb96bd01f12b9850476a066e124d57be1a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1.6.4-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:6a78a135961dde77e0a3e9171928717694804d7cfb3d6aedbebfadb42bf4f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f599634d068048f3fcd01d27356e8cc57fb8937f8bbf03cfccaebddd3b1e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:35 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:14:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:14:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:14:45 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:14:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09629d4032ef7ab1ef9db974170b9cf0e98f6c5d68cb9f3d0e21a37889d50030`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad68e6c6d9b805cb5d27e526a335f55ae1e22e51fb78ed5cd842984966ec752`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097cdb4e276728ffaa69c00b45edf54d761118176e68ef12d68092b7417f986`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 107.6 KB (107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc806c3d4f80593516df4d73efec6cd1cf16dfd200d5fd6adda41910072975`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d250500ebc740f642b6509ef0a3f0576fe4b93cb687a514ceede64292cd717f`  
		Last Modified: Fri, 17 Apr 2026 00:14:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dcf1f88cd35b0648a36b53371be8057efc788150c247273946f22f226c8922f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695771cd59164f79af4e3d51a194af63f71274fa2ca45642700481f66706680`

```dockerfile
```

-	Layers:
	-	`sha256:9047c6064b6fcd9efa90aa0c959722cd5d0677dd3e15d576484c71664c66a025`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ebf9604f23105cb6660c6767d301a937a4b9d6d85433f32e35ffb2ba1e86d8`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:e61a3952e5718375c379136684659c21136328808a6c3f88e9585943251e9a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c576e8f7269c2ef4826f92b4a22494225a6cd470d17d9f30f01d9cc229e696f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:28:10 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:28:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:28:20 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:28:20 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28595f303e8390d8534900bd78b38647a907732d3d3e842c7b3a9caf747dfa`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2d882259c543692d98198b2c8f098f64b95d9b8018fbe3daf4bce16ccdea8`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 7.9 KB (7941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750bf6b03a38c9f5493952dd7c83dba844fa70e86926b54303c228f996e864fb`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 89.2 KB (89153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0b56fb727ea9f7a3dad23a396c81b60139284396a263e6658329c844b5dad`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6b266845306bbbcbee6801a12889b7c152b510808934deb45a090cedc3a06`  
		Last Modified: Fri, 17 Apr 2026 00:28:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e8ab0469cf1a0658dd7f777f120002189b116eedc60e2d13004809373539fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbd38bcf39cf976d74f4ea0d61a864e9b890815035438f477a99caff10eae99`

```dockerfile
```

-	Layers:
	-	`sha256:acf29d68d1e7fa30dc5742c4211ffe81430df68660be1f3d0207d5a94d98bc39`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:147fe0124aa237fa168a69becb6a2db57f4a9ad7144beb44a52a7735a75ed88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3316848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fac8ff5e55f7bb423942ebc9a0dcfe62ab45560df8acbf81f20fce40adfb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:13:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:13:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:13:54 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:13:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48112adbff0844ea29be59655ce36bdc68db268960b43349a213160861be5b`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b71c7a3ae36749950f95514df7064116e47fac5d0e8f2b2a7465a08ec730b1`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc42fa35611c27c8478a77677c7599958f859178a2ae432cdeea23ff283fe`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 81.7 KB (81682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17f9759dca0bc64327214acbd9fd3deb78375c7afd7010e30d54ffe9eafdb6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eff9de0017984f4c4aceb50f22ba5600d01062af116b4a3d8666f104982e79`  
		Last Modified: Fri, 17 Apr 2026 00:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:87b16d20b49f4fd531d2a7882ebf70ab433c78455a68ecb63229df2b111b80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db1828da7718e04747ebb0f602b5974b0a7a0da76481d2a933ecbb6b1869fd9`

```dockerfile
```

-	Layers:
	-	`sha256:32fd82b374cd8966ecaddf73d35913d341f1bf089acec4758b0eddc9ae15bf6c`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451cb443bac28fadec04af355b08de89c30845228bcead9735b3be6a627381f6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1fd688a89197aa9ec5aa2ecf456f856d56b46639e5d0733ee167c8e1f1f67c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e3a3494482e2c117fe69680a253048739b96db6b666e0ba693d69f12f3cffa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:30 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:23:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:23:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:23:40 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:23:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b70cf46309ade34c5a66991fc83a20e95c2a2ca7662393d07532b98169b897`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5fdf2c2bb57fb12d420f1ebc379b73a6a07a076dd649edbdfb2ec65e9b52f`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bde94e8b5d108bfaf26624adc0087452e38a2a8176cc98ece876fe2117fc72`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 100.6 KB (100601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b88c8155b1bdcaf3ceb67be1cd60eac4d053dbde4189b58b41e709ce71a5d`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb330bcfc9ca5ba0cfa2155b2866b977ad2c3ce1d9ae151d07e639bbada8ed2`  
		Last Modified: Fri, 17 Apr 2026 00:23:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fc73de67fe7f5bcda008d343140166980bf4176b3096a535d83f3dcd2d534e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a18fe2b2319a581866e1c86ace119888f0e7b9a60b55a3ce6b779f28fe92710`

```dockerfile
```

-	Layers:
	-	`sha256:a96c2085f2ac76644e77254bfa9bf6d1b56c67d9d9405eaa8416f74fcba97701`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d5f7f4737f85a0e24460592078844c64dafe02803bdf87581c20f597e952bb`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:60c2f83afdec0385615a7286994daa8f205766ef71d83fa8ddc2e700ac81936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc7573391c8c621e1b2f987722ca168aebbe555b0499e62e86738da10c96e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:54:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 05:54:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 05:55:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 05:55:09 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 05:55:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 05:55:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f934ad8efa54d7383ed1d7daf8f07d69a316c785b55e29d855f59724767ac5`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad6a50d64bebedb5b11ecc9dbad14debf2baa30235c5ed093775151dd20c5f`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9ad205a738e9a190290cb841b91a7516b90d39ccefc8a464803a80e5d3bf2`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 120.1 KB (120105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13bce07410da4d5d2d2271580461ed3ae19008e5249df3c1003a06c213c180b`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d30a682d686a1255ac7f31b311acf6f01b819da6af05a18bb59cf9285441247`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:499b7ec7b9c4e4eec426321c8934ac7fac003aeff1b6247ccf002c546cd6a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072722cf70bdbdd1bd5420a6744bc8ca176440a12571a40e33ce18862067a55`

```dockerfile
```

-	Layers:
	-	`sha256:dd1f08b2c21c938da19a9533a1b9dcb5f15e078dab41c9a4bd4ab244cd979858`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517f76f905b9dca96e65eec9ad79a6211e1b541723537e827a226d4839aa2649`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:cd9ed7a248ccd86ed221ed62ccb5fccc85d88f92bb07eacf32a54aa285d3baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b17425a87a9b3f6cf310b87ae46b1234772bd0b80ea164489da909a148229e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 01:13:49 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 01:14:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 01:14:15 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 01:14:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4eb2b31b373fa4117e61ee4973c717af31bc2e3376684ddf64780f6a0cfbf2`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5bc892fe10dffc5824aa6f02e4a3fd2d8872fcc548dc32d8271fbeda871d54`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f69169c64986eaf44f560100f0ace1b79586cff5d1f517fcf6f2810fcf476`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 112.7 KB (112676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc1153f644e2e26a00aa90bf9b03917ab7f9ec331b32bd9bc295281cee7151`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94785087e434424ecd2b2a79b34d04d7aa53bdc943265138216cadd6badf5495`  
		Last Modified: Fri, 17 Apr 2026 01:14:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:42b060f58ef29347aa95f2a95a49a750c85e6dc1283a7429bdbd08cbb35d8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeddc4f5e06133647f4d77b87d5471240c741e9ac4581ee0469cd5e684bde41`

```dockerfile
```

-	Layers:
	-	`sha256:8054970ddb854b9dbe87ad8cc6cb52f8ac69bae6393895a2cc0ec179d9890648`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf789792086c7df442c741fa726e1c634b400a002527085dcc36c87a5bdd724`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eaf86ffaae6edde3dcb5bc958a07fa09bfe7cf9bcd05be9ace676e83efe5f761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508a25834d52056b9c731fc2100ea35e54d563c093104a90eef8c05cb0cd1cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 03:43:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Apr 2026 03:43:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 19 Apr 2026 03:45:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
VOLUME [/spiped]
# Sun, 19 Apr 2026 03:45:16 GMT
WORKDIR /spiped
# Sun, 19 Apr 2026 03:45:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Apr 2026 03:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Apr 2026 03:45:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6ee73726995fef9f6ea4faf4767bcea48e04bfd71f1eea0bd05f9534d43f8`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dd3bcf1d4c6316b374da1b2790b7de4b60cf8e6512e5f30f8d7b2d7a3b38`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e66ca15c2a84ed0ad5aac95f1257383ec006115c07282942c1fd6f06bc2b26`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a854d7ad8f0e7a7a6274e5c362b1a896bd76e462c14408778ba02dff83d37b`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff5f61469b0ef7c1c8bf56662d9b762181e909bc3c749eacbaaecf7bb475ab`  
		Last Modified: Sun, 19 Apr 2026 03:45:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f21b45950838bc0c80c8410cc4f2814b68f96ecad1e19be90b06994c99afbf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abe71f567ae68daf6e6dfeaafd74f8104d7a6958082dd986f64838b44c12b9f`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4f6fe1bacdcf68608f4eb99bf2115bae97f39b1056b72d36c08b63e32ef42`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e5c1e0a1d68c8bdb360c97f9072a3c973409b2f9afe7ff5795d523cae5119b`  
		Last Modified: Sun, 19 Apr 2026 03:45:38 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:d63a333156f14c550016968b48b61e03d6ffa7cdadeb4dc11994993be83c667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f883e0aba651c328e78b42abc6210940d11022f1ee5d1ff5258ebca42e51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:11 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:41:12 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:41:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:41:19 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:41:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:41:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5658f716398e67bcdf451aa62d9268badc01207fb2761dde286827e782131`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d837fc0069a0ae8449bb0adb9f65b43fff5ff059948bf845ea728a30d3eaca0`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f2f936af1acb505aa131fbad0547df0d36ff3dc9c4f8c3a396c9877b87798`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.9 KB (96930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33930e4a86d8157d355b84eecf720d4f20b38ee3502ab3baa6329d6c6acac811`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27970db5cca98e64b9bdffc3b4445e18a503e3e0dc858c6ae91eff10bccd50bd`  
		Last Modified: Fri, 17 Apr 2026 00:41:29 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3a63421a60ad516e8ae99df7c008ce97158220da99f3e592d9090f762eb254c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ae27771b3c7505fb78b0f0546a7416b11e879220de4dc6090bf643dedf8614`

```dockerfile
```

-	Layers:
	-	`sha256:c6abf9efd631a7212221f0b771ec35e734885be3d3a6755a004bba8bd46cc068`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033e56e9f47fa0453060710502d5ab3daddcba0cc4e51e5e138a57faf3e873d6`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:10785aa58079387363e472d7e20eb96bd01f12b9850476a066e124d57be1a8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:6a78a135961dde77e0a3e9171928717694804d7cfb3d6aedbebfadb42bf4f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f599634d068048f3fcd01d27356e8cc57fb8937f8bbf03cfccaebddd3b1e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:35 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:14:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:14:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:14:45 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:14:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09629d4032ef7ab1ef9db974170b9cf0e98f6c5d68cb9f3d0e21a37889d50030`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad68e6c6d9b805cb5d27e526a335f55ae1e22e51fb78ed5cd842984966ec752`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097cdb4e276728ffaa69c00b45edf54d761118176e68ef12d68092b7417f986`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 107.6 KB (107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc806c3d4f80593516df4d73efec6cd1cf16dfd200d5fd6adda41910072975`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d250500ebc740f642b6509ef0a3f0576fe4b93cb687a514ceede64292cd717f`  
		Last Modified: Fri, 17 Apr 2026 00:14:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dcf1f88cd35b0648a36b53371be8057efc788150c247273946f22f226c8922f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695771cd59164f79af4e3d51a194af63f71274fa2ca45642700481f66706680`

```dockerfile
```

-	Layers:
	-	`sha256:9047c6064b6fcd9efa90aa0c959722cd5d0677dd3e15d576484c71664c66a025`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ebf9604f23105cb6660c6767d301a937a4b9d6d85433f32e35ffb2ba1e86d8`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:e61a3952e5718375c379136684659c21136328808a6c3f88e9585943251e9a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c576e8f7269c2ef4826f92b4a22494225a6cd470d17d9f30f01d9cc229e696f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:28:10 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:28:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:28:20 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:28:20 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28595f303e8390d8534900bd78b38647a907732d3d3e842c7b3a9caf747dfa`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2d882259c543692d98198b2c8f098f64b95d9b8018fbe3daf4bce16ccdea8`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 7.9 KB (7941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750bf6b03a38c9f5493952dd7c83dba844fa70e86926b54303c228f996e864fb`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 89.2 KB (89153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0b56fb727ea9f7a3dad23a396c81b60139284396a263e6658329c844b5dad`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6b266845306bbbcbee6801a12889b7c152b510808934deb45a090cedc3a06`  
		Last Modified: Fri, 17 Apr 2026 00:28:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e8ab0469cf1a0658dd7f777f120002189b116eedc60e2d13004809373539fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbd38bcf39cf976d74f4ea0d61a864e9b890815035438f477a99caff10eae99`

```dockerfile
```

-	Layers:
	-	`sha256:acf29d68d1e7fa30dc5742c4211ffe81430df68660be1f3d0207d5a94d98bc39`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:147fe0124aa237fa168a69becb6a2db57f4a9ad7144beb44a52a7735a75ed88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3316848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fac8ff5e55f7bb423942ebc9a0dcfe62ab45560df8acbf81f20fce40adfb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:13:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:13:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:13:54 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:13:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48112adbff0844ea29be59655ce36bdc68db268960b43349a213160861be5b`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b71c7a3ae36749950f95514df7064116e47fac5d0e8f2b2a7465a08ec730b1`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc42fa35611c27c8478a77677c7599958f859178a2ae432cdeea23ff283fe`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 81.7 KB (81682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17f9759dca0bc64327214acbd9fd3deb78375c7afd7010e30d54ffe9eafdb6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eff9de0017984f4c4aceb50f22ba5600d01062af116b4a3d8666f104982e79`  
		Last Modified: Fri, 17 Apr 2026 00:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:87b16d20b49f4fd531d2a7882ebf70ab433c78455a68ecb63229df2b111b80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db1828da7718e04747ebb0f602b5974b0a7a0da76481d2a933ecbb6b1869fd9`

```dockerfile
```

-	Layers:
	-	`sha256:32fd82b374cd8966ecaddf73d35913d341f1bf089acec4758b0eddc9ae15bf6c`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451cb443bac28fadec04af355b08de89c30845228bcead9735b3be6a627381f6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1fd688a89197aa9ec5aa2ecf456f856d56b46639e5d0733ee167c8e1f1f67c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e3a3494482e2c117fe69680a253048739b96db6b666e0ba693d69f12f3cffa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:30 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:23:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:23:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:23:40 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:23:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b70cf46309ade34c5a66991fc83a20e95c2a2ca7662393d07532b98169b897`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5fdf2c2bb57fb12d420f1ebc379b73a6a07a076dd649edbdfb2ec65e9b52f`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bde94e8b5d108bfaf26624adc0087452e38a2a8176cc98ece876fe2117fc72`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 100.6 KB (100601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b88c8155b1bdcaf3ceb67be1cd60eac4d053dbde4189b58b41e709ce71a5d`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb330bcfc9ca5ba0cfa2155b2866b977ad2c3ce1d9ae151d07e639bbada8ed2`  
		Last Modified: Fri, 17 Apr 2026 00:23:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fc73de67fe7f5bcda008d343140166980bf4176b3096a535d83f3dcd2d534e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a18fe2b2319a581866e1c86ace119888f0e7b9a60b55a3ce6b779f28fe92710`

```dockerfile
```

-	Layers:
	-	`sha256:a96c2085f2ac76644e77254bfa9bf6d1b56c67d9d9405eaa8416f74fcba97701`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d5f7f4737f85a0e24460592078844c64dafe02803bdf87581c20f597e952bb`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:60c2f83afdec0385615a7286994daa8f205766ef71d83fa8ddc2e700ac81936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc7573391c8c621e1b2f987722ca168aebbe555b0499e62e86738da10c96e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:54:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 05:54:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 05:55:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 05:55:09 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 05:55:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 05:55:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f934ad8efa54d7383ed1d7daf8f07d69a316c785b55e29d855f59724767ac5`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad6a50d64bebedb5b11ecc9dbad14debf2baa30235c5ed093775151dd20c5f`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9ad205a738e9a190290cb841b91a7516b90d39ccefc8a464803a80e5d3bf2`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 120.1 KB (120105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13bce07410da4d5d2d2271580461ed3ae19008e5249df3c1003a06c213c180b`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d30a682d686a1255ac7f31b311acf6f01b819da6af05a18bb59cf9285441247`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:499b7ec7b9c4e4eec426321c8934ac7fac003aeff1b6247ccf002c546cd6a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072722cf70bdbdd1bd5420a6744bc8ca176440a12571a40e33ce18862067a55`

```dockerfile
```

-	Layers:
	-	`sha256:dd1f08b2c21c938da19a9533a1b9dcb5f15e078dab41c9a4bd4ab244cd979858`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517f76f905b9dca96e65eec9ad79a6211e1b541723537e827a226d4839aa2649`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:cd9ed7a248ccd86ed221ed62ccb5fccc85d88f92bb07eacf32a54aa285d3baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b17425a87a9b3f6cf310b87ae46b1234772bd0b80ea164489da909a148229e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 01:13:49 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 01:14:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 01:14:15 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 01:14:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4eb2b31b373fa4117e61ee4973c717af31bc2e3376684ddf64780f6a0cfbf2`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5bc892fe10dffc5824aa6f02e4a3fd2d8872fcc548dc32d8271fbeda871d54`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f69169c64986eaf44f560100f0ace1b79586cff5d1f517fcf6f2810fcf476`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 112.7 KB (112676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc1153f644e2e26a00aa90bf9b03917ab7f9ec331b32bd9bc295281cee7151`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94785087e434424ecd2b2a79b34d04d7aa53bdc943265138216cadd6badf5495`  
		Last Modified: Fri, 17 Apr 2026 01:14:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:42b060f58ef29347aa95f2a95a49a750c85e6dc1283a7429bdbd08cbb35d8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeddc4f5e06133647f4d77b87d5471240c741e9ac4581ee0469cd5e684bde41`

```dockerfile
```

-	Layers:
	-	`sha256:8054970ddb854b9dbe87ad8cc6cb52f8ac69bae6393895a2cc0ec179d9890648`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf789792086c7df442c741fa726e1c634b400a002527085dcc36c87a5bdd724`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eaf86ffaae6edde3dcb5bc958a07fa09bfe7cf9bcd05be9ace676e83efe5f761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508a25834d52056b9c731fc2100ea35e54d563c093104a90eef8c05cb0cd1cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 03:43:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Apr 2026 03:43:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 19 Apr 2026 03:45:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
VOLUME [/spiped]
# Sun, 19 Apr 2026 03:45:16 GMT
WORKDIR /spiped
# Sun, 19 Apr 2026 03:45:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Apr 2026 03:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Apr 2026 03:45:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6ee73726995fef9f6ea4faf4767bcea48e04bfd71f1eea0bd05f9534d43f8`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dd3bcf1d4c6316b374da1b2790b7de4b60cf8e6512e5f30f8d7b2d7a3b38`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e66ca15c2a84ed0ad5aac95f1257383ec006115c07282942c1fd6f06bc2b26`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a854d7ad8f0e7a7a6274e5c362b1a896bd76e462c14408778ba02dff83d37b`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff5f61469b0ef7c1c8bf56662d9b762181e909bc3c749eacbaaecf7bb475ab`  
		Last Modified: Sun, 19 Apr 2026 03:45:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f21b45950838bc0c80c8410cc4f2814b68f96ecad1e19be90b06994c99afbf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abe71f567ae68daf6e6dfeaafd74f8104d7a6958082dd986f64838b44c12b9f`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4f6fe1bacdcf68608f4eb99bf2115bae97f39b1056b72d36c08b63e32ef42`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e5c1e0a1d68c8bdb360c97f9072a3c973409b2f9afe7ff5795d523cae5119b`  
		Last Modified: Sun, 19 Apr 2026 03:45:38 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:d63a333156f14c550016968b48b61e03d6ffa7cdadeb4dc11994993be83c667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f883e0aba651c328e78b42abc6210940d11022f1ee5d1ff5258ebca42e51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:11 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:41:12 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:41:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:41:19 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:41:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:41:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5658f716398e67bcdf451aa62d9268badc01207fb2761dde286827e782131`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d837fc0069a0ae8449bb0adb9f65b43fff5ff059948bf845ea728a30d3eaca0`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f2f936af1acb505aa131fbad0547df0d36ff3dc9c4f8c3a396c9877b87798`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.9 KB (96930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33930e4a86d8157d355b84eecf720d4f20b38ee3502ab3baa6329d6c6acac811`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27970db5cca98e64b9bdffc3b4445e18a503e3e0dc858c6ae91eff10bccd50bd`  
		Last Modified: Fri, 17 Apr 2026 00:41:29 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3a63421a60ad516e8ae99df7c008ce97158220da99f3e592d9090f762eb254c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ae27771b3c7505fb78b0f0546a7416b11e879220de4dc6090bf643dedf8614`

```dockerfile
```

-	Layers:
	-	`sha256:c6abf9efd631a7212221f0b771ec35e734885be3d3a6755a004bba8bd46cc068`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033e56e9f47fa0453060710502d5ab3daddcba0cc4e51e5e138a57faf3e873d6`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:3b6ac3e45f172915009c7662a28b4462f14812bdaa14d3256155618d0262ca50
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:3697a0c4441ffdebbc45026e68caef4b180d0435c04825aea8683826608b6a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36830248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7651265801ee07aaa82006e38d9ac3f69a351f0133ed076c95fac3c4070b5869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:34:23 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 01:34:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 01:34:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 01:34:47 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 01:34:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:34:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:34:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9b6c12ee3ac5c9fd735735d76164bc3226971d664e3cf1cde43f281aac222f`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c82eb68b5775c3e49cf91b695f5b281d5635a64d68a48d315ad05b5c25c423a`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6541376dd96a6fc09591396c5ee3d29921d988f4bf5c8ce27b07276d38546423`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 7.0 MB (7047707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffaa1a14fd226e56da74302eab175251416360e90c228fd94dade206c9d78c9`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5303c4f9d1890510b3fa6ddd08d126352bdc1920a3c7c4ce5f8238ef9f18db`  
		Last Modified: Wed, 22 Apr 2026 01:34:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d0c6471bc8d160d5788eb73aea715f40a47deb73ce301ef156c476a711c3efd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce174c86dade55ce31b891e3eb31393c052de868272c4047ea5f570c54a06c6d`

```dockerfile
```

-	Layers:
	-	`sha256:4cb9cddb67663afe5f2c1f31b7b70b74b000c8330a998fe3c01e31047495cea6`  
		Last Modified: Wed, 22 Apr 2026 01:34:54 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b2345e28b73fe57e118cead927bed244d50e3bd5ce1d6cec6d4134ab93184f`  
		Last Modified: Wed, 22 Apr 2026 01:34:53 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:58a9096e9da905bf9e7530a00b0386ae545910541ba7636134b7f325a3dabccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d21b5f45c11b35928dffe02224e155b54d9ab4a072b30193e228c96092ef243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:15:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:16:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:16:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:16:28 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:16:28 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:16:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4794e1957b3cf639e20aa4a0d33a68c0170d04be31dfa0d1e3032edec682050`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506884dd4194f6c16e334d33decb7e25face9b3cf73131bf09e3a676569f278c`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ddf0bad83cb62e304347253656f7c58364f61c63151f32241919af173cab8d`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 5.8 MB (5789064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e465e59da14247ef0cbca66c2a5502e3a48bce76072d98ea60321006753a2b20`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cd1db1a45425ed24b69890f937f29324664c3ad90bbd4a1103a1e5c7a59527`  
		Last Modified: Wed, 22 Apr 2026 02:16:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9710231581fc8bd5e10a24a668c5f93c84658a05f2489c9e329561f21aef8ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f876370a99391838ecfc8b380afcf44edfdb92b7866cc035577e33d97017db`

```dockerfile
```

-	Layers:
	-	`sha256:0fc5644cca517238d76d5f7971f9b147255edf3e7f6eda96e7449b4d72ecbe70`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bffcc7d5d03f329eed1cbe5f2ef5ae347e4005ac12647f80dff37b77315c0b8`  
		Last Modified: Wed, 22 Apr 2026 02:16:36 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:c4e99b1c150ce516a4f8bfd06f5ce36db9619da989d63041e2e3ed867e16d9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31801768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eee37b96c47b6d13903255f49ebefb808aad92497750349796120f32c768530`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:17:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:17:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:17:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:17:41 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:17:41 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:17:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac891b940103b402884a868ba78e5b89adc92b82368d5cde3f77372c4d9389ba`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ca0590d621a8fd0bb16855593ec7aa1a43dd3f5cbeab09fc15524c20ed2a4f`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c42837a740b33ee79a0dce997a8890719b42fb8983d80880b7dc711c26b63d`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 5.6 MB (5584567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c84840421fc2932ed7fc419b920bb76552acdc93cf1f503f5de9ecdc6933750`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad350f0e865bb8da2f7a450f0b57ff622e290ac3621cff158b4fa2c0c2de22c`  
		Last Modified: Wed, 22 Apr 2026 02:17:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ee0717b32090e6ea950cc06ea270b71a8c63f09983c60bbee4b7585f217e6a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41537f87b8289ede8bd21a4a0bc0e3582af61d1aa3ca9207aab388dd397eda3a`

```dockerfile
```

-	Layers:
	-	`sha256:d1540387f53a59551e2a390fe3f53e3c532260ee888cedba47ad3cfaeabfd8b1`  
		Last Modified: Wed, 22 Apr 2026 02:17:49 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acba014320a761b4346330d8f6d015a8b553e0d6fffb49bf6ee42f168f8db01f`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f4d2c7ba22fbdd4c39d643fc06400642b6d479a7dfc684a3939b41bd69392c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36379770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b678a615cd6adb58ebf5f146ff8d89909b5200fed70f6093a1252adb559d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:36:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:37:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:37:14 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:37:14 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:37:14 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:37:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68b1d288c6fda5c3d291b76142d35c7ec90bba49f2f7e249984ab5030b2a8a`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72258c478f2f0cacc665dd483d41ad5142247c03f899d55173f931b7e1127ccd`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff059afbb00a8d0c47938a8cd83a2cb69138df7c613c1ff73877639d5839980`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 6.2 MB (6233755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3566292154189efcb23707ad78ae15514dc0e956d1fb5b4f10ca4fe927840`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290e4c2f5ef9aaf2f014d15a44512a40b25b7bc0cac6db9b8ae073550aadfd21`  
		Last Modified: Fri, 08 May 2026 19:37:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b8025f0910028dd9817f393058197a8d68cf5196c0a4e130126c5b48c10cb344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ab8802b871f6dee336412a2abb98089de33fd8aaab9762c3cda2637371d0f2`

```dockerfile
```

-	Layers:
	-	`sha256:1778e062fea4855a339744af921af7d4db3810975c7e16ccd96cf39b1c6b1c2c`  
		Last Modified: Fri, 08 May 2026 19:37:22 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5180c5ea69da7069bfd3b17dcadb7c91742ce10c5bb6bedca95126234abc14a7`  
		Last Modified: Fri, 08 May 2026 19:37:21 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:a5a42b31c5133e64d03f5a1b023ee8d27a65307ee447e6c38d72f9cc58a69dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37740931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517dcd55889daad945724e78840508a57f4309eb60f7ac48ae3e1fd811ded477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 01:42:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 01:42:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 01:42:38 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 01:42:38 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:38 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aca6cb7748c68cb25492fc9f24d7346509f08daab07852187997f5ec83a17`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac35082291b9c1a69c7516c860296f3f63b00268d97bb3318b375aa7c6e218`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c774ae6d18e11f6370e728ab01c1d87ca3d68bc6588743766f2b410cb763d96`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 6.4 MB (6442237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfb397ca7fc0085e5a145933ae46d485e5ce1ccb26ddbd354479221999788d3`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8607271c493cf7697bd03deb4ca4dbfcc0bf3ac55d61e8713977ef73d03df5`  
		Last Modified: Wed, 22 Apr 2026 01:42:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3baf1644c67233842338f1d079882c89f34e0e2f0f8f84b79cdc47157827753e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d28367327b2843b2ec92143d178c6a8a51fa102072a88cb902f253539f42bb`

```dockerfile
```

-	Layers:
	-	`sha256:5c6cf5a178a57a0b0343af5d1335e683c16678501f7d68da3537e480e6791951`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0617f04db6a5465841cac97c304341518b612bb2fb1a516a809a02e779d9994a`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:fb2e82a303c6437dde676fa9c556b3600b2cdc7a5e46e19f152e81e5dcc0f36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1897646fdd9349183d12ff126cdfff37d385745dbc739a89f6192070bb64c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:36:47 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 03:36:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:37:49 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 03:37:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 03:37:49 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 03:37:49 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 03:37:50 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 03:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 03:37:50 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7133018187518174bce13421d93aab7d9276fdbb69c490faa8b0ae4dd915be69`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69ca05c79ecee8f52da5603e09290cc97f59f47547a0118206125ada7ffb118`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f362f773d738a0f6c8a9577379a42baa3a6a6ec4e705aa022b87cbe05ec796d`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 6.8 MB (6840643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce985e16ab67f426410c46f9b52b9521c468c6920d27e53c9149213439e7fa5f`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0dcef50dd0fbf39b2d4d37449d8581150d42d9007f0786e4391b4e8f1ef447`  
		Last Modified: Wed, 22 Apr 2026 03:38:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:de14cc2fcdb7dd56234b4b059a2ebac8ab8098ee3f63a2116aa8807058d5f44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e1dc9be890f0321945d897b84572fa1cf0fdfa3c0fcef100e6932f69fb14fc`

```dockerfile
```

-	Layers:
	-	`sha256:e38d24758f530ffb8b0e868d26eb42289904324921b249a7a4130a3b1fe4ed16`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f376bdb6254bdd4e959421b91495c5b0cdbe2185b945455eeec0fdb3994221`  
		Last Modified: Wed, 22 Apr 2026 03:38:19 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:4b71cf53987a9707a16131c1318e249b3fd3d6ce9a82cb42cc7f49e072e18fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37638423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a4b86552c1e9439f4f551a02d1d47a8a09b1564576e2077689ea60ed92ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 16:08:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 23 Apr 2026 16:09:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 23 Apr 2026 16:12:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 23 Apr 2026 16:12:07 GMT
VOLUME [/spiped]
# Thu, 23 Apr 2026 16:12:07 GMT
WORKDIR /spiped
# Thu, 23 Apr 2026 16:12:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 16:12:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 16:12:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3fe48b86e812e3913e5d13d1a9629869d202426b9c61e1715fa21c49eefb0`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34a84840c5fe62bd145180a478a04eb839e8ebc46151483b24496cb9f4a91f`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d24129e4ff9e3418ef7a713edd9546c25c9b66ed26f8d5aa09e53f0c443a147`  
		Last Modified: Thu, 23 Apr 2026 16:13:23 GMT  
		Size: 9.4 MB (9355868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9de411851378c843f1fa5367128062cec83a39214793d042c62249d045708d`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45064277bc4d512497c03c09b867eecba1e9f36520600b1b7cf50ccf931c314`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:8f1fdb09a20e86779bcd22247e4e7dc45779eadf380ed22541529e1f7c49f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30611531e32494ce7228fad7644d17d3b521a5eb65e2cab640541ec507a3ccff`

```dockerfile
```

-	Layers:
	-	`sha256:28e7945cedc25231eedc0925db8b02ae1dfc5c3c41f66ebd1d3a8ef39e217551`  
		Last Modified: Thu, 23 Apr 2026 16:13:22 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3f06dd63e825c9c98e9b4bfdc4f7087ec431640aee8976c15796ae26a216eb`  
		Last Modified: Thu, 23 Apr 2026 16:13:20 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:019df0384f80e6004366c1482c1a614e1840ece9ddd6e99f1d6bb7ce37049ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35964050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2664081e57843cec9f0abdb42b2f77fbcff9c6301724ad452dfb66ef5c07b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:31:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 22 Apr 2026 02:31:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 22 Apr 2026 02:31:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
VOLUME [/spiped]
# Wed, 22 Apr 2026 02:31:27 GMT
WORKDIR /spiped
# Wed, 22 Apr 2026 02:31:27 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:31:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:31:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c273de4662c09d441d0991d3d1cad27add170f42a58b680c85262c0783bdb0b3`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819848a163b2883ddd6e28cee23ce28b8e14b9b83d1e88475875d55c72185cde`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173a50efe24c4e4255e01d86628f8813bed0b1f4dea66438798d4c154ca4af00`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 6.1 MB (6121383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358262f84455a81b0386d68dfa7aaf68b3631255c9bcacc7d9a9391c7ef41e6`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367fe4dffeb063a80c231a46e76b12ba5555c5ca56bff7bd52e453ad07e0a15`  
		Last Modified: Wed, 22 Apr 2026 02:31:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d96cd204f455c5dc272e462fd8e316e5a97c0504452f2c27d6ac7530e72a0ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b22090b5ebb684acefa119a6124cb7ae2cba0c11749e40e357bc7e2091a88a`

```dockerfile
```

-	Layers:
	-	`sha256:0b1762ce516402255cd017adeca5b00cc772560a4f5608adf1b1827327879424`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07989d6af49ab13c5428e2cd294f3458939a021ba915616b8dd5dfc2fdcd4d8c`  
		Last Modified: Wed, 22 Apr 2026 02:31:38 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json
