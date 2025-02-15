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
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7196154f35d46a29a47883173fde58814cfb6bb853a3c4a61cca9430cf1f8159`  
		Last Modified: Wed, 05 Feb 2025 05:01:35 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd3a971ecf92f9d804a86b505518d4c7b4542035f10e32e0b0c1482acdb10b`  
		Last Modified: Wed, 05 Feb 2025 05:01:35 GMT  
		Size: 2.4 MB (2401342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf2c3578328d143a0c13eac4322d3a7ba1c09d0bb431e3fb8bccb93fac7409`  
		Last Modified: Tue, 04 Feb 2025 21:21:10 GMT  
		Size: 6.5 MB (6482493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c051f65857ae1a80b319d09976092265d695e37fb3b0c69fcf014ec2643d7`  
		Last Modified: Tue, 04 Feb 2025 21:21:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7250acc401675038e92dc4a884eee09833a19e8adba51f183326d29fcc2ca6`  
		Last Modified: Tue, 04 Feb 2025 21:21:09 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:45 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:49 GMT  
		Size: 5.1 MB (5146798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4af1d5f9bc51aca0b2d09e04074a8f703930c4176b241a50d5ff3492ed47ce`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddabd99982fc01efcad0872592b12613c3b224baeb5ee91a78f4dbf692df1843`  
		Last Modified: Mon, 10 Feb 2025 00:47:49 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:55 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:01:17 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d40b8c33eed4efe5d43b21f211ccc96a002e6246f8b80e0e6f53f45a5c1334`  
		Last Modified: Mon, 10 Feb 2025 00:47:58 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f95294c83140a5f312fe0e0f3673b125c4718f4c4f531b3d58735aec00054b`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.9 MB (1855579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36310be6ec666453ebf3cbf37d05cda567f1a1a76d531826880d258eba1676e4`  
		Last Modified: Mon, 10 Feb 2025 00:47:58 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:02 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445785d885b1d4f4c62b22f763a4c23c5ef61dbcf8561b1f373f1122a157a32`  
		Last Modified: Wed, 05 Feb 2025 05:01:55 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e83c554a066c3f065b78b3307f98c54d4a3753271ce9398dcfb644a034658f`  
		Last Modified: Thu, 06 Feb 2025 05:16:17 GMT  
		Size: 2.2 MB (2247024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb79cb22695e7006611aaa6075a06126c1e46b6ec26a36bc59b2024e0692bb0`  
		Last Modified: Wed, 05 Feb 2025 05:05:08 GMT  
		Size: 5.5 MB (5491103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5f8d83d3803bc3372d3b2f901b9a579d0fe0892f5c55c7ffbcb4841f2509f`  
		Last Modified: Thu, 06 Feb 2025 05:16:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786f9a23b172afb3253a266af44a47a83cf5676a8b5fca783047e454090874f`  
		Last Modified: Wed, 05 Feb 2025 05:05:09 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:10 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a084f64ea6359821d9e6154f483978b063d4a671e0f59b1c9ed8b46ddb71f34`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b626f23d4ddc2323109743108c51c43a1fe05d501d0e7ded9368531db9ab7`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 2.4 MB (2398651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d27cbe14fcb4784bdf925fe2c6365bc3781a5667e0f64765c11702c029adab`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 6.0 MB (5956440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f9893150c1f1ac3dbda70997a910e68f713cbbbf84707c63383aa657bef3a2`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1739d36dcea86126749ade8e41d5e26216a42e18cce7c574440f9a6dc9541`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:18 GMT  
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
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e2b18cfa28e78209d84a30bbacfa4539a85ee636689c58538621e572a4133b`  
		Last Modified: Wed, 05 Feb 2025 08:46:19 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d49f8446481472986048351b40e96fcad9c44128630158e4319ae5b69b2feca`  
		Last Modified: Mon, 10 Feb 2025 00:48:21 GMT  
		Size: 1.8 MB (1841114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0200fc9cacb2091aa304f8f172882d407f93a42a059f02ffc2ae0acaf682671`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 5.8 MB (5813078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2152b44d1116d5c1168680113e8fdd466ebcc7ee99c07fdfe1b3fbf39ba7e`  
		Last Modified: Mon, 10 Feb 2025 00:48:21 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:25 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaa4db2f41f33b473ee9e3d23526c2a5c3d06e4c63d975f8c329650781bfc50`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9aa243ee14d1187269f15a51bdd0121c76f084de8c950caf576d98b70e463`  
		Last Modified: Mon, 10 Feb 2025 00:48:29 GMT  
		Size: 2.6 MB (2582094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb78a29a1de352d83b7220b0199eb455f02534bd728d801150686e7e720a273`  
		Last Modified: Mon, 10 Feb 2025 00:48:29 GMT  
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
		Last Modified: Wed, 05 Feb 2025 08:46:22 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d5bc74f88a190910aebb2f129af625cf7b0d44d488bf251a42bd4bda622586`  
		Last Modified: Wed, 05 Feb 2025 08:46:22 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a6e7d0775375fc3d1e148728013c288c159edf09d7f89268dbd2b94adb02e`  
		Last Modified: Mon, 10 Feb 2025 00:48:36 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:36 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:41 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:3d31eaca520d6c98cf7e32d37881cf706272125baa213206dcb74813b96911ca
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
$ docker pull spiped@sha256:7ac6025838d2bc44ef0e0fafaf5982e0fc4373b688d82fd8fcf05d8b97ca538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38502c733d8809263c7b9aef9befc5daac0d3a04ff701311a9df754f155a16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cbb4d14e8e59f505be1081c094889a892e335b697f6d0c4944a24ea721d7a2`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14bfd2d59e15880cb805303a18fd6fc6bc7e980d9ea46c8fddaf5072a577e7`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 7.9 KB (7910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f93bc17b0afa3407e99dd41fd4909fb96e359b2cb4612c46ded356003ed053`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 107.6 KB (107606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d9fa481a10b5130c48f48db6dbbe9a30b114bf719e8fe78001449bca914634`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585408ce1d63439f4bd520d967524dbc4d7e05e0d452c10c0dc69c4709d28e50`  
		Last Modified: Fri, 14 Feb 2025 19:24:09 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:91bf4effc5a6d6617632764adb1237e80919976921e5e3964f445b458cdffe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e2618e51acb8116b41dc6c3e43f214685385070706f8e531392d2a2b5a32f`

```dockerfile
```

-	Layers:
	-	`sha256:2744be77085e9a3321af7adcd6b3545cf6bfe6ed121b65fb85ada625330919e6`  
		Last Modified: Fri, 14 Feb 2025 23:04:36 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54db7fc3515a2461325d4de9fc957a390badfaab3a19d15be7868d671af57e54`  
		Last Modified: Fri, 14 Feb 2025 23:04:36 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:df12325bd4f67527eef210da2e785cccf9fee709f5839bb817095148b372e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2998ff82432e374d083b5b629bb256e09097ef1a9f83eea7d0ab00e5516ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb96c10a3bddea4cf5fb950ac49b22112a43dc906ac1a150c2651b21621161`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 89.1 KB (89139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7b5d6ff490ba5ca8f35cbb9b0d65060b194abf98610c588e99805f81d8e35d`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce1526e7b45007e682aa0fd80fbd9c1aa1537c854c4ee7ec3a9ad9037b0b67`  
		Last Modified: Fri, 14 Feb 2025 22:32:56 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45bcf73666108868c8355e70fce85a00349f2a252225bb8117406a06cb74e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f115d9a33ace52d319c520b7bfc5952bc13d2e791d27cd9170c8ee19fbeefa12`

```dockerfile
```

-	Layers:
	-	`sha256:787453bd83dce9d473689f5e983cfc99224f335f52dda1d16a0e5b0302d0f106`  
		Last Modified: Fri, 14 Feb 2025 23:04:37 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:243dcf0d023243a3b61aee8cb2b205b8fe61fc470d82257934575de8a39dcbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4241711a55ea959adb9faab82cba6408126c91cbec6d0af49161185a7031a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19710bb16bad23e16e1942366ab47dc67214cc321581fe20fa6c6ff243be2f`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66da5915b0a972b3b239c655a0797a199a02875109463ca9231c3c764542ebec`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e673af941f44b5da1cc7a57b60bb8dc744fb13be7bc3f249e2bffc928309186`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 81.7 KB (81660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f14c2ace1cb5e92040b8c20569aa9bc1f844aa0a668c66c2e9f43b1d1e71d3`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ed75a52b489ce3cd4cc2e7a2f1c304b60aca0c041bdbc91901221011420dc`  
		Last Modified: Fri, 14 Feb 2025 21:48:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c53f275713194c826f486ee2d8eaac5d420edc72a311fa688ae6e01b45c058c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aa7c5afef13f34cc7da917449cd3b867e0efd586073777180b4f3322da556d`

```dockerfile
```

-	Layers:
	-	`sha256:f944c77504e84bfc3b670136a0525be52ff36579d52cf1bdc60500ce40e8cd2b`  
		Last Modified: Fri, 14 Feb 2025 23:04:49 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965d6330c884c6fff95b9c9614e372105c03df6e0066d24b9719318d47c7a4fd`  
		Last Modified: Fri, 14 Feb 2025 23:04:49 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47f6dfb20be478dce9979b1e2494b93143aa488741abf7dc66ba6f515e197d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f508cb0494d2702e3a13db5d6fc2fd1ca41256c5959e0c4652e04994a249388a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9ace35db34c3304a810302430fb8aef69b65f583bd5e243d327da73e37c2a`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714b728344222c6dfa8f49bd713be1cc1d83e747cab7f88cfaac3caef9ebe58`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a90c58f039279dd810920bc66f47f0c176890374bc494740bfa97ecbfa53767`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 100.6 KB (100551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec4dd7aa4832397a2e91d629904b2a48c8298de7db9365c04d33ebbf1bedc`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26adf19273ff38a41503b067a8d1c5a35d4048e2291780e1ffa91def36425f6a`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b00591e00a263982885b0bee54a5d7c27ebcf5249fdaa334c51fc223467aabf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bf2a0d811c39c7759e43d4257b01711ffdf36fa3dceffc397887cc7f8fa9d0`

```dockerfile
```

-	Layers:
	-	`sha256:c19f26a228bd4be6de3aa9d8196866405d54f8bc38d014c8f26254efe16ae04e`  
		Last Modified: Fri, 14 Feb 2025 23:04:40 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a1704deb4400e22af6abe356817cdee187689b0cba34988ce227508adfd78f`  
		Last Modified: Fri, 14 Feb 2025 23:04:40 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:61b83f6f4da433231db95db1a13fe86dbe85aaecde12dcb9a669f0b0ed0b6e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea95baf750c2a2749ec794c8238c510e5792dc8857ed4a3645d071f394823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de02b79b34b2bc491f8c7e8607233cc124ed19295cf456e64382e5afc72fbd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1d235c70003f61e0de885229553d72517e82d7f45df6d561b480b2cd9c5fc`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a0453a1d3c0248fee96f306a8ede9aa3d7f2dd02652a8dbdff1b0d8c9438b`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 120.1 KB (120130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e021c9b7ed20e7390deef74c89a7a5540f6309865137308f9a80ac607be260f`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872beb154170ecfc36e7b32d8019cfc1e29a60d26d251929d28131277a7fd0c`  
		Last Modified: Fri, 14 Feb 2025 19:11:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4c3f4670bd80d3c0136a64e6f27ff285948a413faee904ef1c460b8f51d4e516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5f2d723a731a066cf77f9a59824e65134fef732e62678056b932016e17282`

```dockerfile
```

-	Layers:
	-	`sha256:b1e174fd16318b9fb1190150ba833822f30825a45606ea9af9ec1723ce03867c`  
		Last Modified: Fri, 14 Feb 2025 23:04:42 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e4a7deb35e498340a41c762c8316785005a9ab4e93a2ab0a677fc623e721fd`  
		Last Modified: Fri, 14 Feb 2025 23:04:42 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:0763e833f3d2e767ad7c1ab64d3a1778d9543cffbe2731d7f8c40bee27d44a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cde70893ef4a0b94f4624b6bd8ea6a51522d65faf50b2646cac866d386dafe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ff6ba800883c9495b3d17b7735935035a83bdb153e380d5f5f6c80c3573c5`  
		Last Modified: Sat, 15 Feb 2025 09:24:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb59aefcf51d96da7771cb0671fa43ebe8e636326ce4db947ff446ea9b4eaa`  
		Last Modified: Sat, 15 Feb 2025 09:24:34 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b657e1255fd2cfb228ed06e75846652368ff0d80307f8b278c3db5e5558f4f64`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 112.6 KB (112646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de73da0d337b9f7fd4e60cf9b67d3592f9e6f6f539421800b167a2735f1bdb`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ad280a5133fac353984bead0c9962cf3a9c94714d7806a61832de902c8e929`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:522f73a6a1f1e955300602615eb9a993897959108be79c09d235f1db5e488940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95185cb2bad6bef09c576b8e4d9d0bf6563783c294a92e69f28b758029f2ac0`

```dockerfile
```

-	Layers:
	-	`sha256:eb306f89b50101c069df46fb92b19620767f2503887c596aedfc415f347a4246`  
		Last Modified: Fri, 14 Feb 2025 23:04:43 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c821af9afc609e7780dcfb284627dd581cbede4a66c24cc04b41f590c6244531`  
		Last Modified: Fri, 14 Feb 2025 23:04:43 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
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
		Last Modified: Fri, 14 Feb 2025 23:04:44 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Fri, 14 Feb 2025 23:04:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:de25b12e766fe57e24177257227c53d5a27fc1a3ca4abe48e8bc60e0351bdaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb095475057abb702522c9d705013168c8522d986f39b9047739ee6efe16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a28161d111a002ad388fefdd709f7bb67cb61071bfdfa7960202816d14c2e2`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30984a12769648824acad7e1386b7ba7193bf81929e37f44ce5f3c04f82acc6`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5b85eee8dde04ba3dbc50eb3b644d79d18255b1eb4dfa5c888403b0ad97cc`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.9 KB (96918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860fa829f189bb5e960d5036162d15a1aac72e9ce8bed6c40b68549752c2199`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb23aa9487acbddced4252bb38b3510de48d049a3a347fcfb6b24f40c9ff730`  
		Last Modified: Fri, 14 Feb 2025 22:26:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2065dca98493b203898ab91ad7de40fb703351116ab3bfc12c9a52026ce6c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f932f07832d03eeec80862781aec2cb3efb7c48fadec873786bd1c8af939e6f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b919ae512d1430c2c7488ea884c9bc49e2ae21b5170043f2a370c90e9af6c60`  
		Last Modified: Fri, 14 Feb 2025 23:04:46 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf9c418603cd0c1fdf650dfd352e9ae11c6eec907de4024a31a994019249053`  
		Last Modified: Fri, 14 Feb 2025 23:04:46 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7196154f35d46a29a47883173fde58814cfb6bb853a3c4a61cca9430cf1f8159`  
		Last Modified: Wed, 05 Feb 2025 05:01:35 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd3a971ecf92f9d804a86b505518d4c7b4542035f10e32e0b0c1482acdb10b`  
		Last Modified: Wed, 05 Feb 2025 05:01:35 GMT  
		Size: 2.4 MB (2401342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf2c3578328d143a0c13eac4322d3a7ba1c09d0bb431e3fb8bccb93fac7409`  
		Last Modified: Tue, 04 Feb 2025 21:21:10 GMT  
		Size: 6.5 MB (6482493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c051f65857ae1a80b319d09976092265d695e37fb3b0c69fcf014ec2643d7`  
		Last Modified: Tue, 04 Feb 2025 21:21:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7250acc401675038e92dc4a884eee09833a19e8adba51f183326d29fcc2ca6`  
		Last Modified: Tue, 04 Feb 2025 21:21:09 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:45 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:49 GMT  
		Size: 5.1 MB (5146798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4af1d5f9bc51aca0b2d09e04074a8f703930c4176b241a50d5ff3492ed47ce`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddabd99982fc01efcad0872592b12613c3b224baeb5ee91a78f4dbf692df1843`  
		Last Modified: Mon, 10 Feb 2025 00:47:49 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:55 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:01:17 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d40b8c33eed4efe5d43b21f211ccc96a002e6246f8b80e0e6f53f45a5c1334`  
		Last Modified: Mon, 10 Feb 2025 00:47:58 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f95294c83140a5f312fe0e0f3673b125c4718f4c4f531b3d58735aec00054b`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.9 MB (1855579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36310be6ec666453ebf3cbf37d05cda567f1a1a76d531826880d258eba1676e4`  
		Last Modified: Mon, 10 Feb 2025 00:47:58 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:02 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445785d885b1d4f4c62b22f763a4c23c5ef61dbcf8561b1f373f1122a157a32`  
		Last Modified: Wed, 05 Feb 2025 05:01:55 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e83c554a066c3f065b78b3307f98c54d4a3753271ce9398dcfb644a034658f`  
		Last Modified: Thu, 06 Feb 2025 05:16:17 GMT  
		Size: 2.2 MB (2247024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb79cb22695e7006611aaa6075a06126c1e46b6ec26a36bc59b2024e0692bb0`  
		Last Modified: Wed, 05 Feb 2025 05:05:08 GMT  
		Size: 5.5 MB (5491103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5f8d83d3803bc3372d3b2f901b9a579d0fe0892f5c55c7ffbcb4841f2509f`  
		Last Modified: Thu, 06 Feb 2025 05:16:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786f9a23b172afb3253a266af44a47a83cf5676a8b5fca783047e454090874f`  
		Last Modified: Wed, 05 Feb 2025 05:05:09 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:10 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a084f64ea6359821d9e6154f483978b063d4a671e0f59b1c9ed8b46ddb71f34`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b626f23d4ddc2323109743108c51c43a1fe05d501d0e7ded9368531db9ab7`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 2.4 MB (2398651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d27cbe14fcb4784bdf925fe2c6365bc3781a5667e0f64765c11702c029adab`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 6.0 MB (5956440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f9893150c1f1ac3dbda70997a910e68f713cbbbf84707c63383aa657bef3a2`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1739d36dcea86126749ade8e41d5e26216a42e18cce7c574440f9a6dc9541`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:18 GMT  
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
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e2b18cfa28e78209d84a30bbacfa4539a85ee636689c58538621e572a4133b`  
		Last Modified: Wed, 05 Feb 2025 08:46:19 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d49f8446481472986048351b40e96fcad9c44128630158e4319ae5b69b2feca`  
		Last Modified: Mon, 10 Feb 2025 00:48:21 GMT  
		Size: 1.8 MB (1841114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0200fc9cacb2091aa304f8f172882d407f93a42a059f02ffc2ae0acaf682671`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 5.8 MB (5813078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2152b44d1116d5c1168680113e8fdd466ebcc7ee99c07fdfe1b3fbf39ba7e`  
		Last Modified: Mon, 10 Feb 2025 00:48:21 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:25 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaa4db2f41f33b473ee9e3d23526c2a5c3d06e4c63d975f8c329650781bfc50`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9aa243ee14d1187269f15a51bdd0121c76f084de8c950caf576d98b70e463`  
		Last Modified: Mon, 10 Feb 2025 00:48:29 GMT  
		Size: 2.6 MB (2582094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb78a29a1de352d83b7220b0199eb455f02534bd728d801150686e7e720a273`  
		Last Modified: Mon, 10 Feb 2025 00:48:29 GMT  
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
		Last Modified: Wed, 05 Feb 2025 08:46:22 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d5bc74f88a190910aebb2f129af625cf7b0d44d488bf251a42bd4bda622586`  
		Last Modified: Wed, 05 Feb 2025 08:46:22 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a6e7d0775375fc3d1e148728013c288c159edf09d7f89268dbd2b94adb02e`  
		Last Modified: Mon, 10 Feb 2025 00:48:36 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:36 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:41 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:3d31eaca520d6c98cf7e32d37881cf706272125baa213206dcb74813b96911ca
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
$ docker pull spiped@sha256:7ac6025838d2bc44ef0e0fafaf5982e0fc4373b688d82fd8fcf05d8b97ca538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38502c733d8809263c7b9aef9befc5daac0d3a04ff701311a9df754f155a16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cbb4d14e8e59f505be1081c094889a892e335b697f6d0c4944a24ea721d7a2`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14bfd2d59e15880cb805303a18fd6fc6bc7e980d9ea46c8fddaf5072a577e7`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 7.9 KB (7910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f93bc17b0afa3407e99dd41fd4909fb96e359b2cb4612c46ded356003ed053`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 107.6 KB (107606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d9fa481a10b5130c48f48db6dbbe9a30b114bf719e8fe78001449bca914634`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585408ce1d63439f4bd520d967524dbc4d7e05e0d452c10c0dc69c4709d28e50`  
		Last Modified: Fri, 14 Feb 2025 19:24:09 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:91bf4effc5a6d6617632764adb1237e80919976921e5e3964f445b458cdffe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e2618e51acb8116b41dc6c3e43f214685385070706f8e531392d2a2b5a32f`

```dockerfile
```

-	Layers:
	-	`sha256:2744be77085e9a3321af7adcd6b3545cf6bfe6ed121b65fb85ada625330919e6`  
		Last Modified: Fri, 14 Feb 2025 23:04:36 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54db7fc3515a2461325d4de9fc957a390badfaab3a19d15be7868d671af57e54`  
		Last Modified: Fri, 14 Feb 2025 23:04:36 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:df12325bd4f67527eef210da2e785cccf9fee709f5839bb817095148b372e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2998ff82432e374d083b5b629bb256e09097ef1a9f83eea7d0ab00e5516ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb96c10a3bddea4cf5fb950ac49b22112a43dc906ac1a150c2651b21621161`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 89.1 KB (89139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7b5d6ff490ba5ca8f35cbb9b0d65060b194abf98610c588e99805f81d8e35d`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce1526e7b45007e682aa0fd80fbd9c1aa1537c854c4ee7ec3a9ad9037b0b67`  
		Last Modified: Fri, 14 Feb 2025 22:32:56 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45bcf73666108868c8355e70fce85a00349f2a252225bb8117406a06cb74e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f115d9a33ace52d319c520b7bfc5952bc13d2e791d27cd9170c8ee19fbeefa12`

```dockerfile
```

-	Layers:
	-	`sha256:787453bd83dce9d473689f5e983cfc99224f335f52dda1d16a0e5b0302d0f106`  
		Last Modified: Fri, 14 Feb 2025 23:04:37 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:243dcf0d023243a3b61aee8cb2b205b8fe61fc470d82257934575de8a39dcbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4241711a55ea959adb9faab82cba6408126c91cbec6d0af49161185a7031a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19710bb16bad23e16e1942366ab47dc67214cc321581fe20fa6c6ff243be2f`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66da5915b0a972b3b239c655a0797a199a02875109463ca9231c3c764542ebec`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e673af941f44b5da1cc7a57b60bb8dc744fb13be7bc3f249e2bffc928309186`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 81.7 KB (81660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f14c2ace1cb5e92040b8c20569aa9bc1f844aa0a668c66c2e9f43b1d1e71d3`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ed75a52b489ce3cd4cc2e7a2f1c304b60aca0c041bdbc91901221011420dc`  
		Last Modified: Fri, 14 Feb 2025 21:48:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c53f275713194c826f486ee2d8eaac5d420edc72a311fa688ae6e01b45c058c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aa7c5afef13f34cc7da917449cd3b867e0efd586073777180b4f3322da556d`

```dockerfile
```

-	Layers:
	-	`sha256:f944c77504e84bfc3b670136a0525be52ff36579d52cf1bdc60500ce40e8cd2b`  
		Last Modified: Fri, 14 Feb 2025 23:04:49 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965d6330c884c6fff95b9c9614e372105c03df6e0066d24b9719318d47c7a4fd`  
		Last Modified: Fri, 14 Feb 2025 23:04:49 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47f6dfb20be478dce9979b1e2494b93143aa488741abf7dc66ba6f515e197d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f508cb0494d2702e3a13db5d6fc2fd1ca41256c5959e0c4652e04994a249388a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9ace35db34c3304a810302430fb8aef69b65f583bd5e243d327da73e37c2a`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714b728344222c6dfa8f49bd713be1cc1d83e747cab7f88cfaac3caef9ebe58`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a90c58f039279dd810920bc66f47f0c176890374bc494740bfa97ecbfa53767`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 100.6 KB (100551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec4dd7aa4832397a2e91d629904b2a48c8298de7db9365c04d33ebbf1bedc`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26adf19273ff38a41503b067a8d1c5a35d4048e2291780e1ffa91def36425f6a`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b00591e00a263982885b0bee54a5d7c27ebcf5249fdaa334c51fc223467aabf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bf2a0d811c39c7759e43d4257b01711ffdf36fa3dceffc397887cc7f8fa9d0`

```dockerfile
```

-	Layers:
	-	`sha256:c19f26a228bd4be6de3aa9d8196866405d54f8bc38d014c8f26254efe16ae04e`  
		Last Modified: Fri, 14 Feb 2025 23:04:40 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a1704deb4400e22af6abe356817cdee187689b0cba34988ce227508adfd78f`  
		Last Modified: Fri, 14 Feb 2025 23:04:40 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:61b83f6f4da433231db95db1a13fe86dbe85aaecde12dcb9a669f0b0ed0b6e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea95baf750c2a2749ec794c8238c510e5792dc8857ed4a3645d071f394823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de02b79b34b2bc491f8c7e8607233cc124ed19295cf456e64382e5afc72fbd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1d235c70003f61e0de885229553d72517e82d7f45df6d561b480b2cd9c5fc`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a0453a1d3c0248fee96f306a8ede9aa3d7f2dd02652a8dbdff1b0d8c9438b`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 120.1 KB (120130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e021c9b7ed20e7390deef74c89a7a5540f6309865137308f9a80ac607be260f`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872beb154170ecfc36e7b32d8019cfc1e29a60d26d251929d28131277a7fd0c`  
		Last Modified: Fri, 14 Feb 2025 19:11:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4c3f4670bd80d3c0136a64e6f27ff285948a413faee904ef1c460b8f51d4e516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5f2d723a731a066cf77f9a59824e65134fef732e62678056b932016e17282`

```dockerfile
```

-	Layers:
	-	`sha256:b1e174fd16318b9fb1190150ba833822f30825a45606ea9af9ec1723ce03867c`  
		Last Modified: Fri, 14 Feb 2025 23:04:42 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e4a7deb35e498340a41c762c8316785005a9ab4e93a2ab0a677fc623e721fd`  
		Last Modified: Fri, 14 Feb 2025 23:04:42 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:0763e833f3d2e767ad7c1ab64d3a1778d9543cffbe2731d7f8c40bee27d44a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cde70893ef4a0b94f4624b6bd8ea6a51522d65faf50b2646cac866d386dafe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ff6ba800883c9495b3d17b7735935035a83bdb153e380d5f5f6c80c3573c5`  
		Last Modified: Sat, 15 Feb 2025 09:24:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb59aefcf51d96da7771cb0671fa43ebe8e636326ce4db947ff446ea9b4eaa`  
		Last Modified: Sat, 15 Feb 2025 09:24:34 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b657e1255fd2cfb228ed06e75846652368ff0d80307f8b278c3db5e5558f4f64`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 112.6 KB (112646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de73da0d337b9f7fd4e60cf9b67d3592f9e6f6f539421800b167a2735f1bdb`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ad280a5133fac353984bead0c9962cf3a9c94714d7806a61832de902c8e929`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:522f73a6a1f1e955300602615eb9a993897959108be79c09d235f1db5e488940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95185cb2bad6bef09c576b8e4d9d0bf6563783c294a92e69f28b758029f2ac0`

```dockerfile
```

-	Layers:
	-	`sha256:eb306f89b50101c069df46fb92b19620767f2503887c596aedfc415f347a4246`  
		Last Modified: Fri, 14 Feb 2025 23:04:43 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c821af9afc609e7780dcfb284627dd581cbede4a66c24cc04b41f590c6244531`  
		Last Modified: Fri, 14 Feb 2025 23:04:43 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
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
		Last Modified: Fri, 14 Feb 2025 23:04:44 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Fri, 14 Feb 2025 23:04:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:de25b12e766fe57e24177257227c53d5a27fc1a3ca4abe48e8bc60e0351bdaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb095475057abb702522c9d705013168c8522d986f39b9047739ee6efe16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a28161d111a002ad388fefdd709f7bb67cb61071bfdfa7960202816d14c2e2`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30984a12769648824acad7e1386b7ba7193bf81929e37f44ce5f3c04f82acc6`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5b85eee8dde04ba3dbc50eb3b644d79d18255b1eb4dfa5c888403b0ad97cc`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.9 KB (96918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860fa829f189bb5e960d5036162d15a1aac72e9ce8bed6c40b68549752c2199`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb23aa9487acbddced4252bb38b3510de48d049a3a347fcfb6b24f40c9ff730`  
		Last Modified: Fri, 14 Feb 2025 22:26:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2065dca98493b203898ab91ad7de40fb703351116ab3bfc12c9a52026ce6c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f932f07832d03eeec80862781aec2cb3efb7c48fadec873786bd1c8af939e6f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b919ae512d1430c2c7488ea884c9bc49e2ae21b5170043f2a370c90e9af6c60`  
		Last Modified: Fri, 14 Feb 2025 23:04:46 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf9c418603cd0c1fdf650dfd352e9ae11c6eec907de4024a31a994019249053`  
		Last Modified: Fri, 14 Feb 2025 23:04:46 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7196154f35d46a29a47883173fde58814cfb6bb853a3c4a61cca9430cf1f8159`  
		Last Modified: Wed, 05 Feb 2025 05:01:35 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd3a971ecf92f9d804a86b505518d4c7b4542035f10e32e0b0c1482acdb10b`  
		Last Modified: Wed, 05 Feb 2025 05:01:35 GMT  
		Size: 2.4 MB (2401342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf2c3578328d143a0c13eac4322d3a7ba1c09d0bb431e3fb8bccb93fac7409`  
		Last Modified: Tue, 04 Feb 2025 21:21:10 GMT  
		Size: 6.5 MB (6482493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c051f65857ae1a80b319d09976092265d695e37fb3b0c69fcf014ec2643d7`  
		Last Modified: Tue, 04 Feb 2025 21:21:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7250acc401675038e92dc4a884eee09833a19e8adba51f183326d29fcc2ca6`  
		Last Modified: Tue, 04 Feb 2025 21:21:09 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:45 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:49 GMT  
		Size: 5.1 MB (5146798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4af1d5f9bc51aca0b2d09e04074a8f703930c4176b241a50d5ff3492ed47ce`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddabd99982fc01efcad0872592b12613c3b224baeb5ee91a78f4dbf692df1843`  
		Last Modified: Mon, 10 Feb 2025 00:47:49 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:55 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:01:17 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d40b8c33eed4efe5d43b21f211ccc96a002e6246f8b80e0e6f53f45a5c1334`  
		Last Modified: Mon, 10 Feb 2025 00:47:58 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f95294c83140a5f312fe0e0f3673b125c4718f4c4f531b3d58735aec00054b`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.9 MB (1855579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36310be6ec666453ebf3cbf37d05cda567f1a1a76d531826880d258eba1676e4`  
		Last Modified: Mon, 10 Feb 2025 00:47:58 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:02 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445785d885b1d4f4c62b22f763a4c23c5ef61dbcf8561b1f373f1122a157a32`  
		Last Modified: Wed, 05 Feb 2025 05:01:55 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e83c554a066c3f065b78b3307f98c54d4a3753271ce9398dcfb644a034658f`  
		Last Modified: Thu, 06 Feb 2025 05:16:17 GMT  
		Size: 2.2 MB (2247024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb79cb22695e7006611aaa6075a06126c1e46b6ec26a36bc59b2024e0692bb0`  
		Last Modified: Wed, 05 Feb 2025 05:05:08 GMT  
		Size: 5.5 MB (5491103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5f8d83d3803bc3372d3b2f901b9a579d0fe0892f5c55c7ffbcb4841f2509f`  
		Last Modified: Thu, 06 Feb 2025 05:16:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786f9a23b172afb3253a266af44a47a83cf5676a8b5fca783047e454090874f`  
		Last Modified: Wed, 05 Feb 2025 05:05:09 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:10 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a084f64ea6359821d9e6154f483978b063d4a671e0f59b1c9ed8b46ddb71f34`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b626f23d4ddc2323109743108c51c43a1fe05d501d0e7ded9368531db9ab7`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 2.4 MB (2398651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d27cbe14fcb4784bdf925fe2c6365bc3781a5667e0f64765c11702c029adab`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 6.0 MB (5956440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f9893150c1f1ac3dbda70997a910e68f713cbbbf84707c63383aa657bef3a2`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1739d36dcea86126749ade8e41d5e26216a42e18cce7c574440f9a6dc9541`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:18 GMT  
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
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e2b18cfa28e78209d84a30bbacfa4539a85ee636689c58538621e572a4133b`  
		Last Modified: Wed, 05 Feb 2025 08:46:19 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d49f8446481472986048351b40e96fcad9c44128630158e4319ae5b69b2feca`  
		Last Modified: Mon, 10 Feb 2025 00:48:21 GMT  
		Size: 1.8 MB (1841114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0200fc9cacb2091aa304f8f172882d407f93a42a059f02ffc2ae0acaf682671`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 5.8 MB (5813078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2152b44d1116d5c1168680113e8fdd466ebcc7ee99c07fdfe1b3fbf39ba7e`  
		Last Modified: Mon, 10 Feb 2025 00:48:21 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:25 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaa4db2f41f33b473ee9e3d23526c2a5c3d06e4c63d975f8c329650781bfc50`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9aa243ee14d1187269f15a51bdd0121c76f084de8c950caf576d98b70e463`  
		Last Modified: Mon, 10 Feb 2025 00:48:29 GMT  
		Size: 2.6 MB (2582094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb78a29a1de352d83b7220b0199eb455f02534bd728d801150686e7e720a273`  
		Last Modified: Mon, 10 Feb 2025 00:48:29 GMT  
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
		Last Modified: Wed, 05 Feb 2025 08:46:22 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d5bc74f88a190910aebb2f129af625cf7b0d44d488bf251a42bd4bda622586`  
		Last Modified: Wed, 05 Feb 2025 08:46:22 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a6e7d0775375fc3d1e148728013c288c159edf09d7f89268dbd2b94adb02e`  
		Last Modified: Mon, 10 Feb 2025 00:48:36 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:36 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:41 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.3-alpine`

```console
$ docker pull spiped@sha256:3d31eaca520d6c98cf7e32d37881cf706272125baa213206dcb74813b96911ca
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
$ docker pull spiped@sha256:7ac6025838d2bc44ef0e0fafaf5982e0fc4373b688d82fd8fcf05d8b97ca538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38502c733d8809263c7b9aef9befc5daac0d3a04ff701311a9df754f155a16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cbb4d14e8e59f505be1081c094889a892e335b697f6d0c4944a24ea721d7a2`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14bfd2d59e15880cb805303a18fd6fc6bc7e980d9ea46c8fddaf5072a577e7`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 7.9 KB (7910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f93bc17b0afa3407e99dd41fd4909fb96e359b2cb4612c46ded356003ed053`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 107.6 KB (107606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d9fa481a10b5130c48f48db6dbbe9a30b114bf719e8fe78001449bca914634`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585408ce1d63439f4bd520d967524dbc4d7e05e0d452c10c0dc69c4709d28e50`  
		Last Modified: Fri, 14 Feb 2025 19:24:09 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:91bf4effc5a6d6617632764adb1237e80919976921e5e3964f445b458cdffe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e2618e51acb8116b41dc6c3e43f214685385070706f8e531392d2a2b5a32f`

```dockerfile
```

-	Layers:
	-	`sha256:2744be77085e9a3321af7adcd6b3545cf6bfe6ed121b65fb85ada625330919e6`  
		Last Modified: Fri, 14 Feb 2025 23:04:36 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54db7fc3515a2461325d4de9fc957a390badfaab3a19d15be7868d671af57e54`  
		Last Modified: Fri, 14 Feb 2025 23:04:36 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:df12325bd4f67527eef210da2e785cccf9fee709f5839bb817095148b372e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2998ff82432e374d083b5b629bb256e09097ef1a9f83eea7d0ab00e5516ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb96c10a3bddea4cf5fb950ac49b22112a43dc906ac1a150c2651b21621161`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 89.1 KB (89139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7b5d6ff490ba5ca8f35cbb9b0d65060b194abf98610c588e99805f81d8e35d`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce1526e7b45007e682aa0fd80fbd9c1aa1537c854c4ee7ec3a9ad9037b0b67`  
		Last Modified: Fri, 14 Feb 2025 22:32:56 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45bcf73666108868c8355e70fce85a00349f2a252225bb8117406a06cb74e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f115d9a33ace52d319c520b7bfc5952bc13d2e791d27cd9170c8ee19fbeefa12`

```dockerfile
```

-	Layers:
	-	`sha256:787453bd83dce9d473689f5e983cfc99224f335f52dda1d16a0e5b0302d0f106`  
		Last Modified: Fri, 14 Feb 2025 23:04:37 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:243dcf0d023243a3b61aee8cb2b205b8fe61fc470d82257934575de8a39dcbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4241711a55ea959adb9faab82cba6408126c91cbec6d0af49161185a7031a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19710bb16bad23e16e1942366ab47dc67214cc321581fe20fa6c6ff243be2f`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66da5915b0a972b3b239c655a0797a199a02875109463ca9231c3c764542ebec`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e673af941f44b5da1cc7a57b60bb8dc744fb13be7bc3f249e2bffc928309186`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 81.7 KB (81660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f14c2ace1cb5e92040b8c20569aa9bc1f844aa0a668c66c2e9f43b1d1e71d3`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ed75a52b489ce3cd4cc2e7a2f1c304b60aca0c041bdbc91901221011420dc`  
		Last Modified: Fri, 14 Feb 2025 21:48:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c53f275713194c826f486ee2d8eaac5d420edc72a311fa688ae6e01b45c058c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aa7c5afef13f34cc7da917449cd3b867e0efd586073777180b4f3322da556d`

```dockerfile
```

-	Layers:
	-	`sha256:f944c77504e84bfc3b670136a0525be52ff36579d52cf1bdc60500ce40e8cd2b`  
		Last Modified: Fri, 14 Feb 2025 23:04:49 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965d6330c884c6fff95b9c9614e372105c03df6e0066d24b9719318d47c7a4fd`  
		Last Modified: Fri, 14 Feb 2025 23:04:49 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47f6dfb20be478dce9979b1e2494b93143aa488741abf7dc66ba6f515e197d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f508cb0494d2702e3a13db5d6fc2fd1ca41256c5959e0c4652e04994a249388a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9ace35db34c3304a810302430fb8aef69b65f583bd5e243d327da73e37c2a`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714b728344222c6dfa8f49bd713be1cc1d83e747cab7f88cfaac3caef9ebe58`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a90c58f039279dd810920bc66f47f0c176890374bc494740bfa97ecbfa53767`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 100.6 KB (100551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec4dd7aa4832397a2e91d629904b2a48c8298de7db9365c04d33ebbf1bedc`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26adf19273ff38a41503b067a8d1c5a35d4048e2291780e1ffa91def36425f6a`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b00591e00a263982885b0bee54a5d7c27ebcf5249fdaa334c51fc223467aabf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bf2a0d811c39c7759e43d4257b01711ffdf36fa3dceffc397887cc7f8fa9d0`

```dockerfile
```

-	Layers:
	-	`sha256:c19f26a228bd4be6de3aa9d8196866405d54f8bc38d014c8f26254efe16ae04e`  
		Last Modified: Fri, 14 Feb 2025 23:04:40 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a1704deb4400e22af6abe356817cdee187689b0cba34988ce227508adfd78f`  
		Last Modified: Fri, 14 Feb 2025 23:04:40 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; 386

```console
$ docker pull spiped@sha256:61b83f6f4da433231db95db1a13fe86dbe85aaecde12dcb9a669f0b0ed0b6e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea95baf750c2a2749ec794c8238c510e5792dc8857ed4a3645d071f394823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de02b79b34b2bc491f8c7e8607233cc124ed19295cf456e64382e5afc72fbd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1d235c70003f61e0de885229553d72517e82d7f45df6d561b480b2cd9c5fc`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a0453a1d3c0248fee96f306a8ede9aa3d7f2dd02652a8dbdff1b0d8c9438b`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 120.1 KB (120130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e021c9b7ed20e7390deef74c89a7a5540f6309865137308f9a80ac607be260f`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872beb154170ecfc36e7b32d8019cfc1e29a60d26d251929d28131277a7fd0c`  
		Last Modified: Fri, 14 Feb 2025 19:11:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4c3f4670bd80d3c0136a64e6f27ff285948a413faee904ef1c460b8f51d4e516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5f2d723a731a066cf77f9a59824e65134fef732e62678056b932016e17282`

```dockerfile
```

-	Layers:
	-	`sha256:b1e174fd16318b9fb1190150ba833822f30825a45606ea9af9ec1723ce03867c`  
		Last Modified: Fri, 14 Feb 2025 23:04:42 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e4a7deb35e498340a41c762c8316785005a9ab4e93a2ab0a677fc623e721fd`  
		Last Modified: Fri, 14 Feb 2025 23:04:42 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:0763e833f3d2e767ad7c1ab64d3a1778d9543cffbe2731d7f8c40bee27d44a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cde70893ef4a0b94f4624b6bd8ea6a51522d65faf50b2646cac866d386dafe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ff6ba800883c9495b3d17b7735935035a83bdb153e380d5f5f6c80c3573c5`  
		Last Modified: Sat, 15 Feb 2025 09:24:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb59aefcf51d96da7771cb0671fa43ebe8e636326ce4db947ff446ea9b4eaa`  
		Last Modified: Sat, 15 Feb 2025 09:24:34 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b657e1255fd2cfb228ed06e75846652368ff0d80307f8b278c3db5e5558f4f64`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 112.6 KB (112646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de73da0d337b9f7fd4e60cf9b67d3592f9e6f6f539421800b167a2735f1bdb`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ad280a5133fac353984bead0c9962cf3a9c94714d7806a61832de902c8e929`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:522f73a6a1f1e955300602615eb9a993897959108be79c09d235f1db5e488940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95185cb2bad6bef09c576b8e4d9d0bf6563783c294a92e69f28b758029f2ac0`

```dockerfile
```

-	Layers:
	-	`sha256:eb306f89b50101c069df46fb92b19620767f2503887c596aedfc415f347a4246`  
		Last Modified: Fri, 14 Feb 2025 23:04:43 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c821af9afc609e7780dcfb284627dd581cbede4a66c24cc04b41f590c6244531`  
		Last Modified: Fri, 14 Feb 2025 23:04:43 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
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
		Last Modified: Fri, 14 Feb 2025 23:04:44 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Fri, 14 Feb 2025 23:04:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:de25b12e766fe57e24177257227c53d5a27fc1a3ca4abe48e8bc60e0351bdaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb095475057abb702522c9d705013168c8522d986f39b9047739ee6efe16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a28161d111a002ad388fefdd709f7bb67cb61071bfdfa7960202816d14c2e2`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30984a12769648824acad7e1386b7ba7193bf81929e37f44ce5f3c04f82acc6`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5b85eee8dde04ba3dbc50eb3b644d79d18255b1eb4dfa5c888403b0ad97cc`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.9 KB (96918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860fa829f189bb5e960d5036162d15a1aac72e9ce8bed6c40b68549752c2199`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb23aa9487acbddced4252bb38b3510de48d049a3a347fcfb6b24f40c9ff730`  
		Last Modified: Fri, 14 Feb 2025 22:26:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2065dca98493b203898ab91ad7de40fb703351116ab3bfc12c9a52026ce6c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f932f07832d03eeec80862781aec2cb3efb7c48fadec873786bd1c8af939e6f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b919ae512d1430c2c7488ea884c9bc49e2ae21b5170043f2a370c90e9af6c60`  
		Last Modified: Fri, 14 Feb 2025 23:04:46 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf9c418603cd0c1fdf650dfd352e9ae11c6eec907de4024a31a994019249053`  
		Last Modified: Fri, 14 Feb 2025 23:04:46 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:3d31eaca520d6c98cf7e32d37881cf706272125baa213206dcb74813b96911ca
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
$ docker pull spiped@sha256:7ac6025838d2bc44ef0e0fafaf5982e0fc4373b688d82fd8fcf05d8b97ca538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38502c733d8809263c7b9aef9befc5daac0d3a04ff701311a9df754f155a16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cbb4d14e8e59f505be1081c094889a892e335b697f6d0c4944a24ea721d7a2`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14bfd2d59e15880cb805303a18fd6fc6bc7e980d9ea46c8fddaf5072a577e7`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 7.9 KB (7910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f93bc17b0afa3407e99dd41fd4909fb96e359b2cb4612c46ded356003ed053`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 107.6 KB (107606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d9fa481a10b5130c48f48db6dbbe9a30b114bf719e8fe78001449bca914634`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585408ce1d63439f4bd520d967524dbc4d7e05e0d452c10c0dc69c4709d28e50`  
		Last Modified: Fri, 14 Feb 2025 19:24:09 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:91bf4effc5a6d6617632764adb1237e80919976921e5e3964f445b458cdffe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e2618e51acb8116b41dc6c3e43f214685385070706f8e531392d2a2b5a32f`

```dockerfile
```

-	Layers:
	-	`sha256:2744be77085e9a3321af7adcd6b3545cf6bfe6ed121b65fb85ada625330919e6`  
		Last Modified: Fri, 14 Feb 2025 23:04:36 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54db7fc3515a2461325d4de9fc957a390badfaab3a19d15be7868d671af57e54`  
		Last Modified: Fri, 14 Feb 2025 23:04:36 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:df12325bd4f67527eef210da2e785cccf9fee709f5839bb817095148b372e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2998ff82432e374d083b5b629bb256e09097ef1a9f83eea7d0ab00e5516ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb96c10a3bddea4cf5fb950ac49b22112a43dc906ac1a150c2651b21621161`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 89.1 KB (89139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7b5d6ff490ba5ca8f35cbb9b0d65060b194abf98610c588e99805f81d8e35d`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce1526e7b45007e682aa0fd80fbd9c1aa1537c854c4ee7ec3a9ad9037b0b67`  
		Last Modified: Fri, 14 Feb 2025 22:32:56 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45bcf73666108868c8355e70fce85a00349f2a252225bb8117406a06cb74e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f115d9a33ace52d319c520b7bfc5952bc13d2e791d27cd9170c8ee19fbeefa12`

```dockerfile
```

-	Layers:
	-	`sha256:787453bd83dce9d473689f5e983cfc99224f335f52dda1d16a0e5b0302d0f106`  
		Last Modified: Fri, 14 Feb 2025 23:04:37 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:243dcf0d023243a3b61aee8cb2b205b8fe61fc470d82257934575de8a39dcbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4241711a55ea959adb9faab82cba6408126c91cbec6d0af49161185a7031a78a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19710bb16bad23e16e1942366ab47dc67214cc321581fe20fa6c6ff243be2f`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66da5915b0a972b3b239c655a0797a199a02875109463ca9231c3c764542ebec`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e673af941f44b5da1cc7a57b60bb8dc744fb13be7bc3f249e2bffc928309186`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 81.7 KB (81660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f14c2ace1cb5e92040b8c20569aa9bc1f844aa0a668c66c2e9f43b1d1e71d3`  
		Last Modified: Fri, 14 Feb 2025 21:48:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ed75a52b489ce3cd4cc2e7a2f1c304b60aca0c041bdbc91901221011420dc`  
		Last Modified: Fri, 14 Feb 2025 21:48:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c53f275713194c826f486ee2d8eaac5d420edc72a311fa688ae6e01b45c058c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aa7c5afef13f34cc7da917449cd3b867e0efd586073777180b4f3322da556d`

```dockerfile
```

-	Layers:
	-	`sha256:f944c77504e84bfc3b670136a0525be52ff36579d52cf1bdc60500ce40e8cd2b`  
		Last Modified: Fri, 14 Feb 2025 23:04:49 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965d6330c884c6fff95b9c9614e372105c03df6e0066d24b9719318d47c7a4fd`  
		Last Modified: Fri, 14 Feb 2025 23:04:49 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47f6dfb20be478dce9979b1e2494b93143aa488741abf7dc66ba6f515e197d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f508cb0494d2702e3a13db5d6fc2fd1ca41256c5959e0c4652e04994a249388a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9ace35db34c3304a810302430fb8aef69b65f583bd5e243d327da73e37c2a`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714b728344222c6dfa8f49bd713be1cc1d83e747cab7f88cfaac3caef9ebe58`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a90c58f039279dd810920bc66f47f0c176890374bc494740bfa97ecbfa53767`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 100.6 KB (100551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec4dd7aa4832397a2e91d629904b2a48c8298de7db9365c04d33ebbf1bedc`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26adf19273ff38a41503b067a8d1c5a35d4048e2291780e1ffa91def36425f6a`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b00591e00a263982885b0bee54a5d7c27ebcf5249fdaa334c51fc223467aabf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bf2a0d811c39c7759e43d4257b01711ffdf36fa3dceffc397887cc7f8fa9d0`

```dockerfile
```

-	Layers:
	-	`sha256:c19f26a228bd4be6de3aa9d8196866405d54f8bc38d014c8f26254efe16ae04e`  
		Last Modified: Fri, 14 Feb 2025 23:04:40 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a1704deb4400e22af6abe356817cdee187689b0cba34988ce227508adfd78f`  
		Last Modified: Fri, 14 Feb 2025 23:04:40 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:61b83f6f4da433231db95db1a13fe86dbe85aaecde12dcb9a669f0b0ed0b6e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea95baf750c2a2749ec794c8238c510e5792dc8857ed4a3645d071f394823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de02b79b34b2bc491f8c7e8607233cc124ed19295cf456e64382e5afc72fbd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1d235c70003f61e0de885229553d72517e82d7f45df6d561b480b2cd9c5fc`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a0453a1d3c0248fee96f306a8ede9aa3d7f2dd02652a8dbdff1b0d8c9438b`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 120.1 KB (120130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e021c9b7ed20e7390deef74c89a7a5540f6309865137308f9a80ac607be260f`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872beb154170ecfc36e7b32d8019cfc1e29a60d26d251929d28131277a7fd0c`  
		Last Modified: Fri, 14 Feb 2025 19:11:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4c3f4670bd80d3c0136a64e6f27ff285948a413faee904ef1c460b8f51d4e516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5f2d723a731a066cf77f9a59824e65134fef732e62678056b932016e17282`

```dockerfile
```

-	Layers:
	-	`sha256:b1e174fd16318b9fb1190150ba833822f30825a45606ea9af9ec1723ce03867c`  
		Last Modified: Fri, 14 Feb 2025 23:04:42 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e4a7deb35e498340a41c762c8316785005a9ab4e93a2ab0a677fc623e721fd`  
		Last Modified: Fri, 14 Feb 2025 23:04:42 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:0763e833f3d2e767ad7c1ab64d3a1778d9543cffbe2731d7f8c40bee27d44a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cde70893ef4a0b94f4624b6bd8ea6a51522d65faf50b2646cac866d386dafe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ff6ba800883c9495b3d17b7735935035a83bdb153e380d5f5f6c80c3573c5`  
		Last Modified: Sat, 15 Feb 2025 09:24:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb59aefcf51d96da7771cb0671fa43ebe8e636326ce4db947ff446ea9b4eaa`  
		Last Modified: Sat, 15 Feb 2025 09:24:34 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b657e1255fd2cfb228ed06e75846652368ff0d80307f8b278c3db5e5558f4f64`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 112.6 KB (112646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de73da0d337b9f7fd4e60cf9b67d3592f9e6f6f539421800b167a2735f1bdb`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ad280a5133fac353984bead0c9962cf3a9c94714d7806a61832de902c8e929`  
		Last Modified: Sat, 15 Feb 2025 09:24:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:522f73a6a1f1e955300602615eb9a993897959108be79c09d235f1db5e488940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95185cb2bad6bef09c576b8e4d9d0bf6563783c294a92e69f28b758029f2ac0`

```dockerfile
```

-	Layers:
	-	`sha256:eb306f89b50101c069df46fb92b19620767f2503887c596aedfc415f347a4246`  
		Last Modified: Fri, 14 Feb 2025 23:04:43 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c821af9afc609e7780dcfb284627dd581cbede4a66c24cc04b41f590c6244531`  
		Last Modified: Fri, 14 Feb 2025 23:04:43 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
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
		Last Modified: Fri, 14 Feb 2025 23:04:44 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Fri, 14 Feb 2025 23:04:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:de25b12e766fe57e24177257227c53d5a27fc1a3ca4abe48e8bc60e0351bdaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb095475057abb702522c9d705013168c8522d986f39b9047739ee6efe16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a28161d111a002ad388fefdd709f7bb67cb61071bfdfa7960202816d14c2e2`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30984a12769648824acad7e1386b7ba7193bf81929e37f44ce5f3c04f82acc6`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5b85eee8dde04ba3dbc50eb3b644d79d18255b1eb4dfa5c888403b0ad97cc`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.9 KB (96918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860fa829f189bb5e960d5036162d15a1aac72e9ce8bed6c40b68549752c2199`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb23aa9487acbddced4252bb38b3510de48d049a3a347fcfb6b24f40c9ff730`  
		Last Modified: Fri, 14 Feb 2025 22:26:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2065dca98493b203898ab91ad7de40fb703351116ab3bfc12c9a52026ce6c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f932f07832d03eeec80862781aec2cb3efb7c48fadec873786bd1c8af939e6f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b919ae512d1430c2c7488ea884c9bc49e2ae21b5170043f2a370c90e9af6c60`  
		Last Modified: Fri, 14 Feb 2025 23:04:46 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf9c418603cd0c1fdf650dfd352e9ae11c6eec907de4024a31a994019249053`  
		Last Modified: Fri, 14 Feb 2025 23:04:46 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7196154f35d46a29a47883173fde58814cfb6bb853a3c4a61cca9430cf1f8159`  
		Last Modified: Wed, 05 Feb 2025 05:01:35 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd3a971ecf92f9d804a86b505518d4c7b4542035f10e32e0b0c1482acdb10b`  
		Last Modified: Wed, 05 Feb 2025 05:01:35 GMT  
		Size: 2.4 MB (2401342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf2c3578328d143a0c13eac4322d3a7ba1c09d0bb431e3fb8bccb93fac7409`  
		Last Modified: Tue, 04 Feb 2025 21:21:10 GMT  
		Size: 6.5 MB (6482493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c051f65857ae1a80b319d09976092265d695e37fb3b0c69fcf014ec2643d7`  
		Last Modified: Tue, 04 Feb 2025 21:21:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7250acc401675038e92dc4a884eee09833a19e8adba51f183326d29fcc2ca6`  
		Last Modified: Tue, 04 Feb 2025 21:21:09 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:45 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:49 GMT  
		Size: 5.1 MB (5146798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4af1d5f9bc51aca0b2d09e04074a8f703930c4176b241a50d5ff3492ed47ce`  
		Last Modified: Tue, 04 Feb 2025 08:02:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddabd99982fc01efcad0872592b12613c3b224baeb5ee91a78f4dbf692df1843`  
		Last Modified: Mon, 10 Feb 2025 00:47:49 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:47:55 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:01:17 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d40b8c33eed4efe5d43b21f211ccc96a002e6246f8b80e0e6f53f45a5c1334`  
		Last Modified: Mon, 10 Feb 2025 00:47:58 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f95294c83140a5f312fe0e0f3673b125c4718f4c4f531b3d58735aec00054b`  
		Last Modified: Tue, 04 Feb 2025 10:26:46 GMT  
		Size: 1.9 MB (1855579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36310be6ec666453ebf3cbf37d05cda567f1a1a76d531826880d258eba1676e4`  
		Last Modified: Mon, 10 Feb 2025 00:47:58 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:02 GMT  
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
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445785d885b1d4f4c62b22f763a4c23c5ef61dbcf8561b1f373f1122a157a32`  
		Last Modified: Wed, 05 Feb 2025 05:01:55 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e83c554a066c3f065b78b3307f98c54d4a3753271ce9398dcfb644a034658f`  
		Last Modified: Thu, 06 Feb 2025 05:16:17 GMT  
		Size: 2.2 MB (2247024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb79cb22695e7006611aaa6075a06126c1e46b6ec26a36bc59b2024e0692bb0`  
		Last Modified: Wed, 05 Feb 2025 05:05:08 GMT  
		Size: 5.5 MB (5491103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5f8d83d3803bc3372d3b2f901b9a579d0fe0892f5c55c7ffbcb4841f2509f`  
		Last Modified: Thu, 06 Feb 2025 05:16:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786f9a23b172afb3253a266af44a47a83cf5676a8b5fca783047e454090874f`  
		Last Modified: Wed, 05 Feb 2025 05:05:09 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:10 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a084f64ea6359821d9e6154f483978b063d4a671e0f59b1c9ed8b46ddb71f34`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b626f23d4ddc2323109743108c51c43a1fe05d501d0e7ded9368531db9ab7`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 2.4 MB (2398651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d27cbe14fcb4784bdf925fe2c6365bc3781a5667e0f64765c11702c029adab`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 6.0 MB (5956440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f9893150c1f1ac3dbda70997a910e68f713cbbbf84707c63383aa657bef3a2`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1739d36dcea86126749ade8e41d5e26216a42e18cce7c574440f9a6dc9541`  
		Last Modified: Mon, 10 Feb 2025 00:48:13 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:18 GMT  
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
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e2b18cfa28e78209d84a30bbacfa4539a85ee636689c58538621e572a4133b`  
		Last Modified: Wed, 05 Feb 2025 08:46:19 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d49f8446481472986048351b40e96fcad9c44128630158e4319ae5b69b2feca`  
		Last Modified: Mon, 10 Feb 2025 00:48:21 GMT  
		Size: 1.8 MB (1841114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0200fc9cacb2091aa304f8f172882d407f93a42a059f02ffc2ae0acaf682671`  
		Last Modified: Tue, 04 Feb 2025 19:23:38 GMT  
		Size: 5.8 MB (5813078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e2152b44d1116d5c1168680113e8fdd466ebcc7ee99c07fdfe1b3fbf39ba7e`  
		Last Modified: Mon, 10 Feb 2025 00:48:21 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:25 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaa4db2f41f33b473ee9e3d23526c2a5c3d06e4c63d975f8c329650781bfc50`  
		Last Modified: Tue, 04 Feb 2025 07:09:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d9aa243ee14d1187269f15a51bdd0121c76f084de8c950caf576d98b70e463`  
		Last Modified: Mon, 10 Feb 2025 00:48:29 GMT  
		Size: 2.6 MB (2582094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb78a29a1de352d83b7220b0199eb455f02534bd728d801150686e7e720a273`  
		Last Modified: Mon, 10 Feb 2025 00:48:29 GMT  
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
		Last Modified: Wed, 05 Feb 2025 08:46:22 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d5bc74f88a190910aebb2f129af625cf7b0d44d488bf251a42bd4bda622586`  
		Last Modified: Wed, 05 Feb 2025 08:46:22 GMT  
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
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a6e7d0775375fc3d1e148728013c288c159edf09d7f89268dbd2b94adb02e`  
		Last Modified: Mon, 10 Feb 2025 00:48:36 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:36 GMT  
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
		Last Modified: Mon, 10 Feb 2025 00:48:41 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
