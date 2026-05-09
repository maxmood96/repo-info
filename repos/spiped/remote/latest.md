## `spiped:latest`

```console
$ docker pull spiped@sha256:01fbb1b5d7cc01008ba99a78129c9ff54d66d34553e7659390c292101284b0c7
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
$ docker pull spiped@sha256:6efd769d805f600ba739d18173542643175bc85a275a6c2b774507b866215473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36830428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3193b704891a8a18ac61ecedd914fc9f5bd4f08bcb9f49c1bf5d515f1d635642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:35:11 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:35:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:35:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:35:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:35:34 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:35:35 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:35:35 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:35:35 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57dde26e20eb068bd1c6070f0dd034bd2fd4bb74b1da82102adef70cdfed8b`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc21a8189b7a94c8796b3a7235e2b6031c3bb5c38a32e6dd145ecc6bbf04b7`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86acbd1889987e9e18c2f14f31b0434706f81121130868eda3c8c530a20af8`  
		Last Modified: Fri, 08 May 2026 19:35:42 GMT  
		Size: 7.0 MB (7047830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8465fa5d80692f7b30c835d41e84147136800e2c926a318e6f844e8aa3836bac`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c6cb3750ff6c08d0efb53fca666dfb8b02730a76835cddd23324fdb9c8a50`  
		Last Modified: Fri, 08 May 2026 19:35:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:487c3ee9e344c1a378f97678431d3e69821f86c4eda6453de29af68a08d68173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc31b2a2f275eaf7500af7747def58d03e41f11827d308adb17d72a49c616aac`

```dockerfile
```

-	Layers:
	-	`sha256:4b40916ec2afebb3f0a5a2048230524b2afb160289fc9744212b19b511be425d`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c2e4615b4f2b4e4ffd2810f21ba67d9914c2f032810327b3488715ae97a747`  
		Last Modified: Fri, 08 May 2026 19:35:41 GMT  
		Size: 15.0 KB (14980 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:6cbedd59e1b9ab471903f2f35a283d6f759be7121323441a6ca11573d8ae1cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d990d2ba40ebc977000d42cedd17ab74640ddafe3cdee97d15362100231d6383`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 20:56:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:57:21 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 20:57:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 20:57:21 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 20:57:21 GMT
WORKDIR /spiped
# Fri, 08 May 2026 20:57:21 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:57:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:57:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147b3e27022cec78f27ab492347bf10b38fbc6c422c905e72f65841af2c2d35`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6f9b4d53a44c3aa0c748c56ea7420bc6a2ab57d31e476283c807a478c52a3b`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7292710fe7c3115e3ec777cbaae5e736fe457c7abb0b37105d16f3dd0e6aa0d0`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 5.8 MB (5789227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be583d842fa62ff531b016e5bcc500de7cb8e354eddd92a4d45dc6617a54826`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e608db2fba73f6cd7cc5367f133a6f818229089838eec0abce963f0960c957e`  
		Last Modified: Fri, 08 May 2026 20:57:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ee5c5f8032a4007863cf92bf644d1f00091054b2afe7ed6c0a2abd05eabee240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713b5a387e4efd3ea171616d9b76dcad6c85e7fd7c9406dc19495e279cbaebbd`

```dockerfile
```

-	Layers:
	-	`sha256:c1b655131c2f9a200d94f4a9833890220f71e30981b4064d2f16f8a833f997bb`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 3.6 MB (3619254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ddef005c38ab7a29e8f27a8e717e4f7c45fbf16cf5484b232c46b7d559ff7c`  
		Last Modified: Fri, 08 May 2026 20:57:28 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:4ff1f64955f0baac28dd640dfec3eb6e7155387c14a4c6857815f04a5019ffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31802065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c7a8a4fd74a9ea680b4826c71ad4261c1b369234cf1e5a1af74de4f0f02780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:48 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:43:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:44:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:44:15 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:44:15 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:44:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:44:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:44:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f160c4481d462904aa24778c4b01da7a50dd3330da0f3146ecd0fa1750b36e3`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f6312484a065cbbbc3f38cbdcd14f9d0d288af4570dc95d0b422521d5a4e9`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cfb1c37acf55579035e448653f38eb6ee097fa7f5c76c63e12e4b73e6bed7e`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 5.6 MB (5584782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a95cb661cfcd83f6253fbdfda5fdca5527107bcaceb6cd297381b4a90ff390`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d438e2f2f47da106abfac0e9680692ac80d185181f12e690966a0581ad54dd02`  
		Last Modified: Fri, 08 May 2026 19:44:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:26f57e59b1a522ae1a687b8df8cf930ddf2c1d699112e21280421a49ca910972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2c0796641018c39128df86b179e33a156dcb32c5541d96e2972f2e703e151b`

```dockerfile
```

-	Layers:
	-	`sha256:418008c48573eba24e549885dce4ad96fd0a220792017aeb5f7acce11418e708`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 3.6 MB (3618375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6e39d76bd241efe3b0b538efe61306d7f2392070a38f4c7231ff87fb17c6fc`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 15.1 KB (15087 bytes)  
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
$ docker pull spiped@sha256:d981618a0d9c00684e6abf3d84a440dd8149f059c1fa1770e74b57656b7d1660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37741286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5cb61d1ba1a94f11c6345a5fdb6fea544260c32c6125120a8872687fa142f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 19:42:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:23 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 19:43:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 19:43:23 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 19:43:24 GMT
WORKDIR /spiped
# Fri, 08 May 2026 19:43:24 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17b41ec4f852447201aeb965c3aa2bafdee78fd8912e91f0b7978c569be5e2f`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70e5c72cd4936724086c00ec89429bded5df26b92391c2566ed2fb716f18aa7`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709085b6edd21ce82957d908045c521464897a7c5aa9403a2dd9fd0f92d5140e`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 6.4 MB (6442518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b14de3e13da7ff3cc57333aab9a6a05e63d3b95b75b2817946da6be54d9c921`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82008a569b9479b56a58f4f85ce555a0023f34e26440b092f1cf31191ce34456`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3408744cec174cbb267a63b72e71e41b4e396fdbf4d8b29a489532fce7271e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a172af2f2faf106a865ab5dc37e0b74df8c431777dbc521aa563779b97a0365`

```dockerfile
```

-	Layers:
	-	`sha256:aedee6e6a52a08621420305a03eeabe6aaa0173b995b54b09f9326e9c235f2be`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 3.6 MB (3620389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58a647b7d7db8950d4a473142cb3d7427b419850101f376d98d507d3a374200`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
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
$ docker pull spiped@sha256:bd86a35901c83fdbe0b1dd9ab57c28d30a6565052dbe1ae0ef315fc89adffc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35964636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e9eead17c9f5aa0363836fa2a870f271ca50be7e2f1899fb3e7e0c17e6add5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:52:18 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 08 May 2026 20:52:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:52:41 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 08 May 2026 20:52:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 20:52:41 GMT
VOLUME [/spiped]
# Fri, 08 May 2026 20:52:41 GMT
WORKDIR /spiped
# Fri, 08 May 2026 20:52:41 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:52:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:52:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379c83725970f21bcd83cf3380670f0ea271dd1fc30bc3e9568c083f2580ba55`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3284a3de5bccf5d6b269c2b7bf9b319d15f9bebd9af7f1c95123337f82ffc`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee74470711143892631998b06f797b17b8f24c199e31160dbad3fa3f9f4b1b`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 6.1 MB (6121916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efe750c150333b99cd25f27597baa8d209228b9898aac1c0a7355a41ab17040`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b3234d867e10e2e459de5bd4cf9e1156a19cf24d495f2dfc7415071ae5715f`  
		Last Modified: Fri, 08 May 2026 20:52:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:7c6bfdf45b3649d1b3f9001e65846a9f9c95d3e42d468a4d78f4b4419a680bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5894b164eadfcc36f173a9f50f9038140f4fd57fd4528d5251f9f417819c1e0c`

```dockerfile
```

-	Layers:
	-	`sha256:117c16ab57c2ffc82accce55a8dd174232910aa2a2d2f4121a9924747a140c28`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 3.6 MB (3618623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7501e35b7a1f23c01cc4fa7d7fe477f7d1e791f6af13d52b1b0b27d654c13a4`  
		Last Modified: Fri, 08 May 2026 20:52:53 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
