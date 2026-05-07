## `golang:tip`

```console
$ docker pull golang@sha256:abb38cd7cbf566b0b6cb166c0ad5ea35d379d1498c8ca00d8cf1bd437eb758c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:1b8308c433b9367d1f1fa2cdec42ff2a4a87f5e99887e2fe7c096e6c2f2412ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342476038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fa78aa3c2b441c48c82bb2db442459b93a1ffec305550c08698e9a89cdef5f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:43:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:45:17 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:45:17 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:45:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:45:17 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:45:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:45:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a342715aa7e3a349aea677a347d09f417d2053f1d7604388b7aed4fe7bb95ad6`  
		Last Modified: Thu, 07 May 2026 17:45:46 GMT  
		Size: 102.2 MB (102222438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32be2e0f5add9aa550a86f2638e1a5bddb598fef09f796f2626b736ae1c11c9`  
		Last Modified: Tue, 05 May 2026 23:04:31 GMT  
		Size: 97.5 MB (97538809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992bdca92ea0897269e38566ed5eada1d25d998a3cc572942f552d926a4228e`  
		Last Modified: Thu, 07 May 2026 17:45:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:acc10c5b6a099d6183924c5ef44909fa1e0ce9487bd852d95935864139f7cb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030fc87d0164ac1ebaabefdfb6de6a3579966eb5be1d5b611487300df70313a7`

```dockerfile
```

-	Layers:
	-	`sha256:4a987f59d994210024be66fb14ef5f57c316a3a087e5ba55df0c3ed87b4e924f`  
		Last Modified: Thu, 07 May 2026 17:45:43 GMT  
		Size: 10.8 MB (10785713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8f674c59187ca0916d24cb505ceab5cf3213f7ba630e9a01b828013f015710d`  
		Last Modified: Thu, 07 May 2026 17:45:42 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:dee11cf71a66d80d3ea25b6218c2914b605b34be461b4ecb220aa078b2b17733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298341263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729d759dfe9a92abfe8d3c0d638b051b13542c188eec2c5a6d2a0715a30e0af8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 18:12:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 18:15:54 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:15:54 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:15:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:15:54 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:15:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:15:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f411318175ae51ff20f60969311f63c366288f8aad04eda4d0389d8b016c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 23.6 MB (23636616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341da7892f7aceb1342cb554bdaf16f78292d5247e1ef9fb0f351c24aadb1f0b`  
		Last Modified: Wed, 22 Apr 2026 03:52:40 GMT  
		Size: 62.7 MB (62721455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804fbb3ca23bb80a88fc647ac2eb6fcab188ec923ad4e182cc08360c51de91eb`  
		Last Modified: Thu, 07 May 2026 18:16:22 GMT  
		Size: 72.9 MB (72865811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124712ceb426f7d5ea56fbdf12ab02ae56c25941c6892b6e8ce38b9f03ee67d`  
		Last Modified: Tue, 05 May 2026 23:09:06 GMT  
		Size: 93.4 MB (93379030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8d6e9c6f727483b9d8135ec83f13a61d8ebc6f0d3c98b5ab45be43c29a2d2`  
		Last Modified: Thu, 07 May 2026 18:16:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:41e690866cfde510c5cf1f882d72be112eb1ec27e1d6cb3af0cd7bd999b7f2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b02a58193bf4405f490893bb386052336d21d0128931ebbe30afbf06f5c3e8e`

```dockerfile
```

-	Layers:
	-	`sha256:2ada065f79a7758a255a96b5ab1ea2d523e9d34f9dece66936524d82a1d3e10f`  
		Last Modified: Thu, 07 May 2026 18:16:20 GMT  
		Size: 10.6 MB (10581600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00ad9b047b9b4e32faded55eceb888ff6f4a515b2e84671ae0fae3a4307368ca`  
		Last Modified: Thu, 07 May 2026 18:16:19 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:923918a79e2c98476ff1b958cec7b93a806edae7ccbd025ba9594d5e5f0c3ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332886890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71f15db3bd94bbd5052bbe6523911c1805e71da02ee587ab737861d90707029`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:48:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:50:23 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:50:23 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:50:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:50:23 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:50:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:50:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3027ce799e6fea972d34070bb507afe9f917a0d8931f3f291cc51482f9d7dc`  
		Last Modified: Thu, 07 May 2026 17:50:52 GMT  
		Size: 98.4 MB (98366980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310d7048cbd083a777980fa032397ddcbb87e03b5b4b31ddec2b7fa305c5ce5`  
		Last Modified: Tue, 05 May 2026 23:04:45 GMT  
		Size: 92.2 MB (92242363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee4ecabe415a60231d23556aee82f73880cf19d59811b433dbb78429ac03a52`  
		Last Modified: Thu, 07 May 2026 17:50:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:907cf9fba571c44309bc8babdb58b131cdb51c7a6d8296a9c0959be2b2462d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf07ead5ebc052e4d9dbf19754355de358cc4c7dc9f2ca5d977a44449479776e`

```dockerfile
```

-	Layers:
	-	`sha256:94aeece95cd61e018f0c90bcad218acd3dba2acb7198e61374cbf079da45e909`  
		Last Modified: Thu, 07 May 2026 17:50:50 GMT  
		Size: 10.9 MB (10906168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457bdd0c79c22b8351fca5f7f6c9219e995b0d17555feb735891917f928a61bb`  
		Last Modified: Thu, 07 May 2026 17:50:50 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:db9d6e104b8d9e6508ed1531811daf5965c41d347975a3e10e3fc229697cb9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343364854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fea33e77cc9272b4c782964c12e2e5d0768d978069da12ea8e1f5dbeeb7fb26`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:44:18 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:44:18 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:44:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:44:18 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:44:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:44:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5321bfd0f3573fe94aa2216d1519cf604989d7a9e912196633f5d9b7a4e8097c`  
		Last Modified: Wed, 22 Apr 2026 01:43:12 GMT  
		Size: 26.8 MB (26784835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66cdc00799a2a5d425863c783516cdc5139f867d081df458a78cfa749e9d7c3`  
		Last Modified: Wed, 22 Apr 2026 05:03:55 GMT  
		Size: 69.8 MB (69809793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23da63c9b623cf1e53b55a9ec8360a0ccb64a313a3537a93850f861bb10f36bb`  
		Last Modified: Thu, 07 May 2026 17:44:48 GMT  
		Size: 100.7 MB (100664883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b12f480be5869cc9862686abcdcfb3464484b704815a3a70c6077d05037bb`  
		Last Modified: Tue, 05 May 2026 23:01:30 GMT  
		Size: 95.3 MB (95279830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aba472b97870b51ecee9c3d0b7075b214398ea9db6bf6fc6c45cf3c1d74cdfb`  
		Last Modified: Thu, 07 May 2026 17:44:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f9784b771cf9c77017ddf176e358a7e52a06c1d05d8993c0ebcc0402b93a12f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d32dbc3d2c25447a5256a9c19dc62d18504716d0eb9e48447ac878f55608cf`

```dockerfile
```

-	Layers:
	-	`sha256:fa99fb161f9644442ba6ecc7e4b1c7fa69437e40345a7c2224e619e2c6762d25`  
		Last Modified: Thu, 07 May 2026 17:44:46 GMT  
		Size: 10.8 MB (10756976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfda900b5210f525febcc5d126c4ccc8e0c93091a1a4bcdfb4bbf16e32b060e`  
		Last Modified: Thu, 07 May 2026 17:44:45 GMT  
		Size: 28.9 KB (28924 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:20412a007790159dc1c1fb7eb7967b00cc1c1b4f8834c8ee782d9f4944717898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340234309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8956906fb79fba8a0088bf6316066b95aa24c2038432b0fd860793b0ac65e6c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 05 May 2026 23:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:40:06 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:40:06 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:40:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:40:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454d511c21492888baf49902a298f334e8095ce0fe93b53b274ab3f39febd31`  
		Last Modified: Wed, 22 Apr 2026 03:40:51 GMT  
		Size: 27.0 MB (27014616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9e1a80821bce13187cd275a074ab44791a07c4796e61afbcda3a692b97ac4`  
		Last Modified: Wed, 22 Apr 2026 09:39:58 GMT  
		Size: 73.0 MB (73039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32542f6ae8fa91e3c4f7aa2ae71b01665f1f0f2721fad64b8c6c798ae91cefd5`  
		Last Modified: Tue, 05 May 2026 23:41:42 GMT  
		Size: 92.9 MB (92928186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df66d548befa9f03e6fb22cc6385677d9c13ab71d11ae10a9cbc0d2e3d0efc16`  
		Last Modified: Tue, 05 May 2026 23:41:42 GMT  
		Size: 94.1 MB (94128677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ffe1ddcbfaa8c6da8237e96a5f8cbc5bb2fe068d9e535108c816dcf5a040e`  
		Last Modified: Tue, 05 May 2026 23:41:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:96bd501de05e6db326fc0381c4973e095921540f65238bf67dc66b39e89373d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbefa6d36e90c5a7b10b93f281c723a5a3fd3648ec761f6369dd7dbaff600881`

```dockerfile
```

-	Layers:
	-	`sha256:cc77ca15d570c330bb6ab0c53d69b2c83f7fbfada3be8e43265bba9c8051a26f`  
		Last Modified: Tue, 05 May 2026 23:41:38 GMT  
		Size: 10.8 MB (10781501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c53001cad588d92ff3c7b69f4b77dd35c602ed58dd407d4b4a033e50f28944de`  
		Last Modified: Tue, 05 May 2026 23:41:37 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:b101b3530a834f6f2637934631929654e436fc35c9dda8381ce82629581e3343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365673574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97a02948ed67849ed219091967d854bf2ed613ab8c6e1c2acba313f89ca49b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 19:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 20:31:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 06:45:06 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 May 2026 06:45:06 GMT
ENV GOPATH=/go
# Wed, 06 May 2026 06:45:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 06:45:06 GMT
COPY /target/ / # buildkit
# Wed, 06 May 2026 06:45:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 May 2026 06:45:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad20ed76b58e7abcec15ac3129845a802887c092560883b4939e006992099b`  
		Last Modified: Sun, 26 Apr 2026 15:22:58 GMT  
		Size: 25.0 MB (24955805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233e35e9c32890f2d416d3e6707a14b173707fad25985773c22f4606dee5c05`  
		Last Modified: Sun, 26 Apr 2026 19:10:01 GMT  
		Size: 66.6 MB (66648074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954c4b6ce8f364903d1d8a7ac953d1cbfe6ecf95f3d8c267e0b27a58b6e61bc`  
		Last Modified: Sun, 26 Apr 2026 20:39:36 GMT  
		Size: 131.6 MB (131649887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d77dd072bbe9d4ad01204d701c796e83867bd2e370f7f50879f12652b55ef`  
		Last Modified: Wed, 06 May 2026 06:52:06 GMT  
		Size: 94.6 MB (94621433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9b99fb2cf5b5e5ae00b5a307aede37e49ad6185be029faa9a7d2d16cbe5087`  
		Last Modified: Wed, 06 May 2026 06:51:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:1bf3c5cd79effde86c569d59a4efa2efaf655c0e8fc50a49c512abda4bb94a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c76be1fc8380fc35898c9aee1718f73783c88470c254c67dcd5d3aa1bb1a2c`

```dockerfile
```

-	Layers:
	-	`sha256:84108ed3b601c6d36e56b947c104b072e29bbcffee990f2657bc0188c4b980de`  
		Last Modified: Wed, 06 May 2026 06:51:53 GMT  
		Size: 10.9 MB (10855334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c42688186c1da119f2be2e426528f8f693876aea10fa6700f25559591e02c4`  
		Last Modified: Wed, 06 May 2026 06:51:50 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:e8049597941504c1cd06ffb521b72fea76fc5a98255429b957cfe4ea0b53a5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (316950863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf7d1e7e80faaa8a451709d31c047d9019bfd6feaa57e79c9c2b8ec59799ea1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 05 May 2026 23:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:58:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:58:46 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:58:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:58:46 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:58:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:58:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a3da428dd91e4b5df556514e279e6a571eec116b1f2b3ed1bc95489fcee4`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 26.8 MB (26802425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81397603fbb04688ca83ea8697469c3a01388a59e003d38dd37d22beb13789`  
		Last Modified: Wed, 22 Apr 2026 04:21:39 GMT  
		Size: 68.6 MB (68636900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc6a2d536e288af87ccee171508f7485452c85c478a1a2916967410856a3ebb`  
		Last Modified: Wed, 06 May 2026 00:00:33 GMT  
		Size: 76.0 MB (76033684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2604867f1d33ea36e2647b9da201fb796e01f541d58d01f7899b6b2cfc20d4`  
		Last Modified: Wed, 06 May 2026 00:00:26 GMT  
		Size: 96.1 MB (96105590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1947e08859b0c3f97c35038351830813035cc3c013360a7fb7297c7bfc0beb8f`  
		Last Modified: Wed, 06 May 2026 00:00:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:ddb37034dbf21c1010ff73a880096111081a7d079900026be507dc1012c5b95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f42d34884be43eb3c19dac3f0f6f4c7654d730a60f7aec70d86595b9a4ff2e1`

```dockerfile
```

-	Layers:
	-	`sha256:d24440f7425ba276a10259afb3a1d8e7c5eb2f0b77b5c63d88ee1ca382415862`  
		Last Modified: Wed, 06 May 2026 00:00:30 GMT  
		Size: 10.6 MB (10596861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fa92673422ef544cc11c19bb95fa0d48223b8852b6c2567c66ca1a57889c5b`  
		Last Modified: Wed, 06 May 2026 00:00:29 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
