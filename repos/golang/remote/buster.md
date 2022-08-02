## `golang:buster`

```console
$ docker pull golang@sha256:691a58334576632f889194f2df09d7990fe850fad3628c93944250cdcd3d6fef
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

### `golang:buster` - linux; amd64

```console
$ docker pull golang@sha256:e954361140fcb6e886a700212ef8e49d1a53931b8132ac5c46437f175fe65873
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330823759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0a44337dca709211d6de6fd526b9763d128e627c17408f837441816425a824`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:20 GMT
ADD file:d738977543f4afc4c3040c6fca3e3f15388ec3b7263a29a6aa83f9a4bf05fed1 in / 
# Tue, 12 Jul 2022 01:20:21 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:49:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:49:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 23:55:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 23:55:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 16:20:08 GMT
ENV GOLANG_VERSION=1.18.5
# Mon, 01 Aug 2022 16:20:21 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.5.linux-amd64.tar.gz'; 			sha256='9e5de37f9c49942c601b191ac5fba404b868bfc21d446d6960acc12283d6e5f2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.5.linux-armv6l.tar.gz'; 			sha256='d5ac34ac5f060a5274319aa04b7b11e41b123bd7887d64efb5f44ead236957af'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.5.linux-arm64.tar.gz'; 			sha256='006f6622718212363fa1ff004a6ab4d87bbbe772ec5631bab7cac10be346e4f1'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.5.linux-386.tar.gz'; 			sha256='0c44f85d146c6f98c34e8ff436a42af22e90e36fe232d3d9d3101f23fd61362b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.5.linux-ppc64le.tar.gz'; 			sha256='2e37fb9c7cbaedd4e729492d658aa4cde821fc94117391a8105c13b25ca1c84b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.5.linux-s390x.tar.gz'; 			sha256='e3d536e7873639f85353e892444f83b14cb6670603961f215986ae8e28e8e07a'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.5.src.tar.gz'; 		sha256='9920d3306a1ac536cdd2c796d6cb3c54bc559c226fc3cc39c32f1e0bd7f50d2a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Mon, 01 Aug 2022 16:20:22 GMT
ENV GOPATH=/go
# Mon, 01 Aug 2022 16:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 16:20:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Mon, 01 Aug 2022 16:20:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:80b89a2b88b24e7be7c8038e2cbff99ad4fd2f07ad914da4bab80dabaadf8a99`  
		Last Modified: Tue, 12 Jul 2022 01:24:55 GMT  
		Size: 50.4 MB (50440555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0405f798f5b335d83b02371187f3be0ce2092aa0c6b6178ff11290ee6a14c9`  
		Last Modified: Tue, 12 Jul 2022 02:56:14 GMT  
		Size: 7.9 MB (7856888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab80b2b0494ab26b41941fb73a028292e2e5d2070c56b3488e890eda20e04641`  
		Last Modified: Tue, 12 Jul 2022 02:56:14 GMT  
		Size: 10.0 MB (9998095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb827974c1cb152eae96a7b67abce3afa75353dec7790c0c07fdbb8906925921`  
		Last Modified: Tue, 12 Jul 2022 02:56:31 GMT  
		Size: 51.8 MB (51843739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107910070fddb285b7efcd0059371a3e6390693a973af12e3dc7588fa1d4630e`  
		Last Modified: Wed, 13 Jul 2022 00:09:17 GMT  
		Size: 68.8 MB (68828758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2680a618b10da175cbb4774513729fcba23c8bc3c24c91e5c064149607e00810`  
		Last Modified: Mon, 01 Aug 2022 16:29:39 GMT  
		Size: 141.9 MB (141855570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802b12f6e0a4efd60cbf5aad8545d82940fe3b671b0b849cf384cc45053aa024`  
		Last Modified: Mon, 01 Aug 2022 16:29:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:f42a2031c0ba5272b5316af38fccc941556e020f234f5fd3579cf0ec47342d32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279252805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b0728a4f03bc7bcc3219c22b4718900ad5a06344548e7ec735fc6cf7315de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:51:06 GMT
ADD file:46ca1be3e2e70869adc2c2213ad21ac3c743f1c7c0bbec927f855a82888f603d in / 
# Tue, 12 Jul 2022 00:51:07 GMT
CMD ["bash"]
# Wed, 27 Jul 2022 19:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Jul 2022 19:56:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Jul 2022 19:57:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 07:54:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 07:54:36 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 16:54:26 GMT
ENV GOLANG_VERSION=1.18.5
# Mon, 01 Aug 2022 17:01:44 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.5.linux-amd64.tar.gz'; 			sha256='9e5de37f9c49942c601b191ac5fba404b868bfc21d446d6960acc12283d6e5f2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.5.linux-armv6l.tar.gz'; 			sha256='d5ac34ac5f060a5274319aa04b7b11e41b123bd7887d64efb5f44ead236957af'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.5.linux-arm64.tar.gz'; 			sha256='006f6622718212363fa1ff004a6ab4d87bbbe772ec5631bab7cac10be346e4f1'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.5.linux-386.tar.gz'; 			sha256='0c44f85d146c6f98c34e8ff436a42af22e90e36fe232d3d9d3101f23fd61362b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.5.linux-ppc64le.tar.gz'; 			sha256='2e37fb9c7cbaedd4e729492d658aa4cde821fc94117391a8105c13b25ca1c84b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.5.linux-s390x.tar.gz'; 			sha256='e3d536e7873639f85353e892444f83b14cb6670603961f215986ae8e28e8e07a'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.5.src.tar.gz'; 		sha256='9920d3306a1ac536cdd2c796d6cb3c54bc559c226fc3cc39c32f1e0bd7f50d2a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Mon, 01 Aug 2022 17:01:45 GMT
ENV GOPATH=/go
# Mon, 01 Aug 2022 17:01:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 17:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Mon, 01 Aug 2022 17:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:83500cf45b6520b8ee0db35bb2065dcec25da5fca7b08fdb211039411146182b`  
		Last Modified: Tue, 12 Jul 2022 01:03:49 GMT  
		Size: 48.2 MB (48160548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3614dbc8455f283a03bbfe3df1fdec54f70177c8a2a7471eb91ee4d0b7868470`  
		Last Modified: Wed, 27 Jul 2022 20:08:49 GMT  
		Size: 7.4 MB (7401174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690635105de975fa2ba9c9de6bd3d35669dc154872bbec26d9f0669035ff8473`  
		Last Modified: Wed, 27 Jul 2022 20:08:50 GMT  
		Size: 9.7 MB (9688645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbb334edc1b145841273d75ba0c7f9a7ddaed304a3bb5f7428a8b00d9faf0a1`  
		Last Modified: Wed, 27 Jul 2022 20:09:21 GMT  
		Size: 49.6 MB (49582756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2090a91f6b13b6f4f17a5194cb96bef7f3a52a0d27f79b8f7feeb211e439c0`  
		Last Modified: Thu, 28 Jul 2022 08:43:58 GMT  
		Size: 52.1 MB (52133711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cda4c6f4508a79554a34ad3411b1bbcf0992d714cba7fbbfa018fbee9dc82da`  
		Last Modified: Mon, 01 Aug 2022 17:21:22 GMT  
		Size: 112.3 MB (112285815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64992783c909791079b179f959b763d99b6f377f2d98afcb66562d17efa869db`  
		Last Modified: Mon, 01 Aug 2022 17:20:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:462d11013fe1fd6576a5b63bb6f427201aee05864a3ce1fbb4ff27a95a16e7f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273180268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98b05726fcab0f26e1cbb3073883359b434b0705f06d9f0ec9547907ee580f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:00:25 GMT
ADD file:8795228d7a914d37160bb846066961f7c4c5f5da1452e6ae888a2a766cd8739f in / 
# Tue, 12 Jul 2022 01:00:26 GMT
CMD ["bash"]
# Thu, 28 Jul 2022 13:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 13:28:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 28 Jul 2022 13:29:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 29 Jul 2022 14:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Jul 2022 14:49:12 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 16:58:56 GMT
ENV GOLANG_VERSION=1.18.5
# Mon, 01 Aug 2022 16:59:22 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.5.linux-amd64.tar.gz'; 			sha256='9e5de37f9c49942c601b191ac5fba404b868bfc21d446d6960acc12283d6e5f2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.5.linux-armv6l.tar.gz'; 			sha256='d5ac34ac5f060a5274319aa04b7b11e41b123bd7887d64efb5f44ead236957af'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.5.linux-arm64.tar.gz'; 			sha256='006f6622718212363fa1ff004a6ab4d87bbbe772ec5631bab7cac10be346e4f1'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.5.linux-386.tar.gz'; 			sha256='0c44f85d146c6f98c34e8ff436a42af22e90e36fe232d3d9d3101f23fd61362b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.5.linux-ppc64le.tar.gz'; 			sha256='2e37fb9c7cbaedd4e729492d658aa4cde821fc94117391a8105c13b25ca1c84b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.5.linux-s390x.tar.gz'; 			sha256='e3d536e7873639f85353e892444f83b14cb6670603961f215986ae8e28e8e07a'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.5.src.tar.gz'; 		sha256='9920d3306a1ac536cdd2c796d6cb3c54bc559c226fc3cc39c32f1e0bd7f50d2a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Mon, 01 Aug 2022 16:59:23 GMT
ENV GOPATH=/go
# Mon, 01 Aug 2022 16:59:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 16:59:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Mon, 01 Aug 2022 16:59:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13036b2c6f13fd64780f7786c065cc2f0788024adbc684878bc4e33285ffcd1e`  
		Last Modified: Tue, 12 Jul 2022 01:13:22 GMT  
		Size: 45.9 MB (45915505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ee655d152d3acb35f3825891e9643f3691ede0af3d9d3d2148308272ad147e`  
		Last Modified: Thu, 28 Jul 2022 13:54:29 GMT  
		Size: 7.1 MB (7145473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69443875e8fdb06680327c732654bbfa6b479a256d0d865012b3f931609bd0f3`  
		Last Modified: Thu, 28 Jul 2022 13:54:29 GMT  
		Size: 9.3 MB (9344322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bdfec5c03781bcb3c6813122f21d30df45bbedb3c172824b93ddba76a9bfe0`  
		Last Modified: Thu, 28 Jul 2022 13:54:59 GMT  
		Size: 47.4 MB (47359742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4d441ffab1f9a42248b30a07cc9825e2667026444978cbd62cbb2ed02bac7d`  
		Last Modified: Fri, 29 Jul 2022 15:14:14 GMT  
		Size: 53.3 MB (53291757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bb4fb73f32e75ce5a68dbf90fc463033feca6819a966fc557f6f1aa78405a1`  
		Last Modified: Mon, 01 Aug 2022 17:34:39 GMT  
		Size: 110.1 MB (110123314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a162d3e794169365173af709d8941cbbe9bd05eaa021acbbaaaf5bb0379294`  
		Last Modified: Mon, 01 Aug 2022 17:34:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2a3ddd7a95ece6ba52a9dd26a917a3aa11ac93f4cc20ddfaedb711ffdbf9f788
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290348353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f852465b0db9d165b7fcc49d0485a6fe3a39a0bd53eaeb850e529546634577c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:46 GMT
ADD file:ea39534c5e9a548d7938f6b0e2459383caaf3906f3cc5eafe8bf66053b19f2d5 in / 
# Tue, 12 Jul 2022 00:40:47 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:34:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:35:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 21:22:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 21:22:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 16:40:45 GMT
ENV GOLANG_VERSION=1.18.5
# Mon, 01 Aug 2022 16:40:57 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.5.linux-amd64.tar.gz'; 			sha256='9e5de37f9c49942c601b191ac5fba404b868bfc21d446d6960acc12283d6e5f2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.5.linux-armv6l.tar.gz'; 			sha256='d5ac34ac5f060a5274319aa04b7b11e41b123bd7887d64efb5f44ead236957af'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.5.linux-arm64.tar.gz'; 			sha256='006f6622718212363fa1ff004a6ab4d87bbbe772ec5631bab7cac10be346e4f1'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.5.linux-386.tar.gz'; 			sha256='0c44f85d146c6f98c34e8ff436a42af22e90e36fe232d3d9d3101f23fd61362b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.5.linux-ppc64le.tar.gz'; 			sha256='2e37fb9c7cbaedd4e729492d658aa4cde821fc94117391a8105c13b25ca1c84b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.5.linux-s390x.tar.gz'; 			sha256='e3d536e7873639f85353e892444f83b14cb6670603961f215986ae8e28e8e07a'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.5.src.tar.gz'; 		sha256='9920d3306a1ac536cdd2c796d6cb3c54bc559c226fc3cc39c32f1e0bd7f50d2a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Mon, 01 Aug 2022 16:40:58 GMT
ENV GOPATH=/go
# Mon, 01 Aug 2022 16:40:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 16:41:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Mon, 01 Aug 2022 16:41:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:891a1587d3644a8b4b6dab3726ef380a725a0e19bfbf0eac02a275f711985862`  
		Last Modified: Tue, 12 Jul 2022 00:46:46 GMT  
		Size: 49.2 MB (49228928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5d1ed6a27dab15e77b7afa9c8697a170f017a73ec9ea8f3f00d5f322e1d3ab`  
		Last Modified: Tue, 12 Jul 2022 02:43:49 GMT  
		Size: 7.7 MB (7720027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186afd5d5e89c602b988d31dd5210c9e3c19435f849f6cc4a6a22a2388e83cf`  
		Last Modified: Tue, 12 Jul 2022 02:43:46 GMT  
		Size: 9.8 MB (9768648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5359768b018a374b04e8bf19e97c814527cb448f87c25de12fbabbb2ff3556d`  
		Last Modified: Tue, 12 Jul 2022 02:44:07 GMT  
		Size: 52.2 MB (52174846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa18f8501e4d284a9ce0729c6bb2aea70693faccddb329e9852ab4280adf3ab`  
		Last Modified: Tue, 12 Jul 2022 21:27:48 GMT  
		Size: 62.5 MB (62470498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f5c9c69531fbadd75500f4cff64131fc6e43c82ec683658e56005d1248046c`  
		Last Modified: Mon, 01 Aug 2022 16:50:44 GMT  
		Size: 109.0 MB (108985281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67832404757528a38ce2c6a2e2cc1adcd9c45d2af7c52331f5a4dd6333caf10c`  
		Last Modified: Mon, 01 Aug 2022 16:50:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; 386

```console
$ docker pull golang@sha256:402a572437dcb066cb120b94ef9ef44dd02fe84e1b253f7fb16e4ae54542e1bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309241646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f97a652f5e323e3f1ef75666d9d3dc6ac7c6f3f75a079ad8c2efea3397f68d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:31 GMT
ADD file:a25646092eaa55ba1e77da8bf292a71c17f8f54e6fa7a3cc057a8bd7d2febd63 in / 
# Tue, 02 Aug 2022 00:39:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:10:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:10:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:11:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:29:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:29:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:30:40 GMT
ENV GOLANG_VERSION=1.18.5
# Tue, 02 Aug 2022 16:30:56 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.5.linux-amd64.tar.gz'; 			sha256='9e5de37f9c49942c601b191ac5fba404b868bfc21d446d6960acc12283d6e5f2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.5.linux-armv6l.tar.gz'; 			sha256='d5ac34ac5f060a5274319aa04b7b11e41b123bd7887d64efb5f44ead236957af'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.5.linux-arm64.tar.gz'; 			sha256='006f6622718212363fa1ff004a6ab4d87bbbe772ec5631bab7cac10be346e4f1'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.5.linux-386.tar.gz'; 			sha256='0c44f85d146c6f98c34e8ff436a42af22e90e36fe232d3d9d3101f23fd61362b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.5.linux-ppc64le.tar.gz'; 			sha256='2e37fb9c7cbaedd4e729492d658aa4cde821fc94117391a8105c13b25ca1c84b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.5.linux-s390x.tar.gz'; 			sha256='e3d536e7873639f85353e892444f83b14cb6670603961f215986ae8e28e8e07a'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.5.src.tar.gz'; 		sha256='9920d3306a1ac536cdd2c796d6cb3c54bc559c226fc3cc39c32f1e0bd7f50d2a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 02 Aug 2022 16:30:57 GMT
ENV GOPATH=/go
# Tue, 02 Aug 2022 16:30:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:31:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Aug 2022 16:31:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:87423d7294b9d02dc4a6174f8947a28436937897c107e94249f27f8c987b91b5`  
		Last Modified: Tue, 02 Aug 2022 00:45:43 GMT  
		Size: 51.2 MB (51204266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ca86ab44db76ba51c2d76e29ec6f2a19a2b03060e0b6da3e4231c3180697e1`  
		Last Modified: Tue, 02 Aug 2022 01:25:38 GMT  
		Size: 8.0 MB (8022888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0164e37a3da34d457fecf12a96b86a0e0d31d0b8c3887c0f39d967de254add3f`  
		Last Modified: Tue, 02 Aug 2022 01:25:38 GMT  
		Size: 10.1 MB (10123381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4de0ffd612da4ff4187c1967f85b741a05492de87bb37a199340d32ec6d464`  
		Last Modified: Tue, 02 Aug 2022 01:26:02 GMT  
		Size: 53.4 MB (53442974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991c088ab48df3b3430b317802182948b159e48e2ecd050ec26028c5c3168ae8`  
		Last Modified: Tue, 02 Aug 2022 16:34:32 GMT  
		Size: 73.5 MB (73463902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79a349e589c79eca96824bd4953153fc46438f93e2a4c6a47f3a09c603d49b5`  
		Last Modified: Tue, 02 Aug 2022 16:35:42 GMT  
		Size: 113.0 MB (112984108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b0cc456d2747c109bf3af185db70310435edb056f144087d33b3c3b55cb2e6`  
		Last Modified: Tue, 02 Aug 2022 16:35:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; mips64le

```console
$ docker pull golang@sha256:a6e3a053d0a06d4d002b6c3e13fd7a222b3538876e0cc5a341d7733ae62c990c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279984378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d68818594181acb7e8d6d36a959fb42b25cb2841134916fbb87e4f199bc7edb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 04:41:32 GMT
ADD file:8ae876ce5db0069235a78103d9a680e349fc6b910a6111ea49467d374abbfc60 in / 
# Tue, 12 Jul 2022 04:41:37 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:18:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 06:20:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 00:50:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 00:50:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 19:13:35 GMT
ENV GOLANG_VERSION=1.18.5
# Mon, 01 Aug 2022 19:25:12 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.5.linux-amd64.tar.gz'; 			sha256='9e5de37f9c49942c601b191ac5fba404b868bfc21d446d6960acc12283d6e5f2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.5.linux-armv6l.tar.gz'; 			sha256='d5ac34ac5f060a5274319aa04b7b11e41b123bd7887d64efb5f44ead236957af'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.5.linux-arm64.tar.gz'; 			sha256='006f6622718212363fa1ff004a6ab4d87bbbe772ec5631bab7cac10be346e4f1'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.5.linux-386.tar.gz'; 			sha256='0c44f85d146c6f98c34e8ff436a42af22e90e36fe232d3d9d3101f23fd61362b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.5.linux-ppc64le.tar.gz'; 			sha256='2e37fb9c7cbaedd4e729492d658aa4cde821fc94117391a8105c13b25ca1c84b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.5.linux-s390x.tar.gz'; 			sha256='e3d536e7873639f85353e892444f83b14cb6670603961f215986ae8e28e8e07a'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.5.src.tar.gz'; 		sha256='9920d3306a1ac536cdd2c796d6cb3c54bc559c226fc3cc39c32f1e0bd7f50d2a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Mon, 01 Aug 2022 19:25:20 GMT
ENV GOPATH=/go
# Mon, 01 Aug 2022 19:25:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 19:25:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Mon, 01 Aug 2022 19:25:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f63d44b039884b9b81e12964f9b3c96fb7d550431e7bb657b94e25e0aaa6bb37`  
		Last Modified: Tue, 12 Jul 2022 04:52:25 GMT  
		Size: 49.1 MB (49073132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c7a5d202e81fdd1d4ce140e78b454956f14227f4349a35cd40690c076022f3`  
		Last Modified: Tue, 12 Jul 2022 06:43:42 GMT  
		Size: 7.3 MB (7273075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb7b23ca08db2ded7c067fb3a76ba6a87e04788fafc9d03045c18ed1b73631b`  
		Last Modified: Tue, 12 Jul 2022 06:43:43 GMT  
		Size: 9.8 MB (9801031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c96b7a7a2661117b397129ea53ebb97213b2398e5ee07a56031b2ea06fdd9e1`  
		Last Modified: Tue, 12 Jul 2022 06:44:30 GMT  
		Size: 50.9 MB (50861855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c098f17e65fb4e34b83b7d6f7aac54139eeb04169f4e7a59283c25890faff3a`  
		Last Modified: Wed, 13 Jul 2022 01:53:57 GMT  
		Size: 54.5 MB (54520209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd891a769fd942a89e2d37f7deefe6453b4d448b6c5aef0133d19efac3f0f63`  
		Last Modified: Mon, 01 Aug 2022 19:50:37 GMT  
		Size: 108.5 MB (108454950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd470f86dc965911bc126e65da7f42ed0dffa089a641ba9a3839e03175ecb15`  
		Last Modified: Mon, 01 Aug 2022 19:49:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; ppc64le

```console
$ docker pull golang@sha256:15b293b2860535fad0bb446c4704d200e4cf8c38a18f77057620c0f232774d5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313391185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81676fc2d80553807265fe4c96b2f7ae54a98ac364593ac00af2fb2cc228f7bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:48 GMT
ADD file:2148d05c090aaf9547831ad92d0e8afca3df183ef38c21db2a5b8962fcc3bfa0 in / 
# Tue, 12 Jul 2022 01:25:53 GMT
CMD ["bash"]
# Tue, 26 Jul 2022 22:44:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 22:45:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 26 Jul 2022 22:46:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Jul 2022 22:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Jul 2022 22:23:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 16:17:51 GMT
ENV GOLANG_VERSION=1.18.5
# Mon, 01 Aug 2022 16:18:14 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.5.linux-amd64.tar.gz'; 			sha256='9e5de37f9c49942c601b191ac5fba404b868bfc21d446d6960acc12283d6e5f2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.5.linux-armv6l.tar.gz'; 			sha256='d5ac34ac5f060a5274319aa04b7b11e41b123bd7887d64efb5f44ead236957af'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.5.linux-arm64.tar.gz'; 			sha256='006f6622718212363fa1ff004a6ab4d87bbbe772ec5631bab7cac10be346e4f1'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.5.linux-386.tar.gz'; 			sha256='0c44f85d146c6f98c34e8ff436a42af22e90e36fe232d3d9d3101f23fd61362b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.5.linux-ppc64le.tar.gz'; 			sha256='2e37fb9c7cbaedd4e729492d658aa4cde821fc94117391a8105c13b25ca1c84b'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.5.linux-s390x.tar.gz'; 			sha256='e3d536e7873639f85353e892444f83b14cb6670603961f215986ae8e28e8e07a'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.5.src.tar.gz'; 		sha256='9920d3306a1ac536cdd2c796d6cb3c54bc559c226fc3cc39c32f1e0bd7f50d2a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Mon, 01 Aug 2022 16:18:18 GMT
ENV GOPATH=/go
# Mon, 01 Aug 2022 16:18:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Aug 2022 16:18:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Mon, 01 Aug 2022 16:18:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:985c65736f23a90bf354a992729a4278b1841d9385b35f881ba5b8293ce58b29`  
		Last Modified: Tue, 12 Jul 2022 01:36:56 GMT  
		Size: 54.2 MB (54177075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7a789c037c1213028caf90471958a150307f11fa83385599382efd4359871`  
		Last Modified: Tue, 26 Jul 2022 23:49:47 GMT  
		Size: 8.3 MB (8293658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b74f28090e08e85a0bc514eff519f0a818a4ba5ba4a35fa902374b14b9ce9e0`  
		Last Modified: Tue, 26 Jul 2022 23:49:47 GMT  
		Size: 10.7 MB (10728735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1ca673ff0f16fe67764a8d7e4e7b354d3eb7a42b63153637583a5ff2127f40`  
		Last Modified: Tue, 26 Jul 2022 23:50:15 GMT  
		Size: 57.5 MB (57457451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3110ca297fc8cc8fb049a5914ee0ffbb09db92e0b5e424d9bd9199da039f7064`  
		Last Modified: Wed, 27 Jul 2022 22:46:49 GMT  
		Size: 73.7 MB (73733993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28950f04e6bcc96eb2d661bc9d4ba8a343a6bf5cf7bc228e908bb7b755b6163`  
		Last Modified: Mon, 01 Aug 2022 16:33:49 GMT  
		Size: 109.0 MB (109000117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c3162d544a49dc89ceb44be1370872995a46f4f09fe1fe4c7e4587b5c28842`  
		Last Modified: Mon, 01 Aug 2022 16:33:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; s390x

```console
$ docker pull golang@sha256:67a4cf0187acdb92fb78f325aa81d55378575ead743e8409662c06a736bfbb87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293571199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5c0139a3773026f33c41287b200be43d8c3b681e0d5680bf985463b5f383b5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:39 GMT
ADD file:d4184c5029732fe05023927be89b0c768483920c072c2069f92b3f4912c1c09b in / 
# Tue, 02 Aug 2022 00:42:41 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:10:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:10:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:10:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:31:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:31:19 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 18:31:19 GMT
ENV GOLANG_VERSION=1.19
# Tue, 02 Aug 2022 18:31:35 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.linux-amd64.tar.gz'; 			sha256='464b6b66591f6cf055bc5df90a9750bf5fbc9d038722bb84a9d56a2bea974be6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.linux-armv6l.tar.gz'; 			sha256='25197c7d70c6bf2b34d7d7c29a2ff92ba1c393f0fb395218f1147aac2948fb93'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.linux-arm64.tar.gz'; 			sha256='efa97fac9574fc6ef6c9ff3e3758fb85f1439b046573bf434cccb5e012bd00c8'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.linux-386.tar.gz'; 			sha256='6f721fa3e8f823827b875b73579d8ceadd9053ad1db8eaa2393c084865fb4873'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.linux-ppc64le.tar.gz'; 			sha256='92bf5aa598a01b279d03847c32788a3a7e0a247a029dedb7c759811c2a4241fc'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.linux-s390x.tar.gz'; 			sha256='58723eb8e3c7b9e8f5e97b2d38ace8fd62d9e5423eaa6cdb7ffe5f881cb11875'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.src.tar.gz'; 		sha256='9419cc70dc5a2523f29a77053cafff658ed21ef3561d9b6b020280ebceab28b9'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 02 Aug 2022 18:31:40 GMT
ENV GOPATH=/go
# Tue, 02 Aug 2022 18:31:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 18:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 02 Aug 2022 18:31:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8031e15331a0dfcc3509ff9e409d7bbbf567a40367f9eff78effb21b904d39ba`  
		Last Modified: Tue, 02 Aug 2022 00:48:16 GMT  
		Size: 49.0 MB (49007278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f3cfff1171566bc4507fbae110f76801339a99608218a65aa7c6eb9e99233a`  
		Last Modified: Tue, 02 Aug 2022 01:36:08 GMT  
		Size: 7.4 MB (7423882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c4fc1114e3b423bba8330a810105ed3b4c8cb807e853ca0fccdfac0b580ffd`  
		Last Modified: Tue, 02 Aug 2022 01:36:08 GMT  
		Size: 9.9 MB (9884760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc3c137faa880b9f1ba62f3a53f147bccc22fd4106874528df4d25714e6a767`  
		Last Modified: Tue, 02 Aug 2022 01:36:22 GMT  
		Size: 51.4 MB (51383225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4460d569be2430f3c91e38be78c74806191760c7dea23b68efd06e22e1c2fd`  
		Last Modified: Tue, 02 Aug 2022 18:38:33 GMT  
		Size: 56.9 MB (56895501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7065437faceafd626b5ffa79b609c3a36049ee43c69c557ff69709238cda3ae1`  
		Last Modified: Tue, 02 Aug 2022 18:38:40 GMT  
		Size: 119.0 MB (118976397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb703c871b27a542fa2373f65fee5a3da0e3bec41ed8c4c22957de0ed0f66ca5`  
		Last Modified: Tue, 02 Aug 2022 18:38:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
