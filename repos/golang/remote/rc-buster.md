## `golang:rc-buster`

```console
$ docker pull golang@sha256:68d6ac224a876cffb6b80243ae95af3814c41150fe34e46c1eae5028af74f8da
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
$ docker pull golang@sha256:b511f2ad0c0fadf6fa12bfa8328cc9936cb9cacbfb7346d21028da56625f1d13
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323311866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50c1debe67e5d2f6aff077091f079cc1b33a0c6bd1503efb6b82e8b2d3caf2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:55:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:55:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:56:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 19:23:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 19:23:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 21:19:50 GMT
ENV GOLANG_VERSION=1.17beta1
# Thu, 10 Jun 2021 21:20:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17beta1.linux-amd64.tar.gz'; 			sha256='a479681705b65971f9db079bfce53c4393bfa241d952eb09de88fb40677d3c4c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17beta1.linux-armv6l.tar.gz'; 			sha256='f4ab69c75a1f9e43b07ca9a0bfdf68ca1e2b0b51d4ebfb8c79f60ed14629f4e6'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17beta1.linux-arm64.tar.gz'; 			sha256='ede56f79c5061146929ab4a128e8ee7bc713d141e87b3df4e0aa670938e128b3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17beta1.linux-386.tar.gz'; 			sha256='cebbf75985ba7e6f1a5b137916a6019685d52ecf36c262092ffc3f714cd85974'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17beta1.linux-ppc64le.tar.gz'; 			sha256='0a6e5034fcbd4b38642b56841a042135aec1e87f61258d2d70aafc0a667bdd11'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17beta1.linux-s390x.tar.gz'; 			sha256='3501d139a9433775001730f1d9c3fb60d7b93b969fe16bd80fc7387a3d5259b1'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17beta1.src.tar.gz'; 		sha256='02b8973725f9bc545955865576e8c8f6ca672312f69fd9e5549c25b0ce1d75f0'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Jun 2021 21:20:04 GMT
ENV GOPATH=/go
# Thu, 10 Jun 2021 21:20:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 21:20:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Jun 2021 21:20:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d62473a22dec9ffef056b2017968a9dc484c8f836fb6d79f46980b309e9138`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 7.8 MB (7832938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8962bc0fad55b13afedfeb6ad5cb06fd065461cf3e1ae4e7aeae5eeb17b179df`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 10.0 MB (9997157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d943ee54c1fa196b54ab9a6673174c66eea04cfa1a4ac5b0328b74f066a4d9`  
		Last Modified: Wed, 12 May 2021 02:05:07 GMT  
		Size: 51.8 MB (51841468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2253e6fbefa9189360a7818eb45effaed9bcb4ff631741a32609b39a2b2c1a2`  
		Last Modified: Wed, 12 May 2021 19:26:13 GMT  
		Size: 68.7 MB (68736689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d77ff980f1f3009329563d0c657bbf52224725820e468e8e34f3c1444b54f6`  
		Last Modified: Thu, 10 Jun 2021 21:33:25 GMT  
		Size: 134.5 MB (134470218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6620ae247f079535c741d56722385de331d6f9a60e354de61faf2c768ab7fec`  
		Last Modified: Thu, 10 Jun 2021 21:33:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:85c3662980ba5e0ecc5b18c4ed1129d660f4724e8c7048a809dd566397eed172
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272144823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3731f98f5a977507c3cd4fbe211ee7c1ca4b3ec2ce2aefd7adb927f7c40edf8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:54:57 GMT
ADD file:443be99157e29a4ccb29f5d0ffc9994ce41fb51c512815f76fec9e1fb4d5d8ba in / 
# Wed, 12 May 2021 00:55:00 GMT
CMD ["bash"]
# Thu, 27 May 2021 19:52:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 19:52:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 19:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:39:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:39:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 21:48:26 GMT
ENV GOLANG_VERSION=1.17beta1
# Thu, 10 Jun 2021 21:51:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17beta1.linux-amd64.tar.gz'; 			sha256='a479681705b65971f9db079bfce53c4393bfa241d952eb09de88fb40677d3c4c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17beta1.linux-armv6l.tar.gz'; 			sha256='f4ab69c75a1f9e43b07ca9a0bfdf68ca1e2b0b51d4ebfb8c79f60ed14629f4e6'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17beta1.linux-arm64.tar.gz'; 			sha256='ede56f79c5061146929ab4a128e8ee7bc713d141e87b3df4e0aa670938e128b3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17beta1.linux-386.tar.gz'; 			sha256='cebbf75985ba7e6f1a5b137916a6019685d52ecf36c262092ffc3f714cd85974'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17beta1.linux-ppc64le.tar.gz'; 			sha256='0a6e5034fcbd4b38642b56841a042135aec1e87f61258d2d70aafc0a667bdd11'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17beta1.linux-s390x.tar.gz'; 			sha256='3501d139a9433775001730f1d9c3fb60d7b93b969fe16bd80fc7387a3d5259b1'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17beta1.src.tar.gz'; 		sha256='02b8973725f9bc545955865576e8c8f6ca672312f69fd9e5549c25b0ce1d75f0'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Jun 2021 21:51:44 GMT
ENV GOPATH=/go
# Thu, 10 Jun 2021 21:51:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 21:51:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Jun 2021 21:51:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:db69af0c9ce605b61ac30d118d6c6ab4f8579b8c80e5469335f2108afa5d2c66`  
		Last Modified: Wed, 12 May 2021 01:09:52 GMT  
		Size: 48.2 MB (48150747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404ba73f5eb1dbb487e50a5cd752625acb36ffba758e241579e2cb88c3becaac`  
		Last Modified: Thu, 27 May 2021 20:04:54 GMT  
		Size: 7.4 MB (7376519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d6b363679cfa0fcdf5dc9c8564dd9eb369d8d776652cb414b2b23d621ae51`  
		Last Modified: Thu, 27 May 2021 20:04:54 GMT  
		Size: 9.7 MB (9687524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fed7877fa156e7f1cc5cf959724daf2f0db0041371f88494647de4950b987f`  
		Last Modified: Thu, 27 May 2021 20:05:29 GMT  
		Size: 49.6 MB (49575033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a70a9323ee0082c91dd17ba2104f4c01aa4afde922f472c7fa705c4ef7e098`  
		Last Modified: Thu, 27 May 2021 20:48:39 GMT  
		Size: 52.0 MB (52041787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cfb7b68ca7cec3bf35ab0b8c8a76cc64f68920ca7ed2388fd28456a01be234`  
		Last Modified: Thu, 10 Jun 2021 21:53:37 GMT  
		Size: 105.3 MB (105313058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94b030cd63a900285b925d42d6307c2ff6a71d020a3f0cc2a5ef6f8a3cb22c0`  
		Last Modified: Thu, 10 Jun 2021 21:53:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:a3b338a226d681ca8e25d1ae5e6c337b3d9d4a62b4b2dcfa205f776f936c2f02
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265944385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d882f86ea36adfb110de79c6fed09c0b9112be00142ce25286118ce0b7aa0caa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:02:10 GMT
ADD file:51a0472692adf18117444dc1f35d6eb3b4d6d672f28a7f6631f9d5d269b0b85d in / 
# Wed, 12 May 2021 01:02:15 GMT
CMD ["bash"]
# Thu, 27 May 2021 00:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:40:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 00:40:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 15:05:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 15:05:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 22:25:18 GMT
ENV GOLANG_VERSION=1.17beta1
# Thu, 10 Jun 2021 22:25:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17beta1.linux-amd64.tar.gz'; 			sha256='a479681705b65971f9db079bfce53c4393bfa241d952eb09de88fb40677d3c4c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17beta1.linux-armv6l.tar.gz'; 			sha256='f4ab69c75a1f9e43b07ca9a0bfdf68ca1e2b0b51d4ebfb8c79f60ed14629f4e6'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17beta1.linux-arm64.tar.gz'; 			sha256='ede56f79c5061146929ab4a128e8ee7bc713d141e87b3df4e0aa670938e128b3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17beta1.linux-386.tar.gz'; 			sha256='cebbf75985ba7e6f1a5b137916a6019685d52ecf36c262092ffc3f714cd85974'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17beta1.linux-ppc64le.tar.gz'; 			sha256='0a6e5034fcbd4b38642b56841a042135aec1e87f61258d2d70aafc0a667bdd11'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17beta1.linux-s390x.tar.gz'; 			sha256='3501d139a9433775001730f1d9c3fb60d7b93b969fe16bd80fc7387a3d5259b1'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17beta1.src.tar.gz'; 		sha256='02b8973725f9bc545955865576e8c8f6ca672312f69fd9e5549c25b0ce1d75f0'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Jun 2021 22:25:38 GMT
ENV GOPATH=/go
# Thu, 10 Jun 2021 22:25:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 22:25:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Jun 2021 22:25:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:89475607b1df9fc7eec7efe2fa845738a16cee3e92c1bb864c1f5a93b8303bc6`  
		Last Modified: Wed, 12 May 2021 01:18:49 GMT  
		Size: 45.9 MB (45916922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88447de5eb3eca4a1d96b6980b44d82ac19d121f6b77b826989f8d611fd001b0`  
		Last Modified: Thu, 27 May 2021 01:03:02 GMT  
		Size: 7.1 MB (7124249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25b14665fd0185f2f3b90a8d1825fc8ef9f330e1aea452f60fd70cdcfe99bf4`  
		Last Modified: Thu, 27 May 2021 01:03:02 GMT  
		Size: 9.3 MB (9343721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba65a331625e51ba8f0e1af07dcb97c0583204dda094b5da79672fdf554129c4`  
		Last Modified: Thu, 27 May 2021 01:03:40 GMT  
		Size: 47.4 MB (47356403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28c817b2d28b5d681af2625b1d016403efdb2680145a772baa567b9668da9f0`  
		Last Modified: Thu, 27 May 2021 15:18:15 GMT  
		Size: 53.2 MB (53205162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f00fe7a109ad617e336eaf18e917b692ada3c7a4e7f2f5aa5c1dd2cbed1212`  
		Last Modified: Thu, 10 Jun 2021 22:50:25 GMT  
		Size: 103.0 MB (102997773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebc6cbd400d745d4c96f006565963f2f8fe9d674cee991affbf3f7a183efed6`  
		Last Modified: Thu, 10 Jun 2021 22:49:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d972cfb8ad9c5f1aba288df92e7993e21c55eeb559392c7a4bff0d0fed374a3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284214595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72aacad20948023cb4483f7e19862b0e6eed28e5e94478000bcbc2813956046`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:24 GMT
ADD file:bc9eebfc439e3fbf9db01c98dc2448d9bededd394b893e397661227b81859dea in / 
# Tue, 22 Jun 2021 23:49:25 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 00:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 00:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 12:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 12:53:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 12:53:20 GMT
ENV GOLANG_VERSION=1.17beta1
# Wed, 23 Jun 2021 12:53:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17beta1.linux-amd64.tar.gz'; 			sha256='a479681705b65971f9db079bfce53c4393bfa241d952eb09de88fb40677d3c4c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17beta1.linux-armv6l.tar.gz'; 			sha256='f4ab69c75a1f9e43b07ca9a0bfdf68ca1e2b0b51d4ebfb8c79f60ed14629f4e6'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17beta1.linux-arm64.tar.gz'; 			sha256='ede56f79c5061146929ab4a128e8ee7bc713d141e87b3df4e0aa670938e128b3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17beta1.linux-386.tar.gz'; 			sha256='cebbf75985ba7e6f1a5b137916a6019685d52ecf36c262092ffc3f714cd85974'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17beta1.linux-ppc64le.tar.gz'; 			sha256='0a6e5034fcbd4b38642b56841a042135aec1e87f61258d2d70aafc0a667bdd11'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17beta1.linux-s390x.tar.gz'; 			sha256='3501d139a9433775001730f1d9c3fb60d7b93b969fe16bd80fc7387a3d5259b1'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17beta1.src.tar.gz'; 		sha256='02b8973725f9bc545955865576e8c8f6ca672312f69fd9e5549c25b0ce1d75f0'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 23 Jun 2021 12:53:32 GMT
ENV GOPATH=/go
# Wed, 23 Jun 2021 12:53:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 12:53:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Jun 2021 12:53:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:310b368da98207b4fd030cc969461bfba1ea7c73fc5da1f015e05570d3eb2510`  
		Last Modified: Tue, 22 Jun 2021 23:54:51 GMT  
		Size: 49.2 MB (49221986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86422c44ee005c4d5ccb0e2fa32685229207b712728cd4b8c0ef97174f079df7`  
		Last Modified: Wed, 23 Jun 2021 00:33:16 GMT  
		Size: 7.7 MB (7694715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137877e0c26a439a8954003b21876b6059de852c839631e8cf6fda5bd36434c`  
		Last Modified: Wed, 23 Jun 2021 00:33:17 GMT  
		Size: 10.0 MB (9984281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785171b903c4d81c5b7539417a7b05f4a9bc6a35840595233bf4e369d8aee387`  
		Last Modified: Wed, 23 Jun 2021 00:33:41 GMT  
		Size: 52.2 MB (52165169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31a19a8a6841af41513223b2701373734838fc000bd6928b9c55613c3c79d53`  
		Last Modified: Wed, 23 Jun 2021 12:58:51 GMT  
		Size: 62.6 MB (62615492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a908954429f10403d9153b8b7ef4f8b94609e5f330c9f74c817cfe0d553c5b1`  
		Last Modified: Wed, 23 Jun 2021 12:58:58 GMT  
		Size: 102.5 MB (102532797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57128cde34583b9c0e1645dea5427eb4ed24ec3d5fcb3ac30a0ce73c6588dbd0`  
		Last Modified: Wed, 23 Jun 2021 12:58:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; 386

```console
$ docker pull golang@sha256:70d98dddd6a6418b6d7e89ef6761d6ce237876f44a5848a9ea91ff0f4291393f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302101280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d7e1b6dabd42c19eac2e33bcaedc56b0dbc40ed673af9094a117ddcd17d381`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:39:33 GMT
ADD file:f823eb487fd44688b29f866d2c837da27f508db7fc1f19e4dc01dde9ea7c72c4 in / 
# Wed, 12 May 2021 00:39:34 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:09:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:09:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:09:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:27:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:27:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 21:38:36 GMT
ENV GOLANG_VERSION=1.17beta1
# Thu, 10 Jun 2021 21:38:51 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17beta1.linux-amd64.tar.gz'; 			sha256='a479681705b65971f9db079bfce53c4393bfa241d952eb09de88fb40677d3c4c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17beta1.linux-armv6l.tar.gz'; 			sha256='f4ab69c75a1f9e43b07ca9a0bfdf68ca1e2b0b51d4ebfb8c79f60ed14629f4e6'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17beta1.linux-arm64.tar.gz'; 			sha256='ede56f79c5061146929ab4a128e8ee7bc713d141e87b3df4e0aa670938e128b3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17beta1.linux-386.tar.gz'; 			sha256='cebbf75985ba7e6f1a5b137916a6019685d52ecf36c262092ffc3f714cd85974'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17beta1.linux-ppc64le.tar.gz'; 			sha256='0a6e5034fcbd4b38642b56841a042135aec1e87f61258d2d70aafc0a667bdd11'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17beta1.linux-s390x.tar.gz'; 			sha256='3501d139a9433775001730f1d9c3fb60d7b93b969fe16bd80fc7387a3d5259b1'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17beta1.src.tar.gz'; 		sha256='02b8973725f9bc545955865576e8c8f6ca672312f69fd9e5549c25b0ce1d75f0'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Jun 2021 21:38:51 GMT
ENV GOPATH=/go
# Thu, 10 Jun 2021 21:38:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 21:38:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Jun 2021 21:38:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:07a4b6b1756691e1f8a89eb64afc18fb9b4a0712eb810679a4b89b1b351f8e9b`  
		Last Modified: Wed, 12 May 2021 00:46:03 GMT  
		Size: 51.2 MB (51200034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2395b55871bdaf1f7143048f77c63000ab6412664b1ce49fe9a8602e496d1`  
		Last Modified: Wed, 12 May 2021 01:17:52 GMT  
		Size: 8.0 MB (7998534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106083f164cc6c516cf3c838e5ba0c6870172a26217bd766dac43b0ecc89ca3b`  
		Last Modified: Wed, 12 May 2021 01:17:53 GMT  
		Size: 10.3 MB (10339817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfd96379aaff5d0e0fbcadade17bc6dd9c9fce6e229d06bbcf028b432ef82d0`  
		Last Modified: Wed, 12 May 2021 01:18:19 GMT  
		Size: 53.4 MB (53438227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba526a5fe4a69af3e8e28c1d228fd8370432cae20f33bf2f0a8f54323d946aee`  
		Last Modified: Wed, 12 May 2021 17:31:15 GMT  
		Size: 73.6 MB (73597884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba316c335e7e370acea0c9e10a7d6a1a81764d1fbe4e692d1bf7d936a6f452`  
		Last Modified: Thu, 10 Jun 2021 22:14:47 GMT  
		Size: 105.5 MB (105526629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ec8227b1165e595ba67ed752c88d8897f910976ba41a40a6b4fcb123b3f3`  
		Last Modified: Thu, 10 Jun 2021 22:14:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; mips64le

```console
$ docker pull golang@sha256:6239124c48e43dc09446cc257d4d0186c571567bd772e8b5f4fd4738ac02a926
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274397019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b88a133402d939169c0867ffa46419483a78f8f8f0379cb1a1987f921fd7a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:09:17 GMT
ADD file:2e2c1e52b19e85e4299309ed75f088e727e316902a0dd39be198c41ced817b01 in / 
# Wed, 12 May 2021 01:09:18 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:58:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:58:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:59:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:09:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:09:04 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 21:07:24 GMT
ENV GOLANG_VERSION=1.17beta1
# Thu, 10 Jun 2021 21:17:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17beta1.linux-amd64.tar.gz'; 			sha256='a479681705b65971f9db079bfce53c4393bfa241d952eb09de88fb40677d3c4c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17beta1.linux-armv6l.tar.gz'; 			sha256='f4ab69c75a1f9e43b07ca9a0bfdf68ca1e2b0b51d4ebfb8c79f60ed14629f4e6'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17beta1.linux-arm64.tar.gz'; 			sha256='ede56f79c5061146929ab4a128e8ee7bc713d141e87b3df4e0aa670938e128b3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17beta1.linux-386.tar.gz'; 			sha256='cebbf75985ba7e6f1a5b137916a6019685d52ecf36c262092ffc3f714cd85974'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17beta1.linux-ppc64le.tar.gz'; 			sha256='0a6e5034fcbd4b38642b56841a042135aec1e87f61258d2d70aafc0a667bdd11'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17beta1.linux-s390x.tar.gz'; 			sha256='3501d139a9433775001730f1d9c3fb60d7b93b969fe16bd80fc7387a3d5259b1'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17beta1.src.tar.gz'; 		sha256='02b8973725f9bc545955865576e8c8f6ca672312f69fd9e5549c25b0ce1d75f0'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Jun 2021 21:17:14 GMT
ENV GOPATH=/go
# Thu, 10 Jun 2021 21:17:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 21:17:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Jun 2021 21:17:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e18ab78f0b7ce048045ffb547791aaa698db3869d1da87f71e538a7fd19f965`  
		Last Modified: Wed, 12 May 2021 01:15:53 GMT  
		Size: 49.1 MB (49081826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03651915a251d4aae832ea26b7e72a8d93c3b7bde9b9b309c4069e8de71798fe`  
		Last Modified: Wed, 12 May 2021 02:09:54 GMT  
		Size: 7.3 MB (7252462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc21a03fe417b31a222d86e092660202cc0fae5556a43581e06b7d6a7ae1849`  
		Last Modified: Wed, 12 May 2021 02:09:54 GMT  
		Size: 10.0 MB (10016363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0e8057c7976180c1276687f493d7ba1a8ef256364c51e7c518c539f03b9386`  
		Last Modified: Wed, 12 May 2021 02:10:45 GMT  
		Size: 50.8 MB (50845391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96614d650c8fef4a0dcd461fdcc1c392357450920cb3337b84af6bab0b400b85`  
		Last Modified: Wed, 12 May 2021 16:25:52 GMT  
		Size: 54.7 MB (54651519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aabd936d192cec847582244fc612643f0ef4b2d2a446d0b74cda39f7754b6cc`  
		Last Modified: Thu, 10 Jun 2021 21:18:57 GMT  
		Size: 102.5 MB (102549332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4f3c681db4bb0e7ce4c568e1ddfee56c39154299f117750ad5014037051f7a`  
		Last Modified: Thu, 10 Jun 2021 21:17:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:0842559089285dd1b1a5461adf17b2b0f782b3271b2cb7f1bf6ca22ae2834edb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.2 MB (305217752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d4d9c5fc4e947c3b004c246c4fb6967cd651d8144e79c157ca2b2ced58c880`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:34:15 GMT
ADD file:b714397b44737108500b0256abc9750626cfa28cc0bb52623b9a14bb0e2345fc in / 
# Wed, 12 May 2021 01:34:24 GMT
CMD ["bash"]
# Wed, 12 May 2021 03:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 03:37:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 03:42:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 19:14:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 19:14:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 21:18:03 GMT
ENV GOLANG_VERSION=1.17beta1
# Thu, 10 Jun 2021 21:18:42 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17beta1.linux-amd64.tar.gz'; 			sha256='a479681705b65971f9db079bfce53c4393bfa241d952eb09de88fb40677d3c4c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17beta1.linux-armv6l.tar.gz'; 			sha256='f4ab69c75a1f9e43b07ca9a0bfdf68ca1e2b0b51d4ebfb8c79f60ed14629f4e6'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17beta1.linux-arm64.tar.gz'; 			sha256='ede56f79c5061146929ab4a128e8ee7bc713d141e87b3df4e0aa670938e128b3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17beta1.linux-386.tar.gz'; 			sha256='cebbf75985ba7e6f1a5b137916a6019685d52ecf36c262092ffc3f714cd85974'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17beta1.linux-ppc64le.tar.gz'; 			sha256='0a6e5034fcbd4b38642b56841a042135aec1e87f61258d2d70aafc0a667bdd11'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17beta1.linux-s390x.tar.gz'; 			sha256='3501d139a9433775001730f1d9c3fb60d7b93b969fe16bd80fc7387a3d5259b1'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17beta1.src.tar.gz'; 		sha256='02b8973725f9bc545955865576e8c8f6ca672312f69fd9e5549c25b0ce1d75f0'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Jun 2021 21:18:50 GMT
ENV GOPATH=/go
# Thu, 10 Jun 2021 21:18:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 21:19:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Jun 2021 21:19:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bd4ac1330adf594df6c60d33ec5060c79833a8455e6cdb9f5ef2be33cb843845`  
		Last Modified: Wed, 12 May 2021 01:43:19 GMT  
		Size: 54.2 MB (54180124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb8ec8ba72b4c906c6a3b88324130a605cfda687a94ed75e901c7cd141492fb`  
		Last Modified: Wed, 12 May 2021 04:19:32 GMT  
		Size: 8.3 MB (8271865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46415d7d07194b30fe4845342dd9c5927deb73698c2cfe9a55c6417b98ed3855`  
		Last Modified: Wed, 12 May 2021 04:19:32 GMT  
		Size: 10.7 MB (10727703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443c274997562dde0054a5cc26e8bbee59190c34ea8b862e917569cfbee85b63`  
		Last Modified: Wed, 12 May 2021 04:20:12 GMT  
		Size: 57.5 MB (57457050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e6cf94b16ff06dc84fad4f21c7aaff73b114a55ee4233bf2ccb9417664dc80`  
		Last Modified: Wed, 12 May 2021 19:21:01 GMT  
		Size: 73.6 MB (73643497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b14a37c9b8c6855961dd5d105534bd1bf6d4190489ab504d260ec02be1adfaa`  
		Last Modified: Thu, 10 Jun 2021 21:38:35 GMT  
		Size: 100.9 MB (100937358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b0bb61a86f71f69e87da58abf34f8dca3a810ebb6d19f3b19934ced6f62e72`  
		Last Modified: Thu, 10 Jun 2021 21:36:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; s390x

```console
$ docker pull golang@sha256:866290130ec723f37e57782812db7a453046347f4b8786452c3d1cf6eccdf3cd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280164065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb0cbf3e91bc0d49983aa453ab2b4e5f38aa67d60f315f8cb9fc4ab04ffe26a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:42:13 GMT
ADD file:b935574081a3fbceb534880a35e5245e10c52a3b9d70224811e221b4c6254cfe in / 
# Tue, 22 Jun 2021 23:42:16 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:05:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 00:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 00:06:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 12:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 12:22:43 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 12:22:43 GMT
ENV GOLANG_VERSION=1.17beta1
# Wed, 23 Jun 2021 12:23:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17beta1.linux-amd64.tar.gz'; 			sha256='a479681705b65971f9db079bfce53c4393bfa241d952eb09de88fb40677d3c4c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17beta1.linux-armv6l.tar.gz'; 			sha256='f4ab69c75a1f9e43b07ca9a0bfdf68ca1e2b0b51d4ebfb8c79f60ed14629f4e6'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17beta1.linux-arm64.tar.gz'; 			sha256='ede56f79c5061146929ab4a128e8ee7bc713d141e87b3df4e0aa670938e128b3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17beta1.linux-386.tar.gz'; 			sha256='cebbf75985ba7e6f1a5b137916a6019685d52ecf36c262092ffc3f714cd85974'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17beta1.linux-ppc64le.tar.gz'; 			sha256='0a6e5034fcbd4b38642b56841a042135aec1e87f61258d2d70aafc0a667bdd11'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17beta1.linux-s390x.tar.gz'; 			sha256='3501d139a9433775001730f1d9c3fb60d7b93b969fe16bd80fc7387a3d5259b1'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17beta1.src.tar.gz'; 		sha256='02b8973725f9bc545955865576e8c8f6ca672312f69fd9e5549c25b0ce1d75f0'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 23 Jun 2021 12:23:07 GMT
ENV GOPATH=/go
# Wed, 23 Jun 2021 12:23:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 12:23:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Jun 2021 12:23:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2b8d113de06cefaa0768df3e10da0c3b8272e15922e18ea75b0bb4dee23b551d`  
		Last Modified: Tue, 22 Jun 2021 23:45:28 GMT  
		Size: 49.0 MB (49003924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de1b6d51a91a64482d6eabf778b8c4e433f7dc198440476d01d0dbb31aee4fe`  
		Last Modified: Wed, 23 Jun 2021 00:12:08 GMT  
		Size: 7.4 MB (7400480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64019084b252c52592ff8cab3bf20be9bab2801ea36e88025071f901f1cb38e`  
		Last Modified: Wed, 23 Jun 2021 00:12:08 GMT  
		Size: 9.9 MB (9882902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481cb3d9acd652b3fd56e606ff28a1bb48aa89be3365577a33d2cd35c908d867`  
		Last Modified: Wed, 23 Jun 2021 00:12:24 GMT  
		Size: 51.4 MB (51380256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed2826325580193e1f03df87cd7d0c20d5a324c45056157542eaec1654b5b8`  
		Last Modified: Wed, 23 Jun 2021 12:27:41 GMT  
		Size: 56.8 MB (56817772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470e345c468c1d07867d437681e7db2209f5578b714116d75f9c136a548233f7`  
		Last Modified: Wed, 23 Jun 2021 12:27:47 GMT  
		Size: 105.7 MB (105678575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7cfd464ebed356c8ec0d28c07160238860f048d1b27aa14b180d46b2f19a1`  
		Last Modified: Wed, 23 Jun 2021 12:27:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
