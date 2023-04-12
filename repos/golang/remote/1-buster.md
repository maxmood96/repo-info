## `golang:1-buster`

```console
$ docker pull golang@sha256:d4d9672c972b8c32678364ff785c4e073af78fe8ac26efcf159b0c22815fb100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:1-buster` - linux; amd64

```console
$ docker pull golang@sha256:1751112c774258c932b169c4143f767575b4bb68042cd2bc55e9fce25d700125
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289185208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef29dfa0f7d36d483d99cfa0ac14b0c61e3b565dedbcf00333681772604f1f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:15 GMT
ADD file:40953ed6e6f96703b2e0c13288437c2aaf8b3df33dbc423686290cbe0e595a5e in / 
# Wed, 12 Apr 2023 00:20:15 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:52:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:53:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 19:46:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 19:46:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 19:46:06 GMT
ENV GOLANG_VERSION=1.20.3
# Wed, 12 Apr 2023 19:46:14 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.3.linux-amd64.tar.gz'; 			sha256='979694c2c25c735755bf26f4f45e19e64e4811d661dd07b8c010f7a8e18adfca'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.3.linux-armv6l.tar.gz'; 			sha256='b421e90469a83671641f81b6e20df6500f033e9523e89cbe7b7223704dd1035c'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.3.linux-arm64.tar.gz'; 			sha256='eb186529f13f901e7a2c4438a05c2cd90d74706aaa0a888469b2a4a617b6ee54'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.3.linux-386.tar.gz'; 			sha256='e12384311403f1389d14cc1c1295bfb4e0dd5ab919403b80da429f671a223507'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.3.linux-ppc64le.tar.gz'; 			sha256='943c89aa1624ea544a022b31e3d6e16a037200e436370bdd5fd67f3fa60be282'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.3.linux-s390x.tar.gz'; 			sha256='126cf823a5634ef2544b866db107b9d351d3ea70d9e240b0bdcfb46f4dcae54b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.3.src.tar.gz'; 		sha256='e447b498cde50215c4f7619e5124b0fc4e25fb5d16ea47271c47f278e7aa763a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 12 Apr 2023 19:46:15 GMT
ENV GOPATH=/go
# Wed, 12 Apr 2023 19:46:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 19:46:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 12 Apr 2023 19:46:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ff1d7c41c74a25258bfa6f0b8adb0a727f84518f55f65ca845ebc747976c408`  
		Last Modified: Wed, 12 Apr 2023 00:24:01 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b253aeafeaa7e0671bb60008df01de101a38a045ff7bc656e3b0fbfc7c05cca5`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 7.9 MB (7863355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2201bd995cccf12851a50820de03d34a17011dcbb9ac9fdf3a50c952cbb131`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 10.0 MB (10001452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de76e268b103d05fa8960e0f77951ff54b912b63429c34f5d6adfd09f5f9ee2`  
		Last Modified: Wed, 12 Apr 2023 07:58:44 GMT  
		Size: 51.9 MB (51876420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e211ab4e270c4e15d645dfc2dc5dba6ecc620f37851b60da72648429652ac6f8`  
		Last Modified: Wed, 12 Apr 2023 19:47:54 GMT  
		Size: 68.9 MB (68851308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1884307c61e9d348e6ecdb8421a37a2bc42f256ce8f7bcc1fdbcf7ace5dbdde4`  
		Last Modified: Wed, 12 Apr 2023 19:47:57 GMT  
		Size: 100.1 MB (100143791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba1df41d121aec837c0736317d55c70f410b71bfb1de7a73c0ca65d80104b11`  
		Last Modified: Wed, 12 Apr 2023 19:47:45 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:cc027666b1b9d2b2d4c9e69b3e1fadce3434f37e9815b1376a3761f58c7b38a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260977017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f43afe9eae61ee4065b36355961df05538b7abb5bd7b73f8d2dedd7d4cf6902`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:37:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 16:02:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 16:02:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 16:02:01 GMT
ENV GOLANG_VERSION=1.20.3
# Wed, 12 Apr 2023 16:02:13 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.3.linux-amd64.tar.gz'; 			sha256='979694c2c25c735755bf26f4f45e19e64e4811d661dd07b8c010f7a8e18adfca'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.3.linux-armv6l.tar.gz'; 			sha256='b421e90469a83671641f81b6e20df6500f033e9523e89cbe7b7223704dd1035c'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.3.linux-arm64.tar.gz'; 			sha256='eb186529f13f901e7a2c4438a05c2cd90d74706aaa0a888469b2a4a617b6ee54'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.3.linux-386.tar.gz'; 			sha256='e12384311403f1389d14cc1c1295bfb4e0dd5ab919403b80da429f671a223507'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.3.linux-ppc64le.tar.gz'; 			sha256='943c89aa1624ea544a022b31e3d6e16a037200e436370bdd5fd67f3fa60be282'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.3.linux-s390x.tar.gz'; 			sha256='126cf823a5634ef2544b866db107b9d351d3ea70d9e240b0bdcfb46f4dcae54b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.3.src.tar.gz'; 		sha256='e447b498cde50215c4f7619e5124b0fc4e25fb5d16ea47271c47f278e7aa763a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 12 Apr 2023 16:02:15 GMT
ENV GOPATH=/go
# Wed, 12 Apr 2023 16:02:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 16:02:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 12 Apr 2023 16:02:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84460c1688b734c8075a939aae674e32cf7240a0d3a2fa0602a9a9fd472ffe1e`  
		Last Modified: Wed, 12 Apr 2023 09:46:16 GMT  
		Size: 7.2 MB (7153935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4779654861d62e5bc31eea7bacd2c7bbfdb617dd9dc01e2afd24a4baedf7f`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 9.3 MB (9348985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bfe04b18e678bcacb84dd292223f32a76d4837c22ccd16465318f6c1429f21`  
		Last Modified: Wed, 12 Apr 2023 09:46:34 GMT  
		Size: 47.4 MB (47395508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9485f2cdc83cfd8773208c780bc84803c5a5b266b78263c7cad4448d6820fbd5`  
		Last Modified: Wed, 12 Apr 2023 16:03:59 GMT  
		Size: 53.3 MB (53322152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa91d7d07fefb6e3d46b37e54183a1900587a64fff51c2b47f2e4ef88cbb9865`  
		Last Modified: Wed, 12 Apr 2023 16:04:06 GMT  
		Size: 97.8 MB (97840080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a24e547931c5b2e3257d1b9f63ce2ed534bff78615ced2e868b277e4592c18b`  
		Last Modified: Wed, 12 Apr 2023 16:03:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:19089239907e57f3916c66a425300fb8278bffe60882f3112203ab2f8fd05719
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277319310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70118333c6a62432a45e1490ab0458a1e9f42c128ee3021de848587261f7d9ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:08:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 15:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 15:25:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 15:25:26 GMT
ENV GOLANG_VERSION=1.20.3
# Wed, 12 Apr 2023 15:25:43 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.3.linux-amd64.tar.gz'; 			sha256='979694c2c25c735755bf26f4f45e19e64e4811d661dd07b8c010f7a8e18adfca'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.3.linux-armv6l.tar.gz'; 			sha256='b421e90469a83671641f81b6e20df6500f033e9523e89cbe7b7223704dd1035c'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.3.linux-arm64.tar.gz'; 			sha256='eb186529f13f901e7a2c4438a05c2cd90d74706aaa0a888469b2a4a617b6ee54'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.3.linux-386.tar.gz'; 			sha256='e12384311403f1389d14cc1c1295bfb4e0dd5ab919403b80da429f671a223507'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.3.linux-ppc64le.tar.gz'; 			sha256='943c89aa1624ea544a022b31e3d6e16a037200e436370bdd5fd67f3fa60be282'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.3.linux-s390x.tar.gz'; 			sha256='126cf823a5634ef2544b866db107b9d351d3ea70d9e240b0bdcfb46f4dcae54b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.3.src.tar.gz'; 		sha256='e447b498cde50215c4f7619e5124b0fc4e25fb5d16ea47271c47f278e7aa763a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 12 Apr 2023 15:25:45 GMT
ENV GOPATH=/go
# Wed, 12 Apr 2023 15:25:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 15:25:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 12 Apr 2023 15:25:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208fd617b499747daceba851b67da426c285d1e306b316a193f06968123f49da`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 7.7 MB (7732136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efadebfda1423d1b70a0e991e9ff8bb2e3fe0b08d55562359a004c265fc7c86`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe7e7c438113f5e58417f97e7eb0a755b17ee63eebd85a7c3b86a2aad4c993e`  
		Last Modified: Wed, 12 Apr 2023 01:14:27 GMT  
		Size: 52.2 MB (52191713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1538e75d254cd886947ddc9ce8ab9f33688f93c41bfefaac5228d0675b0b6211`  
		Last Modified: Wed, 12 Apr 2023 15:27:14 GMT  
		Size: 62.7 MB (62714387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87444c0e4abcf4e65eead97eaeb704d64d99212daa28d4cdcb7e53303ec8720`  
		Last Modified: Wed, 12 Apr 2023 15:27:18 GMT  
		Size: 95.4 MB (95438707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2d975f0789269daf851d56ab44aa058ce0909be88fe1128ecbe447f1d63091`  
		Last Modified: Wed, 12 Apr 2023 15:27:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; 386

```console
$ docker pull golang@sha256:249ba22f7a47bd241b1e022a62fb9c828728180fe6e8e42001854d5c9cb269fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297306327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17faf1943ff00c6edf0dd02f65e50a5d504fa5ae230d3c69a49397df45470e30`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:29 GMT
ADD file:b1ee2e3a45801f9bc3a5b377c91d729589265495607481a83edb501aacee34e7 in / 
# Thu, 23 Mar 2023 00:39:30 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:47:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 13:47:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Mar 2023 02:58:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Mar 2023 02:58:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Apr 2023 18:24:54 GMT
ENV GOLANG_VERSION=1.20.3
# Tue, 04 Apr 2023 18:25:08 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.20.3.linux-amd64.tar.gz'; 			sha256='979694c2c25c735755bf26f4f45e19e64e4811d661dd07b8c010f7a8e18adfca'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.20.3.linux-armv6l.tar.gz'; 			sha256='b421e90469a83671641f81b6e20df6500f033e9523e89cbe7b7223704dd1035c'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.20.3.linux-arm64.tar.gz'; 			sha256='eb186529f13f901e7a2c4438a05c2cd90d74706aaa0a888469b2a4a617b6ee54'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.20.3.linux-386.tar.gz'; 			sha256='e12384311403f1389d14cc1c1295bfb4e0dd5ab919403b80da429f671a223507'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.20.3.linux-ppc64le.tar.gz'; 			sha256='943c89aa1624ea544a022b31e3d6e16a037200e436370bdd5fd67f3fa60be282'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.20.3.linux-s390x.tar.gz'; 			sha256='126cf823a5634ef2544b866db107b9d351d3ea70d9e240b0bdcfb46f4dcae54b'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.3.src.tar.gz'; 		sha256='e447b498cde50215c4f7619e5124b0fc4e25fb5d16ea47271c47f278e7aa763a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 04 Apr 2023 18:25:10 GMT
ENV GOPATH=/go
# Tue, 04 Apr 2023 18:25:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Apr 2023 18:25:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 04 Apr 2023 18:25:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e3f08b81fb272fb973474eec1fcbeccf665d7941774b72a1e9448a5daba9682d`  
		Last Modified: Thu, 23 Mar 2023 00:43:29 GMT  
		Size: 51.2 MB (51207106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd932bf97a5034f015d0289b8e85e4850b34a0e0e316b8be505798e29445b795`  
		Last Modified: Thu, 23 Mar 2023 13:54:30 GMT  
		Size: 8.0 MB (8033906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a235a06e0c6cba8982980dec3a4574d2f2fa3258419845bb5d6d3b303bae6d89`  
		Last Modified: Thu, 23 Mar 2023 13:54:30 GMT  
		Size: 10.3 MB (10345713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f9f146634a33f6edc08520903923b5e9e1b7ac3449d3de0a4a2fe056491568`  
		Last Modified: Thu, 23 Mar 2023 13:54:49 GMT  
		Size: 53.5 MB (53470794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c430ca87293321cf565c1b2c7581e186a4f100d12ea948472801d9f71c8efc`  
		Last Modified: Fri, 24 Mar 2023 03:01:07 GMT  
		Size: 73.7 MB (73716362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bee589c823bf6610c3d0fff2169371793d184f6293767ddd3e720fe9035db`  
		Last Modified: Tue, 04 Apr 2023 18:39:28 GMT  
		Size: 100.5 MB (100532291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311f981abb28120f269e709d83782b65550c75d6decf8bd564d49544c0f70e20`  
		Last Modified: Tue, 04 Apr 2023 18:39:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
