## `golang:buster`

```console
$ docker pull golang@sha256:4931435cf13ab0c4e55853ecfc6c78a86580e7c2e506307c75ae73c0f669f506
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

### `golang:buster` - linux; amd64

```console
$ docker pull golang@sha256:f254180c5defa2653955e963fb0626e3d4fbbb162f7cff6490e94607d1d867ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317782524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15d23d9676357ce6d4079f4b20f6759bd5412d4be63cc15a1cc24023b21e42a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 04:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 03:46:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 03:46:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:19:58 GMT
ENV GOLANG_VERSION=1.16
# Thu, 25 Feb 2021 04:37:16 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.linux-amd64.tar.gz'; 			sha256='013a489ebb3e24ef3d915abe5b94c3286c070dfe0818d5bca8108f1d6e8440d2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.linux-armv6l.tar.gz'; 			sha256='d1d9404b1dbd77afa2bdc70934e10fbfcf7d785c372efc29462bb7d83d0a32fd'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.linux-arm64.tar.gz'; 			sha256='3770f7eb22d05e25fbee8fb53c2a4e897da043eb83c69b9a14f8d98562cd8098'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.linux-386.tar.gz'; 			sha256='ea435a1ac6d497b03e367fdfb74b33e961d813883468080f6e239b3b03bea6aa'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.linux-ppc64le.tar.gz'; 			sha256='27a1aaa988e930b7932ce459c8a63ad5b3333b3a06b016d87ff289f2a11aacd6'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.linux-s390x.tar.gz'; 			sha256='be4c9e4e2cf058efc4e3eb013a760cb989ddc4362f111950c990d1c63b27ccbe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 		sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 25 Feb 2021 04:37:16 GMT
ENV GOPATH=/go
# Thu, 25 Feb 2021 04:37:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Feb 2021 04:37:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 25 Feb 2021 04:37:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15a0f46f8c38f4ca7daecf160ba9cdb3ddeafda769e2741e179851cfaa14eec`  
		Last Modified: Tue, 09 Feb 2021 04:46:23 GMT  
		Size: 51.8 MB (51830963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1517911a35d7939f446084c1d4c31afc552678e81b3450c2af998b57f72099c2`  
		Last Modified: Wed, 10 Feb 2021 03:48:48 GMT  
		Size: 68.7 MB (68719564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70484a0ec3336f45d3dcff175ef6bc6aac33c5a7217286f0353e05bc74d45033`  
		Last Modified: Thu, 25 Feb 2021 04:48:48 GMT  
		Size: 129.0 MB (129004532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0e01d83af93370572cdf00634074c258618a229eea29db643fd06ddf9848a3`  
		Last Modified: Thu, 25 Feb 2021 04:48:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:9ee9c3f5ff86de9666e07717d0bd0628a387d0158989159b4cadf48dd713279d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269255445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5c38072c5a445e8d2f3b755a95e339dc134c1e71ea2ea8215d77e182bcbd43`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:49:48 GMT
ADD file:0d42654e4fb3d6743aca1ff6ed0c1438b6af430c0e32f32a645a069650192ba8 in / 
# Tue, 09 Feb 2021 02:49:50 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:25:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 03:26:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 14:49:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 14:49:38 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:48:44 GMT
ENV GOLANG_VERSION=1.16
# Thu, 25 Feb 2021 01:54:24 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.linux-amd64.tar.gz'; 			sha256='013a489ebb3e24ef3d915abe5b94c3286c070dfe0818d5bca8108f1d6e8440d2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.linux-armv6l.tar.gz'; 			sha256='d1d9404b1dbd77afa2bdc70934e10fbfcf7d785c372efc29462bb7d83d0a32fd'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.linux-arm64.tar.gz'; 			sha256='3770f7eb22d05e25fbee8fb53c2a4e897da043eb83c69b9a14f8d98562cd8098'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.linux-386.tar.gz'; 			sha256='ea435a1ac6d497b03e367fdfb74b33e961d813883468080f6e239b3b03bea6aa'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.linux-ppc64le.tar.gz'; 			sha256='27a1aaa988e930b7932ce459c8a63ad5b3333b3a06b016d87ff289f2a11aacd6'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.linux-s390x.tar.gz'; 			sha256='be4c9e4e2cf058efc4e3eb013a760cb989ddc4362f111950c990d1c63b27ccbe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 		sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 25 Feb 2021 01:54:27 GMT
ENV GOPATH=/go
# Thu, 25 Feb 2021 01:54:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Feb 2021 01:54:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 25 Feb 2021 01:54:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caefd74d211732bd2d8529a8957297fee583b1eed876add26edaae597ec7eeb3`  
		Last Modified: Tue, 09 Feb 2021 02:58:42 GMT  
		Size: 48.1 MB (48111499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a124d5143cc689eb683e6266a65032891dfe62eeb6cb6b509b97db15c76b32c`  
		Last Modified: Tue, 09 Feb 2021 03:40:13 GMT  
		Size: 7.4 MB (7376268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa139a8bae24b22edced2ecd5c232ad41726a2d3c7735379b893172896d68f7`  
		Last Modified: Tue, 09 Feb 2021 03:40:14 GMT  
		Size: 9.7 MB (9687544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acd73801003dec84d303d6956df994b26ab304d99a457d6b1bd1c70427b5852`  
		Last Modified: Tue, 09 Feb 2021 03:40:39 GMT  
		Size: 49.6 MB (49571258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef551db9da6fd97cf1130c6031667e1e3f5b5b1b7976b8cdc760f339f00acbd9`  
		Last Modified: Tue, 09 Feb 2021 15:00:33 GMT  
		Size: 52.0 MB (52026902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1fa07a6796c4cd490b8ec97e822d45705356cb4d02e431b65d5980b987f5bd`  
		Last Modified: Thu, 25 Feb 2021 02:00:04 GMT  
		Size: 102.5 MB (102481818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54eb465198338957db9da547c73af3df810edb2dd56570e5964401057134646`  
		Last Modified: Thu, 25 Feb 2021 01:59:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:10f7c75218a877534098e16f44e2fadf5b0a9101859c7caa57c0a65ebc8945bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263118663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c22f23952cc53d1b719700ea91958d3fd5ba2bccc7881738d629f43093981ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:29 GMT
ADD file:817a4ff41fcac0be44e95d3f0a51c9fa878d16dac7cdab68bfc445f630c43c22 in / 
# Tue, 09 Feb 2021 03:00:33 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:26:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 04:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 19:41:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 19:41:19 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:58:55 GMT
ENV GOLANG_VERSION=1.16
# Thu, 25 Feb 2021 03:31:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.linux-amd64.tar.gz'; 			sha256='013a489ebb3e24ef3d915abe5b94c3286c070dfe0818d5bca8108f1d6e8440d2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.linux-armv6l.tar.gz'; 			sha256='d1d9404b1dbd77afa2bdc70934e10fbfcf7d785c372efc29462bb7d83d0a32fd'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.linux-arm64.tar.gz'; 			sha256='3770f7eb22d05e25fbee8fb53c2a4e897da043eb83c69b9a14f8d98562cd8098'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.linux-386.tar.gz'; 			sha256='ea435a1ac6d497b03e367fdfb74b33e961d813883468080f6e239b3b03bea6aa'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.linux-ppc64le.tar.gz'; 			sha256='27a1aaa988e930b7932ce459c8a63ad5b3333b3a06b016d87ff289f2a11aacd6'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.linux-s390x.tar.gz'; 			sha256='be4c9e4e2cf058efc4e3eb013a760cb989ddc4362f111950c990d1c63b27ccbe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 		sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 25 Feb 2021 03:31:33 GMT
ENV GOPATH=/go
# Thu, 25 Feb 2021 03:31:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Feb 2021 03:31:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 25 Feb 2021 03:31:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4c2a0a79594a20b9c2f0bfbd535f875ca1b079625052cdd801afb1cc0362d6d0`  
		Last Modified: Tue, 09 Feb 2021 03:09:18 GMT  
		Size: 45.9 MB (45867053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c11c595f6421f88e1b10286a766ae8db88f67c2c0f41cedd170640aee498ab`  
		Last Modified: Tue, 09 Feb 2021 04:39:37 GMT  
		Size: 7.1 MB (7123173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cb22b679409f00e04b8d645444df7181f05cb2967ed73f1a377e7f774b6873`  
		Last Modified: Tue, 09 Feb 2021 04:39:37 GMT  
		Size: 9.3 MB (9343495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e90d4e143c069feee70f90eea83d55b7b0761c67fbbfb7f3734c16c0811ac13`  
		Last Modified: Tue, 09 Feb 2021 04:40:02 GMT  
		Size: 47.4 MB (47355624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589feef49f1bc31f79ce239cc8c07cba582e35acd49a69908014769a9e87fd72`  
		Last Modified: Tue, 09 Feb 2021 19:46:01 GMT  
		Size: 53.2 MB (53192766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dd3693baf76993fa541570965c7af34f1fd846807732437914d840b1961879`  
		Last Modified: Thu, 25 Feb 2021 03:43:57 GMT  
		Size: 100.2 MB (100236396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6dc6cbae769d357c5f3bb3c84b1c53a8a35a0964affa8be0b33da18ff85d8`  
		Last Modified: Thu, 25 Feb 2021 03:43:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:dab4ff7fa29fa2f1b5f2cf6806aea8ddc3965aabecc477eaefe9c24c0e68cfdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281170850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc9032c694f10c1b589ce22cc948f6e4834ea4f4cfdce691715497c329d2693`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:40:45 GMT
ADD file:78412ee35e3dc6fb5fdfce41eb05dd273ba1d49328ab327465639bfa4821aa51 in / 
# Tue, 09 Feb 2021 02:40:50 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:43:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:43:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 04:44:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 21:49:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 21:49:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:40:29 GMT
ENV GOLANG_VERSION=1.16
# Thu, 25 Feb 2021 04:51:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.linux-amd64.tar.gz'; 			sha256='013a489ebb3e24ef3d915abe5b94c3286c070dfe0818d5bca8108f1d6e8440d2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.linux-armv6l.tar.gz'; 			sha256='d1d9404b1dbd77afa2bdc70934e10fbfcf7d785c372efc29462bb7d83d0a32fd'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.linux-arm64.tar.gz'; 			sha256='3770f7eb22d05e25fbee8fb53c2a4e897da043eb83c69b9a14f8d98562cd8098'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.linux-386.tar.gz'; 			sha256='ea435a1ac6d497b03e367fdfb74b33e961d813883468080f6e239b3b03bea6aa'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.linux-ppc64le.tar.gz'; 			sha256='27a1aaa988e930b7932ce459c8a63ad5b3333b3a06b016d87ff289f2a11aacd6'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.linux-s390x.tar.gz'; 			sha256='be4c9e4e2cf058efc4e3eb013a760cb989ddc4362f111950c990d1c63b27ccbe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 		sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 25 Feb 2021 04:51:33 GMT
ENV GOPATH=/go
# Thu, 25 Feb 2021 04:51:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Feb 2021 04:51:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 25 Feb 2021 04:51:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c78c297fb0d010ee085f95ae439636ecb167b050c1acb4273bd576998cf94a83`  
		Last Modified: Tue, 09 Feb 2021 02:47:03 GMT  
		Size: 49.2 MB (49183229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06af62193c25241eb123af8cf115c7a6298e834976fe148ac79ec11a7ca06ee5`  
		Last Modified: Tue, 09 Feb 2021 04:57:24 GMT  
		Size: 7.7 MB (7694122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b846e1b73901174c506ae5e6219ac2f356ef71eaa5896dfbc238dc67ca4bf73`  
		Last Modified: Tue, 09 Feb 2021 04:57:24 GMT  
		Size: 10.0 MB (9984281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb44d26a138a8d064a4ab8f9b472c64e7136c2482ec5af19bab8811b6d2c15b7`  
		Last Modified: Tue, 09 Feb 2021 04:57:46 GMT  
		Size: 52.2 MB (52165287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d638b6994818c673ce32f9ad2ad7c2bac3b21d54c4f341f941e10d9724b16b4b`  
		Last Modified: Tue, 09 Feb 2021 21:53:57 GMT  
		Size: 62.6 MB (62587497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c670ae34f61eac33ad0fb47eade82337108e248574a8ac8bbaade760492b51a`  
		Last Modified: Thu, 25 Feb 2021 05:02:31 GMT  
		Size: 99.6 MB (99556277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c77379489b2553277acd703248ac1d17f6307d7ea4b6ad7f11a4b6b46641b1`  
		Last Modified: Thu, 25 Feb 2021 05:02:08 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; 386

```console
$ docker pull golang@sha256:41bffbb7bdffc376027e3556f4f6223278d905750f6ed01c0edf85ab198bdef7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299561380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6fd3fef8699e5b7101ed96c9af4b9d54ec6f9652b4a37f58f2e5f5fbed73c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:32 GMT
ADD file:174c1471a32619d54d725ea84d52c784b0093e0fa3327988de11aa4c7a1a74f8 in / 
# Tue, 09 Feb 2021 02:39:32 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:09:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 03:10:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 20:28:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 20:28:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 02:24:38 GMT
ENV GOLANG_VERSION=1.16
# Thu, 25 Feb 2021 03:05:41 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.linux-amd64.tar.gz'; 			sha256='013a489ebb3e24ef3d915abe5b94c3286c070dfe0818d5bca8108f1d6e8440d2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.linux-armv6l.tar.gz'; 			sha256='d1d9404b1dbd77afa2bdc70934e10fbfcf7d785c372efc29462bb7d83d0a32fd'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.linux-arm64.tar.gz'; 			sha256='3770f7eb22d05e25fbee8fb53c2a4e897da043eb83c69b9a14f8d98562cd8098'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.linux-386.tar.gz'; 			sha256='ea435a1ac6d497b03e367fdfb74b33e961d813883468080f6e239b3b03bea6aa'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.linux-ppc64le.tar.gz'; 			sha256='27a1aaa988e930b7932ce459c8a63ad5b3333b3a06b016d87ff289f2a11aacd6'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.linux-s390x.tar.gz'; 			sha256='be4c9e4e2cf058efc4e3eb013a760cb989ddc4362f111950c990d1c63b27ccbe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 		sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 25 Feb 2021 03:05:41 GMT
ENV GOPATH=/go
# Thu, 25 Feb 2021 03:05:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Feb 2021 03:05:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 25 Feb 2021 03:05:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ddc66558221fdd621c8a9a9b10318a2be0e73e6e9b5201713c51d24dc672e99f`  
		Last Modified: Tue, 09 Feb 2021 02:45:29 GMT  
		Size: 51.2 MB (51163172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3367f7dc54e20f15e3eb446308d1d90921807cbbbe026653f1e081e0f3f800d4`  
		Last Modified: Tue, 09 Feb 2021 03:20:37 GMT  
		Size: 8.0 MB (7996266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d8d6b6155811224781274d8019eebe0788d1437193d1cc61be4e579108dd74`  
		Last Modified: Tue, 09 Feb 2021 03:20:37 GMT  
		Size: 10.3 MB (10338853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d650a4bdf99a8c28d0ec7f0b518cd93231802ba93726fa384a15c5ea536a87b`  
		Last Modified: Tue, 09 Feb 2021 03:21:05 GMT  
		Size: 53.4 MB (53433487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44bd7f8b94de57e6e725009e64b33628356f58b53e3a5b4888f526b1eb3e5b0`  
		Last Modified: Tue, 09 Feb 2021 20:34:29 GMT  
		Size: 73.6 MB (73588394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a3620e71cf4c7d245c6eab758265c2ec0a445993483dd943690059eed38f`  
		Last Modified: Thu, 25 Feb 2021 03:28:42 GMT  
		Size: 103.0 MB (103041082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551344185de6baffdda6db8144f1502250f122013816a0f3846f30123cdb041a`  
		Last Modified: Thu, 25 Feb 2021 03:28:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; mips64le

```console
$ docker pull golang@sha256:96a7c643d02121402552b372dd7ce142f658bffdef0af3f18039822fa324cdde
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271312774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1431fbad79515f6e0e743ac0e81e168a20d0ed2eeacf2cb02997675064b3b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:04 GMT
ADD file:490a48a20d3dd7f37fb99df67136dba1fd328a9916a73fbc13da9be27e7fd95d in / 
# Tue, 09 Feb 2021 03:09:04 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:05:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 04:06:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:56:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:56:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 02:07:22 GMT
ENV GOLANG_VERSION=1.16
# Thu, 25 Feb 2021 02:15:15 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.linux-amd64.tar.gz'; 			sha256='013a489ebb3e24ef3d915abe5b94c3286c070dfe0818d5bca8108f1d6e8440d2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.linux-armv6l.tar.gz'; 			sha256='d1d9404b1dbd77afa2bdc70934e10fbfcf7d785c372efc29462bb7d83d0a32fd'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.linux-arm64.tar.gz'; 			sha256='3770f7eb22d05e25fbee8fb53c2a4e897da043eb83c69b9a14f8d98562cd8098'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.linux-386.tar.gz'; 			sha256='ea435a1ac6d497b03e367fdfb74b33e961d813883468080f6e239b3b03bea6aa'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.linux-ppc64le.tar.gz'; 			sha256='27a1aaa988e930b7932ce459c8a63ad5b3333b3a06b016d87ff289f2a11aacd6'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.linux-s390x.tar.gz'; 			sha256='be4c9e4e2cf058efc4e3eb013a760cb989ddc4362f111950c990d1c63b27ccbe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 		sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 25 Feb 2021 02:15:17 GMT
ENV GOPATH=/go
# Thu, 25 Feb 2021 02:15:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Feb 2021 02:15:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 25 Feb 2021 02:15:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c66db2c7cd9b921e61702131302689efe48861f2def6b11e1d3ebe56fc06fdad`  
		Last Modified: Tue, 09 Feb 2021 03:15:07 GMT  
		Size: 49.0 MB (49027959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4558012499a65e8af9c0d92bfddea26b0adc56b688f78ce2c33bb72ff0e24b3`  
		Last Modified: Tue, 09 Feb 2021 04:16:37 GMT  
		Size: 7.3 MB (7250591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c64a7693227b692aae0c22e05c8c9b808f4d4ddf20575237a1fec0a0c8fba8d`  
		Last Modified: Tue, 09 Feb 2021 04:16:38 GMT  
		Size: 10.0 MB (10016352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9f01a8e276f4df19d07d9706dc3b0dec6edc61799fcc5f3270e0514fe6c29c`  
		Last Modified: Tue, 09 Feb 2021 04:17:30 GMT  
		Size: 50.8 MB (50843339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74dbde2c64c2527997f0460a51a73a2475d8700be665ff0eed172364ab570d9`  
		Last Modified: Tue, 09 Feb 2021 18:21:00 GMT  
		Size: 54.6 MB (54634805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be61ba72880c39f4d5faa3395cfb6bfe9e668c1430092f76a09d1e248c494d9`  
		Last Modified: Thu, 25 Feb 2021 02:24:42 GMT  
		Size: 99.5 MB (99539602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642f48d146ebbfe39a333b7c13879262a08c46bd306f837209ff5f4bb13d2090`  
		Last Modified: Thu, 25 Feb 2021 02:23:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; ppc64le

```console
$ docker pull golang@sha256:5ea2c8bad06385b26ccff7f7bd927a7d23071f3c8479dd7b441ed7ba37de9f0a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302263118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ccd0969379e517864b9fb325179be7e2536b1e9f3ded27e04d7438d3a8ffa6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:18:34 GMT
ADD file:0fc1572a1f7f423ae98036bea9f9d1f9237ea74bf582a925ecf956383f7dc8e1 in / 
# Tue, 09 Feb 2021 02:18:46 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:02:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 05:03:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 05:07:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 00:06:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Feb 2021 00:06:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:16:54 GMT
ENV GOLANG_VERSION=1.16
# Thu, 25 Feb 2021 04:41:30 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.linux-amd64.tar.gz'; 			sha256='013a489ebb3e24ef3d915abe5b94c3286c070dfe0818d5bca8108f1d6e8440d2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.linux-armv6l.tar.gz'; 			sha256='d1d9404b1dbd77afa2bdc70934e10fbfcf7d785c372efc29462bb7d83d0a32fd'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.linux-arm64.tar.gz'; 			sha256='3770f7eb22d05e25fbee8fb53c2a4e897da043eb83c69b9a14f8d98562cd8098'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.linux-386.tar.gz'; 			sha256='ea435a1ac6d497b03e367fdfb74b33e961d813883468080f6e239b3b03bea6aa'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.linux-ppc64le.tar.gz'; 			sha256='27a1aaa988e930b7932ce459c8a63ad5b3333b3a06b016d87ff289f2a11aacd6'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.linux-s390x.tar.gz'; 			sha256='be4c9e4e2cf058efc4e3eb013a760cb989ddc4362f111950c990d1c63b27ccbe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 		sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 25 Feb 2021 04:41:43 GMT
ENV GOPATH=/go
# Thu, 25 Feb 2021 04:41:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Feb 2021 04:42:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 25 Feb 2021 04:42:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9311932ee2fcc8fed8d2911fda20f73ee92ea26879166cf6cc3192522e83fd0a`  
		Last Modified: Tue, 09 Feb 2021 02:27:25 GMT  
		Size: 54.1 MB (54135809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881ebf746bce396a8b31a683ca6cbcb81f5c9aa7bb2c9e236996aa2c7b5610d5`  
		Last Modified: Tue, 09 Feb 2021 05:48:15 GMT  
		Size: 8.3 MB (8271305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27336f6700d8773d71eb0faf6090217770cffe60d1132c3d46f5375639b8a2e9`  
		Last Modified: Tue, 09 Feb 2021 05:48:16 GMT  
		Size: 10.7 MB (10727781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afedf8a01deada06218528a166adc4366030e683f7c3442f16812ece04158aa`  
		Last Modified: Tue, 09 Feb 2021 05:48:41 GMT  
		Size: 57.5 MB (57455475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f7802c81cec4fa46a988d0de9c3581687f89ccc21b786c7326ec053c55ea67`  
		Last Modified: Wed, 10 Feb 2021 00:13:38 GMT  
		Size: 73.6 MB (73624210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bbb8e9b5b4fbdafabb6cf7eba09e22677ff30b8e923c73ff5b8dbb077495c9`  
		Last Modified: Thu, 25 Feb 2021 04:57:20 GMT  
		Size: 98.0 MB (98048382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4516e4097cf0578f304f1d44c843635968df10429ff05b96c6cc32b197b7ede1`  
		Last Modified: Thu, 25 Feb 2021 04:55:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; s390x

```console
$ docker pull golang@sha256:d1ea51c7f51153a69c98fa2d0c7dcd2eb89b5be9fc06fc7d63ea15ea86b651e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277614663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21694ef87f7d0d15c2235681cc407b58798f4c07a0ac57330ec0a883c9ac44aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:56 GMT
ADD file:f390b371893461fffed2fb48d65b6c930137539a82b9c5329410cef322a5a9ea in / 
# Tue, 09 Feb 2021 02:41:59 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:05:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:05:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 03:05:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 11:30:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 11:31:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:41:29 GMT
ENV GOLANG_VERSION=1.16
# Wed, 17 Feb 2021 01:41:41 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.16.linux-amd64.tar.gz'; 			sha256='013a489ebb3e24ef3d915abe5b94c3286c070dfe0818d5bca8108f1d6e8440d2'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.16.linux-armv6l.tar.gz'; 			sha256='d1d9404b1dbd77afa2bdc70934e10fbfcf7d785c372efc29462bb7d83d0a32fd'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.16.linux-arm64.tar.gz'; 			sha256='3770f7eb22d05e25fbee8fb53c2a4e897da043eb83c69b9a14f8d98562cd8098'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.16.linux-386.tar.gz'; 			sha256='ea435a1ac6d497b03e367fdfb74b33e961d813883468080f6e239b3b03bea6aa'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.16.linux-ppc64le.tar.gz'; 			sha256='27a1aaa988e930b7932ce459c8a63ad5b3333b3a06b016d87ff289f2a11aacd6'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.16.linux-s390x.tar.gz'; 			sha256='be4c9e4e2cf058efc4e3eb013a760cb989ddc4362f111950c990d1c63b27ccbe'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.16.src.tar.gz'; 			sha256='7688063d55656105898f323d90a79a39c378d86fe89ae192eb3b7fc46347c95a'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 17 Feb 2021 01:41:46 GMT
ENV GOPATH=/go
# Wed, 17 Feb 2021 01:41:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Feb 2021 01:41:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 17 Feb 2021 01:41:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb61e252baf0cdce361b288d8df47eab4b2adb45935d61331700aa9281372c74`  
		Last Modified: Tue, 09 Feb 2021 02:45:12 GMT  
		Size: 49.0 MB (48970386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21893889b63220b2786e70a7182ba39dfc2fffcecd394424c4be2eba9d090798`  
		Last Modified: Tue, 09 Feb 2021 03:11:48 GMT  
		Size: 7.4 MB (7399445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadc5e0216d8dc7f2fc17b19146d9e168fadadf4acf3bfee694853596f8ee659`  
		Last Modified: Tue, 09 Feb 2021 03:11:47 GMT  
		Size: 9.9 MB (9883127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c25bdb77d50c2365abbf0b825665a3320edce80f9ee8ce5985b29effa66c21`  
		Last Modified: Tue, 09 Feb 2021 03:12:03 GMT  
		Size: 51.4 MB (51379480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4817940a6d8d1eee948db363ee62efe08ed91d295c8091add842212a9ac8b`  
		Last Modified: Tue, 09 Feb 2021 11:33:40 GMT  
		Size: 56.8 MB (56788493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f5095f3dd9dd8c1fa63e2ad2517711817d5e29481fb8fb61567a13e4e0d21a`  
		Last Modified: Wed, 17 Feb 2021 01:45:48 GMT  
		Size: 103.2 MB (103193576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a344e9f59a1ce77dc347427697dcdde79de8473df768a007ad872b1b91e88558`  
		Last Modified: Wed, 17 Feb 2021 01:45:35 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
