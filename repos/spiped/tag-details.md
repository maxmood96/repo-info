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
$ docker pull spiped@sha256:75913f840d9a5ad3176ed693a6913324812495de158cc45fe72eb7b3c3cfea07
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
$ docker pull spiped@sha256:e0ab6e15a69a394c24e27e4d0e6b01aecdb4276780da735359598a8e7d610065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36827205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f559144e209b38285c9ec2149b96cf8756638f8f6662f714c92430305327b301`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:41:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 29 Dec 2025 23:41:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 29 Dec 2025 23:41:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
VOLUME [/spiped]
# Mon, 29 Dec 2025 23:41:58 GMT
WORKDIR /spiped
# Mon, 29 Dec 2025 23:41:58 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:41:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61114f1a7738d806984fd07548daac6fa1d09d6d1423c07542a8c6aab32b4a0a`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5fb473085a4a935991d9ec63fef7cd3976104ef825622bbddf5484eac405d5`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be147d212d4d67ff160c1229aaadd29b1fd86bc10fe931f17e53f3712d6386a7`  
		Last Modified: Mon, 29 Dec 2025 23:42:12 GMT  
		Size: 7.0 MB (7048306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9588de47f007973e38b96f1d3b803cfc9af343a24f74e0f204f1e1b7cb01f064`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424b48fe70f9ea781b6efbe29557a1ed90ee9a6a28396eb77dac3c7f2e6d68`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:997fdcb5c86c9fb49e7f972e7cd5aa5910c3c8ae5fa53d17cf5802afc2f9ea84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9efb54159f0b55ae1a044da27f4fbe33c623264c14eaae376a6fa71598aa35`

```dockerfile
```

-	Layers:
	-	`sha256:fee02ddcbce0920a76b6f684f83bc056025b9d0d6ae31ca8009bbc5e8149bacc`  
		Last Modified: Tue, 30 Dec 2025 02:05:22 GMT  
		Size: 3.6 MB (3626126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa7911ea504c36133be4385ba95ccc8f549954416a8bc4eff7c5945e617fb4ce`  
		Last Modified: Tue, 30 Dec 2025 02:05:22 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:91b17bfed43cd4cad49c799ca272fedc1a1be14ab28405b63b34a2d8136a7be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33736059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a04c8fd9616a5e22d4dc9f05c1bcc9fea99c18e540ee42c74d2b6afd7898ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:28:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 30 Dec 2025 00:28:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 30 Dec 2025 00:28:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
VOLUME [/spiped]
# Tue, 30 Dec 2025 00:28:46 GMT
WORKDIR /spiped
# Tue, 30 Dec 2025 00:28:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:28:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0193512c6cf65ee9280aa94d68551d1cc99c9945782505a191176a31c40d467`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fcaaf3a6edd0b5fcd46b535cf395e44246af04d83a8749b20c578b804168cf`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968bb20d69c66cb7c0cb819c0842fc86379cb8ae65498f9a43822e2f7f23aa93`  
		Last Modified: Tue, 30 Dec 2025 00:29:04 GMT  
		Size: 5.8 MB (5789542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62430768fd1ff023ecd14eb2f6206cece7aed822f75d39814a94952935f2821`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61f8bab7324653dff9134255853c0eccbdfe3a0309cfbb8aa3d9c6dadfec94c`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:d32b61812ab8572daeabe6b7d9339d20bda55b5c76ba345ccdbf26d60b2dea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9c3958f2f7d8b4eb3b44337db951c0b1bb9e7714990c189010da1c7cdda670`

```dockerfile
```

-	Layers:
	-	`sha256:b30cb319d8121e7bcec7440216b934792921bb31c85e23dd32186b4dee105f77`  
		Last Modified: Tue, 30 Dec 2025 02:05:26 GMT  
		Size: 3.6 MB (3619120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f381644189fbffa088bbbdaba9a72f12a1d42e7e3bb039b1e1e29567fe11d4`  
		Last Modified: Tue, 30 Dec 2025 02:05:27 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:5200083bb38fef4bc7574dc55308b9703006fc9e1d217ddd4bd5bf54ed67e743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31797343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0a36ed22c5498f85b2048a95288b32294a5e7799b1f695ad69ad84c1fc38fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:59:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 09 Dec 2025 00:00:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 09 Dec 2025 00:00:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
VOLUME [/spiped]
# Tue, 09 Dec 2025 00:00:24 GMT
WORKDIR /spiped
# Tue, 09 Dec 2025 00:00:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:00:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fad81476600f360ac6aac53f19096a951b0aa17f7ebcd0af40144c002440746`  
		Last Modified: Tue, 09 Dec 2025 00:00:52 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f2442e1fcfc806776dc7cc0a02758ee841ae774e5dbcf6ce2ec3dd37792d11`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f9951c3bdb9b2566c5e3eac7d8ace68c15bac473cf4448d9246318a43dc0c`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 5.6 MB (5584966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6535c74f54d0fcd5cedd525de4724882f3c4f3e0a291c4cc20e3a4b0a11d4b`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99cda306c96e1344b0f7665b2fd449b3d289dde46535217c355c22dd7cbe82`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:0b1988ed27e75d85e9b3a84e466787ec81bd5a0c97ec53fbd660969aef5f82ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8423f58edd5d3f4981c6adc179173cc30386b1776dae470179d6de1b1568ea`

```dockerfile
```

-	Layers:
	-	`sha256:cb88ad9317068008ece0955b69ab1bf4f1a10fcf8dbb9bd62372819f2f3f7083`  
		Last Modified: Tue, 09 Dec 2025 02:04:58 GMT  
		Size: 3.6 MB (3618241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320acdb3e60bc6bbac56773063a044e47a888ffe3806778cb998cb3739fc5407`  
		Last Modified: Tue, 09 Dec 2025 02:04:59 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d82f0af2b0dc3d8623c9659de5ce444393a5e7bed0896c1a4ff3e20a227339fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36373065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53b5b0e8df0b62268fdc4f0802dfc325c825eb289fa5cd38935f34b1aae63c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:43:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 29 Dec 2025 23:43:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 29 Dec 2025 23:43:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
VOLUME [/spiped]
# Mon, 29 Dec 2025 23:43:54 GMT
WORKDIR /spiped
# Mon, 29 Dec 2025 23:43:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:43:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe15f2c60d175e4fa4c514a3227917d573101d643ffe1f27c9b508c9102ad06`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142436ef7698bd0a0c276cedfaa7633c5b4b62afeaf6a43e68ebee211473b2d`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404bca06018f6b84d5500027da70a274572a04fb849a57ce3bf3f89aa06e769`  
		Last Modified: Mon, 29 Dec 2025 23:44:09 GMT  
		Size: 6.2 MB (6232063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c907968613021498b890cfee8c513c0a9a9f5cb8a072bdaa70682ee6389c90ab`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c188712597b5ba1b163b85abafe3515c309b0957d5f87b1a9b676c33982eea9d`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:4cc1b134021e6d459ebabe835e3ac5db7c257ae4ab4812d53e8614e331345f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89939c1909ed3ceae74c71dd1da09eb64efc62e16c2d31f2eb2e9d2061ae87a9`

```dockerfile
```

-	Layers:
	-	`sha256:ed68b1bfcd292069710110a67f93b2173eec3633332fc8e34e6206f453260e15`  
		Last Modified: Tue, 30 Dec 2025 02:05:34 GMT  
		Size: 3.6 MB (3621162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910cca8c7ce8141f416e527c593be9623ac5f5821cdca2e87064f80cc573afdd`  
		Last Modified: Tue, 30 Dec 2025 02:05:35 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:8187379c6228ce202ff5d4c94456c531f2a98b62f8626197b2394d09fca55436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37737953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe80eb9fc3c8d0bcf1f923f563cfa1a14973030eb8371a9e4e820a3e3430d381`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:12:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 08 Dec 2025 23:13:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 08 Dec 2025 23:13:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
VOLUME [/spiped]
# Mon, 08 Dec 2025 23:13:24 GMT
WORKDIR /spiped
# Mon, 08 Dec 2025 23:13:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:13:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6c3163818b6fb615e6724e571c7dfbf1db92a79858e8cf88fb9731ec063be4`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7614683e35746f5661794b7d905f74dea0dfa5813a6bbe1c58e043be59d2421`  
		Last Modified: Mon, 08 Dec 2025 23:13:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e834535a7b7e92e9a99b0ce53bd665892758fa2f8408b3be2621110510df16`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 6.4 MB (6442516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306cf8704e113ac01607bec5eca6e0302bad834d263c2d1e3202126bf76aa1b`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f985353893e48ccfac69c9c13935e5df63ecd6ce5a920aa8f8810ceeb9c1036`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:01b5afdfe9c701d9cd305b5bb27f2b31dfac4d340f82a9475457c2a5d6faff14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d65e242d82cb0bb5c1663803b1f84dc1aaaf60fe000d9d42b125df3c0c22a2`

```dockerfile
```

-	Layers:
	-	`sha256:2775ed98d9b7d6f1fd3db9b0e3ee54ce228d5e9da4576c5a05e599d55d577645`  
		Last Modified: Tue, 09 Dec 2025 02:05:09 GMT  
		Size: 3.6 MB (3620255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600c7b92499a400c0d0bed536e0c166b1c3403d3041303fb7f254d7197f8bb09`  
		Last Modified: Tue, 09 Dec 2025 02:05:10 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:231a1d43e5e776f583fc38bc47ed55ba2eedfa62290304d48a987615a462aaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40439563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d29fd0db4325b6621cff6f832dd227adcd56d8e6336fe24290042f35406c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 02:05:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 09 Dec 2025 02:05:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:06:11 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 09 Dec 2025 02:06:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 02:06:11 GMT
VOLUME [/spiped]
# Tue, 09 Dec 2025 02:06:12 GMT
WORKDIR /spiped
# Tue, 09 Dec 2025 02:06:13 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:06:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 02:06:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503a46c9fbb88b7b350edb4625885bb779e4f7be07b3082f24d86e36d3057986`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378ab413e123c64fee3801629972f0990f196b621ad4bcf3159eb489575eca96`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c5f2246f4178f1cd407178217dc9a96dbbc4d3c1d1c52aa8721328e9f88e3`  
		Last Modified: Tue, 09 Dec 2025 02:06:39 GMT  
		Size: 6.8 MB (6840311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36f671078cedaf1573055837372fa65c44c7f585cf3c2fc884f54bea5627456`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a5b467385c16a82f5fec93ac662bd467bd3fbecc909fdd8e5dbc0aa4e8ca8f`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:f027b13300b43abae6d2b151f755d9a0a5465e2ca3a5d03c6409f8167af98fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57accfcfec38bd8780719bd67c6bcaa96ea12709c98f4323d55c13426b386c9`

```dockerfile
```

-	Layers:
	-	`sha256:7ec26c40291155e915b5193c1a2408314af2d40f7c81eed8ac6cc4fd251d98d8`  
		Last Modified: Tue, 09 Dec 2025 05:04:51 GMT  
		Size: 3.6 MB (3621863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8e849d88a142868762c6f30924b1afdb7e60a293be00ea74339e88ac9b7c1e`  
		Last Modified: Tue, 09 Dec 2025 05:04:52 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:08978bf28bc0d7ac2e6f47f6e80882b98e0a6a0d6b5ea62730e32f6804801758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37634024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0795418aa4256b921cece24104f61c90d644699fe70f3ffad97e4461254155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 04:08:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Dec 2025 04:08:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 04:11:43 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Dec 2025 04:11:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Dec 2025 04:11:43 GMT
VOLUME [/spiped]
# Thu, 11 Dec 2025 04:11:44 GMT
WORKDIR /spiped
# Thu, 11 Dec 2025 04:11:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 04:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Dec 2025 04:11:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc6ae66f0155b9004dd1f3434d971d0493912ca5ca8e79b6232dcd72464f8ef`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f11fcb3db20b488e3ab58b9d2a5b4dda32f134f0de49f739f1ed5ed6cd3a3`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f91465220a957b207e2529e21cc60cd21ee499f509a66f6fe9d300d562cb1`  
		Last Modified: Thu, 11 Dec 2025 04:13:08 GMT  
		Size: 9.4 MB (9358512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b5259104cf9044c85e9d3b7ae514ce666bb643243f461992ba90a076a0053`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4d228d8e993bd097e714e4d8df72c5544d9cbef509190c3c6f90ad68f4a0fb`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:9e4f64518d61d958491edbfbbf4ad29ea6dfbb803d3ea587c406624c5c2cd30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f825073b9f2d6c7f7334a1d559a30c82e03daa62d80e8cbd028725de18755f0`

```dockerfile
```

-	Layers:
	-	`sha256:730a014b2cbdfd270e520864e6c838e014a8ae2efe5cfe156aba088532f28422`  
		Last Modified: Thu, 11 Dec 2025 08:04:45 GMT  
		Size: 3.6 MB (3613269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e953648960d7c96a844ee9c357d7ba606100a2ca5eab2c925b6eb365518ace8`  
		Last Modified: Thu, 11 Dec 2025 08:04:45 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:fd7f0e30d0f4fa7b0a04170b6350d2b17cfe65ae8784e52a6b7749ec25fd596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35958428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35393eb489a51e91bba712273d44ca8a8c9cc3b845e6d2cffb9d292d4e8eb1bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:37:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 30 Dec 2025 00:37:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 30 Dec 2025 00:38:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
VOLUME [/spiped]
# Tue, 30 Dec 2025 00:38:08 GMT
WORKDIR /spiped
# Tue, 30 Dec 2025 00:38:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:38:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4598f0fe0ec5b6dbe64aac084c86c1ef64cc495e9e0aa59e95e5b5ba2524f7`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91620759fafc1d1c5cb4f18a00f4cb4377652efe7920db9a10895cd0e7e94d68`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2642203b10576c7b7dd707aa9cf88bbbce7471eaa4ea825439abae85cf07212`  
		Last Modified: Tue, 30 Dec 2025 00:38:25 GMT  
		Size: 6.1 MB (6121643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96010cfacda4d93f71ee023511910b20f8b40d4e1e3f54b810a32c0ca838601`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae779a5c1cfac43eca3758b75ace95e6d1d9e6c5723564d11b89c064bfdd008`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:beb09fde5a4716220058166de08ce6f82421330fea3005976df36f2b78bbe59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc76f41916d041fcbdd4277500e819c763801a448c2534be7abf4f316cf1da`

```dockerfile
```

-	Layers:
	-	`sha256:6ca6f58385becddea4ed57434f2dec40641e09de615d06202c7ebd28bffc8f1c`  
		Last Modified: Tue, 30 Dec 2025 02:05:51 GMT  
		Size: 3.6 MB (3618489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050a745f90b1400d1728907caaf1cc2268e61f30e6442658a879615c33a092e9`  
		Last Modified: Tue, 30 Dec 2025 02:05:51 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Tue, 16 Dec 2025 23:20:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Tue, 16 Dec 2025 23:20:31 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Tue, 09 Dec 2025 15:14:13 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Tue, 16 Dec 2025 23:20:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Tue, 09 Dec 2025 15:14:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Tue, 16 Dec 2025 23:20:43 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Tue, 16 Dec 2025 23:20:46 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Tue, 16 Dec 2025 23:20:49 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Tue, 16 Dec 2025 23:20:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Tue, 16 Dec 2025 23:20:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Wed, 08 Oct 2025 22:09:24 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Tue, 16 Dec 2025 23:20:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Tue, 16 Dec 2025 23:21:02 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Tue, 16 Dec 2025 23:21:05 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Tue, 16 Dec 2025 23:21:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Tue, 16 Dec 2025 23:21:12 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Tue, 16 Dec 2025 23:21:18 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Tue, 16 Dec 2025 23:21:20 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Tue, 16 Dec 2025 23:21:23 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Tue, 16 Dec 2025 23:21:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Tue, 16 Dec 2025 23:21:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Tue, 16 Dec 2025 23:21:35 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Tue, 16 Dec 2025 23:21:38 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Tue, 16 Dec 2025 23:21:41 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Tue, 16 Dec 2025 23:21:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Tue, 16 Dec 2025 23:21:47 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Wed, 08 Oct 2025 21:39:30 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Wed, 08 Oct 2025 21:39:30 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Tue, 16 Dec 2025 23:21:52 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Tue, 16 Dec 2025 23:21:55 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Tue, 16 Dec 2025 23:21:58 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Tue, 16 Dec 2025 23:22:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Tue, 16 Dec 2025 23:22:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 03:32:04 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 03:32:04 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Tue, 16 Dec 2025 23:22:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Tue, 16 Dec 2025 23:22:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Tue, 16 Dec 2025 23:22:18 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Tue, 16 Dec 2025 23:22:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Tue, 16 Dec 2025 23:22:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 20:50:03 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 20:50:03 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Tue, 16 Dec 2025 23:22:30 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Tue, 16 Dec 2025 23:22:32 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Tue, 16 Dec 2025 23:22:35 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Tue, 16 Dec 2025 23:22:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Tue, 16 Dec 2025 23:22:40 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 02:25:54 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 02:25:54 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:75913f840d9a5ad3176ed693a6913324812495de158cc45fe72eb7b3c3cfea07
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
$ docker pull spiped@sha256:e0ab6e15a69a394c24e27e4d0e6b01aecdb4276780da735359598a8e7d610065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36827205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f559144e209b38285c9ec2149b96cf8756638f8f6662f714c92430305327b301`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:41:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 29 Dec 2025 23:41:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 29 Dec 2025 23:41:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
VOLUME [/spiped]
# Mon, 29 Dec 2025 23:41:58 GMT
WORKDIR /spiped
# Mon, 29 Dec 2025 23:41:58 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:41:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61114f1a7738d806984fd07548daac6fa1d09d6d1423c07542a8c6aab32b4a0a`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5fb473085a4a935991d9ec63fef7cd3976104ef825622bbddf5484eac405d5`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be147d212d4d67ff160c1229aaadd29b1fd86bc10fe931f17e53f3712d6386a7`  
		Last Modified: Mon, 29 Dec 2025 23:42:12 GMT  
		Size: 7.0 MB (7048306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9588de47f007973e38b96f1d3b803cfc9af343a24f74e0f204f1e1b7cb01f064`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424b48fe70f9ea781b6efbe29557a1ed90ee9a6a28396eb77dac3c7f2e6d68`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:997fdcb5c86c9fb49e7f972e7cd5aa5910c3c8ae5fa53d17cf5802afc2f9ea84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9efb54159f0b55ae1a044da27f4fbe33c623264c14eaae376a6fa71598aa35`

```dockerfile
```

-	Layers:
	-	`sha256:fee02ddcbce0920a76b6f684f83bc056025b9d0d6ae31ca8009bbc5e8149bacc`  
		Last Modified: Tue, 30 Dec 2025 02:05:22 GMT  
		Size: 3.6 MB (3626126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa7911ea504c36133be4385ba95ccc8f549954416a8bc4eff7c5945e617fb4ce`  
		Last Modified: Tue, 30 Dec 2025 02:05:22 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:91b17bfed43cd4cad49c799ca272fedc1a1be14ab28405b63b34a2d8136a7be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33736059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a04c8fd9616a5e22d4dc9f05c1bcc9fea99c18e540ee42c74d2b6afd7898ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:28:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 30 Dec 2025 00:28:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 30 Dec 2025 00:28:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
VOLUME [/spiped]
# Tue, 30 Dec 2025 00:28:46 GMT
WORKDIR /spiped
# Tue, 30 Dec 2025 00:28:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:28:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0193512c6cf65ee9280aa94d68551d1cc99c9945782505a191176a31c40d467`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fcaaf3a6edd0b5fcd46b535cf395e44246af04d83a8749b20c578b804168cf`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968bb20d69c66cb7c0cb819c0842fc86379cb8ae65498f9a43822e2f7f23aa93`  
		Last Modified: Tue, 30 Dec 2025 00:29:04 GMT  
		Size: 5.8 MB (5789542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62430768fd1ff023ecd14eb2f6206cece7aed822f75d39814a94952935f2821`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61f8bab7324653dff9134255853c0eccbdfe3a0309cfbb8aa3d9c6dadfec94c`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:d32b61812ab8572daeabe6b7d9339d20bda55b5c76ba345ccdbf26d60b2dea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9c3958f2f7d8b4eb3b44337db951c0b1bb9e7714990c189010da1c7cdda670`

```dockerfile
```

-	Layers:
	-	`sha256:b30cb319d8121e7bcec7440216b934792921bb31c85e23dd32186b4dee105f77`  
		Last Modified: Tue, 30 Dec 2025 02:05:26 GMT  
		Size: 3.6 MB (3619120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f381644189fbffa088bbbdaba9a72f12a1d42e7e3bb039b1e1e29567fe11d4`  
		Last Modified: Tue, 30 Dec 2025 02:05:27 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:5200083bb38fef4bc7574dc55308b9703006fc9e1d217ddd4bd5bf54ed67e743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31797343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0a36ed22c5498f85b2048a95288b32294a5e7799b1f695ad69ad84c1fc38fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:59:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 09 Dec 2025 00:00:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 09 Dec 2025 00:00:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
VOLUME [/spiped]
# Tue, 09 Dec 2025 00:00:24 GMT
WORKDIR /spiped
# Tue, 09 Dec 2025 00:00:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:00:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fad81476600f360ac6aac53f19096a951b0aa17f7ebcd0af40144c002440746`  
		Last Modified: Tue, 09 Dec 2025 00:00:52 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f2442e1fcfc806776dc7cc0a02758ee841ae774e5dbcf6ce2ec3dd37792d11`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f9951c3bdb9b2566c5e3eac7d8ace68c15bac473cf4448d9246318a43dc0c`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 5.6 MB (5584966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6535c74f54d0fcd5cedd525de4724882f3c4f3e0a291c4cc20e3a4b0a11d4b`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99cda306c96e1344b0f7665b2fd449b3d289dde46535217c355c22dd7cbe82`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:0b1988ed27e75d85e9b3a84e466787ec81bd5a0c97ec53fbd660969aef5f82ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8423f58edd5d3f4981c6adc179173cc30386b1776dae470179d6de1b1568ea`

```dockerfile
```

-	Layers:
	-	`sha256:cb88ad9317068008ece0955b69ab1bf4f1a10fcf8dbb9bd62372819f2f3f7083`  
		Last Modified: Tue, 09 Dec 2025 02:04:58 GMT  
		Size: 3.6 MB (3618241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320acdb3e60bc6bbac56773063a044e47a888ffe3806778cb998cb3739fc5407`  
		Last Modified: Tue, 09 Dec 2025 02:04:59 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d82f0af2b0dc3d8623c9659de5ce444393a5e7bed0896c1a4ff3e20a227339fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36373065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53b5b0e8df0b62268fdc4f0802dfc325c825eb289fa5cd38935f34b1aae63c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:43:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 29 Dec 2025 23:43:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 29 Dec 2025 23:43:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
VOLUME [/spiped]
# Mon, 29 Dec 2025 23:43:54 GMT
WORKDIR /spiped
# Mon, 29 Dec 2025 23:43:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:43:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe15f2c60d175e4fa4c514a3227917d573101d643ffe1f27c9b508c9102ad06`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142436ef7698bd0a0c276cedfaa7633c5b4b62afeaf6a43e68ebee211473b2d`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404bca06018f6b84d5500027da70a274572a04fb849a57ce3bf3f89aa06e769`  
		Last Modified: Mon, 29 Dec 2025 23:44:09 GMT  
		Size: 6.2 MB (6232063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c907968613021498b890cfee8c513c0a9a9f5cb8a072bdaa70682ee6389c90ab`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c188712597b5ba1b163b85abafe3515c309b0957d5f87b1a9b676c33982eea9d`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:4cc1b134021e6d459ebabe835e3ac5db7c257ae4ab4812d53e8614e331345f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89939c1909ed3ceae74c71dd1da09eb64efc62e16c2d31f2eb2e9d2061ae87a9`

```dockerfile
```

-	Layers:
	-	`sha256:ed68b1bfcd292069710110a67f93b2173eec3633332fc8e34e6206f453260e15`  
		Last Modified: Tue, 30 Dec 2025 02:05:34 GMT  
		Size: 3.6 MB (3621162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910cca8c7ce8141f416e527c593be9623ac5f5821cdca2e87064f80cc573afdd`  
		Last Modified: Tue, 30 Dec 2025 02:05:35 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:8187379c6228ce202ff5d4c94456c531f2a98b62f8626197b2394d09fca55436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37737953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe80eb9fc3c8d0bcf1f923f563cfa1a14973030eb8371a9e4e820a3e3430d381`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:12:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 08 Dec 2025 23:13:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 08 Dec 2025 23:13:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
VOLUME [/spiped]
# Mon, 08 Dec 2025 23:13:24 GMT
WORKDIR /spiped
# Mon, 08 Dec 2025 23:13:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:13:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6c3163818b6fb615e6724e571c7dfbf1db92a79858e8cf88fb9731ec063be4`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7614683e35746f5661794b7d905f74dea0dfa5813a6bbe1c58e043be59d2421`  
		Last Modified: Mon, 08 Dec 2025 23:13:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e834535a7b7e92e9a99b0ce53bd665892758fa2f8408b3be2621110510df16`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 6.4 MB (6442516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306cf8704e113ac01607bec5eca6e0302bad834d263c2d1e3202126bf76aa1b`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f985353893e48ccfac69c9c13935e5df63ecd6ce5a920aa8f8810ceeb9c1036`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:01b5afdfe9c701d9cd305b5bb27f2b31dfac4d340f82a9475457c2a5d6faff14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d65e242d82cb0bb5c1663803b1f84dc1aaaf60fe000d9d42b125df3c0c22a2`

```dockerfile
```

-	Layers:
	-	`sha256:2775ed98d9b7d6f1fd3db9b0e3ee54ce228d5e9da4576c5a05e599d55d577645`  
		Last Modified: Tue, 09 Dec 2025 02:05:09 GMT  
		Size: 3.6 MB (3620255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600c7b92499a400c0d0bed536e0c166b1c3403d3041303fb7f254d7197f8bb09`  
		Last Modified: Tue, 09 Dec 2025 02:05:10 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:231a1d43e5e776f583fc38bc47ed55ba2eedfa62290304d48a987615a462aaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40439563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d29fd0db4325b6621cff6f832dd227adcd56d8e6336fe24290042f35406c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 02:05:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 09 Dec 2025 02:05:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:06:11 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 09 Dec 2025 02:06:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 02:06:11 GMT
VOLUME [/spiped]
# Tue, 09 Dec 2025 02:06:12 GMT
WORKDIR /spiped
# Tue, 09 Dec 2025 02:06:13 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:06:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 02:06:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503a46c9fbb88b7b350edb4625885bb779e4f7be07b3082f24d86e36d3057986`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378ab413e123c64fee3801629972f0990f196b621ad4bcf3159eb489575eca96`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c5f2246f4178f1cd407178217dc9a96dbbc4d3c1d1c52aa8721328e9f88e3`  
		Last Modified: Tue, 09 Dec 2025 02:06:39 GMT  
		Size: 6.8 MB (6840311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36f671078cedaf1573055837372fa65c44c7f585cf3c2fc884f54bea5627456`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a5b467385c16a82f5fec93ac662bd467bd3fbecc909fdd8e5dbc0aa4e8ca8f`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:f027b13300b43abae6d2b151f755d9a0a5465e2ca3a5d03c6409f8167af98fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57accfcfec38bd8780719bd67c6bcaa96ea12709c98f4323d55c13426b386c9`

```dockerfile
```

-	Layers:
	-	`sha256:7ec26c40291155e915b5193c1a2408314af2d40f7c81eed8ac6cc4fd251d98d8`  
		Last Modified: Tue, 09 Dec 2025 05:04:51 GMT  
		Size: 3.6 MB (3621863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8e849d88a142868762c6f30924b1afdb7e60a293be00ea74339e88ac9b7c1e`  
		Last Modified: Tue, 09 Dec 2025 05:04:52 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:08978bf28bc0d7ac2e6f47f6e80882b98e0a6a0d6b5ea62730e32f6804801758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37634024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0795418aa4256b921cece24104f61c90d644699fe70f3ffad97e4461254155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 04:08:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Dec 2025 04:08:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 04:11:43 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Dec 2025 04:11:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Dec 2025 04:11:43 GMT
VOLUME [/spiped]
# Thu, 11 Dec 2025 04:11:44 GMT
WORKDIR /spiped
# Thu, 11 Dec 2025 04:11:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 04:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Dec 2025 04:11:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc6ae66f0155b9004dd1f3434d971d0493912ca5ca8e79b6232dcd72464f8ef`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f11fcb3db20b488e3ab58b9d2a5b4dda32f134f0de49f739f1ed5ed6cd3a3`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f91465220a957b207e2529e21cc60cd21ee499f509a66f6fe9d300d562cb1`  
		Last Modified: Thu, 11 Dec 2025 04:13:08 GMT  
		Size: 9.4 MB (9358512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b5259104cf9044c85e9d3b7ae514ce666bb643243f461992ba90a076a0053`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4d228d8e993bd097e714e4d8df72c5544d9cbef509190c3c6f90ad68f4a0fb`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:9e4f64518d61d958491edbfbbf4ad29ea6dfbb803d3ea587c406624c5c2cd30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f825073b9f2d6c7f7334a1d559a30c82e03daa62d80e8cbd028725de18755f0`

```dockerfile
```

-	Layers:
	-	`sha256:730a014b2cbdfd270e520864e6c838e014a8ae2efe5cfe156aba088532f28422`  
		Last Modified: Thu, 11 Dec 2025 08:04:45 GMT  
		Size: 3.6 MB (3613269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e953648960d7c96a844ee9c357d7ba606100a2ca5eab2c925b6eb365518ace8`  
		Last Modified: Thu, 11 Dec 2025 08:04:45 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:fd7f0e30d0f4fa7b0a04170b6350d2b17cfe65ae8784e52a6b7749ec25fd596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35958428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35393eb489a51e91bba712273d44ca8a8c9cc3b845e6d2cffb9d292d4e8eb1bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:37:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 30 Dec 2025 00:37:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 30 Dec 2025 00:38:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
VOLUME [/spiped]
# Tue, 30 Dec 2025 00:38:08 GMT
WORKDIR /spiped
# Tue, 30 Dec 2025 00:38:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:38:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4598f0fe0ec5b6dbe64aac084c86c1ef64cc495e9e0aa59e95e5b5ba2524f7`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91620759fafc1d1c5cb4f18a00f4cb4377652efe7920db9a10895cd0e7e94d68`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2642203b10576c7b7dd707aa9cf88bbbce7471eaa4ea825439abae85cf07212`  
		Last Modified: Tue, 30 Dec 2025 00:38:25 GMT  
		Size: 6.1 MB (6121643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96010cfacda4d93f71ee023511910b20f8b40d4e1e3f54b810a32c0ca838601`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae779a5c1cfac43eca3758b75ace95e6d1d9e6c5723564d11b89c064bfdd008`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:beb09fde5a4716220058166de08ce6f82421330fea3005976df36f2b78bbe59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc76f41916d041fcbdd4277500e819c763801a448c2534be7abf4f316cf1da`

```dockerfile
```

-	Layers:
	-	`sha256:6ca6f58385becddea4ed57434f2dec40641e09de615d06202c7ebd28bffc8f1c`  
		Last Modified: Tue, 30 Dec 2025 02:05:51 GMT  
		Size: 3.6 MB (3618489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050a745f90b1400d1728907caaf1cc2268e61f30e6442658a879615c33a092e9`  
		Last Modified: Tue, 30 Dec 2025 02:05:51 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Tue, 16 Dec 2025 23:20:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Tue, 16 Dec 2025 23:20:31 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Tue, 09 Dec 2025 15:14:13 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Tue, 16 Dec 2025 23:20:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Tue, 09 Dec 2025 15:14:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Tue, 16 Dec 2025 23:20:43 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Tue, 16 Dec 2025 23:20:46 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Tue, 16 Dec 2025 23:20:49 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Tue, 16 Dec 2025 23:20:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Tue, 16 Dec 2025 23:20:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Wed, 08 Oct 2025 22:09:24 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Tue, 16 Dec 2025 23:20:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Tue, 16 Dec 2025 23:21:02 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Tue, 16 Dec 2025 23:21:05 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Tue, 16 Dec 2025 23:21:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Tue, 16 Dec 2025 23:21:12 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Tue, 16 Dec 2025 23:21:18 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Tue, 16 Dec 2025 23:21:20 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Tue, 16 Dec 2025 23:21:23 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Tue, 16 Dec 2025 23:21:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Tue, 16 Dec 2025 23:21:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Tue, 16 Dec 2025 23:21:35 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Tue, 16 Dec 2025 23:21:38 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Tue, 16 Dec 2025 23:21:41 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Tue, 16 Dec 2025 23:21:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Tue, 16 Dec 2025 23:21:47 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Wed, 08 Oct 2025 21:39:30 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Wed, 08 Oct 2025 21:39:30 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Tue, 16 Dec 2025 23:21:52 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Tue, 16 Dec 2025 23:21:55 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Tue, 16 Dec 2025 23:21:58 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Tue, 16 Dec 2025 23:22:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Tue, 16 Dec 2025 23:22:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 03:32:04 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 03:32:04 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Tue, 16 Dec 2025 23:22:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Tue, 16 Dec 2025 23:22:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Tue, 16 Dec 2025 23:22:18 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Tue, 16 Dec 2025 23:22:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Tue, 16 Dec 2025 23:22:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 20:50:03 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 20:50:03 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Tue, 16 Dec 2025 23:22:30 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Tue, 16 Dec 2025 23:22:32 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Tue, 16 Dec 2025 23:22:35 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Tue, 16 Dec 2025 23:22:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Tue, 16 Dec 2025 23:22:40 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 02:25:54 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 02:25:54 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:75913f840d9a5ad3176ed693a6913324812495de158cc45fe72eb7b3c3cfea07
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
$ docker pull spiped@sha256:e0ab6e15a69a394c24e27e4d0e6b01aecdb4276780da735359598a8e7d610065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36827205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f559144e209b38285c9ec2149b96cf8756638f8f6662f714c92430305327b301`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:41:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 29 Dec 2025 23:41:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 29 Dec 2025 23:41:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
VOLUME [/spiped]
# Mon, 29 Dec 2025 23:41:58 GMT
WORKDIR /spiped
# Mon, 29 Dec 2025 23:41:58 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:41:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61114f1a7738d806984fd07548daac6fa1d09d6d1423c07542a8c6aab32b4a0a`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5fb473085a4a935991d9ec63fef7cd3976104ef825622bbddf5484eac405d5`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be147d212d4d67ff160c1229aaadd29b1fd86bc10fe931f17e53f3712d6386a7`  
		Last Modified: Mon, 29 Dec 2025 23:42:12 GMT  
		Size: 7.0 MB (7048306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9588de47f007973e38b96f1d3b803cfc9af343a24f74e0f204f1e1b7cb01f064`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424b48fe70f9ea781b6efbe29557a1ed90ee9a6a28396eb77dac3c7f2e6d68`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:997fdcb5c86c9fb49e7f972e7cd5aa5910c3c8ae5fa53d17cf5802afc2f9ea84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9efb54159f0b55ae1a044da27f4fbe33c623264c14eaae376a6fa71598aa35`

```dockerfile
```

-	Layers:
	-	`sha256:fee02ddcbce0920a76b6f684f83bc056025b9d0d6ae31ca8009bbc5e8149bacc`  
		Last Modified: Tue, 30 Dec 2025 02:05:22 GMT  
		Size: 3.6 MB (3626126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa7911ea504c36133be4385ba95ccc8f549954416a8bc4eff7c5945e617fb4ce`  
		Last Modified: Tue, 30 Dec 2025 02:05:22 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:91b17bfed43cd4cad49c799ca272fedc1a1be14ab28405b63b34a2d8136a7be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33736059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a04c8fd9616a5e22d4dc9f05c1bcc9fea99c18e540ee42c74d2b6afd7898ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:28:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 30 Dec 2025 00:28:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 30 Dec 2025 00:28:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
VOLUME [/spiped]
# Tue, 30 Dec 2025 00:28:46 GMT
WORKDIR /spiped
# Tue, 30 Dec 2025 00:28:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:28:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0193512c6cf65ee9280aa94d68551d1cc99c9945782505a191176a31c40d467`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fcaaf3a6edd0b5fcd46b535cf395e44246af04d83a8749b20c578b804168cf`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968bb20d69c66cb7c0cb819c0842fc86379cb8ae65498f9a43822e2f7f23aa93`  
		Last Modified: Tue, 30 Dec 2025 00:29:04 GMT  
		Size: 5.8 MB (5789542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62430768fd1ff023ecd14eb2f6206cece7aed822f75d39814a94952935f2821`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61f8bab7324653dff9134255853c0eccbdfe3a0309cfbb8aa3d9c6dadfec94c`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:d32b61812ab8572daeabe6b7d9339d20bda55b5c76ba345ccdbf26d60b2dea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9c3958f2f7d8b4eb3b44337db951c0b1bb9e7714990c189010da1c7cdda670`

```dockerfile
```

-	Layers:
	-	`sha256:b30cb319d8121e7bcec7440216b934792921bb31c85e23dd32186b4dee105f77`  
		Last Modified: Tue, 30 Dec 2025 02:05:26 GMT  
		Size: 3.6 MB (3619120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f381644189fbffa088bbbdaba9a72f12a1d42e7e3bb039b1e1e29567fe11d4`  
		Last Modified: Tue, 30 Dec 2025 02:05:27 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:5200083bb38fef4bc7574dc55308b9703006fc9e1d217ddd4bd5bf54ed67e743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31797343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0a36ed22c5498f85b2048a95288b32294a5e7799b1f695ad69ad84c1fc38fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:59:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 09 Dec 2025 00:00:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 09 Dec 2025 00:00:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
VOLUME [/spiped]
# Tue, 09 Dec 2025 00:00:24 GMT
WORKDIR /spiped
# Tue, 09 Dec 2025 00:00:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:00:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fad81476600f360ac6aac53f19096a951b0aa17f7ebcd0af40144c002440746`  
		Last Modified: Tue, 09 Dec 2025 00:00:52 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f2442e1fcfc806776dc7cc0a02758ee841ae774e5dbcf6ce2ec3dd37792d11`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f9951c3bdb9b2566c5e3eac7d8ace68c15bac473cf4448d9246318a43dc0c`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 5.6 MB (5584966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6535c74f54d0fcd5cedd525de4724882f3c4f3e0a291c4cc20e3a4b0a11d4b`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99cda306c96e1344b0f7665b2fd449b3d289dde46535217c355c22dd7cbe82`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:0b1988ed27e75d85e9b3a84e466787ec81bd5a0c97ec53fbd660969aef5f82ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8423f58edd5d3f4981c6adc179173cc30386b1776dae470179d6de1b1568ea`

```dockerfile
```

-	Layers:
	-	`sha256:cb88ad9317068008ece0955b69ab1bf4f1a10fcf8dbb9bd62372819f2f3f7083`  
		Last Modified: Tue, 09 Dec 2025 02:04:58 GMT  
		Size: 3.6 MB (3618241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320acdb3e60bc6bbac56773063a044e47a888ffe3806778cb998cb3739fc5407`  
		Last Modified: Tue, 09 Dec 2025 02:04:59 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d82f0af2b0dc3d8623c9659de5ce444393a5e7bed0896c1a4ff3e20a227339fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36373065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53b5b0e8df0b62268fdc4f0802dfc325c825eb289fa5cd38935f34b1aae63c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:43:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 29 Dec 2025 23:43:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 29 Dec 2025 23:43:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
VOLUME [/spiped]
# Mon, 29 Dec 2025 23:43:54 GMT
WORKDIR /spiped
# Mon, 29 Dec 2025 23:43:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:43:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe15f2c60d175e4fa4c514a3227917d573101d643ffe1f27c9b508c9102ad06`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142436ef7698bd0a0c276cedfaa7633c5b4b62afeaf6a43e68ebee211473b2d`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404bca06018f6b84d5500027da70a274572a04fb849a57ce3bf3f89aa06e769`  
		Last Modified: Mon, 29 Dec 2025 23:44:09 GMT  
		Size: 6.2 MB (6232063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c907968613021498b890cfee8c513c0a9a9f5cb8a072bdaa70682ee6389c90ab`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c188712597b5ba1b163b85abafe3515c309b0957d5f87b1a9b676c33982eea9d`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:4cc1b134021e6d459ebabe835e3ac5db7c257ae4ab4812d53e8614e331345f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89939c1909ed3ceae74c71dd1da09eb64efc62e16c2d31f2eb2e9d2061ae87a9`

```dockerfile
```

-	Layers:
	-	`sha256:ed68b1bfcd292069710110a67f93b2173eec3633332fc8e34e6206f453260e15`  
		Last Modified: Tue, 30 Dec 2025 02:05:34 GMT  
		Size: 3.6 MB (3621162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910cca8c7ce8141f416e527c593be9623ac5f5821cdca2e87064f80cc573afdd`  
		Last Modified: Tue, 30 Dec 2025 02:05:35 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:8187379c6228ce202ff5d4c94456c531f2a98b62f8626197b2394d09fca55436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37737953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe80eb9fc3c8d0bcf1f923f563cfa1a14973030eb8371a9e4e820a3e3430d381`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:12:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 08 Dec 2025 23:13:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 08 Dec 2025 23:13:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
VOLUME [/spiped]
# Mon, 08 Dec 2025 23:13:24 GMT
WORKDIR /spiped
# Mon, 08 Dec 2025 23:13:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:13:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6c3163818b6fb615e6724e571c7dfbf1db92a79858e8cf88fb9731ec063be4`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7614683e35746f5661794b7d905f74dea0dfa5813a6bbe1c58e043be59d2421`  
		Last Modified: Mon, 08 Dec 2025 23:13:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e834535a7b7e92e9a99b0ce53bd665892758fa2f8408b3be2621110510df16`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 6.4 MB (6442516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306cf8704e113ac01607bec5eca6e0302bad834d263c2d1e3202126bf76aa1b`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f985353893e48ccfac69c9c13935e5df63ecd6ce5a920aa8f8810ceeb9c1036`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:01b5afdfe9c701d9cd305b5bb27f2b31dfac4d340f82a9475457c2a5d6faff14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d65e242d82cb0bb5c1663803b1f84dc1aaaf60fe000d9d42b125df3c0c22a2`

```dockerfile
```

-	Layers:
	-	`sha256:2775ed98d9b7d6f1fd3db9b0e3ee54ce228d5e9da4576c5a05e599d55d577645`  
		Last Modified: Tue, 09 Dec 2025 02:05:09 GMT  
		Size: 3.6 MB (3620255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600c7b92499a400c0d0bed536e0c166b1c3403d3041303fb7f254d7197f8bb09`  
		Last Modified: Tue, 09 Dec 2025 02:05:10 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:231a1d43e5e776f583fc38bc47ed55ba2eedfa62290304d48a987615a462aaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40439563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d29fd0db4325b6621cff6f832dd227adcd56d8e6336fe24290042f35406c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 02:05:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 09 Dec 2025 02:05:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:06:11 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 09 Dec 2025 02:06:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 02:06:11 GMT
VOLUME [/spiped]
# Tue, 09 Dec 2025 02:06:12 GMT
WORKDIR /spiped
# Tue, 09 Dec 2025 02:06:13 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:06:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 02:06:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503a46c9fbb88b7b350edb4625885bb779e4f7be07b3082f24d86e36d3057986`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378ab413e123c64fee3801629972f0990f196b621ad4bcf3159eb489575eca96`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c5f2246f4178f1cd407178217dc9a96dbbc4d3c1d1c52aa8721328e9f88e3`  
		Last Modified: Tue, 09 Dec 2025 02:06:39 GMT  
		Size: 6.8 MB (6840311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36f671078cedaf1573055837372fa65c44c7f585cf3c2fc884f54bea5627456`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a5b467385c16a82f5fec93ac662bd467bd3fbecc909fdd8e5dbc0aa4e8ca8f`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:f027b13300b43abae6d2b151f755d9a0a5465e2ca3a5d03c6409f8167af98fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57accfcfec38bd8780719bd67c6bcaa96ea12709c98f4323d55c13426b386c9`

```dockerfile
```

-	Layers:
	-	`sha256:7ec26c40291155e915b5193c1a2408314af2d40f7c81eed8ac6cc4fd251d98d8`  
		Last Modified: Tue, 09 Dec 2025 05:04:51 GMT  
		Size: 3.6 MB (3621863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8e849d88a142868762c6f30924b1afdb7e60a293be00ea74339e88ac9b7c1e`  
		Last Modified: Tue, 09 Dec 2025 05:04:52 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:08978bf28bc0d7ac2e6f47f6e80882b98e0a6a0d6b5ea62730e32f6804801758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37634024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0795418aa4256b921cece24104f61c90d644699fe70f3ffad97e4461254155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 04:08:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Dec 2025 04:08:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 04:11:43 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Dec 2025 04:11:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Dec 2025 04:11:43 GMT
VOLUME [/spiped]
# Thu, 11 Dec 2025 04:11:44 GMT
WORKDIR /spiped
# Thu, 11 Dec 2025 04:11:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 04:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Dec 2025 04:11:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc6ae66f0155b9004dd1f3434d971d0493912ca5ca8e79b6232dcd72464f8ef`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f11fcb3db20b488e3ab58b9d2a5b4dda32f134f0de49f739f1ed5ed6cd3a3`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f91465220a957b207e2529e21cc60cd21ee499f509a66f6fe9d300d562cb1`  
		Last Modified: Thu, 11 Dec 2025 04:13:08 GMT  
		Size: 9.4 MB (9358512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b5259104cf9044c85e9d3b7ae514ce666bb643243f461992ba90a076a0053`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4d228d8e993bd097e714e4d8df72c5544d9cbef509190c3c6f90ad68f4a0fb`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:9e4f64518d61d958491edbfbbf4ad29ea6dfbb803d3ea587c406624c5c2cd30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f825073b9f2d6c7f7334a1d559a30c82e03daa62d80e8cbd028725de18755f0`

```dockerfile
```

-	Layers:
	-	`sha256:730a014b2cbdfd270e520864e6c838e014a8ae2efe5cfe156aba088532f28422`  
		Last Modified: Thu, 11 Dec 2025 08:04:45 GMT  
		Size: 3.6 MB (3613269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e953648960d7c96a844ee9c357d7ba606100a2ca5eab2c925b6eb365518ace8`  
		Last Modified: Thu, 11 Dec 2025 08:04:45 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:fd7f0e30d0f4fa7b0a04170b6350d2b17cfe65ae8784e52a6b7749ec25fd596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35958428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35393eb489a51e91bba712273d44ca8a8c9cc3b845e6d2cffb9d292d4e8eb1bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:37:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 30 Dec 2025 00:37:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 30 Dec 2025 00:38:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
VOLUME [/spiped]
# Tue, 30 Dec 2025 00:38:08 GMT
WORKDIR /spiped
# Tue, 30 Dec 2025 00:38:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:38:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4598f0fe0ec5b6dbe64aac084c86c1ef64cc495e9e0aa59e95e5b5ba2524f7`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91620759fafc1d1c5cb4f18a00f4cb4377652efe7920db9a10895cd0e7e94d68`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2642203b10576c7b7dd707aa9cf88bbbce7471eaa4ea825439abae85cf07212`  
		Last Modified: Tue, 30 Dec 2025 00:38:25 GMT  
		Size: 6.1 MB (6121643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96010cfacda4d93f71ee023511910b20f8b40d4e1e3f54b810a32c0ca838601`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae779a5c1cfac43eca3758b75ace95e6d1d9e6c5723564d11b89c064bfdd008`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:beb09fde5a4716220058166de08ce6f82421330fea3005976df36f2b78bbe59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc76f41916d041fcbdd4277500e819c763801a448c2534be7abf4f316cf1da`

```dockerfile
```

-	Layers:
	-	`sha256:6ca6f58385becddea4ed57434f2dec40641e09de615d06202c7ebd28bffc8f1c`  
		Last Modified: Tue, 30 Dec 2025 02:05:51 GMT  
		Size: 3.6 MB (3618489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050a745f90b1400d1728907caaf1cc2268e61f30e6442658a879615c33a092e9`  
		Last Modified: Tue, 30 Dec 2025 02:05:51 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Tue, 16 Dec 2025 23:20:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Tue, 16 Dec 2025 23:20:31 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Tue, 09 Dec 2025 15:14:13 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Tue, 16 Dec 2025 23:20:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Tue, 09 Dec 2025 15:14:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Tue, 16 Dec 2025 23:20:43 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Tue, 16 Dec 2025 23:20:46 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Tue, 16 Dec 2025 23:20:49 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Tue, 16 Dec 2025 23:20:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Tue, 16 Dec 2025 23:20:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Wed, 08 Oct 2025 22:09:24 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Tue, 16 Dec 2025 23:20:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Tue, 16 Dec 2025 23:21:02 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Tue, 16 Dec 2025 23:21:05 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Tue, 16 Dec 2025 23:21:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Tue, 16 Dec 2025 23:21:12 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Tue, 16 Dec 2025 23:21:18 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Tue, 16 Dec 2025 23:21:20 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Tue, 16 Dec 2025 23:21:23 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Tue, 16 Dec 2025 23:21:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Tue, 16 Dec 2025 23:21:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Tue, 16 Dec 2025 23:21:35 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Tue, 16 Dec 2025 23:21:38 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Tue, 16 Dec 2025 23:21:41 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Tue, 16 Dec 2025 23:21:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Tue, 16 Dec 2025 23:21:47 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Wed, 08 Oct 2025 21:39:30 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Wed, 08 Oct 2025 21:39:30 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Tue, 16 Dec 2025 23:21:52 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Tue, 16 Dec 2025 23:21:55 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Tue, 16 Dec 2025 23:21:58 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Tue, 16 Dec 2025 23:22:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Tue, 16 Dec 2025 23:22:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 03:32:04 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 03:32:04 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Tue, 16 Dec 2025 23:22:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Tue, 16 Dec 2025 23:22:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Tue, 16 Dec 2025 23:22:18 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Tue, 16 Dec 2025 23:22:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Tue, 16 Dec 2025 23:22:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 20:50:03 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 20:50:03 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Tue, 16 Dec 2025 23:22:30 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Tue, 16 Dec 2025 23:22:32 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Tue, 16 Dec 2025 23:22:35 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Tue, 16 Dec 2025 23:22:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Tue, 16 Dec 2025 23:22:40 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 02:25:54 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 02:25:54 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:7b9625a81e8db9045c4eaf8f9bf40b8ef8c78a666bb7201d8d7c80538a418f7a
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
$ docker pull spiped@sha256:7d011e9e579768cd749e2df95806a3b739ebbdd516385dac92f2e9cda3570e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d66303cac034d8960b8128b5967170028d350ecf6e131c4bf30b000a3f836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c041bc04e274276fc6a842ca20a0cf973af7c178bcfb6575c0d8203718fc91`  
		Last Modified: Tue, 16 Dec 2025 23:20:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f81b6f5c689713065e6b968619711a3bd698fd708594cc90dae3977d54ca24e`  
		Last Modified: Tue, 16 Dec 2025 23:20:31 GMT  
		Size: 8.0 KB (7950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a035501670b01c25e6d7ce231bae87ef493bb668e877be52618f03679b673c4f`  
		Last Modified: Tue, 09 Dec 2025 15:14:13 GMT  
		Size: 107.6 KB (107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f81362a47a6b65eaf0da33a0c61df7c9a874d76861e5ae8fa0bc16547593db`  
		Last Modified: Tue, 16 Dec 2025 23:20:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae81c7faaf7b0d0454b9d217085e8da2f5e5a72ead2527e67506b0d4834801`  
		Last Modified: Tue, 09 Dec 2025 15:14:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed8b2f715fbc09ab5fcc75433e022573fd8e46bded0d7dd791180a01b3d4a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b323748eb9cefd40fcfe67d6c7dd561a4f5c4498457b7739b98161ea53a531c`

```dockerfile
```

-	Layers:
	-	`sha256:64366b1f73c30d49b216afd6a2acb0a27ad6d69bbaf554934ef1fb5a1b8ae379`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77f4db066b7ca49f19231acfa8a9f30749e3884bc787f4fcb01d3cb8a54b848`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:07f6c1ec4d9a40087ba1fabf98ca259b39af58fe0aa3d1b5aff7a5c9c85aab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66830d62439293e746c3d4171b26eb7b060853f622562e26647e13254243d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e87cee3c8273a66e75e0a084e6876c74329042a77778cc75c7865eafb5817`  
		Last Modified: Tue, 16 Dec 2025 23:20:43 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e054efed96e629a0c9a72dadd2a8d348aa66730afa5f59ce6e02a530b64b8d73`  
		Last Modified: Tue, 16 Dec 2025 23:20:46 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbbcac13a86093cd5821deda5686d525abf33f1ffacea149ae0a0b642a332f`  
		Last Modified: Tue, 16 Dec 2025 23:20:49 GMT  
		Size: 89.2 KB (89158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448f1d44fa11364cf66800119dd7e5e05fc9b9d8384cce8cc858006c0684aae`  
		Last Modified: Tue, 16 Dec 2025 23:20:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fa931b05c23aa0b5927c5fc4bea0d9aa65908b7ac3e936a5a5888060a49337`  
		Last Modified: Tue, 16 Dec 2025 23:20:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e083a00e19dd556e9a671f1709ffc708a0ab8d2a7373856218a44de2df24d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47da3cb18e03a2142fd48220b0903336c0d8a799d804ac3b38780211559ba36`

```dockerfile
```

-	Layers:
	-	`sha256:069680ffcf03350d43ef8d45bcb21dafd37c1132acdfce2d83391a239a85d47e`  
		Last Modified: Wed, 08 Oct 2025 22:09:24 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:742d7ee47c94e03887525e682c2614d90b9b1f43f674ce4407bcf06b787caa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3312569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db7cd0fffd0a4f2c540dfe37e4c940cf5c7595aeffea1bf7acc4b1793c73d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a85ed9579bf45ac1db2ef56f4067b84fe0c4d8e51e006ec1d925eb0c32bf22`  
		Last Modified: Tue, 16 Dec 2025 23:20:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85621545c13dee2ff1d8660f7847266105703d040c19d1816e374881a3bdf6e`  
		Last Modified: Tue, 16 Dec 2025 23:21:02 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afad049c072c9b6d3ed2946f7d0c0782835979f90696b68ac6e4c0efff5bf4`  
		Last Modified: Tue, 16 Dec 2025 23:21:05 GMT  
		Size: 81.7 KB (81688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35464221f20a70de628e3018e70c13c2e8ed9970a791049f1ba3bae429355536`  
		Last Modified: Tue, 16 Dec 2025 23:21:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6fea506e0050596918141446ad53da32b5b3a4fc9c7a5d497caf9a7ec6390`  
		Last Modified: Tue, 16 Dec 2025 23:21:12 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1db53d701cc5320b98ed95f8e8288e9c84ddb8ad31b517b42fe2faa626874b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53816c0890232fc85b4017c83eabcfb11884aeab001b608b66e2a8c9e183e3`

```dockerfile
```

-	Layers:
	-	`sha256:f33fdb1fd07f91c527d8c950dcb81f1eea51882f51d66c0f4da88547240c6499`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a9fe69db1d74bfbe4aa6a07c0fb4e0e59f4eff9e1636b7e0c486b6435b788b`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1c2f38931ee0ff681a7c140bbc874fa1ff5837de4baf9a50a3498fbcb12a9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0a53163c15fa0112f2865ee8a52cbed044f04fc7001f7bd1f5e407cd57237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94547f3886a10ef8162a5d7fe9f4308e302dcfd48f5be2db3b1e5d4b5156d815`  
		Last Modified: Tue, 16 Dec 2025 23:21:18 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee5fd6e341869b5bcb70e517a1466b54c5191790816dd7956a41164690328b`  
		Last Modified: Tue, 16 Dec 2025 23:21:20 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed7625e00fce702c1adbf90233532e0e4e98935a777f6bdffa076b1c3be2`  
		Last Modified: Tue, 16 Dec 2025 23:21:23 GMT  
		Size: 100.6 KB (100621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612c8ef14c84a7450d3ced7f152a93e533ffbb92d525fae7dde4c2988e230d7`  
		Last Modified: Tue, 16 Dec 2025 23:21:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ac69ec6618a756cde4ab30a4488c3f0f7b89df240ede5a7b0a29d66250444`  
		Last Modified: Tue, 16 Dec 2025 23:21:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f599a056737cf26e2f1e5bfb25bf8cf6f92cea0ea27b040de42b2e4bf139168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 KB (96684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c665f9e5776de9d503dbefb3dccddb1d230d81716f5b086b02065d6f512d0`

```dockerfile
```

-	Layers:
	-	`sha256:8c6690f0ed02188be28287964aecbd171476e7e9484ec40d030c20c7b0e182c3`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4ac6f12c825868630b75c268c91338db29a424c87e551c1153694da325c83`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac72ab4f716c2dabdad650618a34deccd477e31f604bf27a1f630a7a8433d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf996beac99b6a5d8eae08ab4703a9cc11bccf3cb429e61a25bebf2947e4b519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664f8e36f37724daee2260066812a0de8999a28949591daef235c15d49ca301a`  
		Last Modified: Tue, 16 Dec 2025 23:21:35 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee281d18609c0bc414db88c7d17dd26aca0857610126d3e6d974952f5a414ab`  
		Last Modified: Tue, 16 Dec 2025 23:21:38 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8cb95edb963d4e91f7f5ea1c0881091c485846b9df554d3c11102b6a6a753`  
		Last Modified: Tue, 16 Dec 2025 23:21:41 GMT  
		Size: 120.1 KB (120110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473aab810bb857acc1c39fc855966c0a2de5edd8a71287cf2183cea8dc6fdc4b`  
		Last Modified: Tue, 16 Dec 2025 23:21:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1968cadac684d87fbcd83e1d646d178ae33c9242a480ddbd04f8fdf77b5e2ed`  
		Last Modified: Tue, 16 Dec 2025 23:21:47 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2e9fe75d8ecfc557edbdaa8476f159fdb286886f6212788ecb61cda153b3ee2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e13e74ee61a3719d708f5b8486f092d523816b5c47e960b60b25a5d76b1aaee`

```dockerfile
```

-	Layers:
	-	`sha256:565649aba2f7ebad36d4ce1a64e495876030406355bb0f7a99f41f82b8300791`  
		Last Modified: Wed, 08 Oct 2025 21:39:30 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1923abaf687d0c1af4d1718e1e365a3359dbf3e5ff8c339291f60bb0fc220`  
		Last Modified: Wed, 08 Oct 2025 21:39:30 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:506cee7907557b7efa054dc1a4c3261e8956700c9f553e9eb8d9a3470a368431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7a1787271596d011a96a2b5632780587dd9653d8b0410f93093e13ecb8fcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf524fa67a04db3aef99fc4ab2113633c6c1965d0f890616009377904a6284`  
		Last Modified: Tue, 16 Dec 2025 23:21:52 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9d95b7526b98e836dea8e7e9792130d0d6d71b1d6259e6f954ddffc64f5cc`  
		Last Modified: Tue, 16 Dec 2025 23:21:55 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011805850ee2924d217a7651762c507b895c90911b4151207fe8e82e4388fcce`  
		Last Modified: Tue, 16 Dec 2025 23:21:58 GMT  
		Size: 112.7 KB (112682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef441d2768884d48fcb3b73e59f27e5fe6fc1cb5484df89fd3db0df4ce9437`  
		Last Modified: Tue, 16 Dec 2025 23:22:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03005fd392da3ad1cd46c719335ac18f079118e761584617fe8c73405301647d`  
		Last Modified: Tue, 16 Dec 2025 23:22:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:55eac1eb38ff8ce12fb98d86fb70542b4620b4c59ff746effba30530ad8676de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a3d2f7338bf8715707424b7b716c4498d4c3b844d2dc7387da9a1c64357879`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6cde5a2631b7b9b782bb7fdfcf5de409ca1736416d9573c8888daf799d9e0`  
		Last Modified: Thu, 09 Oct 2025 03:32:04 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9220e8aff0f38f3e237e21c128db8adfad10ae35fb9db4dc56ead1ff1235e9d`  
		Last Modified: Thu, 09 Oct 2025 03:32:04 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0f378090b0e02992217f4f2a73d59cfb8c76cf62d83fec92991b3a8b1f0bfcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7d261c52ce9f797be48d32c37a2c3f66b54a18d3599dd071fefa04e588df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c352072eefdbb94e63d3787f16fac871ba719ed362861b9e97b581edd60548`  
		Last Modified: Tue, 16 Dec 2025 23:22:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa05a9bc37f5bb35d75064bac3af035a1d3a82ac079befd8019359672cc322`  
		Last Modified: Tue, 16 Dec 2025 23:22:15 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a4b112c1b7e8d19565628602648b41c69109d0f16548d16e781b095481e4d`  
		Last Modified: Tue, 16 Dec 2025 23:22:18 GMT  
		Size: 98.9 KB (98862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971a3bdcb8df001e3163788a7484aea74c6bf79af7ec5c42ae330638a863112`  
		Last Modified: Tue, 16 Dec 2025 23:22:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e689628a891ec93dec38687edd123814871319bfb552253a1ab8608d94fa74`  
		Last Modified: Tue, 16 Dec 2025 23:22:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ef79fccc5586c74ed7a097a019247ca0f6644364c4e1b931202ce2f00cf4e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35fd6859715e249d4b311ca37e3e8e7886a7ce1788f0688877545e1f0fb2b`

```dockerfile
```

-	Layers:
	-	`sha256:624da72bc5bd15d76a69efe794516160d8151dc3f9b207f42a5b8b5165948a76`  
		Last Modified: Fri, 10 Oct 2025 20:50:03 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83fb34ab49138178f6f97cf97ae672fc5e173707dec2895a8d5b36f2e7689a5`  
		Last Modified: Fri, 10 Oct 2025 20:50:03 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:be3e9a57eb9caa9fb853c68e3efdc680d9d441f399d676b7a437f56a46d71b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3755528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee68dd7eaa10392bbfe4c42a39adf582bc976bf97937637b807540ed7960af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 10 Aug 2025 19:07:57 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["/bin/sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 10 Aug 2025 19:07:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
VOLUME [/spiped]
# Sun, 10 Aug 2025 19:07:57 GMT
WORKDIR /spiped
# Sun, 10 Aug 2025 19:07:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 19:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 19:07:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca97998e3d4f083ea39c1b7e9bd8d771aaa888745b8a60d6baff87ab6f8f37`  
		Last Modified: Tue, 16 Dec 2025 23:22:30 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae19bb237945d6597aced8fc4cd16e5d4f06869978f4f6eb5d90a8bc9be7f39`  
		Last Modified: Tue, 16 Dec 2025 23:22:32 GMT  
		Size: 8.0 KB (7957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce433dda6c532473e5da602686ec5186ad28c43789f172a14efc1cd9e38093d`  
		Last Modified: Tue, 16 Dec 2025 23:22:35 GMT  
		Size: 96.9 KB (96944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b81ca187d86754818499befad84648bb33d900aa6c797f74f14d7f06589dd`  
		Last Modified: Tue, 16 Dec 2025 23:22:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de821656be3d9d0eadaa8bfe8c17052ce64308ac54b60bb962a59498810f549e`  
		Last Modified: Tue, 16 Dec 2025 23:22:40 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:daeef3e785369b94f4c3fec6e7b468c0aa8bcc71748eb82a5dcb98744d0c094a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff814477e4912c3dbc0dc6c3b2d236588fe065252c86c9a2ed142e200619a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3ccf297cff7eee80cdb3e7128fdeabdb48c58df324a049928273000e72eba72d`  
		Last Modified: Thu, 09 Oct 2025 02:25:54 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfca2be336420edbf2af734bab83d3864c289d0e61390ac2cfc5f6d7f183847`  
		Last Modified: Thu, 09 Oct 2025 02:25:54 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:75913f840d9a5ad3176ed693a6913324812495de158cc45fe72eb7b3c3cfea07
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
$ docker pull spiped@sha256:e0ab6e15a69a394c24e27e4d0e6b01aecdb4276780da735359598a8e7d610065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36827205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f559144e209b38285c9ec2149b96cf8756638f8f6662f714c92430305327b301`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:41:33 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 29 Dec 2025 23:41:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 29 Dec 2025 23:41:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
VOLUME [/spiped]
# Mon, 29 Dec 2025 23:41:58 GMT
WORKDIR /spiped
# Mon, 29 Dec 2025 23:41:58 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:41:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:41:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61114f1a7738d806984fd07548daac6fa1d09d6d1423c07542a8c6aab32b4a0a`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5fb473085a4a935991d9ec63fef7cd3976104ef825622bbddf5484eac405d5`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be147d212d4d67ff160c1229aaadd29b1fd86bc10fe931f17e53f3712d6386a7`  
		Last Modified: Mon, 29 Dec 2025 23:42:12 GMT  
		Size: 7.0 MB (7048306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9588de47f007973e38b96f1d3b803cfc9af343a24f74e0f204f1e1b7cb01f064`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424b48fe70f9ea781b6efbe29557a1ed90ee9a6a28396eb77dac3c7f2e6d68`  
		Last Modified: Mon, 29 Dec 2025 23:42:11 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:997fdcb5c86c9fb49e7f972e7cd5aa5910c3c8ae5fa53d17cf5802afc2f9ea84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9efb54159f0b55ae1a044da27f4fbe33c623264c14eaae376a6fa71598aa35`

```dockerfile
```

-	Layers:
	-	`sha256:fee02ddcbce0920a76b6f684f83bc056025b9d0d6ae31ca8009bbc5e8149bacc`  
		Last Modified: Tue, 30 Dec 2025 02:05:22 GMT  
		Size: 3.6 MB (3626126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa7911ea504c36133be4385ba95ccc8f549954416a8bc4eff7c5945e617fb4ce`  
		Last Modified: Tue, 30 Dec 2025 02:05:22 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:91b17bfed43cd4cad49c799ca272fedc1a1be14ab28405b63b34a2d8136a7be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33736059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a04c8fd9616a5e22d4dc9f05c1bcc9fea99c18e540ee42c74d2b6afd7898ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:28:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 30 Dec 2025 00:28:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 30 Dec 2025 00:28:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
VOLUME [/spiped]
# Tue, 30 Dec 2025 00:28:46 GMT
WORKDIR /spiped
# Tue, 30 Dec 2025 00:28:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:28:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:28:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0193512c6cf65ee9280aa94d68551d1cc99c9945782505a191176a31c40d467`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fcaaf3a6edd0b5fcd46b535cf395e44246af04d83a8749b20c578b804168cf`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968bb20d69c66cb7c0cb819c0842fc86379cb8ae65498f9a43822e2f7f23aa93`  
		Last Modified: Tue, 30 Dec 2025 00:29:04 GMT  
		Size: 5.8 MB (5789542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62430768fd1ff023ecd14eb2f6206cece7aed822f75d39814a94952935f2821`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61f8bab7324653dff9134255853c0eccbdfe3a0309cfbb8aa3d9c6dadfec94c`  
		Last Modified: Tue, 30 Dec 2025 00:29:01 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d32b61812ab8572daeabe6b7d9339d20bda55b5c76ba345ccdbf26d60b2dea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9c3958f2f7d8b4eb3b44337db951c0b1bb9e7714990c189010da1c7cdda670`

```dockerfile
```

-	Layers:
	-	`sha256:b30cb319d8121e7bcec7440216b934792921bb31c85e23dd32186b4dee105f77`  
		Last Modified: Tue, 30 Dec 2025 02:05:26 GMT  
		Size: 3.6 MB (3619120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f381644189fbffa088bbbdaba9a72f12a1d42e7e3bb039b1e1e29567fe11d4`  
		Last Modified: Tue, 30 Dec 2025 02:05:27 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:5200083bb38fef4bc7574dc55308b9703006fc9e1d217ddd4bd5bf54ed67e743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31797343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0a36ed22c5498f85b2048a95288b32294a5e7799b1f695ad69ad84c1fc38fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:59:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 09 Dec 2025 00:00:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 09 Dec 2025 00:00:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
VOLUME [/spiped]
# Tue, 09 Dec 2025 00:00:24 GMT
WORKDIR /spiped
# Tue, 09 Dec 2025 00:00:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:00:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:00:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fad81476600f360ac6aac53f19096a951b0aa17f7ebcd0af40144c002440746`  
		Last Modified: Tue, 09 Dec 2025 00:00:52 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f2442e1fcfc806776dc7cc0a02758ee841ae774e5dbcf6ce2ec3dd37792d11`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f9951c3bdb9b2566c5e3eac7d8ace68c15bac473cf4448d9246318a43dc0c`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 5.6 MB (5584966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6535c74f54d0fcd5cedd525de4724882f3c4f3e0a291c4cc20e3a4b0a11d4b`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99cda306c96e1344b0f7665b2fd449b3d289dde46535217c355c22dd7cbe82`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:0b1988ed27e75d85e9b3a84e466787ec81bd5a0c97ec53fbd660969aef5f82ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8423f58edd5d3f4981c6adc179173cc30386b1776dae470179d6de1b1568ea`

```dockerfile
```

-	Layers:
	-	`sha256:cb88ad9317068008ece0955b69ab1bf4f1a10fcf8dbb9bd62372819f2f3f7083`  
		Last Modified: Tue, 09 Dec 2025 02:04:58 GMT  
		Size: 3.6 MB (3618241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320acdb3e60bc6bbac56773063a044e47a888ffe3806778cb998cb3739fc5407`  
		Last Modified: Tue, 09 Dec 2025 02:04:59 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d82f0af2b0dc3d8623c9659de5ce444393a5e7bed0896c1a4ff3e20a227339fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36373065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53b5b0e8df0b62268fdc4f0802dfc325c825eb289fa5cd38935f34b1aae63c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:43:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 29 Dec 2025 23:43:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 29 Dec 2025 23:43:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
VOLUME [/spiped]
# Mon, 29 Dec 2025 23:43:54 GMT
WORKDIR /spiped
# Mon, 29 Dec 2025 23:43:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:43:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe15f2c60d175e4fa4c514a3227917d573101d643ffe1f27c9b508c9102ad06`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c142436ef7698bd0a0c276cedfaa7633c5b4b62afeaf6a43e68ebee211473b2d`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404bca06018f6b84d5500027da70a274572a04fb849a57ce3bf3f89aa06e769`  
		Last Modified: Mon, 29 Dec 2025 23:44:09 GMT  
		Size: 6.2 MB (6232063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c907968613021498b890cfee8c513c0a9a9f5cb8a072bdaa70682ee6389c90ab`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c188712597b5ba1b163b85abafe3515c309b0957d5f87b1a9b676c33982eea9d`  
		Last Modified: Mon, 29 Dec 2025 23:44:08 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:4cc1b134021e6d459ebabe835e3ac5db7c257ae4ab4812d53e8614e331345f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89939c1909ed3ceae74c71dd1da09eb64efc62e16c2d31f2eb2e9d2061ae87a9`

```dockerfile
```

-	Layers:
	-	`sha256:ed68b1bfcd292069710110a67f93b2173eec3633332fc8e34e6206f453260e15`  
		Last Modified: Tue, 30 Dec 2025 02:05:34 GMT  
		Size: 3.6 MB (3621162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910cca8c7ce8141f416e527c593be9623ac5f5821cdca2e87064f80cc573afdd`  
		Last Modified: Tue, 30 Dec 2025 02:05:35 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:8187379c6228ce202ff5d4c94456c531f2a98b62f8626197b2394d09fca55436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37737953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe80eb9fc3c8d0bcf1f923f563cfa1a14973030eb8371a9e4e820a3e3430d381`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:12:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Mon, 08 Dec 2025 23:13:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Mon, 08 Dec 2025 23:13:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
VOLUME [/spiped]
# Mon, 08 Dec 2025 23:13:24 GMT
WORKDIR /spiped
# Mon, 08 Dec 2025 23:13:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:13:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6c3163818b6fb615e6724e571c7dfbf1db92a79858e8cf88fb9731ec063be4`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7614683e35746f5661794b7d905f74dea0dfa5813a6bbe1c58e043be59d2421`  
		Last Modified: Mon, 08 Dec 2025 23:13:40 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e834535a7b7e92e9a99b0ce53bd665892758fa2f8408b3be2621110510df16`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 6.4 MB (6442516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306cf8704e113ac01607bec5eca6e0302bad834d263c2d1e3202126bf76aa1b`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f985353893e48ccfac69c9c13935e5df63ecd6ce5a920aa8f8810ceeb9c1036`  
		Last Modified: Mon, 08 Dec 2025 23:13:38 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:01b5afdfe9c701d9cd305b5bb27f2b31dfac4d340f82a9475457c2a5d6faff14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d65e242d82cb0bb5c1663803b1f84dc1aaaf60fe000d9d42b125df3c0c22a2`

```dockerfile
```

-	Layers:
	-	`sha256:2775ed98d9b7d6f1fd3db9b0e3ee54ce228d5e9da4576c5a05e599d55d577645`  
		Last Modified: Tue, 09 Dec 2025 02:05:09 GMT  
		Size: 3.6 MB (3620255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600c7b92499a400c0d0bed536e0c166b1c3403d3041303fb7f254d7197f8bb09`  
		Last Modified: Tue, 09 Dec 2025 02:05:10 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:231a1d43e5e776f583fc38bc47ed55ba2eedfa62290304d48a987615a462aaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40439563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d29fd0db4325b6621cff6f832dd227adcd56d8e6336fe24290042f35406c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 02:05:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 09 Dec 2025 02:05:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:06:11 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 09 Dec 2025 02:06:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 02:06:11 GMT
VOLUME [/spiped]
# Tue, 09 Dec 2025 02:06:12 GMT
WORKDIR /spiped
# Tue, 09 Dec 2025 02:06:13 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:06:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 02:06:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503a46c9fbb88b7b350edb4625885bb779e4f7be07b3082f24d86e36d3057986`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378ab413e123c64fee3801629972f0990f196b621ad4bcf3159eb489575eca96`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c5f2246f4178f1cd407178217dc9a96dbbc4d3c1d1c52aa8721328e9f88e3`  
		Last Modified: Tue, 09 Dec 2025 02:06:39 GMT  
		Size: 6.8 MB (6840311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36f671078cedaf1573055837372fa65c44c7f585cf3c2fc884f54bea5627456`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a5b467385c16a82f5fec93ac662bd467bd3fbecc909fdd8e5dbc0aa4e8ca8f`  
		Last Modified: Tue, 09 Dec 2025 02:06:38 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:f027b13300b43abae6d2b151f755d9a0a5465e2ca3a5d03c6409f8167af98fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57accfcfec38bd8780719bd67c6bcaa96ea12709c98f4323d55c13426b386c9`

```dockerfile
```

-	Layers:
	-	`sha256:7ec26c40291155e915b5193c1a2408314af2d40f7c81eed8ac6cc4fd251d98d8`  
		Last Modified: Tue, 09 Dec 2025 05:04:51 GMT  
		Size: 3.6 MB (3621863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8e849d88a142868762c6f30924b1afdb7e60a293be00ea74339e88ac9b7c1e`  
		Last Modified: Tue, 09 Dec 2025 05:04:52 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:08978bf28bc0d7ac2e6f47f6e80882b98e0a6a0d6b5ea62730e32f6804801758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37634024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0795418aa4256b921cece24104f61c90d644699fe70f3ffad97e4461254155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 04:08:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 11 Dec 2025 04:08:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 04:11:43 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 11 Dec 2025 04:11:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Dec 2025 04:11:43 GMT
VOLUME [/spiped]
# Thu, 11 Dec 2025 04:11:44 GMT
WORKDIR /spiped
# Thu, 11 Dec 2025 04:11:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 04:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Dec 2025 04:11:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc6ae66f0155b9004dd1f3434d971d0493912ca5ca8e79b6232dcd72464f8ef`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723f11fcb3db20b488e3ab58b9d2a5b4dda32f134f0de49f739f1ed5ed6cd3a3`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f91465220a957b207e2529e21cc60cd21ee499f509a66f6fe9d300d562cb1`  
		Last Modified: Thu, 11 Dec 2025 04:13:08 GMT  
		Size: 9.4 MB (9358512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b5259104cf9044c85e9d3b7ae514ce666bb643243f461992ba90a076a0053`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4d228d8e993bd097e714e4d8df72c5544d9cbef509190c3c6f90ad68f4a0fb`  
		Last Modified: Thu, 11 Dec 2025 04:13:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9e4f64518d61d958491edbfbbf4ad29ea6dfbb803d3ea587c406624c5c2cd30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f825073b9f2d6c7f7334a1d559a30c82e03daa62d80e8cbd028725de18755f0`

```dockerfile
```

-	Layers:
	-	`sha256:730a014b2cbdfd270e520864e6c838e014a8ae2efe5cfe156aba088532f28422`  
		Last Modified: Thu, 11 Dec 2025 08:04:45 GMT  
		Size: 3.6 MB (3613269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e953648960d7c96a844ee9c357d7ba606100a2ca5eab2c925b6eb365518ace8`  
		Last Modified: Thu, 11 Dec 2025 08:04:45 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:fd7f0e30d0f4fa7b0a04170b6350d2b17cfe65ae8784e52a6b7749ec25fd596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35958428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35393eb489a51e91bba712273d44ca8a8c9cc3b845e6d2cffb9d292d4e8eb1bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:37:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 30 Dec 2025 00:37:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 30 Dec 2025 00:38:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
VOLUME [/spiped]
# Tue, 30 Dec 2025 00:38:08 GMT
WORKDIR /spiped
# Tue, 30 Dec 2025 00:38:08 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:38:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:38:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4598f0fe0ec5b6dbe64aac084c86c1ef64cc495e9e0aa59e95e5b5ba2524f7`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91620759fafc1d1c5cb4f18a00f4cb4377652efe7920db9a10895cd0e7e94d68`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2642203b10576c7b7dd707aa9cf88bbbce7471eaa4ea825439abae85cf07212`  
		Last Modified: Tue, 30 Dec 2025 00:38:25 GMT  
		Size: 6.1 MB (6121643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96010cfacda4d93f71ee023511910b20f8b40d4e1e3f54b810a32c0ca838601`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae779a5c1cfac43eca3758b75ace95e6d1d9e6c5723564d11b89c064bfdd008`  
		Last Modified: Tue, 30 Dec 2025 00:38:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:beb09fde5a4716220058166de08ce6f82421330fea3005976df36f2b78bbe59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc76f41916d041fcbdd4277500e819c763801a448c2534be7abf4f316cf1da`

```dockerfile
```

-	Layers:
	-	`sha256:6ca6f58385becddea4ed57434f2dec40641e09de615d06202c7ebd28bffc8f1c`  
		Last Modified: Tue, 30 Dec 2025 02:05:51 GMT  
		Size: 3.6 MB (3618489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050a745f90b1400d1728907caaf1cc2268e61f30e6442658a879615c33a092e9`  
		Last Modified: Tue, 30 Dec 2025 02:05:51 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
