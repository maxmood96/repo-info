<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.3`](#spiped163)
-	[`spiped:1.6.3-alpine`](#spiped163-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:f504c30db9ca75bf547f89bef1cdf557c6d2a3dce57fcf74d43de04f8de593ff
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:4d6064fa1b632e22bdce3cffebf989475f6e2be0eaf6a36498a2e4e28b228d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37097677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54460248729376bb05e1602bb12f5b0a9aa0e710990826e3a73faacdd062b547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7196154f35d46a29a47883173fde58814cfb6bb853a3c4a61cca9430cf1f8159`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd3a971ecf92f9d804a86b505518d4c7b4542035f10e32e0b0c1482acdb10b`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 2.4 MB (2401342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf2c3578328d143a0c13eac4322d3a7ba1c09d0bb431e3fb8bccb93fac7409`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 6.5 MB (6482493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c051f65857ae1a80b319d09976092265d695e37fb3b0c69fcf014ec2643d7`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7250acc401675038e92dc4a884eee09833a19e8adba51f183326d29fcc2ca6`  
		Last Modified: Tue, 04 Feb 2025 04:23:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:697c33cad9224e7f7763c4dbd3db4457416e6f1d07de6625f41e20e5c83072e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbac9dbdf7a50bc8d58d8959455a7fb5e0547b6627570b17db660d45b6effacd`

```dockerfile
```

-	Layers:
	-	`sha256:b4b40f46007e4399d9b995de98a93ac8be64ebfc2a39c66d9abbfa5512688d01`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3522078defe9a24dc1fa0dc53832d9fb3206f653efe38d4cd9d5839c6fc70e`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:6e9ed3ec5459996a7edc1a2f5fa9f91294a34d39e7467e39ffafb3035ccb5c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32882064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1371b30fecc7c3db6ab766bbc4750a8751c93cabe9d75fae796aec4066ec76b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e614f72336dfb4738cbfa9d91d99d2d7008ce16b7acf879b6d9d166dd1c882`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef4a7d930f64716939f723e7ce3c4551621bfb867ac4f4e61e5b05dddfb29dc`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 2.0 MB (1997174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91afdbb82f94d4dd13401231991619b93c99ec48cdcaf0cb0ba8dce74b87642`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 5.1 MB (5146798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4af1d5f9bc51aca0b2d09e04074a8f703930c4176b241a50d5ff3492ed47ce`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddabd99982fc01efcad0872592b12613c3b224baeb5ee91a78f4dbf692df1843`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:7ef4a0bc6c9834e261cda43f045e8d5b1794274f1138907d70934884d34d5f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce6a167142fb12a6a18d59f0d97dfaa6e26415501333d6375aa3a1471ce3d0b`

```dockerfile
```

-	Layers:
	-	`sha256:c6e65141c199dc160de554a46ba815b77e0022fec048fdcf1b0fe1c6b13530b5`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fac543ba7e329c9a615af9d72772e6955538ba4abc8298e3e684fec72c495e2`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 15.1 KB (15140 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:a18f5778ca2f08846bf27be992878deb0a4c267c165517af290b69d341577d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30659675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc7bc7a0d0e4a2dcd29786ded7a4582d24affb641bf0b53d84450510c97ef44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d40b8c33eed4efe5d43b21f211ccc96a002e6246f8b80e0e6f53f45a5c1334`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f95294c83140a5f312fe0e0f3673b125c4718f4c4f531b3d58735aec00054b`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.9 MB (1855579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36310be6ec666453ebf3cbf37d05cda567f1a1a76d531826880d258eba1676e4`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 4.9 MB (4888021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ca7552106b4e46e361314d1d889c4683713c3e9d455c68cdefca8c8f6398d5`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8587687f43a65aec0c478bff612f8274ace1a6e6f519d21be92752ef5e310b`  
		Last Modified: Tue, 04 Feb 2025 10:26:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:48f395833d05679dc7e6fe62d5fbd26b2f600568d0e161f4bec8add466c41174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9242c434cb9698da41a72676a955396192dab94c1f14c49069a83938788cbf9`

```dockerfile
```

-	Layers:
	-	`sha256:88adb85aaabae3f90b457b693796e9e7deae4ca3b7d86c8280553b3f6834f170`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc48124ea568f4a829f5a6697ba88d5decfc16547dba969d09e0fc431dedef7d`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:512de4a1d89736d75c4681f2be68b9e1bab029e3c613da922eaa8b4960135a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35780546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c8f81d42835a979ac6346e5f039e31c1430d6d29427695126d2fa2751dc9f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445785d885b1d4f4c62b22f763a4c23c5ef61dbcf8561b1f373f1122a157a32`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e83c554a066c3f065b78b3307f98c54d4a3753271ce9398dcfb644a034658f`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 2.2 MB (2247024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb79cb22695e7006611aaa6075a06126c1e46b6ec26a36bc59b2024e0692bb0`  
		Last Modified: Tue, 04 Feb 2025 08:36:36 GMT  
		Size: 5.5 MB (5491103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5f8d83d3803bc3372d3b2f901b9a579d0fe0892f5c55c7ffbcb4841f2509f`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786f9a23b172afb3253a266af44a47a83cf5676a8b5fca783047e454090874f`  
		Last Modified: Tue, 04 Feb 2025 08:36:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:1f2b3b9c6d8d47ed3b1ae99990fab63995a73e145a7a7112393c86bdd9442fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f7026f2371bb9fdfe80e13f7478f933109e240f67a727773f50e39d31fc713`

```dockerfile
```

-	Layers:
	-	`sha256:6204b89f04e97cef39e578e6ed3eafaf5f4a5ad99e91966a0a795d19b52a65f6`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3efb69cc87f6603eb18e553aad09ba800952702851ad7d7d050b1d4fd1122d73`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:4396202c141ba5d4ea455a322aab810e9553b5e6a20aa108c9fc5ae7db1af7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37544085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2677d43d830f991ba448c851b51731990b47564a89016bcf439071214ccff3c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a084f64ea6359821d9e6154f483978b063d4a671e0f59b1c9ed8b46ddb71f34`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b626f23d4ddc2323109743108c51c43a1fe05d501d0e7ded9368531db9ab7`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 2.4 MB (2398651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d27cbe14fcb4784bdf925fe2c6365bc3781a5667e0f64765c11702c029adab`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 6.0 MB (5956440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f9893150c1f1ac3dbda70997a910e68f713cbbbf84707c63383aa657bef3a2`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1739d36dcea86126749ade8e41d5e26216a42e18cce7c574440f9a6dc9541`  
		Last Modified: Tue, 04 Feb 2025 04:23:43 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:190b7c5c5be2c9c5120bf3ec3d4b10e82e95f81333b011d1e2ac392b1ebc8418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d950ae27b1b619fc42683fcc84894d47c3d2f6cab9d9365e5a9081e20a870b66`

```dockerfile
```

-	Layers:
	-	`sha256:71740a47ab23a838f20e0cb6d24717d773397bf1b2a403152ef6eb81f2bdbe3d`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c92219d16dbfc537787922ce2f4fe8a90c45a3e868fd697b90b6a525b1d035e`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 15.0 KB (15003 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:228e0bf1261e83b036e9df0c5b3ca867223a333421a2890b3c3720ea81c5a1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36142318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891b41e80be95bdb58c5d4b79cb3ec32056f765cb389c9eac81badc4bd9c27b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e2b18cfa28e78209d84a30bbacfa4539a85ee636689c58538621e572a4133b`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d49f8446481472986048351b40e96fcad9c44128630158e4319ae5b69b2feca`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 1.8 MB (1841114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0200fc9cacb2091aa304f8f172882d407f93a42a059f02ffc2ae0acaf682671`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 5.8 MB (5813078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2152b44d1116d5c1168680113e8fdd466ebcc7ee99c07fdfe1b3fbf39ba7e`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dac11d6a32393a766da366844f6656c0ef0a5443e7206d484655d856a5fb49`  
		Last Modified: Tue, 04 Feb 2025 19:23:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:fcac27653c73b5b7610b7b2e0c943a12ae91de1da06633457d0c9cd6b627629e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855a8edc4f8b24033f2315611577aa502a4cbe311c66c2391b1919db8af2f36c`

```dockerfile
```

-	Layers:
	-	`sha256:a6003ae2d7ac2094ff93c250171d0ca098c7a1e6a808c1c7bd1d6deff6bdadd8`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:978bfe51b8d6c8f3381934ea41c373766dfb48b535bba6ee5f243a193006a387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0540b6aada3775e3adfd4af21f094aa6460b9f09c3d305374563039cddb310e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaa4db2f41f33b473ee9e3d23526c2a5c3d06e4c63d975f8c329650781bfc50`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9aa243ee14d1187269f15a51bdd0121c76f084de8c950caf576d98b70e463`  
		Last Modified: Tue, 04 Feb 2025 07:09:55 GMT  
		Size: 2.6 MB (2582094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb78a29a1de352d83b7220b0199eb455f02534bd728d801150686e7e720a273`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 6.4 MB (6440730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca2cb4355672884568c1eff10a52aae16dac2db14e387628247926c8e48cdc`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4693e453a57e0f33af4fc1efea3a42a24e6381418d131d5aae599efae23f4eb8`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:c3db218145823880cb4767205ac0d1924a1ea93de5ec49956ff101d21069b0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d9f6f6871ede0f731ed47717e49df6baa968b54038d23c64b6a155a3d51f3f`

```dockerfile
```

-	Layers:
	-	`sha256:69b861da7d96b4f3975dc9cd80514ce15bc9a8d5bf9ab3fa2d4fe527e805d2cf`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d5bc74f88a190910aebb2f129af625cf7b0d44d488bf251a42bd4bda622586`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:d602741ec001ec0bd0250c732c173274ba73887a8329ae21abc99750c26dcf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa781d6e5a453fc558205ea8ece3ac80a2ebe01b811e5ee602ec0053c7672138`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a6e7d0775375fc3d1e148728013c288c159edf09d7f89268dbd2b94adb02e`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3dd0162c40e5529113c4043b6a295aaba4477a5614ea6b37101eae051fae91`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 2.1 MB (2068737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89371216de8a5f913d8b5e84022a8820b75c22312a485ed5d4532ec0cc3ad89f`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 5.4 MB (5391937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c639f4e3d3bb15db262a0e635d9bfa87307da8ab93f4de0186dd76242d0bbf92`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d7fb587195e97fb81398a0cda1fed9beabbc7bebb633a6b41d52053b99a1a3`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:c571df89a1b0e77226d84a4ac833f4dda8adf0e04737412c9fdd4785a2c870aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991662535cd5d6a339176b8c9b909132cb73a6c2bebc27790b05b5987af78f30`

```dockerfile
```

-	Layers:
	-	`sha256:69a67dda4c3fd05bb160600c2ea45317f2ff7d014280d03aabc69b0795186b0b`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe307bfbbadd67d2deae85a17c6a372d6f7cce95ba0fedfa0d63d0b641fdde55`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:cff1ff69fc6f8904043ef5d9bb654e468a38fc671dedcecd1f568a1d61f1d634
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
$ docker pull spiped@sha256:2715ebbc20690dda6d438989f61f4eb4fb11162e932ba70cedc0c7f12b3c26f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ec86461245d72383c5662f686c25016cc299d589def9478af4205b484492be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b181c716ebe4d13478b33f2488cb40b954ba24081d61c5bc9d7f0605ba9d113`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ded10ce7d7c8e5d5eb05c5a7d5246a6a045996ee4f18dcc322d6600e68cd81`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d46a15f052086577ecb502311cd9f4d176cd407ad00862e11dd7d6f8c2a868`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 107.6 KB (107614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b34221300809a19087f5d67a70e8167a72247feb52faa8c58a878f5af671d3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89b10c18fcccf667446750b679723f2821a55bf5612caacbb8c510578e77e1`  
		Last Modified: Tue, 28 Jan 2025 01:28:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6a640be7b02114db4704050ac59d1be28b1b8f1a10f0ce877865a41933bc6d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24283cd9a878c00f69d37c768fc27af4fe97d6fa56a0174f6b441c10746770b0`

```dockerfile
```

-	Layers:
	-	`sha256:f6e7df028e10774143b75638cf9a91ae4484ad9be9705a3ab7de160bfbeab308`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307857c2fc1847cc55f2ad19b9b6647658c5135c8b20a447ca114dfaf6cdb9b3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:6f9bbe66f9f9620c0aad2b8b464d5f0912510b5fbbcce31e1458c51d8bdc36a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b357cad96475791645ca664e952dfc2be3a80db4daa6ebc50db2cdb2426d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0919c3817d8379bb41e1be06c4a9ce8b781a7c46fd9a118114bab8de444770a2`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 89.1 KB (89138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e0d0ce3aa2cc891355694b9f4548ada6aa0f587ac1f8f95ff08b62f092ca3`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6048abcd79b046de58bebf91b3eb0b6d1d3cdef973e93188a86da2ad1ffe65`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3f840c3a9d83f847e5bb8879ed8d0fae64e2ab7849ae389421052f6925264c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a31c54f0008afb75dde7c016b9771c6f37268270d33d98c57f6d4c46be550c`

```dockerfile
```

-	Layers:
	-	`sha256:e415d942102ceb25c19c03d57e7aad5f3e309c6a8aebe7422ef678a4f6a8c3c4`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:12817cd6117bed3cdf9e7e4b52de247dd1a87d2876d8dc7434e5115f0fc9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cba0ff108ef4a8e8108d49bf7ccd596afac4a82110a7c14e80a001be5fa5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51637362b800c4f96d7abb05ca7529a770947ee4b1e9623b35af4b936195f4a9`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 81.6 KB (81648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15074482593cb5d5f416eda5eadebe75a10ba5005975523c4c34e81f46e618`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71199d0efb2f82ed5530667b5595dd7a34230b43f8dd94dbe9c99654b1b9ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5a94554ddb9da6514578c1b09075a2b4ab9c4410f3e3e231bae96919d45f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f515b3bed3192db05a2ad5b870421a369f4a33d6b7164dac00142ecf5bc150`

```dockerfile
```

-	Layers:
	-	`sha256:49f4a9e142d4f0bbdb2b6f12f002efa4735f8926b13589ba3a9a5a9ce1a027ef`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c72de5bccb3b20f12aaba84aa22f33c24e0ef214459867af7cbe28470672cb2`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:7bd7eff848bd7ecb4ebeafabcab07a01e40580fc27ad865b3b7dc5c3e8307bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46380b40fc8cf495b0e4fe6bb439caf833e2bbaf42e79ccbccacbd21456f38f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966823473fa57bd0c6c045474918109f56a52c519aa3ff2bbeb53a9bd43f890`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 100.6 KB (100555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487e20745df540295ba2a7d5c3230edfbc1657b671f349f920b261416279acc`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477716625dcd64617f5279d092cb746cef8275524ced557b548fac120fd1e9d`  
		Last Modified: Tue, 28 Jan 2025 01:41:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bf674933baf7156a187fcab52df270880af433ca3e590a2d21c400137e505bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e08d169c62b2f76c8f3d4eae8033be48d397c61a9f6edf7ecbdff2e94987c6`

```dockerfile
```

-	Layers:
	-	`sha256:c463f59b08554468e33ec7d67e5bf358a4422df9ba9c9e8a5c85545acbf01205`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55be9c8a835f959acbc00acf5a1a31119a99c2d3a92aba2088b8f3f0b9b7f56c`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:b310c392ab6f14391fb45b5af6ea15dbcbd23076e497d3d94c110d7b2087f4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbcf6cf269492e27066e7c7bbcb967e81247f0f3f3d09284672b28db7077ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551001421d38a34944d1a96a5df258e75c389ab10abd35456cbb26915537f7fd`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72f77ecf249ccd9496811e0eb3c0cf489c7b7fdbfa9b09a800fc23ce9a5b86`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78fa624f51e7a9f83ca9c71b40f866f13ab95ae1d6fb7f7fb39888ee08b23f5`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 120.1 KB (120111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b172e6f71ba4a3cd0b9d569cc026414ab5ff72c2c999047269348e63b5abaf`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f42fb7496f67e41461243ea1a96721d75c60e36c3fc0bc0cc31f4a05a0a3f`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9927a6df5d8b7dbdb338658808aeddad5564ef5897b94b692df5dfa29b9abdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d905998f2bfd41e52ca5677826d1ba128880dee6ab953a307411406c31b587`

```dockerfile
```

-	Layers:
	-	`sha256:aef24c41d2f2fe02d3f60245a4d8614488af106b27f1694638bb0aa63affdeec`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e634c06318ef153f0dea3d1996b85ebfa8b5d1ae392ac0ae4aba4ce249a2d7ee`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:884a0eb6ba4f64c3edda016b28d4bd99dba5200f5af5ac9cb6b72f18cb3a3a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a09f14f9a1c5c8a4bc39f97cc1d4dfc2da04ebc3eb0e1c14ee25ecf135a583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2bb56ba626edfb899d02de6e190e018998d7573a673f6db87d5ef30de0a050`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 112.6 KB (112648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e93d7242196ad9ca14b560ce78c345dfa536c1a35de8044919beffdf4eb97a`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e06feef4b6941cffa38f96ec7bf4e23040ea0baf7cf6f0a7345c46675eff3`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:02029f95376d43c51ccddf3f8c8bbebb0671c8774aacfa19d44aee40f4773161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4efe04e204e62e8c95b99341d61fcd033d068bcbce5868ae0ec1685e9f9da3e`

```dockerfile
```

-	Layers:
	-	`sha256:f198a76291582efc4f722539762e32a43b96a2acfb2de57f18adfa903c9b3c57`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32d956ebf079b702220519e8a308783736857197d7766e995bfbcd8c71dbf2c`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:756e00d72198e903bfd6356e80496c2936c64fa26149b3662c09c044393ac715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b076b4ea8c2964765a22bf8c5d8b2fb8141f171e1f335b628572524c3ab7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d4da436692d4ab0fd5035ee54eac03b05bf24df9aa3304a4cbb3e6bb7fb7de`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 98.8 KB (98808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f3813ff058c0963785dcdc5c5f860f00840874673c02d724b273f844d53c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d897b6a73cbb856ebfd058f311b8f0e39512fdede0d33460f38db93bb89b6c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:877a9cd3fe26f402674032844c26b7149200267a47a431963b72e3b4563d519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b37c1a9028694f866e7acc219fbf431ce5b97965a6f5489a14f064c84a12b1`

```dockerfile
```

-	Layers:
	-	`sha256:40546cca6e89cde845ebe9184ed940f3b4f38ba1e18049e3b36b047821e42722`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:496d1116424a4c78bad3fdd46c2db89305089a904ff0d42fcd07ffca4576a0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32ae085c92ecf8421e7f161ab96951c317b5e771993504a3e09c8db10414930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398f6409117bd2a57c6b304f740badcea613c5def606a7c072bcd0c73b061e0`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 96.9 KB (96911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ed7682792c020e13d8b547fdbb8c43a4956cb69969b8f5a2724202bbcb39d`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff53239a6486b270ef8a57e32718cefe901786526573b780eb054d1ac053dc6e`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d66b26cdcd77f8b4437bcb47a340f63d583e754a794e2a822931eafa72152360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cdd7bbb43e56276987d1ae0048a6f92a4bca0ccdee9e8e670ddb9ea5e16cb9`

```dockerfile
```

-	Layers:
	-	`sha256:6fe581f275230ca3b53c4a9c2f8f4690c4edf45359ead5089d277953f8872d2a`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0280df9fd96cadb1c6e05a657e4d4caa094e820e2a85ddd2df85b36c0363d18`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:f504c30db9ca75bf547f89bef1cdf557c6d2a3dce57fcf74d43de04f8de593ff
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:4d6064fa1b632e22bdce3cffebf989475f6e2be0eaf6a36498a2e4e28b228d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37097677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54460248729376bb05e1602bb12f5b0a9aa0e710990826e3a73faacdd062b547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7196154f35d46a29a47883173fde58814cfb6bb853a3c4a61cca9430cf1f8159`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd3a971ecf92f9d804a86b505518d4c7b4542035f10e32e0b0c1482acdb10b`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 2.4 MB (2401342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf2c3578328d143a0c13eac4322d3a7ba1c09d0bb431e3fb8bccb93fac7409`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 6.5 MB (6482493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c051f65857ae1a80b319d09976092265d695e37fb3b0c69fcf014ec2643d7`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7250acc401675038e92dc4a884eee09833a19e8adba51f183326d29fcc2ca6`  
		Last Modified: Tue, 04 Feb 2025 04:23:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:697c33cad9224e7f7763c4dbd3db4457416e6f1d07de6625f41e20e5c83072e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbac9dbdf7a50bc8d58d8959455a7fb5e0547b6627570b17db660d45b6effacd`

```dockerfile
```

-	Layers:
	-	`sha256:b4b40f46007e4399d9b995de98a93ac8be64ebfc2a39c66d9abbfa5512688d01`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3522078defe9a24dc1fa0dc53832d9fb3206f653efe38d4cd9d5839c6fc70e`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:6e9ed3ec5459996a7edc1a2f5fa9f91294a34d39e7467e39ffafb3035ccb5c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32882064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1371b30fecc7c3db6ab766bbc4750a8751c93cabe9d75fae796aec4066ec76b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e614f72336dfb4738cbfa9d91d99d2d7008ce16b7acf879b6d9d166dd1c882`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef4a7d930f64716939f723e7ce3c4551621bfb867ac4f4e61e5b05dddfb29dc`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 2.0 MB (1997174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91afdbb82f94d4dd13401231991619b93c99ec48cdcaf0cb0ba8dce74b87642`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 5.1 MB (5146798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4af1d5f9bc51aca0b2d09e04074a8f703930c4176b241a50d5ff3492ed47ce`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddabd99982fc01efcad0872592b12613c3b224baeb5ee91a78f4dbf692df1843`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:7ef4a0bc6c9834e261cda43f045e8d5b1794274f1138907d70934884d34d5f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce6a167142fb12a6a18d59f0d97dfaa6e26415501333d6375aa3a1471ce3d0b`

```dockerfile
```

-	Layers:
	-	`sha256:c6e65141c199dc160de554a46ba815b77e0022fec048fdcf1b0fe1c6b13530b5`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fac543ba7e329c9a615af9d72772e6955538ba4abc8298e3e684fec72c495e2`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 15.1 KB (15140 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:a18f5778ca2f08846bf27be992878deb0a4c267c165517af290b69d341577d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30659675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc7bc7a0d0e4a2dcd29786ded7a4582d24affb641bf0b53d84450510c97ef44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d40b8c33eed4efe5d43b21f211ccc96a002e6246f8b80e0e6f53f45a5c1334`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f95294c83140a5f312fe0e0f3673b125c4718f4c4f531b3d58735aec00054b`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.9 MB (1855579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36310be6ec666453ebf3cbf37d05cda567f1a1a76d531826880d258eba1676e4`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 4.9 MB (4888021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ca7552106b4e46e361314d1d889c4683713c3e9d455c68cdefca8c8f6398d5`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8587687f43a65aec0c478bff612f8274ace1a6e6f519d21be92752ef5e310b`  
		Last Modified: Tue, 04 Feb 2025 10:26:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:48f395833d05679dc7e6fe62d5fbd26b2f600568d0e161f4bec8add466c41174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9242c434cb9698da41a72676a955396192dab94c1f14c49069a83938788cbf9`

```dockerfile
```

-	Layers:
	-	`sha256:88adb85aaabae3f90b457b693796e9e7deae4ca3b7d86c8280553b3f6834f170`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc48124ea568f4a829f5a6697ba88d5decfc16547dba969d09e0fc431dedef7d`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:512de4a1d89736d75c4681f2be68b9e1bab029e3c613da922eaa8b4960135a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35780546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c8f81d42835a979ac6346e5f039e31c1430d6d29427695126d2fa2751dc9f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445785d885b1d4f4c62b22f763a4c23c5ef61dbcf8561b1f373f1122a157a32`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e83c554a066c3f065b78b3307f98c54d4a3753271ce9398dcfb644a034658f`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 2.2 MB (2247024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb79cb22695e7006611aaa6075a06126c1e46b6ec26a36bc59b2024e0692bb0`  
		Last Modified: Tue, 04 Feb 2025 08:36:36 GMT  
		Size: 5.5 MB (5491103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5f8d83d3803bc3372d3b2f901b9a579d0fe0892f5c55c7ffbcb4841f2509f`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786f9a23b172afb3253a266af44a47a83cf5676a8b5fca783047e454090874f`  
		Last Modified: Tue, 04 Feb 2025 08:36:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:1f2b3b9c6d8d47ed3b1ae99990fab63995a73e145a7a7112393c86bdd9442fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f7026f2371bb9fdfe80e13f7478f933109e240f67a727773f50e39d31fc713`

```dockerfile
```

-	Layers:
	-	`sha256:6204b89f04e97cef39e578e6ed3eafaf5f4a5ad99e91966a0a795d19b52a65f6`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3efb69cc87f6603eb18e553aad09ba800952702851ad7d7d050b1d4fd1122d73`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:4396202c141ba5d4ea455a322aab810e9553b5e6a20aa108c9fc5ae7db1af7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37544085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2677d43d830f991ba448c851b51731990b47564a89016bcf439071214ccff3c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a084f64ea6359821d9e6154f483978b063d4a671e0f59b1c9ed8b46ddb71f34`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b626f23d4ddc2323109743108c51c43a1fe05d501d0e7ded9368531db9ab7`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 2.4 MB (2398651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d27cbe14fcb4784bdf925fe2c6365bc3781a5667e0f64765c11702c029adab`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 6.0 MB (5956440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f9893150c1f1ac3dbda70997a910e68f713cbbbf84707c63383aa657bef3a2`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1739d36dcea86126749ade8e41d5e26216a42e18cce7c574440f9a6dc9541`  
		Last Modified: Tue, 04 Feb 2025 04:23:43 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:190b7c5c5be2c9c5120bf3ec3d4b10e82e95f81333b011d1e2ac392b1ebc8418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d950ae27b1b619fc42683fcc84894d47c3d2f6cab9d9365e5a9081e20a870b66`

```dockerfile
```

-	Layers:
	-	`sha256:71740a47ab23a838f20e0cb6d24717d773397bf1b2a403152ef6eb81f2bdbe3d`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c92219d16dbfc537787922ce2f4fe8a90c45a3e868fd697b90b6a525b1d035e`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 15.0 KB (15003 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:228e0bf1261e83b036e9df0c5b3ca867223a333421a2890b3c3720ea81c5a1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36142318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891b41e80be95bdb58c5d4b79cb3ec32056f765cb389c9eac81badc4bd9c27b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e2b18cfa28e78209d84a30bbacfa4539a85ee636689c58538621e572a4133b`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d49f8446481472986048351b40e96fcad9c44128630158e4319ae5b69b2feca`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 1.8 MB (1841114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0200fc9cacb2091aa304f8f172882d407f93a42a059f02ffc2ae0acaf682671`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 5.8 MB (5813078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2152b44d1116d5c1168680113e8fdd466ebcc7ee99c07fdfe1b3fbf39ba7e`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dac11d6a32393a766da366844f6656c0ef0a5443e7206d484655d856a5fb49`  
		Last Modified: Tue, 04 Feb 2025 19:23:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:fcac27653c73b5b7610b7b2e0c943a12ae91de1da06633457d0c9cd6b627629e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855a8edc4f8b24033f2315611577aa502a4cbe311c66c2391b1919db8af2f36c`

```dockerfile
```

-	Layers:
	-	`sha256:a6003ae2d7ac2094ff93c250171d0ca098c7a1e6a808c1c7bd1d6deff6bdadd8`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:978bfe51b8d6c8f3381934ea41c373766dfb48b535bba6ee5f243a193006a387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0540b6aada3775e3adfd4af21f094aa6460b9f09c3d305374563039cddb310e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaa4db2f41f33b473ee9e3d23526c2a5c3d06e4c63d975f8c329650781bfc50`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9aa243ee14d1187269f15a51bdd0121c76f084de8c950caf576d98b70e463`  
		Last Modified: Tue, 04 Feb 2025 07:09:55 GMT  
		Size: 2.6 MB (2582094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb78a29a1de352d83b7220b0199eb455f02534bd728d801150686e7e720a273`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 6.4 MB (6440730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca2cb4355672884568c1eff10a52aae16dac2db14e387628247926c8e48cdc`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4693e453a57e0f33af4fc1efea3a42a24e6381418d131d5aae599efae23f4eb8`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:c3db218145823880cb4767205ac0d1924a1ea93de5ec49956ff101d21069b0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d9f6f6871ede0f731ed47717e49df6baa968b54038d23c64b6a155a3d51f3f`

```dockerfile
```

-	Layers:
	-	`sha256:69b861da7d96b4f3975dc9cd80514ce15bc9a8d5bf9ab3fa2d4fe527e805d2cf`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d5bc74f88a190910aebb2f129af625cf7b0d44d488bf251a42bd4bda622586`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:d602741ec001ec0bd0250c732c173274ba73887a8329ae21abc99750c26dcf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa781d6e5a453fc558205ea8ece3ac80a2ebe01b811e5ee602ec0053c7672138`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a6e7d0775375fc3d1e148728013c288c159edf09d7f89268dbd2b94adb02e`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3dd0162c40e5529113c4043b6a295aaba4477a5614ea6b37101eae051fae91`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 2.1 MB (2068737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89371216de8a5f913d8b5e84022a8820b75c22312a485ed5d4532ec0cc3ad89f`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 5.4 MB (5391937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c639f4e3d3bb15db262a0e635d9bfa87307da8ab93f4de0186dd76242d0bbf92`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d7fb587195e97fb81398a0cda1fed9beabbc7bebb633a6b41d52053b99a1a3`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:c571df89a1b0e77226d84a4ac833f4dda8adf0e04737412c9fdd4785a2c870aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991662535cd5d6a339176b8c9b909132cb73a6c2bebc27790b05b5987af78f30`

```dockerfile
```

-	Layers:
	-	`sha256:69a67dda4c3fd05bb160600c2ea45317f2ff7d014280d03aabc69b0795186b0b`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe307bfbbadd67d2deae85a17c6a372d6f7cce95ba0fedfa0d63d0b641fdde55`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:cff1ff69fc6f8904043ef5d9bb654e468a38fc671dedcecd1f568a1d61f1d634
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
$ docker pull spiped@sha256:2715ebbc20690dda6d438989f61f4eb4fb11162e932ba70cedc0c7f12b3c26f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ec86461245d72383c5662f686c25016cc299d589def9478af4205b484492be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b181c716ebe4d13478b33f2488cb40b954ba24081d61c5bc9d7f0605ba9d113`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ded10ce7d7c8e5d5eb05c5a7d5246a6a045996ee4f18dcc322d6600e68cd81`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d46a15f052086577ecb502311cd9f4d176cd407ad00862e11dd7d6f8c2a868`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 107.6 KB (107614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b34221300809a19087f5d67a70e8167a72247feb52faa8c58a878f5af671d3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89b10c18fcccf667446750b679723f2821a55bf5612caacbb8c510578e77e1`  
		Last Modified: Tue, 28 Jan 2025 01:28:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6a640be7b02114db4704050ac59d1be28b1b8f1a10f0ce877865a41933bc6d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24283cd9a878c00f69d37c768fc27af4fe97d6fa56a0174f6b441c10746770b0`

```dockerfile
```

-	Layers:
	-	`sha256:f6e7df028e10774143b75638cf9a91ae4484ad9be9705a3ab7de160bfbeab308`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307857c2fc1847cc55f2ad19b9b6647658c5135c8b20a447ca114dfaf6cdb9b3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:6f9bbe66f9f9620c0aad2b8b464d5f0912510b5fbbcce31e1458c51d8bdc36a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b357cad96475791645ca664e952dfc2be3a80db4daa6ebc50db2cdb2426d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0919c3817d8379bb41e1be06c4a9ce8b781a7c46fd9a118114bab8de444770a2`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 89.1 KB (89138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e0d0ce3aa2cc891355694b9f4548ada6aa0f587ac1f8f95ff08b62f092ca3`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6048abcd79b046de58bebf91b3eb0b6d1d3cdef973e93188a86da2ad1ffe65`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3f840c3a9d83f847e5bb8879ed8d0fae64e2ab7849ae389421052f6925264c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a31c54f0008afb75dde7c016b9771c6f37268270d33d98c57f6d4c46be550c`

```dockerfile
```

-	Layers:
	-	`sha256:e415d942102ceb25c19c03d57e7aad5f3e309c6a8aebe7422ef678a4f6a8c3c4`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:12817cd6117bed3cdf9e7e4b52de247dd1a87d2876d8dc7434e5115f0fc9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cba0ff108ef4a8e8108d49bf7ccd596afac4a82110a7c14e80a001be5fa5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51637362b800c4f96d7abb05ca7529a770947ee4b1e9623b35af4b936195f4a9`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 81.6 KB (81648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15074482593cb5d5f416eda5eadebe75a10ba5005975523c4c34e81f46e618`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71199d0efb2f82ed5530667b5595dd7a34230b43f8dd94dbe9c99654b1b9ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5a94554ddb9da6514578c1b09075a2b4ab9c4410f3e3e231bae96919d45f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f515b3bed3192db05a2ad5b870421a369f4a33d6b7164dac00142ecf5bc150`

```dockerfile
```

-	Layers:
	-	`sha256:49f4a9e142d4f0bbdb2b6f12f002efa4735f8926b13589ba3a9a5a9ce1a027ef`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c72de5bccb3b20f12aaba84aa22f33c24e0ef214459867af7cbe28470672cb2`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:7bd7eff848bd7ecb4ebeafabcab07a01e40580fc27ad865b3b7dc5c3e8307bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46380b40fc8cf495b0e4fe6bb439caf833e2bbaf42e79ccbccacbd21456f38f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966823473fa57bd0c6c045474918109f56a52c519aa3ff2bbeb53a9bd43f890`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 100.6 KB (100555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487e20745df540295ba2a7d5c3230edfbc1657b671f349f920b261416279acc`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477716625dcd64617f5279d092cb746cef8275524ced557b548fac120fd1e9d`  
		Last Modified: Tue, 28 Jan 2025 01:41:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bf674933baf7156a187fcab52df270880af433ca3e590a2d21c400137e505bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e08d169c62b2f76c8f3d4eae8033be48d397c61a9f6edf7ecbdff2e94987c6`

```dockerfile
```

-	Layers:
	-	`sha256:c463f59b08554468e33ec7d67e5bf358a4422df9ba9c9e8a5c85545acbf01205`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55be9c8a835f959acbc00acf5a1a31119a99c2d3a92aba2088b8f3f0b9b7f56c`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:b310c392ab6f14391fb45b5af6ea15dbcbd23076e497d3d94c110d7b2087f4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbcf6cf269492e27066e7c7bbcb967e81247f0f3f3d09284672b28db7077ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551001421d38a34944d1a96a5df258e75c389ab10abd35456cbb26915537f7fd`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72f77ecf249ccd9496811e0eb3c0cf489c7b7fdbfa9b09a800fc23ce9a5b86`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78fa624f51e7a9f83ca9c71b40f866f13ab95ae1d6fb7f7fb39888ee08b23f5`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 120.1 KB (120111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b172e6f71ba4a3cd0b9d569cc026414ab5ff72c2c999047269348e63b5abaf`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f42fb7496f67e41461243ea1a96721d75c60e36c3fc0bc0cc31f4a05a0a3f`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9927a6df5d8b7dbdb338658808aeddad5564ef5897b94b692df5dfa29b9abdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d905998f2bfd41e52ca5677826d1ba128880dee6ab953a307411406c31b587`

```dockerfile
```

-	Layers:
	-	`sha256:aef24c41d2f2fe02d3f60245a4d8614488af106b27f1694638bb0aa63affdeec`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e634c06318ef153f0dea3d1996b85ebfa8b5d1ae392ac0ae4aba4ce249a2d7ee`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:884a0eb6ba4f64c3edda016b28d4bd99dba5200f5af5ac9cb6b72f18cb3a3a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a09f14f9a1c5c8a4bc39f97cc1d4dfc2da04ebc3eb0e1c14ee25ecf135a583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2bb56ba626edfb899d02de6e190e018998d7573a673f6db87d5ef30de0a050`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 112.6 KB (112648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e93d7242196ad9ca14b560ce78c345dfa536c1a35de8044919beffdf4eb97a`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e06feef4b6941cffa38f96ec7bf4e23040ea0baf7cf6f0a7345c46675eff3`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:02029f95376d43c51ccddf3f8c8bbebb0671c8774aacfa19d44aee40f4773161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4efe04e204e62e8c95b99341d61fcd033d068bcbce5868ae0ec1685e9f9da3e`

```dockerfile
```

-	Layers:
	-	`sha256:f198a76291582efc4f722539762e32a43b96a2acfb2de57f18adfa903c9b3c57`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32d956ebf079b702220519e8a308783736857197d7766e995bfbcd8c71dbf2c`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:756e00d72198e903bfd6356e80496c2936c64fa26149b3662c09c044393ac715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b076b4ea8c2964765a22bf8c5d8b2fb8141f171e1f335b628572524c3ab7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d4da436692d4ab0fd5035ee54eac03b05bf24df9aa3304a4cbb3e6bb7fb7de`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 98.8 KB (98808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f3813ff058c0963785dcdc5c5f860f00840874673c02d724b273f844d53c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d897b6a73cbb856ebfd058f311b8f0e39512fdede0d33460f38db93bb89b6c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:877a9cd3fe26f402674032844c26b7149200267a47a431963b72e3b4563d519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b37c1a9028694f866e7acc219fbf431ce5b97965a6f5489a14f064c84a12b1`

```dockerfile
```

-	Layers:
	-	`sha256:40546cca6e89cde845ebe9184ed940f3b4f38ba1e18049e3b36b047821e42722`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:496d1116424a4c78bad3fdd46c2db89305089a904ff0d42fcd07ffca4576a0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32ae085c92ecf8421e7f161ab96951c317b5e771993504a3e09c8db10414930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398f6409117bd2a57c6b304f740badcea613c5def606a7c072bcd0c73b061e0`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 96.9 KB (96911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ed7682792c020e13d8b547fdbb8c43a4956cb69969b8f5a2724202bbcb39d`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff53239a6486b270ef8a57e32718cefe901786526573b780eb054d1ac053dc6e`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d66b26cdcd77f8b4437bcb47a340f63d583e754a794e2a822931eafa72152360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cdd7bbb43e56276987d1ae0048a6f92a4bca0ccdee9e8e670ddb9ea5e16cb9`

```dockerfile
```

-	Layers:
	-	`sha256:6fe581f275230ca3b53c4a9c2f8f4690c4edf45359ead5089d277953f8872d2a`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0280df9fd96cadb1c6e05a657e4d4caa094e820e2a85ddd2df85b36c0363d18`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.3`

```console
$ docker pull spiped@sha256:f504c30db9ca75bf547f89bef1cdf557c6d2a3dce57fcf74d43de04f8de593ff
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.3` - linux; amd64

```console
$ docker pull spiped@sha256:4d6064fa1b632e22bdce3cffebf989475f6e2be0eaf6a36498a2e4e28b228d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37097677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54460248729376bb05e1602bb12f5b0a9aa0e710990826e3a73faacdd062b547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7196154f35d46a29a47883173fde58814cfb6bb853a3c4a61cca9430cf1f8159`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd3a971ecf92f9d804a86b505518d4c7b4542035f10e32e0b0c1482acdb10b`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 2.4 MB (2401342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf2c3578328d143a0c13eac4322d3a7ba1c09d0bb431e3fb8bccb93fac7409`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 6.5 MB (6482493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c051f65857ae1a80b319d09976092265d695e37fb3b0c69fcf014ec2643d7`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7250acc401675038e92dc4a884eee09833a19e8adba51f183326d29fcc2ca6`  
		Last Modified: Tue, 04 Feb 2025 04:23:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:697c33cad9224e7f7763c4dbd3db4457416e6f1d07de6625f41e20e5c83072e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbac9dbdf7a50bc8d58d8959455a7fb5e0547b6627570b17db660d45b6effacd`

```dockerfile
```

-	Layers:
	-	`sha256:b4b40f46007e4399d9b995de98a93ac8be64ebfc2a39c66d9abbfa5512688d01`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3522078defe9a24dc1fa0dc53832d9fb3206f653efe38d4cd9d5839c6fc70e`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; arm variant v5

```console
$ docker pull spiped@sha256:6e9ed3ec5459996a7edc1a2f5fa9f91294a34d39e7467e39ffafb3035ccb5c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32882064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1371b30fecc7c3db6ab766bbc4750a8751c93cabe9d75fae796aec4066ec76b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e614f72336dfb4738cbfa9d91d99d2d7008ce16b7acf879b6d9d166dd1c882`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef4a7d930f64716939f723e7ce3c4551621bfb867ac4f4e61e5b05dddfb29dc`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 2.0 MB (1997174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91afdbb82f94d4dd13401231991619b93c99ec48cdcaf0cb0ba8dce74b87642`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 5.1 MB (5146798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4af1d5f9bc51aca0b2d09e04074a8f703930c4176b241a50d5ff3492ed47ce`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddabd99982fc01efcad0872592b12613c3b224baeb5ee91a78f4dbf692df1843`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:7ef4a0bc6c9834e261cda43f045e8d5b1794274f1138907d70934884d34d5f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce6a167142fb12a6a18d59f0d97dfaa6e26415501333d6375aa3a1471ce3d0b`

```dockerfile
```

-	Layers:
	-	`sha256:c6e65141c199dc160de554a46ba815b77e0022fec048fdcf1b0fe1c6b13530b5`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fac543ba7e329c9a615af9d72772e6955538ba4abc8298e3e684fec72c495e2`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 15.1 KB (15140 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; arm variant v7

```console
$ docker pull spiped@sha256:a18f5778ca2f08846bf27be992878deb0a4c267c165517af290b69d341577d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30659675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc7bc7a0d0e4a2dcd29786ded7a4582d24affb641bf0b53d84450510c97ef44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d40b8c33eed4efe5d43b21f211ccc96a002e6246f8b80e0e6f53f45a5c1334`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f95294c83140a5f312fe0e0f3673b125c4718f4c4f531b3d58735aec00054b`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.9 MB (1855579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36310be6ec666453ebf3cbf37d05cda567f1a1a76d531826880d258eba1676e4`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 4.9 MB (4888021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ca7552106b4e46e361314d1d889c4683713c3e9d455c68cdefca8c8f6398d5`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8587687f43a65aec0c478bff612f8274ace1a6e6f519d21be92752ef5e310b`  
		Last Modified: Tue, 04 Feb 2025 10:26:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:48f395833d05679dc7e6fe62d5fbd26b2f600568d0e161f4bec8add466c41174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9242c434cb9698da41a72676a955396192dab94c1f14c49069a83938788cbf9`

```dockerfile
```

-	Layers:
	-	`sha256:88adb85aaabae3f90b457b693796e9e7deae4ca3b7d86c8280553b3f6834f170`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc48124ea568f4a829f5a6697ba88d5decfc16547dba969d09e0fc431dedef7d`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:512de4a1d89736d75c4681f2be68b9e1bab029e3c613da922eaa8b4960135a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35780546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c8f81d42835a979ac6346e5f039e31c1430d6d29427695126d2fa2751dc9f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445785d885b1d4f4c62b22f763a4c23c5ef61dbcf8561b1f373f1122a157a32`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e83c554a066c3f065b78b3307f98c54d4a3753271ce9398dcfb644a034658f`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 2.2 MB (2247024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb79cb22695e7006611aaa6075a06126c1e46b6ec26a36bc59b2024e0692bb0`  
		Last Modified: Tue, 04 Feb 2025 08:36:36 GMT  
		Size: 5.5 MB (5491103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5f8d83d3803bc3372d3b2f901b9a579d0fe0892f5c55c7ffbcb4841f2509f`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786f9a23b172afb3253a266af44a47a83cf5676a8b5fca783047e454090874f`  
		Last Modified: Tue, 04 Feb 2025 08:36:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:1f2b3b9c6d8d47ed3b1ae99990fab63995a73e145a7a7112393c86bdd9442fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f7026f2371bb9fdfe80e13f7478f933109e240f67a727773f50e39d31fc713`

```dockerfile
```

-	Layers:
	-	`sha256:6204b89f04e97cef39e578e6ed3eafaf5f4a5ad99e91966a0a795d19b52a65f6`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3efb69cc87f6603eb18e553aad09ba800952702851ad7d7d050b1d4fd1122d73`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; 386

```console
$ docker pull spiped@sha256:4396202c141ba5d4ea455a322aab810e9553b5e6a20aa108c9fc5ae7db1af7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37544085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2677d43d830f991ba448c851b51731990b47564a89016bcf439071214ccff3c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a084f64ea6359821d9e6154f483978b063d4a671e0f59b1c9ed8b46ddb71f34`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b626f23d4ddc2323109743108c51c43a1fe05d501d0e7ded9368531db9ab7`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 2.4 MB (2398651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d27cbe14fcb4784bdf925fe2c6365bc3781a5667e0f64765c11702c029adab`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 6.0 MB (5956440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f9893150c1f1ac3dbda70997a910e68f713cbbbf84707c63383aa657bef3a2`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1739d36dcea86126749ade8e41d5e26216a42e18cce7c574440f9a6dc9541`  
		Last Modified: Tue, 04 Feb 2025 04:23:43 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:190b7c5c5be2c9c5120bf3ec3d4b10e82e95f81333b011d1e2ac392b1ebc8418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d950ae27b1b619fc42683fcc84894d47c3d2f6cab9d9365e5a9081e20a870b66`

```dockerfile
```

-	Layers:
	-	`sha256:71740a47ab23a838f20e0cb6d24717d773397bf1b2a403152ef6eb81f2bdbe3d`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c92219d16dbfc537787922ce2f4fe8a90c45a3e868fd697b90b6a525b1d035e`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 15.0 KB (15003 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; mips64le

```console
$ docker pull spiped@sha256:228e0bf1261e83b036e9df0c5b3ca867223a333421a2890b3c3720ea81c5a1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36142318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891b41e80be95bdb58c5d4b79cb3ec32056f765cb389c9eac81badc4bd9c27b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e2b18cfa28e78209d84a30bbacfa4539a85ee636689c58538621e572a4133b`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d49f8446481472986048351b40e96fcad9c44128630158e4319ae5b69b2feca`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 1.8 MB (1841114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0200fc9cacb2091aa304f8f172882d407f93a42a059f02ffc2ae0acaf682671`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 5.8 MB (5813078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2152b44d1116d5c1168680113e8fdd466ebcc7ee99c07fdfe1b3fbf39ba7e`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dac11d6a32393a766da366844f6656c0ef0a5443e7206d484655d856a5fb49`  
		Last Modified: Tue, 04 Feb 2025 19:23:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:fcac27653c73b5b7610b7b2e0c943a12ae91de1da06633457d0c9cd6b627629e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855a8edc4f8b24033f2315611577aa502a4cbe311c66c2391b1919db8af2f36c`

```dockerfile
```

-	Layers:
	-	`sha256:a6003ae2d7ac2094ff93c250171d0ca098c7a1e6a808c1c7bd1d6deff6bdadd8`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; ppc64le

```console
$ docker pull spiped@sha256:978bfe51b8d6c8f3381934ea41c373766dfb48b535bba6ee5f243a193006a387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0540b6aada3775e3adfd4af21f094aa6460b9f09c3d305374563039cddb310e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaa4db2f41f33b473ee9e3d23526c2a5c3d06e4c63d975f8c329650781bfc50`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9aa243ee14d1187269f15a51bdd0121c76f084de8c950caf576d98b70e463`  
		Last Modified: Tue, 04 Feb 2025 07:09:55 GMT  
		Size: 2.6 MB (2582094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb78a29a1de352d83b7220b0199eb455f02534bd728d801150686e7e720a273`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 6.4 MB (6440730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca2cb4355672884568c1eff10a52aae16dac2db14e387628247926c8e48cdc`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4693e453a57e0f33af4fc1efea3a42a24e6381418d131d5aae599efae23f4eb8`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:c3db218145823880cb4767205ac0d1924a1ea93de5ec49956ff101d21069b0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d9f6f6871ede0f731ed47717e49df6baa968b54038d23c64b6a155a3d51f3f`

```dockerfile
```

-	Layers:
	-	`sha256:69b861da7d96b4f3975dc9cd80514ce15bc9a8d5bf9ab3fa2d4fe527e805d2cf`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d5bc74f88a190910aebb2f129af625cf7b0d44d488bf251a42bd4bda622586`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; s390x

```console
$ docker pull spiped@sha256:d602741ec001ec0bd0250c732c173274ba73887a8329ae21abc99750c26dcf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa781d6e5a453fc558205ea8ece3ac80a2ebe01b811e5ee602ec0053c7672138`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a6e7d0775375fc3d1e148728013c288c159edf09d7f89268dbd2b94adb02e`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3dd0162c40e5529113c4043b6a295aaba4477a5614ea6b37101eae051fae91`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 2.1 MB (2068737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89371216de8a5f913d8b5e84022a8820b75c22312a485ed5d4532ec0cc3ad89f`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 5.4 MB (5391937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c639f4e3d3bb15db262a0e635d9bfa87307da8ab93f4de0186dd76242d0bbf92`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d7fb587195e97fb81398a0cda1fed9beabbc7bebb633a6b41d52053b99a1a3`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:c571df89a1b0e77226d84a4ac833f4dda8adf0e04737412c9fdd4785a2c870aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991662535cd5d6a339176b8c9b909132cb73a6c2bebc27790b05b5987af78f30`

```dockerfile
```

-	Layers:
	-	`sha256:69a67dda4c3fd05bb160600c2ea45317f2ff7d014280d03aabc69b0795186b0b`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe307bfbbadd67d2deae85a17c6a372d6f7cce95ba0fedfa0d63d0b641fdde55`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.3-alpine`

```console
$ docker pull spiped@sha256:cff1ff69fc6f8904043ef5d9bb654e468a38fc671dedcecd1f568a1d61f1d634
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

### `spiped:1.6.3-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:2715ebbc20690dda6d438989f61f4eb4fb11162e932ba70cedc0c7f12b3c26f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ec86461245d72383c5662f686c25016cc299d589def9478af4205b484492be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b181c716ebe4d13478b33f2488cb40b954ba24081d61c5bc9d7f0605ba9d113`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ded10ce7d7c8e5d5eb05c5a7d5246a6a045996ee4f18dcc322d6600e68cd81`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d46a15f052086577ecb502311cd9f4d176cd407ad00862e11dd7d6f8c2a868`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 107.6 KB (107614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b34221300809a19087f5d67a70e8167a72247feb52faa8c58a878f5af671d3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89b10c18fcccf667446750b679723f2821a55bf5612caacbb8c510578e77e1`  
		Last Modified: Tue, 28 Jan 2025 01:28:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6a640be7b02114db4704050ac59d1be28b1b8f1a10f0ce877865a41933bc6d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24283cd9a878c00f69d37c768fc27af4fe97d6fa56a0174f6b441c10746770b0`

```dockerfile
```

-	Layers:
	-	`sha256:f6e7df028e10774143b75638cf9a91ae4484ad9be9705a3ab7de160bfbeab308`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307857c2fc1847cc55f2ad19b9b6647658c5135c8b20a447ca114dfaf6cdb9b3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:6f9bbe66f9f9620c0aad2b8b464d5f0912510b5fbbcce31e1458c51d8bdc36a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b357cad96475791645ca664e952dfc2be3a80db4daa6ebc50db2cdb2426d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0919c3817d8379bb41e1be06c4a9ce8b781a7c46fd9a118114bab8de444770a2`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 89.1 KB (89138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e0d0ce3aa2cc891355694b9f4548ada6aa0f587ac1f8f95ff08b62f092ca3`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6048abcd79b046de58bebf91b3eb0b6d1d3cdef973e93188a86da2ad1ffe65`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3f840c3a9d83f847e5bb8879ed8d0fae64e2ab7849ae389421052f6925264c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a31c54f0008afb75dde7c016b9771c6f37268270d33d98c57f6d4c46be550c`

```dockerfile
```

-	Layers:
	-	`sha256:e415d942102ceb25c19c03d57e7aad5f3e309c6a8aebe7422ef678a4f6a8c3c4`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:12817cd6117bed3cdf9e7e4b52de247dd1a87d2876d8dc7434e5115f0fc9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cba0ff108ef4a8e8108d49bf7ccd596afac4a82110a7c14e80a001be5fa5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51637362b800c4f96d7abb05ca7529a770947ee4b1e9623b35af4b936195f4a9`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 81.6 KB (81648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15074482593cb5d5f416eda5eadebe75a10ba5005975523c4c34e81f46e618`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71199d0efb2f82ed5530667b5595dd7a34230b43f8dd94dbe9c99654b1b9ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5a94554ddb9da6514578c1b09075a2b4ab9c4410f3e3e231bae96919d45f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f515b3bed3192db05a2ad5b870421a369f4a33d6b7164dac00142ecf5bc150`

```dockerfile
```

-	Layers:
	-	`sha256:49f4a9e142d4f0bbdb2b6f12f002efa4735f8926b13589ba3a9a5a9ce1a027ef`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c72de5bccb3b20f12aaba84aa22f33c24e0ef214459867af7cbe28470672cb2`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:7bd7eff848bd7ecb4ebeafabcab07a01e40580fc27ad865b3b7dc5c3e8307bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46380b40fc8cf495b0e4fe6bb439caf833e2bbaf42e79ccbccacbd21456f38f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966823473fa57bd0c6c045474918109f56a52c519aa3ff2bbeb53a9bd43f890`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 100.6 KB (100555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487e20745df540295ba2a7d5c3230edfbc1657b671f349f920b261416279acc`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477716625dcd64617f5279d092cb746cef8275524ced557b548fac120fd1e9d`  
		Last Modified: Tue, 28 Jan 2025 01:41:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bf674933baf7156a187fcab52df270880af433ca3e590a2d21c400137e505bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e08d169c62b2f76c8f3d4eae8033be48d397c61a9f6edf7ecbdff2e94987c6`

```dockerfile
```

-	Layers:
	-	`sha256:c463f59b08554468e33ec7d67e5bf358a4422df9ba9c9e8a5c85545acbf01205`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55be9c8a835f959acbc00acf5a1a31119a99c2d3a92aba2088b8f3f0b9b7f56c`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; 386

```console
$ docker pull spiped@sha256:b310c392ab6f14391fb45b5af6ea15dbcbd23076e497d3d94c110d7b2087f4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbcf6cf269492e27066e7c7bbcb967e81247f0f3f3d09284672b28db7077ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551001421d38a34944d1a96a5df258e75c389ab10abd35456cbb26915537f7fd`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72f77ecf249ccd9496811e0eb3c0cf489c7b7fdbfa9b09a800fc23ce9a5b86`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78fa624f51e7a9f83ca9c71b40f866f13ab95ae1d6fb7f7fb39888ee08b23f5`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 120.1 KB (120111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b172e6f71ba4a3cd0b9d569cc026414ab5ff72c2c999047269348e63b5abaf`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f42fb7496f67e41461243ea1a96721d75c60e36c3fc0bc0cc31f4a05a0a3f`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9927a6df5d8b7dbdb338658808aeddad5564ef5897b94b692df5dfa29b9abdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d905998f2bfd41e52ca5677826d1ba128880dee6ab953a307411406c31b587`

```dockerfile
```

-	Layers:
	-	`sha256:aef24c41d2f2fe02d3f60245a4d8614488af106b27f1694638bb0aa63affdeec`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e634c06318ef153f0dea3d1996b85ebfa8b5d1ae392ac0ae4aba4ce249a2d7ee`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:884a0eb6ba4f64c3edda016b28d4bd99dba5200f5af5ac9cb6b72f18cb3a3a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a09f14f9a1c5c8a4bc39f97cc1d4dfc2da04ebc3eb0e1c14ee25ecf135a583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2bb56ba626edfb899d02de6e190e018998d7573a673f6db87d5ef30de0a050`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 112.6 KB (112648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e93d7242196ad9ca14b560ce78c345dfa536c1a35de8044919beffdf4eb97a`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e06feef4b6941cffa38f96ec7bf4e23040ea0baf7cf6f0a7345c46675eff3`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:02029f95376d43c51ccddf3f8c8bbebb0671c8774aacfa19d44aee40f4773161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4efe04e204e62e8c95b99341d61fcd033d068bcbce5868ae0ec1685e9f9da3e`

```dockerfile
```

-	Layers:
	-	`sha256:f198a76291582efc4f722539762e32a43b96a2acfb2de57f18adfa903c9b3c57`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32d956ebf079b702220519e8a308783736857197d7766e995bfbcd8c71dbf2c`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:756e00d72198e903bfd6356e80496c2936c64fa26149b3662c09c044393ac715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b076b4ea8c2964765a22bf8c5d8b2fb8141f171e1f335b628572524c3ab7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d4da436692d4ab0fd5035ee54eac03b05bf24df9aa3304a4cbb3e6bb7fb7de`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 98.8 KB (98808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f3813ff058c0963785dcdc5c5f860f00840874673c02d724b273f844d53c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d897b6a73cbb856ebfd058f311b8f0e39512fdede0d33460f38db93bb89b6c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:877a9cd3fe26f402674032844c26b7149200267a47a431963b72e3b4563d519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b37c1a9028694f866e7acc219fbf431ce5b97965a6f5489a14f064c84a12b1`

```dockerfile
```

-	Layers:
	-	`sha256:40546cca6e89cde845ebe9184ed940f3b4f38ba1e18049e3b36b047821e42722`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:496d1116424a4c78bad3fdd46c2db89305089a904ff0d42fcd07ffca4576a0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32ae085c92ecf8421e7f161ab96951c317b5e771993504a3e09c8db10414930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398f6409117bd2a57c6b304f740badcea613c5def606a7c072bcd0c73b061e0`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 96.9 KB (96911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ed7682792c020e13d8b547fdbb8c43a4956cb69969b8f5a2724202bbcb39d`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff53239a6486b270ef8a57e32718cefe901786526573b780eb054d1ac053dc6e`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d66b26cdcd77f8b4437bcb47a340f63d583e754a794e2a822931eafa72152360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cdd7bbb43e56276987d1ae0048a6f92a4bca0ccdee9e8e670ddb9ea5e16cb9`

```dockerfile
```

-	Layers:
	-	`sha256:6fe581f275230ca3b53c4a9c2f8f4690c4edf45359ead5089d277953f8872d2a`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0280df9fd96cadb1c6e05a657e4d4caa094e820e2a85ddd2df85b36c0363d18`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:cff1ff69fc6f8904043ef5d9bb654e468a38fc671dedcecd1f568a1d61f1d634
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
$ docker pull spiped@sha256:2715ebbc20690dda6d438989f61f4eb4fb11162e932ba70cedc0c7f12b3c26f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ec86461245d72383c5662f686c25016cc299d589def9478af4205b484492be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b181c716ebe4d13478b33f2488cb40b954ba24081d61c5bc9d7f0605ba9d113`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ded10ce7d7c8e5d5eb05c5a7d5246a6a045996ee4f18dcc322d6600e68cd81`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d46a15f052086577ecb502311cd9f4d176cd407ad00862e11dd7d6f8c2a868`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 107.6 KB (107614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b34221300809a19087f5d67a70e8167a72247feb52faa8c58a878f5af671d3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89b10c18fcccf667446750b679723f2821a55bf5612caacbb8c510578e77e1`  
		Last Modified: Tue, 28 Jan 2025 01:28:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6a640be7b02114db4704050ac59d1be28b1b8f1a10f0ce877865a41933bc6d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24283cd9a878c00f69d37c768fc27af4fe97d6fa56a0174f6b441c10746770b0`

```dockerfile
```

-	Layers:
	-	`sha256:f6e7df028e10774143b75638cf9a91ae4484ad9be9705a3ab7de160bfbeab308`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307857c2fc1847cc55f2ad19b9b6647658c5135c8b20a447ca114dfaf6cdb9b3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:6f9bbe66f9f9620c0aad2b8b464d5f0912510b5fbbcce31e1458c51d8bdc36a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b357cad96475791645ca664e952dfc2be3a80db4daa6ebc50db2cdb2426d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0919c3817d8379bb41e1be06c4a9ce8b781a7c46fd9a118114bab8de444770a2`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 89.1 KB (89138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e0d0ce3aa2cc891355694b9f4548ada6aa0f587ac1f8f95ff08b62f092ca3`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6048abcd79b046de58bebf91b3eb0b6d1d3cdef973e93188a86da2ad1ffe65`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3f840c3a9d83f847e5bb8879ed8d0fae64e2ab7849ae389421052f6925264c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a31c54f0008afb75dde7c016b9771c6f37268270d33d98c57f6d4c46be550c`

```dockerfile
```

-	Layers:
	-	`sha256:e415d942102ceb25c19c03d57e7aad5f3e309c6a8aebe7422ef678a4f6a8c3c4`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:12817cd6117bed3cdf9e7e4b52de247dd1a87d2876d8dc7434e5115f0fc9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cba0ff108ef4a8e8108d49bf7ccd596afac4a82110a7c14e80a001be5fa5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51637362b800c4f96d7abb05ca7529a770947ee4b1e9623b35af4b936195f4a9`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 81.6 KB (81648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15074482593cb5d5f416eda5eadebe75a10ba5005975523c4c34e81f46e618`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71199d0efb2f82ed5530667b5595dd7a34230b43f8dd94dbe9c99654b1b9ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5a94554ddb9da6514578c1b09075a2b4ab9c4410f3e3e231bae96919d45f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f515b3bed3192db05a2ad5b870421a369f4a33d6b7164dac00142ecf5bc150`

```dockerfile
```

-	Layers:
	-	`sha256:49f4a9e142d4f0bbdb2b6f12f002efa4735f8926b13589ba3a9a5a9ce1a027ef`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c72de5bccb3b20f12aaba84aa22f33c24e0ef214459867af7cbe28470672cb2`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:7bd7eff848bd7ecb4ebeafabcab07a01e40580fc27ad865b3b7dc5c3e8307bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46380b40fc8cf495b0e4fe6bb439caf833e2bbaf42e79ccbccacbd21456f38f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966823473fa57bd0c6c045474918109f56a52c519aa3ff2bbeb53a9bd43f890`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 100.6 KB (100555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487e20745df540295ba2a7d5c3230edfbc1657b671f349f920b261416279acc`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477716625dcd64617f5279d092cb746cef8275524ced557b548fac120fd1e9d`  
		Last Modified: Tue, 28 Jan 2025 01:41:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bf674933baf7156a187fcab52df270880af433ca3e590a2d21c400137e505bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e08d169c62b2f76c8f3d4eae8033be48d397c61a9f6edf7ecbdff2e94987c6`

```dockerfile
```

-	Layers:
	-	`sha256:c463f59b08554468e33ec7d67e5bf358a4422df9ba9c9e8a5c85545acbf01205`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55be9c8a835f959acbc00acf5a1a31119a99c2d3a92aba2088b8f3f0b9b7f56c`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:b310c392ab6f14391fb45b5af6ea15dbcbd23076e497d3d94c110d7b2087f4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbcf6cf269492e27066e7c7bbcb967e81247f0f3f3d09284672b28db7077ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551001421d38a34944d1a96a5df258e75c389ab10abd35456cbb26915537f7fd`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72f77ecf249ccd9496811e0eb3c0cf489c7b7fdbfa9b09a800fc23ce9a5b86`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78fa624f51e7a9f83ca9c71b40f866f13ab95ae1d6fb7f7fb39888ee08b23f5`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 120.1 KB (120111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b172e6f71ba4a3cd0b9d569cc026414ab5ff72c2c999047269348e63b5abaf`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f42fb7496f67e41461243ea1a96721d75c60e36c3fc0bc0cc31f4a05a0a3f`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9927a6df5d8b7dbdb338658808aeddad5564ef5897b94b692df5dfa29b9abdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d905998f2bfd41e52ca5677826d1ba128880dee6ab953a307411406c31b587`

```dockerfile
```

-	Layers:
	-	`sha256:aef24c41d2f2fe02d3f60245a4d8614488af106b27f1694638bb0aa63affdeec`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e634c06318ef153f0dea3d1996b85ebfa8b5d1ae392ac0ae4aba4ce249a2d7ee`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:884a0eb6ba4f64c3edda016b28d4bd99dba5200f5af5ac9cb6b72f18cb3a3a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a09f14f9a1c5c8a4bc39f97cc1d4dfc2da04ebc3eb0e1c14ee25ecf135a583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2bb56ba626edfb899d02de6e190e018998d7573a673f6db87d5ef30de0a050`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 112.6 KB (112648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e93d7242196ad9ca14b560ce78c345dfa536c1a35de8044919beffdf4eb97a`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e06feef4b6941cffa38f96ec7bf4e23040ea0baf7cf6f0a7345c46675eff3`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:02029f95376d43c51ccddf3f8c8bbebb0671c8774aacfa19d44aee40f4773161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4efe04e204e62e8c95b99341d61fcd033d068bcbce5868ae0ec1685e9f9da3e`

```dockerfile
```

-	Layers:
	-	`sha256:f198a76291582efc4f722539762e32a43b96a2acfb2de57f18adfa903c9b3c57`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32d956ebf079b702220519e8a308783736857197d7766e995bfbcd8c71dbf2c`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:756e00d72198e903bfd6356e80496c2936c64fa26149b3662c09c044393ac715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b076b4ea8c2964765a22bf8c5d8b2fb8141f171e1f335b628572524c3ab7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d4da436692d4ab0fd5035ee54eac03b05bf24df9aa3304a4cbb3e6bb7fb7de`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 98.8 KB (98808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f3813ff058c0963785dcdc5c5f860f00840874673c02d724b273f844d53c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d897b6a73cbb856ebfd058f311b8f0e39512fdede0d33460f38db93bb89b6c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:877a9cd3fe26f402674032844c26b7149200267a47a431963b72e3b4563d519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b37c1a9028694f866e7acc219fbf431ce5b97965a6f5489a14f064c84a12b1`

```dockerfile
```

-	Layers:
	-	`sha256:40546cca6e89cde845ebe9184ed940f3b4f38ba1e18049e3b36b047821e42722`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:496d1116424a4c78bad3fdd46c2db89305089a904ff0d42fcd07ffca4576a0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32ae085c92ecf8421e7f161ab96951c317b5e771993504a3e09c8db10414930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398f6409117bd2a57c6b304f740badcea613c5def606a7c072bcd0c73b061e0`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 96.9 KB (96911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ed7682792c020e13d8b547fdbb8c43a4956cb69969b8f5a2724202bbcb39d`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff53239a6486b270ef8a57e32718cefe901786526573b780eb054d1ac053dc6e`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d66b26cdcd77f8b4437bcb47a340f63d583e754a794e2a822931eafa72152360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cdd7bbb43e56276987d1ae0048a6f92a4bca0ccdee9e8e670ddb9ea5e16cb9`

```dockerfile
```

-	Layers:
	-	`sha256:6fe581f275230ca3b53c4a9c2f8f4690c4edf45359ead5089d277953f8872d2a`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0280df9fd96cadb1c6e05a657e4d4caa094e820e2a85ddd2df85b36c0363d18`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:f504c30db9ca75bf547f89bef1cdf557c6d2a3dce57fcf74d43de04f8de593ff
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:4d6064fa1b632e22bdce3cffebf989475f6e2be0eaf6a36498a2e4e28b228d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37097677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54460248729376bb05e1602bb12f5b0a9aa0e710990826e3a73faacdd062b547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7196154f35d46a29a47883173fde58814cfb6bb853a3c4a61cca9430cf1f8159`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd3a971ecf92f9d804a86b505518d4c7b4542035f10e32e0b0c1482acdb10b`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 2.4 MB (2401342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf2c3578328d143a0c13eac4322d3a7ba1c09d0bb431e3fb8bccb93fac7409`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 6.5 MB (6482493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c051f65857ae1a80b319d09976092265d695e37fb3b0c69fcf014ec2643d7`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7250acc401675038e92dc4a884eee09833a19e8adba51f183326d29fcc2ca6`  
		Last Modified: Tue, 04 Feb 2025 04:23:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:697c33cad9224e7f7763c4dbd3db4457416e6f1d07de6625f41e20e5c83072e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbac9dbdf7a50bc8d58d8959455a7fb5e0547b6627570b17db660d45b6effacd`

```dockerfile
```

-	Layers:
	-	`sha256:b4b40f46007e4399d9b995de98a93ac8be64ebfc2a39c66d9abbfa5512688d01`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3522078defe9a24dc1fa0dc53832d9fb3206f653efe38d4cd9d5839c6fc70e`  
		Last Modified: Tue, 04 Feb 2025 04:23:58 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:6e9ed3ec5459996a7edc1a2f5fa9f91294a34d39e7467e39ffafb3035ccb5c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32882064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1371b30fecc7c3db6ab766bbc4750a8751c93cabe9d75fae796aec4066ec76b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e614f72336dfb4738cbfa9d91d99d2d7008ce16b7acf879b6d9d166dd1c882`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef4a7d930f64716939f723e7ce3c4551621bfb867ac4f4e61e5b05dddfb29dc`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 2.0 MB (1997174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91afdbb82f94d4dd13401231991619b93c99ec48cdcaf0cb0ba8dce74b87642`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 5.1 MB (5146798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4af1d5f9bc51aca0b2d09e04074a8f703930c4176b241a50d5ff3492ed47ce`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddabd99982fc01efcad0872592b12613c3b224baeb5ee91a78f4dbf692df1843`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:7ef4a0bc6c9834e261cda43f045e8d5b1794274f1138907d70934884d34d5f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce6a167142fb12a6a18d59f0d97dfaa6e26415501333d6375aa3a1471ce3d0b`

```dockerfile
```

-	Layers:
	-	`sha256:c6e65141c199dc160de554a46ba815b77e0022fec048fdcf1b0fe1c6b13530b5`  
		Last Modified: Tue, 04 Feb 2025 08:02:27 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fac543ba7e329c9a615af9d72772e6955538ba4abc8298e3e684fec72c495e2`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 15.1 KB (15140 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:a18f5778ca2f08846bf27be992878deb0a4c267c165517af290b69d341577d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30659675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc7bc7a0d0e4a2dcd29786ded7a4582d24affb641bf0b53d84450510c97ef44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d40b8c33eed4efe5d43b21f211ccc96a002e6246f8b80e0e6f53f45a5c1334`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f95294c83140a5f312fe0e0f3673b125c4718f4c4f531b3d58735aec00054b`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.9 MB (1855579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36310be6ec666453ebf3cbf37d05cda567f1a1a76d531826880d258eba1676e4`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 4.9 MB (4888021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ca7552106b4e46e361314d1d889c4683713c3e9d455c68cdefca8c8f6398d5`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8587687f43a65aec0c478bff612f8274ace1a6e6f519d21be92752ef5e310b`  
		Last Modified: Tue, 04 Feb 2025 10:26:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:48f395833d05679dc7e6fe62d5fbd26b2f600568d0e161f4bec8add466c41174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9242c434cb9698da41a72676a955396192dab94c1f14c49069a83938788cbf9`

```dockerfile
```

-	Layers:
	-	`sha256:88adb85aaabae3f90b457b693796e9e7deae4ca3b7d86c8280553b3f6834f170`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc48124ea568f4a829f5a6697ba88d5decfc16547dba969d09e0fc431dedef7d`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:512de4a1d89736d75c4681f2be68b9e1bab029e3c613da922eaa8b4960135a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35780546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c8f81d42835a979ac6346e5f039e31c1430d6d29427695126d2fa2751dc9f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445785d885b1d4f4c62b22f763a4c23c5ef61dbcf8561b1f373f1122a157a32`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e83c554a066c3f065b78b3307f98c54d4a3753271ce9398dcfb644a034658f`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 2.2 MB (2247024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb79cb22695e7006611aaa6075a06126c1e46b6ec26a36bc59b2024e0692bb0`  
		Last Modified: Tue, 04 Feb 2025 08:36:36 GMT  
		Size: 5.5 MB (5491103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5f8d83d3803bc3372d3b2f901b9a579d0fe0892f5c55c7ffbcb4841f2509f`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786f9a23b172afb3253a266af44a47a83cf5676a8b5fca783047e454090874f`  
		Last Modified: Tue, 04 Feb 2025 08:36:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:1f2b3b9c6d8d47ed3b1ae99990fab63995a73e145a7a7112393c86bdd9442fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f7026f2371bb9fdfe80e13f7478f933109e240f67a727773f50e39d31fc713`

```dockerfile
```

-	Layers:
	-	`sha256:6204b89f04e97cef39e578e6ed3eafaf5f4a5ad99e91966a0a795d19b52a65f6`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3efb69cc87f6603eb18e553aad09ba800952702851ad7d7d050b1d4fd1122d73`  
		Last Modified: Tue, 04 Feb 2025 08:36:35 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:4396202c141ba5d4ea455a322aab810e9553b5e6a20aa108c9fc5ae7db1af7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37544085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2677d43d830f991ba448c851b51731990b47564a89016bcf439071214ccff3c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a084f64ea6359821d9e6154f483978b063d4a671e0f59b1c9ed8b46ddb71f34`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b626f23d4ddc2323109743108c51c43a1fe05d501d0e7ded9368531db9ab7`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 2.4 MB (2398651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d27cbe14fcb4784bdf925fe2c6365bc3781a5667e0f64765c11702c029adab`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 6.0 MB (5956440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f9893150c1f1ac3dbda70997a910e68f713cbbbf84707c63383aa657bef3a2`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1739d36dcea86126749ade8e41d5e26216a42e18cce7c574440f9a6dc9541`  
		Last Modified: Tue, 04 Feb 2025 04:23:43 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:190b7c5c5be2c9c5120bf3ec3d4b10e82e95f81333b011d1e2ac392b1ebc8418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d950ae27b1b619fc42683fcc84894d47c3d2f6cab9d9365e5a9081e20a870b66`

```dockerfile
```

-	Layers:
	-	`sha256:71740a47ab23a838f20e0cb6d24717d773397bf1b2a403152ef6eb81f2bdbe3d`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c92219d16dbfc537787922ce2f4fe8a90c45a3e868fd697b90b6a525b1d035e`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 15.0 KB (15003 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:228e0bf1261e83b036e9df0c5b3ca867223a333421a2890b3c3720ea81c5a1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36142318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891b41e80be95bdb58c5d4b79cb3ec32056f765cb389c9eac81badc4bd9c27b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e2b18cfa28e78209d84a30bbacfa4539a85ee636689c58538621e572a4133b`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d49f8446481472986048351b40e96fcad9c44128630158e4319ae5b69b2feca`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 1.8 MB (1841114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0200fc9cacb2091aa304f8f172882d407f93a42a059f02ffc2ae0acaf682671`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 5.8 MB (5813078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2152b44d1116d5c1168680113e8fdd466ebcc7ee99c07fdfe1b3fbf39ba7e`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dac11d6a32393a766da366844f6656c0ef0a5443e7206d484655d856a5fb49`  
		Last Modified: Tue, 04 Feb 2025 19:23:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:fcac27653c73b5b7610b7b2e0c943a12ae91de1da06633457d0c9cd6b627629e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855a8edc4f8b24033f2315611577aa502a4cbe311c66c2391b1919db8af2f36c`

```dockerfile
```

-	Layers:
	-	`sha256:a6003ae2d7ac2094ff93c250171d0ca098c7a1e6a808c1c7bd1d6deff6bdadd8`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:978bfe51b8d6c8f3381934ea41c373766dfb48b535bba6ee5f243a193006a387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0540b6aada3775e3adfd4af21f094aa6460b9f09c3d305374563039cddb310e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaa4db2f41f33b473ee9e3d23526c2a5c3d06e4c63d975f8c329650781bfc50`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9aa243ee14d1187269f15a51bdd0121c76f084de8c950caf576d98b70e463`  
		Last Modified: Tue, 04 Feb 2025 07:09:55 GMT  
		Size: 2.6 MB (2582094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb78a29a1de352d83b7220b0199eb455f02534bd728d801150686e7e720a273`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 6.4 MB (6440730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca2cb4355672884568c1eff10a52aae16dac2db14e387628247926c8e48cdc`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4693e453a57e0f33af4fc1efea3a42a24e6381418d131d5aae599efae23f4eb8`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:c3db218145823880cb4767205ac0d1924a1ea93de5ec49956ff101d21069b0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d9f6f6871ede0f731ed47717e49df6baa968b54038d23c64b6a155a3d51f3f`

```dockerfile
```

-	Layers:
	-	`sha256:69b861da7d96b4f3975dc9cd80514ce15bc9a8d5bf9ab3fa2d4fe527e805d2cf`  
		Last Modified: Tue, 04 Feb 2025 07:09:52 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d5bc74f88a190910aebb2f129af625cf7b0d44d488bf251a42bd4bda622586`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:d602741ec001ec0bd0250c732c173274ba73887a8329ae21abc99750c26dcf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa781d6e5a453fc558205ea8ece3ac80a2ebe01b811e5ee602ec0053c7672138`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a6e7d0775375fc3d1e148728013c288c159edf09d7f89268dbd2b94adb02e`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3dd0162c40e5529113c4043b6a295aaba4477a5614ea6b37101eae051fae91`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 2.1 MB (2068737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89371216de8a5f913d8b5e84022a8820b75c22312a485ed5d4532ec0cc3ad89f`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 5.4 MB (5391937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c639f4e3d3bb15db262a0e635d9bfa87307da8ab93f4de0186dd76242d0bbf92`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d7fb587195e97fb81398a0cda1fed9beabbc7bebb633a6b41d52053b99a1a3`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:c571df89a1b0e77226d84a4ac833f4dda8adf0e04737412c9fdd4785a2c870aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991662535cd5d6a339176b8c9b909132cb73a6c2bebc27790b05b5987af78f30`

```dockerfile
```

-	Layers:
	-	`sha256:69a67dda4c3fd05bb160600c2ea45317f2ff7d014280d03aabc69b0795186b0b`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe307bfbbadd67d2deae85a17c6a372d6f7cce95ba0fedfa0d63d0b641fdde55`  
		Last Modified: Tue, 04 Feb 2025 07:19:33 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
