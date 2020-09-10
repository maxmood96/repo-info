## `golang:1-buster`

```console
$ docker pull golang@sha256:4f0a644105db27ad25a94a143490b83ded254717e787fec0d3fd398d8445e7b6
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
$ docker pull golang@sha256:5976acadfa9ccd05b6950c709c1dc99c8a4f3068ea71150cb143f16c4c83ca04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.9 MB (309857700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2ea509005fef772885f0fe3472e82f92739a4080a73558559822ead302c445`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:33 GMT
ADD file:4b03b5f551e3fbdf47ec609712007327828f7530cc3455c43bbcdcaf449a75a9 in / 
# Tue, 04 Aug 2020 15:42:34 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:26:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:26:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 23:26:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 10:31:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 10:31:10 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:19:48 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:19:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 09 Sep 2020 22:20:00 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:20:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:20:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:20:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d6ff36c9ec4822c9ff8953560f7ba41653b348a9c1136755e653575f58fbded7`  
		Last Modified: Tue, 04 Aug 2020 15:48:55 GMT  
		Size: 50.4 MB (50396000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c958d65b3090aefea91284d018b2a86530a3c8174b72616c4e76993c696a5797`  
		Last Modified: Tue, 04 Aug 2020 23:39:28 GMT  
		Size: 7.8 MB (7811570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf0a6b092f5673ec05b40edb606ce58881b2f40494251117d31805225ef064`  
		Last Modified: Tue, 04 Aug 2020 23:39:27 GMT  
		Size: 10.0 MB (9996337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80931cf6881673fd161a3fd73e8971fe4a569fd7fbb44e956d261ca58d97dfab`  
		Last Modified: Tue, 04 Aug 2020 23:39:45 GMT  
		Size: 51.8 MB (51829826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813643441356759e9202aeebde31d45192b5e5e6218cd8d2ad216304bf415551`  
		Last Modified: Wed, 05 Aug 2020 10:33:40 GMT  
		Size: 68.7 MB (68672152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c0b5f68f2d7e175d64567abea52b8d21f1dee9cff806f9f504ecb60882e00f`  
		Last Modified: Wed, 09 Sep 2020 22:28:34 GMT  
		Size: 121.2 MB (121151689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00eb2776cffd052bb7fb6fb11cc9f271b8b26812210ffa92f628ff71372e3d4`  
		Last Modified: Wed, 09 Sep 2020 22:28:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:6997df243a686237c6137b0edd9bb621f14f557adac6531c00e49eb8ec78bf33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269815288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1f5d1c2916940d17c981a67f18c8a8b18b7d1f121bdc98c2b1ffbee2838432`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:11:38 GMT
ADD file:e1152998db9c9a59e88100fa415cb22c317d906c5143042e7e36fa6911264f66 in / 
# Tue, 04 Aug 2020 03:11:50 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:13:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:13:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 06:14:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 15:39:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 15:39:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:48:26 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:51:51 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 09 Sep 2020 22:51:56 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:51:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:52:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:52:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:43e007f43c47fbc3bc147d3d82021dc9a400b509f9c30dc687c1a3ed5fd23065`  
		Last Modified: Tue, 04 Aug 2020 03:33:39 GMT  
		Size: 48.1 MB (48108803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0270eaf99061a6aa3af6cdd0f5e0ae94bf697d7565783759c971252b202c37dd`  
		Last Modified: Tue, 04 Aug 2020 06:36:56 GMT  
		Size: 7.4 MB (7360991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e527b7990670f219ff9d29ac8963fbdc4756e6c6190434bba9c0482626f4ca`  
		Last Modified: Tue, 04 Aug 2020 06:36:57 GMT  
		Size: 9.7 MB (9687011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556ab5cdb159eebd1404529d56d69ebe7cdffa65e8113e5d41a2e11fee7a734e`  
		Last Modified: Tue, 04 Aug 2020 06:37:26 GMT  
		Size: 49.6 MB (49572627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafbe12c84a35ce4d898d99657a0d607864ab5b33b05b3d2b359ea6510cd7bbc`  
		Last Modified: Tue, 04 Aug 2020 17:07:14 GMT  
		Size: 52.0 MB (51975393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d473dcdb6796ec2e927cf6fc29c201d1c7c79774b8ec805a6a821669e62374c`  
		Last Modified: Wed, 09 Sep 2020 22:56:53 GMT  
		Size: 103.1 MB (103110307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad3cd7be5ccc90a3e3a70de70c9f4c29306ef998ee8dc1adea5d9ce4d290afa`  
		Last Modified: Wed, 09 Sep 2020 22:56:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:38b3015aea4cf3e1340b08167f629fa9e9c5cbc87b3329b0a57211d98770d9bb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260792844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8f9a94db6257c0e823580d22d00a95730ca9dae82c37db1af77fd2f6165688`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:56:26 GMT
ADD file:aaf5c6340b3d662631775fa4536c2e48e9f68b6cc8d53e18fb8fd76ae41b305e in / 
# Tue, 04 Aug 2020 04:56:28 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:52:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:53:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 07:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:40:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:40:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:01:17 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:01:40 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 09 Sep 2020 22:01:43 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:01:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:01:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e7cf402ee4b1ba67e92813d50297a082bbdbdd4d47f6aeb62f2316b81d5dc843`  
		Last Modified: Tue, 04 Aug 2020 05:04:56 GMT  
		Size: 45.9 MB (45869261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff6bd4a89fc21d80ca6924320f86708f35ddea71c7aa34a408a5b64257c764e`  
		Last Modified: Tue, 04 Aug 2020 08:25:56 GMT  
		Size: 7.1 MB (7097820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48f5852a753b7731e5d374567ae9b64e309805758f336c76d5f13bb67c94e20`  
		Last Modified: Tue, 04 Aug 2020 08:25:56 GMT  
		Size: 9.3 MB (9343353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58a93b33dd4d533cc1e04eab8045940d69cb287134aa90c982e3d248739044e`  
		Last Modified: Tue, 04 Aug 2020 08:26:25 GMT  
		Size: 47.4 MB (47355829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb05471d9930e275bf9cac0b1bb0b93b8dde80ac8dd073dcb65c384d6d9e2ad`  
		Last Modified: Wed, 05 Aug 2020 01:45:54 GMT  
		Size: 53.1 MB (53140891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89771798b1f208e52c4ea6d1a4202757e46f5742db41361ca5281fc6498601e3`  
		Last Modified: Wed, 09 Sep 2020 22:11:36 GMT  
		Size: 98.0 MB (97985534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b81762607d01d8091c5e5a2517902fc20596de0b289ebd024cfb90d7a4ee44`  
		Last Modified: Wed, 09 Sep 2020 22:11:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:dc3a7e178f65d59b9090324a9fd572c774374b14ce5c70b330dc427fd220cd3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279275304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d03c3f0157b2c237b0c668874642c750dbeb48caf78ce42cf6946a0d19c1ce4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:06 GMT
ADD file:ce999027b153d392f8a0f85e2e7a17b9279f3cf7ad0e45192378d527275f99c6 in / 
# Tue, 04 Aug 2020 06:57:08 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:10:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:10:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 11:10:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 07:19:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 07:19:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:39:43 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:40:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 09 Sep 2020 22:40:08 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:40:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:40:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:40:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d5517ee72007172d5b814636405254dea459120ce08f85777bb287d106a6a240`  
		Last Modified: Tue, 04 Aug 2020 07:03:41 GMT  
		Size: 49.2 MB (49175491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283897ad4463628bd259e1cbb5eb788e7df554b42ae17fc6f5d02c4a56035c2`  
		Last Modified: Tue, 04 Aug 2020 11:23:01 GMT  
		Size: 7.7 MB (7681458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feb40d9f5fecfa098b8f7ece6c287c6fd61b114043c8b4647359120a7d943a3`  
		Last Modified: Tue, 04 Aug 2020 11:23:02 GMT  
		Size: 10.0 MB (9983917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b5fabb62f79acd92186da3c02d23bd8c15d79603a700959b582bd9e62854c`  
		Last Modified: Tue, 04 Aug 2020 11:23:28 GMT  
		Size: 52.2 MB (52163657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c836803dd1977ffe173b42414e8c2ae2e147cee2e1ee34a383f4251cf15a44`  
		Last Modified: Wed, 05 Aug 2020 07:23:33 GMT  
		Size: 62.5 MB (62532046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b556a00ff9cfc239503650b4b2c20b4de85187f22658499ab49bc37e479d3a`  
		Last Modified: Wed, 09 Sep 2020 22:48:28 GMT  
		Size: 97.7 MB (97738579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b433502103c4591f09f7e30da803c2401e12404d953a99799a4bc3f89c26b58e`  
		Last Modified: Wed, 09 Sep 2020 22:48:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; 386

```console
$ docker pull golang@sha256:b3735ce7ee5e7691098f0a661d093835f98ec350afacb45d344b47393410f3ee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (297045649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3757c4f7bbef558097811d229f33ed1c118145f749d16acfe9464a92e3b85c3a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:21 GMT
ADD file:e8aac36755acd0915e9f9bae82fc8fcd0bbc3911ca4a5a40e104b2a4ebce44da in / 
# Tue, 04 Aug 2020 03:37:21 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:06:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:06:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 08:07:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 18:43:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 18:43:53 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:38:28 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:38:41 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 09 Sep 2020 22:38:41 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:38:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:38:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:38:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b19305c328889ec69ec0d76e403c2cbc4603e5f27213a0e4d5f6597feefcf6e1`  
		Last Modified: Tue, 04 Aug 2020 03:42:18 GMT  
		Size: 51.2 MB (51158828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d9322a54f80129fd5cd69b7be3ac6ba44b9a0268afcbd10876508eb0f9264c`  
		Last Modified: Tue, 04 Aug 2020 08:25:50 GMT  
		Size: 8.0 MB (7981119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a7f32100867eafa619a9265416538a2a374b88219902c6270b6f023d19061`  
		Last Modified: Tue, 04 Aug 2020 08:25:51 GMT  
		Size: 10.3 MB (10338494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ea04987808c324433cf4b1b813ccf6528f9bf603422fbee2725c1e4018eb8`  
		Last Modified: Tue, 04 Aug 2020 08:26:25 GMT  
		Size: 53.4 MB (53433408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a9b823cf68f4d55b8db75bbbafe8018b21b444b78e7eaeab85ee790d02848`  
		Last Modified: Tue, 04 Aug 2020 18:46:40 GMT  
		Size: 73.5 MB (73530875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b871a7b9b0b04fb2b278ded4f21ceafd30ced7998618bc00e1f97b47148f2e3`  
		Last Modified: Wed, 09 Sep 2020 22:48:39 GMT  
		Size: 100.6 MB (100602799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66decbf2e90e1dda7b4a3568f72cbd15909f7579bcf6856c3c1e970f2c5fed56`  
		Last Modified: Wed, 09 Sep 2020 22:48:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; mips64le

```console
$ docker pull golang@sha256:49a2fae97e27db365b884cf08eeb7d9cfb6852bc72804c689483709cd462cefe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272456821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8379dd9938a642f5c86886be646f52cbba8f18ed6a5f09c0eecba426c3ebe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:42:01 GMT
ADD file:b98dee5937df5f9781b3c514a8c53f6f42fa8016979e581d1252ae689da15ebc in / 
# Tue, 04 Aug 2020 06:42:01 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 10:38:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:39:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 10:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 20:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 20:42:59 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:07:23 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:14:51 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 09 Sep 2020 22:14:53 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:14:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:14:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:14:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:91cc9e0aa8bcda5d45dd8780d9369f22c649c4d8fcd354183a1d0d6a7102744e`  
		Last Modified: Tue, 04 Aug 2020 06:47:56 GMT  
		Size: 49.0 MB (49017231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1447a30fea55273b0a628cb142daba1f5482171d155f458d47b5cadd49079d9`  
		Last Modified: Tue, 04 Aug 2020 10:50:50 GMT  
		Size: 7.2 MB (7231573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2846bcb2ba044284b6ee8c358e6d443ac48b4e01c2e72e0f8bd252128a30a0d`  
		Last Modified: Tue, 04 Aug 2020 10:50:50 GMT  
		Size: 10.0 MB (10015826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb4e1f307e1aa9ad1acfb68478ca06e971c7136b431f8d954ac34b08301dd7a`  
		Last Modified: Tue, 04 Aug 2020 10:51:40 GMT  
		Size: 50.8 MB (50842110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c52db771909adccb0c2e856f6f758b5cd8ee4c13737741bc18882f8f97544ea`  
		Last Modified: Tue, 04 Aug 2020 21:07:17 GMT  
		Size: 54.6 MB (54586297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cff3c9d5e0904b47b9bb4649cbdd5dbeaa8a7c7b47fb69689f65a7fedc9924`  
		Last Modified: Wed, 09 Sep 2020 22:24:23 GMT  
		Size: 100.8 MB (100763659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e8fc63e9b3914623640a429cff6f232998ec738dddd82b137d74057b479fad`  
		Last Modified: Wed, 09 Sep 2020 22:23:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:7cd50da530ba3c518f71bcce6d6514471ff33e1ff830147663dd0d6d947e51af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300608304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09737dfa3730cd36aa0f92acd8558c07562012af72cdedc9a214e3b4a0f49d15`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:44:59 GMT
ADD file:7cc5195cf323fbee8e0c74a76984198dca35599ab18b1ecc5639fa719326bd35 in / 
# Tue, 04 Aug 2020 04:45:05 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:12:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:13:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 07:15:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 18:53:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 18:53:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:19:17 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:20:08 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 09 Sep 2020 22:20:42 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:20:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:21:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:21:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:db4e2d8d5901311f959f0a2271be587f91ea2826238f2a17347ffab142413f53`  
		Last Modified: Tue, 04 Aug 2020 04:52:50 GMT  
		Size: 54.1 MB (54142497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe2d012519ce68bcd2414835909fb4784fd4eb5bea2c88916fdea0c661c872e`  
		Last Modified: Tue, 04 Aug 2020 07:45:05 GMT  
		Size: 8.3 MB (8254809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f1d1f9197bf1817cda35a89da9bd2544ceb7bf0c7b92fba5977ab2b2ab9e6`  
		Last Modified: Tue, 04 Aug 2020 07:45:07 GMT  
		Size: 10.7 MB (10727103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1301750ffb48db80c63d6d21adae9f88f4f4aaf4f561ab3512287683a04c04c0`  
		Last Modified: Tue, 04 Aug 2020 07:45:33 GMT  
		Size: 57.5 MB (57455994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5c6edc9cffc52d437053d5b7d8f834d50534c930afa90b1b3aff08912cddad`  
		Last Modified: Tue, 04 Aug 2020 18:58:15 GMT  
		Size: 73.6 MB (73577651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c67fa95ee88e94d909470c1716d169446a88634f3c7e36dfdd2f6e3f43745fb`  
		Last Modified: Wed, 09 Sep 2020 22:38:50 GMT  
		Size: 96.5 MB (96450093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8ff98dd860534b1ef43864108ba354e5b46c7645da4389c787a9174cd1ed89`  
		Last Modified: Wed, 09 Sep 2020 22:36:57 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; s390x

```console
$ docker pull golang@sha256:2ad9e34e44166a2b8bdf11e6a8d274735e3e40766c5ccdb136e043aaf26d40df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275531535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab167b85270f4401f3f210443043166b3f41eba268ddc817cc066029cc868932`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:42:11 GMT
ADD file:67eedff26215ed3c8100b93d0201c563ec8efe2af7bdfff5c7717037f95057af in / 
# Wed, 09 Sep 2020 23:42:15 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 04:39:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 04:39:51 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 04:39:52 GMT
ENV GOLANG_VERSION=1.15.2
# Thu, 10 Sep 2020 04:40:02 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Sep 2020 04:40:07 GMT
ENV GOPATH=/go
# Thu, 10 Sep 2020 04:40:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 04:40:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Sep 2020 04:40:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4c594945c9b37f16bdb296d1c06754e5bbcc3c28a736d7aa6091f61a081b3cfb`  
		Last Modified: Wed, 09 Sep 2020 23:46:12 GMT  
		Size: 49.0 MB (48966294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e127f29ba8a9174c7c67de6a285e78af9f06c2c36fed6521332d7854917d2782`  
		Last Modified: Thu, 10 Sep 2020 00:12:13 GMT  
		Size: 7.4 MB (7385208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e209a7f0db80455bc526e00593053bd27892e74f2f355899c7b05b2f8b74dce1`  
		Last Modified: Thu, 10 Sep 2020 00:12:13 GMT  
		Size: 9.9 MB (9882116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d094fc7b8815cbefc16bd1eb31d1052bf6fa6016dbaf460808e7a49665906c`  
		Last Modified: Thu, 10 Sep 2020 00:12:27 GMT  
		Size: 51.4 MB (51380064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40237c894313b226af675481b48e6b85ef4294d631e6b7a087be64fb583afbf`  
		Last Modified: Thu, 10 Sep 2020 04:41:31 GMT  
		Size: 56.7 MB (56736965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86fcc2be5e4c718221356b2b5831c09c944f03ef18f638abd3b9e87e7c6db84`  
		Last Modified: Thu, 10 Sep 2020 04:41:36 GMT  
		Size: 101.2 MB (101180731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9402dff5d57a5926e4cb83a0422f253922f41ff9d10226ef213be9617a9a3db2`  
		Last Modified: Thu, 10 Sep 2020 04:41:23 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
