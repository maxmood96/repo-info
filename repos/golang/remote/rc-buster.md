## `golang:rc-buster`

```console
$ docker pull golang@sha256:4d39840a5850604ef6729bf1bd9dfd2d8c42d788435e05e7d2b6fd7bf6302e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `golang:rc-buster` - linux; amd64

```console
$ docker pull golang@sha256:17792be58c4cd5c20a1e958752c3b5e364a11109eb87b5966568373be248a011
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.8 MB (309847852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f246c5aedc453a72fb3718e1ee0bdc1f99ec5f16fadaa1b88b33c7767698f0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:33 GMT
ADD file:4b03b5f551e3fbdf47ec609712007327828f7530cc3455c43bbcdcaf449a75a9 in / 
# Tue, 04 Aug 2020 15:42:34 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:26:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:26:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 23:26:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 10:31:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 10:31:10 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:21:27 GMT
ENV GOLANG_VERSION=1.15rc2
# Fri, 07 Aug 2020 23:21:39 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='f41a08f630f018bc5d9fd100bd9899516e4965356c78165157eb0eda9a17ac09' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='60d4d7723ef55d49bbf8326f37011f967048ae9167ef462ee4b9af311c4f3244' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='e3e2cd95df2491d3cd74af9f73235dbf031dd2ecaf1140ab2793756be87d915f' ;; 		i386) goRelArch='linux-386'; goRelSha256='9c1f1ed42bd5f776f3585e39e3ba165a9b8ac8fde45dafbb6e41e04bae44bb3d' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='9eb1d694eaf5104bf80187b6a3c3f0201c598b095f23e8af2bbb19ca3fb12d21' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='272793157e27c5a09e216f61f6a84d70808a901b89cc69b9e8cd6f8e019be27a' ;; 		*) goRelArch='src'; goRelSha256='3c6b4db00ec6d8958bb5693729343d08c245b634267130a966f052758579626b'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 07 Aug 2020 23:21:40 GMT
ENV GOPATH=/go
# Fri, 07 Aug 2020 23:21:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:21:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 Aug 2020 23:21:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d6ff36c9ec4822c9ff8953560f7ba41653b348a9c1136755e653575f58fbded7`  
		Last Modified: Tue, 04 Aug 2020 15:48:55 GMT  
		Size: 50.4 MB (50396000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c958d65b3090aefea91284d018b2a86530a3c8174b72616c4e76993c696a5797`  
		Last Modified: Tue, 04 Aug 2020 23:39:28 GMT  
		Size: 7.8 MB (7811570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf0a6b092f5673ec05b40edb606ce58881b2f40494251117d31805225ef064`  
		Last Modified: Tue, 04 Aug 2020 23:39:27 GMT  
		Size: 10.0 MB (9996337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80931cf6881673fd161a3fd73e8971fe4a569fd7fbb44e956d261ca58d97dfab`  
		Last Modified: Tue, 04 Aug 2020 23:39:45 GMT  
		Size: 51.8 MB (51829826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813643441356759e9202aeebde31d45192b5e5e6218cd8d2ad216304bf415551`  
		Last Modified: Wed, 05 Aug 2020 10:33:40 GMT  
		Size: 68.7 MB (68672152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c64575eb181681a6e2f55b679bcd3be99a37a94356af5dead6cc7d9f7405fb`  
		Last Modified: Fri, 07 Aug 2020 23:25:22 GMT  
		Size: 121.1 MB (121141841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82ffcd6a33a895dc866d5b4a940fb237c62b2491964eb6c453031227485a8b1`  
		Last Modified: Fri, 07 Aug 2020 23:25:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:f793f2347d7916a2dda355e494b8a49a0e0b29fbd68c413e89634bce876b6c6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269793948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a93b6d539757ff63906a8a58f6da6cb720756508c83d446b4224cbe49a26384`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:11:38 GMT
ADD file:e1152998db9c9a59e88100fa415cb22c317d906c5143042e7e36fa6911264f66 in / 
# Tue, 04 Aug 2020 03:11:50 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:13:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:13:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 06:14:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 15:39:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 15:39:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:48:35 GMT
ENV GOLANG_VERSION=1.15rc2
# Sat, 08 Aug 2020 00:17:16 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='f41a08f630f018bc5d9fd100bd9899516e4965356c78165157eb0eda9a17ac09' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='60d4d7723ef55d49bbf8326f37011f967048ae9167ef462ee4b9af311c4f3244' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='e3e2cd95df2491d3cd74af9f73235dbf031dd2ecaf1140ab2793756be87d915f' ;; 		i386) goRelArch='linux-386'; goRelSha256='9c1f1ed42bd5f776f3585e39e3ba165a9b8ac8fde45dafbb6e41e04bae44bb3d' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='9eb1d694eaf5104bf80187b6a3c3f0201c598b095f23e8af2bbb19ca3fb12d21' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='272793157e27c5a09e216f61f6a84d70808a901b89cc69b9e8cd6f8e019be27a' ;; 		*) goRelArch='src'; goRelSha256='3c6b4db00ec6d8958bb5693729343d08c245b634267130a966f052758579626b'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 08 Aug 2020 00:17:42 GMT
ENV GOPATH=/go
# Sat, 08 Aug 2020 00:18:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Aug 2020 00:19:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 08 Aug 2020 00:19:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:43e007f43c47fbc3bc147d3d82021dc9a400b509f9c30dc687c1a3ed5fd23065`  
		Last Modified: Tue, 04 Aug 2020 03:33:39 GMT  
		Size: 48.1 MB (48108803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0270eaf99061a6aa3af6cdd0f5e0ae94bf697d7565783759c971252b202c37dd`  
		Last Modified: Tue, 04 Aug 2020 06:36:56 GMT  
		Size: 7.4 MB (7360991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e527b7990670f219ff9d29ac8963fbdc4756e6c6190434bba9c0482626f4ca`  
		Last Modified: Tue, 04 Aug 2020 06:36:57 GMT  
		Size: 9.7 MB (9687011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556ab5cdb159eebd1404529d56d69ebe7cdffa65e8113e5d41a2e11fee7a734e`  
		Last Modified: Tue, 04 Aug 2020 06:37:26 GMT  
		Size: 49.6 MB (49572627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafbe12c84a35ce4d898d99657a0d607864ab5b33b05b3d2b359ea6510cd7bbc`  
		Last Modified: Tue, 04 Aug 2020 17:07:14 GMT  
		Size: 52.0 MB (51975393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac66df6990aef1e83303b2e1399cb66e774c9b1194b71e06eb1190737e0c64ef`  
		Last Modified: Sat, 08 Aug 2020 00:21:09 GMT  
		Size: 103.1 MB (103088967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5821fef2c932168549b38f28343bd429fd73c3a645a3c872a613e10de7ec0c7`  
		Last Modified: Sat, 08 Aug 2020 00:20:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:47ef947e476bcd81b3581a9e40cb0306a14ccabde8434ff8d93c595f9006bfef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260775241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e32b4a4edf0ac36fe597966c2b739ed61a54bb79886dfffd18cf4cf097f4853`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:56:26 GMT
ADD file:aaf5c6340b3d662631775fa4536c2e48e9f68b6cc8d53e18fb8fd76ae41b305e in / 
# Tue, 04 Aug 2020 04:56:28 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:52:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:53:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 07:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:40:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:40:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:58:11 GMT
ENV GOLANG_VERSION=1.15rc2
# Sat, 08 Aug 2020 00:00:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='f41a08f630f018bc5d9fd100bd9899516e4965356c78165157eb0eda9a17ac09' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='60d4d7723ef55d49bbf8326f37011f967048ae9167ef462ee4b9af311c4f3244' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='e3e2cd95df2491d3cd74af9f73235dbf031dd2ecaf1140ab2793756be87d915f' ;; 		i386) goRelArch='linux-386'; goRelSha256='9c1f1ed42bd5f776f3585e39e3ba165a9b8ac8fde45dafbb6e41e04bae44bb3d' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='9eb1d694eaf5104bf80187b6a3c3f0201c598b095f23e8af2bbb19ca3fb12d21' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='272793157e27c5a09e216f61f6a84d70808a901b89cc69b9e8cd6f8e019be27a' ;; 		*) goRelArch='src'; goRelSha256='3c6b4db00ec6d8958bb5693729343d08c245b634267130a966f052758579626b'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 08 Aug 2020 00:00:41 GMT
ENV GOPATH=/go
# Sat, 08 Aug 2020 00:01:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Aug 2020 00:02:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 08 Aug 2020 00:02:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e7cf402ee4b1ba67e92813d50297a082bbdbdd4d47f6aeb62f2316b81d5dc843`  
		Last Modified: Tue, 04 Aug 2020 05:04:56 GMT  
		Size: 45.9 MB (45869261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff6bd4a89fc21d80ca6924320f86708f35ddea71c7aa34a408a5b64257c764e`  
		Last Modified: Tue, 04 Aug 2020 08:25:56 GMT  
		Size: 7.1 MB (7097820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48f5852a753b7731e5d374567ae9b64e309805758f336c76d5f13bb67c94e20`  
		Last Modified: Tue, 04 Aug 2020 08:25:56 GMT  
		Size: 9.3 MB (9343353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58a93b33dd4d533cc1e04eab8045940d69cb287134aa90c982e3d248739044e`  
		Last Modified: Tue, 04 Aug 2020 08:26:25 GMT  
		Size: 47.4 MB (47355829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb05471d9930e275bf9cac0b1bb0b93b8dde80ac8dd073dcb65c384d6d9e2ad`  
		Last Modified: Wed, 05 Aug 2020 01:45:54 GMT  
		Size: 53.1 MB (53140891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aafea0748830cc72686faf57d95552211d3be3371dd71e2d6b96db90990e18`  
		Last Modified: Sat, 08 Aug 2020 01:15:13 GMT  
		Size: 98.0 MB (97967933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de32b2986a8e65591c32def1f8bc925dba0ee8096a11cac4998bb0293cdd44bd`  
		Last Modified: Sat, 08 Aug 2020 01:14:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:fe458194debc09f08c10a26b6cd4f49915974525891d7dd21090dde3cfe0483f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279261651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e277c1efef26dc760e509fab82816cb08476e9565d0489c87f7b2b755c5488`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:06 GMT
ADD file:ce999027b153d392f8a0f85e2e7a17b9279f3cf7ad0e45192378d527275f99c6 in / 
# Tue, 04 Aug 2020 06:57:08 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:10:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:10:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 11:10:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 07:19:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 07:19:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:42:50 GMT
ENV GOLANG_VERSION=1.15rc2
# Fri, 07 Aug 2020 23:43:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='f41a08f630f018bc5d9fd100bd9899516e4965356c78165157eb0eda9a17ac09' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='60d4d7723ef55d49bbf8326f37011f967048ae9167ef462ee4b9af311c4f3244' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='e3e2cd95df2491d3cd74af9f73235dbf031dd2ecaf1140ab2793756be87d915f' ;; 		i386) goRelArch='linux-386'; goRelSha256='9c1f1ed42bd5f776f3585e39e3ba165a9b8ac8fde45dafbb6e41e04bae44bb3d' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='9eb1d694eaf5104bf80187b6a3c3f0201c598b095f23e8af2bbb19ca3fb12d21' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='272793157e27c5a09e216f61f6a84d70808a901b89cc69b9e8cd6f8e019be27a' ;; 		*) goRelArch='src'; goRelSha256='3c6b4db00ec6d8958bb5693729343d08c245b634267130a966f052758579626b'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 07 Aug 2020 23:43:09 GMT
ENV GOPATH=/go
# Fri, 07 Aug 2020 23:43:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:43:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 Aug 2020 23:43:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d5517ee72007172d5b814636405254dea459120ce08f85777bb287d106a6a240`  
		Last Modified: Tue, 04 Aug 2020 07:03:41 GMT  
		Size: 49.2 MB (49175491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283897ad4463628bd259e1cbb5eb788e7df554b42ae17fc6f5d02c4a56035c2`  
		Last Modified: Tue, 04 Aug 2020 11:23:01 GMT  
		Size: 7.7 MB (7681458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feb40d9f5fecfa098b8f7ece6c287c6fd61b114043c8b4647359120a7d943a3`  
		Last Modified: Tue, 04 Aug 2020 11:23:02 GMT  
		Size: 10.0 MB (9983917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b5fabb62f79acd92186da3c02d23bd8c15d79603a700959b582bd9e62854c`  
		Last Modified: Tue, 04 Aug 2020 11:23:28 GMT  
		Size: 52.2 MB (52163657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c836803dd1977ffe173b42414e8c2ae2e147cee2e1ee34a383f4251cf15a44`  
		Last Modified: Wed, 05 Aug 2020 07:23:33 GMT  
		Size: 62.5 MB (62532046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe89de62d06fef490027b98a28ee95d260d7227bdeba4a8b7feb11753e65116`  
		Last Modified: Fri, 07 Aug 2020 23:46:56 GMT  
		Size: 97.7 MB (97724926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b275c2365e96dda87effa3783e5c267b4d9203b67cf15004e72ee079f7ff9`  
		Last Modified: Fri, 07 Aug 2020 23:46:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; 386

```console
$ docker pull golang@sha256:04e249d1ee4eb163625defc04b48ef75747010abadf34f5c6f91fd0e2bc6fb0e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (297043170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ff36efcd6c85d5a06f6c35b0d103cdafeec9f9e43a88a5a3231ef732c3850b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:21 GMT
ADD file:e8aac36755acd0915e9f9bae82fc8fcd0bbc3911ca4a5a40e104b2a4ebce44da in / 
# Tue, 04 Aug 2020 03:37:21 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:06:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:06:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 08:07:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 18:43:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 18:43:53 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:39:44 GMT
ENV GOLANG_VERSION=1.15rc2
# Fri, 07 Aug 2020 23:40:07 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='f41a08f630f018bc5d9fd100bd9899516e4965356c78165157eb0eda9a17ac09' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='60d4d7723ef55d49bbf8326f37011f967048ae9167ef462ee4b9af311c4f3244' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='e3e2cd95df2491d3cd74af9f73235dbf031dd2ecaf1140ab2793756be87d915f' ;; 		i386) goRelArch='linux-386'; goRelSha256='9c1f1ed42bd5f776f3585e39e3ba165a9b8ac8fde45dafbb6e41e04bae44bb3d' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='9eb1d694eaf5104bf80187b6a3c3f0201c598b095f23e8af2bbb19ca3fb12d21' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='272793157e27c5a09e216f61f6a84d70808a901b89cc69b9e8cd6f8e019be27a' ;; 		*) goRelArch='src'; goRelSha256='3c6b4db00ec6d8958bb5693729343d08c245b634267130a966f052758579626b'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 07 Aug 2020 23:40:07 GMT
ENV GOPATH=/go
# Fri, 07 Aug 2020 23:40:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:40:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 Aug 2020 23:40:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b19305c328889ec69ec0d76e403c2cbc4603e5f27213a0e4d5f6597feefcf6e1`  
		Last Modified: Tue, 04 Aug 2020 03:42:18 GMT  
		Size: 51.2 MB (51158828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d9322a54f80129fd5cd69b7be3ac6ba44b9a0268afcbd10876508eb0f9264c`  
		Last Modified: Tue, 04 Aug 2020 08:25:50 GMT  
		Size: 8.0 MB (7981119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a7f32100867eafa619a9265416538a2a374b88219902c6270b6f023d19061`  
		Last Modified: Tue, 04 Aug 2020 08:25:51 GMT  
		Size: 10.3 MB (10338494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ea04987808c324433cf4b1b813ccf6528f9bf603422fbee2725c1e4018eb8`  
		Last Modified: Tue, 04 Aug 2020 08:26:25 GMT  
		Size: 53.4 MB (53433408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a9b823cf68f4d55b8db75bbbafe8018b21b444b78e7eaeab85ee790d02848`  
		Last Modified: Tue, 04 Aug 2020 18:46:40 GMT  
		Size: 73.5 MB (73530875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9aa3e4c4ab08fdbcd918e600cb8c53554f166aa858bfb96e5f64638f6f8f18`  
		Last Modified: Fri, 07 Aug 2020 23:44:06 GMT  
		Size: 100.6 MB (100600320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff145dd3f730723e7956792d34f9fa2764b83c1ef5c536565f7c5251fd0df62`  
		Last Modified: Fri, 07 Aug 2020 23:43:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; mips64le

```console
$ docker pull golang@sha256:a49c2606d8f8fd04b0fb6b45d1c6598a120d054f93b9889049e41e31eda0258b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272442350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e282a5989c5e827a1bcabb9499c51f487e4f4a53d5dba43fd7d7decdf488ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:42:01 GMT
ADD file:b98dee5937df5f9781b3c514a8c53f6f42fa8016979e581d1252ae689da15ebc in / 
# Tue, 04 Aug 2020 06:42:01 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 10:38:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:39:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 10:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 20:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 20:42:59 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Aug 2020 00:07:17 GMT
ENV GOLANG_VERSION=1.15rc2
# Sat, 08 Aug 2020 00:14:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='f41a08f630f018bc5d9fd100bd9899516e4965356c78165157eb0eda9a17ac09' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='60d4d7723ef55d49bbf8326f37011f967048ae9167ef462ee4b9af311c4f3244' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='e3e2cd95df2491d3cd74af9f73235dbf031dd2ecaf1140ab2793756be87d915f' ;; 		i386) goRelArch='linux-386'; goRelSha256='9c1f1ed42bd5f776f3585e39e3ba165a9b8ac8fde45dafbb6e41e04bae44bb3d' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='9eb1d694eaf5104bf80187b6a3c3f0201c598b095f23e8af2bbb19ca3fb12d21' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='272793157e27c5a09e216f61f6a84d70808a901b89cc69b9e8cd6f8e019be27a' ;; 		*) goRelArch='src'; goRelSha256='3c6b4db00ec6d8958bb5693729343d08c245b634267130a966f052758579626b'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 08 Aug 2020 00:14:45 GMT
ENV GOPATH=/go
# Sat, 08 Aug 2020 00:14:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Aug 2020 00:14:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 08 Aug 2020 00:14:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:91cc9e0aa8bcda5d45dd8780d9369f22c649c4d8fcd354183a1d0d6a7102744e`  
		Last Modified: Tue, 04 Aug 2020 06:47:56 GMT  
		Size: 49.0 MB (49017231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1447a30fea55273b0a628cb142daba1f5482171d155f458d47b5cadd49079d9`  
		Last Modified: Tue, 04 Aug 2020 10:50:50 GMT  
		Size: 7.2 MB (7231573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2846bcb2ba044284b6ee8c358e6d443ac48b4e01c2e72e0f8bd252128a30a0d`  
		Last Modified: Tue, 04 Aug 2020 10:50:50 GMT  
		Size: 10.0 MB (10015826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb4e1f307e1aa9ad1acfb68478ca06e971c7136b431f8d954ac34b08301dd7a`  
		Last Modified: Tue, 04 Aug 2020 10:51:40 GMT  
		Size: 50.8 MB (50842110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c52db771909adccb0c2e856f6f758b5cd8ee4c13737741bc18882f8f97544ea`  
		Last Modified: Tue, 04 Aug 2020 21:07:17 GMT  
		Size: 54.6 MB (54586297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a32e90d6e9477b0c6bbdba9dee31293a03fe10a16fd5ed49da4a10e311ec017`  
		Last Modified: Sat, 08 Aug 2020 00:16:35 GMT  
		Size: 100.7 MB (100749187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229b5e53ed5b60b3b139532006c6bafbcbd92f74fb9dd1e1389499b39be86be`  
		Last Modified: Sat, 08 Aug 2020 00:15:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:77eb29530b6c7236d7c97167a8b7a60b6bdc21ba4a2da8b27a1a1b73e60d8db9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300564034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7055f0d491bd839d627b0f3ca4c3cd76c6a2a96948dacc266c92489cbffc383`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:44:59 GMT
ADD file:7cc5195cf323fbee8e0c74a76984198dca35599ab18b1ecc5639fa719326bd35 in / 
# Tue, 04 Aug 2020 04:45:05 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:12:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:13:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 07:15:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 18:53:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 18:53:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:17:17 GMT
ENV GOLANG_VERSION=1.15rc2
# Fri, 07 Aug 2020 23:17:47 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='f41a08f630f018bc5d9fd100bd9899516e4965356c78165157eb0eda9a17ac09' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='60d4d7723ef55d49bbf8326f37011f967048ae9167ef462ee4b9af311c4f3244' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='e3e2cd95df2491d3cd74af9f73235dbf031dd2ecaf1140ab2793756be87d915f' ;; 		i386) goRelArch='linux-386'; goRelSha256='9c1f1ed42bd5f776f3585e39e3ba165a9b8ac8fde45dafbb6e41e04bae44bb3d' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='9eb1d694eaf5104bf80187b6a3c3f0201c598b095f23e8af2bbb19ca3fb12d21' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='272793157e27c5a09e216f61f6a84d70808a901b89cc69b9e8cd6f8e019be27a' ;; 		*) goRelArch='src'; goRelSha256='3c6b4db00ec6d8958bb5693729343d08c245b634267130a966f052758579626b'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 07 Aug 2020 23:17:56 GMT
ENV GOPATH=/go
# Fri, 07 Aug 2020 23:18:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:18:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 Aug 2020 23:18:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:db4e2d8d5901311f959f0a2271be587f91ea2826238f2a17347ffab142413f53`  
		Last Modified: Tue, 04 Aug 2020 04:52:50 GMT  
		Size: 54.1 MB (54142497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe2d012519ce68bcd2414835909fb4784fd4eb5bea2c88916fdea0c661c872e`  
		Last Modified: Tue, 04 Aug 2020 07:45:05 GMT  
		Size: 8.3 MB (8254809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f1d1f9197bf1817cda35a89da9bd2544ceb7bf0c7b92fba5977ab2b2ab9e6`  
		Last Modified: Tue, 04 Aug 2020 07:45:07 GMT  
		Size: 10.7 MB (10727103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1301750ffb48db80c63d6d21adae9f88f4f4aaf4f561ab3512287683a04c04c0`  
		Last Modified: Tue, 04 Aug 2020 07:45:33 GMT  
		Size: 57.5 MB (57455994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5c6edc9cffc52d437053d5b7d8f834d50534c930afa90b1b3aff08912cddad`  
		Last Modified: Tue, 04 Aug 2020 18:58:15 GMT  
		Size: 73.6 MB (73577651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a63614e70e218dc1561e14f1df80aeb478b82a6e43772a125ea313b669a6d75`  
		Last Modified: Fri, 07 Aug 2020 23:21:53 GMT  
		Size: 96.4 MB (96405824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e60f717efbbef5c5e29495e9b4f6e67e7fc4d7cb6a52f813aab3ed9b05c5ba3`  
		Last Modified: Fri, 07 Aug 2020 23:21:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; s390x

```console
$ docker pull golang@sha256:4e6537c8bdbb1abcdee148fdefd6b540fd0f53fad8f979ea357726c5555a05cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275524362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb57d3984793020503578981013e78cfdb4d54230d16e7b736d865f46426416`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:02 GMT
ADD file:07519836baf21317676c799c0905c76bf767fe8caa1fa718c0dfe0a152577ee8 in / 
# Tue, 04 Aug 2020 01:17:04 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 02:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:22:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 02:22:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 09:33:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 09:33:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:41:34 GMT
ENV GOLANG_VERSION=1.15rc2
# Fri, 07 Aug 2020 23:41:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='f41a08f630f018bc5d9fd100bd9899516e4965356c78165157eb0eda9a17ac09' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='60d4d7723ef55d49bbf8326f37011f967048ae9167ef462ee4b9af311c4f3244' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='e3e2cd95df2491d3cd74af9f73235dbf031dd2ecaf1140ab2793756be87d915f' ;; 		i386) goRelArch='linux-386'; goRelSha256='9c1f1ed42bd5f776f3585e39e3ba165a9b8ac8fde45dafbb6e41e04bae44bb3d' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='9eb1d694eaf5104bf80187b6a3c3f0201c598b095f23e8af2bbb19ca3fb12d21' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='272793157e27c5a09e216f61f6a84d70808a901b89cc69b9e8cd6f8e019be27a' ;; 		*) goRelArch='src'; goRelSha256='3c6b4db00ec6d8958bb5693729343d08c245b634267130a966f052758579626b'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 07 Aug 2020 23:41:50 GMT
ENV GOPATH=/go
# Fri, 07 Aug 2020 23:41:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Aug 2020 23:41:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 Aug 2020 23:41:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f2b199a6d9adcfa5f879ec8042306ab2f919623f8018d0d7a6f4e9dade5e1a71`  
		Last Modified: Tue, 04 Aug 2020 01:19:47 GMT  
		Size: 49.0 MB (48966275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5615f13ce6c82698ac5df02b39113e3a8949db1a7a7f7f5d07c9265ee15b79d0`  
		Last Modified: Tue, 04 Aug 2020 02:28:11 GMT  
		Size: 7.4 MB (7385167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ffecb808bd421be3db88ff08f67b19f28c1ffe0d4c157be3fcff3360f527bc`  
		Last Modified: Tue, 04 Aug 2020 02:28:11 GMT  
		Size: 9.9 MB (9882139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e2ce491a55134d5e4118405670fcc19b140898dc8ac62156e47a49f52e9f2d`  
		Last Modified: Tue, 04 Aug 2020 02:28:29 GMT  
		Size: 51.4 MB (51379924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e060fbdc544cffa8f72ebc5c629d0fd77e9f0ea787a2eec80f4a77dd0833d747`  
		Last Modified: Tue, 04 Aug 2020 09:35:19 GMT  
		Size: 56.7 MB (56736713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462b6b49282066721c4351582179d064ff38114748fcbabd861eade60699b601`  
		Last Modified: Fri, 07 Aug 2020 23:44:09 GMT  
		Size: 101.2 MB (101173988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3042fa739859ff3750a15e8690f7377d0aaf3cd44e5306be582a9a2e191564`  
		Last Modified: Fri, 07 Aug 2020 23:43:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
