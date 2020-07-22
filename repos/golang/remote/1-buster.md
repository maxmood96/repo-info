## `golang:1-buster`

```console
$ docker pull golang@sha256:02edbb3bba95c27ac10524bd03aea88182c3f6c4ad30c07dd36b13c73da288f8
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

### `golang:1-buster` - linux; amd64

```console
$ docker pull golang@sha256:93dd5b4bf229952226b698a28a771ff4ea9e79cd9abe155185da86e603e6cbef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312423022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf8a7ac7476f9939d55865736a3833b56338926c29eeb85d9ca90cafefbf315`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 21:13:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Jun 2020 21:11:32 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:19:53 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:20:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 17 Jul 2020 02:20:05 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:20:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:20:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:20:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4020e2aa747ca4d0ca2e87305f22f089fd57a696fd19bfa30182316d51b089a`  
		Last Modified: Tue, 09 Jun 2020 21:15:44 GMT  
		Size: 68.7 MB (68650396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca02d9b2370f6aa65d8da107f760cdd339938a8683dcb5a0fbba6669bb95c2`  
		Last Modified: Fri, 17 Jul 2020 02:31:36 GMT  
		Size: 123.7 MB (123747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6cba09e61d563b719356cd7d33f4256a32f419bd9af7e02a6643c91c0ac833`  
		Last Modified: Fri, 17 Jul 2020 02:31:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:def29066790e809ed2d8c30fe4b6bf802434133a005595ebcc7c12aa69abedb5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270494789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91a4605c60c08ca88ab823b04e05fe4aee8c664aee86d6e92ca92db1a99c2ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:50:16 GMT
ADD file:0431730a3850ee2a710a03ba04d05224938cf2f5318e1f73ed74677c70d09b78 in / 
# Wed, 22 Jul 2020 00:50:20 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:31:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:32:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:33:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 12:53:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 12:54:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 13:26:49 GMT
ENV GOLANG_VERSION=1.14.6
# Wed, 22 Jul 2020 13:56:36 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 22 Jul 2020 13:56:45 GMT
ENV GOPATH=/go
# Wed, 22 Jul 2020 13:56:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 13:57:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 22 Jul 2020 13:57:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:71cf5632cfeb30dc5a7a7ccd4742a02af636cd970ef3a45bebc17d3f20b3662d`  
		Last Modified: Wed, 22 Jul 2020 00:58:30 GMT  
		Size: 48.1 MB (48107278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87dffc06540f2eca873274114a3d8d49684b38428e946f67b0b62aa848ae49c`  
		Last Modified: Wed, 22 Jul 2020 02:02:59 GMT  
		Size: 7.4 MB (7360981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad12a2dc68e08e793efc12362e49a16257506721c8074ee8361c242244763bc4`  
		Last Modified: Wed, 22 Jul 2020 02:03:00 GMT  
		Size: 9.7 MB (9686988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94df5576e4481b3422d3ba55ceb470a19b7245355de69b1ee3efb03aec34668b`  
		Last Modified: Wed, 22 Jul 2020 02:03:38 GMT  
		Size: 49.6 MB (49572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff9d576316bd207e17a4df02e19b54d84c032ffbb919859e8c36aa226513712`  
		Last Modified: Wed, 22 Jul 2020 14:26:27 GMT  
		Size: 52.0 MB (51955015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02606364c69452a951ac7f3381037291781feed85ac614707c410c44f03df64c`  
		Last Modified: Wed, 22 Jul 2020 14:27:32 GMT  
		Size: 103.8 MB (103812001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9950538461cf34f83f8b02d4c1760706ece9c71475a34dea7b29e04d3e10d5`  
		Last Modified: Wed, 22 Jul 2020 14:27:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:e202cd00b2999d30c699fc76cadd89a3f9ed5a5ef6f01373b8d656f4902bb61c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264592630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898c852847a7914d755771170e20e4e28def68f6700850de2fdc68cc9856caf9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:00:40 GMT
ADD file:35073a186411c4b773a9d4d540ec0693ced845cb847b43d8465f9579174cd2b0 in / 
# Tue, 09 Jun 2020 01:00:45 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:48:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 18:36:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Jun 2020 21:26:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 01:58:15 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 01:59:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 17 Jul 2020 01:59:46 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 01:59:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:00:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:00:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cff0731da2e4f4a0ae8329840eb7fed7ea6aac11aecbfa15c6e684caec03920d`  
		Last Modified: Tue, 09 Jun 2020 01:09:57 GMT  
		Size: 45.9 MB (45868949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbeb0ded58d68be17265763fda36a4e1a520234a291d66f370d98a3e0d6e591`  
		Last Modified: Tue, 09 Jun 2020 02:11:21 GMT  
		Size: 7.1 MB (7097860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6159fbed770bb99a219eae06828da55caaa649879843c0b9df18ddda9b698b3`  
		Last Modified: Tue, 09 Jun 2020 02:11:20 GMT  
		Size: 9.3 MB (9343524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba732bafeb6b1467fd6908c64c6e8d10ffb27e44e3a25ab4c6c38e8f753baa5`  
		Last Modified: Tue, 09 Jun 2020 02:11:43 GMT  
		Size: 47.4 MB (47356467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10fbc5ac1d2a89d2b9d45778fc9215409db3c14b82290c3f4bb4afff39a8687f`  
		Last Modified: Tue, 09 Jun 2020 18:39:55 GMT  
		Size: 53.1 MB (53110939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733f2f4b4bbbebac432518fe9d21921652262258451b8d68403ef271884aa80b`  
		Last Modified: Fri, 17 Jul 2020 06:26:18 GMT  
		Size: 101.8 MB (101814736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c8a256d45c5eb99bfc32e46a123b639bf501e62a3dd489e41fe8f4e102a63d`  
		Last Modified: Fri, 17 Jul 2020 06:25:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f1771b648d25e905aaa5cbdce877583f256701bbc54c7ddfb24c312d5e1e444d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282572164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936378aa50bb22f8b92d84fe58a0b1747d0cf90679136b29124a0af4e4aff657`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:51:33 GMT
ADD file:73f1cc6ac15b24788e78ae41cd6c89cb5211d64baf491accbd95b6fe9718f17f in / 
# Tue, 09 Jun 2020 01:51:36 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:31:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:32:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:32:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 21:55:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Jun 2020 21:06:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:47:26 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:51:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 17 Jul 2020 02:51:27 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:51:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:52:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:53:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1db90d3d3b6598d485690f804e96153fb632e7434251d334e9a0c49b773855c9`  
		Last Modified: Tue, 09 Jun 2020 01:57:52 GMT  
		Size: 49.2 MB (49167914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e848fd373270c8ed6d276649dd8a5860d188f7d0ff306e91e4e3e092e541d99`  
		Last Modified: Tue, 09 Jun 2020 02:47:16 GMT  
		Size: 7.7 MB (7681351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c85f14a5d8064020366c03aa05ec1c8b0f731e0966bb9788960d27258634aef`  
		Last Modified: Tue, 09 Jun 2020 02:47:16 GMT  
		Size: 10.0 MB (9983910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334e38f2d6fff7c08f4ad1b38ec441d2cf963b761b5d85983396a75ff6d0c08f`  
		Last Modified: Tue, 09 Jun 2020 02:47:41 GMT  
		Size: 52.2 MB (52156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f849c8ccad7f367e6e10b4b4606706efb0ae2a5122783b9cb982de2df9423579`  
		Last Modified: Tue, 09 Jun 2020 22:00:39 GMT  
		Size: 62.5 MB (62515043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04be2e03ae25fc71f1da613c1a2d02a0f7eda25ddd2a8dcfa9f2bfcf02efee2a`  
		Last Modified: Fri, 17 Jul 2020 03:34:18 GMT  
		Size: 101.1 MB (101067533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacca364f6d27020d1b22f84b44737e946cef720ad636cba85e1e7a0edc46956`  
		Last Modified: Fri, 17 Jul 2020 03:33:42 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; 386

```console
$ docker pull golang@sha256:5f2e4d48cf52cda0ef612c1cad3fb0d5da8d4f552c08bc94e8f475f0b8327814
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301295397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191fe7d9ca513721931bb4c3c948259bfedb1a264d5702ac76304ba5da56c9a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:33 GMT
ADD file:f95fda6e1e7823d93ca50dd67a1ab99bdc8a7dea372ef27426915702500d54a2 in / 
# Tue, 09 Jun 2020 01:39:33 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:11:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:11:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:12:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 19:49:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Jun 2020 21:39:53 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:38:36 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:38:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 17 Jul 2020 02:38:55 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:38:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:38:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:38:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ca172633df711443e1bcc46650b24074efa097045feee542ecbb4934ae3ae01b`  
		Last Modified: Tue, 09 Jun 2020 01:44:44 GMT  
		Size: 51.2 MB (51156157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e4e2e742db8627ba5d7e0f076114e90c4fea4407cedd3599355e4c00828543`  
		Last Modified: Tue, 09 Jun 2020 02:32:03 GMT  
		Size: 8.0 MB (7981054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ba43d083b56bb094a5bac45d723e9bec0fe65d033950b3c4dc392e890c7e41`  
		Last Modified: Tue, 09 Jun 2020 02:32:03 GMT  
		Size: 10.3 MB (10338453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2391b0310a0be022e7ac6e202273ea7cc0ac5f16e862e5cb19c43c5db30b5b`  
		Last Modified: Tue, 09 Jun 2020 02:32:24 GMT  
		Size: 53.4 MB (53429728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6418909c851cb25d795df9db25552f37bd19b4f855e3f4390ac56df413186b7`  
		Last Modified: Tue, 09 Jun 2020 19:53:02 GMT  
		Size: 73.5 MB (73511520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0b25ad884775b14abde0de744f44fc734ae96cc3e5ef0f57af89dcf6e546d2`  
		Last Modified: Fri, 17 Jul 2020 02:53:05 GMT  
		Size: 104.9 MB (104878360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4732d9995a6ecebb957ff15df8bf59c751789b05e719a1de3be6d40a3769032d`  
		Last Modified: Fri, 17 Jul 2020 02:52:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; mips64le

```console
$ docker pull golang@sha256:4e4e3a1f782199d54f19a95bef534e92821622bcc0d8d8505bc4bc9afacc2e65
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272660429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e78cb75e1fefc7db4f009398304338d4647dab752ec059782a7c3000d186ecb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:09:26 GMT
ADD file:977c467052f70f2e12137d029c9b03878551b1d47fabd10269bb0eefa21dfcf8 in / 
# Wed, 22 Jul 2020 01:09:27 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 10:34:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:34:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 10:35:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 15:07:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 15:07:04 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 15:14:43 GMT
ENV GOLANG_VERSION=1.14.6
# Wed, 22 Jul 2020 15:22:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 22 Jul 2020 15:22:22 GMT
ENV GOPATH=/go
# Wed, 22 Jul 2020 15:22:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 15:22:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 22 Jul 2020 15:22:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c04e94f82f3062ec5b60ae7bab01bf211a4a344fd83f7a014cfce0dea431fe8`  
		Last Modified: Wed, 22 Jul 2020 01:16:02 GMT  
		Size: 49.0 MB (49019482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052a483e51a26250616636fb64798fc3d2dae1d604bc2d2600938715ebcae62d`  
		Last Modified: Wed, 22 Jul 2020 10:47:02 GMT  
		Size: 7.2 MB (7231450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b65fc0bfc54a9bae7903f08c85b8a726be9b67a28d1b595ebda596154742797`  
		Last Modified: Wed, 22 Jul 2020 10:47:03 GMT  
		Size: 10.0 MB (10015795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a021a129008c5cd9aca6c98d0298edbbf4a92493ac5235e8db1796637485a18`  
		Last Modified: Wed, 22 Jul 2020 10:47:57 GMT  
		Size: 50.8 MB (50838886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaee7ecd2bbe2c9b43a55110c511a44bbe3655df010bc4cc5c69a1bf125946b9`  
		Last Modified: Wed, 22 Jul 2020 15:31:07 GMT  
		Size: 54.6 MB (54562006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5656445930271a883766d47425d1334408f16f2193e7f6c2909a82c6dd511e0`  
		Last Modified: Wed, 22 Jul 2020 15:32:56 GMT  
		Size: 101.0 MB (100992684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a7d5842c64f8947559efd8b40ba81ef539e3dd55c990b520174ee31b339769`  
		Last Modified: Wed, 22 Jul 2020 15:31:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:c59b39932bb1a514c82c2c8689e25278856f7d13f8a7bbefee19b53dbe63ce37
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304063288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4e02bb549803c448eeccb32ddc283039260f39dc9eb136972f1b4b8abdac4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:01 GMT
ADD file:18a41180457a190a9dede1228479d2e332a348f22ac027c36e14d6d92e556f22 in / 
# Tue, 09 Jun 2020 01:22:06 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:57:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:58:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 03:00:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 23:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Jun 2020 21:57:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:18:30 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:19:15 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 17 Jul 2020 02:19:26 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:19:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:19:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:19:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0cad52b1770a1b4a84068be3efe78098837be582f5905e627b2cdba07e641fd1`  
		Last Modified: Tue, 09 Jun 2020 01:30:12 GMT  
		Size: 54.1 MB (54143376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0318f8e4196d9f742fcca63ed04f9c2cb14ac6541f33cd67dae342ef35845da`  
		Last Modified: Tue, 09 Jun 2020 03:43:38 GMT  
		Size: 8.3 MB (8254819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec302fe954105553bdc7cac9100b6bfd114d3b56ef94d850b0364da83650fc6`  
		Last Modified: Tue, 09 Jun 2020 03:43:37 GMT  
		Size: 10.7 MB (10727191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf65a8c1ffe0371d22a42dfd9c0b4ac2900e0ca4d9d12502c488c59d3aff6aee`  
		Last Modified: Tue, 09 Jun 2020 03:44:31 GMT  
		Size: 57.5 MB (57460152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7355b492f1f701da421ddd7977f8f9ee92f9f31598a5645d08dfa1b430004aa7`  
		Last Modified: Tue, 09 Jun 2020 23:26:09 GMT  
		Size: 73.6 MB (73554069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d4f5e6c9322a1634d6f5beeed416e350e2bc0f5fd587e332d79fbdbbae8ad7`  
		Last Modified: Fri, 17 Jul 2020 02:40:33 GMT  
		Size: 99.9 MB (99923525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445d38f9bb48e84bce795e40c7d3354d4e4b91546884ab176a39be6f88c2523c`  
		Last Modified: Fri, 17 Jul 2020 02:37:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; s390x

```console
$ docker pull golang@sha256:b0bfd46021ae709a14ca005dcfddc8919d37f34b0362b8679ea06769fd5f8a74
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279700659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2fc49784ef69eef61bd3ff176fe37c89cb0faf65e3cc0e16fa337b87f069a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:24 GMT
ADD file:e5fcdcbbd996899922beac57e202b7e0895321e07263147e96c6e3b7b811d8a2 in / 
# Wed, 22 Jul 2020 00:42:26 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:06:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:06:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:07:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 06:01:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 06:01:50 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 06:02:21 GMT
ENV GOLANG_VERSION=1.14.6
# Wed, 22 Jul 2020 06:02:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 22 Jul 2020 06:02:38 GMT
ENV GOPATH=/go
# Wed, 22 Jul 2020 06:02:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 06:02:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 22 Jul 2020 06:02:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ecdd8436fd4d951f4ca002a2aa8b01d427a7c4b535083e3ef0792444053154d`  
		Last Modified: Wed, 22 Jul 2020 00:45:30 GMT  
		Size: 49.0 MB (48966422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e8e5cabcd07c3b92963e637fc22608613c8a9013bf41d621452d8827c71214`  
		Last Modified: Wed, 22 Jul 2020 01:12:20 GMT  
		Size: 7.4 MB (7385174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a68e3c7fb279126bd2a86ecae67a5c1bd01806670cb45ad4367f30176fcdb7`  
		Last Modified: Wed, 22 Jul 2020 01:12:20 GMT  
		Size: 9.9 MB (9882077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0fa137f6994d756f1fea600570b23bd7bf9a0bd77a3fd5369f522e337d0e14`  
		Last Modified: Wed, 22 Jul 2020 01:12:33 GMT  
		Size: 51.4 MB (51369332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e525026a356ed8ac8f61b36fa3ea38163eda2b31e20d468e6ef3539d04e5248`  
		Last Modified: Wed, 22 Jul 2020 06:04:00 GMT  
		Size: 56.7 MB (56716385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0373920b310f92672967a2279f95d3b61185bdc56e08afa0c56ec254034147e1`  
		Last Modified: Wed, 22 Jul 2020 06:04:29 GMT  
		Size: 105.4 MB (105381114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e217ae97ce3126dd259339c9aadfede933f99e851cc4dfa6539187354944e03`  
		Last Modified: Wed, 22 Jul 2020 06:04:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
