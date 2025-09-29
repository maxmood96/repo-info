## `golang:tip-trixie`

```console
$ docker pull golang@sha256:332b0ff61201733b6d4f822f76e41a98cf0f0c94d6c76a07fb827e915b66be68
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

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:589208d60b1896635aebe666d8c50677f6d112b3f87c571ba2461de6479b3a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328620052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7dc5a61817a1352b0ab9c3870ed16d73b557a71b8764c37ac3ab6f7decd53f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22718812f617084a0c5e539e02723b75bf79ea2a589430f820efcbb07f45b91b`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 25.6 MB (25613635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a98f7495bee3e8e6943da9f52f0ab1043c43eb1d107a3817fc2a4b916be97`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 67.8 MB (67776756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8309fe7423492816421bd7fa249625a75849c95e5c57380756c62420fab61715`  
		Last Modified: Mon, 29 Sep 2025 17:59:26 GMT  
		Size: 102.1 MB (102088442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd392ccd6779e7a888cee1ecce65db01995a1886c75ae75a375deb44486fd071`  
		Last Modified: Mon, 29 Sep 2025 20:26:43 GMT  
		Size: 83.9 MB (83861530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddcf5141a0aacca4384c7ef5105fa5023f29d572c8d8ab69b8db1628b8af23b`  
		Last Modified: Mon, 29 Sep 2025 17:59:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b459aa91f1ae0fae240db4c59b09ca6f8c846c2b7439070bd9fc7f6f56435c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10811945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee6af86291af398812759df5c5fd9769b14643451bfb7148a6cbf095655547b`

```dockerfile
```

-	Layers:
	-	`sha256:d0a256d32191d4efa8720f519340dd0272348374b15cd6653ff6f40fa79a47cd`  
		Last Modified: Mon, 29 Sep 2025 20:23:31 GMT  
		Size: 10.8 MB (10782934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c78a8cf113a85557581ad4d62ab0b88348d106e7abf1f7f2fac65ca105d6da`  
		Last Modified: Mon, 29 Sep 2025 20:23:32 GMT  
		Size: 29.0 KB (29011 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:c1f026c2c464928bd08287217dffed6d7a4606f53bb7d82ac91d5e11908b6ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285673071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cb5a7ba0790102e27d148adeadd09045a4fb9b752b8431e47dabf003918910`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:395f9ad3c9d37c6ea60897f33e8b189e9cd41fba6c60ab63882fd95de8ebb9f2`  
		Last Modified: Mon, 08 Sep 2025 21:15:43 GMT  
		Size: 45.7 MB (45711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87266d99f84095bec303de1733ad218d485653dfb6da729b7a066c18810645f9`  
		Last Modified: Tue, 09 Sep 2025 00:02:54 GMT  
		Size: 23.6 MB (23614030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0847685b749ce0208c0ad2a407e89f30279b1c8515c5c33f13a9c9b4c5e3da02`  
		Last Modified: Tue, 09 Sep 2025 06:20:22 GMT  
		Size: 62.7 MB (62719599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c6e34baf9854c6853ac2dde4db477e6602af6c755e813036bc7e693ef5628c`  
		Last Modified: Mon, 29 Sep 2025 18:04:45 GMT  
		Size: 72.7 MB (72733729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eea36933200b5f141ab18c26e141eacf675fe2778fc8f3cca0727236a934dcf`  
		Last Modified: Mon, 29 Sep 2025 18:04:27 GMT  
		Size: 80.9 MB (80893837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e3534c65552e07990c7403bab56a0994ebfe6fc0e5bcecc9e35d004c7abc73`  
		Last Modified: Mon, 29 Sep 2025 18:04:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c80f7dd8ca14c49359eeb2f8831fd55e60c5f9e90fd01348398adcb8fd4e240c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10607958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522c6f48267eeeed20238474d9490ef67cbf86e8d395797f2c06cc8e5f7360bf`

```dockerfile
```

-	Layers:
	-	`sha256:d09412d2d3a1abf815ed4376cf9845e719043dfbdc9e838334b196bdd74f5483`  
		Last Modified: Mon, 29 Sep 2025 20:23:47 GMT  
		Size: 10.6 MB (10578823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d551033bf36384ebbfc545cd577b0bd4540c8b8028f0470e4edb8c593ac323f3`  
		Last Modified: Mon, 29 Sep 2025 20:23:49 GMT  
		Size: 29.1 KB (29135 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:dd0c39217e05571de6f65e33e6531719d372cfb1ac6daff312656c4314e0c688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.3 MB (320291746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64db436f5a098e472266a3fed2a47ea74fea62fe866e4aff58814f1c013822f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd36c08acb8bfd3ecaef97bc215303e9b1c59f47cb418c4692d97f29cb1b17c`  
		Last Modified: Mon, 08 Sep 2025 22:26:04 GMT  
		Size: 25.0 MB (25015321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fd600967e6c49c98883d12d3ca7ba50395f75eb436373e95780141122745a6`  
		Last Modified: Tue, 09 Sep 2025 02:13:16 GMT  
		Size: 67.6 MB (67583121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f99979fb84acb6e99a30cd8377d4291ae9cbf1367c9ce7942778164ee382b6`  
		Last Modified: Mon, 29 Sep 2025 21:12:05 GMT  
		Size: 98.2 MB (98234629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94a779ece8baaa3a2b9ccff68843c683bfb8ad46a4cbd1f1c29fcc7f5e6802e`  
		Last Modified: Mon, 29 Sep 2025 18:02:35 GMT  
		Size: 79.8 MB (79814772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45617ef6eeaff0bde92bc2d5bddf6fd9c84a4bf8e9bb532aadda0d6ea0612850`  
		Last Modified: Mon, 29 Sep 2025 18:02:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4193e004341d469e21fb9f1e8e434f0990dbf1cdbcbc40bdc2f635469831ce9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10932556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5d33dbe2ce14c196a8e989196bc23de436e2f8cefa8d92603b625d68ac0368`

```dockerfile
```

-	Layers:
	-	`sha256:89aa1d5f7c800f30d4c6662a366c8405ddbaf7711396b7e91b1404b42305a6c0`  
		Last Modified: Mon, 29 Sep 2025 20:23:57 GMT  
		Size: 10.9 MB (10903389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85485219f502530700a221f857be6b271d18c3bd48693cc887b853a3d6efa42`  
		Last Modified: Mon, 29 Sep 2025 20:23:58 GMT  
		Size: 29.2 KB (29167 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:48ae4123432cc4ab4b5773c03c291529a248d4cbd3c0217462cdb7df4772b22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330426765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3201e21f1e27c7c84d7606ffba6932e205e7b248d09ba5b8bc5d0e3f89588cc8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95e6ff4859ead75e29b179b0636a999dd68cde264f9c74ad8882d9d5dcfc9c7`  
		Last Modified: Mon, 08 Sep 2025 21:55:26 GMT  
		Size: 26.8 MB (26773510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4adf19bf3e6f542f3c00d3fc4bb83f2ec48ccc9675502c518d9eb368d0232a`  
		Last Modified: Mon, 08 Sep 2025 22:13:48 GMT  
		Size: 69.8 MB (69794254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ddee6848f3c7553d2f09caa8fa71a3298ce47aff877c83ce656cfa9661aaeb`  
		Last Modified: Mon, 29 Sep 2025 17:56:31 GMT  
		Size: 100.5 MB (100533204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe29e58b8c06a986ae5ca92831db1a0d8e315d4140a28e6305b3b9513f262ee`  
		Last Modified: Mon, 29 Sep 2025 17:56:00 GMT  
		Size: 82.5 MB (82530689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1973ab304142b1f93f3e547713db1530d01a5e3fd56f4a99402ea405e107dfa`  
		Last Modified: Mon, 29 Sep 2025 17:56:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6056c744926a8ee76923e28c02d6fb8ad87862499ad17609ebc79ceb11ed8d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10783169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98be95f1d2e528f62dc2b2c577eeeda04271146e71d77be5b9a85d2bdadb77c0`

```dockerfile
```

-	Layers:
	-	`sha256:5ff5a1257e97aa3790cb20863a2638700a5c1ea566b95b3465efad9b48af505f`  
		Last Modified: Mon, 29 Sep 2025 20:24:05 GMT  
		Size: 10.8 MB (10754200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e22affcb17513db0bb7b755e22390a0c6e102a60a80b11f8884365d74271db`  
		Last Modified: Mon, 29 Sep 2025 20:24:06 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:13dc957c166649ec10cdfd12f55f3231cf8bca61d2d43d40ce77431dac41277d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327134545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9f8ccb2b3d146b2a2a29242d0811be5dc8b8bc3994fc99429c186ad866e516`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bf3914a916f37a54163b2eb02b685f6e0d654680e02a5e51b78387e81e4077`  
		Last Modified: Tue, 09 Sep 2025 06:02:47 GMT  
		Size: 27.0 MB (26993871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31355a04af67dd51f580585ba523dfd2b5ad7d91e873cb7213748a572df48bb6`  
		Last Modified: Tue, 09 Sep 2025 15:30:51 GMT  
		Size: 73.0 MB (73033628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8672ea681bc1020ea13fedba257ffcddf80ac9064cc95839dafcc76d676aeca`  
		Last Modified: Mon, 29 Sep 2025 18:06:48 GMT  
		Size: 92.8 MB (92794864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4682e6be6673e7aa33301c5b30874cd778044246d060f0fbf3c29475651b8b`  
		Last Modified: Mon, 29 Sep 2025 18:07:23 GMT  
		Size: 81.2 MB (81207592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa39ffd67e922714c103a86fa0b75372d24b05911527debb49f81cf45d1402f6`  
		Last Modified: Mon, 29 Sep 2025 18:07:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ea57ea5b2589f5ac4e040154afbaaa70a749daa79a6c3160b02ae84cdac58316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10807783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8931bbe1711f750eb1953636096afadcee1b76447aad4542fd66d53143b8366e`

```dockerfile
```

-	Layers:
	-	`sha256:c7f8f64844969ab78498d8497767e83f7f7954782d7b5f819305ca4ce840c511`  
		Last Modified: Mon, 29 Sep 2025 20:24:14 GMT  
		Size: 10.8 MB (10778718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b17d1d9c73fd4e0ba2a8649185f3ee5744ef5f0d276aafbd32e821fefc0e00`  
		Last Modified: Mon, 29 Sep 2025 20:24:15 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:f4da1ba9c9c7ad918101c26d0ac64f2310e6a162a5d506847c64dfecb25bb699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352463360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5102795c9c08e1e1446eec4cb8f5e28028b6f387543784c19f96d53a44441347`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1afb27b72dabce7ba373ba8319bd1ccd2205d7724f23909527bd3da7476b1`  
		Last Modified: Thu, 11 Sep 2025 01:43:59 GMT  
		Size: 25.0 MB (24952790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32856986223852ec3f854d1a7c152bc97555c3c9e06114ce074d65dc96a8dee`  
		Last Modified: Fri, 12 Sep 2025 02:24:28 GMT  
		Size: 66.7 MB (66660361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ccaac1efde5b5edf5e06fc7214fdc1986a9341055511d69b9c3f5e789f783`  
		Last Modified: Mon, 15 Sep 2025 06:09:44 GMT  
		Size: 131.6 MB (131561217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1abfcbaa70a0168de1aea7c77a550816bb9fc5ed593a95bf38e36239223dcc`  
		Last Modified: Mon, 29 Sep 2025 19:43:19 GMT  
		Size: 81.5 MB (81523388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2c56556b49c578f23a92e42e210b7b13986f3cc8d56482663e5a031b815bd4`  
		Last Modified: Mon, 29 Sep 2025 19:43:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:27955e6ee5599c455ee98f250178a9b86b6e33d4cd3c94bbc5ae09c2b432b670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10881621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59eb908ff1722084c248fce56cf8ff20c2dc66f6cc4fb97d7f9fce23402039fc`

```dockerfile
```

-	Layers:
	-	`sha256:d0cbacb0b9b39856fcd5920eb5bd5895f0515c03993fcb93b9b36d09fc268c1d`  
		Last Modified: Mon, 29 Sep 2025 20:24:26 GMT  
		Size: 10.9 MB (10852551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8c0d04ce966ad6a8b54cae50e03991573fc26651136658232cce5cb78fb74d`  
		Last Modified: Mon, 29 Sep 2025 20:24:27 GMT  
		Size: 29.1 KB (29070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:e47f0341f62d628c69dc899d973f6e3c76912c1985e0f1fcbb9f4c3193377d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303101229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9664e2226d6a42a612ae22049c0d9e7ff504279e3d9a8326c1fd337e981e93a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 29 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775d8e7868b319a235eef909d5a12163c48c579e84d18d78ed794653cb126a0`  
		Last Modified: Tue, 09 Sep 2025 06:02:49 GMT  
		Size: 26.8 MB (26780367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76c2286bf1bfe1b0d2250435d28c0af55c645ac84ddeac003b9da9b68c9c87`  
		Last Modified: Tue, 09 Sep 2025 12:08:32 GMT  
		Size: 68.6 MB (68636032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891b0563252f214cb0223fbb0c0ce70a68fc283bcf28977ad8d51239efb3c4c3`  
		Last Modified: Mon, 29 Sep 2025 18:05:39 GMT  
		Size: 75.9 MB (75900343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ed6e6981e4c029c9853a9bbba242bc2c9b41f236141c1f10c1334ce58549f0`  
		Last Modified: Mon, 29 Sep 2025 18:05:39 GMT  
		Size: 82.4 MB (82438002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e9492694eea7934c1a9656013b19ea12ce898df57eb8858aefa7cece0ee72c`  
		Last Modified: Mon, 29 Sep 2025 18:05:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7210ae2b04ac57337a9e696a9f2a6181763857900791bc95a2e696e5b477c9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10622341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df967678961939cbee59e6c296bf109500c374c9748e9ffba68a76a9d59c7b5`

```dockerfile
```

-	Layers:
	-	`sha256:545a6b6664528ac4446d89530b5f141a4bb2b39e9348f3d28acb27df7c423d94`  
		Last Modified: Mon, 29 Sep 2025 20:24:33 GMT  
		Size: 10.6 MB (10593334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a6fc86316a1ae632cd1de5b0f7977feaf993430eb36f6ea2418ce6ee0441b65`  
		Last Modified: Mon, 29 Sep 2025 20:24:34 GMT  
		Size: 29.0 KB (29007 bytes)  
		MIME: application/vnd.in-toto+json
