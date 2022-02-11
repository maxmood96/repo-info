## `golang:1-stretch`

```console
$ docker pull golang@sha256:9ff43cf673142369460f468969c0a9d45d4d3e17c8080f366045021f8242b60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:1-stretch` - linux; amd64

```console
$ docker pull golang@sha256:dd4fd6ff04b64550a404903b42dc30e5baa49cd4f304faee14ed8e40c10ab7db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303481615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b00ac24788b9fde8b69e086e0e8752e8e4a203d8b91666610d44a1c6d1cc35`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:44 GMT
ADD file:8486e54cd9c7f48cd93b4dc399b71f2053aa61655dcc37e06a9274d4878408a1 in / 
# Wed, 26 Jan 2022 01:42:44 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:16:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:16:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:17:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 10:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 10:07:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Feb 2022 00:23:19 GMT
ENV GOLANG_VERSION=1.17.7
# Fri, 11 Feb 2022 00:24:55 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.7.linux-amd64.tar.gz'; 			sha256='02b111284bedbfa35a7e5b74a06082d18632eff824fd144312f6063943d49259'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.7.linux-armv6l.tar.gz'; 			sha256='874774f078b182fa21ffcb3878467eb5cb7e78bbffa6343ea5f0fbe47983433b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.7.linux-arm64.tar.gz'; 			sha256='a5aa1ed17d45ee1d58b4a4099b12f8942acbd1dd09b2e9a6abb1c4898043c5f5'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.7.linux-386.tar.gz'; 			sha256='5d5472672a2e0252fe31f4ec30583d9f2b320f9b9296eda430f03cbc848400ce'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.7.linux-ppc64le.tar.gz'; 			sha256='2262fdee9147eb61fd1e719cfd19b9c035009c14890de02b5a77071b0a577405'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.7.linux-s390x.tar.gz'; 			sha256='24dd117581d592f52b4cf45d75ae68a6a1e42691a8671a2d3c2ddd739894a1e4'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.7.src.tar.gz'; 		sha256='c108cd33b73b1911a02b697741df3dea43e01a5c4e08e409e8b3a0e3745d2b4d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 11 Feb 2022 00:24:56 GMT
ENV GOPATH=/go
# Fri, 11 Feb 2022 00:24:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Feb 2022 00:24:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 11 Feb 2022 00:24:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a834d7c95167a3e129adb00a5ddbaf5d3c035ad748ff7ee1273373d150457820`  
		Last Modified: Wed, 26 Jan 2022 01:50:37 GMT  
		Size: 45.4 MB (45381397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b3fa6f1b88b95ac6adeafdb618011e672d4c9f5637b92be373276ee7e066dd`  
		Last Modified: Wed, 26 Jan 2022 02:26:13 GMT  
		Size: 11.3 MB (11301881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778df3ecaa0fbba90d3a7d88947a4376ebdc7e2fcf8a4b5ce43b3c699faadff6`  
		Last Modified: Wed, 26 Jan 2022 02:26:12 GMT  
		Size: 4.3 MB (4342406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d353c340774e155d838e2e0f0952201366cee28591b065b7d328fde7bc72e034`  
		Last Modified: Wed, 26 Jan 2022 02:26:33 GMT  
		Size: 49.8 MB (49762420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b15e1d90c2715053b7b3cc20a6a792c2c98aac8d52e85a32959bd6422e5073`  
		Last Modified: Thu, 27 Jan 2022 10:18:40 GMT  
		Size: 57.9 MB (57863228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47777a5ef00eee15517dda1b957528b6256efef45548373d4d4602cbc99e7827`  
		Last Modified: Fri, 11 Feb 2022 00:44:15 GMT  
		Size: 134.8 MB (134830127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972f354d8ea56f475adf3fb7b1326d17fef724cc691ead4974a1a3eec612b1e`  
		Last Modified: Fri, 11 Feb 2022 00:43:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:80f3f172f08bec770deeed7b32294a7c61b0fd500238f337d6edeb0993736355
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251402922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f70176cfd57fe0a11bd0686c027e3c01e551bd7865858fe1840f3a0915658f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:47:34 GMT
ADD file:2d0ec7b989e0ef6e7c2d7cdfa1710507ce32d2218c0769aa5adc804e485973dd in / 
# Wed, 26 Jan 2022 01:47:35 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 16:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 16:49:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 16:50:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 20:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 20:33:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Feb 2022 01:01:36 GMT
ENV GOLANG_VERSION=1.17.7
# Fri, 11 Feb 2022 01:02:23 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.7.linux-amd64.tar.gz'; 			sha256='02b111284bedbfa35a7e5b74a06082d18632eff824fd144312f6063943d49259'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.7.linux-armv6l.tar.gz'; 			sha256='874774f078b182fa21ffcb3878467eb5cb7e78bbffa6343ea5f0fbe47983433b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.7.linux-arm64.tar.gz'; 			sha256='a5aa1ed17d45ee1d58b4a4099b12f8942acbd1dd09b2e9a6abb1c4898043c5f5'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.7.linux-386.tar.gz'; 			sha256='5d5472672a2e0252fe31f4ec30583d9f2b320f9b9296eda430f03cbc848400ce'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.7.linux-ppc64le.tar.gz'; 			sha256='2262fdee9147eb61fd1e719cfd19b9c035009c14890de02b5a77071b0a577405'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.7.linux-s390x.tar.gz'; 			sha256='24dd117581d592f52b4cf45d75ae68a6a1e42691a8671a2d3c2ddd739894a1e4'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.7.src.tar.gz'; 		sha256='c108cd33b73b1911a02b697741df3dea43e01a5c4e08e409e8b3a0e3745d2b4d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 11 Feb 2022 01:02:25 GMT
ENV GOPATH=/go
# Fri, 11 Feb 2022 01:02:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Feb 2022 01:02:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 11 Feb 2022 01:02:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a4becb4205b812ec841e47cdf4840f3cd4afedb320617c1a611bd7daacd1b1e2`  
		Last Modified: Wed, 26 Jan 2022 02:05:16 GMT  
		Size: 42.1 MB (42116772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19142ccd43f320261157cec769910c598094bd2f6235ca3fb72f11ff969ba877`  
		Last Modified: Wed, 26 Jan 2022 17:12:46 GMT  
		Size: 10.0 MB (9956581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bc45f0a06bfebcf8cb3dd7f3b1577bb99c1c9a19b3dc44bab307cdd59267bb`  
		Last Modified: Wed, 26 Jan 2022 17:12:42 GMT  
		Size: 3.9 MB (3921220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f5aa09ea754ba47aefee810b542e69d5f77d134463813ea07489fa9ec46932`  
		Last Modified: Wed, 26 Jan 2022 17:13:26 GMT  
		Size: 46.1 MB (46126065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcebddff60b038c4a2d28edf63a333bffa990ce9a3f4fb80a0ed3c69a94d29d3`  
		Last Modified: Thu, 27 Jan 2022 20:51:05 GMT  
		Size: 46.2 MB (46193612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d908c05466a37a06daca1e5f1ed4af32d7f59bcc9eb4ffc4eaced1ea7df0ad6`  
		Last Modified: Fri, 11 Feb 2022 01:30:10 GMT  
		Size: 103.1 MB (103088516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292561cacdf33b4ec4096ca47443e494971485b33bd96c2bc5defc9481618776`  
		Last Modified: Fri, 11 Feb 2022 01:29:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c8dddf94cd54ba2cdf6be8032f26f309b414956d9c1f33def27cd3bce0c4f3aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256679113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671a960996a0a55bb8a124a177d03acfc7a533fd04f7c33cf007b8a0a6eadc63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:44:34 GMT
ADD file:fc57ceb549dcf9223a7806f1dbd83ede31ad1705eda04387f43795b8949b19c4 in / 
# Wed, 26 Jan 2022 01:44:34 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:17:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:17:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:18:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 18:47:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 18:48:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Feb 2022 00:42:38 GMT
ENV GOLANG_VERSION=1.17.7
# Fri, 11 Feb 2022 00:43:09 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.7.linux-amd64.tar.gz'; 			sha256='02b111284bedbfa35a7e5b74a06082d18632eff824fd144312f6063943d49259'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.7.linux-armv6l.tar.gz'; 			sha256='874774f078b182fa21ffcb3878467eb5cb7e78bbffa6343ea5f0fbe47983433b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.7.linux-arm64.tar.gz'; 			sha256='a5aa1ed17d45ee1d58b4a4099b12f8942acbd1dd09b2e9a6abb1c4898043c5f5'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.7.linux-386.tar.gz'; 			sha256='5d5472672a2e0252fe31f4ec30583d9f2b320f9b9296eda430f03cbc848400ce'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.7.linux-ppc64le.tar.gz'; 			sha256='2262fdee9147eb61fd1e719cfd19b9c035009c14890de02b5a77071b0a577405'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.7.linux-s390x.tar.gz'; 			sha256='24dd117581d592f52b4cf45d75ae68a6a1e42691a8671a2d3c2ddd739894a1e4'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.7.src.tar.gz'; 		sha256='c108cd33b73b1911a02b697741df3dea43e01a5c4e08e409e8b3a0e3745d2b4d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 11 Feb 2022 00:43:11 GMT
ENV GOPATH=/go
# Fri, 11 Feb 2022 00:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Feb 2022 00:43:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 11 Feb 2022 00:43:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:11cbe372cf332799e1339b2b8a04723e8224eb56d69212a1308d1df0da55eae2`  
		Last Modified: Wed, 26 Jan 2022 01:52:53 GMT  
		Size: 43.2 MB (43173725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf576a0611a8862b3ac5cc25b79aedd7b2f5a1a457ead352a467fa5b906d0f6`  
		Last Modified: Wed, 26 Jan 2022 02:27:24 GMT  
		Size: 10.2 MB (10216892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc21f7f695aceaf60c5d2590b7acb0d3937aab7af8a9470dd74605632805610`  
		Last Modified: Wed, 26 Jan 2022 02:27:24 GMT  
		Size: 3.9 MB (3873916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16466baa01cbf2b86dbc5f9f876247c80462e423aa7a6b68dfec79de47f85e9e`  
		Last Modified: Wed, 26 Jan 2022 02:27:43 GMT  
		Size: 47.7 MB (47733953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96683053ff7cbf1282b084b86af507f79dfb403dc2a55e375406af0d30cfcd7c`  
		Last Modified: Wed, 26 Jan 2022 19:00:06 GMT  
		Size: 49.0 MB (49022901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c783ec32df176b64959882c35c2387f79b439f1830f6f5d6803cedd1c3ee27`  
		Last Modified: Fri, 11 Feb 2022 00:55:57 GMT  
		Size: 102.7 MB (102657600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18a15043b91b32b50bb01e52dcad6007a63b1d19d259d168823e5ec7b278934`  
		Last Modified: Fri, 11 Feb 2022 00:55:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; 386

```console
$ docker pull golang@sha256:c79b67f615626a15c6a374c2c8ba02aedbf3c87b94745063001ce60ebf627d20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281327364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0e1b03e5f81f9d37860048cec86451f468190ee2e8d56cd1dc66631422e295`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:51 GMT
ADD file:84c4f9ca5f39d4d5afa373f2ef32d0a65a614861bd5e53fe072387283ea5901d in / 
# Wed, 26 Jan 2022 01:42:52 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:22:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 04:57:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 04:57:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Feb 2022 00:41:29 GMT
ENV GOLANG_VERSION=1.17.7
# Fri, 11 Feb 2022 00:42:35 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.7.linux-amd64.tar.gz'; 			sha256='02b111284bedbfa35a7e5b74a06082d18632eff824fd144312f6063943d49259'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.7.linux-armv6l.tar.gz'; 			sha256='874774f078b182fa21ffcb3878467eb5cb7e78bbffa6343ea5f0fbe47983433b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.7.linux-arm64.tar.gz'; 			sha256='a5aa1ed17d45ee1d58b4a4099b12f8942acbd1dd09b2e9a6abb1c4898043c5f5'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.7.linux-386.tar.gz'; 			sha256='5d5472672a2e0252fe31f4ec30583d9f2b320f9b9296eda430f03cbc848400ce'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.7.linux-ppc64le.tar.gz'; 			sha256='2262fdee9147eb61fd1e719cfd19b9c035009c14890de02b5a77071b0a577405'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.7.linux-s390x.tar.gz'; 			sha256='24dd117581d592f52b4cf45d75ae68a6a1e42691a8671a2d3c2ddd739894a1e4'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.7.src.tar.gz'; 		sha256='c108cd33b73b1911a02b697741df3dea43e01a5c4e08e409e8b3a0e3745d2b4d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 11 Feb 2022 00:42:36 GMT
ENV GOPATH=/go
# Fri, 11 Feb 2022 00:42:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Feb 2022 00:42:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 11 Feb 2022 00:42:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58d50d1151db66fec3407a887e75ea0080e2b06c23447d1aa582592c9fbd7eec`  
		Last Modified: Wed, 26 Jan 2022 01:53:54 GMT  
		Size: 46.1 MB (46097933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cc62fa793c6ec57e2be9c7b8ec84514c2c0118cdbc2b4336ee49f720fe729c`  
		Last Modified: Wed, 26 Jan 2022 02:33:31 GMT  
		Size: 11.4 MB (11359514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1167f9e9e1ee3be249d14a5d199dbb303b25457deb6ff54ac1887165400cc0b`  
		Last Modified: Wed, 26 Jan 2022 02:33:31 GMT  
		Size: 4.6 MB (4564913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb5396177d46c4d42762f2b25f0a04d0b1af759b32f35024060a9e5945b4400`  
		Last Modified: Wed, 26 Jan 2022 02:33:55 GMT  
		Size: 51.3 MB (51265223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada88b4c38be46f64d8310fdf0c0067df9e92df229f678bdb6c1fc582506c450`  
		Last Modified: Thu, 27 Jan 2022 05:12:52 GMT  
		Size: 62.4 MB (62387840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7b5624a55880aa91c2e124512ec6a8e03d71a78493dbd17e94e4debd653c1`  
		Last Modified: Fri, 11 Feb 2022 01:02:33 GMT  
		Size: 105.7 MB (105651785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d76040fdb218079e1a5023bf21ccef15687b149ec169d619de134af75c9c9e4`  
		Last Modified: Fri, 11 Feb 2022 01:02:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
