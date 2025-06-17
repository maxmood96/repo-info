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
$ docker pull spiped@sha256:b83df7863588b91b6f69e3fb3476e144c4036c90beaac879e9b04f38fc10a7d5
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
$ docker pull spiped@sha256:a5d4dfe0765417cab49f9c8c81905d94b3bbd8d80bb5b1cb47df0e8668a5e4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37092818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f736b6abf32c93830c88ccb720707ddabf04bfe77052c4e4fa32800066b420b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901060e6b8a7884c01efa6270dd3f90d3843ac68e684337d24de3ca84decb99d`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5b73802790441257b5f7e4dd01f56a8f25141dbd7f471a01967e3667ce61b9`  
		Last Modified: Tue, 10 Jun 2025 23:36:25 GMT  
		Size: 2.4 MB (2402195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4e093b3597052dc43e0db358fa01a1b0d418b22dcaaad8b58366b2aa6d5460`  
		Last Modified: Tue, 10 Jun 2025 23:36:25 GMT  
		Size: 6.5 MB (6458953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff5c6f0cf05be8aeb9731139b2c42db7bd0b95a6cb4498ce4c5472915a2ebfb`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caafbfe845e21d65a68ad3391d7abb7e582c3d476b6e13e0d0602457089d379`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:00b0ab8f2820c628fd250eb63cc4cd938175c4341dd502243dddbbaa8076f425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cc64ebe1bc3ddec01febd10d49f5640f8f00e405e04e89be5111e6b11854ad`

```dockerfile
```

-	Layers:
	-	`sha256:5958f2544848781ee234867326e5230742d46d3d70e9ed6dacb5f2522e51420e`  
		Last Modified: Wed, 11 Jun 2025 01:04:24 GMT  
		Size: 3.6 MB (3631793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215a4c084e1c1c9d1bfb431aa3ee606276bbabbc814c065cd4e53f4268fed4c7`  
		Last Modified: Wed, 11 Jun 2025 01:04:25 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b049c3c815392540b5a67b398586d60aef642c918e6744f0f9e87839825c571d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b19d93be75f680289976bc19c584f7ffdf835c910772406637fefe166cb3246`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1052a6a8cb6216f507d9ebf741e442e35734ac86617a8bb1ce8aeb6378eb702b`  
		Last Modified: Wed, 11 Jun 2025 03:11:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55c33e57388de6005641bb68d8036264a16fc700c43545e0e780e7e5a3a7187`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 2.0 MB (1998289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ba223a0b28036e632aca948791e7ea0ec2ea20ed64c3658681f69e9b80161`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 5.1 MB (5147777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85477c497bb56282915ec3bde6c516852dea4c471c76d294e4b07cda81a5609d`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92173adb4d90fe4f7c0a5b937ff3cafa90326106208c7c4e16e5dc0d8ce91e10`  
		Last Modified: Wed, 11 Jun 2025 03:11:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:dbf4c17085fcb424ad33b6f2698c9d69610edb46f2916f0fde1ce11fb7f2726c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f1871eb04d3f1f6cea6f92f3f51c2e8f77f41b680f661b54c5356b19c0a574`

```dockerfile
```

-	Layers:
	-	`sha256:4314f998c143791479147c72437ceca0c9358e305b914e1cf764a95b6d17d972`  
		Last Modified: Wed, 11 Jun 2025 07:04:29 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e986205c455de4b0e54eeec2f42c4936ef395a37b1a511a9e819185f34c32561`  
		Last Modified: Wed, 11 Jun 2025 07:04:30 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9ce1fc0dc2d1f996039a56a7cfbd378133b51755333301f848efca7a7fad5776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1921127603a2388cd25100dc1a40dd4a882e503c99c18a1c94affea6d8318c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b3efe4f51fb3f46017d32a189e76502c05ebbe62a4f3734f609d087648aef`  
		Last Modified: Wed, 11 Jun 2025 04:49:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ddb002179312e93532c834e5a8082a2d73feda8078b2ce73b951b3e45020d`  
		Last Modified: Wed, 11 Jun 2025 04:49:06 GMT  
		Size: 1.9 MB (1856413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714ec40b518a9456e36344a7732ddbd1daf761542ba21f6350a63ed6f652917a`  
		Last Modified: Wed, 11 Jun 2025 04:49:18 GMT  
		Size: 4.9 MB (4888712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c379236ab7a7ce88d18f78e77b41389fcef6e28730401b67ed4d35afb95ed2c2`  
		Last Modified: Wed, 11 Jun 2025 04:51:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5150130b703fde6b91fc459f573bafe2bd5048ddab660d82204dc88bc8ff26c7`  
		Last Modified: Wed, 11 Jun 2025 04:51:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:f1d93a3b47e53aefe111a468b535741ebf3c44b479196c920c1131ae3945be4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe8b73dbdca091b6a3cfc7fc1cbe516b479f8cf66cfb32973f1c08f4f92467b`

```dockerfile
```

-	Layers:
	-	`sha256:e11d0f6c12be4f061b56a863eadca9d24cba81ade81668d540c29d14815dca80`  
		Last Modified: Wed, 11 Jun 2025 07:04:34 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7398098987796bea294105e7389cac1c9b15dc4f47d3389c2ad39ad6daced0f`  
		Last Modified: Wed, 11 Jun 2025 07:04:35 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b5143746337b9bac98b518650f2e9ed5b4b9886eabd460426ceb3de5ec9f386b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35818470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37585eab662d0b615e056a5ef9795b640ce9a89a931957d10ef73e596f21268b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f876cc248b0c7ec91a68879fb0ecc212568f3e4a637e295be916be6edeeb8`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd86f82bcea91f9ced30eff144ee24770b00b7f2c177420dbd9ac9b49a43079d`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 2.2 MB (2247471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df866991bdf5e32b6e9c1f1eb9720415e874e95be0247c4694eff05e37ca98b3`  
		Last Modified: Wed, 11 Jun 2025 02:35:32 GMT  
		Size: 5.5 MB (5491782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68a815d97977aedeb7c8399fd91c72bd238a307f23708808c8a427312e4eb47`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bb490ebf89b9d37cf331e0e031ca55e54357903611110f42a60ffa4f0765c9`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:0cf35df2d4678aa90666b297ace71852e525bb0d58e8a619042d808ec755eb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a83a2fc05bd0588064870c4991b5732847da041258de103593e4278457a0e5`

```dockerfile
```

-	Layers:
	-	`sha256:ca4a2821dcebb2491eb6b24e0f92a32a0dbabed04f40af44570075175a909d20`  
		Last Modified: Wed, 11 Jun 2025 04:04:32 GMT  
		Size: 3.6 MB (3603021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2fbdf9a4be762dbccd1fa0a114ca7fb82d1621e3ffb4599640ec48fb9a7faee`  
		Last Modified: Wed, 11 Jun 2025 04:04:34 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:3685d33d3492f37cb915d62a095d9950c525202482709a60fbb4bf8c916d983a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37571428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55b824f1bbb90b5013110d52b3815591e7111e6b5fa1f6353f73553b75f375f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a914757ab7329775b986ea09052bc3721b1cf32e7376c259ab8e6ec4fc6cd5`  
		Last Modified: Tue, 10 Jun 2025 23:35:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d929aa956bdb096d2ca0822ef0ce3f9bb39b4b1a26ae5689185a3e8b403914`  
		Last Modified: Wed, 11 Jun 2025 00:04:18 GMT  
		Size: 2.4 MB (2400608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ff70a3441b68775b255dcb87b1f4a758ff1092fcbad78929bab5873fb91bf1`  
		Last Modified: Sun, 15 Jun 2025 19:03:35 GMT  
		Size: 6.0 MB (5956846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93f7ce598f27009edb19a25f2d7c744afe35f163eb6082e8a85b4887419e91c`  
		Last Modified: Wed, 11 Jun 2025 00:04:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa6d8a399b95819bc64981c47a790410105ec47d812c777921d8d418c24c42d`  
		Last Modified: Wed, 11 Jun 2025 00:04:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:c54d8107727a524b2bc5efbf3d34e55983da13e32728d515443d51c71b6eb356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92499a9366a830fdbcc23418768edb48096426a54126918b85e1c0c67e73a61`

```dockerfile
```

-	Layers:
	-	`sha256:637794aaa808a61855cb1344d5dbaa76db671fe43c05217b37134c1077b58369`  
		Last Modified: Wed, 11 Jun 2025 01:04:50 GMT  
		Size: 3.6 MB (3625772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e51e59cdbbfda42a97d9b5963ed0a9d602b2fc384ef1c05f4d8afe7ee0c61722`  
		Last Modified: Wed, 11 Jun 2025 01:04:52 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:44a7ea572ee5ded3f2ceeb336ebf9f4b19e5c1721cd638675de7ea6a2365a05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e178694b114b2b500387f26b4a03570b5397e036a413c99d5252b6a40471ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bdd8e35937df27b0968ae8a23741b39da32971cd7b93300071387fb995566f`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b256192f977eee0878018b3b88849faac10e38c96758feb6025fe97506622e3`  
		Last Modified: Wed, 11 Jun 2025 12:58:49 GMT  
		Size: 1.8 MB (1842270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dbd97c4f500cedd0e46e05c6718376077029907325d8b425eaa1868dd89711`  
		Last Modified: Wed, 11 Jun 2025 12:58:50 GMT  
		Size: 5.8 MB (5813695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e8d0a0cba57075c6e87aa5c196d709f79ddf523ee3af39a64ddf7bf645fc8`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89390ae038a588fb2fbecb5444cc0f64955ddba34a4c65c9f0922cb722826aaa`  
		Last Modified: Wed, 11 Jun 2025 12:58:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:82053f23f3186d8684d3e7b169e166514810bb0b54ed29568f52924dfd2c8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac7464c90ddadce8fd091e3ad3f97cdad7caaa5783f4f82d90906e9ab0d1e3e`

```dockerfile
```

-	Layers:
	-	`sha256:172483dac84d11e985c77a0c8e905873e020a5da1c9bee18ef7cb5331e5ada85`  
		Last Modified: Wed, 11 Jun 2025 16:04:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:39202814ad9a5a922dc39dee07a4c78a270a2dce9aacbe94cc5a993a67c3559e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41099457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f783c55ba71b9a04b09e905aa6d9a08d4f4cdbff59558134dc1675d9bd8a9c82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a701c078494b40af714029424f155a0c9aed7224256d32afafe72eaeaaa198e`  
		Last Modified: Wed, 11 Jun 2025 04:35:20 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81506e3faae4b3c7fdc55d44193d3ef7bf42c7bede9ecedc53fb7969f5740511`  
		Last Modified: Wed, 11 Jun 2025 04:35:25 GMT  
		Size: 2.6 MB (2583799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab89e8ce102c77aff32ae4b9f1341daba6707b0fed586438bd88ab009194695`  
		Last Modified: Wed, 11 Jun 2025 12:11:07 GMT  
		Size: 6.4 MB (6441322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474549e981a5c68f6355c03d5a65208c8f1ff83b48cbac360a1b2f1e899db9d0`  
		Last Modified: Wed, 11 Jun 2025 04:35:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03042930b914a2cc771b8a16e96de29f1fbc200b2e4827fcf3363ae89e4c2b6`  
		Last Modified: Wed, 11 Jun 2025 04:35:32 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:1bbdeff6fabf1f52aac982cfecc50d8d8ddf103d535bf968f341d2f3be73fa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247da2141d694fd96b11b86334f9242c90d2417b5503e7ae2ecfc5e21200a51d`

```dockerfile
```

-	Layers:
	-	`sha256:490a93ddac89e61f323832758d7434a8bc0eb69d57d5320f241943175d2074ab`  
		Last Modified: Wed, 11 Jun 2025 07:04:47 GMT  
		Size: 3.6 MB (3617578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ff99a61598aacfa935a26a4686e00f1df40336e08cb9b88a7669a99e9a688`  
		Last Modified: Wed, 11 Jun 2025 07:04:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:1f81a83169a2f8dc6b44819dedd42d66f5bbe5df87852868fff1df284ba9c279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34350952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2037d0b0ecd0c097289e1415f39b5c2ead5667748a82c541c41a13b12c892ef2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58de45a649e69d16b556199d2ab1e1a3f7d125d46b9cd16e1089e96d7cefa826`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3d4626d3f4bbc854f1c1234cf6b0ee2c193de1051deb16f7c2891f16fca96f`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 2.1 MB (2069158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4f64f3ab37142abe901c392f0f67b586f082fa0ae0ab4a03ab39171b8b8ec`  
		Last Modified: Wed, 11 Jun 2025 02:40:41 GMT  
		Size: 5.4 MB (5392400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de79387160e54ed225d3a0a3a8ff4c57a454eee6fd186181d4ec1cbd9ef331f`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f8e7b261543a312c7b1ad7c07a65a3f9349ddc7982903e31f44a8c0f340b2c`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:e6c50e6a029398c99b2b9176f2b69309f59e0d3af95a76db4c89f46c471e2c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695b35f06bbfbb170bb2e5e78b7fd2261c394b6496b0d6f48bcaf52dc30fb02d`

```dockerfile
```

-	Layers:
	-	`sha256:36828141ff79d8fb67953b34fd662f613d4b733b01245cf17dfe86ac8cd65dda`  
		Last Modified: Wed, 11 Jun 2025 04:04:46 GMT  
		Size: 3.6 MB (3617087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a6dbc92f810f611f28ab51c90eb087f7373028e32f74d3b80c9d77b668eaaa`  
		Last Modified: Wed, 11 Jun 2025 04:04:46 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
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
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Thu, 08 May 2025 23:05:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Tue, 17 Jun 2025 23:31:45 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Tue, 17 Jun 2025 23:31:46 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
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
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Fri, 09 May 2025 01:34:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:b83df7863588b91b6f69e3fb3476e144c4036c90beaac879e9b04f38fc10a7d5
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
$ docker pull spiped@sha256:a5d4dfe0765417cab49f9c8c81905d94b3bbd8d80bb5b1cb47df0e8668a5e4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37092818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f736b6abf32c93830c88ccb720707ddabf04bfe77052c4e4fa32800066b420b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901060e6b8a7884c01efa6270dd3f90d3843ac68e684337d24de3ca84decb99d`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5b73802790441257b5f7e4dd01f56a8f25141dbd7f471a01967e3667ce61b9`  
		Last Modified: Tue, 10 Jun 2025 23:36:25 GMT  
		Size: 2.4 MB (2402195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4e093b3597052dc43e0db358fa01a1b0d418b22dcaaad8b58366b2aa6d5460`  
		Last Modified: Tue, 10 Jun 2025 23:36:25 GMT  
		Size: 6.5 MB (6458953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff5c6f0cf05be8aeb9731139b2c42db7bd0b95a6cb4498ce4c5472915a2ebfb`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caafbfe845e21d65a68ad3391d7abb7e582c3d476b6e13e0d0602457089d379`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:00b0ab8f2820c628fd250eb63cc4cd938175c4341dd502243dddbbaa8076f425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cc64ebe1bc3ddec01febd10d49f5640f8f00e405e04e89be5111e6b11854ad`

```dockerfile
```

-	Layers:
	-	`sha256:5958f2544848781ee234867326e5230742d46d3d70e9ed6dacb5f2522e51420e`  
		Last Modified: Wed, 11 Jun 2025 01:04:24 GMT  
		Size: 3.6 MB (3631793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215a4c084e1c1c9d1bfb431aa3ee606276bbabbc814c065cd4e53f4268fed4c7`  
		Last Modified: Wed, 11 Jun 2025 01:04:25 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b049c3c815392540b5a67b398586d60aef642c918e6744f0f9e87839825c571d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b19d93be75f680289976bc19c584f7ffdf835c910772406637fefe166cb3246`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1052a6a8cb6216f507d9ebf741e442e35734ac86617a8bb1ce8aeb6378eb702b`  
		Last Modified: Wed, 11 Jun 2025 03:11:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55c33e57388de6005641bb68d8036264a16fc700c43545e0e780e7e5a3a7187`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 2.0 MB (1998289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ba223a0b28036e632aca948791e7ea0ec2ea20ed64c3658681f69e9b80161`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 5.1 MB (5147777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85477c497bb56282915ec3bde6c516852dea4c471c76d294e4b07cda81a5609d`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92173adb4d90fe4f7c0a5b937ff3cafa90326106208c7c4e16e5dc0d8ce91e10`  
		Last Modified: Wed, 11 Jun 2025 03:11:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:dbf4c17085fcb424ad33b6f2698c9d69610edb46f2916f0fde1ce11fb7f2726c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f1871eb04d3f1f6cea6f92f3f51c2e8f77f41b680f661b54c5356b19c0a574`

```dockerfile
```

-	Layers:
	-	`sha256:4314f998c143791479147c72437ceca0c9358e305b914e1cf764a95b6d17d972`  
		Last Modified: Wed, 11 Jun 2025 07:04:29 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e986205c455de4b0e54eeec2f42c4936ef395a37b1a511a9e819185f34c32561`  
		Last Modified: Wed, 11 Jun 2025 07:04:30 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9ce1fc0dc2d1f996039a56a7cfbd378133b51755333301f848efca7a7fad5776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1921127603a2388cd25100dc1a40dd4a882e503c99c18a1c94affea6d8318c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b3efe4f51fb3f46017d32a189e76502c05ebbe62a4f3734f609d087648aef`  
		Last Modified: Wed, 11 Jun 2025 04:49:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ddb002179312e93532c834e5a8082a2d73feda8078b2ce73b951b3e45020d`  
		Last Modified: Wed, 11 Jun 2025 04:49:06 GMT  
		Size: 1.9 MB (1856413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714ec40b518a9456e36344a7732ddbd1daf761542ba21f6350a63ed6f652917a`  
		Last Modified: Wed, 11 Jun 2025 04:49:18 GMT  
		Size: 4.9 MB (4888712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c379236ab7a7ce88d18f78e77b41389fcef6e28730401b67ed4d35afb95ed2c2`  
		Last Modified: Wed, 11 Jun 2025 04:51:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5150130b703fde6b91fc459f573bafe2bd5048ddab660d82204dc88bc8ff26c7`  
		Last Modified: Wed, 11 Jun 2025 04:51:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:f1d93a3b47e53aefe111a468b535741ebf3c44b479196c920c1131ae3945be4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe8b73dbdca091b6a3cfc7fc1cbe516b479f8cf66cfb32973f1c08f4f92467b`

```dockerfile
```

-	Layers:
	-	`sha256:e11d0f6c12be4f061b56a863eadca9d24cba81ade81668d540c29d14815dca80`  
		Last Modified: Wed, 11 Jun 2025 07:04:34 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7398098987796bea294105e7389cac1c9b15dc4f47d3389c2ad39ad6daced0f`  
		Last Modified: Wed, 11 Jun 2025 07:04:35 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b5143746337b9bac98b518650f2e9ed5b4b9886eabd460426ceb3de5ec9f386b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35818470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37585eab662d0b615e056a5ef9795b640ce9a89a931957d10ef73e596f21268b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f876cc248b0c7ec91a68879fb0ecc212568f3e4a637e295be916be6edeeb8`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd86f82bcea91f9ced30eff144ee24770b00b7f2c177420dbd9ac9b49a43079d`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 2.2 MB (2247471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df866991bdf5e32b6e9c1f1eb9720415e874e95be0247c4694eff05e37ca98b3`  
		Last Modified: Wed, 11 Jun 2025 02:35:32 GMT  
		Size: 5.5 MB (5491782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68a815d97977aedeb7c8399fd91c72bd238a307f23708808c8a427312e4eb47`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bb490ebf89b9d37cf331e0e031ca55e54357903611110f42a60ffa4f0765c9`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:0cf35df2d4678aa90666b297ace71852e525bb0d58e8a619042d808ec755eb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a83a2fc05bd0588064870c4991b5732847da041258de103593e4278457a0e5`

```dockerfile
```

-	Layers:
	-	`sha256:ca4a2821dcebb2491eb6b24e0f92a32a0dbabed04f40af44570075175a909d20`  
		Last Modified: Wed, 11 Jun 2025 04:04:32 GMT  
		Size: 3.6 MB (3603021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2fbdf9a4be762dbccd1fa0a114ca7fb82d1621e3ffb4599640ec48fb9a7faee`  
		Last Modified: Wed, 11 Jun 2025 04:04:34 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:3685d33d3492f37cb915d62a095d9950c525202482709a60fbb4bf8c916d983a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37571428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55b824f1bbb90b5013110d52b3815591e7111e6b5fa1f6353f73553b75f375f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a914757ab7329775b986ea09052bc3721b1cf32e7376c259ab8e6ec4fc6cd5`  
		Last Modified: Tue, 10 Jun 2025 23:35:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d929aa956bdb096d2ca0822ef0ce3f9bb39b4b1a26ae5689185a3e8b403914`  
		Last Modified: Wed, 11 Jun 2025 00:04:18 GMT  
		Size: 2.4 MB (2400608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ff70a3441b68775b255dcb87b1f4a758ff1092fcbad78929bab5873fb91bf1`  
		Last Modified: Sun, 15 Jun 2025 19:03:35 GMT  
		Size: 6.0 MB (5956846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93f7ce598f27009edb19a25f2d7c744afe35f163eb6082e8a85b4887419e91c`  
		Last Modified: Wed, 11 Jun 2025 00:04:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa6d8a399b95819bc64981c47a790410105ec47d812c777921d8d418c24c42d`  
		Last Modified: Wed, 11 Jun 2025 00:04:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:c54d8107727a524b2bc5efbf3d34e55983da13e32728d515443d51c71b6eb356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92499a9366a830fdbcc23418768edb48096426a54126918b85e1c0c67e73a61`

```dockerfile
```

-	Layers:
	-	`sha256:637794aaa808a61855cb1344d5dbaa76db671fe43c05217b37134c1077b58369`  
		Last Modified: Wed, 11 Jun 2025 01:04:50 GMT  
		Size: 3.6 MB (3625772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e51e59cdbbfda42a97d9b5963ed0a9d602b2fc384ef1c05f4d8afe7ee0c61722`  
		Last Modified: Wed, 11 Jun 2025 01:04:52 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:44a7ea572ee5ded3f2ceeb336ebf9f4b19e5c1721cd638675de7ea6a2365a05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e178694b114b2b500387f26b4a03570b5397e036a413c99d5252b6a40471ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bdd8e35937df27b0968ae8a23741b39da32971cd7b93300071387fb995566f`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b256192f977eee0878018b3b88849faac10e38c96758feb6025fe97506622e3`  
		Last Modified: Wed, 11 Jun 2025 12:58:49 GMT  
		Size: 1.8 MB (1842270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dbd97c4f500cedd0e46e05c6718376077029907325d8b425eaa1868dd89711`  
		Last Modified: Wed, 11 Jun 2025 12:58:50 GMT  
		Size: 5.8 MB (5813695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e8d0a0cba57075c6e87aa5c196d709f79ddf523ee3af39a64ddf7bf645fc8`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89390ae038a588fb2fbecb5444cc0f64955ddba34a4c65c9f0922cb722826aaa`  
		Last Modified: Wed, 11 Jun 2025 12:58:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:82053f23f3186d8684d3e7b169e166514810bb0b54ed29568f52924dfd2c8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac7464c90ddadce8fd091e3ad3f97cdad7caaa5783f4f82d90906e9ab0d1e3e`

```dockerfile
```

-	Layers:
	-	`sha256:172483dac84d11e985c77a0c8e905873e020a5da1c9bee18ef7cb5331e5ada85`  
		Last Modified: Wed, 11 Jun 2025 16:04:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:39202814ad9a5a922dc39dee07a4c78a270a2dce9aacbe94cc5a993a67c3559e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41099457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f783c55ba71b9a04b09e905aa6d9a08d4f4cdbff59558134dc1675d9bd8a9c82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a701c078494b40af714029424f155a0c9aed7224256d32afafe72eaeaaa198e`  
		Last Modified: Wed, 11 Jun 2025 04:35:20 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81506e3faae4b3c7fdc55d44193d3ef7bf42c7bede9ecedc53fb7969f5740511`  
		Last Modified: Wed, 11 Jun 2025 04:35:25 GMT  
		Size: 2.6 MB (2583799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab89e8ce102c77aff32ae4b9f1341daba6707b0fed586438bd88ab009194695`  
		Last Modified: Wed, 11 Jun 2025 12:11:07 GMT  
		Size: 6.4 MB (6441322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474549e981a5c68f6355c03d5a65208c8f1ff83b48cbac360a1b2f1e899db9d0`  
		Last Modified: Wed, 11 Jun 2025 04:35:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03042930b914a2cc771b8a16e96de29f1fbc200b2e4827fcf3363ae89e4c2b6`  
		Last Modified: Wed, 11 Jun 2025 04:35:32 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:1bbdeff6fabf1f52aac982cfecc50d8d8ddf103d535bf968f341d2f3be73fa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247da2141d694fd96b11b86334f9242c90d2417b5503e7ae2ecfc5e21200a51d`

```dockerfile
```

-	Layers:
	-	`sha256:490a93ddac89e61f323832758d7434a8bc0eb69d57d5320f241943175d2074ab`  
		Last Modified: Wed, 11 Jun 2025 07:04:47 GMT  
		Size: 3.6 MB (3617578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ff99a61598aacfa935a26a4686e00f1df40336e08cb9b88a7669a99e9a688`  
		Last Modified: Wed, 11 Jun 2025 07:04:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:1f81a83169a2f8dc6b44819dedd42d66f5bbe5df87852868fff1df284ba9c279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34350952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2037d0b0ecd0c097289e1415f39b5c2ead5667748a82c541c41a13b12c892ef2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58de45a649e69d16b556199d2ab1e1a3f7d125d46b9cd16e1089e96d7cefa826`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3d4626d3f4bbc854f1c1234cf6b0ee2c193de1051deb16f7c2891f16fca96f`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 2.1 MB (2069158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4f64f3ab37142abe901c392f0f67b586f082fa0ae0ab4a03ab39171b8b8ec`  
		Last Modified: Wed, 11 Jun 2025 02:40:41 GMT  
		Size: 5.4 MB (5392400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de79387160e54ed225d3a0a3a8ff4c57a454eee6fd186181d4ec1cbd9ef331f`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f8e7b261543a312c7b1ad7c07a65a3f9349ddc7982903e31f44a8c0f340b2c`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:e6c50e6a029398c99b2b9176f2b69309f59e0d3af95a76db4c89f46c471e2c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695b35f06bbfbb170bb2e5e78b7fd2261c394b6496b0d6f48bcaf52dc30fb02d`

```dockerfile
```

-	Layers:
	-	`sha256:36828141ff79d8fb67953b34fd662f613d4b733b01245cf17dfe86ac8cd65dda`  
		Last Modified: Wed, 11 Jun 2025 04:04:46 GMT  
		Size: 3.6 MB (3617087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a6dbc92f810f611f28ab51c90eb087f7373028e32f74d3b80c9d77b668eaaa`  
		Last Modified: Wed, 11 Jun 2025 04:04:46 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
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
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Thu, 08 May 2025 23:05:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Tue, 17 Jun 2025 23:31:45 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Tue, 17 Jun 2025 23:31:46 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
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
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Fri, 09 May 2025 01:34:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:b83df7863588b91b6f69e3fb3476e144c4036c90beaac879e9b04f38fc10a7d5
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

### `spiped:1.6.4` - linux; amd64

```console
$ docker pull spiped@sha256:a5d4dfe0765417cab49f9c8c81905d94b3bbd8d80bb5b1cb47df0e8668a5e4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37092818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f736b6abf32c93830c88ccb720707ddabf04bfe77052c4e4fa32800066b420b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901060e6b8a7884c01efa6270dd3f90d3843ac68e684337d24de3ca84decb99d`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5b73802790441257b5f7e4dd01f56a8f25141dbd7f471a01967e3667ce61b9`  
		Last Modified: Tue, 10 Jun 2025 23:36:25 GMT  
		Size: 2.4 MB (2402195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4e093b3597052dc43e0db358fa01a1b0d418b22dcaaad8b58366b2aa6d5460`  
		Last Modified: Tue, 10 Jun 2025 23:36:25 GMT  
		Size: 6.5 MB (6458953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff5c6f0cf05be8aeb9731139b2c42db7bd0b95a6cb4498ce4c5472915a2ebfb`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caafbfe845e21d65a68ad3391d7abb7e582c3d476b6e13e0d0602457089d379`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:00b0ab8f2820c628fd250eb63cc4cd938175c4341dd502243dddbbaa8076f425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cc64ebe1bc3ddec01febd10d49f5640f8f00e405e04e89be5111e6b11854ad`

```dockerfile
```

-	Layers:
	-	`sha256:5958f2544848781ee234867326e5230742d46d3d70e9ed6dacb5f2522e51420e`  
		Last Modified: Wed, 11 Jun 2025 01:04:24 GMT  
		Size: 3.6 MB (3631793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215a4c084e1c1c9d1bfb431aa3ee606276bbabbc814c065cd4e53f4268fed4c7`  
		Last Modified: Wed, 11 Jun 2025 01:04:25 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b049c3c815392540b5a67b398586d60aef642c918e6744f0f9e87839825c571d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b19d93be75f680289976bc19c584f7ffdf835c910772406637fefe166cb3246`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1052a6a8cb6216f507d9ebf741e442e35734ac86617a8bb1ce8aeb6378eb702b`  
		Last Modified: Wed, 11 Jun 2025 03:11:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55c33e57388de6005641bb68d8036264a16fc700c43545e0e780e7e5a3a7187`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 2.0 MB (1998289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ba223a0b28036e632aca948791e7ea0ec2ea20ed64c3658681f69e9b80161`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 5.1 MB (5147777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85477c497bb56282915ec3bde6c516852dea4c471c76d294e4b07cda81a5609d`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92173adb4d90fe4f7c0a5b937ff3cafa90326106208c7c4e16e5dc0d8ce91e10`  
		Last Modified: Wed, 11 Jun 2025 03:11:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:dbf4c17085fcb424ad33b6f2698c9d69610edb46f2916f0fde1ce11fb7f2726c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f1871eb04d3f1f6cea6f92f3f51c2e8f77f41b680f661b54c5356b19c0a574`

```dockerfile
```

-	Layers:
	-	`sha256:4314f998c143791479147c72437ceca0c9358e305b914e1cf764a95b6d17d972`  
		Last Modified: Wed, 11 Jun 2025 07:04:29 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e986205c455de4b0e54eeec2f42c4936ef395a37b1a511a9e819185f34c32561`  
		Last Modified: Wed, 11 Jun 2025 07:04:30 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9ce1fc0dc2d1f996039a56a7cfbd378133b51755333301f848efca7a7fad5776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1921127603a2388cd25100dc1a40dd4a882e503c99c18a1c94affea6d8318c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b3efe4f51fb3f46017d32a189e76502c05ebbe62a4f3734f609d087648aef`  
		Last Modified: Wed, 11 Jun 2025 04:49:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ddb002179312e93532c834e5a8082a2d73feda8078b2ce73b951b3e45020d`  
		Last Modified: Wed, 11 Jun 2025 04:49:06 GMT  
		Size: 1.9 MB (1856413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714ec40b518a9456e36344a7732ddbd1daf761542ba21f6350a63ed6f652917a`  
		Last Modified: Wed, 11 Jun 2025 04:49:18 GMT  
		Size: 4.9 MB (4888712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c379236ab7a7ce88d18f78e77b41389fcef6e28730401b67ed4d35afb95ed2c2`  
		Last Modified: Wed, 11 Jun 2025 04:51:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5150130b703fde6b91fc459f573bafe2bd5048ddab660d82204dc88bc8ff26c7`  
		Last Modified: Wed, 11 Jun 2025 04:51:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:f1d93a3b47e53aefe111a468b535741ebf3c44b479196c920c1131ae3945be4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe8b73dbdca091b6a3cfc7fc1cbe516b479f8cf66cfb32973f1c08f4f92467b`

```dockerfile
```

-	Layers:
	-	`sha256:e11d0f6c12be4f061b56a863eadca9d24cba81ade81668d540c29d14815dca80`  
		Last Modified: Wed, 11 Jun 2025 07:04:34 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7398098987796bea294105e7389cac1c9b15dc4f47d3389c2ad39ad6daced0f`  
		Last Modified: Wed, 11 Jun 2025 07:04:35 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b5143746337b9bac98b518650f2e9ed5b4b9886eabd460426ceb3de5ec9f386b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35818470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37585eab662d0b615e056a5ef9795b640ce9a89a931957d10ef73e596f21268b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f876cc248b0c7ec91a68879fb0ecc212568f3e4a637e295be916be6edeeb8`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd86f82bcea91f9ced30eff144ee24770b00b7f2c177420dbd9ac9b49a43079d`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 2.2 MB (2247471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df866991bdf5e32b6e9c1f1eb9720415e874e95be0247c4694eff05e37ca98b3`  
		Last Modified: Wed, 11 Jun 2025 02:35:32 GMT  
		Size: 5.5 MB (5491782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68a815d97977aedeb7c8399fd91c72bd238a307f23708808c8a427312e4eb47`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bb490ebf89b9d37cf331e0e031ca55e54357903611110f42a60ffa4f0765c9`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:0cf35df2d4678aa90666b297ace71852e525bb0d58e8a619042d808ec755eb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a83a2fc05bd0588064870c4991b5732847da041258de103593e4278457a0e5`

```dockerfile
```

-	Layers:
	-	`sha256:ca4a2821dcebb2491eb6b24e0f92a32a0dbabed04f40af44570075175a909d20`  
		Last Modified: Wed, 11 Jun 2025 04:04:32 GMT  
		Size: 3.6 MB (3603021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2fbdf9a4be762dbccd1fa0a114ca7fb82d1621e3ffb4599640ec48fb9a7faee`  
		Last Modified: Wed, 11 Jun 2025 04:04:34 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:3685d33d3492f37cb915d62a095d9950c525202482709a60fbb4bf8c916d983a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37571428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55b824f1bbb90b5013110d52b3815591e7111e6b5fa1f6353f73553b75f375f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a914757ab7329775b986ea09052bc3721b1cf32e7376c259ab8e6ec4fc6cd5`  
		Last Modified: Tue, 10 Jun 2025 23:35:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d929aa956bdb096d2ca0822ef0ce3f9bb39b4b1a26ae5689185a3e8b403914`  
		Last Modified: Wed, 11 Jun 2025 00:04:18 GMT  
		Size: 2.4 MB (2400608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ff70a3441b68775b255dcb87b1f4a758ff1092fcbad78929bab5873fb91bf1`  
		Last Modified: Sun, 15 Jun 2025 19:03:35 GMT  
		Size: 6.0 MB (5956846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93f7ce598f27009edb19a25f2d7c744afe35f163eb6082e8a85b4887419e91c`  
		Last Modified: Wed, 11 Jun 2025 00:04:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa6d8a399b95819bc64981c47a790410105ec47d812c777921d8d418c24c42d`  
		Last Modified: Wed, 11 Jun 2025 00:04:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:c54d8107727a524b2bc5efbf3d34e55983da13e32728d515443d51c71b6eb356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92499a9366a830fdbcc23418768edb48096426a54126918b85e1c0c67e73a61`

```dockerfile
```

-	Layers:
	-	`sha256:637794aaa808a61855cb1344d5dbaa76db671fe43c05217b37134c1077b58369`  
		Last Modified: Wed, 11 Jun 2025 01:04:50 GMT  
		Size: 3.6 MB (3625772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e51e59cdbbfda42a97d9b5963ed0a9d602b2fc384ef1c05f4d8afe7ee0c61722`  
		Last Modified: Wed, 11 Jun 2025 01:04:52 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; mips64le

```console
$ docker pull spiped@sha256:44a7ea572ee5ded3f2ceeb336ebf9f4b19e5c1721cd638675de7ea6a2365a05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e178694b114b2b500387f26b4a03570b5397e036a413c99d5252b6a40471ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bdd8e35937df27b0968ae8a23741b39da32971cd7b93300071387fb995566f`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b256192f977eee0878018b3b88849faac10e38c96758feb6025fe97506622e3`  
		Last Modified: Wed, 11 Jun 2025 12:58:49 GMT  
		Size: 1.8 MB (1842270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dbd97c4f500cedd0e46e05c6718376077029907325d8b425eaa1868dd89711`  
		Last Modified: Wed, 11 Jun 2025 12:58:50 GMT  
		Size: 5.8 MB (5813695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e8d0a0cba57075c6e87aa5c196d709f79ddf523ee3af39a64ddf7bf645fc8`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89390ae038a588fb2fbecb5444cc0f64955ddba34a4c65c9f0922cb722826aaa`  
		Last Modified: Wed, 11 Jun 2025 12:58:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:82053f23f3186d8684d3e7b169e166514810bb0b54ed29568f52924dfd2c8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac7464c90ddadce8fd091e3ad3f97cdad7caaa5783f4f82d90906e9ab0d1e3e`

```dockerfile
```

-	Layers:
	-	`sha256:172483dac84d11e985c77a0c8e905873e020a5da1c9bee18ef7cb5331e5ada85`  
		Last Modified: Wed, 11 Jun 2025 16:04:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:39202814ad9a5a922dc39dee07a4c78a270a2dce9aacbe94cc5a993a67c3559e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41099457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f783c55ba71b9a04b09e905aa6d9a08d4f4cdbff59558134dc1675d9bd8a9c82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a701c078494b40af714029424f155a0c9aed7224256d32afafe72eaeaaa198e`  
		Last Modified: Wed, 11 Jun 2025 04:35:20 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81506e3faae4b3c7fdc55d44193d3ef7bf42c7bede9ecedc53fb7969f5740511`  
		Last Modified: Wed, 11 Jun 2025 04:35:25 GMT  
		Size: 2.6 MB (2583799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab89e8ce102c77aff32ae4b9f1341daba6707b0fed586438bd88ab009194695`  
		Last Modified: Wed, 11 Jun 2025 12:11:07 GMT  
		Size: 6.4 MB (6441322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474549e981a5c68f6355c03d5a65208c8f1ff83b48cbac360a1b2f1e899db9d0`  
		Last Modified: Wed, 11 Jun 2025 04:35:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03042930b914a2cc771b8a16e96de29f1fbc200b2e4827fcf3363ae89e4c2b6`  
		Last Modified: Wed, 11 Jun 2025 04:35:32 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:1bbdeff6fabf1f52aac982cfecc50d8d8ddf103d535bf968f341d2f3be73fa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247da2141d694fd96b11b86334f9242c90d2417b5503e7ae2ecfc5e21200a51d`

```dockerfile
```

-	Layers:
	-	`sha256:490a93ddac89e61f323832758d7434a8bc0eb69d57d5320f241943175d2074ab`  
		Last Modified: Wed, 11 Jun 2025 07:04:47 GMT  
		Size: 3.6 MB (3617578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ff99a61598aacfa935a26a4686e00f1df40336e08cb9b88a7669a99e9a688`  
		Last Modified: Wed, 11 Jun 2025 07:04:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:1f81a83169a2f8dc6b44819dedd42d66f5bbe5df87852868fff1df284ba9c279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34350952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2037d0b0ecd0c097289e1415f39b5c2ead5667748a82c541c41a13b12c892ef2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58de45a649e69d16b556199d2ab1e1a3f7d125d46b9cd16e1089e96d7cefa826`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3d4626d3f4bbc854f1c1234cf6b0ee2c193de1051deb16f7c2891f16fca96f`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 2.1 MB (2069158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4f64f3ab37142abe901c392f0f67b586f082fa0ae0ab4a03ab39171b8b8ec`  
		Last Modified: Wed, 11 Jun 2025 02:40:41 GMT  
		Size: 5.4 MB (5392400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de79387160e54ed225d3a0a3a8ff4c57a454eee6fd186181d4ec1cbd9ef331f`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f8e7b261543a312c7b1ad7c07a65a3f9349ddc7982903e31f44a8c0f340b2c`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:e6c50e6a029398c99b2b9176f2b69309f59e0d3af95a76db4c89f46c471e2c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695b35f06bbfbb170bb2e5e78b7fd2261c394b6496b0d6f48bcaf52dc30fb02d`

```dockerfile
```

-	Layers:
	-	`sha256:36828141ff79d8fb67953b34fd662f613d4b733b01245cf17dfe86ac8cd65dda`  
		Last Modified: Wed, 11 Jun 2025 04:04:46 GMT  
		Size: 3.6 MB (3617087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a6dbc92f810f611f28ab51c90eb087f7373028e32f74d3b80c9d77b668eaaa`  
		Last Modified: Wed, 11 Jun 2025 04:04:46 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
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
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Thu, 08 May 2025 23:05:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Tue, 17 Jun 2025 23:31:45 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Tue, 17 Jun 2025 23:31:46 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
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
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Fri, 09 May 2025 01:34:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
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
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Thu, 08 May 2025 23:05:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Tue, 17 Jun 2025 23:31:45 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Tue, 17 Jun 2025 23:31:46 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
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
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Fri, 09 May 2025 01:34:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:b83df7863588b91b6f69e3fb3476e144c4036c90beaac879e9b04f38fc10a7d5
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
$ docker pull spiped@sha256:a5d4dfe0765417cab49f9c8c81905d94b3bbd8d80bb5b1cb47df0e8668a5e4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37092818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f736b6abf32c93830c88ccb720707ddabf04bfe77052c4e4fa32800066b420b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901060e6b8a7884c01efa6270dd3f90d3843ac68e684337d24de3ca84decb99d`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5b73802790441257b5f7e4dd01f56a8f25141dbd7f471a01967e3667ce61b9`  
		Last Modified: Tue, 10 Jun 2025 23:36:25 GMT  
		Size: 2.4 MB (2402195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4e093b3597052dc43e0db358fa01a1b0d418b22dcaaad8b58366b2aa6d5460`  
		Last Modified: Tue, 10 Jun 2025 23:36:25 GMT  
		Size: 6.5 MB (6458953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff5c6f0cf05be8aeb9731139b2c42db7bd0b95a6cb4498ce4c5472915a2ebfb`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caafbfe845e21d65a68ad3391d7abb7e582c3d476b6e13e0d0602457089d379`  
		Last Modified: Tue, 10 Jun 2025 23:36:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:00b0ab8f2820c628fd250eb63cc4cd938175c4341dd502243dddbbaa8076f425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cc64ebe1bc3ddec01febd10d49f5640f8f00e405e04e89be5111e6b11854ad`

```dockerfile
```

-	Layers:
	-	`sha256:5958f2544848781ee234867326e5230742d46d3d70e9ed6dacb5f2522e51420e`  
		Last Modified: Wed, 11 Jun 2025 01:04:24 GMT  
		Size: 3.6 MB (3631793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215a4c084e1c1c9d1bfb431aa3ee606276bbabbc814c065cd4e53f4268fed4c7`  
		Last Modified: Wed, 11 Jun 2025 01:04:25 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b049c3c815392540b5a67b398586d60aef642c918e6744f0f9e87839825c571d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b19d93be75f680289976bc19c584f7ffdf835c910772406637fefe166cb3246`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1052a6a8cb6216f507d9ebf741e442e35734ac86617a8bb1ce8aeb6378eb702b`  
		Last Modified: Wed, 11 Jun 2025 03:11:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55c33e57388de6005641bb68d8036264a16fc700c43545e0e780e7e5a3a7187`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 2.0 MB (1998289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ba223a0b28036e632aca948791e7ea0ec2ea20ed64c3658681f69e9b80161`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 5.1 MB (5147777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85477c497bb56282915ec3bde6c516852dea4c471c76d294e4b07cda81a5609d`  
		Last Modified: Wed, 11 Jun 2025 03:11:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92173adb4d90fe4f7c0a5b937ff3cafa90326106208c7c4e16e5dc0d8ce91e10`  
		Last Modified: Wed, 11 Jun 2025 03:11:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:dbf4c17085fcb424ad33b6f2698c9d69610edb46f2916f0fde1ce11fb7f2726c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f1871eb04d3f1f6cea6f92f3f51c2e8f77f41b680f661b54c5356b19c0a574`

```dockerfile
```

-	Layers:
	-	`sha256:4314f998c143791479147c72437ceca0c9358e305b914e1cf764a95b6d17d972`  
		Last Modified: Wed, 11 Jun 2025 07:04:29 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e986205c455de4b0e54eeec2f42c4936ef395a37b1a511a9e819185f34c32561`  
		Last Modified: Wed, 11 Jun 2025 07:04:30 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:9ce1fc0dc2d1f996039a56a7cfbd378133b51755333301f848efca7a7fad5776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1921127603a2388cd25100dc1a40dd4a882e503c99c18a1c94affea6d8318c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b3efe4f51fb3f46017d32a189e76502c05ebbe62a4f3734f609d087648aef`  
		Last Modified: Wed, 11 Jun 2025 04:49:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ddb002179312e93532c834e5a8082a2d73feda8078b2ce73b951b3e45020d`  
		Last Modified: Wed, 11 Jun 2025 04:49:06 GMT  
		Size: 1.9 MB (1856413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714ec40b518a9456e36344a7732ddbd1daf761542ba21f6350a63ed6f652917a`  
		Last Modified: Wed, 11 Jun 2025 04:49:18 GMT  
		Size: 4.9 MB (4888712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c379236ab7a7ce88d18f78e77b41389fcef6e28730401b67ed4d35afb95ed2c2`  
		Last Modified: Wed, 11 Jun 2025 04:51:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5150130b703fde6b91fc459f573bafe2bd5048ddab660d82204dc88bc8ff26c7`  
		Last Modified: Wed, 11 Jun 2025 04:51:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:f1d93a3b47e53aefe111a468b535741ebf3c44b479196c920c1131ae3945be4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe8b73dbdca091b6a3cfc7fc1cbe516b479f8cf66cfb32973f1c08f4f92467b`

```dockerfile
```

-	Layers:
	-	`sha256:e11d0f6c12be4f061b56a863eadca9d24cba81ade81668d540c29d14815dca80`  
		Last Modified: Wed, 11 Jun 2025 07:04:34 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7398098987796bea294105e7389cac1c9b15dc4f47d3389c2ad39ad6daced0f`  
		Last Modified: Wed, 11 Jun 2025 07:04:35 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b5143746337b9bac98b518650f2e9ed5b4b9886eabd460426ceb3de5ec9f386b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35818470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37585eab662d0b615e056a5ef9795b640ce9a89a931957d10ef73e596f21268b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f876cc248b0c7ec91a68879fb0ecc212568f3e4a637e295be916be6edeeb8`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd86f82bcea91f9ced30eff144ee24770b00b7f2c177420dbd9ac9b49a43079d`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 2.2 MB (2247471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df866991bdf5e32b6e9c1f1eb9720415e874e95be0247c4694eff05e37ca98b3`  
		Last Modified: Wed, 11 Jun 2025 02:35:32 GMT  
		Size: 5.5 MB (5491782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68a815d97977aedeb7c8399fd91c72bd238a307f23708808c8a427312e4eb47`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bb490ebf89b9d37cf331e0e031ca55e54357903611110f42a60ffa4f0765c9`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:0cf35df2d4678aa90666b297ace71852e525bb0d58e8a619042d808ec755eb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a83a2fc05bd0588064870c4991b5732847da041258de103593e4278457a0e5`

```dockerfile
```

-	Layers:
	-	`sha256:ca4a2821dcebb2491eb6b24e0f92a32a0dbabed04f40af44570075175a909d20`  
		Last Modified: Wed, 11 Jun 2025 04:04:32 GMT  
		Size: 3.6 MB (3603021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2fbdf9a4be762dbccd1fa0a114ca7fb82d1621e3ffb4599640ec48fb9a7faee`  
		Last Modified: Wed, 11 Jun 2025 04:04:34 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:3685d33d3492f37cb915d62a095d9950c525202482709a60fbb4bf8c916d983a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37571428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55b824f1bbb90b5013110d52b3815591e7111e6b5fa1f6353f73553b75f375f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a914757ab7329775b986ea09052bc3721b1cf32e7376c259ab8e6ec4fc6cd5`  
		Last Modified: Tue, 10 Jun 2025 23:35:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d929aa956bdb096d2ca0822ef0ce3f9bb39b4b1a26ae5689185a3e8b403914`  
		Last Modified: Wed, 11 Jun 2025 00:04:18 GMT  
		Size: 2.4 MB (2400608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ff70a3441b68775b255dcb87b1f4a758ff1092fcbad78929bab5873fb91bf1`  
		Last Modified: Sun, 15 Jun 2025 19:03:35 GMT  
		Size: 6.0 MB (5956846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93f7ce598f27009edb19a25f2d7c744afe35f163eb6082e8a85b4887419e91c`  
		Last Modified: Wed, 11 Jun 2025 00:04:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa6d8a399b95819bc64981c47a790410105ec47d812c777921d8d418c24c42d`  
		Last Modified: Wed, 11 Jun 2025 00:04:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:c54d8107727a524b2bc5efbf3d34e55983da13e32728d515443d51c71b6eb356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92499a9366a830fdbcc23418768edb48096426a54126918b85e1c0c67e73a61`

```dockerfile
```

-	Layers:
	-	`sha256:637794aaa808a61855cb1344d5dbaa76db671fe43c05217b37134c1077b58369`  
		Last Modified: Wed, 11 Jun 2025 01:04:50 GMT  
		Size: 3.6 MB (3625772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e51e59cdbbfda42a97d9b5963ed0a9d602b2fc384ef1c05f4d8afe7ee0c61722`  
		Last Modified: Wed, 11 Jun 2025 01:04:52 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:44a7ea572ee5ded3f2ceeb336ebf9f4b19e5c1721cd638675de7ea6a2365a05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e178694b114b2b500387f26b4a03570b5397e036a413c99d5252b6a40471ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bdd8e35937df27b0968ae8a23741b39da32971cd7b93300071387fb995566f`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b256192f977eee0878018b3b88849faac10e38c96758feb6025fe97506622e3`  
		Last Modified: Wed, 11 Jun 2025 12:58:49 GMT  
		Size: 1.8 MB (1842270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dbd97c4f500cedd0e46e05c6718376077029907325d8b425eaa1868dd89711`  
		Last Modified: Wed, 11 Jun 2025 12:58:50 GMT  
		Size: 5.8 MB (5813695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e8d0a0cba57075c6e87aa5c196d709f79ddf523ee3af39a64ddf7bf645fc8`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89390ae038a588fb2fbecb5444cc0f64955ddba34a4c65c9f0922cb722826aaa`  
		Last Modified: Wed, 11 Jun 2025 12:58:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:82053f23f3186d8684d3e7b169e166514810bb0b54ed29568f52924dfd2c8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac7464c90ddadce8fd091e3ad3f97cdad7caaa5783f4f82d90906e9ab0d1e3e`

```dockerfile
```

-	Layers:
	-	`sha256:172483dac84d11e985c77a0c8e905873e020a5da1c9bee18ef7cb5331e5ada85`  
		Last Modified: Wed, 11 Jun 2025 16:04:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:39202814ad9a5a922dc39dee07a4c78a270a2dce9aacbe94cc5a993a67c3559e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41099457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f783c55ba71b9a04b09e905aa6d9a08d4f4cdbff59558134dc1675d9bd8a9c82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a701c078494b40af714029424f155a0c9aed7224256d32afafe72eaeaaa198e`  
		Last Modified: Wed, 11 Jun 2025 04:35:20 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81506e3faae4b3c7fdc55d44193d3ef7bf42c7bede9ecedc53fb7969f5740511`  
		Last Modified: Wed, 11 Jun 2025 04:35:25 GMT  
		Size: 2.6 MB (2583799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab89e8ce102c77aff32ae4b9f1341daba6707b0fed586438bd88ab009194695`  
		Last Modified: Wed, 11 Jun 2025 12:11:07 GMT  
		Size: 6.4 MB (6441322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474549e981a5c68f6355c03d5a65208c8f1ff83b48cbac360a1b2f1e899db9d0`  
		Last Modified: Wed, 11 Jun 2025 04:35:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03042930b914a2cc771b8a16e96de29f1fbc200b2e4827fcf3363ae89e4c2b6`  
		Last Modified: Wed, 11 Jun 2025 04:35:32 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:1bbdeff6fabf1f52aac982cfecc50d8d8ddf103d535bf968f341d2f3be73fa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247da2141d694fd96b11b86334f9242c90d2417b5503e7ae2ecfc5e21200a51d`

```dockerfile
```

-	Layers:
	-	`sha256:490a93ddac89e61f323832758d7434a8bc0eb69d57d5320f241943175d2074ab`  
		Last Modified: Wed, 11 Jun 2025 07:04:47 GMT  
		Size: 3.6 MB (3617578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ff99a61598aacfa935a26a4686e00f1df40336e08cb9b88a7669a99e9a688`  
		Last Modified: Wed, 11 Jun 2025 07:04:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:1f81a83169a2f8dc6b44819dedd42d66f5bbe5df87852868fff1df284ba9c279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34350952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2037d0b0ecd0c097289e1415f39b5c2ead5667748a82c541c41a13b12c892ef2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58de45a649e69d16b556199d2ab1e1a3f7d125d46b9cd16e1089e96d7cefa826`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3d4626d3f4bbc854f1c1234cf6b0ee2c193de1051deb16f7c2891f16fca96f`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 2.1 MB (2069158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4f64f3ab37142abe901c392f0f67b586f082fa0ae0ab4a03ab39171b8b8ec`  
		Last Modified: Wed, 11 Jun 2025 02:40:41 GMT  
		Size: 5.4 MB (5392400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de79387160e54ed225d3a0a3a8ff4c57a454eee6fd186181d4ec1cbd9ef331f`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f8e7b261543a312c7b1ad7c07a65a3f9349ddc7982903e31f44a8c0f340b2c`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:e6c50e6a029398c99b2b9176f2b69309f59e0d3af95a76db4c89f46c471e2c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695b35f06bbfbb170bb2e5e78b7fd2261c394b6496b0d6f48bcaf52dc30fb02d`

```dockerfile
```

-	Layers:
	-	`sha256:36828141ff79d8fb67953b34fd662f613d4b733b01245cf17dfe86ac8cd65dda`  
		Last Modified: Wed, 11 Jun 2025 04:04:46 GMT  
		Size: 3.6 MB (3617087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a6dbc92f810f611f28ab51c90eb087f7373028e32f74d3b80c9d77b668eaaa`  
		Last Modified: Wed, 11 Jun 2025 04:04:46 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
