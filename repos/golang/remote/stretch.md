## `golang:stretch`

```console
$ docker pull golang@sha256:dc465114d58a324bbf36a58e9a34de201cb8d0375dfdd5522b05f688f0585aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:stretch` - linux; amd64

```console
$ docker pull golang@sha256:8d314fedd4e3e5d51e8faa498e84d1a5f9315c3bcd1a235d70789cf31bc2c26a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297619793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c471be631dd0f5619fae73aff7d487215d6cbeb756fb9bfe2de8b276d43a4002`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:52:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:14:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 04:14:29 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Mar 2021 04:14:29 GMT
ENV GOLANG_VERSION=1.16.2
# Sat, 13 Mar 2021 04:14:44 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 13 Mar 2021 04:14:45 GMT
ENV GOPATH=/go
# Sat, 13 Mar 2021 04:14:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Mar 2021 04:14:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 13 Mar 2021 04:14:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a403cc031caeb1ddbae71b9f7e47d7854415c8aa6f0b84b8e7be4b3db513867e`  
		Last Modified: Fri, 12 Mar 2021 03:22:42 GMT  
		Size: 49.8 MB (49786779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9701e8560289d77efa3d3db55e7ddb8eb7d4b4ab2b196fe9387e4a79716bc80`  
		Last Modified: Sat, 13 Mar 2021 04:17:20 GMT  
		Size: 57.8 MB (57829052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efd1ded946fb5e11566517b3415936619fae70bdd21dfbbb525a0eea3c44f8d`  
		Last Modified: Sat, 13 Mar 2021 04:17:32 GMT  
		Size: 129.0 MB (129010384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88b6bb26ed47cd4f2788cb201df8e5e261dcdfe9cd848d49427a802a4765676`  
		Last Modified: Sat, 13 Mar 2021 04:17:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:f7aa618853fc49c96b645618a69ec2505d95462518c7d0c991e8615648afe8fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248538934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e794dc6f3b70c6063b62c5422e69e2bd302eb91f49fe13b68df936b7e70afe94`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:31:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 13:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:00:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:00:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 09:00:07 GMT
ENV GOLANG_VERSION=1.16.2
# Sat, 27 Mar 2021 09:00:41 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 27 Mar 2021 09:00:46 GMT
ENV GOPATH=/go
# Sat, 27 Mar 2021 09:00:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 09:00:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 27 Mar 2021 09:00:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf4418db1e976b0b84122d61cab9eb3bf7616e363a557275308ca2ccc72365`  
		Last Modified: Fri, 26 Mar 2021 13:55:29 GMT  
		Size: 9.9 MB (9939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfe21b354ae04ba513e56799a77ae6f0f57339ee9fec76a66d4e7aaffda99e4`  
		Last Modified: Fri, 26 Mar 2021 13:55:25 GMT  
		Size: 3.9 MB (3921260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017f4a3c6ff8566959485607b47c6d4748a4e04e25a1b7d98c2e289c887074c9`  
		Last Modified: Fri, 26 Mar 2021 13:55:55 GMT  
		Size: 46.1 MB (46127623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7c9dd0f9d0feff2708b4132b15ce6c63f5b6d60a3d647760098e98a78e8061`  
		Last Modified: Sat, 27 Mar 2021 09:04:31 GMT  
		Size: 46.2 MB (46161474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf80466a0b2a7473ec3bbc587688cffabdd31b04a9414d741b0208dd669860d`  
		Last Modified: Sat, 27 Mar 2021 09:04:51 GMT  
		Size: 100.3 MB (100268823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8fd2bbafb67aa7f172d7d373c2052b440fd085623d3fd72b9a4a6ea404296e`  
		Last Modified: Sat, 27 Mar 2021 09:04:19 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:56d733e5423a88a9c3d15cedbefa503bb15581d066d64d7d99ecff7b1c01c6f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253993358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13e4b1b1f88f262b092018661449cb39aa4e5e12828fec956a9f9ca32483e61`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:37:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:43:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:43:36 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 19:43:37 GMT
ENV GOLANG_VERSION=1.16.2
# Fri, 12 Mar 2021 19:43:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 12 Mar 2021 19:43:58 GMT
ENV GOPATH=/go
# Fri, 12 Mar 2021 19:43:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 19:44:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 12 Mar 2021 19:44:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aef9c13609053a0f18bfd7ec1ca3e02fd48ed839084b2d58f79a51c9082893d`  
		Last Modified: Fri, 12 Mar 2021 02:46:37 GMT  
		Size: 47.7 MB (47734975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d1ec60dbebd7327b3fc0d100872dbc73e62741ef594015684d0c5460aae986`  
		Last Modified: Fri, 12 Mar 2021 19:47:00 GMT  
		Size: 49.2 MB (49224799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29193df6411c1d2009d3d646a8bbaefe9825dc54601189ee6fd4b6f59f581dbf`  
		Last Modified: Fri, 12 Mar 2021 19:47:13 GMT  
		Size: 99.6 MB (99575244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f10bfd62fced81255c1af5ced67c5aafe28725b091a870205f0f55471d6dbd`  
		Last Modified: Fri, 12 Mar 2021 19:46:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; 386

```console
$ docker pull golang@sha256:c2b71811eebf781dd8a7b15d3a567ca7a6638d525e5a79bbed8f50de8f982d08
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278679227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b79db8ca3947151111a75ac8c61f36e17d65015b9e5741f503a533b95c8fe21`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:55:57 GMT
ADD file:0a48869723941cb015604aec94e5f955449b86eca7c73ec978c3d1dcaf3517ba in / 
# Fri, 26 Mar 2021 13:55:58 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 22:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 22:48:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 22:49:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 11:18:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 11:18:36 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 11:18:36 GMT
ENV GOLANG_VERSION=1.16.2
# Sat, 27 Mar 2021 11:18:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-amd64.tar.gz'; 			sha256='542e936b19542e62679766194364f45141fde55169db2d8d01046555ca9eb4b8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-armv6l.tar.gz'; 			sha256='49765b1ac36f77a84ce8186b08713c3811db5426e4ecfaa4344453e12d756c22'; 			;; 		'arm64') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-arm64.tar.gz'; 			sha256='6924601d998a0917694fd14261347e3798bd2ad6b13c4d7f2edd70c9d57f62ab'; 			;; 		'i386') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-386.tar.gz'; 			sha256='3638abf8e8272a4ddc3e5189487c932d680abfb151e2c48ae18c9a04a90ded73'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-ppc64le.tar.gz'; 			sha256='e1dcc9b460b2d522added8dfce764a06c5e455c8047b45b67a06f7f5ab19c4e0'; 			;; 		's390x') 			url='https://storage.googleapis.com/golang/go1.16.2.linux-s390x.tar.gz'; 			sha256='a686743b0803d54e051756ce946d9d72436f23e9f815739c947934e0052bf9ff'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://storage.googleapis.com/golang/go1.16.2.src.tar.gz'; 		sha256='37ca14287a23cb8ba2ac3f5c3dd8adbc1f7a54b9701a57824bf19a0b271f83ea'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Sat, 27 Mar 2021 11:18:51 GMT
ENV GOPATH=/go
# Sat, 27 Mar 2021 11:18:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 11:18:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 27 Mar 2021 11:18:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:01c2b0829d8abcf8cd9012766b99919fd21d4a2c1fae4d9312b5716bf40ba27e`  
		Last Modified: Fri, 26 Mar 2021 14:06:26 GMT  
		Size: 46.1 MB (46098430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd034d6463d3d9372f405b356a0e09c553416c4c875ff58bfc709940c165f19d`  
		Last Modified: Fri, 26 Mar 2021 23:00:01 GMT  
		Size: 11.3 MB (11336731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9889d71e348186e773160024e7d403e8a0ac99f4fd04c26eb0b04023c8eb7da`  
		Last Modified: Fri, 26 Mar 2021 23:00:00 GMT  
		Size: 4.6 MB (4565051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ce5dd564d786a704453c35a01a5b0f08bf43708c6479077ea140e47ce9d1a3`  
		Last Modified: Fri, 26 Mar 2021 23:00:31 GMT  
		Size: 51.3 MB (51264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e5a73b554801e7d75cd241b5c8d77130b53653f86d80b5e622638ac0608673`  
		Last Modified: Sat, 27 Mar 2021 11:22:37 GMT  
		Size: 62.4 MB (62355830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486594661db36c0c22d411929a4476fcdc7bfd0ba9c1ed40eb1d23cc03eacabc`  
		Last Modified: Sat, 27 Mar 2021 11:22:44 GMT  
		Size: 103.1 MB (103058167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e274745ed87a515e816ffbdc88827bf58a0b1bfa9b049c7a72a162fed478a28`  
		Last Modified: Sat, 27 Mar 2021 11:22:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
