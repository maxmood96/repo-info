## `golang:bullseye`

```console
$ docker pull golang@sha256:c641419ef5be653b3fe46dc8642ef10db8e974e1cdd2fe96d697c7031c49ab02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `golang:bullseye` - linux; amd64

```console
$ docker pull golang@sha256:3b27ac95762ce1340a4824dc3cab2dc9d63f194f0899a0a9887402c1b1463f41
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346086781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d939cc1fb139e00f0a1540f2b2b405072919bc0be08a1b974783370831606cdc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:30 GMT
ADD file:aea313ae50ce6474a3df142b34d4dcba4e7e0186ea6fe55389cb2ea903b9ebbb in / 
# Tue, 12 Oct 2021 01:20:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:42:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 15:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:14:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:19:37 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:19:56 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 04 Nov 2021 20:19:57 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:19:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:19:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:19:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb7d5a84853b217ac05783963f12b034243070c1c9c8d2e60ada47444f3cce04`  
		Last Modified: Tue, 12 Oct 2021 01:25:37 GMT  
		Size: 54.9 MB (54917520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b617c6a8c415a175f44d7e2c5d3b521059f2a6112c5f022e005a44a759f2d`  
		Last Modified: Tue, 12 Oct 2021 15:52:48 GMT  
		Size: 5.2 MB (5153273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32e17419b7ee61bbd89c2f0d2833a99cf45e594257d15cb567e4cf7771ce34a`  
		Last Modified: Tue, 12 Oct 2021 15:52:48 GMT  
		Size: 10.9 MB (10871935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d2d81226a43a97871acd5afb7e8aabfad4d6b62ae1709c870df3ee230bc3f5`  
		Last Modified: Tue, 12 Oct 2021 15:53:13 GMT  
		Size: 54.6 MB (54567761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd370e02e50430c538ca78431003aa3aeca86bf892c9f75aa7013ac0ad42f49`  
		Last Modified: Wed, 13 Oct 2021 06:19:25 GMT  
		Size: 85.8 MB (85771431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd7280c3f585fe2ee59884cfb82b71708ee17ca4c89b6e0719acae41f036c7`  
		Last Modified: Thu, 04 Nov 2021 20:31:23 GMT  
		Size: 134.8 MB (134804705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776d069e7b0456f78adf6d04ca84e3d93d107111afcff84776df32f53787f869`  
		Last Modified: Thu, 04 Nov 2021 20:31:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; arm variant v5

```console
$ docker pull golang@sha256:2f83d69bbc6026bb9576a89fb6c0abcffa7548b9dd57206004bb3837e0614a37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294518508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3512306de5dcb81b741e2b9175f1b789c27db4b399bd702ecd95d77aadbef89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:49:54 GMT
ADD file:b9969604315238de271e1769a4b8dd85cdf0d33f9fac387e940d5195ac3030a1 in / 
# Tue, 12 Oct 2021 00:49:55 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 05:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 05:41:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 05:42:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 02:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 02:25:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:48:36 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:52:36 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 04 Nov 2021 20:52:38 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:52:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:52:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:52:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a97c782f2538791984ce12c859cada96e395e3950d4cb7d1238e08acd2eb74ec`  
		Last Modified: Tue, 12 Oct 2021 01:05:12 GMT  
		Size: 52.5 MB (52452198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34dc529b005dbeff70906cd4baf2310c918ae6379fdf53ef632c3cd1203aa38`  
		Last Modified: Tue, 12 Oct 2021 06:01:18 GMT  
		Size: 5.1 MB (5063794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2876b7f933f68a5b4f35f854cc8c651bf3d21476fe2bb0a786e6376f389b44b`  
		Last Modified: Tue, 12 Oct 2021 06:01:20 GMT  
		Size: 10.6 MB (10571017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c918a5faa65bffd689b9869a942e77a3fbc7d89566be880da188d6050f4f627`  
		Last Modified: Tue, 12 Oct 2021 06:02:11 GMT  
		Size: 52.3 MB (52322898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0d202c31f9db17d1287966694df2b0c2785373394439ac9e552a1600deae5a`  
		Last Modified: Wed, 13 Oct 2021 02:48:02 GMT  
		Size: 68.7 MB (68705247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b997fed422540b2666bbdb93ba199161669f21f53da09e62b1b6c270f0897222`  
		Last Modified: Thu, 04 Nov 2021 21:06:41 GMT  
		Size: 105.4 MB (105403199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e06045dc6779d8dcc5c0f66c0ae0d3a96d510c0eba20fda77664e7cd19df6a`  
		Last Modified: Thu, 04 Nov 2021 21:05:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:cdc4852113d61b3986ee42c581e21b533584b7a07ef6ff027b3f689813717ecf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283399016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4593e0a4b6a29408e1f839161ab4843a24f2bbd99df37829867f80a23993519`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:27:59 GMT
ADD file:d9f40ca54fb79741d1e76c7bca9250f78453d0b39fb6c921337f3071a79a55a9 in / 
# Tue, 12 Oct 2021 01:28:00 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:35:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 18:36:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 00:31:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 00:31:36 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:57:59 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:58:29 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 04 Nov 2021 20:58:32 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:58:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:58:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:58:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:88ce59c3081c4041f41eb407032db40c207cc2d806ba0eb12e170b697db91e52`  
		Last Modified: Tue, 12 Oct 2021 01:43:42 GMT  
		Size: 50.1 MB (50118673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d212c40843ca0a1c4c7b2cd635c4801f93ea3c3470b17d99c403c0e065a8711`  
		Last Modified: Tue, 12 Oct 2021 18:57:54 GMT  
		Size: 4.9 MB (4922722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdffc4d771520b3975a2a5a85d9d8594ae6d055776a553760db80a5f8e7a279`  
		Last Modified: Tue, 12 Oct 2021 18:57:56 GMT  
		Size: 10.2 MB (10216977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ea64c0b77d8c40a4101ce92be9b38e5c45e0efe6b4e9c6712d624ba7438be`  
		Last Modified: Tue, 12 Oct 2021 18:58:42 GMT  
		Size: 50.3 MB (50327625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9ffa78769c2fa52c776a0672a4b8b747baea79cb3d08fd3c9671f8b01ed33c`  
		Last Modified: Thu, 14 Oct 2021 00:41:41 GMT  
		Size: 64.7 MB (64727801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee468a201999a9c098d3d07d77d08b4cd37ea2ddbd232863d27015b92df36a27`  
		Last Modified: Thu, 04 Nov 2021 21:20:03 GMT  
		Size: 103.1 MB (103085062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878d61ffbf5b524c7e89628ca7a0980ffdc06da1dccdf5336a218d98ddd34a6f`  
		Last Modified: Thu, 04 Nov 2021 21:18:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:188890221179ae813175fef21829b84a005878c78ff92a507d260fbcbdfe6208
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307682426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075a07855af2d20a814bdf24c69dd07b1bc730b9c6e3f6cbe40198dbf131acda`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:04 GMT
ADD file:1529ae12e334fd992892d3fb97c103297cff7e0115b0475bec4c093939a2bff7 in / 
# Tue, 12 Oct 2021 01:41:04 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:58:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 Oct 2021 02:58:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 09:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 09:06:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:43:31 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:43:48 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 04 Nov 2021 20:43:49 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:43:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:43:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:43:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1c47a423366578e5ce665d03788914bf0459485a627a27896fa9c5663ce55cdf`  
		Last Modified: Tue, 12 Oct 2021 01:47:41 GMT  
		Size: 53.6 MB (53603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889b1f128be8ebd64f787c46418ffe34ce1096d1ccd6938924d7397713720758`  
		Last Modified: Sat, 16 Oct 2021 03:14:21 GMT  
		Size: 5.1 MB (5141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c338d42ad921985fb8ebb6e2c48d381f6e03a91535eeffce7f08084b3dfbfdf4`  
		Last Modified: Sat, 16 Oct 2021 03:14:21 GMT  
		Size: 10.7 MB (10655847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27d3d9a061af78e3fcbefe5dbbe718db380687319e5ba8a7c9fd7ba55d16cc3`  
		Last Modified: Sat, 16 Oct 2021 03:14:43 GMT  
		Size: 54.7 MB (54669931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80358db0081cf5ec4ef497601a753594b1210526031a5c7710032157913cff04`  
		Last Modified: Sat, 16 Oct 2021 09:11:27 GMT  
		Size: 81.0 MB (80986873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72d0a336dc8c16cec62eaead12a46921ca485b7ad3734768e9146f1dc43c248`  
		Last Modified: Thu, 04 Nov 2021 20:53:43 GMT  
		Size: 102.6 MB (102624773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc67d6f857fef62ac6aa770f3466d4364cc2e728c9582ff34a26136b10930f97`  
		Last Modified: Thu, 04 Nov 2021 20:53:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:d8665fa9025fc943c843330cf33d39de71d127e39f9c5abc0beb2ffcf0e14bd0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321209594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b158b24d813eb05a7d3b5527a89328b3305bc653ad88d4ec76eb97eaca0278a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:39:30 GMT
ADD file:e007d6eff02dbc696e1166db315b97a77ae8aa65f2e66ca8074765dde9c70a59 in / 
# Tue, 12 Oct 2021 01:39:31 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:35:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:36:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 04:36:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 22:34:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 22:34:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 22:34:27 GMT
ENV GOLANG_VERSION=1.17.2
# Tue, 12 Oct 2021 22:34:56 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.2.linux-amd64.tar.gz'; 			sha256='f242a9db6a0ad1846de7b6d94d507915d14062660616a61ef7c808a76e4f1676'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.2.linux-armv6l.tar.gz'; 			sha256='04d16105008230a9763005be05606f7eb1c683a3dbf0fbfed4034b23889cb7f2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.2.linux-arm64.tar.gz'; 			sha256='a5a43c9cdabdb9f371d56951b14290eba8ce2f9b0db48fb5fc657943984fd4fc'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.2.linux-386.tar.gz'; 			sha256='8617f2e40d51076983502894181ae639d1d8101bfbc4d7463a2b442f239f5596'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.2.linux-ppc64le.tar.gz'; 			sha256='12e2dc7e0ffeebe77083f267ef6705fec1621cdf2ed6489b3af04a13597ed68d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.2.linux-s390x.tar.gz'; 			sha256='c4b2349a8d11350ca038b8c57f3cc58dc0b31284bcbed4f7fca39aeed28b4a51'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.2.src.tar.gz'; 		sha256='2255eb3e4e824dd7d5fcdc2e7f84534371c186312e546fb1086a34c17752f431'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 12 Oct 2021 22:34:58 GMT
ENV GOPATH=/go
# Tue, 12 Oct 2021 22:34:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 22:35:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 12 Oct 2021 22:35:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6911c8f66691266d86e2cafa67ca005d919f357436fac971c694d37625b5ba90`  
		Last Modified: Tue, 12 Oct 2021 01:47:06 GMT  
		Size: 55.9 MB (55923419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0f31369a20c178b1d5c84f192412ed962068e8932d5821eefb00bc7d1cbc1a`  
		Last Modified: Tue, 12 Oct 2021 04:47:26 GMT  
		Size: 5.3 MB (5283102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97aa3d222d7e8d6e0b06e57e5bd03168c422475942f92d09a487bd98d09bb742`  
		Last Modified: Tue, 12 Oct 2021 04:47:27 GMT  
		Size: 11.3 MB (11250699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae99d06bab5fc31ba3db9436a22c452db74a7b5e559a451de2d971a493abe52`  
		Last Modified: Tue, 12 Oct 2021 04:48:03 GMT  
		Size: 55.9 MB (55917451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ce6387c0d8e24fecfb834485f4e01fe761e4fd12131bb2457f15f834b059ac`  
		Last Modified: Tue, 12 Oct 2021 22:41:43 GMT  
		Size: 87.2 MB (87222809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ed34db0f14053427cd98673e1ea2dc47f3e6447c275d85b437ae9f1b10560a`  
		Last Modified: Tue, 12 Oct 2021 22:41:46 GMT  
		Size: 105.6 MB (105611958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e306c3614ddac0da6e1c7b9fb15138fd1ef19f0ba876a65077ae4e41ad4f688`  
		Last Modified: Tue, 12 Oct 2021 22:41:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:de6f810e7921d0ec31ab0b569c721cfc810601d3ebd9090ef7b7116593c052ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291991524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fce00a6050d4fdeead0f8259f0881d62c2e5fc92e249be8532fc63cdee0b81`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:10:49 GMT
ADD file:856952232716a2e2d5069387a06a537937a1dec1bb75bc9519c60d6ad226bddb in / 
# Tue, 12 Oct 2021 01:10:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 01:49:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 01:50:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 09:33:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 09:33:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:10:24 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:20:35 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 04 Nov 2021 20:20:37 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:20:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:20:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:20:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d2cd78b9c44ce4eadbb0cc35b884bfd0dac51123f3c8c6645cb8dc9dc9c1512`  
		Last Modified: Tue, 12 Oct 2021 01:19:18 GMT  
		Size: 53.2 MB (53169836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc92c0f1b1ba16db081439cf0fe0ba300c5acb087b88f97abb47cd8aa1760d6`  
		Last Modified: Tue, 12 Oct 2021 02:04:54 GMT  
		Size: 5.1 MB (5114923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f090a91c9dcffdc8ccb3d0c43f49469a175e0c902bdae900df04c7afe0799f64`  
		Last Modified: Tue, 12 Oct 2021 02:04:56 GMT  
		Size: 10.9 MB (10873345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dca8dc314040adde734540d22d6ece8f751dd2fa78662083691ed36be6a2a8f`  
		Last Modified: Tue, 12 Oct 2021 02:05:49 GMT  
		Size: 53.3 MB (53296535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec238840bc7e9c095c1b03a00718fd1a1712e237dbce38774964c0141fd2a25a`  
		Last Modified: Wed, 13 Oct 2021 10:11:41 GMT  
		Size: 66.9 MB (66896982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7fabae5342647c10c94b5612fd2b663d81746a9a028c53607093c38bd6adf0`  
		Last Modified: Thu, 04 Nov 2021 20:48:43 GMT  
		Size: 102.6 MB (102639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfaac2dfc7582287fb48d2126ed57757fb3825e4e538c21362f4b2dfc27c3b`  
		Last Modified: Thu, 04 Nov 2021 20:47:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:9ce4c9a42762df5935bfbd09fd5b785b442d0ddd11cf9db94ccd4b2019d7aedf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315979137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed75b0ccb06e33170941bf7ee3e8bf5611ab9fb64bdbce264be4074315f413a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:25:04 GMT
ADD file:127b21494e1c790bdbb4c277638b3e16b25fbbcd1e0cdb52e60a4f55a57cd0f2 in / 
# Tue, 12 Oct 2021 01:25:10 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 03:46:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 03:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 03:50:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 12:56:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 12:56:21 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 12:56:24 GMT
ENV GOLANG_VERSION=1.17.2
# Wed, 13 Oct 2021 12:57:03 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.2.linux-amd64.tar.gz'; 			sha256='f242a9db6a0ad1846de7b6d94d507915d14062660616a61ef7c808a76e4f1676'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.2.linux-armv6l.tar.gz'; 			sha256='04d16105008230a9763005be05606f7eb1c683a3dbf0fbfed4034b23889cb7f2'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.2.linux-arm64.tar.gz'; 			sha256='a5a43c9cdabdb9f371d56951b14290eba8ce2f9b0db48fb5fc657943984fd4fc'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.2.linux-386.tar.gz'; 			sha256='8617f2e40d51076983502894181ae639d1d8101bfbc4d7463a2b442f239f5596'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.2.linux-ppc64le.tar.gz'; 			sha256='12e2dc7e0ffeebe77083f267ef6705fec1621cdf2ed6489b3af04a13597ed68d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.2.linux-s390x.tar.gz'; 			sha256='c4b2349a8d11350ca038b8c57f3cc58dc0b31284bcbed4f7fca39aeed28b4a51'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.2.src.tar.gz'; 		sha256='2255eb3e4e824dd7d5fcdc2e7f84534371c186312e546fb1086a34c17752f431'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Oct 2021 12:57:14 GMT
ENV GOPATH=/go
# Wed, 13 Oct 2021 12:57:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 12:57:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Oct 2021 12:57:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c7e7ddcf3b3abfed2b7aab50c1b68bfdfc6fcffed2f4b93ebff4d6050b3d5e72`  
		Last Modified: Tue, 12 Oct 2021 01:36:12 GMT  
		Size: 58.8 MB (58808876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ad477ff0e1489411f419167095ae70f3711a8505b497821289b706b6117c86`  
		Last Modified: Tue, 12 Oct 2021 04:41:09 GMT  
		Size: 5.4 MB (5401977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110cf21b1de9b38b05498de988be3daa0d8ef99e8cb1ff84b5a3d01c61e9d831`  
		Last Modified: Tue, 12 Oct 2021 04:41:11 GMT  
		Size: 11.6 MB (11625975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2384a9fb45c6c30c61d87780024c7b377d81b00dec3596a5222eb6e5687e131e`  
		Last Modified: Tue, 12 Oct 2021 04:41:52 GMT  
		Size: 58.9 MB (58851024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107c8735935d87de1dbb78060add9e217ee2f65868de146ae0b88fce0a7463f4`  
		Last Modified: Wed, 13 Oct 2021 13:05:22 GMT  
		Size: 80.3 MB (80254643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18eace693d1984920c7375692dc0416dbc196df8e5985571a94a22665e1dab4`  
		Last Modified: Wed, 13 Oct 2021 13:05:26 GMT  
		Size: 101.0 MB (101036487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edaf8885c3049ce513e25d702495859243f60f78c93881f8d82c65c81a36fb2`  
		Last Modified: Wed, 13 Oct 2021 13:05:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; s390x

```console
$ docker pull golang@sha256:e6d7101b1e7b84ff3dda7530d38084b55bce590dff79522435de3d23503d3417
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294427231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17aaf1d05374aa42382046814741f2b89a73190af371891600f5b1d7621787b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:09 GMT
ADD file:a7a74f6be757ceb5e84c440e739019782df1a118264eef70aa49886a976c43f6 in / 
# Tue, 12 Oct 2021 00:42:12 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:39:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 07:40:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 07:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:00:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:00:50 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:41:29 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:41:50 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 04 Nov 2021 20:41:56 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:41:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:41:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:41:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:081299fd984cd296112766e1cc55f44fffbf898b2900b01c0333962494a2dd80`  
		Last Modified: Tue, 12 Oct 2021 00:47:43 GMT  
		Size: 53.2 MB (53192895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1178bd9843e3f60ffd4f7a474e885f9965bdc7a92f5831d7250a4cac2c253fa`  
		Last Modified: Tue, 12 Oct 2021 07:48:23 GMT  
		Size: 5.1 MB (5137194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d430256819c7836ccd1840b5eba2bfbd0a31e0767d637abcd72ad92f2b8249`  
		Last Modified: Tue, 12 Oct 2021 07:48:23 GMT  
		Size: 10.8 MB (10761497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4a0391a320de679eaaea8841ae41b0b549a2b83a22e9c766291fa89aa3a7cf`  
		Last Modified: Tue, 12 Oct 2021 07:48:39 GMT  
		Size: 54.0 MB (54041550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab92279b1c3363beb53ae93ffeb95f2d0f92d2b3432d1af93c922a77b70c1361`  
		Last Modified: Tue, 12 Oct 2021 15:04:54 GMT  
		Size: 65.5 MB (65502694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a192055702d0006a28ec234fb65bf2d8c343735b5571d864e07d0e983d631a96`  
		Last Modified: Thu, 04 Nov 2021 20:51:18 GMT  
		Size: 105.8 MB (105791245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbe48a09aacca82668da77c865e3b8b04f16e34c12a1cb9e3792d1142cc853b`  
		Last Modified: Thu, 04 Nov 2021 20:51:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
