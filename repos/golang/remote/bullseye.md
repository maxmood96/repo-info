## `golang:bullseye`

```console
$ docker pull golang@sha256:12152217ef79f60fd71a64375d818b7be68c69c7611ca471c2e2c28324cbf4cd
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

### `golang:bullseye` - linux; amd64

```console
$ docker pull golang@sha256:c6f8317dee8f00e46411030655998a59d38bddc43d3a6223fcaba7f00b88c5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (294983779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b7b4a121732db8080f2fe028d1315a0a760cf3b5ae9b18e225df13f0cb8420`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bacc10016b88388ffcfc95d83dde951e3dcedae487c398eab0b93b6357c4f4`  
		Last Modified: Thu, 05 Jun 2025 19:27:57 GMT  
		Size: 91.7 MB (91729433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f67fead7e33763b5fa924cb2e4644bbf5332ed056eb32ba0bcd3bdb68eea3b`  
		Last Modified: Thu, 05 Jun 2025 19:27:55 GMT  
		Size: 79.0 MB (78981811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a236e58c425af64772545258ae8e119fa5ab230ed5da2e18151bb910c111c66`  
		Last Modified: Thu, 05 Jun 2025 19:27:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:7adcc3673b4d89232da60bd1518e6c24ce955aae130a08b385b9b0ad11dc3676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10340575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b155dcf154be1e9b6ab71b0120e3a9887b2108256c4b89026423835f3d826b5e`

```dockerfile
```

-	Layers:
	-	`sha256:bca4b35612a74830a524c988d9b54a06c49d91d49cb0b73f396c3bd17570dc07`  
		Last Modified: Thu, 05 Jun 2025 20:23:46 GMT  
		Size: 10.3 MB (10314107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eef40b8921fdbd1ae89ba2a42a3b488a902a08854b727b161901ef44aa32447`  
		Last Modified: Thu, 05 Jun 2025 20:23:47 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:09b38cdfe714b2ab968471dcf5d69bcb88a9d526760e08ddabb6ad10d8c44a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256640743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2160cebbff34e08319ad536ff1dcaa24c2f86895a29f8c66bf99b50b36eda3d8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Tue, 03 Jun 2025 14:32:58 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd4739ceb6e38b56a017a3579cc385de56e1cf7fc98c2c4b4dabd966a9c123d`  
		Last Modified: Tue, 03 Jun 2025 20:02:27 GMT  
		Size: 64.9 MB (64942454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca4d2f2221547bbb6d011d5b305d7607f58d76e99b3112e811b1627f40e830`  
		Last Modified: Thu, 05 Jun 2025 19:28:26 GMT  
		Size: 77.1 MB (77144302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf921c0fdf08bf437091e97743106903a1d620e63829a373fadc9a24227770`  
		Last Modified: Thu, 05 Jun 2025 19:28:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:be74cc0507f876206fa214289fc79a84b55a2940c9ae1d8ae4738446e9eb92dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10144636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dd20d07e8846ae7545727288c2b915042db9acac02428aa2a7c9ff490bcefe`

```dockerfile
```

-	Layers:
	-	`sha256:2e03b69939dbbf2b43368c4fbe100575e63eef10a6634165313103b92ded5f7a`  
		Last Modified: Thu, 05 Jun 2025 20:23:56 GMT  
		Size: 10.1 MB (10118066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8bc4012b47d0ee3a2d42575a891309aaa3165f5ce4b21241498036ed471dece`  
		Last Modified: Thu, 05 Jun 2025 20:23:57 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3c29ef6aa10cc4498aadb5e738e61cdd139b4a86e4316068065c91099b3b4820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284437742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d01a15f5c45afa11656659324d1aa01b0a3d189373110b354aadd3ce4c172d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4f13c9f2ba35edbb5cc356335d05db12609ba76252d1006e9168557548c91`  
		Last Modified: Tue, 03 Jun 2025 13:56:16 GMT  
		Size: 86.4 MB (86354667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244882bda0eb70b1153262e9054d1f8801651888a3a6fc5a828db420391040e`  
		Last Modified: Thu, 05 Jun 2025 19:28:02 GMT  
		Size: 75.2 MB (75231544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450dad13c64a85eebac34532d753166654ddadf2d23dad56754c431400911d23`  
		Last Modified: Thu, 05 Jun 2025 19:28:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f7958037b372034a28ccf69d9f6debd7f42a782d295640f309c2ddffdeb7a8c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10342015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32df71067f51928feff0646d27665457a43657c17e794e941fc01157c686b4e4`

```dockerfile
```

-	Layers:
	-	`sha256:6f482227c9706492f31683394c74d35bbeb217c2a55f70cbc19892706e870bb1`  
		Last Modified: Thu, 05 Jun 2025 20:24:05 GMT  
		Size: 10.3 MB (10315413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2920bb47fba56fdaca7ae3c119a10dcea1f2337b9628cc02de452ee85026893b`  
		Last Modified: Thu, 05 Jun 2025 20:24:05 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:86392dc04429517522609201a2ad5b43ef947f58ea3e2b0597e296dc49fde46b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296631182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f970d504f2c1406dae96ea75c2679209de7512af68d306c87ca1f513b42c3e5d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Tue, 03 Jun 2025 13:41:46 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Tue, 03 Jun 2025 14:32:57 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1698ef35ecd0acc6689a4ea9ed268b625490f41274a474b1505cfef6f36bb0e`  
		Last Modified: Thu, 05 Jun 2025 19:28:20 GMT  
		Size: 92.7 MB (92726397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae592fba0490bc253690fa17e5004b2923bab9e7f9c8d6e116245da17997d7d0`  
		Last Modified: Thu, 05 Jun 2025 19:28:06 GMT  
		Size: 76.9 MB (76900579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3fb319fac23d502a3909c352c934c898907fa929cd90d6744a7be843bc4e97`  
		Last Modified: Thu, 05 Jun 2025 19:27:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:c0abcf61cdff4024794f8c4045c69081c165ce1d4e638bc3e218900217550010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb576d317216b8b1bd706627051949542dc928179dceee52d5b7d6459437050a`

```dockerfile
```

-	Layers:
	-	`sha256:fe7a4df9ab7aa73c5a5a061bf24b8bc8eda92fbb3fd8012151638e17fb269c2f`  
		Last Modified: Thu, 05 Jun 2025 20:24:12 GMT  
		Size: 10.3 MB (10303414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:981fb060b7c5b9ddadd9c1b794375b233eb0a257a13a188e802f983f33c0c2d8`  
		Last Modified: Thu, 05 Jun 2025 20:24:13 GMT  
		Size: 26.4 KB (26431 bytes)  
		MIME: application/vnd.in-toto+json
