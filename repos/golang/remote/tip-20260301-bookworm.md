## `golang:tip-20260301-bookworm`

```console
$ docker pull golang@sha256:e75b88ba9929e57ff90305d484aff9a1ff1cf9a90756fe82fae5dd4e1bcbdd53
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260301-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:947f7c0c376b7640dc9899169cb20faa96722d8076e2b4df5efd442c98e44a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.0 MB (322971315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636d4358b315bb06646c7bc67400e8bed87a16c5f05f8c0691e27fd09300220c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:03:35 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:03:35 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:03:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:03:35 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:03:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:03:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a806d1e12c09424b872487f9ccee174eb0afa65e10980478abfe468ac328e1a`  
		Last Modified: Mon, 02 Mar 2026 22:04:04 GMT  
		Size: 92.4 MB (92444733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689a8c664b692c42c224e696026ec9ec2afa2556b09a298fb5881d3823f0c6dd`  
		Last Modified: Mon, 02 Mar 2026 22:02:43 GMT  
		Size: 93.6 MB (93603346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81ff1dacc317de92fa7bba814a48b6c7d17f4afe9bc1b5f5c3a85090102c338`  
		Last Modified: Mon, 02 Mar 2026 22:04:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0d1725d24eb9c63949482e5f0205d03abfcf4d9b2262b4dbeb4182a7003aa756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c9a76e91a78bef58baaa7cdb39ddd09d8f7eaecd15280f64a9e387075b07ea`

```dockerfile
```

-	Layers:
	-	`sha256:5c409d3443c1da62a3635c3ff2f290fd3e0ee18fb119ad2c6b9965146b985633`  
		Last Modified: Mon, 02 Mar 2026 22:04:02 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c040941822eed6b40be18f153ae05dbc44a7586068e5a9e8ad4e688683e3a4a3`  
		Last Modified: Mon, 02 Mar 2026 22:04:01 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:7fd52cff9f9a1842203f3a97607d580c5f290317c1f0f73fde154f407025ff2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281809121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6990979dc685eeea95784358794b2083e73894446c79b91b5fcbb0873f7b374a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:05:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:04:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:04:14 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:04:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:04:14 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:08:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:08:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742857c89c3fff9f983a1595594994ae63f49f2e0dd92faaa9d5886d69aedc6`  
		Last Modified: Tue, 24 Feb 2026 21:34:25 GMT  
		Size: 59.7 MB (59651871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8136eb60a27b074b4d0e8e332921995dcebaf7d33d81d7f406498f91da42e240`  
		Last Modified: Mon, 02 Mar 2026 22:09:09 GMT  
		Size: 66.3 MB (66310527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d47f42e49b5b1824f0c700b4d521593aedaa7278226bf8d2c8c937a0110183`  
		Last Modified: Mon, 02 Mar 2026 22:04:34 GMT  
		Size: 89.7 MB (89696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18094b4a9e9d5d5fbbb08d3554762e0b4b25ebe6e70899ecd1b1dc831d6c031`  
		Last Modified: Mon, 02 Mar 2026 22:09:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:83fc3e273d13bb54129df51bc853fbe580999f9db2b2ed5cb6caf15d5fcafe81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdc8f5b4c07d1ef76f2e1c926003eb35252e04a94e52b53fef4d2e21e805787`

```dockerfile
```

-	Layers:
	-	`sha256:13073c0466fe15ee26a1a1aedbb85957057793ae41762bf03aab96ea9410b75e`  
		Last Modified: Mon, 02 Mar 2026 22:09:07 GMT  
		Size: 10.3 MB (10303727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5e2c39db617e7eb5fbd9d83bd744c265068efd52dc948a0cb4d4a145ffe90e5`  
		Last Modified: Mon, 02 Mar 2026 22:09:07 GMT  
		Size: 28.5 KB (28497 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f8efb86c74da354a983e96ceb09632cfd08e10cebda68494fe2d808d350eb5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 MB (311767583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bbeb9f24d2edc4214209788b32c9e28f9c0af2174c95e80efe98337f6020ffa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:03:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:02:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:02:37 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:02:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:02:37 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:05:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:05:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d64f5ce50c971aa912f0a71c5620d5d62643e7420090b345153a56b171d6c1`  
		Last Modified: Mon, 02 Mar 2026 22:05:51 GMT  
		Size: 86.5 MB (86525243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e982fdcb72c3ad1cca7a139b473ea3951042395bd4cf7fbdb4f775c24a9b551`  
		Last Modified: Mon, 02 Mar 2026 22:03:07 GMT  
		Size: 88.8 MB (88784830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79106678797899c1b25a563fd6eb316bd26b5239d28744aa2e8a78a896cb9305`  
		Last Modified: Mon, 02 Mar 2026 22:05:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:743e35733fdb80882d79808bdd0e579235ff08103930e7eaed1ad36301419550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114f9887cf9e27fb0f506aeb427156f7c63aa64a7743b2b30ea36c3d188cdd31`

```dockerfile
```

-	Layers:
	-	`sha256:6e162ce771b18a369c744a11bdc7dbed3e893de8df355fb6239ece00a4dc6024`  
		Last Modified: Mon, 02 Mar 2026 22:05:48 GMT  
		Size: 10.5 MB (10524855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f785edbc6ebbc154b76e5b1f43572af51d7ec190db1f85f37397405af700fe85`  
		Last Modified: Mon, 02 Mar 2026 22:05:48 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; 386

```console
$ docker pull golang@sha256:dfc49c9dd4f76f3361f03daf53bac6bf0d117c2f7681bbccf8874ac42887538c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321904914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c30bd70e25f8863682a98d8898ab8396f62b07a8537d8d5d01a35a1a18e7730`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:05:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:05:00 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:05:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:05:00 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:05:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:05:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31e1fab6283d72f6ce2de137bc123a8ab89a85f0baa0b6c11c2c6d28c359a32`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 24.9 MB (24872106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383bd8d2ca9c40d67394c0121b8fdb7d7c8f44082342e21f4188fc611c88e9a6`  
		Last Modified: Tue, 24 Feb 2026 19:56:53 GMT  
		Size: 66.2 MB (66234334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca01e88a8611bc923dfa30ad9b55a23c05ced287b052f1bca5f88378b9e469bc`  
		Last Modified: Mon, 02 Mar 2026 22:05:28 GMT  
		Size: 89.9 MB (89871541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b2140e9f06d205b6b5af3fcc14f26b13013365f22129c2ff99cb48ee34776`  
		Last Modified: Mon, 02 Mar 2026 22:04:44 GMT  
		Size: 91.4 MB (91448922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1133d13c1a5d4313cb05644e3cc7d18e490db31954e630f1c7cea27c3d6b000`  
		Last Modified: Mon, 02 Mar 2026 22:05:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7e233fb02c48c0a33bbb677452dcbbf623993b38d870e91af24fa7247b1696ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681d15d424e91bfdea0c9a4d4c365ced40ab30b02771bf0343c18e317c787b6e`

```dockerfile
```

-	Layers:
	-	`sha256:cba799d8e1f7f1456ebc8eda5d74c99c078adccc427dbd7e094132f42b89fee0`  
		Last Modified: Mon, 02 Mar 2026 22:05:26 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64a785b1499a385d73e3fee6db998a1936789ea61ad64120a2de909287e1d23`  
		Last Modified: Mon, 02 Mar 2026 22:05:25 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:1173f126b75c1c2e4ea6910b00f1d8f0a5b26d1bcea20c4679743eb3328edc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 MB (293186744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd498cf681911a3264280edbb501f79625a8b4d6da178b607112b793ffe2933`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 06:07:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 11:29:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 12:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:22:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:22:37 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:22:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:22:37 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:22:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:22:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6ec71ee94fb878725e70f6a21c20349985b89066361ee1f753b3854cfa2c839a`  
		Last Modified: Tue, 24 Feb 2026 18:41:37 GMT  
		Size: 48.8 MB (48782510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2283ea3597dab73b85bc0ebe9635f3297b9d6d4b8ff5df7913003859ba369`  
		Last Modified: Wed, 25 Feb 2026 06:07:50 GMT  
		Size: 23.6 MB (23615315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372ec86799dac23af2f0ffbced98ecf9eceeaa5ddf68be3af3cc474182e97448`  
		Last Modified: Wed, 25 Feb 2026 11:30:27 GMT  
		Size: 63.3 MB (63310148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8358d10d80c9af8f69fd6083cd0982ee261a68e3865c0f029247660744e146`  
		Last Modified: Wed, 25 Feb 2026 12:20:12 GMT  
		Size: 70.1 MB (70053345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c873d734029e0e4905a401dcf9758b8348160aa0ab7bf1cf0b2f08dfa5025af`  
		Last Modified: Mon, 02 Mar 2026 22:24:43 GMT  
		Size: 87.4 MB (87425268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef0c4dc6bb229ed06c1ac41115700e4ffeba503c4bb5973f9e72ae2fed9dc18`  
		Last Modified: Mon, 02 Mar 2026 22:24:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:32c6b22cc7f95d3e5cfd25da9ea21568cb45240605f1826b069e48aad064a7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1294058d280a4e67a13aa62358279b6db4286b8f0a8a15bd10d4c22b2851c86f`

```dockerfile
```

-	Layers:
	-	`sha256:91dc41cacbe514014232faa4e348f13b9234ef02cf05a6435a8fd6d207626f5a`  
		Last Modified: Mon, 02 Mar 2026 22:24:34 GMT  
		Size: 27.1 KB (27123 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:876df28f1a3d0672d34b325ce8fe67fce41a4fe19020c22beec2d768e64ffc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328621350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21043436c597315d0243f8f917dcb7178765f1751693eb928400011ccf878e66`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 02:56:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:04:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:04:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:04:07 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:04:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:04:07 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:04:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:04:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba53e63c4e3e4d88f0425bc79a37e364db9aabbff9c13ece5cecc63ec880f3`  
		Last Modified: Tue, 24 Feb 2026 21:19:17 GMT  
		Size: 25.7 MB (25671399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eaeecfe60befcd3d5daac43038587e48eaaea46a2b5f8466018b05c5579686`  
		Last Modified: Wed, 25 Feb 2026 02:57:13 GMT  
		Size: 69.8 MB (69846164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc75d834a9e82c03e8959ffd55a7fa0f7b3371dacd78d66433cc7c9509fe11b`  
		Last Modified: Mon, 02 Mar 2026 22:05:31 GMT  
		Size: 90.5 MB (90450944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcc3a57b0d1a4c549275152be846eeab1e4bfda9d363982944775991fe15219`  
		Last Modified: Mon, 02 Mar 2026 22:05:31 GMT  
		Size: 90.3 MB (90315888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958c30677d2b78d127af5c7af92ac08ed37ea666343f082d95375939f8c06b4`  
		Last Modified: Mon, 02 Mar 2026 22:05:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e516d673f9daa00517af17151eb6ce129816e0152afdc752ef4c8bcb1043cd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcca961b255752730a2d347dc8b8fee9685b5b38b7240bc0bee11ca37c64b77c`

```dockerfile
```

-	Layers:
	-	`sha256:610899f941c3da0aee0ab1cdc9d0a4afd81bf541b77d12ee18901ba22c88cc4e`  
		Last Modified: Mon, 02 Mar 2026 22:05:28 GMT  
		Size: 10.5 MB (10469516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5a9eecaccc86f941ba9699f44d74697b41cdb0be99e98438db1181c2f7bb03`  
		Last Modified: Mon, 02 Mar 2026 22:05:27 GMT  
		Size: 28.4 KB (28431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:56b05645b47ec93d8ca1a4007d1f2f34f4989b6a9fe35a738f78b0fee827cf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296531764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7983cf079f386d83a51be0d578f35dbb13a02bbb3bec80967e1ca90e55e713f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:56:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:04:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 22:04:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Mar 2026 22:04:23 GMT
ENV GOPATH=/go
# Mon, 02 Mar 2026 22:04:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:04:23 GMT
COPY /target/ / # buildkit
# Mon, 02 Mar 2026 22:04:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Mar 2026 22:04:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1490eda04f0dc8144e02f684cac28c2862b3a584dd3e8ad7e22b96b35409c89`  
		Last Modified: Tue, 24 Feb 2026 20:56:37 GMT  
		Size: 24.0 MB (24033874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d60976a172fdc4da11bc00a6a1bd9ac1b17420cd914b41c43278a69a7a6013d`  
		Last Modified: Tue, 24 Feb 2026 23:52:41 GMT  
		Size: 63.5 MB (63501714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2890519aea106f7499a75a4e076e7114cf62c5836635308905d485a6c533c66`  
		Last Modified: Mon, 02 Mar 2026 22:05:10 GMT  
		Size: 69.0 MB (69045371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d3098d11b942b930d9b88ef8d2b13e42c10d7ccd12c5e317467f410cfa58`  
		Last Modified: Mon, 02 Mar 2026 22:04:29 GMT  
		Size: 92.8 MB (92802560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e324660e6851b931ef2fa7a4e7c1c113047d20e910de918bbe956a0e05776f`  
		Last Modified: Mon, 02 Mar 2026 22:05:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:82ce9980694a6fd0fa55abc8826de9a2451e1a04b47a39e0ae436bda68bb1b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d89ee03c6ee8212a1c500343bf4a12b949530e2496e628f69417381610969e`

```dockerfile
```

-	Layers:
	-	`sha256:2408644d8b0d4f9763831297aee9e8f612aadf0b026b2e64d269191c9f0d1083`  
		Last Modified: Mon, 02 Mar 2026 22:05:09 GMT  
		Size: 10.3 MB (10328789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba3d985dd0b4bc4b0d28ae5e6fae2d534934f6c78cff063e2eab53f4db25a100`  
		Last Modified: Mon, 02 Mar 2026 22:05:09 GMT  
		Size: 28.4 KB (28384 bytes)  
		MIME: application/vnd.in-toto+json
