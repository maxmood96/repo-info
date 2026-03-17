## `golang:bookworm`

```console
$ docker pull golang@sha256:4465644228bc2857a954b092167e12aa59c006a3492282a6c820bf4755fd64a4
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

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:77d2fa8be6beead13c85eb83d016c17806a376015a8b6a7ba24bc4c992e654b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296587819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f6bb0d92dd258d6f37c7e323e4c0841dd2103c4e795f5209a58c72130cae4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:32 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 17 Mar 2026 00:19:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 00:19:32 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 00:19:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:19:32 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 00:19:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 00:19:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f83c2f7b0b1b208471e45488b49766ed4316c4776bc2dba21d26d0e3467742`  
		Last Modified: Tue, 17 Mar 2026 00:20:04 GMT  
		Size: 92.4 MB (92448373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbff1d4eb7eece408734c05c8c63a49bb181871bc1280cff3f0e28d25a4ea28`  
		Last Modified: Fri, 06 Mar 2026 01:12:19 GMT  
		Size: 67.2 MB (67216879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eba8db39001fdcf35b6ddfb3581804c75b744045071857f53d2112cd88c7ccd`  
		Last Modified: Tue, 17 Mar 2026 00:20:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:01b1dcc59eed848582ec316ac6df8d5c4fe9333237367546bd8eb7bae0b9b5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2dd964814448c4b6ace4d14203d665164261f0f43e4c72477aa8d19757cecd`

```dockerfile
```

-	Layers:
	-	`sha256:cb91d324392c93741628b591922e332a928261514dae6b0ea1dd19269e834ac6`  
		Last Modified: Tue, 17 Mar 2026 00:20:03 GMT  
		Size: 10.5 MB (10497855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa630fcd6dee62679e0fe9125d8c69905856ab28e6b950e0c79b1da23e5b3947`  
		Last Modified: Tue, 17 Mar 2026 00:20:02 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:98a8bef0709f4079daa0fb40ea85c4e4c5d53c559ab8052e31beb492ba05bdab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257864378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76a871a643a0545c351160552618f72d65c345650ffb0840aab21dc972c9060`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:51:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:16:33 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 17 Mar 2026 01:16:33 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 01:16:33 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 01:16:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:16:33 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 01:16:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 01:16:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c259f98025fcc3d44333815b426fe9bea34608d38b537248297aff1482d389`  
		Last Modified: Tue, 17 Mar 2026 00:51:25 GMT  
		Size: 59.7 MB (59652088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8fb6a599622442d2346e0244ca61f9e40ff028d92ee20ab13c821c61fa0a5c`  
		Last Modified: Tue, 17 Mar 2026 01:17:02 GMT  
		Size: 66.3 MB (66305404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c71a08a325c7d5f7b73bc8da93a0980d5401206ec7c3b40584ca8d21ca82f77`  
		Last Modified: Fri, 06 Mar 2026 01:11:53 GMT  
		Size: 65.8 MB (65757104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04279a42db68713efaf5a32cb4d9594440308c229c5efa674fe01aa69a0858d`  
		Last Modified: Tue, 17 Mar 2026 01:17:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:82d06cd0fecd112c19011ae18568d3483ed96f9c1b0404abae25c641ed5a0031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ecd013c91996acc25c70c6c4477510e0080574bbe70c73d0d68b952c436c41`

```dockerfile
```

-	Layers:
	-	`sha256:ccb8a6eba51145436f79a1e97650864353395574cf61f87a6263215a36956bc3`  
		Last Modified: Tue, 17 Mar 2026 01:17:00 GMT  
		Size: 10.3 MB (10304567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbd169492474c5a43e83160fd7604fd2e52ffa81b6d9b4575e4b4a477d492ed7`  
		Last Modified: Tue, 17 Mar 2026 01:17:00 GMT  
		Size: 27.9 KB (27902 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5175dbf45366363da42b8117071b007901ed257f35ce0b96762e6e5338de7c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287084617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1819173be6759fc8a29ff5dac7ce7c2ac7fd0798760051655e5a12fe9c16183d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:43 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 17 Mar 2026 00:19:43 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 00:19:43 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 00:19:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:19:43 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 00:19:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 00:19:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d400e7298ced7068a80e7585bd338ad03202c948fb5679d3290d0b4497af54`  
		Last Modified: Tue, 17 Mar 2026 00:20:12 GMT  
		Size: 86.5 MB (86521155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49db9bb2f958b7444a4f28145af7a815dd0a47fec1608d03e2f1c673b3aa858b`  
		Last Modified: Fri, 06 Mar 2026 01:12:04 GMT  
		Size: 64.1 MB (64106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eacdd96638d1c23d2036ad1f887f1ddb5aa71b14524a49d41783f0d51c35238`  
		Last Modified: Tue, 17 Mar 2026 00:20:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f9a7ca4b0e75ffc9ed7104fa7adcc4ccf85bc0f69354ea4f155f18499ca78d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8fe9a4cdac0fcf7366e3a85aba3b93f3f40c1c9ff4999c62e0522440812aa1`

```dockerfile
```

-	Layers:
	-	`sha256:721a4f99b49c05090c9f0e3836a657fbab979a429873103e8c3fbd3999bc4bc3`  
		Last Modified: Tue, 17 Mar 2026 00:20:11 GMT  
		Size: 10.5 MB (10525703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:509d872f787a44bfdd7efafdd9961c3c8b043db90efbeb12661cdf79fae38702`  
		Last Modified: Tue, 17 Mar 2026 00:20:10 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:28a36c3c309d3a0915b6d17871ded3cca747751fa08f164bac78f230cc5d094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295997005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0663cfe483f9aa4d38d394151c159286b4dd5ca10470f9d063bf9aef0a8e7d8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:41:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:46 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 17 Mar 2026 00:19:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 00:19:46 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 00:19:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:19:46 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 00:19:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 00:19:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7cf39578e27046e7ba7fa5d4d45df198790a004a9eb86583e977b3b055c88`  
		Last Modified: Mon, 16 Mar 2026 22:43:53 GMT  
		Size: 24.9 MB (24871994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9d2da3801adad27eefa73bb7b5ab6c0c94f46583823a923caa8e9b995a97b`  
		Last Modified: Mon, 16 Mar 2026 23:41:39 GMT  
		Size: 66.2 MB (66234305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634f1559517fce4acd712516d6f9885dce98d99aa8d4f1fb511bb5ed62723e3f`  
		Last Modified: Tue, 17 Mar 2026 00:20:16 GMT  
		Size: 89.9 MB (89871099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb07caf9c739767295e4b0d3b36abebfa29f9d22222644122dcb4a2deeeddd8`  
		Last Modified: Fri, 06 Mar 2026 01:12:15 GMT  
		Size: 65.5 MB (65541795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844667254c234171258771591202e8e0856627fc8748a53d7b70e3d76cede19e`  
		Last Modified: Tue, 17 Mar 2026 00:20:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6b7deb443900c9fae0d7c7c028abb3a61ddd98cc90a804a16d18df03d1900abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10505186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9d34c8c4aaf8b159fed76f69766fd5dc01c8aa79645c6779ecb80c0fa71057`

```dockerfile
```

-	Layers:
	-	`sha256:5b7a266632f3ba6cba05d6b2cdc065d9ad293eea77ef37a0c786d5babc187a7e`  
		Last Modified: Tue, 17 Mar 2026 00:20:14 GMT  
		Size: 10.5 MB (10477425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f050c6d70409df8ff0e9f88cc5c0f3fcfa8cd7996210d69a7b1f2f7d3deab4f`  
		Last Modified: Tue, 17 Mar 2026 00:20:13 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:83c83188f0eb01e906157de4d07661cee3a922a03e8a6f0f15ca5a6c2279c3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268573745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7176105cc6c7d9b75c15c15389d74a674c742a1489f861e6b68a7372eb42b7`
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
# Fri, 06 Mar 2026 01:12:58 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:12:58 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:12:58 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:12:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:12:58 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:13:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:13:13 GMT
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
	-	`sha256:64d21856571c72ef8af5b19f925f062fc14aa8908cb92f4df4cdb7813e471c22`  
		Last Modified: Fri, 06 Mar 2026 01:15:01 GMT  
		Size: 62.8 MB (62812269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469937ca5c79e7f534dcb11ac55d0b22b2b07b39db2de6c786d571eb5b30112d`  
		Last Modified: Fri, 06 Mar 2026 01:14:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:32ec9e31b3acee2810c3045680031b5c87698382accfae229c6c741dac16e508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667fefd34d2c4da351bfb05642ab37633ae534866f03424727dd7efa538bf137`

```dockerfile
```

-	Layers:
	-	`sha256:370829e532096ab1e42a9b3ca6ae6b6e191cf7e808b2d30d6f8064a3ccd0fae0`  
		Last Modified: Fri, 06 Mar 2026 01:14:54 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:3d2a119c572fa9fab029aa7981fdbf0cb8ff5e2289337404794daeb2181a8d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303083215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e028128c81824aa684b087d13f0afe154eebd641ac84fb7fc3d870b4f12a587a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 06:03:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:42:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:10:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:10:37 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 08:42:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 08:42:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6053003aae760c21f129e32066714b891ab6bc6ec6abdf0f13ff20cb85ede`  
		Last Modified: Tue, 17 Mar 2026 01:49:00 GMT  
		Size: 25.7 MB (25671576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc763fa93abbd05d9932abad5e62ea754d4d526450c9517c9e5b75b5c914969`  
		Last Modified: Tue, 17 Mar 2026 06:04:00 GMT  
		Size: 69.8 MB (69846151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6def63f9899aff9dec9e9602eb9cdc01aa08dd0545734ab481d2e9c86c5213`  
		Last Modified: Tue, 17 Mar 2026 08:43:26 GMT  
		Size: 90.5 MB (90462652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace710cfb3bb4da72d185d83d05e86cb22a686c0abd5be3e83cdf74e34b68d02`  
		Last Modified: Fri, 06 Mar 2026 01:12:05 GMT  
		Size: 64.8 MB (64765980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67dfe706ac5dcf941588fa9bf37ca305dbefede92ab97b32dcfa601b0f5cd08`  
		Last Modified: Tue, 17 Mar 2026 08:43:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2d203b21311efdeb88518bdc73983227ddbba3f893491614e91148055e2da1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7cd9216d8e3a746aa527449e85283962dd974022bdb7043a110f739146a04f`

```dockerfile
```

-	Layers:
	-	`sha256:e33b6b333ebebf1dbe2e12c17707a2725972153f2ca2c9811900bb207c3324ce`  
		Last Modified: Tue, 17 Mar 2026 08:43:24 GMT  
		Size: 10.5 MB (10470352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fe9f2fb382f8c66e768ef232cff15780a5bd7c40c776b1b1c9acd108c67af2`  
		Last Modified: Tue, 17 Mar 2026 08:43:23 GMT  
		Size: 27.7 KB (27671 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:658aefd14dfc03ab71b0035ce8da7c30fb7319098300d4a442bb4898de2ae829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270171217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe78d7ec0e8d112a1a6331a57a0fde7941530e045accba24b986400b71ce136b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:10:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:10:52 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 02:24:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 02:24:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d904b886f0656b8d9f7b2cc64089c6c03aa31b22b97fbf96b0bc6c4e3726e429`  
		Last Modified: Mon, 16 Mar 2026 23:44:29 GMT  
		Size: 24.0 MB (24033614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3244a56b42252330a5ec4502181ecac45b16d96de3113430b375f7d10e72bde6`  
		Last Modified: Tue, 17 Mar 2026 01:33:52 GMT  
		Size: 63.5 MB (63501466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a757a435c6399d13de6560d3516a2b4b0945c41375506fc8eccb2e411c3db`  
		Last Modified: Tue, 17 Mar 2026 02:25:46 GMT  
		Size: 69.1 MB (69055313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ac4fc296175935efd55931d7d181f8e7c85d38405c6fdcb1a96bcb9115d7eb`  
		Last Modified: Fri, 06 Mar 2026 01:11:11 GMT  
		Size: 66.4 MB (66432747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faea77de6eaef80edd01b32032dc1b0402ae24e4bfcf67e30b6faa36698fb86b`  
		Last Modified: Tue, 17 Mar 2026 02:25:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6882448d061081f004062bd064a4158b11953a056b906c3b2d1dbf5c87f47d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5b8a9aab8c89cc723e4bb7fb43604159874114fdcededc4c5daa3e4ea7e62f`

```dockerfile
```

-	Layers:
	-	`sha256:fbe7a4b00e64364c6199041101f0c7a8bdaa414ce5d94d591bf0b0350020081f`  
		Last Modified: Tue, 17 Mar 2026 02:25:45 GMT  
		Size: 10.3 MB (10329613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cff798a5b99864d94d2d401b5facd769c656072c4a2e1acb737e8bc21349e4d`  
		Last Modified: Tue, 17 Mar 2026 02:25:44 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json
