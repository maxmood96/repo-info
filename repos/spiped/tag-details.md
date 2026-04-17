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
$ docker pull spiped@sha256:22bd43d626a442991c4cced930625aa55b241be778f28fb46221103dec40dc7c
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
$ docker pull spiped@sha256:a3e2ba12f248fe7dfe821e5c4544f956fb8f6982156435656feb15535e65d879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36825780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507c88cfcc4672ac607c8eec5726dd8f9c6e695d9dc0a0aef8ca23840e6b9b92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:41:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:41:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:42:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:42:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:42:00 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:42:01 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:42:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:42:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241b70042111b50831052e463f8c36f46e7cd27bbbaeeed9faa54a50b21e9d5f`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d85b3b2421b3b5fc68393c5f2d9d82431804098deacda83193e6328d87d035`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a478cf2b7a922f008a2c3ed2a49fc619d7713e19830fc721e0b36f3d6c21099b`  
		Last Modified: Tue, 07 Apr 2026 01:42:08 GMT  
		Size: 7.0 MB (7047768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38f7c4fcb0c778cabd304b72bd2dee1718d36452be6e7b3e20fbd170a9c41f3`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5733502a2a646bc6a97ca03fb756b92d359d8ed6912eef64a0adbc0644477654`  
		Last Modified: Tue, 07 Apr 2026 01:42:09 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:aa2c0709b2a7dd96572681c842e0c3ef3a22be0d0d6815caf966a6cee2864ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f728528d821e69e56c3dd90e8dc75257bcd13318fae4a795b6e9dbd4b3990e0f`

```dockerfile
```

-	Layers:
	-	`sha256:1a4e5a8e2b699289058f143b6a6630b2df64eec04b5144c6d27aab53eab8aca6`  
		Last Modified: Tue, 07 Apr 2026 01:42:08 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b191389c378d65248dda301c92386106c1e990d3eb3ff583b816c1ac789788f2`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b9752fa7cebde10760dc4a92cf1add0d71389536c0fadc9103ee7ac42d3c28ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753206012e26cdcfc67aba0e15122baccaa308a313e45dfa421117302dcfbca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:44:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 02:44:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 02:44:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 02:44:44 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 02:44:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:44:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db2337a9daf6c7349a4348c46b064f676d7db505cf3ecd9631b722f5d7efd1`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a999823a7c579778c69b2165050956ebbbcf97d033a17c25bd1b33b92ce7c6`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7befd368637b8c0d89cbaa145cb5758fa39c0996d6b90b5d8aba208dfd13288`  
		Last Modified: Tue, 07 Apr 2026 02:44:52 GMT  
		Size: 5.8 MB (5789110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c838cdbcba0fbcd482e6aa549e3c5aa9ea6c7725ec3ea39ad6ec4bd01b2fb1`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a29b6bf38b8a6ed8469c97a62b1355ed1c8de06bf3ab3175ddcecc97b4db0`  
		Last Modified: Tue, 07 Apr 2026 02:44:52 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:bdfee195558b3b0ea408e01d2c0de4f907563058275ffcb0dcc4a97dce9c61f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bd1dc54b4dcdc3531b00acaab110439c43129e708ba848cd76425ffdb9c985`

```dockerfile
```

-	Layers:
	-	`sha256:cfffdf2f2bc673d0962ccc72948fd40b9c494459522d2b0d880f00274ce64421`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0157165ff7842ac2ed5a4887f2f6221fe1432566b1363edbb1f78ccce99187b2`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9a8582c92541927d6cc6b1231e3f9fc087634e8ebf740f22932ced1fa84e6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31796505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78afdb203bf64361dc4a6539eb4f7afa7db2600858593dfd37097874854af75f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:57:41 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:57:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:58:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:58:09 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:58:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4c3f24a8c67fe9d39009a981843ee5dd2f56fad9e606d7b59792acfd232f4a`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4367de839e4ddd19b09eb146c6add980bc3bc6b37f896557dd766f7a91a3eb`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c921174dc4f14b12d5e1373ba4e9dcdce0e25101dd048cf97d127f7f988706f`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 5.6 MB (5584481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff37b32652071edf1c320151ec362df4ce897d0e942b56853e314b2cb7d9a77`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1025fd50b8baa88dd6f89830e0c4249202bbc1703d69bc2afa5e02f19070b2d1`  
		Last Modified: Tue, 07 Apr 2026 01:58:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:a1c85e8d160123fe75e4e428de5030c34bced1afc1a222176e42a03353f7ca86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74665bee3b6f99ce7b5b54b5f2cbc329376ebb705376c95223459b535aa289d`

```dockerfile
```

-	Layers:
	-	`sha256:61d35ea2bfc8c09cba13551b4ee3ad0700517cece547096fc39a29ce4ba2d7f4`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed71dff4cc1ad51bf4c38a0c7b1cadb1287246ab35f0bec2a619e3d9e35b66`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d30ebc6ea0efd7067ddd5465200f316680955d148ec7ee740bf77e9f26776d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36374635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028134019e80f1ad2729ce283b69e420a7e87c10b1f90704f60aba8c66640d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:44:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:44:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:44:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:44:35 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:44:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:44:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78386c1f339617a7514f5c5850a35392c79415338c48df95534347bfb66dbd`  
		Last Modified: Tue, 07 Apr 2026 01:44:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbe44cc1411ff7b718c6c32487316d0de9e2e84d5b71f1f50889d436557da5b`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36237e30e614284ea3149f330180e9abd28233c7e56ea1ee5978407cd7e354e9`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 6.2 MB (6233711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d3fe23a684c92d3b9df580f910367a15e1516c0bce117cd01717a0fd1f70d1`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db60e764a9b2a2389e56088a56c0cd50608a83c4e463f881b7b9a4d652f11f32`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:d2830d9ee8319621f2b65a684225f90d0eb138954081954ef653581ef6357953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b67e488a21abfb3b8a3ca6b05ed397275015cb79280117e1e286cda4047440`

```dockerfile
```

-	Layers:
	-	`sha256:4023c6866b5098980de4a82760fc4a5c5b5c437ad84d91ba4218736f94211056`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63ada7739a03a3c861e386268b5489839840bc30290399ce78d105ca004e36e`  
		Last Modified: Tue, 07 Apr 2026 01:44:41 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:fdba21dc9ed99ac757f7db3552f2fb3c7ee3f40ba0c5833d61065da583f5c075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37735973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d069883d47f5c8b13decfe94a8e20e7cbbb45a7ffb60b8b0d1b4656b2adf4e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:45:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:45:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:45:57 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:45:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:45:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe1f9ad83d46736d171810638a97d75cca03c9b4a511520e2a5ea7bf236ec1e`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec45cc8c1429a10738a1b8cf80de924f317f30d79ab8f16df7c111572459b25f`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59588fe2cad3f5d3ed274dd5340d2d0264ab0ac22df03bfd63ba5580f94f85f`  
		Last Modified: Tue, 07 Apr 2026 01:46:05 GMT  
		Size: 6.4 MB (6442351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b43e60f19cb0ad95d1a96d3820660d70997c0076652baa3e077fb08394f45`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef277f865aa5227526a7f75b1acd5208e7a1f665263f54e1623d399e5e8a399`  
		Last Modified: Tue, 07 Apr 2026 01:46:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:21d075407fe32f0f730f50e2593e33a2fcec94f04da56f4750599400588d7956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ae5cab45b127fae7709c8c41698e534cba9b7c6cc6fab44c58cc57af01390c`

```dockerfile
```

-	Layers:
	-	`sha256:616d8e60678ffc448b015c93ea6b71f155e346c6803b5e8ce2399868bd7dc4ee`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c1bebdefb8ac4db5dee341d7b7a17d565afa0a140b5f4dc8c348c2c81f3ba0`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:c0a453063892828d0fb816889260b2c5f99fba2b9edc331339d6d224700718a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580742e53478938982c276ba05ef6aea1feddc27f3166c8f5c5d7ea6df4b4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:18:54 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 04:18:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:20:04 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 04:20:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 04:20:04 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 04:20:05 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 04:20:05 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 04:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 04:20:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75139b25c1163efa600a1092483a109211fbe92ad95197d07fa71ef7a03aa199`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98f08d8269e6b0be51b2c864c4eca24109b6b99713bda09c8e9c57203dddf0e`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7564825c015f3bef02badeecdb11be2e23c0fe99787e570b94cdfdcd4b56352`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 6.8 MB (6840674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0746a2a48a65f4c41b7be26456f56607ee731936781c5a9498e7f6b60edaaf51`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d264dd18051fec52d9e9d773ab8dc08ab88bb65721a3cd1f5dd0d4b9024a0497`  
		Last Modified: Tue, 07 Apr 2026 04:20:31 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:2449d893ea7867f05190ed3b87f5acc9415eb7dba16b1291ef9c71fa8b845c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9538c764a62583ed14715893afb0bbc4d286a569c9ad2a652b0c2de87beae9b`

```dockerfile
```

-	Layers:
	-	`sha256:a7cae8514458b1fc537b1985abd7c9c51a3e60670412e57fa09b99d0c32c03c3`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7f6a424912f840da5acc7994e0b410d77ea2da4b2aee5b8dfaab3e56dc0b6b`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:62524bfd97797aa199c180642403ffaba659b996e9789af10309c736a0958c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40298595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a83d0d12ce259b66549d2f71ac7d9f81ea279ef1f6586189805ecdeccce9982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 00:09:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 09 Apr 2026 00:09:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 09 Apr 2026 00:13:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
VOLUME [/spiped]
# Thu, 09 Apr 2026 00:13:03 GMT
WORKDIR /spiped
# Thu, 09 Apr 2026 00:13:03 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 00:13:03 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353d16b8234198686b3afc079e10ceb632aad857a9760042d6f813a4792893a4`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6838fc2cc2ae3970bd10a42658413616714e7526ffc0eefa5b7f6739a1b26ce`  
		Last Modified: Thu, 09 Apr 2026 00:14:17 GMT  
		Size: 2.7 MB (2665148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8b54dc228fa06c8f98b630722d41503ff93919fa303e7785590ff38951c2cc`  
		Last Modified: Thu, 09 Apr 2026 00:14:18 GMT  
		Size: 9.4 MB (9356127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b2146f14ce9acd32759db2c4b58b0aa96f0b9a39bcc998ec0c574b4f7af125`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a0c469fc9cb466c96a6b7a65dc72474dc4e48c72d667cef319ec00410bc9db`  
		Last Modified: Thu, 09 Apr 2026 00:14:18 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:a32b4f298629e988573b612f99ed7a03311851f5fe86863006b8339a6e63ab4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5ad88771b56b7444669dfe43fbc1178d34893b163258fe60da3ba11a493fe4`

```dockerfile
```

-	Layers:
	-	`sha256:b2bb30d415e973e0ab358209ce964521772ecf6951d2c496aa08112a7c116118`  
		Last Modified: Thu, 09 Apr 2026 00:14:17 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a031708803e467d97b91a4666d7ddb2fd344283d41baba870ae198b40d7ead`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 15.0 KB (15046 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:5377c325f2e677a38dd81a6618db4df283c0b163aa8c4003bc3fd3e36860fd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35959459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339a11ff88fcf4abc9de57162ebbd74759fb778478405f1f2f7336979527e0bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:03:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 03:03:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 03:04:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 03:04:17 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 03:04:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:04:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e369b5ab19c2212fd86d57eda1cf3c506c29704f544d9860de891f00673d9fd`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6669d921ff7e40cebaba94c08a71cf0ec7b2fc4651fcc1e038e5795723535c1`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f8a307634deaa96dd6de60d2e3bf8fa5cb2b8efdc9048bb3ee207d3797a73`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 6.1 MB (6121669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773dc6511e525dfa9f3ba508de6e2ca76db7b727ac06923c99b6a44efe919fa`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cc190018f9de55d4b8fcf1181885ac8b5cd049b39999592aa4198f9501e4a3`  
		Last Modified: Tue, 07 Apr 2026 03:04:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:46d304ddb6375e95dc4644cc7edc92bad5cb61f0e64de098bb3ca676cf8d8b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d94cc4d62ed8e676852259037a7643ef7cab6ff6d0664bf5a1e3ec7f949d7`

```dockerfile
```

-	Layers:
	-	`sha256:a929665e980ab68c90beabcaf6acf299c0f48cc3bedb83f9c6f5db524e0beeb6`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0059e152b4573a43d5717820ac10affa0f56ca5f425d939a7971ddb8cb35e52e`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:027025cc0b5ca751a8f2194f4a6aef0720a1bff70cc29271225adaa1e2061db0
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
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
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
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
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
$ docker pull spiped@sha256:22bd43d626a442991c4cced930625aa55b241be778f28fb46221103dec40dc7c
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
$ docker pull spiped@sha256:a3e2ba12f248fe7dfe821e5c4544f956fb8f6982156435656feb15535e65d879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36825780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507c88cfcc4672ac607c8eec5726dd8f9c6e695d9dc0a0aef8ca23840e6b9b92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:41:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:41:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:42:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:42:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:42:00 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:42:01 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:42:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:42:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241b70042111b50831052e463f8c36f46e7cd27bbbaeeed9faa54a50b21e9d5f`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d85b3b2421b3b5fc68393c5f2d9d82431804098deacda83193e6328d87d035`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a478cf2b7a922f008a2c3ed2a49fc619d7713e19830fc721e0b36f3d6c21099b`  
		Last Modified: Tue, 07 Apr 2026 01:42:08 GMT  
		Size: 7.0 MB (7047768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38f7c4fcb0c778cabd304b72bd2dee1718d36452be6e7b3e20fbd170a9c41f3`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5733502a2a646bc6a97ca03fb756b92d359d8ed6912eef64a0adbc0644477654`  
		Last Modified: Tue, 07 Apr 2026 01:42:09 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:aa2c0709b2a7dd96572681c842e0c3ef3a22be0d0d6815caf966a6cee2864ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f728528d821e69e56c3dd90e8dc75257bcd13318fae4a795b6e9dbd4b3990e0f`

```dockerfile
```

-	Layers:
	-	`sha256:1a4e5a8e2b699289058f143b6a6630b2df64eec04b5144c6d27aab53eab8aca6`  
		Last Modified: Tue, 07 Apr 2026 01:42:08 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b191389c378d65248dda301c92386106c1e990d3eb3ff583b816c1ac789788f2`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b9752fa7cebde10760dc4a92cf1add0d71389536c0fadc9103ee7ac42d3c28ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753206012e26cdcfc67aba0e15122baccaa308a313e45dfa421117302dcfbca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:44:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 02:44:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 02:44:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 02:44:44 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 02:44:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:44:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db2337a9daf6c7349a4348c46b064f676d7db505cf3ecd9631b722f5d7efd1`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a999823a7c579778c69b2165050956ebbbcf97d033a17c25bd1b33b92ce7c6`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7befd368637b8c0d89cbaa145cb5758fa39c0996d6b90b5d8aba208dfd13288`  
		Last Modified: Tue, 07 Apr 2026 02:44:52 GMT  
		Size: 5.8 MB (5789110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c838cdbcba0fbcd482e6aa549e3c5aa9ea6c7725ec3ea39ad6ec4bd01b2fb1`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a29b6bf38b8a6ed8469c97a62b1355ed1c8de06bf3ab3175ddcecc97b4db0`  
		Last Modified: Tue, 07 Apr 2026 02:44:52 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:bdfee195558b3b0ea408e01d2c0de4f907563058275ffcb0dcc4a97dce9c61f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bd1dc54b4dcdc3531b00acaab110439c43129e708ba848cd76425ffdb9c985`

```dockerfile
```

-	Layers:
	-	`sha256:cfffdf2f2bc673d0962ccc72948fd40b9c494459522d2b0d880f00274ce64421`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0157165ff7842ac2ed5a4887f2f6221fe1432566b1363edbb1f78ccce99187b2`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9a8582c92541927d6cc6b1231e3f9fc087634e8ebf740f22932ced1fa84e6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31796505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78afdb203bf64361dc4a6539eb4f7afa7db2600858593dfd37097874854af75f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:57:41 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:57:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:58:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:58:09 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:58:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4c3f24a8c67fe9d39009a981843ee5dd2f56fad9e606d7b59792acfd232f4a`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4367de839e4ddd19b09eb146c6add980bc3bc6b37f896557dd766f7a91a3eb`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c921174dc4f14b12d5e1373ba4e9dcdce0e25101dd048cf97d127f7f988706f`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 5.6 MB (5584481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff37b32652071edf1c320151ec362df4ce897d0e942b56853e314b2cb7d9a77`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1025fd50b8baa88dd6f89830e0c4249202bbc1703d69bc2afa5e02f19070b2d1`  
		Last Modified: Tue, 07 Apr 2026 01:58:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:a1c85e8d160123fe75e4e428de5030c34bced1afc1a222176e42a03353f7ca86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74665bee3b6f99ce7b5b54b5f2cbc329376ebb705376c95223459b535aa289d`

```dockerfile
```

-	Layers:
	-	`sha256:61d35ea2bfc8c09cba13551b4ee3ad0700517cece547096fc39a29ce4ba2d7f4`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed71dff4cc1ad51bf4c38a0c7b1cadb1287246ab35f0bec2a619e3d9e35b66`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d30ebc6ea0efd7067ddd5465200f316680955d148ec7ee740bf77e9f26776d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36374635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028134019e80f1ad2729ce283b69e420a7e87c10b1f90704f60aba8c66640d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:44:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:44:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:44:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:44:35 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:44:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:44:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78386c1f339617a7514f5c5850a35392c79415338c48df95534347bfb66dbd`  
		Last Modified: Tue, 07 Apr 2026 01:44:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbe44cc1411ff7b718c6c32487316d0de9e2e84d5b71f1f50889d436557da5b`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36237e30e614284ea3149f330180e9abd28233c7e56ea1ee5978407cd7e354e9`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 6.2 MB (6233711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d3fe23a684c92d3b9df580f910367a15e1516c0bce117cd01717a0fd1f70d1`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db60e764a9b2a2389e56088a56c0cd50608a83c4e463f881b7b9a4d652f11f32`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:d2830d9ee8319621f2b65a684225f90d0eb138954081954ef653581ef6357953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b67e488a21abfb3b8a3ca6b05ed397275015cb79280117e1e286cda4047440`

```dockerfile
```

-	Layers:
	-	`sha256:4023c6866b5098980de4a82760fc4a5c5b5c437ad84d91ba4218736f94211056`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63ada7739a03a3c861e386268b5489839840bc30290399ce78d105ca004e36e`  
		Last Modified: Tue, 07 Apr 2026 01:44:41 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:fdba21dc9ed99ac757f7db3552f2fb3c7ee3f40ba0c5833d61065da583f5c075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37735973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d069883d47f5c8b13decfe94a8e20e7cbbb45a7ffb60b8b0d1b4656b2adf4e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:45:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:45:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:45:57 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:45:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:45:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe1f9ad83d46736d171810638a97d75cca03c9b4a511520e2a5ea7bf236ec1e`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec45cc8c1429a10738a1b8cf80de924f317f30d79ab8f16df7c111572459b25f`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59588fe2cad3f5d3ed274dd5340d2d0264ab0ac22df03bfd63ba5580f94f85f`  
		Last Modified: Tue, 07 Apr 2026 01:46:05 GMT  
		Size: 6.4 MB (6442351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b43e60f19cb0ad95d1a96d3820660d70997c0076652baa3e077fb08394f45`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef277f865aa5227526a7f75b1acd5208e7a1f665263f54e1623d399e5e8a399`  
		Last Modified: Tue, 07 Apr 2026 01:46:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:21d075407fe32f0f730f50e2593e33a2fcec94f04da56f4750599400588d7956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ae5cab45b127fae7709c8c41698e534cba9b7c6cc6fab44c58cc57af01390c`

```dockerfile
```

-	Layers:
	-	`sha256:616d8e60678ffc448b015c93ea6b71f155e346c6803b5e8ce2399868bd7dc4ee`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c1bebdefb8ac4db5dee341d7b7a17d565afa0a140b5f4dc8c348c2c81f3ba0`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:c0a453063892828d0fb816889260b2c5f99fba2b9edc331339d6d224700718a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580742e53478938982c276ba05ef6aea1feddc27f3166c8f5c5d7ea6df4b4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:18:54 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 04:18:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:20:04 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 04:20:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 04:20:04 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 04:20:05 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 04:20:05 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 04:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 04:20:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75139b25c1163efa600a1092483a109211fbe92ad95197d07fa71ef7a03aa199`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98f08d8269e6b0be51b2c864c4eca24109b6b99713bda09c8e9c57203dddf0e`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7564825c015f3bef02badeecdb11be2e23c0fe99787e570b94cdfdcd4b56352`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 6.8 MB (6840674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0746a2a48a65f4c41b7be26456f56607ee731936781c5a9498e7f6b60edaaf51`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d264dd18051fec52d9e9d773ab8dc08ab88bb65721a3cd1f5dd0d4b9024a0497`  
		Last Modified: Tue, 07 Apr 2026 04:20:31 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:2449d893ea7867f05190ed3b87f5acc9415eb7dba16b1291ef9c71fa8b845c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9538c764a62583ed14715893afb0bbc4d286a569c9ad2a652b0c2de87beae9b`

```dockerfile
```

-	Layers:
	-	`sha256:a7cae8514458b1fc537b1985abd7c9c51a3e60670412e57fa09b99d0c32c03c3`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7f6a424912f840da5acc7994e0b410d77ea2da4b2aee5b8dfaab3e56dc0b6b`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:62524bfd97797aa199c180642403ffaba659b996e9789af10309c736a0958c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40298595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a83d0d12ce259b66549d2f71ac7d9f81ea279ef1f6586189805ecdeccce9982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 00:09:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 09 Apr 2026 00:09:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 09 Apr 2026 00:13:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
VOLUME [/spiped]
# Thu, 09 Apr 2026 00:13:03 GMT
WORKDIR /spiped
# Thu, 09 Apr 2026 00:13:03 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 00:13:03 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353d16b8234198686b3afc079e10ceb632aad857a9760042d6f813a4792893a4`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6838fc2cc2ae3970bd10a42658413616714e7526ffc0eefa5b7f6739a1b26ce`  
		Last Modified: Thu, 09 Apr 2026 00:14:17 GMT  
		Size: 2.7 MB (2665148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8b54dc228fa06c8f98b630722d41503ff93919fa303e7785590ff38951c2cc`  
		Last Modified: Thu, 09 Apr 2026 00:14:18 GMT  
		Size: 9.4 MB (9356127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b2146f14ce9acd32759db2c4b58b0aa96f0b9a39bcc998ec0c574b4f7af125`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a0c469fc9cb466c96a6b7a65dc72474dc4e48c72d667cef319ec00410bc9db`  
		Last Modified: Thu, 09 Apr 2026 00:14:18 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:a32b4f298629e988573b612f99ed7a03311851f5fe86863006b8339a6e63ab4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5ad88771b56b7444669dfe43fbc1178d34893b163258fe60da3ba11a493fe4`

```dockerfile
```

-	Layers:
	-	`sha256:b2bb30d415e973e0ab358209ce964521772ecf6951d2c496aa08112a7c116118`  
		Last Modified: Thu, 09 Apr 2026 00:14:17 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a031708803e467d97b91a4666d7ddb2fd344283d41baba870ae198b40d7ead`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 15.0 KB (15046 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:5377c325f2e677a38dd81a6618db4df283c0b163aa8c4003bc3fd3e36860fd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35959459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339a11ff88fcf4abc9de57162ebbd74759fb778478405f1f2f7336979527e0bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:03:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 03:03:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 03:04:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 03:04:17 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 03:04:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:04:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e369b5ab19c2212fd86d57eda1cf3c506c29704f544d9860de891f00673d9fd`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6669d921ff7e40cebaba94c08a71cf0ec7b2fc4651fcc1e038e5795723535c1`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f8a307634deaa96dd6de60d2e3bf8fa5cb2b8efdc9048bb3ee207d3797a73`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 6.1 MB (6121669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773dc6511e525dfa9f3ba508de6e2ca76db7b727ac06923c99b6a44efe919fa`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cc190018f9de55d4b8fcf1181885ac8b5cd049b39999592aa4198f9501e4a3`  
		Last Modified: Tue, 07 Apr 2026 03:04:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:46d304ddb6375e95dc4644cc7edc92bad5cb61f0e64de098bb3ca676cf8d8b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d94cc4d62ed8e676852259037a7643ef7cab6ff6d0664bf5a1e3ec7f949d7`

```dockerfile
```

-	Layers:
	-	`sha256:a929665e980ab68c90beabcaf6acf299c0f48cc3bedb83f9c6f5db524e0beeb6`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0059e152b4573a43d5717820ac10affa0f56ca5f425d939a7971ddb8cb35e52e`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:027025cc0b5ca751a8f2194f4a6aef0720a1bff70cc29271225adaa1e2061db0
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
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
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
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
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
$ docker pull spiped@sha256:22bd43d626a442991c4cced930625aa55b241be778f28fb46221103dec40dc7c
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
$ docker pull spiped@sha256:a3e2ba12f248fe7dfe821e5c4544f956fb8f6982156435656feb15535e65d879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36825780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507c88cfcc4672ac607c8eec5726dd8f9c6e695d9dc0a0aef8ca23840e6b9b92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:41:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:41:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:42:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:42:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:42:00 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:42:01 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:42:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:42:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241b70042111b50831052e463f8c36f46e7cd27bbbaeeed9faa54a50b21e9d5f`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d85b3b2421b3b5fc68393c5f2d9d82431804098deacda83193e6328d87d035`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a478cf2b7a922f008a2c3ed2a49fc619d7713e19830fc721e0b36f3d6c21099b`  
		Last Modified: Tue, 07 Apr 2026 01:42:08 GMT  
		Size: 7.0 MB (7047768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38f7c4fcb0c778cabd304b72bd2dee1718d36452be6e7b3e20fbd170a9c41f3`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5733502a2a646bc6a97ca03fb756b92d359d8ed6912eef64a0adbc0644477654`  
		Last Modified: Tue, 07 Apr 2026 01:42:09 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:aa2c0709b2a7dd96572681c842e0c3ef3a22be0d0d6815caf966a6cee2864ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f728528d821e69e56c3dd90e8dc75257bcd13318fae4a795b6e9dbd4b3990e0f`

```dockerfile
```

-	Layers:
	-	`sha256:1a4e5a8e2b699289058f143b6a6630b2df64eec04b5144c6d27aab53eab8aca6`  
		Last Modified: Tue, 07 Apr 2026 01:42:08 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b191389c378d65248dda301c92386106c1e990d3eb3ff583b816c1ac789788f2`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b9752fa7cebde10760dc4a92cf1add0d71389536c0fadc9103ee7ac42d3c28ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753206012e26cdcfc67aba0e15122baccaa308a313e45dfa421117302dcfbca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:44:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 02:44:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 02:44:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 02:44:44 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 02:44:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:44:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db2337a9daf6c7349a4348c46b064f676d7db505cf3ecd9631b722f5d7efd1`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a999823a7c579778c69b2165050956ebbbcf97d033a17c25bd1b33b92ce7c6`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7befd368637b8c0d89cbaa145cb5758fa39c0996d6b90b5d8aba208dfd13288`  
		Last Modified: Tue, 07 Apr 2026 02:44:52 GMT  
		Size: 5.8 MB (5789110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c838cdbcba0fbcd482e6aa549e3c5aa9ea6c7725ec3ea39ad6ec4bd01b2fb1`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a29b6bf38b8a6ed8469c97a62b1355ed1c8de06bf3ab3175ddcecc97b4db0`  
		Last Modified: Tue, 07 Apr 2026 02:44:52 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:bdfee195558b3b0ea408e01d2c0de4f907563058275ffcb0dcc4a97dce9c61f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bd1dc54b4dcdc3531b00acaab110439c43129e708ba848cd76425ffdb9c985`

```dockerfile
```

-	Layers:
	-	`sha256:cfffdf2f2bc673d0962ccc72948fd40b9c494459522d2b0d880f00274ce64421`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0157165ff7842ac2ed5a4887f2f6221fe1432566b1363edbb1f78ccce99187b2`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9a8582c92541927d6cc6b1231e3f9fc087634e8ebf740f22932ced1fa84e6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31796505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78afdb203bf64361dc4a6539eb4f7afa7db2600858593dfd37097874854af75f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:57:41 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:57:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:58:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:58:09 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:58:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4c3f24a8c67fe9d39009a981843ee5dd2f56fad9e606d7b59792acfd232f4a`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4367de839e4ddd19b09eb146c6add980bc3bc6b37f896557dd766f7a91a3eb`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c921174dc4f14b12d5e1373ba4e9dcdce0e25101dd048cf97d127f7f988706f`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 5.6 MB (5584481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff37b32652071edf1c320151ec362df4ce897d0e942b56853e314b2cb7d9a77`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1025fd50b8baa88dd6f89830e0c4249202bbc1703d69bc2afa5e02f19070b2d1`  
		Last Modified: Tue, 07 Apr 2026 01:58:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:a1c85e8d160123fe75e4e428de5030c34bced1afc1a222176e42a03353f7ca86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74665bee3b6f99ce7b5b54b5f2cbc329376ebb705376c95223459b535aa289d`

```dockerfile
```

-	Layers:
	-	`sha256:61d35ea2bfc8c09cba13551b4ee3ad0700517cece547096fc39a29ce4ba2d7f4`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed71dff4cc1ad51bf4c38a0c7b1cadb1287246ab35f0bec2a619e3d9e35b66`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d30ebc6ea0efd7067ddd5465200f316680955d148ec7ee740bf77e9f26776d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36374635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028134019e80f1ad2729ce283b69e420a7e87c10b1f90704f60aba8c66640d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:44:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:44:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:44:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:44:35 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:44:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:44:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78386c1f339617a7514f5c5850a35392c79415338c48df95534347bfb66dbd`  
		Last Modified: Tue, 07 Apr 2026 01:44:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbe44cc1411ff7b718c6c32487316d0de9e2e84d5b71f1f50889d436557da5b`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36237e30e614284ea3149f330180e9abd28233c7e56ea1ee5978407cd7e354e9`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 6.2 MB (6233711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d3fe23a684c92d3b9df580f910367a15e1516c0bce117cd01717a0fd1f70d1`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db60e764a9b2a2389e56088a56c0cd50608a83c4e463f881b7b9a4d652f11f32`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:d2830d9ee8319621f2b65a684225f90d0eb138954081954ef653581ef6357953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b67e488a21abfb3b8a3ca6b05ed397275015cb79280117e1e286cda4047440`

```dockerfile
```

-	Layers:
	-	`sha256:4023c6866b5098980de4a82760fc4a5c5b5c437ad84d91ba4218736f94211056`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63ada7739a03a3c861e386268b5489839840bc30290399ce78d105ca004e36e`  
		Last Modified: Tue, 07 Apr 2026 01:44:41 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:fdba21dc9ed99ac757f7db3552f2fb3c7ee3f40ba0c5833d61065da583f5c075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37735973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d069883d47f5c8b13decfe94a8e20e7cbbb45a7ffb60b8b0d1b4656b2adf4e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:45:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:45:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:45:57 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:45:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:45:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe1f9ad83d46736d171810638a97d75cca03c9b4a511520e2a5ea7bf236ec1e`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec45cc8c1429a10738a1b8cf80de924f317f30d79ab8f16df7c111572459b25f`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59588fe2cad3f5d3ed274dd5340d2d0264ab0ac22df03bfd63ba5580f94f85f`  
		Last Modified: Tue, 07 Apr 2026 01:46:05 GMT  
		Size: 6.4 MB (6442351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b43e60f19cb0ad95d1a96d3820660d70997c0076652baa3e077fb08394f45`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef277f865aa5227526a7f75b1acd5208e7a1f665263f54e1623d399e5e8a399`  
		Last Modified: Tue, 07 Apr 2026 01:46:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:21d075407fe32f0f730f50e2593e33a2fcec94f04da56f4750599400588d7956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ae5cab45b127fae7709c8c41698e534cba9b7c6cc6fab44c58cc57af01390c`

```dockerfile
```

-	Layers:
	-	`sha256:616d8e60678ffc448b015c93ea6b71f155e346c6803b5e8ce2399868bd7dc4ee`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c1bebdefb8ac4db5dee341d7b7a17d565afa0a140b5f4dc8c348c2c81f3ba0`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:c0a453063892828d0fb816889260b2c5f99fba2b9edc331339d6d224700718a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580742e53478938982c276ba05ef6aea1feddc27f3166c8f5c5d7ea6df4b4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:18:54 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 04:18:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:20:04 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 04:20:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 04:20:04 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 04:20:05 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 04:20:05 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 04:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 04:20:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75139b25c1163efa600a1092483a109211fbe92ad95197d07fa71ef7a03aa199`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98f08d8269e6b0be51b2c864c4eca24109b6b99713bda09c8e9c57203dddf0e`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7564825c015f3bef02badeecdb11be2e23c0fe99787e570b94cdfdcd4b56352`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 6.8 MB (6840674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0746a2a48a65f4c41b7be26456f56607ee731936781c5a9498e7f6b60edaaf51`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d264dd18051fec52d9e9d773ab8dc08ab88bb65721a3cd1f5dd0d4b9024a0497`  
		Last Modified: Tue, 07 Apr 2026 04:20:31 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:2449d893ea7867f05190ed3b87f5acc9415eb7dba16b1291ef9c71fa8b845c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9538c764a62583ed14715893afb0bbc4d286a569c9ad2a652b0c2de87beae9b`

```dockerfile
```

-	Layers:
	-	`sha256:a7cae8514458b1fc537b1985abd7c9c51a3e60670412e57fa09b99d0c32c03c3`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7f6a424912f840da5acc7994e0b410d77ea2da4b2aee5b8dfaab3e56dc0b6b`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:62524bfd97797aa199c180642403ffaba659b996e9789af10309c736a0958c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40298595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a83d0d12ce259b66549d2f71ac7d9f81ea279ef1f6586189805ecdeccce9982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 00:09:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 09 Apr 2026 00:09:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 09 Apr 2026 00:13:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
VOLUME [/spiped]
# Thu, 09 Apr 2026 00:13:03 GMT
WORKDIR /spiped
# Thu, 09 Apr 2026 00:13:03 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 00:13:03 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353d16b8234198686b3afc079e10ceb632aad857a9760042d6f813a4792893a4`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6838fc2cc2ae3970bd10a42658413616714e7526ffc0eefa5b7f6739a1b26ce`  
		Last Modified: Thu, 09 Apr 2026 00:14:17 GMT  
		Size: 2.7 MB (2665148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8b54dc228fa06c8f98b630722d41503ff93919fa303e7785590ff38951c2cc`  
		Last Modified: Thu, 09 Apr 2026 00:14:18 GMT  
		Size: 9.4 MB (9356127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b2146f14ce9acd32759db2c4b58b0aa96f0b9a39bcc998ec0c574b4f7af125`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a0c469fc9cb466c96a6b7a65dc72474dc4e48c72d667cef319ec00410bc9db`  
		Last Modified: Thu, 09 Apr 2026 00:14:18 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:a32b4f298629e988573b612f99ed7a03311851f5fe86863006b8339a6e63ab4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5ad88771b56b7444669dfe43fbc1178d34893b163258fe60da3ba11a493fe4`

```dockerfile
```

-	Layers:
	-	`sha256:b2bb30d415e973e0ab358209ce964521772ecf6951d2c496aa08112a7c116118`  
		Last Modified: Thu, 09 Apr 2026 00:14:17 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a031708803e467d97b91a4666d7ddb2fd344283d41baba870ae198b40d7ead`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 15.0 KB (15046 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:5377c325f2e677a38dd81a6618db4df283c0b163aa8c4003bc3fd3e36860fd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35959459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339a11ff88fcf4abc9de57162ebbd74759fb778478405f1f2f7336979527e0bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:03:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 03:03:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 03:04:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 03:04:17 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 03:04:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:04:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e369b5ab19c2212fd86d57eda1cf3c506c29704f544d9860de891f00673d9fd`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6669d921ff7e40cebaba94c08a71cf0ec7b2fc4651fcc1e038e5795723535c1`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f8a307634deaa96dd6de60d2e3bf8fa5cb2b8efdc9048bb3ee207d3797a73`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 6.1 MB (6121669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773dc6511e525dfa9f3ba508de6e2ca76db7b727ac06923c99b6a44efe919fa`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cc190018f9de55d4b8fcf1181885ac8b5cd049b39999592aa4198f9501e4a3`  
		Last Modified: Tue, 07 Apr 2026 03:04:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:46d304ddb6375e95dc4644cc7edc92bad5cb61f0e64de098bb3ca676cf8d8b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d94cc4d62ed8e676852259037a7643ef7cab6ff6d0664bf5a1e3ec7f949d7`

```dockerfile
```

-	Layers:
	-	`sha256:a929665e980ab68c90beabcaf6acf299c0f48cc3bedb83f9c6f5db524e0beeb6`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0059e152b4573a43d5717820ac10affa0f56ca5f425d939a7971ddb8cb35e52e`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:027025cc0b5ca751a8f2194f4a6aef0720a1bff70cc29271225adaa1e2061db0
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
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
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
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
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
$ docker pull spiped@sha256:027025cc0b5ca751a8f2194f4a6aef0720a1bff70cc29271225adaa1e2061db0
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
$ docker pull spiped@sha256:d29799b7499dd97718236dec910ca0fb21a58b93b04c13b9d32bd3972850d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829adab8d4ab1c5c9eef2ab8cd6fc3b09ac7a5b2c98b60eb750eaadcf3ca449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:31:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:31:32 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:31:32 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:31:32 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088b329d71531fcaf8b6b6b5fb05bd132488a9b146463fda72d73f3b193da77`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6327ced333146d36cce9bad13d15f14d00cfba342ef14347eb76323f377623`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f74692486d32e3c25efb4bcdbdd450b58db493d05a003140a026ba85c130a6`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 120.1 KB (120096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b377c56ed7e39aeec7320819a810cd8637819dc2c7f00e5f02f6008223d5ed8`  
		Last Modified: Wed, 28 Jan 2026 02:31:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023ec54765d4d3764e0855b6d7cfe0e2f9966db68bd933fe3f4fe6c41a2474f`  
		Last Modified: Wed, 28 Jan 2026 02:31:38 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:49494f0bf8ea2a9ac91bc338facd2f7cede025b28b7848656878d7ce0deadf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16387e224ee0b4762e3111436b2fdc3a8bfebe61d796cc65af094da1ebf76cd0`

```dockerfile
```

-	Layers:
	-	`sha256:bdc547d749394448a39cd679c285ba250424589df32f26c116cdc3bca37fedf9`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f968b5a19cf7dfb341a81ce64526ba67dbdecae7dbd82f7332ab1f24bf7e26a`  
		Last Modified: Wed, 28 Jan 2026 02:31:36 GMT  
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
$ docker pull spiped@sha256:0e7e07e5944d0951da4949f8298cdccfa6ec9395c2d0ddf983aa7f40bf7807f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00565f6907e5ae385b224d048c255c22407d6a59d79533da4912c486d4ee1360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:56:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 29 Jan 2026 18:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 29 Jan 2026 18:58:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 29 Jan 2026 18:58:38 GMT
VOLUME [/spiped]
# Thu, 29 Jan 2026 18:58:39 GMT
WORKDIR /spiped
# Thu, 29 Jan 2026 18:58:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:58:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:58:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85b2fc2b9bdc2a30eea3483d034231cba4cf794b774e9c668e43189f965204b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35d458c7098a7c5f24f347a75cf6930f742a2e14ae40067defc23e63d57b5`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbaf165e7e5cf59739b8e5317789f9a907da0dc26f3803ae533e05f7a2068e`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 98.9 KB (98867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0973003e6d2e757a9f14bfb9ab4d4b6be0abf8bbdfa7a9b699232646e0df6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509faeca8d8af4689f4b76d19f92f0deeb48d08e62ab656d5ad988fe97b48e9`  
		Last Modified: Thu, 29 Jan 2026 18:59:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45c5a2bccce0c2d968718cdc5b92e2d54486ce35d6f21169c8e2975138906721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3828726b576d70b513dac001f2810887cf67c235a77086291ebdeb6df7a249f`

```dockerfile
```

-	Layers:
	-	`sha256:53e8f0117ebdf17125860003417afad58a90f091d2b04b6763e9b4ce1899228b`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edfbeca58a13ce30fdd21ef302873aa05c28498d058231b777fe51653a06eb6`  
		Last Modified: Thu, 29 Jan 2026 18:58:59 GMT  
		Size: 14.3 KB (14304 bytes)  
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
$ docker pull spiped@sha256:22bd43d626a442991c4cced930625aa55b241be778f28fb46221103dec40dc7c
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
$ docker pull spiped@sha256:a3e2ba12f248fe7dfe821e5c4544f956fb8f6982156435656feb15535e65d879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36825780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507c88cfcc4672ac607c8eec5726dd8f9c6e695d9dc0a0aef8ca23840e6b9b92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:41:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:41:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:42:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:42:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:42:00 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:42:01 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:42:01 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:42:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241b70042111b50831052e463f8c36f46e7cd27bbbaeeed9faa54a50b21e9d5f`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d85b3b2421b3b5fc68393c5f2d9d82431804098deacda83193e6328d87d035`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a478cf2b7a922f008a2c3ed2a49fc619d7713e19830fc721e0b36f3d6c21099b`  
		Last Modified: Tue, 07 Apr 2026 01:42:08 GMT  
		Size: 7.0 MB (7047768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38f7c4fcb0c778cabd304b72bd2dee1718d36452be6e7b3e20fbd170a9c41f3`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5733502a2a646bc6a97ca03fb756b92d359d8ed6912eef64a0adbc0644477654`  
		Last Modified: Tue, 07 Apr 2026 01:42:09 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:aa2c0709b2a7dd96572681c842e0c3ef3a22be0d0d6815caf966a6cee2864ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f728528d821e69e56c3dd90e8dc75257bcd13318fae4a795b6e9dbd4b3990e0f`

```dockerfile
```

-	Layers:
	-	`sha256:1a4e5a8e2b699289058f143b6a6630b2df64eec04b5144c6d27aab53eab8aca6`  
		Last Modified: Tue, 07 Apr 2026 01:42:08 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b191389c378d65248dda301c92386106c1e990d3eb3ff583b816c1ac789788f2`  
		Last Modified: Tue, 07 Apr 2026 01:42:07 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b9752fa7cebde10760dc4a92cf1add0d71389536c0fadc9103ee7ac42d3c28ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33735293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753206012e26cdcfc67aba0e15122baccaa308a313e45dfa421117302dcfbca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:44:14 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 02:44:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 02:44:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 02:44:44 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 02:44:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:44:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:44:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db2337a9daf6c7349a4348c46b064f676d7db505cf3ecd9631b722f5d7efd1`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a999823a7c579778c69b2165050956ebbbcf97d033a17c25bd1b33b92ce7c6`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7befd368637b8c0d89cbaa145cb5758fa39c0996d6b90b5d8aba208dfd13288`  
		Last Modified: Tue, 07 Apr 2026 02:44:52 GMT  
		Size: 5.8 MB (5789110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c838cdbcba0fbcd482e6aa549e3c5aa9ea6c7725ec3ea39ad6ec4bd01b2fb1`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a29b6bf38b8a6ed8469c97a62b1355ed1c8de06bf3ab3175ddcecc97b4db0`  
		Last Modified: Tue, 07 Apr 2026 02:44:52 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:bdfee195558b3b0ea408e01d2c0de4f907563058275ffcb0dcc4a97dce9c61f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bd1dc54b4dcdc3531b00acaab110439c43129e708ba848cd76425ffdb9c985`

```dockerfile
```

-	Layers:
	-	`sha256:cfffdf2f2bc673d0962ccc72948fd40b9c494459522d2b0d880f00274ce64421`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0157165ff7842ac2ed5a4887f2f6221fe1432566b1363edbb1f78ccce99187b2`  
		Last Modified: Tue, 07 Apr 2026 02:44:51 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9a8582c92541927d6cc6b1231e3f9fc087634e8ebf740f22932ced1fa84e6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31796505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78afdb203bf64361dc4a6539eb4f7afa7db2600858593dfd37097874854af75f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:57:41 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:57:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:58:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:58:09 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:58:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:58:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4c3f24a8c67fe9d39009a981843ee5dd2f56fad9e606d7b59792acfd232f4a`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4367de839e4ddd19b09eb146c6add980bc3bc6b37f896557dd766f7a91a3eb`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c921174dc4f14b12d5e1373ba4e9dcdce0e25101dd048cf97d127f7f988706f`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 5.6 MB (5584481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff37b32652071edf1c320151ec362df4ce897d0e942b56853e314b2cb7d9a77`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1025fd50b8baa88dd6f89830e0c4249202bbc1703d69bc2afa5e02f19070b2d1`  
		Last Modified: Tue, 07 Apr 2026 01:58:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:a1c85e8d160123fe75e4e428de5030c34bced1afc1a222176e42a03353f7ca86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74665bee3b6f99ce7b5b54b5f2cbc329376ebb705376c95223459b535aa289d`

```dockerfile
```

-	Layers:
	-	`sha256:61d35ea2bfc8c09cba13551b4ee3ad0700517cece547096fc39a29ce4ba2d7f4`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed71dff4cc1ad51bf4c38a0c7b1cadb1287246ab35f0bec2a619e3d9e35b66`  
		Last Modified: Tue, 07 Apr 2026 01:58:16 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d30ebc6ea0efd7067ddd5465200f316680955d148ec7ee740bf77e9f26776d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36374635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028134019e80f1ad2729ce283b69e420a7e87c10b1f90704f60aba8c66640d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:44:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:44:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:44:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:44:35 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:44:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:44:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:44:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78386c1f339617a7514f5c5850a35392c79415338c48df95534347bfb66dbd`  
		Last Modified: Tue, 07 Apr 2026 01:44:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbe44cc1411ff7b718c6c32487316d0de9e2e84d5b71f1f50889d436557da5b`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36237e30e614284ea3149f330180e9abd28233c7e56ea1ee5978407cd7e354e9`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 6.2 MB (6233711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d3fe23a684c92d3b9df580f910367a15e1516c0bce117cd01717a0fd1f70d1`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db60e764a9b2a2389e56088a56c0cd50608a83c4e463f881b7b9a4d652f11f32`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d2830d9ee8319621f2b65a684225f90d0eb138954081954ef653581ef6357953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b67e488a21abfb3b8a3ca6b05ed397275015cb79280117e1e286cda4047440`

```dockerfile
```

-	Layers:
	-	`sha256:4023c6866b5098980de4a82760fc4a5c5b5c437ad84d91ba4218736f94211056`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 3.6 MB (3621296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63ada7739a03a3c861e386268b5489839840bc30290399ce78d105ca004e36e`  
		Last Modified: Tue, 07 Apr 2026 01:44:41 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:fdba21dc9ed99ac757f7db3552f2fb3c7ee3f40ba0c5833d61065da583f5c075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37735973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d069883d47f5c8b13decfe94a8e20e7cbbb45a7ffb60b8b0d1b4656b2adf4e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 01:45:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 01:45:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 01:45:57 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 01:45:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:45:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe1f9ad83d46736d171810638a97d75cca03c9b4a511520e2a5ea7bf236ec1e`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec45cc8c1429a10738a1b8cf80de924f317f30d79ab8f16df7c111572459b25f`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59588fe2cad3f5d3ed274dd5340d2d0264ab0ac22df03bfd63ba5580f94f85f`  
		Last Modified: Tue, 07 Apr 2026 01:46:05 GMT  
		Size: 6.4 MB (6442351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b43e60f19cb0ad95d1a96d3820660d70997c0076652baa3e077fb08394f45`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef277f865aa5227526a7f75b1acd5208e7a1f665263f54e1623d399e5e8a399`  
		Last Modified: Tue, 07 Apr 2026 01:46:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:21d075407fe32f0f730f50e2593e33a2fcec94f04da56f4750599400588d7956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ae5cab45b127fae7709c8c41698e534cba9b7c6cc6fab44c58cc57af01390c`

```dockerfile
```

-	Layers:
	-	`sha256:616d8e60678ffc448b015c93ea6b71f155e346c6803b5e8ce2399868bd7dc4ee`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c1bebdefb8ac4db5dee341d7b7a17d565afa0a140b5f4dc8c348c2c81f3ba0`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:c0a453063892828d0fb816889260b2c5f99fba2b9edc331339d6d224700718a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40436067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580742e53478938982c276ba05ef6aea1feddc27f3166c8f5c5d7ea6df4b4b5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:18:54 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 04:18:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:20:04 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 04:20:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 04:20:04 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 04:20:05 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 04:20:05 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 04:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 04:20:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75139b25c1163efa600a1092483a109211fbe92ad95197d07fa71ef7a03aa199`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98f08d8269e6b0be51b2c864c4eca24109b6b99713bda09c8e9c57203dddf0e`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7564825c015f3bef02badeecdb11be2e23c0fe99787e570b94cdfdcd4b56352`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 6.8 MB (6840674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0746a2a48a65f4c41b7be26456f56607ee731936781c5a9498e7f6b60edaaf51`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d264dd18051fec52d9e9d773ab8dc08ab88bb65721a3cd1f5dd0d4b9024a0497`  
		Last Modified: Tue, 07 Apr 2026 04:20:31 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:2449d893ea7867f05190ed3b87f5acc9415eb7dba16b1291ef9c71fa8b845c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9538c764a62583ed14715893afb0bbc4d286a569c9ad2a652b0c2de87beae9b`

```dockerfile
```

-	Layers:
	-	`sha256:a7cae8514458b1fc537b1985abd7c9c51a3e60670412e57fa09b99d0c32c03c3`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 3.6 MB (3621997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7f6a424912f840da5acc7994e0b410d77ea2da4b2aee5b8dfaab3e56dc0b6b`  
		Last Modified: Tue, 07 Apr 2026 04:20:30 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:62524bfd97797aa199c180642403ffaba659b996e9789af10309c736a0958c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40298595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a83d0d12ce259b66549d2f71ac7d9f81ea279ef1f6586189805ecdeccce9982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 00:09:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 09 Apr 2026 00:09:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 09 Apr 2026 00:13:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
VOLUME [/spiped]
# Thu, 09 Apr 2026 00:13:03 GMT
WORKDIR /spiped
# Thu, 09 Apr 2026 00:13:03 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 00:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 00:13:03 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353d16b8234198686b3afc079e10ceb632aad857a9760042d6f813a4792893a4`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6838fc2cc2ae3970bd10a42658413616714e7526ffc0eefa5b7f6739a1b26ce`  
		Last Modified: Thu, 09 Apr 2026 00:14:17 GMT  
		Size: 2.7 MB (2665148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8b54dc228fa06c8f98b630722d41503ff93919fa303e7785590ff38951c2cc`  
		Last Modified: Thu, 09 Apr 2026 00:14:18 GMT  
		Size: 9.4 MB (9356127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b2146f14ce9acd32759db2c4b58b0aa96f0b9a39bcc998ec0c574b4f7af125`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a0c469fc9cb466c96a6b7a65dc72474dc4e48c72d667cef319ec00410bc9db`  
		Last Modified: Thu, 09 Apr 2026 00:14:18 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:a32b4f298629e988573b612f99ed7a03311851f5fe86863006b8339a6e63ab4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5ad88771b56b7444669dfe43fbc1178d34893b163258fe60da3ba11a493fe4`

```dockerfile
```

-	Layers:
	-	`sha256:b2bb30d415e973e0ab358209ce964521772ecf6951d2c496aa08112a7c116118`  
		Last Modified: Thu, 09 Apr 2026 00:14:17 GMT  
		Size: 3.6 MB (3613403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a031708803e467d97b91a4666d7ddb2fd344283d41baba870ae198b40d7ead`  
		Last Modified: Thu, 09 Apr 2026 00:14:16 GMT  
		Size: 15.0 KB (15046 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:5377c325f2e677a38dd81a6618db4df283c0b163aa8c4003bc3fd3e36860fd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35959459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339a11ff88fcf4abc9de57162ebbd74759fb778478405f1f2f7336979527e0bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:03:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 07 Apr 2026 03:03:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 07 Apr 2026 03:04:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
VOLUME [/spiped]
# Tue, 07 Apr 2026 03:04:17 GMT
WORKDIR /spiped
# Tue, 07 Apr 2026 03:04:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 03:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:04:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e369b5ab19c2212fd86d57eda1cf3c506c29704f544d9860de891f00673d9fd`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6669d921ff7e40cebaba94c08a71cf0ec7b2fc4651fcc1e038e5795723535c1`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f8a307634deaa96dd6de60d2e3bf8fa5cb2b8efdc9048bb3ee207d3797a73`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 6.1 MB (6121669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773dc6511e525dfa9f3ba508de6e2ca76db7b727ac06923c99b6a44efe919fa`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cc190018f9de55d4b8fcf1181885ac8b5cd049b39999592aa4198f9501e4a3`  
		Last Modified: Tue, 07 Apr 2026 03:04:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:46d304ddb6375e95dc4644cc7edc92bad5cb61f0e64de098bb3ca676cf8d8b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d94cc4d62ed8e676852259037a7643ef7cab6ff6d0664bf5a1e3ec7f949d7`

```dockerfile
```

-	Layers:
	-	`sha256:a929665e980ab68c90beabcaf6acf299c0f48cc3bedb83f9c6f5db524e0beeb6`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0059e152b4573a43d5717820ac10affa0f56ca5f425d939a7971ddb8cb35e52e`  
		Last Modified: Tue, 07 Apr 2026 03:04:28 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
