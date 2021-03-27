## `golang:1-buster`

```console
$ docker pull golang@sha256:092d047f4a49510fe22998f24a2fb31e86727f46f168c134481456d67d0adaf3
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
$ docker pull golang@sha256:a23a7e49a820f9ae69df0fedf64f037cb15b004997effa93ec885e5032277bc1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317798991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb42f2526a722fa033cee51bc74088849afa3c22b843c33c4c7a5644414f5cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:13:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:14:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Mar 2021 04:14:00 GMT
ENV GOLANG_VERSION=1.16.2
# Sat, 13 Mar 2021 04:14:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 13 Mar 2021 04:14:12 GMT
ENV GOPATH=/go
# Sat, 13 Mar 2021 04:14:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Mar 2021 04:14:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 13 Mar 2021 04:14:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e499244fe254b6f980c82ea555f38e7a6527e5105545922005e88a6b81b01cac`  
		Last Modified: Fri, 12 Mar 2021 03:19:36 GMT  
		Size: 51.8 MB (51839506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec253d6133ed5960bf3c30c9d6e1e45b7fd705a5b4ec85d19aedcb00d1a0d0fa`  
		Last Modified: Sat, 13 Mar 2021 04:16:32 GMT  
		Size: 68.7 MB (68718988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07b05f2a22dca55194c797223a3b79a90f3be1243f806b7bb19c3e59247912f`  
		Last Modified: Sat, 13 Mar 2021 04:16:52 GMT  
		Size: 129.0 MB (129010367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f298da50fa054c31f3042de44a7c6a9d66e0c84b334977f2dcdef55a05aee192`  
		Last Modified: Sat, 13 Mar 2021 04:16:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:2a9f4ad66cd72dcd3139cd7837ff90749b0b4cff361ee2d7850493f5a19a4449
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269264279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ed4d9be1d8f8b16628e1583b96633c651e7df00c429ca72be206c65a36e8c1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:51:21 GMT
ADD file:8451124009ea487b77e0efd08279d813677a58a69c3e008efffe72456f5b4cd4 in / 
# Fri, 26 Mar 2021 07:51:25 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 09:10:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:10:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 09:11:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 21:40:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 21:40:21 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 21:40:21 GMT
ENV GOLANG_VERSION=1.16.2
# Fri, 26 Mar 2021 21:43:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 26 Mar 2021 21:44:04 GMT
ENV GOPATH=/go
# Fri, 26 Mar 2021 21:44:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 21:44:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 26 Mar 2021 21:44:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d38b01f6f9cb629c11a3283c08ac8942a1dabc09a0fd1cf882e144886c4d4c2d`  
		Last Modified: Fri, 26 Mar 2021 07:59:52 GMT  
		Size: 48.1 MB (48111655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b79e4c1a18c62ae0b58fc10bc99ce795232cbcd2cd5aacdda45457357bf228`  
		Last Modified: Fri, 26 Mar 2021 09:27:37 GMT  
		Size: 7.4 MB (7376462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4722e17bbecf50bf547d60af44536f7fe5f2e819630c31abb41dd678e56c40b0`  
		Last Modified: Fri, 26 Mar 2021 09:27:38 GMT  
		Size: 9.7 MB (9687518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02aedf3b95b92593cff7caa2a868b2adc310bc9b40c76820162cfb61f4467959`  
		Last Modified: Fri, 26 Mar 2021 09:28:02 GMT  
		Size: 49.6 MB (49573869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8c6b44e1cc417a3a769b7605face9fab010b05b3a27d17d3d4f30523879e25`  
		Last Modified: Fri, 26 Mar 2021 21:48:05 GMT  
		Size: 52.0 MB (52026857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f764966986cbadc03079cbfd377d12e7c49d4dfe7be6dc8d344ccd5bd6088fa4`  
		Last Modified: Fri, 26 Mar 2021 21:48:20 GMT  
		Size: 102.5 MB (102487762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3ff756b687856a7ce7a2c5d6ae45834902612b62502daaa3970ce780d7c708`  
		Last Modified: Fri, 26 Mar 2021 21:47:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:518f4376d0f19b7ec83cf62f20b81ea5447ad67802dbdcc2ed15f4fa521f845a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263154089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f53abc3dc8e95af6fd26734c7f144416c4232fac76c04094146b7c0daf668c5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:17:10 GMT
ADD file:b3e1f7b8ae0587f7850210420c8dd6da7fb60fa87c5863e6fe5a8bab1bdc7abc in / 
# Fri, 26 Mar 2021 11:17:11 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:22:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 13:23:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:58:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:58:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 08:58:53 GMT
ENV GOLANG_VERSION=1.16.2
# Sat, 27 Mar 2021 08:59:18 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 27 Mar 2021 08:59:23 GMT
ENV GOPATH=/go
# Sat, 27 Mar 2021 08:59:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 08:59:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 27 Mar 2021 08:59:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2703ee001e01b49055599d26cac8b1a472b75d8643e8a00ab281b97e3fe6aefd`  
		Last Modified: Fri, 26 Mar 2021 11:26:53 GMT  
		Size: 45.9 MB (45868006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f00d516e34bfa5a11e13fd33e0649e2bfcfa443418341f1cda5463ed8ee8046`  
		Last Modified: Fri, 26 Mar 2021 13:51:18 GMT  
		Size: 7.1 MB (7123912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac789cd7e7d8f8003e7ac6b6bbf96d3859a2318c4569114ccb686ffd779ce119`  
		Last Modified: Fri, 26 Mar 2021 13:51:16 GMT  
		Size: 9.3 MB (9343659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e16bfec3cd4c49403ed5b98e6216074d4f3c68c5dc09e6e12252c09aa8952cc`  
		Last Modified: Fri, 26 Mar 2021 13:52:03 GMT  
		Size: 47.4 MB (47356546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2477c5a65c38c8b37a3f5cf8396730d934898bc9917fb8cf4f06c467681312a3`  
		Last Modified: Sat, 27 Mar 2021 09:03:51 GMT  
		Size: 53.2 MB (53192930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a905e5530cd6a1f21f1a77e2efbee7253b5052c96470cb5de9b73ff1ac4e9048`  
		Last Modified: Sat, 27 Mar 2021 09:04:08 GMT  
		Size: 100.3 MB (100268882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a207e2aae99c0142c7cdc36b5b9901e292687f5b8f82be44f6ccd1ed3eff574f`  
		Last Modified: Sat, 27 Mar 2021 09:03:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e87ba3a72191846a32f464512073a561090d468f6d20dc68f9c4956ccf002c15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281201926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46b7c18e5b0d7c4a519c601a4de86416e44bbd4f6d64cd61b726d362340bea7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:30:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:42:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:42:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 19:42:40 GMT
ENV GOLANG_VERSION=1.16.2
# Fri, 12 Mar 2021 19:42:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 12 Mar 2021 19:43:01 GMT
ENV GOPATH=/go
# Fri, 12 Mar 2021 19:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 19:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 12 Mar 2021 19:43:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34041dfaf60ca49c213d83e89205fc2b7e222817c9728a4aa4f7d3f09d579c9`  
		Last Modified: Fri, 12 Mar 2021 02:43:54 GMT  
		Size: 52.2 MB (52165212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a0c71a3bdd5c6450fbd64071d7dc839a0bcb4b25cb4da17cee99e4003e08ba`  
		Last Modified: Fri, 12 Mar 2021 19:46:22 GMT  
		Size: 62.6 MB (62587002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a086f1a1722b807b6ba4f85da1d7425d05af6cdd2e1ea0b1fb5a26b60e49db32`  
		Last Modified: Fri, 12 Mar 2021 19:46:38 GMT  
		Size: 99.6 MB (99575048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d758bfab17e3578adf29f70b354ef2ac6daf97c874a46e1d2c5ffa47d3cc98c8`  
		Last Modified: Fri, 12 Mar 2021 19:46:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; 386

```console
$ docker pull golang@sha256:daa8b3a60ccb8d99362daf96c5906a8334b36bc1dacce149c354f9b7fc6461c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299591998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705ad584f5436214c2699cbbfabd68bcfe637354d7f21b99fe685fed54629711`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:52:53 GMT
ADD file:631a0d940844da5859827f6532f16d070023eb5af86b98b26e8225892a728141 in / 
# Fri, 26 Mar 2021 13:52:53 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 22:43:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 22:43:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 22:43:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 11:17:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 11:17:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 11:17:54 GMT
ENV GOLANG_VERSION=1.16.2
# Sat, 27 Mar 2021 11:18:07 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 27 Mar 2021 11:18:08 GMT
ENV GOPATH=/go
# Sat, 27 Mar 2021 11:18:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 11:18:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 27 Mar 2021 11:18:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94f8ae80c7bd585581d232dff8e781c1feaab54ea8d41718d95f0c1059908488`  
		Last Modified: Fri, 26 Mar 2021 14:00:56 GMT  
		Size: 51.2 MB (51160351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f4518622de265d7d3f5069177f5b74a159365d671532dd8008b136906f5bc2`  
		Last Modified: Fri, 26 Mar 2021 22:56:04 GMT  
		Size: 8.0 MB (7997773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a088421a3906a0c48a07e35676054ae4ed2982936d931624723f6d6c6c1e53e`  
		Last Modified: Fri, 26 Mar 2021 22:56:05 GMT  
		Size: 10.3 MB (10340027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46f38ff13dccaac573470e0e14ff2b88a265abe995ffaa863e5690821b2ee7a`  
		Last Modified: Fri, 26 Mar 2021 22:56:41 GMT  
		Size: 53.4 MB (53437511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b95ff9db7b4ad53917899eb88ea76bf3c305799d733751b43fd7c8ea546347`  
		Last Modified: Sat, 27 Mar 2021 11:21:52 GMT  
		Size: 73.6 MB (73597965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b40c4626543295303de8a0b40f241da3c2f44957323513678afebf76f2ebe2`  
		Last Modified: Sat, 27 Mar 2021 11:21:56 GMT  
		Size: 103.1 MB (103058215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b82194445bc93c46f146896722e1f691c3d6d44b03c3313951c29120cbe4b7c`  
		Last Modified: Sat, 27 Mar 2021 11:21:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; mips64le

```console
$ docker pull golang@sha256:46b29f5da42eae400fc15357bfed749f3a23fcc9c476ec099a4fd8709b553b09
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271348997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275786ee7539df658806b4f7104a6f3e03335111c9f748c852c8c4071581e4f7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 08:09:33 GMT
ADD file:24fb0f672b9623c5b9e2dc416fe7b91a485519962826a3def620d449c72052f6 in / 
# Fri, 26 Mar 2021 08:09:34 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 18:19:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 18:19:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 18:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 01:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 01:38:04 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 01:38:05 GMT
ENV GOLANG_VERSION=1.16.2
# Sat, 27 Mar 2021 01:46:02 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 27 Mar 2021 01:46:04 GMT
ENV GOPATH=/go
# Sat, 27 Mar 2021 01:46:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 01:46:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 27 Mar 2021 01:46:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:45e930b5a161529bdb19c7b813062fdeb224d004c1a5a716c817094752214853`  
		Last Modified: Fri, 26 Mar 2021 08:15:45 GMT  
		Size: 49.0 MB (49029292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ad80a148224544b054bd02d9e38d4e3faab1fd0f5fc036b1fef76b47e3fdee`  
		Last Modified: Fri, 26 Mar 2021 18:30:40 GMT  
		Size: 7.3 MB (7251155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f469c4240f70d8f2677ee4262b580b494bdb76348d54127726bc52308ef1504d`  
		Last Modified: Fri, 26 Mar 2021 18:30:37 GMT  
		Size: 10.0 MB (10016333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b70d7b92eec946956f610ecfb902f11596ce8501cb6ec617e44f7d3608ca5`  
		Last Modified: Fri, 26 Mar 2021 18:31:32 GMT  
		Size: 50.8 MB (50843088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2954fd334fbb3daa760b99809b464e369ca1a00be8c5bb8600453b3fbf6aca`  
		Last Modified: Sat, 27 Mar 2021 01:54:51 GMT  
		Size: 54.6 MB (54634686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2035fa0323cc724c1eefecb5f5e0a73da6d61dc1a0b934c5b7f463d0fe82e56d`  
		Last Modified: Sat, 27 Mar 2021 01:55:20 GMT  
		Size: 99.6 MB (99574317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92db20764f49641cd987b17a109e5d1b485efd75d7c3570a81cab5816591a4a7`  
		Last Modified: Sat, 27 Mar 2021 01:54:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:064377665c26ab428a83e1da3b76ed7496687e760f07d44f7d3ab60b11430dad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302267694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e45ac5680fa3310f22bfa19436d6f475c931a6c7c28221c31dfbe1852d977e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:31:55 GMT
ADD file:75cbd246f27dc871f6d43b196814d29950e19fbcf60ba31740b0f3b69d1eb5cf in / 
# Fri, 12 Mar 2021 02:32:10 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 11:02:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:03:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 11:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 02:26:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 02:26:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Mar 2021 02:26:45 GMT
ENV GOLANG_VERSION=1.16.2
# Sat, 13 Mar 2021 02:27:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 13 Mar 2021 02:27:42 GMT
ENV GOPATH=/go
# Sat, 13 Mar 2021 02:27:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Mar 2021 02:28:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 13 Mar 2021 02:28:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e82e55acc97d8fc958b57715031c249868ac5d8978e8d9f94ca4c15d553fe3cf`  
		Last Modified: Fri, 12 Mar 2021 02:44:17 GMT  
		Size: 54.1 MB (54136226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d7821ad6b4fb4c264f87306146cca85ae319c012535ca5ba869f297681f528`  
		Last Modified: Fri, 12 Mar 2021 12:00:12 GMT  
		Size: 8.3 MB (8271375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efadb27dbbd9968d195399537fc5c6be6627d842ed384ff4e9510632b9f24720`  
		Last Modified: Fri, 12 Mar 2021 12:00:09 GMT  
		Size: 10.7 MB (10727647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65fb57ad94f43eee037ef854e05c8d78064d228650a412c8cbf509359c99228`  
		Last Modified: Fri, 12 Mar 2021 12:02:19 GMT  
		Size: 57.5 MB (57456654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac5ab22b7e95f441d3508b3a27b8c2d834b3d529f3a85d9a0779557430be580`  
		Last Modified: Sat, 13 Mar 2021 02:32:05 GMT  
		Size: 73.6 MB (73624203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eab641465e4965fd5e63f8e9fc1a35cf27211c566c870bed8503bc0532cb708`  
		Last Modified: Sat, 13 Mar 2021 02:32:10 GMT  
		Size: 98.1 MB (98051433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dbde775eecd3117b139dbcc663c1cee4c51c9e3f13a05b9a72ced725ee3cd9`  
		Last Modified: Sat, 13 Mar 2021 02:31:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; s390x

```console
$ docker pull golang@sha256:e2b0d407401ec10264728be2f81b8282b2d88df1e7634c547634a11e5b1f0509
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277603372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f9049a8a3efd0104a7811cb7ef8a0263b77b9020c0dfe4e55343196ddd8beb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 10:53:31 GMT
ADD file:a8707fa1aa1620bd4a2cfb08af992575ed92583d76d9bc5cdf7512c966ef97ec in / 
# Fri, 26 Mar 2021 10:53:35 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:44:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:44:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 15:45:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 22:06:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 22:07:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 22:07:00 GMT
ENV GOLANG_VERSION=1.16.2
# Fri, 26 Mar 2021 22:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 26 Mar 2021 22:07:16 GMT
ENV GOPATH=/go
# Fri, 26 Mar 2021 22:07:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 22:07:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 26 Mar 2021 22:07:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1b0086a5cca01c7491d8c2f15dbad8cb1c1829a7d6d1edd7f8c3dd02be85f2b`  
		Last Modified: Fri, 26 Mar 2021 10:57:27 GMT  
		Size: 49.0 MB (48968913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b853ff3a647fb66a2e5b7307061cdfcb221462bf3a73b0a84e58f90ac3b881a`  
		Last Modified: Fri, 26 Mar 2021 15:55:02 GMT  
		Size: 7.4 MB (7399988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286674edc11eb23904d49908925aff4fe5babc031d3c022fff443a078dd87e21`  
		Last Modified: Fri, 26 Mar 2021 15:55:02 GMT  
		Size: 9.9 MB (9883250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62476e7ae0d7567aa0af0346254446c4959eb64b48882d260b31cdd605477fa`  
		Last Modified: Fri, 26 Mar 2021 15:55:21 GMT  
		Size: 51.4 MB (51380222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a79e3210f90831ffef1f05c93b5e83c300fde8d46ecb91c1885637f388a8fd`  
		Last Modified: Fri, 26 Mar 2021 22:08:34 GMT  
		Size: 56.8 MB (56788621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7688f7c043ad40c2f1084798e2d4f24c683003a771d13389b5e51c819e83a`  
		Last Modified: Fri, 26 Mar 2021 22:08:40 GMT  
		Size: 103.2 MB (103182223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7e11f19d86724330a774f3985bd1974778676ba4a23623fa7cc9376349cd9b`  
		Last Modified: Fri, 26 Mar 2021 22:08:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
