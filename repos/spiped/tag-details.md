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
$ docker pull spiped@sha256:b37d298bf05ecf3d2b1fa9ad6a1faa526d8f6ad09950fd1fa2f10a61cead55be
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
$ docker pull spiped@sha256:0d1c334e5c8c9a1482016dd7c81e161dab08a26a1f8537b7903432102d451868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36829432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c6e9fb649d94d08febe4acc1e055839a37da2c42592f79b234111a578fa779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:17:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:17:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:18:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:18:19 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:18:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:18:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f901b75fd05193d3ad4d413b9141afe4839c042a6371f33946fbe47efe47c`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee711db5622013b1d0a286930e78cc115b892e515bd2b74884d9706efb3fcc2`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ffcd4f57e39f1b0c6e284086b329aac3d99bba85f3d8db0a07595a3b7704c8`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 7.0 MB (7048432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa98f4373c484290992def4e28ca78f4d611794962d5e80e2376cbb0475460ad`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698f8b4f8d85c7878d49b3d09d4a893b1bbfb076376dfdfbcbdae85f7d1278c6`  
		Last Modified: Tue, 24 Feb 2026 19:18:27 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:913c8865c349f366c3068b316a5ecdb18147952dc0aee7498ad38e99e424b06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1b7e144e78fcc2cc2df9c9e685f4a7fbd06a5f02a9f6231eca16326e187f2c`

```dockerfile
```

-	Layers:
	-	`sha256:4454c48faf74e6d296f98d6d6999c3e74e9b7a952fbf069882d1f41396f4621a`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 3.6 MB (3626224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2bffe3af9f788104990231e51ee8e00bfd2bca6c9d6f3b403e15bf6420535a8`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:c4e19115468a9609ab171bfb50ba349826e5b45e0aee93bf7cd5c13048448787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e919cf4084856ae1dcbca01c72c1a632e39fd375cd01734ac8fef9eb6d3fe1a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:53:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:53:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:53:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:53:39 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:53:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:53:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c198268ff1c5ca902e3283584c9ed32fa711a2cf10e3a924ff5bd2c42e4b48`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cccb512fca00e135cec19f2482d6ec435eec15138610557719f7842baafe2a`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654e9a48c37c202be208834a489946cf92f91a21e6cf15c17458c02165e2c063`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 5.8 MB (5789288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada106fd65b27b787c26f0a28ce024f3ba38d1fa6788382cbb0c176a5142c9c8`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a890e111189051061b9f8bcbf2ebc36ac489e856bda9ca5d71a0187748d2e9`  
		Last Modified: Tue, 24 Feb 2026 19:53:47 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:69bfd3e675534ca1872423565cb1640224fd03ac12e3913a7f6b9c0477e6d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b529af9a3bf89decd1f57354fd1f1a906e3e7d32909d56eb13396576a55242`

```dockerfile
```

-	Layers:
	-	`sha256:ea0da76632dc1c96bb9c6034a4957d7c614ee95a93588db43bba8f29949a327b`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 3.6 MB (3619218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0052c2aa4ddf97f634cad7ee4a2fbf861200bc3f5215c162fddcafd2577fd480`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:b6c8d341f5e42f60a0ea6ad851c018181e69fd9af14df412cd8d0d32e5188c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7158910c12ab601276d7fa94f62712e71c7a62901875e8b0084e445ab0d0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:59:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:59:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:59:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:59:57 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:59:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:59:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b619584000476ce9b92659debeea088be8a3f430b26b3b31313373342bbe764`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cac6db5f98a1ac43951d2b2e3b1ed63a3ad80259e3697a344771a19cd25e7af`  
		Last Modified: Tue, 24 Feb 2026 20:00:09 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3783b0bb342b3a78b8cbf1594be27307eacf99849d98767eb175f5373dde825a`  
		Last Modified: Tue, 24 Feb 2026 20:00:08 GMT  
		Size: 5.6 MB (5584641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c493775ff90db9aebf059cbb6d4b754d5d3bde3cdba564acf5d5e4d9e37b8760`  
		Last Modified: Tue, 24 Feb 2026 20:00:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da041ec1755b24b1dce3f9967c76fbd9d57c7d5bc14a7a687f2a73c0224fe934`  
		Last Modified: Tue, 24 Feb 2026 20:00:13 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:8bc5e57bd6a8affda4eab4feb147fe074d6714e0cc5e5bf6df9b72cc33fc924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293b678e0d719326f722c4cbc6d18daa87f2885284d3f523040759c7f0759712`

```dockerfile
```

-	Layers:
	-	`sha256:38118694c8deba31fb2f231d972a1b717a7e67e99881f03bc3a1573404f45aa1`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 3.6 MB (3618339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbaada0809e420c18e0373cda990ad76cea3b71803f638ac0741a403e6c48a65`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0f1abb33a92e1c585ead9dddc782a7b66b51850c4d82d7cc27237227c94875b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922aacc7550a272b9c976c4ed76afd6391ea4e88703985dd28b31071794d21e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:23:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:23:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:23:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:23:37 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:23:37 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:23:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ed2ecdfd2e2a5f9323e19d20098f8653dfafed6a26430c6ae454d2c285fd60`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfac042c5cb69a73cdcc6401209530223ae8c8c236991e440eecc758484c451`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ce2e61248378161b4d55ebdf0a6f5a566384f9c5f5f84887f6505d2d5d4cf0`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 6.2 MB (6232845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1871ab8d2053ebe33f6b3c1de0922c3c4036ae5c6a842523e6e73fc1f7c132bb`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3db97a39d0d57606acb70e3b988bf408110a1ec22b13bd90b0096a6f468f843`  
		Last Modified: Tue, 24 Feb 2026 19:23:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:726f192ef59dd0155888ef52984e02bce8d56c8e760d571db4dbc610237b5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bece38d0e1923f09df6d6188b2fe9621a590b011c6f18a6fb0d8e405b0fb0545`

```dockerfile
```

-	Layers:
	-	`sha256:34056d5e6dfe40fbb3aa9127f1d4c4545ef508bcdd64942e6670e0b84ee7f50b`  
		Last Modified: Tue, 24 Feb 2026 19:23:45 GMT  
		Size: 3.6 MB (3621260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69d024a4e16fc1a11159aaf427a6ecb1c740e7895cc06b807a52218f1480b0a`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:a157a00a667365ab5ed49f538a1a066ce49e1b004687174fef8c5d8b78c706ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37738983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5e10b8ca505080c96ca00702e753b8e9e54423489cc23c1f0c286dab529b0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:24:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:24:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:24:36 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:24:36 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed616e6fff66cd009ec779287a335a2be1e348ccd44ede848d9d436cc00d6044`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8c64027cc40891219069c8ad75c2064da78484dd95ff0277a4d5355eee4657`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b943e889ee51e1ad6c052eb18cb8a96f04e76bdafac5e3c0a6a69af9be4709`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 6.4 MB (6442695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed5467f7f04ad6c5c280bcf57e7a06a73a52cbe23722ee9bb204d63f98f017`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb93962389450844c84c19f2b6e2a17ec6dc3d8347d2456ec18b4f24d31ed1d`  
		Last Modified: Tue, 24 Feb 2026 19:24:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:1b23c72b600c320cffa66a0c877dc6ce51fb20caa1f5c332464204a851f8fd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6273dbe2958ed3318df882a44802b0bffa3b69374c0b6c4360248913ec972185`

```dockerfile
```

-	Layers:
	-	`sha256:f25242888619593a7ea11ce819a23a144c545e563cfdb96d6a3be08ddafc7e8e`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 3.6 MB (3620353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c9e0d51a914006db4560e4405b97545e215d38cc392644f540f30511821acf`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:5b75c8c015774b8d23c079933627c1cc198b2ab1897e2ef9625ffe1a44e00abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40443061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4641f5e0942fce77295555370ecd0871fdbf48e9ca9f3c89303de4a4c16f22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:18:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 21:18:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:19:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 21:19:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:19:24 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 21:19:25 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 21:19:26 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:19:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:19:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032a2ca89d1a60962edc7ecaa5da32bbedd88b2d8b8010b10b80a7063ab6a42f`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352996af11d6ff12d58bc6f649d29adf801139a224b20d6d11f7986c3aa1a268`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a6629e08d34283ee8a3ea0798a9576779ff8dff51e7a37556b91251719aeb2`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 6.8 MB (6840475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d31d92746a14a820bd5990737171f219afdf1a48b9420be8522f528453432d`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad414bd9f5175c4827944d16ad82c7d0f33352e88b1729a3daa666a3fc94b177`  
		Last Modified: Tue, 24 Feb 2026 21:19:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:e4c070340a937f959027c51e25fcd835db51920ef30e24656d63af8e5e4c349f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f57a77227f8d58bfb6c9b06eeca3c5834f85771a2544714984c3f31e020c32d`

```dockerfile
```

-	Layers:
	-	`sha256:4e9cc3f215f4a204420884148121537cde4ff9af11a8cd76af0f3b5eefd7a5da`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 3.6 MB (3621961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967e301e427ae74d7411a5639dc6b5dc5825b933477bfe5d1e67465d3f44cd69`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; riscv64

```console
$ docker pull spiped@sha256:09783c4b01b0ff8c202fb26ef91603406e2758f0318b0f1daf6d42feb13c79cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37637171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a6aabadc5ebf87448c37f16f04e599fc861f845b9f3b472f2b434a320aea38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 03:04:18 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 05 Feb 2026 03:04:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 03:07:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 05 Feb 2026 03:07:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 05 Feb 2026 03:07:55 GMT
VOLUME [/spiped]
# Thu, 05 Feb 2026 03:07:56 GMT
WORKDIR /spiped
# Thu, 05 Feb 2026 03:07:56 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 03:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 03:07:56 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8525326a14b8a2f76773a30afbef5c22ed9293bc6da990616cbafd44ada6214f`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4056eefe513b961d3bd58ca86f11f00e23e0d20a44212052543469c3209f47c6`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890a93809726093bd14175f0ddafa3b16d2e6f70c6279892e2906c6e7e3ece54`  
		Last Modified: Thu, 05 Feb 2026 03:09:11 GMT  
		Size: 9.4 MB (9358421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd55e0daa803fb19a0d1715e1b6b4a1b0b8111069ec4577a82ece42bcf5008e`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92a4382dc33847551587860a6e2f0af1d60936e1a7941092fae0ce1280a219f`  
		Last Modified: Thu, 05 Feb 2026 03:09:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:1e373ded01a970ebae5566463fbec00e9be9dd80c27e8f97ff21da84ba19db68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45b45edd4dfa78a5d24882e4fa291588bb618a19aaccd25b531caf9219005b4`

```dockerfile
```

-	Layers:
	-	`sha256:a3c0166e8b9b6fb6b047956d064b1aa53ce13b39ee3103d5572cf70871221255`  
		Last Modified: Thu, 05 Feb 2026 03:09:10 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c49513027be2d086c9be28bf8525c760b6800b488fc7a207cdaa0fe79f30c69`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:d114290ecbbd13fe474f84310fb347e832e6bc85948a905227cda849a8ab28df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35962656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d4e52f7ccbd9605fa5fad30dda7622945ead71edb8113da175554ffe8e30ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:55:11 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 20:55:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 20:56:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 20:56:26 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 20:56:26 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:56:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e967cd97845f2bb25e9db030db7ed70580a36eeeacfcacabb36c6117e9a36938`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef093a72b4064b3aedf5c79fe1487a4c680f7f032a5cf5f6d8a8b0f9a1db723`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2901e38ec4493054d3c87cd872a25237bf3d3c288b4ea22daa082a138d547e`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 6.1 MB (6122105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1be5449fc2c85523492d3bef232de1436912215215ebe2290c4d72200c37a8`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a77e0718d9315a0c818af4496b9f586d37e405f08d097d780a98a720ca083`  
		Last Modified: Tue, 24 Feb 2026 20:56:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:cb5443a956dc6b17402568be81fdc4d1dceddaf5a9a8c1e80830778adf7c13fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c288a018da559cd12966f69462da3153dd292fc88c079f53872c384cafe584`

```dockerfile
```

-	Layers:
	-	`sha256:a1bb69f4f385138aac8ff6ced3ca7a83c6be173bd981f7afdb03355ac883324c`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 3.6 MB (3618587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae847d59a6c50e85cf74ae6eff5c381e8db42f1bda73d932082284f756252a8`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
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
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
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
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:b37d298bf05ecf3d2b1fa9ad6a1faa526d8f6ad09950fd1fa2f10a61cead55be
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
$ docker pull spiped@sha256:0d1c334e5c8c9a1482016dd7c81e161dab08a26a1f8537b7903432102d451868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36829432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c6e9fb649d94d08febe4acc1e055839a37da2c42592f79b234111a578fa779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:17:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:17:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:18:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:18:19 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:18:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:18:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f901b75fd05193d3ad4d413b9141afe4839c042a6371f33946fbe47efe47c`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee711db5622013b1d0a286930e78cc115b892e515bd2b74884d9706efb3fcc2`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ffcd4f57e39f1b0c6e284086b329aac3d99bba85f3d8db0a07595a3b7704c8`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 7.0 MB (7048432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa98f4373c484290992def4e28ca78f4d611794962d5e80e2376cbb0475460ad`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698f8b4f8d85c7878d49b3d09d4a893b1bbfb076376dfdfbcbdae85f7d1278c6`  
		Last Modified: Tue, 24 Feb 2026 19:18:27 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:913c8865c349f366c3068b316a5ecdb18147952dc0aee7498ad38e99e424b06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1b7e144e78fcc2cc2df9c9e685f4a7fbd06a5f02a9f6231eca16326e187f2c`

```dockerfile
```

-	Layers:
	-	`sha256:4454c48faf74e6d296f98d6d6999c3e74e9b7a952fbf069882d1f41396f4621a`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 3.6 MB (3626224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2bffe3af9f788104990231e51ee8e00bfd2bca6c9d6f3b403e15bf6420535a8`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:c4e19115468a9609ab171bfb50ba349826e5b45e0aee93bf7cd5c13048448787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e919cf4084856ae1dcbca01c72c1a632e39fd375cd01734ac8fef9eb6d3fe1a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:53:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:53:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:53:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:53:39 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:53:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:53:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c198268ff1c5ca902e3283584c9ed32fa711a2cf10e3a924ff5bd2c42e4b48`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cccb512fca00e135cec19f2482d6ec435eec15138610557719f7842baafe2a`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654e9a48c37c202be208834a489946cf92f91a21e6cf15c17458c02165e2c063`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 5.8 MB (5789288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada106fd65b27b787c26f0a28ce024f3ba38d1fa6788382cbb0c176a5142c9c8`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a890e111189051061b9f8bcbf2ebc36ac489e856bda9ca5d71a0187748d2e9`  
		Last Modified: Tue, 24 Feb 2026 19:53:47 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:69bfd3e675534ca1872423565cb1640224fd03ac12e3913a7f6b9c0477e6d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b529af9a3bf89decd1f57354fd1f1a906e3e7d32909d56eb13396576a55242`

```dockerfile
```

-	Layers:
	-	`sha256:ea0da76632dc1c96bb9c6034a4957d7c614ee95a93588db43bba8f29949a327b`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 3.6 MB (3619218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0052c2aa4ddf97f634cad7ee4a2fbf861200bc3f5215c162fddcafd2577fd480`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:b6c8d341f5e42f60a0ea6ad851c018181e69fd9af14df412cd8d0d32e5188c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7158910c12ab601276d7fa94f62712e71c7a62901875e8b0084e445ab0d0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:59:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:59:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:59:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:59:57 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:59:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:59:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b619584000476ce9b92659debeea088be8a3f430b26b3b31313373342bbe764`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cac6db5f98a1ac43951d2b2e3b1ed63a3ad80259e3697a344771a19cd25e7af`  
		Last Modified: Tue, 24 Feb 2026 20:00:09 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3783b0bb342b3a78b8cbf1594be27307eacf99849d98767eb175f5373dde825a`  
		Last Modified: Tue, 24 Feb 2026 20:00:08 GMT  
		Size: 5.6 MB (5584641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c493775ff90db9aebf059cbb6d4b754d5d3bde3cdba564acf5d5e4d9e37b8760`  
		Last Modified: Tue, 24 Feb 2026 20:00:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da041ec1755b24b1dce3f9967c76fbd9d57c7d5bc14a7a687f2a73c0224fe934`  
		Last Modified: Tue, 24 Feb 2026 20:00:13 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:8bc5e57bd6a8affda4eab4feb147fe074d6714e0cc5e5bf6df9b72cc33fc924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293b678e0d719326f722c4cbc6d18daa87f2885284d3f523040759c7f0759712`

```dockerfile
```

-	Layers:
	-	`sha256:38118694c8deba31fb2f231d972a1b717a7e67e99881f03bc3a1573404f45aa1`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 3.6 MB (3618339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbaada0809e420c18e0373cda990ad76cea3b71803f638ac0741a403e6c48a65`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0f1abb33a92e1c585ead9dddc782a7b66b51850c4d82d7cc27237227c94875b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922aacc7550a272b9c976c4ed76afd6391ea4e88703985dd28b31071794d21e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:23:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:23:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:23:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:23:37 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:23:37 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:23:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ed2ecdfd2e2a5f9323e19d20098f8653dfafed6a26430c6ae454d2c285fd60`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfac042c5cb69a73cdcc6401209530223ae8c8c236991e440eecc758484c451`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ce2e61248378161b4d55ebdf0a6f5a566384f9c5f5f84887f6505d2d5d4cf0`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 6.2 MB (6232845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1871ab8d2053ebe33f6b3c1de0922c3c4036ae5c6a842523e6e73fc1f7c132bb`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3db97a39d0d57606acb70e3b988bf408110a1ec22b13bd90b0096a6f468f843`  
		Last Modified: Tue, 24 Feb 2026 19:23:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:726f192ef59dd0155888ef52984e02bce8d56c8e760d571db4dbc610237b5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bece38d0e1923f09df6d6188b2fe9621a590b011c6f18a6fb0d8e405b0fb0545`

```dockerfile
```

-	Layers:
	-	`sha256:34056d5e6dfe40fbb3aa9127f1d4c4545ef508bcdd64942e6670e0b84ee7f50b`  
		Last Modified: Tue, 24 Feb 2026 19:23:45 GMT  
		Size: 3.6 MB (3621260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69d024a4e16fc1a11159aaf427a6ecb1c740e7895cc06b807a52218f1480b0a`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:a157a00a667365ab5ed49f538a1a066ce49e1b004687174fef8c5d8b78c706ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37738983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5e10b8ca505080c96ca00702e753b8e9e54423489cc23c1f0c286dab529b0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:24:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:24:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:24:36 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:24:36 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed616e6fff66cd009ec779287a335a2be1e348ccd44ede848d9d436cc00d6044`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8c64027cc40891219069c8ad75c2064da78484dd95ff0277a4d5355eee4657`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b943e889ee51e1ad6c052eb18cb8a96f04e76bdafac5e3c0a6a69af9be4709`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 6.4 MB (6442695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed5467f7f04ad6c5c280bcf57e7a06a73a52cbe23722ee9bb204d63f98f017`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb93962389450844c84c19f2b6e2a17ec6dc3d8347d2456ec18b4f24d31ed1d`  
		Last Modified: Tue, 24 Feb 2026 19:24:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:1b23c72b600c320cffa66a0c877dc6ce51fb20caa1f5c332464204a851f8fd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6273dbe2958ed3318df882a44802b0bffa3b69374c0b6c4360248913ec972185`

```dockerfile
```

-	Layers:
	-	`sha256:f25242888619593a7ea11ce819a23a144c545e563cfdb96d6a3be08ddafc7e8e`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 3.6 MB (3620353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c9e0d51a914006db4560e4405b97545e215d38cc392644f540f30511821acf`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:5b75c8c015774b8d23c079933627c1cc198b2ab1897e2ef9625ffe1a44e00abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40443061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4641f5e0942fce77295555370ecd0871fdbf48e9ca9f3c89303de4a4c16f22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:18:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 21:18:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:19:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 21:19:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:19:24 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 21:19:25 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 21:19:26 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:19:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:19:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032a2ca89d1a60962edc7ecaa5da32bbedd88b2d8b8010b10b80a7063ab6a42f`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352996af11d6ff12d58bc6f649d29adf801139a224b20d6d11f7986c3aa1a268`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a6629e08d34283ee8a3ea0798a9576779ff8dff51e7a37556b91251719aeb2`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 6.8 MB (6840475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d31d92746a14a820bd5990737171f219afdf1a48b9420be8522f528453432d`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad414bd9f5175c4827944d16ad82c7d0f33352e88b1729a3daa666a3fc94b177`  
		Last Modified: Tue, 24 Feb 2026 21:19:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:e4c070340a937f959027c51e25fcd835db51920ef30e24656d63af8e5e4c349f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f57a77227f8d58bfb6c9b06eeca3c5834f85771a2544714984c3f31e020c32d`

```dockerfile
```

-	Layers:
	-	`sha256:4e9cc3f215f4a204420884148121537cde4ff9af11a8cd76af0f3b5eefd7a5da`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 3.6 MB (3621961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967e301e427ae74d7411a5639dc6b5dc5825b933477bfe5d1e67465d3f44cd69`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; riscv64

```console
$ docker pull spiped@sha256:09783c4b01b0ff8c202fb26ef91603406e2758f0318b0f1daf6d42feb13c79cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37637171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a6aabadc5ebf87448c37f16f04e599fc861f845b9f3b472f2b434a320aea38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 03:04:18 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 05 Feb 2026 03:04:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 03:07:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 05 Feb 2026 03:07:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 05 Feb 2026 03:07:55 GMT
VOLUME [/spiped]
# Thu, 05 Feb 2026 03:07:56 GMT
WORKDIR /spiped
# Thu, 05 Feb 2026 03:07:56 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 03:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 03:07:56 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8525326a14b8a2f76773a30afbef5c22ed9293bc6da990616cbafd44ada6214f`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4056eefe513b961d3bd58ca86f11f00e23e0d20a44212052543469c3209f47c6`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890a93809726093bd14175f0ddafa3b16d2e6f70c6279892e2906c6e7e3ece54`  
		Last Modified: Thu, 05 Feb 2026 03:09:11 GMT  
		Size: 9.4 MB (9358421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd55e0daa803fb19a0d1715e1b6b4a1b0b8111069ec4577a82ece42bcf5008e`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92a4382dc33847551587860a6e2f0af1d60936e1a7941092fae0ce1280a219f`  
		Last Modified: Thu, 05 Feb 2026 03:09:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:1e373ded01a970ebae5566463fbec00e9be9dd80c27e8f97ff21da84ba19db68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45b45edd4dfa78a5d24882e4fa291588bb618a19aaccd25b531caf9219005b4`

```dockerfile
```

-	Layers:
	-	`sha256:a3c0166e8b9b6fb6b047956d064b1aa53ce13b39ee3103d5572cf70871221255`  
		Last Modified: Thu, 05 Feb 2026 03:09:10 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c49513027be2d086c9be28bf8525c760b6800b488fc7a207cdaa0fe79f30c69`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:d114290ecbbd13fe474f84310fb347e832e6bc85948a905227cda849a8ab28df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35962656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d4e52f7ccbd9605fa5fad30dda7622945ead71edb8113da175554ffe8e30ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:55:11 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 20:55:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 20:56:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 20:56:26 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 20:56:26 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:56:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e967cd97845f2bb25e9db030db7ed70580a36eeeacfcacabb36c6117e9a36938`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef093a72b4064b3aedf5c79fe1487a4c680f7f032a5cf5f6d8a8b0f9a1db723`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2901e38ec4493054d3c87cd872a25237bf3d3c288b4ea22daa082a138d547e`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 6.1 MB (6122105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1be5449fc2c85523492d3bef232de1436912215215ebe2290c4d72200c37a8`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a77e0718d9315a0c818af4496b9f586d37e405f08d097d780a98a720ca083`  
		Last Modified: Tue, 24 Feb 2026 20:56:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:cb5443a956dc6b17402568be81fdc4d1dceddaf5a9a8c1e80830778adf7c13fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c288a018da559cd12966f69462da3153dd292fc88c079f53872c384cafe584`

```dockerfile
```

-	Layers:
	-	`sha256:a1bb69f4f385138aac8ff6ced3ca7a83c6be173bd981f7afdb03355ac883324c`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 3.6 MB (3618587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae847d59a6c50e85cf74ae6eff5c381e8db42f1bda73d932082284f756252a8`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
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
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
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
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:b37d298bf05ecf3d2b1fa9ad6a1faa526d8f6ad09950fd1fa2f10a61cead55be
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
$ docker pull spiped@sha256:0d1c334e5c8c9a1482016dd7c81e161dab08a26a1f8537b7903432102d451868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36829432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c6e9fb649d94d08febe4acc1e055839a37da2c42592f79b234111a578fa779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:17:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:17:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:18:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:18:19 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:18:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:18:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f901b75fd05193d3ad4d413b9141afe4839c042a6371f33946fbe47efe47c`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee711db5622013b1d0a286930e78cc115b892e515bd2b74884d9706efb3fcc2`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ffcd4f57e39f1b0c6e284086b329aac3d99bba85f3d8db0a07595a3b7704c8`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 7.0 MB (7048432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa98f4373c484290992def4e28ca78f4d611794962d5e80e2376cbb0475460ad`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698f8b4f8d85c7878d49b3d09d4a893b1bbfb076376dfdfbcbdae85f7d1278c6`  
		Last Modified: Tue, 24 Feb 2026 19:18:27 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:913c8865c349f366c3068b316a5ecdb18147952dc0aee7498ad38e99e424b06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1b7e144e78fcc2cc2df9c9e685f4a7fbd06a5f02a9f6231eca16326e187f2c`

```dockerfile
```

-	Layers:
	-	`sha256:4454c48faf74e6d296f98d6d6999c3e74e9b7a952fbf069882d1f41396f4621a`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 3.6 MB (3626224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2bffe3af9f788104990231e51ee8e00bfd2bca6c9d6f3b403e15bf6420535a8`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:c4e19115468a9609ab171bfb50ba349826e5b45e0aee93bf7cd5c13048448787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e919cf4084856ae1dcbca01c72c1a632e39fd375cd01734ac8fef9eb6d3fe1a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:53:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:53:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:53:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:53:39 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:53:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:53:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c198268ff1c5ca902e3283584c9ed32fa711a2cf10e3a924ff5bd2c42e4b48`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cccb512fca00e135cec19f2482d6ec435eec15138610557719f7842baafe2a`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654e9a48c37c202be208834a489946cf92f91a21e6cf15c17458c02165e2c063`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 5.8 MB (5789288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada106fd65b27b787c26f0a28ce024f3ba38d1fa6788382cbb0c176a5142c9c8`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a890e111189051061b9f8bcbf2ebc36ac489e856bda9ca5d71a0187748d2e9`  
		Last Modified: Tue, 24 Feb 2026 19:53:47 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:69bfd3e675534ca1872423565cb1640224fd03ac12e3913a7f6b9c0477e6d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b529af9a3bf89decd1f57354fd1f1a906e3e7d32909d56eb13396576a55242`

```dockerfile
```

-	Layers:
	-	`sha256:ea0da76632dc1c96bb9c6034a4957d7c614ee95a93588db43bba8f29949a327b`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 3.6 MB (3619218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0052c2aa4ddf97f634cad7ee4a2fbf861200bc3f5215c162fddcafd2577fd480`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:b6c8d341f5e42f60a0ea6ad851c018181e69fd9af14df412cd8d0d32e5188c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7158910c12ab601276d7fa94f62712e71c7a62901875e8b0084e445ab0d0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:59:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:59:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:59:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:59:57 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:59:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:59:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b619584000476ce9b92659debeea088be8a3f430b26b3b31313373342bbe764`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cac6db5f98a1ac43951d2b2e3b1ed63a3ad80259e3697a344771a19cd25e7af`  
		Last Modified: Tue, 24 Feb 2026 20:00:09 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3783b0bb342b3a78b8cbf1594be27307eacf99849d98767eb175f5373dde825a`  
		Last Modified: Tue, 24 Feb 2026 20:00:08 GMT  
		Size: 5.6 MB (5584641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c493775ff90db9aebf059cbb6d4b754d5d3bde3cdba564acf5d5e4d9e37b8760`  
		Last Modified: Tue, 24 Feb 2026 20:00:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da041ec1755b24b1dce3f9967c76fbd9d57c7d5bc14a7a687f2a73c0224fe934`  
		Last Modified: Tue, 24 Feb 2026 20:00:13 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:8bc5e57bd6a8affda4eab4feb147fe074d6714e0cc5e5bf6df9b72cc33fc924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293b678e0d719326f722c4cbc6d18daa87f2885284d3f523040759c7f0759712`

```dockerfile
```

-	Layers:
	-	`sha256:38118694c8deba31fb2f231d972a1b717a7e67e99881f03bc3a1573404f45aa1`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 3.6 MB (3618339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbaada0809e420c18e0373cda990ad76cea3b71803f638ac0741a403e6c48a65`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0f1abb33a92e1c585ead9dddc782a7b66b51850c4d82d7cc27237227c94875b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922aacc7550a272b9c976c4ed76afd6391ea4e88703985dd28b31071794d21e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:23:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:23:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:23:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:23:37 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:23:37 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:23:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ed2ecdfd2e2a5f9323e19d20098f8653dfafed6a26430c6ae454d2c285fd60`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfac042c5cb69a73cdcc6401209530223ae8c8c236991e440eecc758484c451`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ce2e61248378161b4d55ebdf0a6f5a566384f9c5f5f84887f6505d2d5d4cf0`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 6.2 MB (6232845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1871ab8d2053ebe33f6b3c1de0922c3c4036ae5c6a842523e6e73fc1f7c132bb`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3db97a39d0d57606acb70e3b988bf408110a1ec22b13bd90b0096a6f468f843`  
		Last Modified: Tue, 24 Feb 2026 19:23:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:726f192ef59dd0155888ef52984e02bce8d56c8e760d571db4dbc610237b5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bece38d0e1923f09df6d6188b2fe9621a590b011c6f18a6fb0d8e405b0fb0545`

```dockerfile
```

-	Layers:
	-	`sha256:34056d5e6dfe40fbb3aa9127f1d4c4545ef508bcdd64942e6670e0b84ee7f50b`  
		Last Modified: Tue, 24 Feb 2026 19:23:45 GMT  
		Size: 3.6 MB (3621260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69d024a4e16fc1a11159aaf427a6ecb1c740e7895cc06b807a52218f1480b0a`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:a157a00a667365ab5ed49f538a1a066ce49e1b004687174fef8c5d8b78c706ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37738983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5e10b8ca505080c96ca00702e753b8e9e54423489cc23c1f0c286dab529b0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:24:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:24:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:24:36 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:24:36 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed616e6fff66cd009ec779287a335a2be1e348ccd44ede848d9d436cc00d6044`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8c64027cc40891219069c8ad75c2064da78484dd95ff0277a4d5355eee4657`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b943e889ee51e1ad6c052eb18cb8a96f04e76bdafac5e3c0a6a69af9be4709`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 6.4 MB (6442695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed5467f7f04ad6c5c280bcf57e7a06a73a52cbe23722ee9bb204d63f98f017`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb93962389450844c84c19f2b6e2a17ec6dc3d8347d2456ec18b4f24d31ed1d`  
		Last Modified: Tue, 24 Feb 2026 19:24:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:1b23c72b600c320cffa66a0c877dc6ce51fb20caa1f5c332464204a851f8fd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6273dbe2958ed3318df882a44802b0bffa3b69374c0b6c4360248913ec972185`

```dockerfile
```

-	Layers:
	-	`sha256:f25242888619593a7ea11ce819a23a144c545e563cfdb96d6a3be08ddafc7e8e`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 3.6 MB (3620353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c9e0d51a914006db4560e4405b97545e215d38cc392644f540f30511821acf`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:5b75c8c015774b8d23c079933627c1cc198b2ab1897e2ef9625ffe1a44e00abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40443061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4641f5e0942fce77295555370ecd0871fdbf48e9ca9f3c89303de4a4c16f22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:18:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 21:18:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:19:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 21:19:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:19:24 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 21:19:25 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 21:19:26 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:19:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:19:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032a2ca89d1a60962edc7ecaa5da32bbedd88b2d8b8010b10b80a7063ab6a42f`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352996af11d6ff12d58bc6f649d29adf801139a224b20d6d11f7986c3aa1a268`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a6629e08d34283ee8a3ea0798a9576779ff8dff51e7a37556b91251719aeb2`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 6.8 MB (6840475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d31d92746a14a820bd5990737171f219afdf1a48b9420be8522f528453432d`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad414bd9f5175c4827944d16ad82c7d0f33352e88b1729a3daa666a3fc94b177`  
		Last Modified: Tue, 24 Feb 2026 21:19:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:e4c070340a937f959027c51e25fcd835db51920ef30e24656d63af8e5e4c349f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f57a77227f8d58bfb6c9b06eeca3c5834f85771a2544714984c3f31e020c32d`

```dockerfile
```

-	Layers:
	-	`sha256:4e9cc3f215f4a204420884148121537cde4ff9af11a8cd76af0f3b5eefd7a5da`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 3.6 MB (3621961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967e301e427ae74d7411a5639dc6b5dc5825b933477bfe5d1e67465d3f44cd69`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; riscv64

```console
$ docker pull spiped@sha256:09783c4b01b0ff8c202fb26ef91603406e2758f0318b0f1daf6d42feb13c79cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37637171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a6aabadc5ebf87448c37f16f04e599fc861f845b9f3b472f2b434a320aea38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 03:04:18 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 05 Feb 2026 03:04:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 03:07:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 05 Feb 2026 03:07:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 05 Feb 2026 03:07:55 GMT
VOLUME [/spiped]
# Thu, 05 Feb 2026 03:07:56 GMT
WORKDIR /spiped
# Thu, 05 Feb 2026 03:07:56 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 03:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 03:07:56 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8525326a14b8a2f76773a30afbef5c22ed9293bc6da990616cbafd44ada6214f`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4056eefe513b961d3bd58ca86f11f00e23e0d20a44212052543469c3209f47c6`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890a93809726093bd14175f0ddafa3b16d2e6f70c6279892e2906c6e7e3ece54`  
		Last Modified: Thu, 05 Feb 2026 03:09:11 GMT  
		Size: 9.4 MB (9358421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd55e0daa803fb19a0d1715e1b6b4a1b0b8111069ec4577a82ece42bcf5008e`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92a4382dc33847551587860a6e2f0af1d60936e1a7941092fae0ce1280a219f`  
		Last Modified: Thu, 05 Feb 2026 03:09:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:1e373ded01a970ebae5566463fbec00e9be9dd80c27e8f97ff21da84ba19db68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45b45edd4dfa78a5d24882e4fa291588bb618a19aaccd25b531caf9219005b4`

```dockerfile
```

-	Layers:
	-	`sha256:a3c0166e8b9b6fb6b047956d064b1aa53ce13b39ee3103d5572cf70871221255`  
		Last Modified: Thu, 05 Feb 2026 03:09:10 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c49513027be2d086c9be28bf8525c760b6800b488fc7a207cdaa0fe79f30c69`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:d114290ecbbd13fe474f84310fb347e832e6bc85948a905227cda849a8ab28df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35962656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d4e52f7ccbd9605fa5fad30dda7622945ead71edb8113da175554ffe8e30ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:55:11 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 20:55:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 20:56:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 20:56:26 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 20:56:26 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:56:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e967cd97845f2bb25e9db030db7ed70580a36eeeacfcacabb36c6117e9a36938`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef093a72b4064b3aedf5c79fe1487a4c680f7f032a5cf5f6d8a8b0f9a1db723`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2901e38ec4493054d3c87cd872a25237bf3d3c288b4ea22daa082a138d547e`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 6.1 MB (6122105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1be5449fc2c85523492d3bef232de1436912215215ebe2290c4d72200c37a8`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a77e0718d9315a0c818af4496b9f586d37e405f08d097d780a98a720ca083`  
		Last Modified: Tue, 24 Feb 2026 20:56:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:cb5443a956dc6b17402568be81fdc4d1dceddaf5a9a8c1e80830778adf7c13fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c288a018da559cd12966f69462da3153dd292fc88c079f53872c384cafe584`

```dockerfile
```

-	Layers:
	-	`sha256:a1bb69f4f385138aac8ff6ced3ca7a83c6be173bd981f7afdb03355ac883324c`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 3.6 MB (3618587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae847d59a6c50e85cf74ae6eff5c381e8db42f1bda73d932082284f756252a8`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
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
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
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
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:2e861202f057586ae2e6dc3a5290d61949120d861e272b5700c1e30e1ae9774c
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
$ docker pull spiped@sha256:45aa25e16b20aaf22415c03717dfbffb2460250d93ccfbf50d304296f0323560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c42c3ad8f87ea2a2987c07857dc357c5caa6eb7fe68f8ab758c81d2c67f6316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:36:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:36:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:36:57 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:36:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255f2b198269941f9011d88cebad6e20b25c8054b5ac4ebd1b07f9750a69d255`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed562f6049bf766f9af2aeb064224279b938162b44667a74bc7ca9c31ac1d70a`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 7.9 KB (7945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20d0ab7b6d45d1dbeebe557e32936e50678b9985769e6bd0ff3e1ff5e433e69`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 107.6 KB (107647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868415b885be47751e88ed3c97ca195abec55deffeb9f4ad2846ad3d25cdec28`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8f030e4a64f48108d2120539708364c71dc39133649b15a0ad263ec9bfe40`  
		Last Modified: Wed, 28 Jan 2026 02:37:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:14bccfab21e7b3f36806b9521edfd711ef99c418ce1a38f2c913859e95caa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f387ff25d96b6eec2a5942d1be095ce8d2cd8945dadefd293a3706d31ea69`

```dockerfile
```

-	Layers:
	-	`sha256:3abca7ed4aae68f57768d18d39b5d6b1c58a733af4507188677241020e39e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6768ac276576d5f59511c63ded4afa12e2d77d28be7bffc6d1537d58bb57bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:03 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3840e207c5f175385b57ca037766c41623e4a780197b93760ca83297bd8e51ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07ce0978d45ec15bdc0a08bdc59ff908f2bd78005af85d4bbad7345be081ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:33 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:44 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:44 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5ad93e4f03c704fabcd2728cb1ab8244c96ef0876f3fcc9779085a8d3be96`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092107d3ff0fcf3229ae39acf729a354fda97b10c713e7073d550bb7c69025bc`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb00245db6ff8769dfa116d0e6194c8908449cd54b3995e5f0044b278d0fb45`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3375ee92dad5bd59b0dde03ad45bdf7a8f7df3aaa1e2847b17cdd6734893cfb8`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc41431154f4cccb130328f9bda92ac3cd374c3bc4ef8b29827399ebd22bc749`  
		Last Modified: Wed, 28 Jan 2026 02:56:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:193c4ff5e06269d1446ab3235284aa43d244fdbc13dffdc98c715540fcc455e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b8b064e4aba529d56ef354367ffae940f6b152b36f64ea427dfcd51e51f1e`

```dockerfile
```

-	Layers:
	-	`sha256:9257c6b08dae939c45fb6b5cd969064dde84328d15653df8b0ab98dae6b31d32`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 14.1 KB (14146 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:71592cfee4b071cad3b52c3cfdefddd8ff72e3d5e644d8859d2d8cec8397a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3314649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c48ddb927471eeb09c0d2e183b02bb1074d36b5caa9dbd3477ee935a8eed01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:56:25 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:56:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:56:34 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:56:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:56:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba379620ebeacb95d57ee5ff3ce395b9868fe9f8d00a5b85dd41df19b3a23`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e6c87dbde5f46d8cd1e26b6a653a7d77209c851df54df0c065355b1c36749`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e2b19aaa32cc304579e079305131ee112e7015524177e84f33379315c24f6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 81.7 KB (81685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d229583db181996be822e85b4fe259ecd55350b04637a090977de317d8cb53`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283dd24da1a4b40bed9d28f9196f24341abf5ee8a13f180db2b3e6daa7e85b8d`  
		Last Modified: Wed, 28 Jan 2026 02:56:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b0d30665b0b25a584022937647a82e260a99dc3822f06eae03c777c08c589459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de7b9137b4705f6bfaa43d68be9ab47cda877656a88568a8b98eaecf834d723`

```dockerfile
```

-	Layers:
	-	`sha256:bf20f6c9425bc14bf83c368ad820cbac85037f9cfe9e8f428105dcae79aa5f0a`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c326467351e8aaa1070327395a8ce06feaf36e791288cc8d0efc059293853a6`  
		Last Modified: Wed, 28 Jan 2026 02:56:39 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:effcfa5e900325dc5a9f2ce725d32bb928170b9fae13c2414035f7c74db4832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129da21c1ac14cfe9747c51280fa104e3e2a4a7fb499fce9d2f79394c096e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 02:37:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 02:37:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 02:37:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 02:37:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:37:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215f43d3f31692bff6dbb7a8464a9777ff146fd6817d85616dd79d628db9a4e`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a149826e8201bd60e39e8acb8c71ee749c537b2c783a541e04af7a7b3fc6b5d`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3816514d66f19e4e15afc0dae177ea8f1397bbaeba0189b4a33a3f265afbb21`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 100.6 KB (100615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073eca19d0c28ea18c16d7aa1388a52393935ac0e76036549b53fca85d50741`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae442366147b99273aabaaf180c7a0347dd957817ff21ec6495a8f374fd7b5`  
		Last Modified: Wed, 28 Jan 2026 02:38:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:20c426c97f5ccc77dcb4c2895905f7a3e9aedaf5bf12fbf4b3ff87748f7ebc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f74a0ff8267a4110c62ab6dcdcf2bf4949f9f54a7ff5e5b96a7e78b99f9770c`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e8f74c44956e8b3a9213e0686a5007c77ddc5cd5210760e512537c99dcb4f`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744a1e9a5178b40c2e43ceccdad37fa256e17fb5a7e73342aa361c38b071ea6`  
		Last Modified: Wed, 28 Jan 2026 02:38:00 GMT  
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
$ docker pull spiped@sha256:ec49e51d1b31aef6ee4c32cbd2374c5115032febd535905c0146f19ca7d1b88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e05f6841b2c0f9dcb913e52c349b3ec2747c75f53e9b3d6a41cd3c6103a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:19 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:59:21 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:59:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:59:33 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:59:33 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:59:34 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:59:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52389dd33bb155b2c78fa5202c8c9909e97b12049d41f7cb5369100d2a7be819`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd5646a7c2ce724b02160a31080c85b3571ffddbc309ccb39fb23e5075d4aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:47 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83f042b4cb936ae2f704768b0462b7f539ba799143799dc6a8ce0babc73884`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 112.7 KB (112673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f4a6884030927f7cdd451b10bba40c6cf61fd40534ca3a9cf653bb742ea8f`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbfb80739dd4ce26eb065be080a75c602340f3242a297925caf40baf400db0`  
		Last Modified: Wed, 28 Jan 2026 03:59:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1d08517919e2dfe608c1e408886b7ef4659cd9f15bf49a67583fe931eb307650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68d34137d518c2381ecd841ecef0a23786265f08c1952e0ed2134cc2ba9073`

```dockerfile
```

-	Layers:
	-	`sha256:b57bb2bf93c55cd637df776032387ee2beae0039a87bacf4e588dd43aaa36711`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a73d72709b0315e9f657137bb6dbf7c0679131d8e10876ea8a1bb94e4201b4`  
		Last Modified: Wed, 28 Jan 2026 03:59:48 GMT  
		Size: 14.3 KB (14303 bytes)  
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
$ docker pull spiped@sha256:0aeb96b9c7c968a0ad51a4c785e0c76534a115d395c587eacd587a3aad55b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72691935166b1882b3040950315ed19d9cf1a3678909a868fa5c27a1a58e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 28 Jan 2026 03:05:48 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 28 Jan 2026 03:05:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
VOLUME [/spiped]
# Wed, 28 Jan 2026 03:05:55 GMT
WORKDIR /spiped
# Wed, 28 Jan 2026 03:05:55 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0789ee1817b07966cd80a07b05a82d8e0c9bf85f6053f4955ac4731e47448ad`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526c5a7e2d6f02b24c7ed3860ec8221dcd7d0c6e4112d267da6729a13890448`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10bca7622d69f6335c554b1c8cec2a82753df66ed9cf072d635820439e1af3c`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.9 KB (96933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d81cea7ec993f5c76e72bd06b1579e878f6a4d1a4a2f11114f710747ef40d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ab53d5ebb5741d97d120d1a1ad7797bf2fda46a7ff1f9a033efa0117cd233`  
		Last Modified: Wed, 28 Jan 2026 03:06:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c32f5675d459d866b7c69b2159549861b770e81fa270485088e909f23c515b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76bce779a8727519c7fb65566c2ce929337d21a3d6addd2f301cd51f95516c4`

```dockerfile
```

-	Layers:
	-	`sha256:85780af5cccece93dbeac028f8517ebc14f3298ca69ddd75bcf80809c0ea3432`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797300601f0f43bd14d2b3e327c7100b2a1b8356e4290096f308e710af773718`  
		Last Modified: Wed, 28 Jan 2026 03:06:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:b37d298bf05ecf3d2b1fa9ad6a1faa526d8f6ad09950fd1fa2f10a61cead55be
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
$ docker pull spiped@sha256:0d1c334e5c8c9a1482016dd7c81e161dab08a26a1f8537b7903432102d451868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36829432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c6e9fb649d94d08febe4acc1e055839a37da2c42592f79b234111a578fa779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:17:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:17:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:18:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:18:19 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:18:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:18:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:18:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f901b75fd05193d3ad4d413b9141afe4839c042a6371f33946fbe47efe47c`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee711db5622013b1d0a286930e78cc115b892e515bd2b74884d9706efb3fcc2`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ffcd4f57e39f1b0c6e284086b329aac3d99bba85f3d8db0a07595a3b7704c8`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 7.0 MB (7048432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa98f4373c484290992def4e28ca78f4d611794962d5e80e2376cbb0475460ad`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698f8b4f8d85c7878d49b3d09d4a893b1bbfb076376dfdfbcbdae85f7d1278c6`  
		Last Modified: Tue, 24 Feb 2026 19:18:27 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:913c8865c349f366c3068b316a5ecdb18147952dc0aee7498ad38e99e424b06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1b7e144e78fcc2cc2df9c9e685f4a7fbd06a5f02a9f6231eca16326e187f2c`

```dockerfile
```

-	Layers:
	-	`sha256:4454c48faf74e6d296f98d6d6999c3e74e9b7a952fbf069882d1f41396f4621a`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 3.6 MB (3626224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2bffe3af9f788104990231e51ee8e00bfd2bca6c9d6f3b403e15bf6420535a8`  
		Last Modified: Tue, 24 Feb 2026 19:18:26 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:c4e19115468a9609ab171bfb50ba349826e5b45e0aee93bf7cd5c13048448787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33739270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e919cf4084856ae1dcbca01c72c1a632e39fd375cd01734ac8fef9eb6d3fe1a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:53:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:53:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:53:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:53:39 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:53:39 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:53:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:53:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c198268ff1c5ca902e3283584c9ed32fa711a2cf10e3a924ff5bd2c42e4b48`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cccb512fca00e135cec19f2482d6ec435eec15138610557719f7842baafe2a`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654e9a48c37c202be208834a489946cf92f91a21e6cf15c17458c02165e2c063`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 5.8 MB (5789288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada106fd65b27b787c26f0a28ce024f3ba38d1fa6788382cbb0c176a5142c9c8`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a890e111189051061b9f8bcbf2ebc36ac489e856bda9ca5d71a0187748d2e9`  
		Last Modified: Tue, 24 Feb 2026 19:53:47 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:69bfd3e675534ca1872423565cb1640224fd03ac12e3913a7f6b9c0477e6d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b529af9a3bf89decd1f57354fd1f1a906e3e7d32909d56eb13396576a55242`

```dockerfile
```

-	Layers:
	-	`sha256:ea0da76632dc1c96bb9c6034a4957d7c614ee95a93588db43bba8f29949a327b`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 3.6 MB (3619218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0052c2aa4ddf97f634cad7ee4a2fbf861200bc3f5215c162fddcafd2577fd480`  
		Last Modified: Tue, 24 Feb 2026 19:53:46 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:b6c8d341f5e42f60a0ea6ad851c018181e69fd9af14df412cd8d0d32e5188c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7158910c12ab601276d7fa94f62712e71c7a62901875e8b0084e445ab0d0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:59:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:59:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:59:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:59:57 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:59:57 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:59:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:59:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b619584000476ce9b92659debeea088be8a3f430b26b3b31313373342bbe764`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cac6db5f98a1ac43951d2b2e3b1ed63a3ad80259e3697a344771a19cd25e7af`  
		Last Modified: Tue, 24 Feb 2026 20:00:09 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3783b0bb342b3a78b8cbf1594be27307eacf99849d98767eb175f5373dde825a`  
		Last Modified: Tue, 24 Feb 2026 20:00:08 GMT  
		Size: 5.6 MB (5584641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c493775ff90db9aebf059cbb6d4b754d5d3bde3cdba564acf5d5e4d9e37b8760`  
		Last Modified: Tue, 24 Feb 2026 20:00:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da041ec1755b24b1dce3f9967c76fbd9d57c7d5bc14a7a687f2a73c0224fe934`  
		Last Modified: Tue, 24 Feb 2026 20:00:13 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:8bc5e57bd6a8affda4eab4feb147fe074d6714e0cc5e5bf6df9b72cc33fc924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293b678e0d719326f722c4cbc6d18daa87f2885284d3f523040759c7f0759712`

```dockerfile
```

-	Layers:
	-	`sha256:38118694c8deba31fb2f231d972a1b717a7e67e99881f03bc3a1573404f45aa1`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 3.6 MB (3618339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbaada0809e420c18e0373cda990ad76cea3b71803f638ac0741a403e6c48a65`  
		Last Modified: Tue, 24 Feb 2026 20:00:07 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0f1abb33a92e1c585ead9dddc782a7b66b51850c4d82d7cc27237227c94875b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922aacc7550a272b9c976c4ed76afd6391ea4e88703985dd28b31071794d21e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:23:12 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:23:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:23:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:23:37 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:23:37 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:23:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:23:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ed2ecdfd2e2a5f9323e19d20098f8653dfafed6a26430c6ae454d2c285fd60`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfac042c5cb69a73cdcc6401209530223ae8c8c236991e440eecc758484c451`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ce2e61248378161b4d55ebdf0a6f5a566384f9c5f5f84887f6505d2d5d4cf0`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 6.2 MB (6232845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1871ab8d2053ebe33f6b3c1de0922c3c4036ae5c6a842523e6e73fc1f7c132bb`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3db97a39d0d57606acb70e3b988bf408110a1ec22b13bd90b0096a6f468f843`  
		Last Modified: Tue, 24 Feb 2026 19:23:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:726f192ef59dd0155888ef52984e02bce8d56c8e760d571db4dbc610237b5ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bece38d0e1923f09df6d6188b2fe9621a590b011c6f18a6fb0d8e405b0fb0545`

```dockerfile
```

-	Layers:
	-	`sha256:34056d5e6dfe40fbb3aa9127f1d4c4545ef508bcdd64942e6670e0b84ee7f50b`  
		Last Modified: Tue, 24 Feb 2026 19:23:45 GMT  
		Size: 3.6 MB (3621260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69d024a4e16fc1a11159aaf427a6ecb1c740e7895cc06b807a52218f1480b0a`  
		Last Modified: Tue, 24 Feb 2026 19:23:44 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:a157a00a667365ab5ed49f538a1a066ce49e1b004687174fef8c5d8b78c706ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37738983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5e10b8ca505080c96ca00702e753b8e9e54423489cc23c1f0c286dab529b0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:09 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 19:24:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 19:24:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 19:24:36 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 19:24:36 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed616e6fff66cd009ec779287a335a2be1e348ccd44ede848d9d436cc00d6044`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8c64027cc40891219069c8ad75c2064da78484dd95ff0277a4d5355eee4657`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b943e889ee51e1ad6c052eb18cb8a96f04e76bdafac5e3c0a6a69af9be4709`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 6.4 MB (6442695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed5467f7f04ad6c5c280bcf57e7a06a73a52cbe23722ee9bb204d63f98f017`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb93962389450844c84c19f2b6e2a17ec6dc3d8347d2456ec18b4f24d31ed1d`  
		Last Modified: Tue, 24 Feb 2026 19:24:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:1b23c72b600c320cffa66a0c877dc6ce51fb20caa1f5c332464204a851f8fd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6273dbe2958ed3318df882a44802b0bffa3b69374c0b6c4360248913ec972185`

```dockerfile
```

-	Layers:
	-	`sha256:f25242888619593a7ea11ce819a23a144c545e563cfdb96d6a3be08ddafc7e8e`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 3.6 MB (3620353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c9e0d51a914006db4560e4405b97545e215d38cc392644f540f30511821acf`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 14.9 KB (14946 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:5b75c8c015774b8d23c079933627c1cc198b2ab1897e2ef9625ffe1a44e00abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40443061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4641f5e0942fce77295555370ecd0871fdbf48e9ca9f3c89303de4a4c16f22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:18:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 21:18:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:19:24 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 21:19:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:19:24 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 21:19:25 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 21:19:26 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:19:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:19:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032a2ca89d1a60962edc7ecaa5da32bbedd88b2d8b8010b10b80a7063ab6a42f`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352996af11d6ff12d58bc6f649d29adf801139a224b20d6d11f7986c3aa1a268`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a6629e08d34283ee8a3ea0798a9576779ff8dff51e7a37556b91251719aeb2`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 6.8 MB (6840475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d31d92746a14a820bd5990737171f219afdf1a48b9420be8522f528453432d`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad414bd9f5175c4827944d16ad82c7d0f33352e88b1729a3daa666a3fc94b177`  
		Last Modified: Tue, 24 Feb 2026 21:19:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:e4c070340a937f959027c51e25fcd835db51920ef30e24656d63af8e5e4c349f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f57a77227f8d58bfb6c9b06eeca3c5834f85771a2544714984c3f31e020c32d`

```dockerfile
```

-	Layers:
	-	`sha256:4e9cc3f215f4a204420884148121537cde4ff9af11a8cd76af0f3b5eefd7a5da`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 3.6 MB (3621961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967e301e427ae74d7411a5639dc6b5dc5825b933477bfe5d1e67465d3f44cd69`  
		Last Modified: Tue, 24 Feb 2026 21:19:41 GMT  
		Size: 15.0 KB (15029 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:09783c4b01b0ff8c202fb26ef91603406e2758f0318b0f1daf6d42feb13c79cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37637171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a6aabadc5ebf87448c37f16f04e599fc861f845b9f3b472f2b434a320aea38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 03:04:18 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Thu, 05 Feb 2026 03:04:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 03:07:55 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Thu, 05 Feb 2026 03:07:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 05 Feb 2026 03:07:55 GMT
VOLUME [/spiped]
# Thu, 05 Feb 2026 03:07:56 GMT
WORKDIR /spiped
# Thu, 05 Feb 2026 03:07:56 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 03:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 03:07:56 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8525326a14b8a2f76773a30afbef5c22ed9293bc6da990616cbafd44ada6214f`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4056eefe513b961d3bd58ca86f11f00e23e0d20a44212052543469c3209f47c6`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890a93809726093bd14175f0ddafa3b16d2e6f70c6279892e2906c6e7e3ece54`  
		Last Modified: Thu, 05 Feb 2026 03:09:11 GMT  
		Size: 9.4 MB (9358421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd55e0daa803fb19a0d1715e1b6b4a1b0b8111069ec4577a82ece42bcf5008e`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92a4382dc33847551587860a6e2f0af1d60936e1a7941092fae0ce1280a219f`  
		Last Modified: Thu, 05 Feb 2026 03:09:11 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:1e373ded01a970ebae5566463fbec00e9be9dd80c27e8f97ff21da84ba19db68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45b45edd4dfa78a5d24882e4fa291588bb618a19aaccd25b531caf9219005b4`

```dockerfile
```

-	Layers:
	-	`sha256:a3c0166e8b9b6fb6b047956d064b1aa53ce13b39ee3103d5572cf70871221255`  
		Last Modified: Thu, 05 Feb 2026 03:09:10 GMT  
		Size: 3.6 MB (3613367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c49513027be2d086c9be28bf8525c760b6800b488fc7a207cdaa0fe79f30c69`  
		Last Modified: Thu, 05 Feb 2026 03:09:09 GMT  
		Size: 15.0 KB (15030 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:d114290ecbbd13fe474f84310fb347e832e6bc85948a905227cda849a8ab28df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35962656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d4e52f7ccbd9605fa5fad30dda7622945ead71edb8113da175554ffe8e30ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:55:11 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 24 Feb 2026 20:55:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 24 Feb 2026 20:56:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
VOLUME [/spiped]
# Tue, 24 Feb 2026 20:56:26 GMT
WORKDIR /spiped
# Tue, 24 Feb 2026 20:56:26 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:56:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e967cd97845f2bb25e9db030db7ed70580a36eeeacfcacabb36c6117e9a36938`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef093a72b4064b3aedf5c79fe1487a4c680f7f032a5cf5f6d8a8b0f9a1db723`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2901e38ec4493054d3c87cd872a25237bf3d3c288b4ea22daa082a138d547e`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 6.1 MB (6122105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1be5449fc2c85523492d3bef232de1436912215215ebe2290c4d72200c37a8`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a77e0718d9315a0c818af4496b9f586d37e405f08d097d780a98a720ca083`  
		Last Modified: Tue, 24 Feb 2026 20:56:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:cb5443a956dc6b17402568be81fdc4d1dceddaf5a9a8c1e80830778adf7c13fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c288a018da559cd12966f69462da3153dd292fc88c079f53872c384cafe584`

```dockerfile
```

-	Layers:
	-	`sha256:a1bb69f4f385138aac8ff6ced3ca7a83c6be173bd981f7afdb03355ac883324c`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 3.6 MB (3618587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae847d59a6c50e85cf74ae6eff5c381e8db42f1bda73d932082284f756252a8`  
		Last Modified: Tue, 24 Feb 2026 20:56:44 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
