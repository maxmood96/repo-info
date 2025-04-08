## `spiped:latest`

```console
$ docker pull spiped@sha256:3fa002478e7899b74b3db52d3f367852e5aeb61fa041afcf4fe1e73acb8aae78
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
$ docker pull spiped@sha256:6d32e7ce5d2ff3fad1d2f3d94a22d68d5413a362064aa908b48ed362c646e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37088911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d67e962c3ded24a6dab2509707858c7fa3cf753284603796c172419d0eb59f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500c15cab9723743d022a0be9c8911bf8f9fdd14e69a059888c422c3a7eb7aae`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdad9df9d537267ba5dd12011d934d96301ed61602c2b4f0d9b9dbfe0c731f1e`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 2.4 MB (2401350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a30878ff4b6f5bc5eceeeb9e30629360559e162847ebede379c15e007a31e17`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 6.5 MB (6458758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bc440eccb40b040214e24750ddf74febce1d745e5ac126274169834b3370be`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748117a2d043fcf5ff02f40ce053491edaa3998889d2f5050a49c4403aa41657`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ee9bbd17b18e19a6bad7f22f1a0b4e99aa1de86d2a773a9cc1d7a0217c27038b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3532222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8cc1f1b4c9f49ab6a90dcacbc557193cf1d6bbf25895d25a2f0e97b79d9b38`

```dockerfile
```

-	Layers:
	-	`sha256:f89efe38d6726731e9443c49c8e46571eadcab1a0910cf21695b0e3dc35c3970`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 3.5 MB (3517182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4acae7df28a2274c21fe0512e758ac7156fa9f8b810c96dc6d86719f1de2ec`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:76fc0874f6253115ec7614da4fab48df49576f27c39ac557c9e64e6b5a2ab5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32882119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907713bf289d8b0e5a35a821b1f4dab34c04e01a32ae2cf0e15f25e021371f74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
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
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb569ca2eec4285db13c74287f3bcf8faa848ddb9975dd2bbb62c4fead95d86`  
		Last Modified: Tue, 18 Mar 2025 03:24:18 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cbf9db5b77268dd958309b33f3addfd17a4733cff852604ffbb0c67376fec9`  
		Last Modified: Tue, 18 Mar 2025 03:24:19 GMT  
		Size: 2.0 MB (1997313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11b3ac6b8b6f9833bade68f34d5c0668e5d51657c1b15e31b233bebc1279660`  
		Last Modified: Wed, 02 Apr 2025 21:50:40 GMT  
		Size: 5.1 MB (5147412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c6408728f690bda53322c99aec63191578246553d858b47bf3b853f03699fe`  
		Last Modified: Wed, 02 Apr 2025 21:50:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a41b8dc481c71ba2c86842eebc28e00c899b531d72172efb09b6f8ce23ef72`  
		Last Modified: Wed, 02 Apr 2025 21:50:39 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:74a293a96a9fb18475b9eede75ebbc28f2fd380955715d1ec14a6422ed17cabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2357f42de6fbb9ca2b2aeaf5ec8f344fd0ccc5c147e21730e90abf4c19629aa2`

```dockerfile
```

-	Layers:
	-	`sha256:f7f11eaff3780c91d4d2294c08b6f44e7232988c928d3b7c01f1725048a2c819`  
		Last Modified: Wed, 02 Apr 2025 21:50:40 GMT  
		Size: 3.5 MB (3486410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79059f0bb54d60a57d999f5fea3b18e08a4bf4b854db6f1eca7a921d4dcf062`  
		Last Modified: Wed, 02 Apr 2025 21:50:39 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:06d634e652bed4eb1f075673523d9c71426042bd6aa29eb9c1a07622b169327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30660755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d91f60e2fd21f3f10991d662f3b8efa78830e59ee8e0eebd8fcb3528b9066f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
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
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8d51780c747bff67325359e4189287e9a9f25ee0a5f6ba8d6e4366e8a28b87`  
		Last Modified: Wed, 02 Apr 2025 21:50:50 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd7b33acbdee9c8a9f9a780f44fa3a7d89e377cf6d5966f8fd93d5c32ae0bb`  
		Last Modified: Wed, 02 Apr 2025 21:50:51 GMT  
		Size: 1.9 MB (1855553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ec2179e737ed0a2196359efc8c15503d1b0763d8edec601ef88d41f95446e0`  
		Last Modified: Wed, 02 Apr 2025 21:50:51 GMT  
		Size: 4.9 MB (4888571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a392ea5ab06b759ec68bab5212ba611a0d0a7994aef6fa152c68683e1d2048`  
		Last Modified: Wed, 02 Apr 2025 21:50:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4709e6bf39efe80963cc0794899a3766cc9c9a7e431374f3d2fedf1edf5ea2b2`  
		Last Modified: Wed, 02 Apr 2025 21:50:51 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:97dc44a977c6a10a09fd8f738ce485210cba6e1492a0a1b17c5d028ae665b478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3da156c918457432a2010ce3742d068bab457af26e6225a4a01c8df665dc2c6`

```dockerfile
```

-	Layers:
	-	`sha256:3f85807126cc679b48b86697c994c8b00e9bff0fe8754861cb8cc4da8355c1a2`  
		Last Modified: Wed, 02 Apr 2025 21:50:51 GMT  
		Size: 3.5 MB (3485901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ff4ba03b9e853a5fc48394d029bfe24d594d11224d6294f57c8c543c16322e`  
		Last Modified: Wed, 02 Apr 2025 21:50:50 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:33e4732325b7b4b0ae1c89d2b80bd17f9527267422f598e9ff89b6a21c8be5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35784119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df891aa2ffc795e0a6bd36af5803f080354c3d1d1c9ca3daa8c1c4a4a90854a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82025847babafc59539636b0a07115b34a4e45ca5ff7aeaf226841cebd003b5`  
		Last Modified: Wed, 02 Apr 2025 21:51:04 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd8777e30e3809a49ed4a527b81e71f92430db60dec564ab301de714e6f1d52`  
		Last Modified: Wed, 02 Apr 2025 21:51:05 GMT  
		Size: 2.2 MB (2247005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f4642ec1bc0ab58eef35992fe622d9f770ec04f1a6fff74ccd09640f52874c`  
		Last Modified: Wed, 02 Apr 2025 21:51:05 GMT  
		Size: 5.5 MB (5491533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931c500934841f811fcbb686abaf5fa080ab6306e8646581ba9e23bc69bf0eb1`  
		Last Modified: Wed, 02 Apr 2025 21:51:04 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e97bdce3f018b1a7f47e19ab9614971c52b89cd0065a17d5ab6cf419902150`  
		Last Modified: Wed, 02 Apr 2025 21:51:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:36c251cba6ad46b3c7228e5ed2df8fe7964d2ccf819bb126b61b3c8658d3d5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c54cb743af4102f3185db302cacdbdb9156e3d6cb64944e7160bc7a9428eb9`

```dockerfile
```

-	Layers:
	-	`sha256:3ef9e1fe2a7ff2f94ab814149503dda958127fa00cd376f2ce020e0c41132d1b`  
		Last Modified: Wed, 02 Apr 2025 21:51:05 GMT  
		Size: 3.5 MB (3487108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22768b6ff285d5a284435afa663771e9089fd2231b18aea23788dc0a158bfeed`  
		Last Modified: Wed, 02 Apr 2025 21:51:04 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:09bbaccba1e02da0360520389764dae62d2a39dfbf4dca09b0319e7195dcc997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37567726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8112da5f401aaac5619a8cf2a15f8da1bb4e44dd45d75181e1ee223b5b52a866`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d51be41883d1d657d26ebcfb1e529833ae8b0a9802ddb22ab0f23a6eb284ecb`  
		Last Modified: Tue, 08 Apr 2025 01:23:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746da8913c78f166aeb1a394beb52ba6030633e4ee1ce8a8df740cfb40ff9481`  
		Last Modified: Tue, 08 Apr 2025 01:23:10 GMT  
		Size: 2.4 MB (2398662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862fc06984c8de6269a3417f3fd18a6c73c8cd43b7ea546cdcbc6e7112db198`  
		Last Modified: Tue, 08 Apr 2025 01:23:10 GMT  
		Size: 6.0 MB (5956791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778c8d5698f859e8fb0f4880b6a6944c58b027f6f9b430d9545dc18731472f4f`  
		Last Modified: Tue, 08 Apr 2025 01:23:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dfe9f163de16cb7ddec786703f8bb27e091c21ed9bf5ed3d3b16fc8bc7aa33`  
		Last Modified: Tue, 08 Apr 2025 01:23:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:331d8d2dec88f8240c15596e178b59ec620665f9cd19d929e55d0ebecf9559d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3526113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e54f3966558c21d1e73b9374ad9f0720e852549b0544186f81c9a5a1875aff`

```dockerfile
```

-	Layers:
	-	`sha256:9beca25a7a12911e0746fcba05193701a9cd141a54bb38826d10331daab4a15a`  
		Last Modified: Tue, 08 Apr 2025 01:23:09 GMT  
		Size: 3.5 MB (3511109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555fc6c42ad1e8a9137960e15b55a26a359d67b9a535a626187ea893c0656e4c`  
		Last Modified: Tue, 08 Apr 2025 01:23:09 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:af361ca928f10b87bc7088ad70d66b1ac0f289e02ea567d70a27e0ef3f961a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36145655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad2b5369e47894c178e651dba1ea5c0e7dabcff1981bee1cd3c5435e5d46a88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
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
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fc01cf5975edc30b3953dd0641dacf3fd2e7e28e6bf5eac7349432e2dd1914`  
		Last Modified: Tue, 18 Mar 2025 16:36:12 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba21d0c0e6333189aebdca953d5aa4d6832c4225d0f535b238b43df07c391d9`  
		Last Modified: Wed, 02 Apr 2025 21:53:12 GMT  
		Size: 1.8 MB (1841139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb878fca6b960367da492dce9bc89133fec6ef8abe690fa75b3c4029bf4d1056`  
		Last Modified: Wed, 02 Apr 2025 21:53:13 GMT  
		Size: 5.8 MB (5813518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08beba086c0cdb5f0ef13cde8899b7a939e265ada2afeaebca1e3f6433b73442`  
		Last Modified: Wed, 02 Apr 2025 21:53:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed26c312d42d97093f598968ccaec2c6dd7b718692e268abd1173ea3ed9a016`  
		Last Modified: Wed, 02 Apr 2025 21:53:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d9a1d4eeb6c24c0a7ca2d6fa4f76ea813c95863b57223f427bb815eeed5f928a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5797d53036f5e828dd0186f6b410a14ba0aa7534d6b3ada2f73931afd31d90e6`

```dockerfile
```

-	Layers:
	-	`sha256:66eeadd1e483c3b263a8273416d3908880602bbac8a9e31d0395f36624b6161e`  
		Last Modified: Wed, 02 Apr 2025 21:53:12 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:c793d0ee858eb5529ffbafe1294b7073356c3071a8a07ef5c41aa0ccd2bd654d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41072745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e32b2e6cd438a302dab972abb6ce3fd98151f564f890e87830930dc07fad075`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
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
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4b15fde547f1bf481c1d7406ee73c11dc9811c22ea4b93e98d0ad9bfbd1c13`  
		Last Modified: Wed, 02 Apr 2025 21:51:17 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0358a73f8874b4210632790dbf439966cb32f32fc92ac7cc5666acefd6a9f9`  
		Last Modified: Wed, 02 Apr 2025 21:52:12 GMT  
		Size: 2.6 MB (2582103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febe251d8aeee0575feb7267f174bb782f746cf996428faa1d8cd5508ae89971`  
		Last Modified: Wed, 02 Apr 2025 21:52:12 GMT  
		Size: 6.4 MB (6441285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41968e2ed674766c572df20543af7a03f6f05ad8ebfda084e7398844fbe46c56`  
		Last Modified: Wed, 02 Apr 2025 21:52:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c21fddc33d3dc041407c44624ac181512bfcb38c9c57a3fb912653a565d6db9`  
		Last Modified: Wed, 02 Apr 2025 21:52:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:34ff736d365622ae062de0b56a8defda6e4e1f48681201dd2e0400e47e2c28d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b7fcf61570fb52b0fd090c5963a07390869f14430b6a0766bc332b1ab82b46`

```dockerfile
```

-	Layers:
	-	`sha256:2bebd5e7d7fbbd5b788569c2f6edf571a73aad05f7bd0bf7b54d5c34206e070c`  
		Last Modified: Wed, 02 Apr 2025 21:52:12 GMT  
		Size: 3.5 MB (3501549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc28066a59fd238920b274fdc221f67a3765580d23364152e0ad122eb8537680`  
		Last Modified: Wed, 02 Apr 2025 21:52:11 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:f6133ca266b72741881eb6c9bfd156ba87eee4f8196e67550ae49c046e5cfbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34323537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5f2d6527ce999227b3aea4d12049570ba56a2c45efc015846d3f3d5fccb347`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0864fd152eeb18959ea16343bbed89d7ac39429986c8785c2d6e74dc7e1358`  
		Last Modified: Wed, 02 Apr 2025 21:51:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f565ff004c31d4bba4c816fdf7c29edd9778fd7f1fb423f3df25440f1e94494e`  
		Last Modified: Wed, 02 Apr 2025 21:51:36 GMT  
		Size: 2.1 MB (2068751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b4729d07e2b71804e6571485c24df93c5de6130827af2dbce44d49095c5d39`  
		Last Modified: Wed, 02 Apr 2025 21:51:36 GMT  
		Size: 5.4 MB (5392184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c5596fbce935429b6caf85f6ba1bad7d579d6eb42a8052325f149b679891b3`  
		Last Modified: Wed, 02 Apr 2025 21:51:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1703b09a453f040cf60bd226e9580df45a605cb5dda5eedc7157a7e8a09f6641`  
		Last Modified: Wed, 02 Apr 2025 21:51:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9a8d71de46caa587beeae944eb48c2f264e49484550234bac3aae3fb30943949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32629ec67ccf812df1829d8703497826784b5ce8aa05aa1bd2190836c87ac606`

```dockerfile
```

-	Layers:
	-	`sha256:09f3797943a2e2e835199c219d4fefe063235bd874748a43e6bfac34be1ea3eb`  
		Last Modified: Wed, 02 Apr 2025 21:51:36 GMT  
		Size: 3.5 MB (3504066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91414bb86d3ec695e587d46aaa3ea6c92ff72b04a0c4f537ffa5db25237a363a`  
		Last Modified: Wed, 02 Apr 2025 21:51:36 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
