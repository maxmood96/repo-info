## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:386cc1e729fbe38f3455e517dbacb36c6864fda94de3903195390b896dbe9984
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2cca36cad420802e2d283d7f1cd1782827758a3b0a896ea6b7be13c438a36148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124306711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b3ce5e621536e484b67fdf56890f715aa8ce691cb0b842d74fa8a5409180f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:41:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:28:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816526a6d4acf81b392ec5a1e6d8d402fbc4bf0460323c5ad45b376b247ca6fc`  
		Last Modified: Wed, 24 Jun 2026 01:41:36 GMT  
		Size: 15.8 MB (15790805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3cf50c221acb61e259a7ecd20caf425597eca7d93e329dde2640ca7ec8aaf4`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 54.7 MB (54742897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f56b1a717817f168f819b5cced017c47f4709e6e8f046475081b988cb5f6c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7928697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7fe267974bf7f368441143a819a904034deca30a2fe773c0e868d48f4d89cd`

```dockerfile
```

-	Layers:
	-	`sha256:8ce9dff56aee7debd6d1d9c2714123f60dc403271417143dbeee7747dc57733c`  
		Last Modified: Wed, 24 Jun 2026 02:28:34 GMT  
		Size: 7.9 MB (7921381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f0d8d510fff50ec85d9d0c0bc6fc0b276f1d603b3483fe55328fb454c053ff`  
		Last Modified: Wed, 24 Jun 2026 02:28:34 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:390410d18857a48e4c0ebde662c45b136bf2979f17d295654a208a6c27ad6a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114628601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee100ae8ba52223a63b3c2e4bb3ed296a9fbcef1ae0db79e4d431dfaed1cd3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fc5ae1e57bd12fc3393aea9c4c883b87d2ec58e18ce0892f8effba71fbfcd039`  
		Last Modified: Wed, 24 Jun 2026 00:28:02 GMT  
		Size: 49.1 MB (49064073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354f5593b138af5d5b60d8e82c822aa52fd74f6a603db24886e0573d60561397`  
		Last Modified: Wed, 24 Jun 2026 02:23:28 GMT  
		Size: 14.9 MB (14905363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf4cfcfd51cd63cbc0a86a0ed17f661e5157a3b24f24a750cdb7ac4191f84c2`  
		Last Modified: Wed, 24 Jun 2026 03:55:06 GMT  
		Size: 50.7 MB (50659165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dfc375661e95b30e9696ab2bb6466bfb0ae2b9fa6e377093042d43256d880b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7930163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571a0b4df2adac41a6019e1d5e561410ca13b900e8eaeeca94cd2687caa79f2e`

```dockerfile
```

-	Layers:
	-	`sha256:8761c0dfbc99b0a329d450c1d34051c0c4ebbc242f8b95f62a893e756c6040c1`  
		Last Modified: Wed, 24 Jun 2026 03:55:04 GMT  
		Size: 7.9 MB (7922783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1a3bb49fd029384a8d8c22b761f82fcaa45395f09a38bc0fcad17aae2c5e61`  
		Last Modified: Wed, 24 Jun 2026 03:55:04 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8a8c25029e34ff919f7b938ac5d88bc50e0dfec7695d51cd4072ffe55b374e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122911740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484a23b74abeb6740ad4ac7813b779e1afd1ed923b6482f9b994913775569148`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:35:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf305d6ad7bad47ee0696c3db8b8fed8e9c2a42c53b57d047f8ab32f5d9b546`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 15.8 MB (15774954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f37219bba62c0b4908476dc3cf7f0f98f1c87e8908c188797b1dc1f610c77`  
		Last Modified: Wed, 24 Jun 2026 02:35:29 GMT  
		Size: 54.9 MB (54879567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d620d3dc0aaa0d0004399cd0ce27e1080c26edd62d67c3278894441a3684d4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7934511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78211b45f5f50319fb6f325ce69be5438d12918546405f83eab4ee7282f4c10`

```dockerfile
```

-	Layers:
	-	`sha256:5151ee78d1a8888c43834ff720a7e6bb84a3212bd8eabd0c290282d745bce356`  
		Last Modified: Wed, 24 Jun 2026 02:35:28 GMT  
		Size: 7.9 MB (7927115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6d94699309c0c4ffd7cdd2e830728c685e2d49dd3a2c793b733829e6f0aac0`  
		Last Modified: Wed, 24 Jun 2026 02:35:27 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8c4675ff4efb60a089327eef6a64bc78bfdf74ee4271988b0e0b2f5311c1db53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127056069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0779cadcc161d7ef7fd76b0b78505e4ff73bd690240c335141a9768bc736d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:44:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7baf1917f31dc6264a068963cb19f53c4fc1fb3df24b85fb7b1a7235134b9d`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 16.3 MB (16295657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c66634bc3fa0a0bcd10bde2aef17a8a2d29d8cc303406e191342fab9599745`  
		Last Modified: Thu, 11 Jun 2026 02:24:53 GMT  
		Size: 56.0 MB (56047555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b778828141bd1dfb523e76327a9275ed19d1cba7809d7e9de5fbe5b1fc0b05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffc9b370bba35c2ce6debf15cde9ad548f9ca865d72a53a0b17614700d02685`

```dockerfile
```

-	Layers:
	-	`sha256:3b4539b2c1e7f2e80c197f3eaeceee7b28c777ea781c16b281e6434eb9d776a8`  
		Last Modified: Thu, 11 Jun 2026 02:24:51 GMT  
		Size: 7.9 MB (7916951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd2c8b134233229b7240d346742d67a2073abe81bcaed463a8703661b9dc98a`  
		Last Modified: Thu, 11 Jun 2026 02:24:52 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
