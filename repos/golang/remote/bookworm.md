## `golang:bookworm`

```console
$ docker pull golang@sha256:092d4d173606496cee017bf41ffbdd361a74872f9e9c91d9a5472019c76d3c4b
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

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:7f2cf491a0d8c1afcdc55120cda9d3777ee98852eff619c6c3e5a0b2386a69b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330131703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a118f29bfadd6529ee8da6b1261fab7d0d80de3bb9b496ee6a189a21f17029`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:44 GMT
ADD file:5d17ca085473e890bd6eca4abf6d324c3181f80692523b83ef25d1c42576b99f in / 
# Tue, 04 Jul 2023 01:19:44 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:28:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 03:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 03:27:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:28:10 GMT
ENV GOLANG_VERSION=1.20.5
# Wed, 05 Jul 2023 03:28:19 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz'; 			sha256='d7ec48cde0d3d2be2c69203bc3e0a44de8660b9c09a6e85c4732a3f7dc442612'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.5.linux-armv6l.tar.gz'; 			sha256='79d8210efd4390569912274a98dffc16eb85993cccdeef4d704e9b0dfd50743a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.5.linux-arm64.tar.gz'; 			sha256='aa2fab0a7da20213ff975fa7876a66d47b48351558d98851b87d1cfef4360d09'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.5.linux-386.tar.gz'; 			sha256='d394ac8fecf66812c78ffba7fb9a265bb1b9917564c7fd77f0edb0df6d5777a1'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.5.linux-ppc64le.tar.gz'; 			sha256='049b8ab07d34077b90c0642138e10207f6db14bdd1743ea994a21e228f8ca53d'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.5.linux-s390x.tar.gz'; 			sha256='bac14667f1217ccce1d2ef4e204687fe6191e6dc19a8870cfb81a41f78b04e48'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.5.src.tar.gz'; 		sha256='9a15c133ba2cfafe79652f4815b62e7cfc267f68df1b9454c6ab2a3ca8b96a88'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 05 Jul 2023 03:28:19 GMT
ENV GOPATH=/go
# Wed, 05 Jul 2023 03:28:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:28:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 05 Jul 2023 03:28:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d52e4f012db158bb7c0fe215b98af1facaddcbaee530efd69b1bae07d597b711`  
		Last Modified: Tue, 04 Jul 2023 01:24:39 GMT  
		Size: 49.6 MB (49551432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd206bea61ff3e3b54be1c20b58d8475ddd6f89df176146ddb7a2fd2c747ea2`  
		Last Modified: Tue, 04 Jul 2023 03:51:23 GMT  
		Size: 24.0 MB (24030593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2320f9be4a9c605d1ac847cf67cec42b91484a7cf7c94996417a0c7c316deadc`  
		Last Modified: Tue, 04 Jul 2023 03:51:42 GMT  
		Size: 64.1 MB (64111613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c0c50a70de44530fb9f35321081e7dd67f9aeae1ca5ab99161eb6322e2868`  
		Last Modified: Wed, 05 Jul 2023 03:30:00 GMT  
		Size: 92.2 MB (92233360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec14dce7e7846bbadf40f19d3d871f619c54c1fa6296cc3cfaa810b3c66024d`  
		Last Modified: Wed, 05 Jul 2023 03:30:42 GMT  
		Size: 100.2 MB (100204550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ad738259f2ede8cfe2e998bd5abecbbf5089124842893452008bc64055d4a9`  
		Last Modified: Wed, 05 Jul 2023 03:30:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; arm variant v5

```console
$ docker pull golang@sha256:913f2fb01aec2b513da28cf67ef02ef80f8010700f16c459dfa1019f847f92de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302144023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f899fbf178df6e9417af3105cd828ba4ec509d03244b769dcfc5c580906e9319`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:22 GMT
ADD file:09001854dc5081f907ac2a66d301e4b3d6b4bf2c2483aad5395a535bf068698d in / 
# Tue, 04 Jul 2023 00:48:22 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:21:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:03:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:03:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 18:08:32 GMT
ENV GOLANG_VERSION=1.20.5
# Tue, 04 Jul 2023 18:10:31 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz'; 			sha256='d7ec48cde0d3d2be2c69203bc3e0a44de8660b9c09a6e85c4732a3f7dc442612'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.5.linux-armv6l.tar.gz'; 			sha256='79d8210efd4390569912274a98dffc16eb85993cccdeef4d704e9b0dfd50743a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.5.linux-arm64.tar.gz'; 			sha256='aa2fab0a7da20213ff975fa7876a66d47b48351558d98851b87d1cfef4360d09'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.5.linux-386.tar.gz'; 			sha256='d394ac8fecf66812c78ffba7fb9a265bb1b9917564c7fd77f0edb0df6d5777a1'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.5.linux-ppc64le.tar.gz'; 			sha256='049b8ab07d34077b90c0642138e10207f6db14bdd1743ea994a21e228f8ca53d'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.5.linux-s390x.tar.gz'; 			sha256='bac14667f1217ccce1d2ef4e204687fe6191e6dc19a8870cfb81a41f78b04e48'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.5.src.tar.gz'; 		sha256='9a15c133ba2cfafe79652f4815b62e7cfc267f68df1b9454c6ab2a3ca8b96a88'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 04 Jul 2023 18:10:33 GMT
ENV GOPATH=/go
# Tue, 04 Jul 2023 18:10:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 18:10:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 04 Jul 2023 18:10:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7e0a1f476b42bcc214197ec9c5ef753ddf2ab36a314416a6ac96cd921ff0d41d`  
		Last Modified: Tue, 04 Jul 2023 00:51:29 GMT  
		Size: 47.4 MB (47402786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68311cc5ff511aa59283fdd7f1e25bc33dfc3ad9ae87e5c94447f36c3f7c4817`  
		Last Modified: Tue, 04 Jul 2023 04:28:32 GMT  
		Size: 22.7 MB (22708933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09518fc93ba137cac901dd7b0cc5fab1e20a21a7d6bbe3a35b7f921a069ddc5c`  
		Last Modified: Tue, 04 Jul 2023 04:28:53 GMT  
		Size: 61.6 MB (61553936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7066c0d857eea041a04e2ad95001c8214a5b28bd0b257ab9baac1fbf2470fb`  
		Last Modified: Tue, 04 Jul 2023 18:18:18 GMT  
		Size: 71.2 MB (71235513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d776a1f31e6e93b8c3d9a6ad6158e9e9c1cb705e1e5841fe48ff7088f6d6e9`  
		Last Modified: Tue, 04 Jul 2023 18:19:09 GMT  
		Size: 99.2 MB (99242699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666bee6415d979d1244151d878f6ee3d2112deb8cd23c2c297f0769f8b8c3c36`  
		Last Modified: Tue, 04 Jul 2023 18:18:54 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:964cfbf561af86350497345bea346374ca9a44dd9b76e59753e49895010e47a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290430853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7b1f1c94ecc84c1916410a0fc5811e32c4827dcfabcd9f7143c310c52add4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:57:42 GMT
ADD file:279ef7213d41f1f7ae76bd76293a5107fd1f8caf557f837cab9c834d2841e031 in / 
# Tue, 04 Jul 2023 00:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:49:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:50:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:25:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:25:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:26:51 GMT
ENV GOLANG_VERSION=1.20.5
# Tue, 04 Jul 2023 20:27:08 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz'; 			sha256='d7ec48cde0d3d2be2c69203bc3e0a44de8660b9c09a6e85c4732a3f7dc442612'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.5.linux-armv6l.tar.gz'; 			sha256='79d8210efd4390569912274a98dffc16eb85993cccdeef4d704e9b0dfd50743a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.5.linux-arm64.tar.gz'; 			sha256='aa2fab0a7da20213ff975fa7876a66d47b48351558d98851b87d1cfef4360d09'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.5.linux-386.tar.gz'; 			sha256='d394ac8fecf66812c78ffba7fb9a265bb1b9917564c7fd77f0edb0df6d5777a1'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.5.linux-ppc64le.tar.gz'; 			sha256='049b8ab07d34077b90c0642138e10207f6db14bdd1743ea994a21e228f8ca53d'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.5.linux-s390x.tar.gz'; 			sha256='bac14667f1217ccce1d2ef4e204687fe6191e6dc19a8870cfb81a41f78b04e48'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.5.src.tar.gz'; 		sha256='9a15c133ba2cfafe79652f4815b62e7cfc267f68df1b9454c6ab2a3ca8b96a88'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 04 Jul 2023 20:27:09 GMT
ENV GOPATH=/go
# Tue, 04 Jul 2023 20:27:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:27:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 04 Jul 2023 20:27:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b9bdcf1a9a6361f231594c76a75bfb4c2fef5f9745b9713bbd50efaf37ca11b8`  
		Last Modified: Tue, 04 Jul 2023 01:02:26 GMT  
		Size: 45.2 MB (45236201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8ee33ea63b2391e912423c14b2f1e789137ffb03659568cb361a2fa2b4efbd`  
		Last Modified: Tue, 04 Jul 2023 06:18:41 GMT  
		Size: 21.9 MB (21936446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2a5b4416a84ac4585c3e3879ca49a6fc3e8d46028a4f27098ae1bdb4ae710d`  
		Last Modified: Tue, 04 Jul 2023 06:19:01 GMT  
		Size: 59.3 MB (59261674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8b43ac2d39a65f3e23dfa2170cabc5c1ab30a923f51ff703bf75c1b9d565b`  
		Last Modified: Tue, 04 Jul 2023 20:29:09 GMT  
		Size: 66.1 MB (66070661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9e86578e98a35085a28f764ad8dd792ecc64ca6f6809a2bda34356da594664`  
		Last Modified: Tue, 04 Jul 2023 20:30:00 GMT  
		Size: 97.9 MB (97925715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095bfee5e600375d4a9a2dd7da7eec28cea7b5f5206ff017d404c8ea4fa8ffdd`  
		Last Modified: Tue, 04 Jul 2023 20:29:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:bdc4911404c468c03b374e7c578479c3ed40f801123d0f070e7e92ac6b54093c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318919606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b4bfabe2336568b6aa132be58e6f406a8af1db0a37102f9f94304772a64546`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:26 GMT
ADD file:ab1761d899751c4d24e15179fc9e7e7ac3fb83798ee37ca13d6a6ac44fbeded3 in / 
# Tue, 04 Jul 2023 01:57:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:54:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:33:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:35:00 GMT
ENV GOLANG_VERSION=1.20.5
# Tue, 04 Jul 2023 20:35:09 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz'; 			sha256='d7ec48cde0d3d2be2c69203bc3e0a44de8660b9c09a6e85c4732a3f7dc442612'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.5.linux-armv6l.tar.gz'; 			sha256='79d8210efd4390569912274a98dffc16eb85993cccdeef4d704e9b0dfd50743a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.5.linux-arm64.tar.gz'; 			sha256='aa2fab0a7da20213ff975fa7876a66d47b48351558d98851b87d1cfef4360d09'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.5.linux-386.tar.gz'; 			sha256='d394ac8fecf66812c78ffba7fb9a265bb1b9917564c7fd77f0edb0df6d5777a1'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.5.linux-ppc64le.tar.gz'; 			sha256='049b8ab07d34077b90c0642138e10207f6db14bdd1743ea994a21e228f8ca53d'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.5.linux-s390x.tar.gz'; 			sha256='bac14667f1217ccce1d2ef4e204687fe6191e6dc19a8870cfb81a41f78b04e48'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.5.src.tar.gz'; 		sha256='9a15c133ba2cfafe79652f4815b62e7cfc267f68df1b9454c6ab2a3ca8b96a88'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 04 Jul 2023 20:35:10 GMT
ENV GOPATH=/go
# Tue, 04 Jul 2023 20:35:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:35:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 04 Jul 2023 20:35:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:42cbebf8bc116ba1aed7897e2d0566bf49da9d5c70be71b6a7cb07805d2f5b7a`  
		Last Modified: Tue, 04 Jul 2023 02:00:57 GMT  
		Size: 49.6 MB (49572781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0518ec57568a70561f7c04650f9554c88dada973f54d88e36f65b0796d35de`  
		Last Modified: Tue, 04 Jul 2023 06:21:03 GMT  
		Size: 23.6 MB (23569546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356172c718acf9930d9465b170864319079e2d2ebac0ddef781d64e85789531e`  
		Last Modified: Tue, 04 Jul 2023 06:21:20 GMT  
		Size: 64.0 MB (63984075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c1d40c82551fded3ae8435595284e568a5c425b275785f3a78b95ed6f25b15`  
		Last Modified: Tue, 04 Jul 2023 20:36:55 GMT  
		Size: 86.3 MB (86263948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a25fd6c67db457856f2591a1302480b69bc7c20f51974a91ab7317cb34a9cd`  
		Last Modified: Tue, 04 Jul 2023 20:37:32 GMT  
		Size: 95.5 MB (95529101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4a4d5175d574eafdd97d63485c1075146d5707efacfd0cc361722e878540b9`  
		Last Modified: Tue, 04 Jul 2023 20:37:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:3a27e287139274678c9907646e35acddc4c5498a21e8c97f6f3b040355f4a225
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.6 MB (331640643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f2b5c25efb07de578bb410f61e234c2467a3b2441ea42d9cee8275d0cf4dff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:25 GMT
ADD file:e0a25fe261e09183ec383698ab2c800f93c5b0805564d7104ad5119db52cccb7 in / 
# Tue, 04 Jul 2023 01:38:25 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:28:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:40:38 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 01:41:30 GMT
ENV GOLANG_VERSION=1.20.5
# Wed, 05 Jul 2023 01:41:45 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz'; 			sha256='d7ec48cde0d3d2be2c69203bc3e0a44de8660b9c09a6e85c4732a3f7dc442612'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.5.linux-armv6l.tar.gz'; 			sha256='79d8210efd4390569912274a98dffc16eb85993cccdeef4d704e9b0dfd50743a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.5.linux-arm64.tar.gz'; 			sha256='aa2fab0a7da20213ff975fa7876a66d47b48351558d98851b87d1cfef4360d09'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.5.linux-386.tar.gz'; 			sha256='d394ac8fecf66812c78ffba7fb9a265bb1b9917564c7fd77f0edb0df6d5777a1'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.5.linux-ppc64le.tar.gz'; 			sha256='049b8ab07d34077b90c0642138e10207f6db14bdd1743ea994a21e228f8ca53d'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.5.linux-s390x.tar.gz'; 			sha256='bac14667f1217ccce1d2ef4e204687fe6191e6dc19a8870cfb81a41f78b04e48'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.5.src.tar.gz'; 		sha256='9a15c133ba2cfafe79652f4815b62e7cfc267f68df1b9454c6ab2a3ca8b96a88'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 05 Jul 2023 01:41:47 GMT
ENV GOPATH=/go
# Wed, 05 Jul 2023 01:41:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 01:41:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 05 Jul 2023 01:41:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:381263dab43af8bfb8e85c7a9a32f35492cbdcc3a046b35f947cf3bf3a55f4c1`  
		Last Modified: Tue, 04 Jul 2023 01:43:02 GMT  
		Size: 50.6 MB (50562388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af522778d6fcd5f4b85dafb1f21b89441dedee6ce875890b15ad8c454bbb9fe6`  
		Last Modified: Tue, 04 Jul 2023 05:38:10 GMT  
		Size: 24.9 MB (24869747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501f685d713d76bdc0731a917b074d79f3de7c84bfe09c53585642801175a72f`  
		Last Modified: Tue, 04 Jul 2023 05:38:34 GMT  
		Size: 66.0 MB (65972310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7528798e49d9412d7c11ffd93e7c0e57e39eef83b14c75d0e1281e36638aa`  
		Last Modified: Wed, 05 Jul 2023 01:43:49 GMT  
		Size: 89.6 MB (89635624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048d50dd8354d0a2a6ec12ee41c7ec36b729ade602cfb147363888feced05c89`  
		Last Modified: Wed, 05 Jul 2023 01:44:46 GMT  
		Size: 100.6 MB (100600418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c235abe5f1f1c4fe24565b2c9ff95c80b896cb2b3520aa07f5e7e90bc3de14`  
		Last Modified: Wed, 05 Jul 2023 01:44:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:88d621d09e8a9e846ddb545b358dddafc2e1dad605ea71aa43cc46b4a89ddac0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 MB (300049775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f11d9a959207d172ecd188fae2a7dff1bae7e8848a4c565ba6e7e423f3a3ba1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:08:08 GMT
ADD file:fbe506fea544eae98a8a13d6b55d001b4327c933053d898d5a19bf9ffd7470f8 in / 
# Tue, 13 Jun 2023 00:08:13 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 01:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 01:56:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:08:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 18:08:44 GMT
ENV GOLANG_VERSION=1.20.5
# Thu, 22 Jun 2023 01:37:29 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz'; 			sha256='d7ec48cde0d3d2be2c69203bc3e0a44de8660b9c09a6e85c4732a3f7dc442612'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.5.linux-armv6l.tar.gz'; 			sha256='79d8210efd4390569912274a98dffc16eb85993cccdeef4d704e9b0dfd50743a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.5.linux-arm64.tar.gz'; 			sha256='aa2fab0a7da20213ff975fa7876a66d47b48351558d98851b87d1cfef4360d09'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.5.linux-386.tar.gz'; 			sha256='d394ac8fecf66812c78ffba7fb9a265bb1b9917564c7fd77f0edb0df6d5777a1'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.5.linux-ppc64le.tar.gz'; 			sha256='049b8ab07d34077b90c0642138e10207f6db14bdd1743ea994a21e228f8ca53d'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.5.linux-s390x.tar.gz'; 			sha256='bac14667f1217ccce1d2ef4e204687fe6191e6dc19a8870cfb81a41f78b04e48'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.5.src.tar.gz'; 		sha256='9a15c133ba2cfafe79652f4815b62e7cfc267f68df1b9454c6ab2a3ca8b96a88'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 22 Jun 2023 01:37:37 GMT
ENV GOPATH=/go
# Thu, 22 Jun 2023 01:37:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jun 2023 01:37:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 22 Jun 2023 01:37:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb5fba29e113a7ea4313a026e3a37cd5bc1425850dfd19a63973d48c89e0f266`  
		Last Modified: Tue, 13 Jun 2023 00:21:46 GMT  
		Size: 49.5 MB (49541536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d455436c8b88038e08b0000c9ee013619617a7c7820a0bf065a54b80a660d`  
		Last Modified: Tue, 13 Jun 2023 02:19:52 GMT  
		Size: 23.6 MB (23611740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ac31b2b51452164efc6b46cc660d0ea7af24261706ad3f016de4af1ae4cf65`  
		Last Modified: Tue, 13 Jun 2023 02:20:45 GMT  
		Size: 63.0 MB (62950447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19e2eebba64d92ff46f76ed0da2c6d997a1a2fe28a4d5792bd31d7b150060d`  
		Last Modified: Wed, 14 Jun 2023 18:35:48 GMT  
		Size: 69.6 MB (69585508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566344bd284f71ea08eec859a54b1a952b8d9d22e8d36f9b16aa40da55b43bf3`  
		Last Modified: Thu, 22 Jun 2023 02:20:38 GMT  
		Size: 94.4 MB (94360420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f999fae17485df629d9230da6e087fd43d5c47310fdc2652fcd0e29d5eb953`  
		Last Modified: Thu, 22 Jun 2023 02:19:40 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:273bbb6f0ca1fbd893aa753975c40e7f163e576fa618ebb94f729166b66b8ac6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.0 MB (335011796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b572cac563bf2fa7aed0e6024a6a83e520291942e5e25c7946606acc5202e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:17:10 GMT
ADD file:016534815cb7d12cae071da7f55250eeaff3ebdc6c1e4689e32d50df1fb158db in / 
# Mon, 12 Jun 2023 23:17:12 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:27:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:08:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:08:51 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 18:08:51 GMT
ENV GOLANG_VERSION=1.20.5
# Thu, 22 Jun 2023 00:39:48 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz'; 			sha256='d7ec48cde0d3d2be2c69203bc3e0a44de8660b9c09a6e85c4732a3f7dc442612'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.5.linux-armv6l.tar.gz'; 			sha256='79d8210efd4390569912274a98dffc16eb85993cccdeef4d704e9b0dfd50743a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.5.linux-arm64.tar.gz'; 			sha256='aa2fab0a7da20213ff975fa7876a66d47b48351558d98851b87d1cfef4360d09'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.5.linux-386.tar.gz'; 			sha256='d394ac8fecf66812c78ffba7fb9a265bb1b9917564c7fd77f0edb0df6d5777a1'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.5.linux-ppc64le.tar.gz'; 			sha256='049b8ab07d34077b90c0642138e10207f6db14bdd1743ea994a21e228f8ca53d'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.5.linux-s390x.tar.gz'; 			sha256='bac14667f1217ccce1d2ef4e204687fe6191e6dc19a8870cfb81a41f78b04e48'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.5.src.tar.gz'; 		sha256='9a15c133ba2cfafe79652f4815b62e7cfc267f68df1b9454c6ab2a3ca8b96a88'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 22 Jun 2023 00:39:53 GMT
ENV GOPATH=/go
# Thu, 22 Jun 2023 00:39:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jun 2023 00:39:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 22 Jun 2023 00:39:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:622cd3709abdd2a8ae1c5270932d62e2474b25e69dbd2e143ebf083f3a8696aa`  
		Last Modified: Mon, 12 Jun 2023 23:23:39 GMT  
		Size: 53.5 MB (53536755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6494f6dc0238175097ef6b12f430652fda3d2d85972d141df00788a75d057a5b`  
		Last Modified: Tue, 13 Jun 2023 07:39:43 GMT  
		Size: 25.7 MB (25681431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b744ccb19960a6ec40bededbe48af365fe2a854c731f264b21053307eef9edc0`  
		Last Modified: Tue, 13 Jun 2023 07:40:11 GMT  
		Size: 69.6 MB (69569353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00df7417b48b2bdebb555a11845d91c25c0d78d753e2d1046c796d6df90ed9ce`  
		Last Modified: Wed, 14 Jun 2023 18:11:17 GMT  
		Size: 90.2 MB (90202460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1facaf457ccbd188f9d148c16e7cf42e3d512269f7c94025ed7894221bfcc571`  
		Last Modified: Thu, 22 Jun 2023 00:44:51 GMT  
		Size: 96.0 MB (96021641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f4c29380846113e6783c5b8c50c1c5b9a573cc2cc8e6f4e6dc7bf84b8fd804`  
		Last Modified: Thu, 22 Jun 2023 00:44:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:afb250fcac739a81c34e7dfd2ef8159641252f986122ec263e5cb11ecccb70a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304111151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830d0b44f3c5f8da8071dfca38d1cf556d4a31537bc68722508004b680714003`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:31:54 GMT
ADD file:0ad7ffbe777e5367ad6dcbb4a182e1d578739aa7a4853f82f21bd71d824de7ae in / 
# Tue, 04 Jul 2023 01:31:56 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 12:47:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 12:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:07:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:07:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:09:02 GMT
ENV GOLANG_VERSION=1.20.5
# Tue, 04 Jul 2023 20:09:14 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz'; 			sha256='d7ec48cde0d3d2be2c69203bc3e0a44de8660b9c09a6e85c4732a3f7dc442612'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.5.linux-armv6l.tar.gz'; 			sha256='79d8210efd4390569912274a98dffc16eb85993cccdeef4d704e9b0dfd50743a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.5.linux-arm64.tar.gz'; 			sha256='aa2fab0a7da20213ff975fa7876a66d47b48351558d98851b87d1cfef4360d09'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.5.linux-386.tar.gz'; 			sha256='d394ac8fecf66812c78ffba7fb9a265bb1b9917564c7fd77f0edb0df6d5777a1'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.5.linux-ppc64le.tar.gz'; 			sha256='049b8ab07d34077b90c0642138e10207f6db14bdd1743ea994a21e228f8ca53d'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.5.linux-s390x.tar.gz'; 			sha256='bac14667f1217ccce1d2ef4e204687fe6191e6dc19a8870cfb81a41f78b04e48'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.5.src.tar.gz'; 		sha256='9a15c133ba2cfafe79652f4815b62e7cfc267f68df1b9454c6ab2a3ca8b96a88'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 04 Jul 2023 20:09:19 GMT
ENV GOPATH=/go
# Tue, 04 Jul 2023 20:09:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:09:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 04 Jul 2023 20:09:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ce9d001c0d31ec9b8072b1a9bd01771a10ea8ddfefa381cf9ce7e2d63538aaeb`  
		Last Modified: Tue, 04 Jul 2023 01:36:50 GMT  
		Size: 47.9 MB (47921709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024bda56b20d3018344098f67965337568b532ea03f09d87858a2bb5eae82bf7`  
		Last Modified: Tue, 04 Jul 2023 13:05:34 GMT  
		Size: 24.0 MB (24028793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da5b83dc971cc08c6baeb1ddd5fb5de06beefef83c0444c224b4e377d704705`  
		Last Modified: Tue, 04 Jul 2023 13:05:50 GMT  
		Size: 63.1 MB (63112809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa858ba6fa0e822053442a80cdd711942d14ef08060891ceb95b756e97b38fb3`  
		Last Modified: Tue, 04 Jul 2023 20:12:08 GMT  
		Size: 68.8 MB (68784821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeed76f4c831cca34b7c662dea95d1042eeb4d53f418ba8f0826dfb4edf381a0`  
		Last Modified: Tue, 04 Jul 2023 20:12:47 GMT  
		Size: 100.3 MB (100262864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8158164c3d122eef45eb6968b5511a90ea3f5cb2c61993d474af25d1e5df2580`  
		Last Modified: Tue, 04 Jul 2023 20:12:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
