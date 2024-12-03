<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.2`](#spiped162)
-	[`spiped:1.6.2-alpine`](#spiped162-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:dc865865e32a1753cf039b2fd22a0fbe795e43cc114a72b47337aead272c579b
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
$ docker pull spiped@sha256:200ec4e93c35786b0d6870d1348514227856fca9fe2081fed0bc6a90674ffa1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37105336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d34473cd812231b18a36f9927a0d1043adfd6ed828e9c24cec15c434e92085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3286318ec16df9127f2df21853581c4604d80ddf277571598ba4d3cd9ba8d06`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5820a96fb11372f32db1517cfd3ecdbbc95268d570014b05d5189ff9059558d6`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 2.4 MB (2401316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aae95d27db2c7f60304b6d4caf995e2a4c87c8eb68e59258480356605069757`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 6.5 MB (6470896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f11f1af366366154b69ba358da0eee393f48cb92cd432045a2871b3b48611be`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2f708db687582ba60d4f0a9cf8b5aef58b41e1c9d1e6b55ab2389f651696e`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:beec0572119e6983b373db1541336a5c6e47d7b97d89d6c6bfffa0e7c1f0abf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3534707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdf0c19de4f5fefe621fd39611d51b7337e0cd0c79de9c1ec1df72eba7bbabe`

```dockerfile
```

-	Layers:
	-	`sha256:1ac30357219ecd62dd514f0204dc7d3d893b8d13cd1e564629343ef671ce54b8`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 3.5 MB (3519667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6b7040b0115ed1adbb45eb11a8af1b412044b9808c156a066992393d6f8a408`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:99bae00cf14c15b697d0d763f1cc2786a8ef3014205f92973feec9c433169295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32891828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b5d8ff57ff5b9caeca8c033884260511a9fce334125f1010083d281d1676aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd5640db7c017698d7b30fd28894a8b9ad8a7bc4a4386d6544c58cbaa52cb1`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2f4c086ad6cb5027d62e957a4520d83274ac2410264bc159ef1f2068b5d9da`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 2.0 MB (1997157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece220a1765f83103e52d02b2549660ea3780a2868d9fbefd43008ae531fb1b3`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 5.1 MB (5138204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33ebf0d87cd479ee5b4538f8cc21c8207e49d820150b1aae450bf7f7bad209a`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5500361841fa5eed10c07a2ad67786591f923b91f16100d8d0747cad187c0946`  
		Last Modified: Tue, 03 Dec 2024 05:23:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:0bda7c1c8df2b5dcc25d961783e13814b4edafecb7ba81e21d5cc9147d1491f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3505295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbed979c8633b9a67ac4b5823932537b1fc4f2c62cd494becd49ff5b75ee12fb`

```dockerfile
```

-	Layers:
	-	`sha256:49f065d55e94a2714b8da791b80846d265d7f186ea2b7de24ed2f309b7d0cc80`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 3.5 MB (3490154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954074d055a2da99643a9a77a1427a0a0f9a3a3e0506fc63528185ad283180b5`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:2673df6c6719abf8451fb416c1ef76ef5beb44dc34d5931c44f45615104395e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30671069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e139c71119fc43443aa86def096eff57086f03c8ef209907a3b59915ee073d7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0b33b4924d962002c20a6328508a5d34d55a2268c73260a6ed9573efce1a3`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43684839a478b9597d614ce8c9c4bd4c7249bb2538a7d3ae859c23a0285fd81f`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 1.9 MB (1855568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0997a5f940d2355e20ffc1ad885efbc15e4958e6505c582aee9fa2cf15255672`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 4.9 MB (4880372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3c4bbaffcc0915aab01140cf0a2cb2b5e2459ce7ecdb12b7bae465cfd7569`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814fda2ba08a0128f768b2977da950819bb0b09b7fae8091289c7d5251fd85b1`  
		Last Modified: Tue, 03 Dec 2024 07:24:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:1825ceb8dbe263a5d3ab65967531abe6affbc02d395158656e2ea44cd219611e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3504787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48421b9da41d41313c82951bb2d6f9bc6dfe713ebd7d92e0c78df51cadbeeb1b`

```dockerfile
```

-	Layers:
	-	`sha256:f14bb418cfb656486fac664f1d6454405450d69c15455e32f8b22d7a5784e86c`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 3.5 MB (3489645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43bb8fca856669ae96e3ce21d76a4ea8f735da4bc5c77d5711090d1eb4c3b7cf`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:237639a6abc6759047cbedc84fa3b66cbd6ccdabe961beff525a31d62f53f2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f274e74e766b46776e29d3fd09d41b620a74f401a213567f1baafcb7c41de3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27124ec490922d03dbb43d024c6ce24f8bf5e4b3fefe0fb0bfb176bbca183b43`  
		Last Modified: Tue, 03 Dec 2024 05:16:41 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec665e61bafba9d4661d86c699686653a61a994d6f8971fa01c63a9cda314d`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 2.2 MB (2247018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccd97308df6bd4ed70f344990461d2dce6a0efcb6ddaf951541e773faef1758`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 5.5 MB (5481125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6434819fb7e89a144affd3b9e3844d3924d854be57d0bf57382b920a90d1599`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039fd43622a1fb040edd43e69665a9b13858c04309c19199267294eb4b440391`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:7933207bc00e34d61567d17708940cf55fbdf9024bf9275b844752066bf3a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab86686abd597cf5481b0fa80d1e985f48fb084e88499def7641956d790b7c4`

```dockerfile
```

-	Layers:
	-	`sha256:9e9624492ad3851860a903cb1b54533568f8e63d52121cf62b9791813ffd93a7`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 3.5 MB (3490857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b25ee6ea4f7b0bebbd91b452cb891d955f7f1a3a8a232ff85ee2307b4bc457`  
		Last Modified: Tue, 03 Dec 2024 05:16:41 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:0c48036ddb03cbd18386f7f529320a7a0e2734b25bb9ba88a0e233df4afc5465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37547121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35124833f8faaff990215d08ca41e7a9146829090bd1307a8285fd257feb5606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09adcdaa68ad0ae2d20899558c3f5a745b25e4f7a3147b57507237f3055cd6c2`  
		Last Modified: Tue, 03 Dec 2024 02:28:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a56aef9fda16643b9c58f786c1663fc6a3d816d989e5accfdbf56aed63a4a7`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 2.4 MB (2398659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59538036d425f4d12e2486a8cff87ea62676c585f15e5910464313e59d3de722`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 5.9 MB (5941431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a1fc9f74d6f42e965b4e931a11fbfb3665a8cdacbc228205b3cdbe91822f9`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a4c9b924978cc1c82f37096b2d20118fbfaec773c63a43e8067314a07bd15`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:e551622900280eec46f1c61b514ad6b4664e02b6846dcd275b4cced8be7215ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3528594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1395ecc5ee87d10f8b9c5aa41f9924e74a35e1b57193d5162c6474f8dfe1f8c`

```dockerfile
```

-	Layers:
	-	`sha256:d234e5734879287bbe097634d01e71c39a5ebea3c6ce1fdf8daa67d0eb7359c6`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 3.5 MB (3513590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5895c0c664666e98a0ed2b09c7ff8af6e602358ea01bd6b7f3d24f0aabef6a53`  
		Last Modified: Tue, 03 Dec 2024 02:28:23 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:d89a09b29a3053b1374ac6c3b197938d6f41e4c00d5bb716fd65e61d7c97975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d8acb258cdf976c86134a73453ccf189b3ecbe6040145d37d213c14ad71531`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2a37d1c3544aae9cf855e4f9d96754f7d5aad9c9a3f7d42a3eb8987d04b10a`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c3b1191976c7d74198e8e57529daabebefb487799f83eb7d8681422ef72b8`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 1.8 MB (1841107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cc921943a3967383a50f905dd8868956c3ac63ebb385d9cec2f3cb34a9f87e`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 5.8 MB (5803545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a9ead4b058916305bb6fd71d2599865275170bdb57724c307edf3509f326`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9104292331624763e6d460ca187a0f85b64d1f486b86284c07c95592b8e94da1`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:ee8a92a1ad8cafc8ea99877f6bfd0d92dc91949f54b840b48821ce544aa9bcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ab156a72eff661cd8aed8bf33e1b225c9f5f2c967cb69cf1c020b44d53b44d`

```dockerfile
```

-	Layers:
	-	`sha256:2bd3fbc5d440f518558673839c4fcba7382ea6d548360ed2c57eb7bd0f049a65`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:af9aa2f535cd1595cfa92d7a9e52baf705fac7819551f849259d0773385203a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aace15fe89b9da4f600a9dc531bdbd6bfdbee82149b782c4681754cb7adfd303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea3a25e82a899a69e411606c32e2e99cc0bebb8a679bccefad0be4a58d015d4`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23400003f7cda7b1e93301cfb57cd4c14ab11700d2a8411e720e729961ca8793`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 2.6 MB (2582051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870bccfcc5fad8d6168264e4292e8258a936797cdca22d63a6dda98611eca70b`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 6.4 MB (6422809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8e980b29a23356bdaad6be04ee9d07f878e47c102672c0cbbc2267b312662d`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f80a39c99c65ab61038d0a20509912c99a65518b396c1c09707acf50fc8d5a`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:a6878ec5f64bb53eb8e6891d6b618b5a792e5441d9b5627a5dd11c2e2ca2822a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3520397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1d2b0fa2856909177945d356ef69b730ddff9c36c2c34a5e93a6929889faf6`

```dockerfile
```

-	Layers:
	-	`sha256:5604eff1e7ecc0bd947ae823f1b3167b698a8f87776f0c6e4235cd528f7ec68e`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 3.5 MB (3505309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dbe2726dd7d9e40f87c2a680e65ccb9e04ed8903d5fed191be3cda1b1bba5dc`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:d2cafeab26017fb4a71ae998dd67278c21938f2d343faf1c570737a370669452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34335112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accdb2ffdd7ef8b74474fbb9625d5bd5810716173fd63bceae3b2255fdaa34f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a92276bfaeec39377d48fa1d9d6ef0cf51ae7049c547d7685533e2c998d77b`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a574e2d0214b0ef87a172e8eae67d93559e768d57c8fedae3ed1d5052f94f12f`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 2.1 MB (2068742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7f5725ff13ed749dca3faa23df021676986de5acf06a36519c252168cfe204`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 5.4 MB (5385860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950270ac39f6a347c80a61f296057785a32b5bbad62d7ec84ec02283ff7341e0`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74182e1c99dbd232d7b14d0189173e6dffae260bd6ff2706cdbdb26c44734cd`  
		Last Modified: Tue, 03 Dec 2024 03:58:33 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b5476204a34b24daabf7a1a0278ef0469699405add17f0af6a3fd607fe3dc5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3522879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe5894bb3cc6e8b74a32d689d1a60eea531e88e59c6557991a4987932bcbd12`

```dockerfile
```

-	Layers:
	-	`sha256:a51f52d02353a9af8adc8d7d7bc729c68aa8bf64ec65b2ed8b7ec29a6523c842`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 3.5 MB (3507840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e92c71228fbd9a97a10e8b018b2f248e7da88e6978235f40b6c709394d098db`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 15.0 KB (15039 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:e32b4b32ec1bebd57bcef51d51943394d621e20004e559d74d0a5fadbb262fc5
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
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:da6591d15c86f3bf43fab6ccc0035a0650a5756859870abdd3276d24eedff6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8476d53de131526ad9562517c1b099c24ce9385a5730746d1e83247619389c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa88ab9b012a876209b14e6deee5c7982f819f8de6d7b9ed357459d28c597e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdf98d05f4226e17074c09dea718e6191052243811401bf5891cdfb4f1005a`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc53836a810c0768e9eb515600a82be8862a3129239035de56d851625f2890`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 2.2 MB (2170750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd669ab852fa6faffdff5b54301703ace4f36faf005d628470fcef6f3ba9296`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ad710654b9957b395b764e0751fb8ceb335cd3970bee0870c731d0c9d1631`  
		Last Modified: Wed, 13 Nov 2024 01:24:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:35c0217a072785ece237b37268cd30f7410f423b96bd889e56db03a674044795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f8f74486982bdb4f701b16321ebb5b430c4a06622f6960273f474bfbb2188e`

```dockerfile
```

-	Layers:
	-	`sha256:88a28221c4fd9d156a4ebf0935fa189d8524bb92c8fdc1d76981cf7435c2056e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 72.3 KB (72257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28652304d303135a92cbe69570122aaa332626746b8080a921073de8775bb3`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:dc865865e32a1753cf039b2fd22a0fbe795e43cc114a72b47337aead272c579b
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
$ docker pull spiped@sha256:200ec4e93c35786b0d6870d1348514227856fca9fe2081fed0bc6a90674ffa1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37105336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d34473cd812231b18a36f9927a0d1043adfd6ed828e9c24cec15c434e92085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3286318ec16df9127f2df21853581c4604d80ddf277571598ba4d3cd9ba8d06`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5820a96fb11372f32db1517cfd3ecdbbc95268d570014b05d5189ff9059558d6`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 2.4 MB (2401316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aae95d27db2c7f60304b6d4caf995e2a4c87c8eb68e59258480356605069757`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 6.5 MB (6470896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f11f1af366366154b69ba358da0eee393f48cb92cd432045a2871b3b48611be`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2f708db687582ba60d4f0a9cf8b5aef58b41e1c9d1e6b55ab2389f651696e`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:beec0572119e6983b373db1541336a5c6e47d7b97d89d6c6bfffa0e7c1f0abf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3534707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdf0c19de4f5fefe621fd39611d51b7337e0cd0c79de9c1ec1df72eba7bbabe`

```dockerfile
```

-	Layers:
	-	`sha256:1ac30357219ecd62dd514f0204dc7d3d893b8d13cd1e564629343ef671ce54b8`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 3.5 MB (3519667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6b7040b0115ed1adbb45eb11a8af1b412044b9808c156a066992393d6f8a408`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:99bae00cf14c15b697d0d763f1cc2786a8ef3014205f92973feec9c433169295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32891828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b5d8ff57ff5b9caeca8c033884260511a9fce334125f1010083d281d1676aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd5640db7c017698d7b30fd28894a8b9ad8a7bc4a4386d6544c58cbaa52cb1`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2f4c086ad6cb5027d62e957a4520d83274ac2410264bc159ef1f2068b5d9da`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 2.0 MB (1997157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece220a1765f83103e52d02b2549660ea3780a2868d9fbefd43008ae531fb1b3`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 5.1 MB (5138204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33ebf0d87cd479ee5b4538f8cc21c8207e49d820150b1aae450bf7f7bad209a`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5500361841fa5eed10c07a2ad67786591f923b91f16100d8d0747cad187c0946`  
		Last Modified: Tue, 03 Dec 2024 05:23:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:0bda7c1c8df2b5dcc25d961783e13814b4edafecb7ba81e21d5cc9147d1491f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3505295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbed979c8633b9a67ac4b5823932537b1fc4f2c62cd494becd49ff5b75ee12fb`

```dockerfile
```

-	Layers:
	-	`sha256:49f065d55e94a2714b8da791b80846d265d7f186ea2b7de24ed2f309b7d0cc80`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 3.5 MB (3490154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954074d055a2da99643a9a77a1427a0a0f9a3a3e0506fc63528185ad283180b5`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:2673df6c6719abf8451fb416c1ef76ef5beb44dc34d5931c44f45615104395e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30671069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e139c71119fc43443aa86def096eff57086f03c8ef209907a3b59915ee073d7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0b33b4924d962002c20a6328508a5d34d55a2268c73260a6ed9573efce1a3`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43684839a478b9597d614ce8c9c4bd4c7249bb2538a7d3ae859c23a0285fd81f`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 1.9 MB (1855568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0997a5f940d2355e20ffc1ad885efbc15e4958e6505c582aee9fa2cf15255672`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 4.9 MB (4880372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3c4bbaffcc0915aab01140cf0a2cb2b5e2459ce7ecdb12b7bae465cfd7569`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814fda2ba08a0128f768b2977da950819bb0b09b7fae8091289c7d5251fd85b1`  
		Last Modified: Tue, 03 Dec 2024 07:24:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:1825ceb8dbe263a5d3ab65967531abe6affbc02d395158656e2ea44cd219611e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3504787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48421b9da41d41313c82951bb2d6f9bc6dfe713ebd7d92e0c78df51cadbeeb1b`

```dockerfile
```

-	Layers:
	-	`sha256:f14bb418cfb656486fac664f1d6454405450d69c15455e32f8b22d7a5784e86c`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 3.5 MB (3489645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43bb8fca856669ae96e3ce21d76a4ea8f735da4bc5c77d5711090d1eb4c3b7cf`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:237639a6abc6759047cbedc84fa3b66cbd6ccdabe961beff525a31d62f53f2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f274e74e766b46776e29d3fd09d41b620a74f401a213567f1baafcb7c41de3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27124ec490922d03dbb43d024c6ce24f8bf5e4b3fefe0fb0bfb176bbca183b43`  
		Last Modified: Tue, 03 Dec 2024 05:16:41 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec665e61bafba9d4661d86c699686653a61a994d6f8971fa01c63a9cda314d`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 2.2 MB (2247018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccd97308df6bd4ed70f344990461d2dce6a0efcb6ddaf951541e773faef1758`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 5.5 MB (5481125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6434819fb7e89a144affd3b9e3844d3924d854be57d0bf57382b920a90d1599`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039fd43622a1fb040edd43e69665a9b13858c04309c19199267294eb4b440391`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:7933207bc00e34d61567d17708940cf55fbdf9024bf9275b844752066bf3a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab86686abd597cf5481b0fa80d1e985f48fb084e88499def7641956d790b7c4`

```dockerfile
```

-	Layers:
	-	`sha256:9e9624492ad3851860a903cb1b54533568f8e63d52121cf62b9791813ffd93a7`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 3.5 MB (3490857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b25ee6ea4f7b0bebbd91b452cb891d955f7f1a3a8a232ff85ee2307b4bc457`  
		Last Modified: Tue, 03 Dec 2024 05:16:41 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:0c48036ddb03cbd18386f7f529320a7a0e2734b25bb9ba88a0e233df4afc5465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37547121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35124833f8faaff990215d08ca41e7a9146829090bd1307a8285fd257feb5606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09adcdaa68ad0ae2d20899558c3f5a745b25e4f7a3147b57507237f3055cd6c2`  
		Last Modified: Tue, 03 Dec 2024 02:28:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a56aef9fda16643b9c58f786c1663fc6a3d816d989e5accfdbf56aed63a4a7`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 2.4 MB (2398659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59538036d425f4d12e2486a8cff87ea62676c585f15e5910464313e59d3de722`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 5.9 MB (5941431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a1fc9f74d6f42e965b4e931a11fbfb3665a8cdacbc228205b3cdbe91822f9`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a4c9b924978cc1c82f37096b2d20118fbfaec773c63a43e8067314a07bd15`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:e551622900280eec46f1c61b514ad6b4664e02b6846dcd275b4cced8be7215ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3528594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1395ecc5ee87d10f8b9c5aa41f9924e74a35e1b57193d5162c6474f8dfe1f8c`

```dockerfile
```

-	Layers:
	-	`sha256:d234e5734879287bbe097634d01e71c39a5ebea3c6ce1fdf8daa67d0eb7359c6`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 3.5 MB (3513590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5895c0c664666e98a0ed2b09c7ff8af6e602358ea01bd6b7f3d24f0aabef6a53`  
		Last Modified: Tue, 03 Dec 2024 02:28:23 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:d89a09b29a3053b1374ac6c3b197938d6f41e4c00d5bb716fd65e61d7c97975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d8acb258cdf976c86134a73453ccf189b3ecbe6040145d37d213c14ad71531`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2a37d1c3544aae9cf855e4f9d96754f7d5aad9c9a3f7d42a3eb8987d04b10a`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c3b1191976c7d74198e8e57529daabebefb487799f83eb7d8681422ef72b8`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 1.8 MB (1841107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cc921943a3967383a50f905dd8868956c3ac63ebb385d9cec2f3cb34a9f87e`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 5.8 MB (5803545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a9ead4b058916305bb6fd71d2599865275170bdb57724c307edf3509f326`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9104292331624763e6d460ca187a0f85b64d1f486b86284c07c95592b8e94da1`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:ee8a92a1ad8cafc8ea99877f6bfd0d92dc91949f54b840b48821ce544aa9bcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ab156a72eff661cd8aed8bf33e1b225c9f5f2c967cb69cf1c020b44d53b44d`

```dockerfile
```

-	Layers:
	-	`sha256:2bd3fbc5d440f518558673839c4fcba7382ea6d548360ed2c57eb7bd0f049a65`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:af9aa2f535cd1595cfa92d7a9e52baf705fac7819551f849259d0773385203a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aace15fe89b9da4f600a9dc531bdbd6bfdbee82149b782c4681754cb7adfd303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea3a25e82a899a69e411606c32e2e99cc0bebb8a679bccefad0be4a58d015d4`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23400003f7cda7b1e93301cfb57cd4c14ab11700d2a8411e720e729961ca8793`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 2.6 MB (2582051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870bccfcc5fad8d6168264e4292e8258a936797cdca22d63a6dda98611eca70b`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 6.4 MB (6422809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8e980b29a23356bdaad6be04ee9d07f878e47c102672c0cbbc2267b312662d`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f80a39c99c65ab61038d0a20509912c99a65518b396c1c09707acf50fc8d5a`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:a6878ec5f64bb53eb8e6891d6b618b5a792e5441d9b5627a5dd11c2e2ca2822a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3520397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1d2b0fa2856909177945d356ef69b730ddff9c36c2c34a5e93a6929889faf6`

```dockerfile
```

-	Layers:
	-	`sha256:5604eff1e7ecc0bd947ae823f1b3167b698a8f87776f0c6e4235cd528f7ec68e`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 3.5 MB (3505309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dbe2726dd7d9e40f87c2a680e65ccb9e04ed8903d5fed191be3cda1b1bba5dc`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:d2cafeab26017fb4a71ae998dd67278c21938f2d343faf1c570737a370669452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34335112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accdb2ffdd7ef8b74474fbb9625d5bd5810716173fd63bceae3b2255fdaa34f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a92276bfaeec39377d48fa1d9d6ef0cf51ae7049c547d7685533e2c998d77b`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a574e2d0214b0ef87a172e8eae67d93559e768d57c8fedae3ed1d5052f94f12f`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 2.1 MB (2068742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7f5725ff13ed749dca3faa23df021676986de5acf06a36519c252168cfe204`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 5.4 MB (5385860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950270ac39f6a347c80a61f296057785a32b5bbad62d7ec84ec02283ff7341e0`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74182e1c99dbd232d7b14d0189173e6dffae260bd6ff2706cdbdb26c44734cd`  
		Last Modified: Tue, 03 Dec 2024 03:58:33 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b5476204a34b24daabf7a1a0278ef0469699405add17f0af6a3fd607fe3dc5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3522879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe5894bb3cc6e8b74a32d689d1a60eea531e88e59c6557991a4987932bcbd12`

```dockerfile
```

-	Layers:
	-	`sha256:a51f52d02353a9af8adc8d7d7bc729c68aa8bf64ec65b2ed8b7ec29a6523c842`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 3.5 MB (3507840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e92c71228fbd9a97a10e8b018b2f248e7da88e6978235f40b6c709394d098db`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 15.0 KB (15039 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:e32b4b32ec1bebd57bcef51d51943394d621e20004e559d74d0a5fadbb262fc5
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
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:da6591d15c86f3bf43fab6ccc0035a0650a5756859870abdd3276d24eedff6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8476d53de131526ad9562517c1b099c24ce9385a5730746d1e83247619389c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa88ab9b012a876209b14e6deee5c7982f819f8de6d7b9ed357459d28c597e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdf98d05f4226e17074c09dea718e6191052243811401bf5891cdfb4f1005a`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc53836a810c0768e9eb515600a82be8862a3129239035de56d851625f2890`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 2.2 MB (2170750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd669ab852fa6faffdff5b54301703ace4f36faf005d628470fcef6f3ba9296`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ad710654b9957b395b764e0751fb8ceb335cd3970bee0870c731d0c9d1631`  
		Last Modified: Wed, 13 Nov 2024 01:24:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:35c0217a072785ece237b37268cd30f7410f423b96bd889e56db03a674044795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f8f74486982bdb4f701b16321ebb5b430c4a06622f6960273f474bfbb2188e`

```dockerfile
```

-	Layers:
	-	`sha256:88a28221c4fd9d156a4ebf0935fa189d8524bb92c8fdc1d76981cf7435c2056e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 72.3 KB (72257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28652304d303135a92cbe69570122aaa332626746b8080a921073de8775bb3`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:dc865865e32a1753cf039b2fd22a0fbe795e43cc114a72b47337aead272c579b
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

### `spiped:1.6.2` - linux; amd64

```console
$ docker pull spiped@sha256:200ec4e93c35786b0d6870d1348514227856fca9fe2081fed0bc6a90674ffa1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37105336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d34473cd812231b18a36f9927a0d1043adfd6ed828e9c24cec15c434e92085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3286318ec16df9127f2df21853581c4604d80ddf277571598ba4d3cd9ba8d06`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5820a96fb11372f32db1517cfd3ecdbbc95268d570014b05d5189ff9059558d6`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 2.4 MB (2401316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aae95d27db2c7f60304b6d4caf995e2a4c87c8eb68e59258480356605069757`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 6.5 MB (6470896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f11f1af366366154b69ba358da0eee393f48cb92cd432045a2871b3b48611be`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2f708db687582ba60d4f0a9cf8b5aef58b41e1c9d1e6b55ab2389f651696e`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:beec0572119e6983b373db1541336a5c6e47d7b97d89d6c6bfffa0e7c1f0abf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3534707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdf0c19de4f5fefe621fd39611d51b7337e0cd0c79de9c1ec1df72eba7bbabe`

```dockerfile
```

-	Layers:
	-	`sha256:1ac30357219ecd62dd514f0204dc7d3d893b8d13cd1e564629343ef671ce54b8`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 3.5 MB (3519667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6b7040b0115ed1adbb45eb11a8af1b412044b9808c156a066992393d6f8a408`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:99bae00cf14c15b697d0d763f1cc2786a8ef3014205f92973feec9c433169295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32891828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b5d8ff57ff5b9caeca8c033884260511a9fce334125f1010083d281d1676aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd5640db7c017698d7b30fd28894a8b9ad8a7bc4a4386d6544c58cbaa52cb1`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2f4c086ad6cb5027d62e957a4520d83274ac2410264bc159ef1f2068b5d9da`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 2.0 MB (1997157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece220a1765f83103e52d02b2549660ea3780a2868d9fbefd43008ae531fb1b3`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 5.1 MB (5138204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33ebf0d87cd479ee5b4538f8cc21c8207e49d820150b1aae450bf7f7bad209a`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5500361841fa5eed10c07a2ad67786591f923b91f16100d8d0747cad187c0946`  
		Last Modified: Tue, 03 Dec 2024 05:23:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:0bda7c1c8df2b5dcc25d961783e13814b4edafecb7ba81e21d5cc9147d1491f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3505295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbed979c8633b9a67ac4b5823932537b1fc4f2c62cd494becd49ff5b75ee12fb`

```dockerfile
```

-	Layers:
	-	`sha256:49f065d55e94a2714b8da791b80846d265d7f186ea2b7de24ed2f309b7d0cc80`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 3.5 MB (3490154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954074d055a2da99643a9a77a1427a0a0f9a3a3e0506fc63528185ad283180b5`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:2673df6c6719abf8451fb416c1ef76ef5beb44dc34d5931c44f45615104395e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30671069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e139c71119fc43443aa86def096eff57086f03c8ef209907a3b59915ee073d7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0b33b4924d962002c20a6328508a5d34d55a2268c73260a6ed9573efce1a3`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43684839a478b9597d614ce8c9c4bd4c7249bb2538a7d3ae859c23a0285fd81f`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 1.9 MB (1855568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0997a5f940d2355e20ffc1ad885efbc15e4958e6505c582aee9fa2cf15255672`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 4.9 MB (4880372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3c4bbaffcc0915aab01140cf0a2cb2b5e2459ce7ecdb12b7bae465cfd7569`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814fda2ba08a0128f768b2977da950819bb0b09b7fae8091289c7d5251fd85b1`  
		Last Modified: Tue, 03 Dec 2024 07:24:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:1825ceb8dbe263a5d3ab65967531abe6affbc02d395158656e2ea44cd219611e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3504787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48421b9da41d41313c82951bb2d6f9bc6dfe713ebd7d92e0c78df51cadbeeb1b`

```dockerfile
```

-	Layers:
	-	`sha256:f14bb418cfb656486fac664f1d6454405450d69c15455e32f8b22d7a5784e86c`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 3.5 MB (3489645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43bb8fca856669ae96e3ce21d76a4ea8f735da4bc5c77d5711090d1eb4c3b7cf`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:237639a6abc6759047cbedc84fa3b66cbd6ccdabe961beff525a31d62f53f2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f274e74e766b46776e29d3fd09d41b620a74f401a213567f1baafcb7c41de3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27124ec490922d03dbb43d024c6ce24f8bf5e4b3fefe0fb0bfb176bbca183b43`  
		Last Modified: Tue, 03 Dec 2024 05:16:41 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec665e61bafba9d4661d86c699686653a61a994d6f8971fa01c63a9cda314d`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 2.2 MB (2247018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccd97308df6bd4ed70f344990461d2dce6a0efcb6ddaf951541e773faef1758`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 5.5 MB (5481125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6434819fb7e89a144affd3b9e3844d3924d854be57d0bf57382b920a90d1599`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039fd43622a1fb040edd43e69665a9b13858c04309c19199267294eb4b440391`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:7933207bc00e34d61567d17708940cf55fbdf9024bf9275b844752066bf3a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab86686abd597cf5481b0fa80d1e985f48fb084e88499def7641956d790b7c4`

```dockerfile
```

-	Layers:
	-	`sha256:9e9624492ad3851860a903cb1b54533568f8e63d52121cf62b9791813ffd93a7`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 3.5 MB (3490857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b25ee6ea4f7b0bebbd91b452cb891d955f7f1a3a8a232ff85ee2307b4bc457`  
		Last Modified: Tue, 03 Dec 2024 05:16:41 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:0c48036ddb03cbd18386f7f529320a7a0e2734b25bb9ba88a0e233df4afc5465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37547121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35124833f8faaff990215d08ca41e7a9146829090bd1307a8285fd257feb5606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09adcdaa68ad0ae2d20899558c3f5a745b25e4f7a3147b57507237f3055cd6c2`  
		Last Modified: Tue, 03 Dec 2024 02:28:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a56aef9fda16643b9c58f786c1663fc6a3d816d989e5accfdbf56aed63a4a7`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 2.4 MB (2398659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59538036d425f4d12e2486a8cff87ea62676c585f15e5910464313e59d3de722`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 5.9 MB (5941431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a1fc9f74d6f42e965b4e931a11fbfb3665a8cdacbc228205b3cdbe91822f9`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a4c9b924978cc1c82f37096b2d20118fbfaec773c63a43e8067314a07bd15`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:e551622900280eec46f1c61b514ad6b4664e02b6846dcd275b4cced8be7215ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3528594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1395ecc5ee87d10f8b9c5aa41f9924e74a35e1b57193d5162c6474f8dfe1f8c`

```dockerfile
```

-	Layers:
	-	`sha256:d234e5734879287bbe097634d01e71c39a5ebea3c6ce1fdf8daa67d0eb7359c6`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 3.5 MB (3513590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5895c0c664666e98a0ed2b09c7ff8af6e602358ea01bd6b7f3d24f0aabef6a53`  
		Last Modified: Tue, 03 Dec 2024 02:28:23 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:d89a09b29a3053b1374ac6c3b197938d6f41e4c00d5bb716fd65e61d7c97975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d8acb258cdf976c86134a73453ccf189b3ecbe6040145d37d213c14ad71531`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2a37d1c3544aae9cf855e4f9d96754f7d5aad9c9a3f7d42a3eb8987d04b10a`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c3b1191976c7d74198e8e57529daabebefb487799f83eb7d8681422ef72b8`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 1.8 MB (1841107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cc921943a3967383a50f905dd8868956c3ac63ebb385d9cec2f3cb34a9f87e`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 5.8 MB (5803545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a9ead4b058916305bb6fd71d2599865275170bdb57724c307edf3509f326`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9104292331624763e6d460ca187a0f85b64d1f486b86284c07c95592b8e94da1`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:ee8a92a1ad8cafc8ea99877f6bfd0d92dc91949f54b840b48821ce544aa9bcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ab156a72eff661cd8aed8bf33e1b225c9f5f2c967cb69cf1c020b44d53b44d`

```dockerfile
```

-	Layers:
	-	`sha256:2bd3fbc5d440f518558673839c4fcba7382ea6d548360ed2c57eb7bd0f049a65`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:af9aa2f535cd1595cfa92d7a9e52baf705fac7819551f849259d0773385203a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aace15fe89b9da4f600a9dc531bdbd6bfdbee82149b782c4681754cb7adfd303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea3a25e82a899a69e411606c32e2e99cc0bebb8a679bccefad0be4a58d015d4`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23400003f7cda7b1e93301cfb57cd4c14ab11700d2a8411e720e729961ca8793`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 2.6 MB (2582051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870bccfcc5fad8d6168264e4292e8258a936797cdca22d63a6dda98611eca70b`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 6.4 MB (6422809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8e980b29a23356bdaad6be04ee9d07f878e47c102672c0cbbc2267b312662d`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f80a39c99c65ab61038d0a20509912c99a65518b396c1c09707acf50fc8d5a`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:a6878ec5f64bb53eb8e6891d6b618b5a792e5441d9b5627a5dd11c2e2ca2822a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3520397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1d2b0fa2856909177945d356ef69b730ddff9c36c2c34a5e93a6929889faf6`

```dockerfile
```

-	Layers:
	-	`sha256:5604eff1e7ecc0bd947ae823f1b3167b698a8f87776f0c6e4235cd528f7ec68e`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 3.5 MB (3505309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dbe2726dd7d9e40f87c2a680e65ccb9e04ed8903d5fed191be3cda1b1bba5dc`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:d2cafeab26017fb4a71ae998dd67278c21938f2d343faf1c570737a370669452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34335112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accdb2ffdd7ef8b74474fbb9625d5bd5810716173fd63bceae3b2255fdaa34f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a92276bfaeec39377d48fa1d9d6ef0cf51ae7049c547d7685533e2c998d77b`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a574e2d0214b0ef87a172e8eae67d93559e768d57c8fedae3ed1d5052f94f12f`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 2.1 MB (2068742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7f5725ff13ed749dca3faa23df021676986de5acf06a36519c252168cfe204`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 5.4 MB (5385860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950270ac39f6a347c80a61f296057785a32b5bbad62d7ec84ec02283ff7341e0`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74182e1c99dbd232d7b14d0189173e6dffae260bd6ff2706cdbdb26c44734cd`  
		Last Modified: Tue, 03 Dec 2024 03:58:33 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:b5476204a34b24daabf7a1a0278ef0469699405add17f0af6a3fd607fe3dc5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3522879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe5894bb3cc6e8b74a32d689d1a60eea531e88e59c6557991a4987932bcbd12`

```dockerfile
```

-	Layers:
	-	`sha256:a51f52d02353a9af8adc8d7d7bc729c68aa8bf64ec65b2ed8b7ec29a6523c842`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 3.5 MB (3507840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e92c71228fbd9a97a10e8b018b2f248e7da88e6978235f40b6c709394d098db`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 15.0 KB (15039 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:e32b4b32ec1bebd57bcef51d51943394d621e20004e559d74d0a5fadbb262fc5
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

### `spiped:1.6.2-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:da6591d15c86f3bf43fab6ccc0035a0650a5756859870abdd3276d24eedff6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8476d53de131526ad9562517c1b099c24ce9385a5730746d1e83247619389c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa88ab9b012a876209b14e6deee5c7982f819f8de6d7b9ed357459d28c597e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdf98d05f4226e17074c09dea718e6191052243811401bf5891cdfb4f1005a`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc53836a810c0768e9eb515600a82be8862a3129239035de56d851625f2890`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 2.2 MB (2170750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd669ab852fa6faffdff5b54301703ace4f36faf005d628470fcef6f3ba9296`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ad710654b9957b395b764e0751fb8ceb335cd3970bee0870c731d0c9d1631`  
		Last Modified: Wed, 13 Nov 2024 01:24:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:35c0217a072785ece237b37268cd30f7410f423b96bd889e56db03a674044795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f8f74486982bdb4f701b16321ebb5b430c4a06622f6960273f474bfbb2188e`

```dockerfile
```

-	Layers:
	-	`sha256:88a28221c4fd9d156a4ebf0935fa189d8524bb92c8fdc1d76981cf7435c2056e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 72.3 KB (72257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28652304d303135a92cbe69570122aaa332626746b8080a921073de8775bb3`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:e32b4b32ec1bebd57bcef51d51943394d621e20004e559d74d0a5fadbb262fc5
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
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:da6591d15c86f3bf43fab6ccc0035a0650a5756859870abdd3276d24eedff6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8476d53de131526ad9562517c1b099c24ce9385a5730746d1e83247619389c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa88ab9b012a876209b14e6deee5c7982f819f8de6d7b9ed357459d28c597e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdf98d05f4226e17074c09dea718e6191052243811401bf5891cdfb4f1005a`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc53836a810c0768e9eb515600a82be8862a3129239035de56d851625f2890`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 2.2 MB (2170750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd669ab852fa6faffdff5b54301703ace4f36faf005d628470fcef6f3ba9296`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ad710654b9957b395b764e0751fb8ceb335cd3970bee0870c731d0c9d1631`  
		Last Modified: Wed, 13 Nov 2024 01:24:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:35c0217a072785ece237b37268cd30f7410f423b96bd889e56db03a674044795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f8f74486982bdb4f701b16321ebb5b430c4a06622f6960273f474bfbb2188e`

```dockerfile
```

-	Layers:
	-	`sha256:88a28221c4fd9d156a4ebf0935fa189d8524bb92c8fdc1d76981cf7435c2056e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 72.3 KB (72257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28652304d303135a92cbe69570122aaa332626746b8080a921073de8775bb3`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:dc865865e32a1753cf039b2fd22a0fbe795e43cc114a72b47337aead272c579b
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
$ docker pull spiped@sha256:200ec4e93c35786b0d6870d1348514227856fca9fe2081fed0bc6a90674ffa1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37105336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d34473cd812231b18a36f9927a0d1043adfd6ed828e9c24cec15c434e92085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3286318ec16df9127f2df21853581c4604d80ddf277571598ba4d3cd9ba8d06`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5820a96fb11372f32db1517cfd3ecdbbc95268d570014b05d5189ff9059558d6`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 2.4 MB (2401316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aae95d27db2c7f60304b6d4caf995e2a4c87c8eb68e59258480356605069757`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 6.5 MB (6470896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f11f1af366366154b69ba358da0eee393f48cb92cd432045a2871b3b48611be`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2f708db687582ba60d4f0a9cf8b5aef58b41e1c9d1e6b55ab2389f651696e`  
		Last Modified: Tue, 03 Dec 2024 02:15:23 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:beec0572119e6983b373db1541336a5c6e47d7b97d89d6c6bfffa0e7c1f0abf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3534707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdf0c19de4f5fefe621fd39611d51b7337e0cd0c79de9c1ec1df72eba7bbabe`

```dockerfile
```

-	Layers:
	-	`sha256:1ac30357219ecd62dd514f0204dc7d3d893b8d13cd1e564629343ef671ce54b8`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 3.5 MB (3519667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6b7040b0115ed1adbb45eb11a8af1b412044b9808c156a066992393d6f8a408`  
		Last Modified: Tue, 03 Dec 2024 02:15:22 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:99bae00cf14c15b697d0d763f1cc2786a8ef3014205f92973feec9c433169295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32891828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b5d8ff57ff5b9caeca8c033884260511a9fce334125f1010083d281d1676aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd5640db7c017698d7b30fd28894a8b9ad8a7bc4a4386d6544c58cbaa52cb1`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2f4c086ad6cb5027d62e957a4520d83274ac2410264bc159ef1f2068b5d9da`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 2.0 MB (1997157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece220a1765f83103e52d02b2549660ea3780a2868d9fbefd43008ae531fb1b3`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 5.1 MB (5138204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33ebf0d87cd479ee5b4538f8cc21c8207e49d820150b1aae450bf7f7bad209a`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5500361841fa5eed10c07a2ad67786591f923b91f16100d8d0747cad187c0946`  
		Last Modified: Tue, 03 Dec 2024 05:23:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:0bda7c1c8df2b5dcc25d961783e13814b4edafecb7ba81e21d5cc9147d1491f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3505295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbed979c8633b9a67ac4b5823932537b1fc4f2c62cd494becd49ff5b75ee12fb`

```dockerfile
```

-	Layers:
	-	`sha256:49f065d55e94a2714b8da791b80846d265d7f186ea2b7de24ed2f309b7d0cc80`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 3.5 MB (3490154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954074d055a2da99643a9a77a1427a0a0f9a3a3e0506fc63528185ad283180b5`  
		Last Modified: Tue, 03 Dec 2024 05:23:07 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:2673df6c6719abf8451fb416c1ef76ef5beb44dc34d5931c44f45615104395e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30671069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e139c71119fc43443aa86def096eff57086f03c8ef209907a3b59915ee073d7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0b33b4924d962002c20a6328508a5d34d55a2268c73260a6ed9573efce1a3`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43684839a478b9597d614ce8c9c4bd4c7249bb2538a7d3ae859c23a0285fd81f`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 1.9 MB (1855568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0997a5f940d2355e20ffc1ad885efbc15e4958e6505c582aee9fa2cf15255672`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 4.9 MB (4880372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3c4bbaffcc0915aab01140cf0a2cb2b5e2459ce7ecdb12b7bae465cfd7569`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814fda2ba08a0128f768b2977da950819bb0b09b7fae8091289c7d5251fd85b1`  
		Last Modified: Tue, 03 Dec 2024 07:24:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:1825ceb8dbe263a5d3ab65967531abe6affbc02d395158656e2ea44cd219611e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3504787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48421b9da41d41313c82951bb2d6f9bc6dfe713ebd7d92e0c78df51cadbeeb1b`

```dockerfile
```

-	Layers:
	-	`sha256:f14bb418cfb656486fac664f1d6454405450d69c15455e32f8b22d7a5784e86c`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 3.5 MB (3489645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43bb8fca856669ae96e3ce21d76a4ea8f735da4bc5c77d5711090d1eb4c3b7cf`  
		Last Modified: Tue, 03 Dec 2024 07:24:41 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:237639a6abc6759047cbedc84fa3b66cbd6ccdabe961beff525a31d62f53f2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f274e74e766b46776e29d3fd09d41b620a74f401a213567f1baafcb7c41de3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27124ec490922d03dbb43d024c6ce24f8bf5e4b3fefe0fb0bfb176bbca183b43`  
		Last Modified: Tue, 03 Dec 2024 05:16:41 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec665e61bafba9d4661d86c699686653a61a994d6f8971fa01c63a9cda314d`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 2.2 MB (2247018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccd97308df6bd4ed70f344990461d2dce6a0efcb6ddaf951541e773faef1758`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 5.5 MB (5481125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6434819fb7e89a144affd3b9e3844d3924d854be57d0bf57382b920a90d1599`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039fd43622a1fb040edd43e69665a9b13858c04309c19199267294eb4b440391`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:7933207bc00e34d61567d17708940cf55fbdf9024bf9275b844752066bf3a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab86686abd597cf5481b0fa80d1e985f48fb084e88499def7641956d790b7c4`

```dockerfile
```

-	Layers:
	-	`sha256:9e9624492ad3851860a903cb1b54533568f8e63d52121cf62b9791813ffd93a7`  
		Last Modified: Tue, 03 Dec 2024 05:16:42 GMT  
		Size: 3.5 MB (3490857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b25ee6ea4f7b0bebbd91b452cb891d955f7f1a3a8a232ff85ee2307b4bc457`  
		Last Modified: Tue, 03 Dec 2024 05:16:41 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:0c48036ddb03cbd18386f7f529320a7a0e2734b25bb9ba88a0e233df4afc5465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37547121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35124833f8faaff990215d08ca41e7a9146829090bd1307a8285fd257feb5606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09adcdaa68ad0ae2d20899558c3f5a745b25e4f7a3147b57507237f3055cd6c2`  
		Last Modified: Tue, 03 Dec 2024 02:28:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a56aef9fda16643b9c58f786c1663fc6a3d816d989e5accfdbf56aed63a4a7`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 2.4 MB (2398659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59538036d425f4d12e2486a8cff87ea62676c585f15e5910464313e59d3de722`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 5.9 MB (5941431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a1fc9f74d6f42e965b4e931a11fbfb3665a8cdacbc228205b3cdbe91822f9`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a4c9b924978cc1c82f37096b2d20118fbfaec773c63a43e8067314a07bd15`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:e551622900280eec46f1c61b514ad6b4664e02b6846dcd275b4cced8be7215ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3528594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1395ecc5ee87d10f8b9c5aa41f9924e74a35e1b57193d5162c6474f8dfe1f8c`

```dockerfile
```

-	Layers:
	-	`sha256:d234e5734879287bbe097634d01e71c39a5ebea3c6ce1fdf8daa67d0eb7359c6`  
		Last Modified: Tue, 03 Dec 2024 02:28:24 GMT  
		Size: 3.5 MB (3513590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5895c0c664666e98a0ed2b09c7ff8af6e602358ea01bd6b7f3d24f0aabef6a53`  
		Last Modified: Tue, 03 Dec 2024 02:28:23 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:d89a09b29a3053b1374ac6c3b197938d6f41e4c00d5bb716fd65e61d7c97975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d8acb258cdf976c86134a73453ccf189b3ecbe6040145d37d213c14ad71531`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2a37d1c3544aae9cf855e4f9d96754f7d5aad9c9a3f7d42a3eb8987d04b10a`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c3b1191976c7d74198e8e57529daabebefb487799f83eb7d8681422ef72b8`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 1.8 MB (1841107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cc921943a3967383a50f905dd8868956c3ac63ebb385d9cec2f3cb34a9f87e`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 5.8 MB (5803545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a9ead4b058916305bb6fd71d2599865275170bdb57724c307edf3509f326`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9104292331624763e6d460ca187a0f85b64d1f486b86284c07c95592b8e94da1`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ee8a92a1ad8cafc8ea99877f6bfd0d92dc91949f54b840b48821ce544aa9bcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ab156a72eff661cd8aed8bf33e1b225c9f5f2c967cb69cf1c020b44d53b44d`

```dockerfile
```

-	Layers:
	-	`sha256:2bd3fbc5d440f518558673839c4fcba7382ea6d548360ed2c57eb7bd0f049a65`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:af9aa2f535cd1595cfa92d7a9e52baf705fac7819551f849259d0773385203a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aace15fe89b9da4f600a9dc531bdbd6bfdbee82149b782c4681754cb7adfd303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea3a25e82a899a69e411606c32e2e99cc0bebb8a679bccefad0be4a58d015d4`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23400003f7cda7b1e93301cfb57cd4c14ab11700d2a8411e720e729961ca8793`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 2.6 MB (2582051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870bccfcc5fad8d6168264e4292e8258a936797cdca22d63a6dda98611eca70b`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 6.4 MB (6422809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8e980b29a23356bdaad6be04ee9d07f878e47c102672c0cbbc2267b312662d`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f80a39c99c65ab61038d0a20509912c99a65518b396c1c09707acf50fc8d5a`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:a6878ec5f64bb53eb8e6891d6b618b5a792e5441d9b5627a5dd11c2e2ca2822a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3520397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1d2b0fa2856909177945d356ef69b730ddff9c36c2c34a5e93a6929889faf6`

```dockerfile
```

-	Layers:
	-	`sha256:5604eff1e7ecc0bd947ae823f1b3167b698a8f87776f0c6e4235cd528f7ec68e`  
		Last Modified: Tue, 03 Dec 2024 04:27:12 GMT  
		Size: 3.5 MB (3505309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dbe2726dd7d9e40f87c2a680e65ccb9e04ed8903d5fed191be3cda1b1bba5dc`  
		Last Modified: Tue, 03 Dec 2024 04:27:11 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:d2cafeab26017fb4a71ae998dd67278c21938f2d343faf1c570737a370669452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34335112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accdb2ffdd7ef8b74474fbb9625d5bd5810716173fd63bceae3b2255fdaa34f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a92276bfaeec39377d48fa1d9d6ef0cf51ae7049c547d7685533e2c998d77b`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a574e2d0214b0ef87a172e8eae67d93559e768d57c8fedae3ed1d5052f94f12f`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 2.1 MB (2068742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7f5725ff13ed749dca3faa23df021676986de5acf06a36519c252168cfe204`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 5.4 MB (5385860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950270ac39f6a347c80a61f296057785a32b5bbad62d7ec84ec02283ff7341e0`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74182e1c99dbd232d7b14d0189173e6dffae260bd6ff2706cdbdb26c44734cd`  
		Last Modified: Tue, 03 Dec 2024 03:58:33 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b5476204a34b24daabf7a1a0278ef0469699405add17f0af6a3fd607fe3dc5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3522879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe5894bb3cc6e8b74a32d689d1a60eea531e88e59c6557991a4987932bcbd12`

```dockerfile
```

-	Layers:
	-	`sha256:a51f52d02353a9af8adc8d7d7bc729c68aa8bf64ec65b2ed8b7ec29a6523c842`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 3.5 MB (3507840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e92c71228fbd9a97a10e8b018b2f248e7da88e6978235f40b6c709394d098db`  
		Last Modified: Tue, 03 Dec 2024 03:58:32 GMT  
		Size: 15.0 KB (15039 bytes)  
		MIME: application/vnd.in-toto+json
