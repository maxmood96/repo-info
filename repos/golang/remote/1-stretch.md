## `golang:1-stretch`

```console
$ docker pull golang@sha256:9a0de5e2832fffc5b32c9e618dac247d0ac419f6c6a8e9091a53f84b0b375282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:1-stretch` - linux; amd64

```console
$ docker pull golang@sha256:bfa1bb66a24ad01df908a7b575c75b360f5a3a526a7bdfe81b6dbe8ea354ecb3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303480688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f395e9e97e1ebef61f3b64fda639655ae9ae7e7c785e204e93c6a1ec2e93346d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:31 GMT
ADD file:4937a62e9e92f367221357a58d7438d1f76546bf3669281431633aebcfd7839d in / 
# Tue, 21 Dec 2021 01:24:31 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 01:56:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 08:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 08:03:12 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 22:20:47 GMT
ENV GOLANG_VERSION=1.17.6
# Thu, 06 Jan 2022 22:21:06 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.6.linux-amd64.tar.gz'; 			sha256='231654bbf2dab3d86c1619ce799e77b03d96f9b50770297c8f4dff8836fc8ca2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.6.linux-armv6l.tar.gz'; 			sha256='9ac723e6b41cb7c3651099a09332a8a778b69aa63a5e6baaa47caf0d818e2d6d'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.6.linux-arm64.tar.gz'; 			sha256='82c1a033cce9bc1b47073fd6285233133040f0378439f3c4659fe77cc534622a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.6.linux-386.tar.gz'; 			sha256='06c50fb0d44bb03dd4ea8795f9448379c5825d2765307b51f66905084c3ba541'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.6.linux-ppc64le.tar.gz'; 			sha256='adc35c920b8c0253d4dd001f8979e0db4c6111a60cd5e0785a8bee95dba1fcaa'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.6.linux-s390x.tar.gz'; 			sha256='ccb2d4509db846be7055d1105b28154e72cd43162c4ef79c38a936a3e6f26e1d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.6.src.tar.gz'; 		sha256='4dc1bbf3ff61f0c1ff2b19355e6d88151a70126268a47c761477686ef94748c8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 Jan 2022 22:21:08 GMT
ENV GOPATH=/go
# Thu, 06 Jan 2022 22:21:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 22:21:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Jan 2022 22:21:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a56b4def9c45045931a9cf99e9365b558347ae41ec8bfb104a7787e1c3129b0`  
		Last Modified: Tue, 21 Dec 2021 01:31:13 GMT  
		Size: 45.4 MB (45381404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0a7240797a1605f51c11e7c8f49754a8a78c89616dec348fa937886702d115`  
		Last Modified: Tue, 21 Dec 2021 02:04:58 GMT  
		Size: 11.3 MB (11301861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb8704bdb1f04110dfee1bc6e00f421a37681ff4f136c12337f31c1ccd62bb`  
		Last Modified: Tue, 21 Dec 2021 02:04:58 GMT  
		Size: 4.3 MB (4342385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737a610bfddaa0e7c87d11580b07707489348ac0fb4cdf2f2265ff2e60246c1b`  
		Last Modified: Tue, 21 Dec 2021 02:05:16 GMT  
		Size: 49.8 MB (49762204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4328e086ba810df9b013c851bb2881cc1fa5bf71974a59e8dc00aad454f796`  
		Last Modified: Wed, 22 Dec 2021 08:08:40 GMT  
		Size: 57.9 MB (57863114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e345eceda173aec1846cd681bf328c6af23403fb7077ca12e26c262706446bd`  
		Last Modified: Thu, 06 Jan 2022 22:33:26 GMT  
		Size: 134.8 MB (134829565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1a77e0d0868af0837a648dc82fdbdac1577aff90167c1764c4a29759178e3e`  
		Last Modified: Thu, 06 Jan 2022 22:33:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:59fc70d8aa86c6f7ec6f74d4144cb8da4e0fe4f0a860eeff634aa552aa372bb3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251397795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a4f57d8e2f070385d4ca0dd3115d37587b5d3f82f281bbfc8912da36951fd6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:07 GMT
ADD file:60b016ba67df7136a5c9120c3bda872fe6fc9264670eaec4af04649094d2c53d in / 
# Tue, 21 Dec 2021 02:05:08 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:57:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:58:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 16:06:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 16:06:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Dec 2021 16:10:10 GMT
ENV GOLANG_VERSION=1.17.5
# Wed, 22 Dec 2021 16:10:46 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.5.linux-amd64.tar.gz'; 			sha256='bd78114b0d441b029c8fe0341f4910370925a4d270a6a590668840675b0c653e'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.5.linux-armv6l.tar.gz'; 			sha256='aa1fb6c53b4fe72f159333362a10aca37ae938bde8adc9c6eaf2a8e87d1e47de'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.5.linux-arm64.tar.gz'; 			sha256='6f95ce3da40d9ce1355e48f31f4eb6508382415ca4d7413b1e7a3314e6430e7e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.5.linux-386.tar.gz'; 			sha256='4f4914303bc18f24fd137a97e595735308f5ce81323c7224c12466fd763fc59f'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.5.linux-ppc64le.tar.gz'; 			sha256='3d4be616e568f0a02cb7f7769bcaafda4b0969ed0f9bb4277619930b96847e70'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.5.linux-s390x.tar.gz'; 			sha256='8087d4fe991e82804e6485c26568c2e0ee0bfde00ceb9015dc86cb6bf84ef40b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.5.src.tar.gz'; 		sha256='3defb9a09bed042403195e872dcbc8c6fae1485963332279668ec52e80a95a2d'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 22 Dec 2021 16:10:48 GMT
ENV GOPATH=/go
# Wed, 22 Dec 2021 16:10:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Dec 2021 16:10:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 22 Dec 2021 16:10:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1680a7a0944ad84261b1979d7a37cbfaab55a5d7841917a0fb9a78ccc086ee83`  
		Last Modified: Tue, 21 Dec 2021 02:22:04 GMT  
		Size: 42.1 MB (42116934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feceeddac91e698bf009a378cca3bc65e3bee1199adb92912590e31192ac0437`  
		Last Modified: Tue, 21 Dec 2021 03:20:32 GMT  
		Size: 10.0 MB (9956591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee13a902270fb35c27560bff16e80e54c7122abb938b35cc5188ca753ba23cc`  
		Last Modified: Tue, 21 Dec 2021 03:20:29 GMT  
		Size: 3.9 MB (3921249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cb66d53e7811ef080c8e19ffc98281d9a7e1f083d7f574f6a709b728c2fc01`  
		Last Modified: Tue, 21 Dec 2021 03:21:16 GMT  
		Size: 46.1 MB (46125906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa3a8aa45ad1434b99db4675b8476a991fd7807914e1b90395c1e84964b9c6`  
		Last Modified: Wed, 22 Dec 2021 16:22:06 GMT  
		Size: 46.2 MB (46193779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091cb21f1ed8ec5a36dc871f54f216d6a6a88612adb4c759faa51cabc2a2c1da`  
		Last Modified: Wed, 22 Dec 2021 16:27:26 GMT  
		Size: 103.1 MB (103083181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66242ffb46313a8ff9c94bfa7bb049f45c4853d4290621893030de31a83d7057`  
		Last Modified: Wed, 22 Dec 2021 16:26:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:13d21e4dd9cb58e709a97daa4c7ac2b2634d55096fe07f3ed5469541996ef050
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256670404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e1d9011c014b4f72f1a88af0632bd28d7fc1face9be4664ade628331678c17`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:24 GMT
ADD file:a938be6f1e00e8fe4e0dde6657fcab5db99de34969d54368106a9334f67c1533 in / 
# Tue, 21 Dec 2021 01:44:25 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:16:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:16:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:17:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 18:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 18:39:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 22:41:13 GMT
ENV GOLANG_VERSION=1.17.6
# Thu, 06 Jan 2022 22:41:28 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.6.linux-amd64.tar.gz'; 			sha256='231654bbf2dab3d86c1619ce799e77b03d96f9b50770297c8f4dff8836fc8ca2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.6.linux-armv6l.tar.gz'; 			sha256='9ac723e6b41cb7c3651099a09332a8a778b69aa63a5e6baaa47caf0d818e2d6d'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.6.linux-arm64.tar.gz'; 			sha256='82c1a033cce9bc1b47073fd6285233133040f0378439f3c4659fe77cc534622a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.6.linux-386.tar.gz'; 			sha256='06c50fb0d44bb03dd4ea8795f9448379c5825d2765307b51f66905084c3ba541'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.6.linux-ppc64le.tar.gz'; 			sha256='adc35c920b8c0253d4dd001f8979e0db4c6111a60cd5e0785a8bee95dba1fcaa'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.6.linux-s390x.tar.gz'; 			sha256='ccb2d4509db846be7055d1105b28154e72cd43162c4ef79c38a936a3e6f26e1d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.6.src.tar.gz'; 		sha256='4dc1bbf3ff61f0c1ff2b19355e6d88151a70126268a47c761477686ef94748c8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 Jan 2022 22:41:29 GMT
ENV GOPATH=/go
# Thu, 06 Jan 2022 22:41:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 22:41:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Jan 2022 22:41:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d097540eada98ef0bee6e7283ee6a0fbe163c439c3543706a7fbf2f0158fd907`  
		Last Modified: Tue, 21 Dec 2021 01:52:36 GMT  
		Size: 43.2 MB (43173780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cc8f4026ffff85190545c2b0228f223f2fdbf2c94740c8bc8b6ec6acc7e5cf`  
		Last Modified: Tue, 21 Dec 2021 02:26:14 GMT  
		Size: 10.2 MB (10217083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949ec2ba0d61fd5c0766a70b7db0bd27e7f6e86fbd1511504e8a5c8d0af26411`  
		Last Modified: Tue, 21 Dec 2021 02:26:13 GMT  
		Size: 3.9 MB (3873882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66df5c57061d26479de8f7ee3e37301f5bebfd97c94724dab3e21918f41f749`  
		Last Modified: Tue, 21 Dec 2021 02:26:32 GMT  
		Size: 47.7 MB (47735273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e610ce06baf734615709158a41d26d261b15466eefe454a274b017bdacf795`  
		Last Modified: Tue, 21 Dec 2021 18:46:08 GMT  
		Size: 49.0 MB (49022981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595a12aae8494b2f61b734680e28c23db0f7fbf271e4a0ea3b57d8099a722998`  
		Last Modified: Thu, 06 Jan 2022 22:52:20 GMT  
		Size: 102.6 MB (102647279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee761cfc4e98649cc54b8e0949f174bae9786b4dec1cac0d2a8e6c76a2ce9ec3`  
		Last Modified: Thu, 06 Jan 2022 22:52:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; 386

```console
$ docker pull golang@sha256:5f5ece031c72fbdb3e613fe9ec9638aedca661dc2261b239fa9995e634691902
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281298785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5371a07151f0b176a1d2341ace2448443c96bfe309ff229e92529d9345add30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:43:09 GMT
ADD file:55bfa1f20811d5ad7e0824cb8b85e2d7c75ed74ca2784dae41a80c54c2ee3ca8 in / 
# Tue, 21 Dec 2021 01:43:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:19:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:20:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 04:16:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 04:16:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 22:40:07 GMT
ENV GOLANG_VERSION=1.17.6
# Thu, 06 Jan 2022 22:40:25 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.6.linux-amd64.tar.gz'; 			sha256='231654bbf2dab3d86c1619ce799e77b03d96f9b50770297c8f4dff8836fc8ca2'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.6.linux-armv6l.tar.gz'; 			sha256='9ac723e6b41cb7c3651099a09332a8a778b69aa63a5e6baaa47caf0d818e2d6d'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.6.linux-arm64.tar.gz'; 			sha256='82c1a033cce9bc1b47073fd6285233133040f0378439f3c4659fe77cc534622a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.6.linux-386.tar.gz'; 			sha256='06c50fb0d44bb03dd4ea8795f9448379c5825d2765307b51f66905084c3ba541'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.6.linux-ppc64le.tar.gz'; 			sha256='adc35c920b8c0253d4dd001f8979e0db4c6111a60cd5e0785a8bee95dba1fcaa'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.6.linux-s390x.tar.gz'; 			sha256='ccb2d4509db846be7055d1105b28154e72cd43162c4ef79c38a936a3e6f26e1d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.6.src.tar.gz'; 		sha256='4dc1bbf3ff61f0c1ff2b19355e6d88151a70126268a47c761477686ef94748c8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 Jan 2022 22:40:26 GMT
ENV GOPATH=/go
# Thu, 06 Jan 2022 22:40:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 22:40:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Jan 2022 22:40:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a33597723b77b33e69ce15c675459677dc40eb6b8b822c767d1d106fb2b0365e`  
		Last Modified: Tue, 21 Dec 2021 01:53:18 GMT  
		Size: 46.1 MB (46097707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32c51fce1ac683ec95f0c86c7641f827f198b990803f717ccf546687b4be861`  
		Last Modified: Tue, 21 Dec 2021 02:30:36 GMT  
		Size: 11.4 MB (11359468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8196c269478417443ffdcc48080de94b4136a900f548611f282dc723b34ffa4b`  
		Last Modified: Tue, 21 Dec 2021 02:30:35 GMT  
		Size: 4.6 MB (4564918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0103767f9e30cdb022f48ed2587254717c334195519f35285c473ce97d331f7`  
		Last Modified: Tue, 21 Dec 2021 02:31:01 GMT  
		Size: 51.3 MB (51264824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e10a41c2bb54108fce634a6edb8a6b702cb2c98d81678ad3ee8546ce2ba35ef`  
		Last Modified: Wed, 22 Dec 2021 04:26:03 GMT  
		Size: 62.4 MB (62387753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c8a185d7514dc718356e18fa82d694b6a12c8dedef14db25c8232ffe207b4b`  
		Last Modified: Thu, 06 Jan 2022 22:56:21 GMT  
		Size: 105.6 MB (105623959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d06e12213a5a53001ed854c6a7589ab7bc2a4b7fc1ed44c13e6db8054d2fe`  
		Last Modified: Thu, 06 Jan 2022 22:55:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
