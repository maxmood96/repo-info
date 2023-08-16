## `golang:1-bookworm`

```console
$ docker pull golang@sha256:c4a6da645d4d0c00b407aab58b34e714884ef7c519e52a41cf722bd75d46fd5e
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:709b81692225f264c51939c40318a0b7c4cefea3d9c75317f1355464a8734b71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296837143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3758cb2c0a6b8b21af65fbb468fa935dbdfc9ffd58bc53d2b9fb6e1f920318fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:29 GMT
ADD file:cc1376ecb3d9e93e4160573c110da753ffeb2efe2223351f1fbf483d89f1a756 in / 
# Thu, 27 Jul 2023 23:24:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:00:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:01:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 20:33:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 20:33:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:40:56 GMT
ENV GOLANG_VERSION=1.21.0
# Wed, 09 Aug 2023 04:41:04 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 09 Aug 2023 04:41:05 GMT
ENV GOPATH=/go
# Wed, 09 Aug 2023 04:41:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:41:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 09 Aug 2023 04:41:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:785ef8b9b236a5f027f33cae77513051704c0538bff455ff5548105c954c3b1c`  
		Last Modified: Thu, 27 Jul 2023 23:29:02 GMT  
		Size: 49.6 MB (49557354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6dad8f55ae6c733e986316bd08205c8b2c41640bf8d08ff6e9bbcb6884304f`  
		Last Modified: Fri, 28 Jul 2023 03:07:18 GMT  
		Size: 24.0 MB (24030539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd36c7bfe5f4bdffcc0bbb74b0fb38feb35c286ea58b5992617fb38b0c933603`  
		Last Modified: Fri, 28 Jul 2023 03:07:36 GMT  
		Size: 64.1 MB (64112293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e59e6b803ed24f34e9d1001d46221a69fa46b48d7d007de7d32fc07d031a408`  
		Last Modified: Fri, 28 Jul 2023 20:36:01 GMT  
		Size: 92.3 MB (92267552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e40ac7456b59e503106091ef45f2979fd4730602a4036b91d13972ab1832bd9`  
		Last Modified: Wed, 09 Aug 2023 04:45:47 GMT  
		Size: 66.9 MB (66869250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e11a6c7a2e676a7404b3340b50ab9218e7b44fec21caab54441163139f911d6`  
		Last Modified: Wed, 09 Aug 2023 04:45:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v5

```console
$ docker pull golang@sha256:291849f9186a989b8f5bce22fd10c361d9e446d56ecf335c5f7e8572e98e45a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271120308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94628631ec33c05b8158c83fa8837d7a8374f9ee58456fdfc5a2efaadedbe388`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:21 GMT
ADD file:7b6666a92b89bab40a1b4dda36930e1b5a7b9ab40ac8dadd2179767e027de097 in / 
# Thu, 27 Jul 2023 23:48:21 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 06:19:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:19:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 16:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 16:25:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 20:53:38 GMT
ENV GOLANG_VERSION=1.21.0
# Tue, 08 Aug 2023 20:57:42 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 08 Aug 2023 20:57:43 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 20:57:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 20:57:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 20:57:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:882ddccdc867712377829e4abe9ddf1190166c3dbdfc4cee67aafb08e253cc1f`  
		Last Modified: Thu, 27 Jul 2023 23:51:04 GMT  
		Size: 47.4 MB (47414939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f253718c89752af3d3827fa9e08b951a2eeb9e7fb65162096eff9684d21a4b38`  
		Last Modified: Fri, 28 Jul 2023 06:25:10 GMT  
		Size: 22.7 MB (22709706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54a2e1f4e1f80c2371c6fc46dad3133af5078cb0653caed09e33a1b64063c79`  
		Last Modified: Fri, 28 Jul 2023 06:25:32 GMT  
		Size: 61.6 MB (61554152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2d0be02e95c98ad93bb1974e56fa20c4b73c2fab665b6ef7391f0b1394a90`  
		Last Modified: Fri, 28 Jul 2023 16:39:09 GMT  
		Size: 71.3 MB (71275972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52e393b6b5a368006dce3cb02963e449fc36d284471bd0a88fc35a56a45142b`  
		Last Modified: Tue, 08 Aug 2023 21:02:50 GMT  
		Size: 68.2 MB (68165383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cf72208dbebceac2f0960953c6aaad9343732234f8cd3bc5e7c3e8b147355`  
		Last Modified: Tue, 08 Aug 2023 21:02:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:58c46aa8fdaee1ffabcc9a51f03112f8b3b949d7eedb1232e8b8986a8999f7b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257986789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bf873d3e080b67d5db46227b80bf348e2a2bdf63e960bb4b508f8cdb8722b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:57:34 GMT
ADD file:be1c9c3d1025b24193774f5c0d5f790387924ed669771b461b2c599068512dc5 in / 
# Thu, 27 Jul 2023 23:57:35 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:57:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:58:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 23:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 23:22:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 22:03:28 GMT
ENV GOLANG_VERSION=1.21.0
# Tue, 08 Aug 2023 22:03:46 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 08 Aug 2023 22:03:47 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 22:03:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 22:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 22:03:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f76b23045cf894a3a989a9812af93c6b2eb7169116a938d01b03e6856046fd3a`  
		Last Modified: Fri, 28 Jul 2023 00:02:46 GMT  
		Size: 45.2 MB (45232980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc5ca91792613eb694a9a6a96dea7fa075fa3d9bf6cd91997b3575293631923`  
		Last Modified: Fri, 28 Jul 2023 02:06:30 GMT  
		Size: 21.9 MB (21936835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41630b85b67c30afc21e9a68ad3a0b59c168c1955785b07d9f581d53cf5fa22c`  
		Last Modified: Fri, 28 Jul 2023 02:06:49 GMT  
		Size: 59.3 MB (59261975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a778e7eeea9189d0094336196183eb4017623b1521cecc48c6e21b75b772a0d`  
		Last Modified: Fri, 28 Jul 2023 23:25:04 GMT  
		Size: 66.1 MB (66117528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8e2f76019219a2315578865365c85ad9c47223a8bd8b66c482c0dec5e2b703`  
		Last Modified: Tue, 08 Aug 2023 22:06:00 GMT  
		Size: 65.4 MB (65437316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee15651dca2411a54d2952ae7634afb19b4d1212a4da125ae6c4be86b92f4c1a`  
		Last Modified: Tue, 08 Aug 2023 22:05:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7ae2179405af066285165c058bd07f252851e2867b2da0f44bd832637b3fd306
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287424601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732a5451b1e02c0894e6b0c25776de7b6817070ea570ff713343c5c7b386baed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:42:51 GMT
ADD file:fa545fc37115e874135945921d2cc72df8dc5b16d4354b2052717c7a57043e0d in / 
# Thu, 27 Jul 2023 23:42:51 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:35:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:36:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 15:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 15:26:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:10:00 GMT
ENV GOLANG_VERSION=1.21.0
# Tue, 08 Aug 2023 23:10:07 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 08 Aug 2023 23:10:09 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:10:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:10:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:10:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fc9ce7290e7e014f69623715ba619a0d3488a7b6ecbf09e55e11160365691192`  
		Last Modified: Thu, 27 Jul 2023 23:45:54 GMT  
		Size: 49.6 MB (49591268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73373011d63f722a4ac6bc23ce7831a17f19e27ef530544642f060aa1d6b028b`  
		Last Modified: Fri, 28 Jul 2023 01:41:58 GMT  
		Size: 23.6 MB (23570127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dafffb02e2671e7e5cc07c996fed89f6ccc8e3276ce2dc1bbfb81502cdd795`  
		Last Modified: Fri, 28 Jul 2023 01:42:15 GMT  
		Size: 64.0 MB (63988301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a3c220d5856a80e0d8b608fad172d635ba46d2a583c9ab5d5aa1d22daae0ae`  
		Last Modified: Fri, 28 Jul 2023 15:29:32 GMT  
		Size: 86.3 MB (86297259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0871e76b53ec4d4fc69b883f7a6cefff6072d70a10175872f2989f5500e013`  
		Last Modified: Tue, 08 Aug 2023 23:13:45 GMT  
		Size: 64.0 MB (63977491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6ea1a985e6cd253411f1bd3872c9d0eef919955b7618c20ff890ad157b548a`  
		Last Modified: Tue, 08 Aug 2023 23:13:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:ef5d84ee9678b272e3e924dd228b29ad1652d42228e43044e04bc5fd9289caa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296419593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4db253aab67488228417e13d8beab16d587e05d7f5cfd7fc61ea9e64b8e51e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:44 GMT
ADD file:bfd1a38bf0df9f79f82223093a7cc153dd7b622ab08d82845c29e6c6a2b63344 in / 
# Thu, 27 Jul 2023 23:38:46 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 09:02:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 09:03:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 00:19:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 00:19:10 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:09:11 GMT
ENV GOLANG_VERSION=1.21.0
# Tue, 08 Aug 2023 23:09:22 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 08 Aug 2023 23:09:23 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:09:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:09:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:09:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7edd5f0eb761ecec3cc6497cb7ea8914684087583488efe885ab62bb56ddb33b`  
		Last Modified: Thu, 27 Jul 2023 23:42:57 GMT  
		Size: 50.6 MB (50567875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771ff57b30bb1e44cec48232f2b9d95b183cd6104fc0310512349e546d38d750`  
		Last Modified: Fri, 28 Jul 2023 09:10:55 GMT  
		Size: 24.9 MB (24869747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefdc80306ea3dd4a76cf653b56e8031ba3bea83dc15eb973ce4ff0eb769ea25`  
		Last Modified: Fri, 28 Jul 2023 09:11:19 GMT  
		Size: 66.0 MB (65972278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4901b256037a22cd80fa825a4fdfaffeb5db768cfd267c2438276d6922befd2`  
		Last Modified: Sat, 29 Jul 2023 00:22:31 GMT  
		Size: 89.7 MB (89672307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283b0e8cc101a6a43ddc5ffe51803a0f3b6ef13b8a8d4460062923e5774b1030`  
		Last Modified: Tue, 08 Aug 2023 23:11:03 GMT  
		Size: 65.3 MB (65337232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939b5dc2bf23393a0a5831840278e7f7f900f4e6124f435cf1ceaa08b9f865ce`  
		Last Modified: Tue, 08 Aug 2023 23:10:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:df6053b34b7d25ada150915c20d8a3a92f894edfbe055b6a7870d9d0206a86ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267756477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66bee4b015af14ec2f0f00a9ae20420c683db8c3dc8826c3ed97ecfc76524f4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:10:44 GMT
ADD file:3568f288ff9791a341f5cb0e99c0a63e09a68f3816d7f7a9971127b9b98a04b8 in / 
# Thu, 27 Jul 2023 23:10:50 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:13:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 19:44:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 19:44:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 21:24:42 GMT
ENV GOLANG_VERSION=1.21.0
# Tue, 08 Aug 2023 21:25:32 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 08 Aug 2023 21:25:40 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 21:25:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 21:25:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 21:26:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e4dbd8372ba202a8b430bce8d5c5b8a4bfdbc6ef2703180665e5964d51bb0437`  
		Last Modified: Thu, 27 Jul 2023 23:21:43 GMT  
		Size: 49.5 MB (49542050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69206dfad992d03f1e8e833ae728ffacf2c6919f78c4822d849e341473efebb`  
		Last Modified: Fri, 28 Jul 2023 01:31:27 GMT  
		Size: 23.6 MB (23612647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fab0a49ca1e0cd2eb4b9660e3a70dc1ab671984cc4843ea845a6cf76532eaa`  
		Last Modified: Fri, 28 Jul 2023 01:32:19 GMT  
		Size: 63.0 MB (62950846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3111f1bcc30e6eb541b76a95351b90515be864553f2ca58dcb1f8035e15833f2`  
		Last Modified: Sat, 29 Jul 2023 20:42:16 GMT  
		Size: 69.6 MB (69625048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503e556f1b1861954a25d70f3a5c25853440cbb11869ead2ba011199ff4395e9`  
		Last Modified: Tue, 08 Aug 2023 21:29:15 GMT  
		Size: 62.0 MB (62025760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78bef0024a1147f7116d9d415cfeec8b3b94e6a53d3c739f489f5e8b447851e`  
		Last Modified: Tue, 08 Aug 2023 21:28:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:85f57acfe2e26699b4355cf0e5228078239a8b20a083a1e52ff74e583e2aa302
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (303040989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf58f449b95dea76827ece710718815e049ba315bb4975e89135eaf77421035`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:22:41 GMT
ADD file:b20300808df8e1ce5b5ff534088c39d6b04467476af024e54545f7857f78a508 in / 
# Thu, 27 Jul 2023 23:22:43 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:47:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:48:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 01:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 01:51:44 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:11:53 GMT
ENV GOLANG_VERSION=1.21.0
# Tue, 08 Aug 2023 23:12:14 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 08 Aug 2023 23:12:18 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:12:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:12:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b6d31d119ff78cff1435e4eb51d8918916c2d5057cebf12b76d5352660fb90de`  
		Last Modified: Thu, 27 Jul 2023 23:28:46 GMT  
		Size: 53.5 MB (53543346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a33abb1f7b6ee01625f07108e25c720832ec763cb926abf676b8841aeff7a3`  
		Last Modified: Fri, 28 Jul 2023 01:59:03 GMT  
		Size: 25.7 MB (25680980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b3b1ad4b6d7fdd0b5ed658423ee70f16882053f8cd775f5234fe8217ad8a4a`  
		Last Modified: Fri, 28 Jul 2023 01:59:35 GMT  
		Size: 69.6 MB (69570344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119f2397f35dded363af8493b7b12670a66fb8c96604a889aa53204b073b950c`  
		Last Modified: Sat, 29 Jul 2023 01:57:01 GMT  
		Size: 90.2 MB (90248266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf90a7f7d98de3b09e9222370bbcfce9df3c821ffb64a57b4e73d6475a13c32`  
		Last Modified: Tue, 08 Aug 2023 23:15:38 GMT  
		Size: 64.0 MB (63997898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4e4321a8f6b317ea5b4ffecf64f20fd69bfdfd63f176a5ea9200bb5c776b99`  
		Last Modified: Tue, 08 Aug 2023 23:15:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:8beb7f6648adfc35bce77e6b475ff1ae01cffa7a589539eaeb3b0a2af2be3bdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269978349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9504ae1a7a6c0efbf92055df81a0214cdb4738db6d1ebab822a7aa341643f532`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:42:11 GMT
ADD file:eeb165e8fcc9b8f3a9e8f10fdbd507a91bc934046a4f23f2d636ca4b1796d1e3 in / 
# Tue, 15 Aug 2023 23:42:17 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 04:20:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 04:20:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 11:47:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 11:47:59 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 11:47:59 GMT
ENV GOLANG_VERSION=1.21.0
# Wed, 16 Aug 2023 11:48:19 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz'; 			sha256='d0398903a16ba2232b389fb31032ddf57cac34efda306a0eebac34f0965a0742'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.0.linux-armv6l.tar.gz'; 			sha256='e377a0004957c8c560a3ff99601bce612330a3d95ba3b0a2ae144165fc87deb1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.0.linux-arm64.tar.gz'; 			sha256='f3d4548edf9b22f26bbd49720350bbfe59d75b7090a1a2bff1afad8214febaf3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.0.linux-386.tar.gz'; 			sha256='0e6f378d9b072fab0a3d9ff4d5e990d98487d47252dba8160015a61e6bd0bcba'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.0.linux-mips64le.tar.gz'; 			sha256='92f7933d997c589b4f506c6b3cc5b27ff43b294c3a2d40bf4d7eeaf375f92afb'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.0.linux-ppc64le.tar.gz'; 			sha256='e938ffc81d8ebe5efc179240960ba22da6a841ff05d5cab7ce2547112b14a47f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.0.linux-riscv64.tar.gz'; 			sha256='87b21c06573617842ca9e00b954bc9f534066736a0778eae594ac54b45a9e8b7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.0.linux-s390x.tar.gz'; 			sha256='be7338df8e5d5472dfa307b0df2b446d85d001b0a2a3cdb1a14048d751b70481'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.0.src.tar.gz'; 		sha256='818d46ede85682dd551ad378ef37a4d247006f12ec59b5b755601d2ce114369a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 16 Aug 2023 11:48:25 GMT
ENV GOPATH=/go
# Wed, 16 Aug 2023 11:48:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 11:48:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 16 Aug 2023 11:48:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2bf08d586558a71fd0c5172579e7c378968a16f427fb3af772e4aa11c6b0a7af`  
		Last Modified: Tue, 15 Aug 2023 23:47:38 GMT  
		Size: 47.9 MB (47922016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afba98ba5dea198ec27ff40c833c54ce73ca11dccc94b59611cb506b44fa422`  
		Last Modified: Wed, 16 Aug 2023 04:36:16 GMT  
		Size: 24.0 MB (24028770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc50673f1af082588bca57ac1eaff982b89ce5badbe6d6b389ad96961fe54a81`  
		Last Modified: Wed, 16 Aug 2023 04:36:31 GMT  
		Size: 63.1 MB (63113641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fce761814670516cbaa641efff78723f5770da721461f0f5915a14c68ad49a7`  
		Last Modified: Wed, 16 Aug 2023 11:51:24 GMT  
		Size: 68.8 MB (68826812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48625840d728dfb96322d9c51dc1c8f02f9a705aed84424d736d0a22d7c925c5`  
		Last Modified: Wed, 16 Aug 2023 11:51:25 GMT  
		Size: 66.1 MB (66086953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cafe45aea312c942c9a81e79c613dd8fc7a6e674be7eaee5e4322eef321e528`  
		Last Modified: Wed, 16 Aug 2023 11:51:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
