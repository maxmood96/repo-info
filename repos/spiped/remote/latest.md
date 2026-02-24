## `spiped:latest`

```console
$ docker pull spiped@sha256:81478be1351476b40ae9ff4f498bbae85f763e3ed58ee23ad814de2284a3fe13
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
$ docker pull spiped@sha256:00be49bc99e5b1b637212c605b1848e0b4df978cc1034499cfaea49b6cacb195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40442941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a74d36a815a80a1ee0731f7f9d410231c3f06cd8ffce9e56ec21426052cdbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:21:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 05:21:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:22:15 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 05:22:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 05:22:15 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 05:22:15 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 05:22:16 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:22:16 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54dfec51c06ef5546fc59a333f4b2a700322fc6c08919bf3a34ec2a5634f7b3`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb6ba71a55079b27d2707951a5de51bb2735b3c843e7de0603e966f576a4b42`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa10d34f820fe96de44722a9d2956fd2fffb6c97bfdedbe70eefe38c76f4e372`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 6.8 MB (6840384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a84985e24e00269a3c8628e7ff0586606414c566bc3a545ceb82366fca76b2`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36df81ecd8796a18c1949857ba62294cf17fe04d7c01f5794facab1eed173ad0`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:e34582c751fb4395383437efc5f2ec1e67212bcb14fbc6d710ccd948b6b76e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14889a1d30656cb6f7af02127fae886ef833336f77c621279f791307c5b87a66`

```dockerfile
```

-	Layers:
	-	`sha256:34553b7d1a70804c1f632c8f54460c9d539a26a9f51085d8abdbb770a45417b8`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 3.6 MB (3621961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef2dc18746c6c4784daccf3fb9a520974f92134b86634839540e539c353f9b8`  
		Last Modified: Tue, 03 Feb 2026 05:22:30 GMT  
		Size: 15.0 KB (15030 bytes)  
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
$ docker pull spiped@sha256:138fe4dcc8fb5c0df1a9fe39769aa482f8103179104fb7822432be26d9dc06f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35962521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2d8e7d46dd49c524188f2706e57f1bf10de8a88227685ba47956a2187b9e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:43:35 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Tue, 03 Feb 2026 03:43:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Tue, 03 Feb 2026 03:43:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
VOLUME [/spiped]
# Tue, 03 Feb 2026 03:43:54 GMT
WORKDIR /spiped
# Tue, 03 Feb 2026 03:43:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:43:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb804f8c11f523ce62a7bc09d236baf84abd6e284119dc6e7c812b046ba3ce`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8af71d5729ead8e60802ee40cd20b30288f02d50d14e682fc9af8c7a6aae22`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4467051214cb85c78e6cb79968f755a9833b4b38239855bb9eaca4f83bb5bd`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 6.1 MB (6121999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099202750066c7aa99797cb9282aa06e8187d7a87d111d1af849e70e955f5045`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd30b70482ee075552a0a8c1163f912098b4cfc94f09bb564d7846c8ae6ac9b`  
		Last Modified: Tue, 03 Feb 2026 03:44:06 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:00b19a2ff8b9daff2d46f3641d4e0f1be5d24395d4dfe12e381a836c8ac5e89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f5f17e17e5f54014ea830b208ced2160254e9afd41c57533a22f20ba746d9c`

```dockerfile
```

-	Layers:
	-	`sha256:edf825008cc03344fb619906e7e7ec2b9fc14fd95212f82320a2b93e91e1ade1`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 3.6 MB (3618587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3e88bd64df43446d50200b8b468c4d96319ccedeaec436cca1e26bfa1c2a59`  
		Last Modified: Tue, 03 Feb 2026 03:44:05 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.in-toto+json
