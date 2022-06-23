## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:0b5ce805d045fe181f2e07afe6be3cef67b0e5485660da6fa45a4b763e44f1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9a2c8551369d6262afc9a42248fb6cdc33db8b8121bcdd723e9051948bfd606e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110841585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f043cb9ce993d20a6d17ab94b49fe56670927ff2076224ce5529bb78579b405`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:10 GMT
ADD file:4c5e0bec5f780d9c6bfbafcb9e6ed641781dd7f7c2853a0c49d6613e9fef9516 in / 
# Thu, 23 Jun 2022 00:22:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:54:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:54:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 00:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8372a04f222be82bf67eb0010a59644b1e52f1246b3da9034edaa98f3d591cae`  
		Last Modified: Thu, 23 Jun 2022 00:29:36 GMT  
		Size: 45.4 MB (45430020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1728fee80d376293a9ef5fdcc0acd3f6398fc4159b12064ce4c1e66f67e7e9d`  
		Last Modified: Thu, 23 Jun 2022 01:02:01 GMT  
		Size: 11.3 MB (11302923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cf50aa0a4b80b39d1bf4be232d404da0b1ad38cdd3bb1a017b727947b5f4bb`  
		Last Modified: Thu, 23 Jun 2022 01:02:00 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f576518faec8cbe1e4fdcc36cb9870736c6a0889e0c7db2bde641503f37b6d19`  
		Last Modified: Thu, 23 Jun 2022 01:02:19 GMT  
		Size: 49.8 MB (49765716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bcad1964e50828935b59396610d2eb50e983f12f7fa34cfa17535493456683a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106628112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd7280a3ff5dcb43e282274c236b06b2f37acfe4ed33b8f3f1fe256c1a7d727`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:55:37 GMT
ADD file:4fd9afff1465319b24ccf87076562babe87771f9c1251684705a3896e673aa09 in / 
# Thu, 23 Jun 2022 00:55:38 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:51:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:51:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:52:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ad86940bdd4f85f3b8d536255a8263fa6320c5075402f2a29b22648c59285219`  
		Last Modified: Thu, 23 Jun 2022 01:12:52 GMT  
		Size: 44.1 MB (44124653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98084170c786abfbf207790797183dd497f90f7ec66b04e020227837ceefddb3`  
		Last Modified: Thu, 23 Jun 2022 02:10:52 GMT  
		Size: 10.4 MB (10352939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c4ad88320a89f67b72e3da9e24637fa520977b8bd0d2eb5babcdc92de5a7dd`  
		Last Modified: Thu, 23 Jun 2022 02:10:48 GMT  
		Size: 4.2 MB (4162038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10abeea056854fff008b44d8c721d02a6875ec7be5afaaf6c4eb7e5facce5cb`  
		Last Modified: Thu, 23 Jun 2022 02:11:40 GMT  
		Size: 48.0 MB (47988482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:00e5ae9f05da00f146342f365331857649a8a4677bd19f3758c6345c12b1ecb9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102158071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e1648d4145df7d4b501c23624c7e2355d2d7485198c1e648468e1720b03237`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:05:04 GMT
ADD file:4f45aa06c6a1c011e41ff7e4685f05d91970973768fc88ff3e825c5ac4fd6058 in / 
# Thu, 23 Jun 2022 01:05:05 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:58:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:59:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf35481e5c316d184dac1873898948d1e8108de590a2a940c32cda34173fe7c1`  
		Last Modified: Thu, 23 Jun 2022 01:22:04 GMT  
		Size: 42.2 MB (42150850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b740b174e94fb77095522004355bb6f430f0b25308acd5fc66d325f04f99c6`  
		Last Modified: Thu, 23 Jun 2022 02:21:27 GMT  
		Size: 10.0 MB (9957097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf98bd2fdfbc26a0f8c12d47c32e612d01389ff5e4aafc52aa04b72381a6c823`  
		Last Modified: Thu, 23 Jun 2022 02:21:24 GMT  
		Size: 3.9 MB (3921761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0525b8f82975354336694dce23771eb04576302410a29a334172526e5de07d`  
		Last Modified: Thu, 23 Jun 2022 02:22:12 GMT  
		Size: 46.1 MB (46128363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ef456eb6bd04a75d085a8cf0b564a5280442d4a657add4b494577f8160965f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105042592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b74dafc91243d8335fffa28944d782444b0e33ad6e479955565d1bc59bc01a3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:45 GMT
ADD file:3d8b1da94fcec5d068e3e6465fac70cce404c331bb52e30a5bf7cbd950baa5fe in / 
# Thu, 23 Jun 2022 00:42:45 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:16:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d8ccec8a513f896fedd1d9765f3f2abf98bc8264f61cecf17919c80c9aa7ddbc`  
		Last Modified: Thu, 23 Jun 2022 00:51:18 GMT  
		Size: 43.2 MB (43213121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b40625a6bb21cb2cd6b19ef7592951f90da9ea1d8abf359196bf48300c448b2`  
		Last Modified: Thu, 23 Jun 2022 01:25:28 GMT  
		Size: 10.2 MB (10218617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414226169d0f92fdcd77314cbd06ba7613675d62a3afd63aa88afbf0072c44c2`  
		Last Modified: Thu, 23 Jun 2022 01:25:27 GMT  
		Size: 3.9 MB (3874558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb01f37c2a0f6704c7bc0d24baac1a6d5694b5e2fec5ae71f1c257b337a9348`  
		Last Modified: Thu, 23 Jun 2022 01:25:46 GMT  
		Size: 47.7 MB (47736296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ddee1e41ffe9c09651f062d7b5041e0c98067f7b695ccff7d66c5a59642b773c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113120086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5def5d542740d19211d645723d3a9ba775f9bd9c5c07cbcb8df2a5bfe249839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:44 GMT
ADD file:ec3ab24d5698ffb1c2c01f4cf088854df8d14de655c3ea1235b3ca4c06864be4 in / 
# Thu, 23 Jun 2022 00:41:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:17:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:17:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:198ad075a14b0fdef3454be69cd94a50c01a286b210867ddfc0a62404bdf34b1`  
		Last Modified: Thu, 23 Jun 2022 00:50:47 GMT  
		Size: 46.2 MB (46150601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbaffa0015e0586960116ca5558554b0c37500c89d72de88c1f9d16c4b75f1c3`  
		Last Modified: Thu, 23 Jun 2022 01:25:54 GMT  
		Size: 11.4 MB (11358747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15767d66256ddb61c1d4865abc90dee1afeff18268172fc8e8f0acdc445164ac`  
		Last Modified: Thu, 23 Jun 2022 01:25:53 GMT  
		Size: 4.3 MB (4342258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c04ca75d8a85c2adee31eea858219314e193127787b58a020d53652a7e1487`  
		Last Modified: Thu, 23 Jun 2022 01:26:13 GMT  
		Size: 51.3 MB (51268480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
