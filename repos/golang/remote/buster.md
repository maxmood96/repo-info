## `golang:buster`

```console
$ docker pull golang@sha256:df8293c088b77115cefbf50840e37526a8d3b72e2a8a9c4651dc0f7970aeae89
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

### `golang:buster` - linux; amd64

```console
$ docker pull golang@sha256:0978cc067eb3f53901c00b70a024f182baa371bdfe7f35f3d64e56cab2471c4d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.9 MB (309857505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c8f6d2538a44fd9b6910058b44ae9c0dad98eea3b66277832490d4f5d914ab`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:59:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:59:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:59:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 21:26:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 21:26:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 21:26:57 GMT
ENV GOLANG_VERSION=1.15.2
# Thu, 10 Sep 2020 21:27:08 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Sep 2020 21:27:08 GMT
ENV GOPATH=/go
# Thu, 10 Sep 2020 21:27:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 21:27:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Sep 2020 21:27:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e126169501d71bbbd0d3c8d9f35836c41660869fe8432ac606341ed21f7adb`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 7.8 MB (7811567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af28a55c3f320826db8df3146a2c198f9042877ef679f9e32210aa9a7fac9ef`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 10.0 MB (9996317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f1c9932170e54fface2382b2550b8052ae3d41f27e66ea1294e2055dd2b2e7`  
		Last Modified: Thu, 10 Sep 2020 01:15:45 GMT  
		Size: 51.8 MB (51829661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4773b3414236a2e613e862551f8e9afc2f82dbca223b5ccf1d246ac64b2097e`  
		Last Modified: Thu, 10 Sep 2020 21:28:59 GMT  
		Size: 68.7 MB (68672206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb320882041bd24f7bf6dff92d70e075b0065b608425e4fdcd32558fb30b02da`  
		Last Modified: Thu, 10 Sep 2020 21:29:11 GMT  
		Size: 121.2 MB (121151715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b0ad6f94164c2da7091f413a061765642aa9aa4a11dbdcb21cf8d739b5a510`  
		Last Modified: Thu, 10 Sep 2020 21:28:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:d9333fe36307e2c8e7dda90dc90471dd11b0895cea77183eb60841a7a7227ca9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269828712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6190bf7970db36241c1c877f91b8aee22eb17e23f4aa007f076d0bc8c2ad0e75`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:51:29 GMT
ADD file:eba6b86faf02e328fea78037ab4c892a6d231f067cd5e3078ded86fd5a429ff7 in / 
# Tue, 13 Oct 2020 01:51:33 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 03:42:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:43:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 03:44:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 15:53:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 15:53:51 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 15:54:03 GMT
ENV GOLANG_VERSION=1.15.2
# Tue, 13 Oct 2020 16:26:53 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 13 Oct 2020 16:27:06 GMT
ENV GOPATH=/go
# Tue, 13 Oct 2020 16:27:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 16:28:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 13 Oct 2020 16:28:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d80349201e0e0bc9a1bdeb726d9339525972e3d76225d15b87f72414b0aec137`  
		Last Modified: Tue, 13 Oct 2020 02:01:03 GMT  
		Size: 48.1 MB (48108657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4c9d08d8ee472a70c0c7dffb75c54e692061eb72c3b0ddf55669727b29c7d8`  
		Last Modified: Tue, 13 Oct 2020 04:07:24 GMT  
		Size: 7.4 MB (7361059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c03b81470f92875dbe52bf0054ebf042576e7f28903477ad4abe4c4f9734ce`  
		Last Modified: Tue, 13 Oct 2020 04:07:25 GMT  
		Size: 9.7 MB (9687086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b196b0bc956fafcab3622d17314250431b67b84c0d5938dfff3759e02ba97efa`  
		Last Modified: Tue, 13 Oct 2020 04:07:51 GMT  
		Size: 49.6 MB (49571529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4513ea2e624c1315c50d01e77da41c690aab244542fb1424a914e8881e0fefc`  
		Last Modified: Tue, 13 Oct 2020 17:05:41 GMT  
		Size: 52.0 MB (51989911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00976c1d17339a6bcddf7d1fbb1200e7a0a56569ac9f8f73ed07a019bbea0077`  
		Last Modified: Tue, 13 Oct 2020 17:05:55 GMT  
		Size: 103.1 MB (103110314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ead97258ae1ea0b7bf67161442c2b3f02d76838dc93e16cd9c66ad820d9102`  
		Last Modified: Tue, 13 Oct 2020 17:05:22 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:fbb154997c22f218dd80a282a10b9d14d4ae7cd2e485e0c1b21af06113205ef6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260793369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad568ca0c7e075c954ccfa96cbd850fe9a93b04b628ee871712de1f50c58ce8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:07:32 GMT
ADD file:340663c3add65bd8904ba51984e6080c6aa6d237bd845f4e0aa22626d31497b7 in / 
# Thu, 10 Sep 2020 00:07:35 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:39:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:39:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:40:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 21:41:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 21:41:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 21:41:35 GMT
ENV GOLANG_VERSION=1.15.2
# Thu, 10 Sep 2020 21:41:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Sep 2020 21:42:01 GMT
ENV GOPATH=/go
# Thu, 10 Sep 2020 21:42:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 21:42:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Sep 2020 21:42:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d9beb74056b685831827b5f21351f021873d8ba1a1170b378e5edf5f46d114e`  
		Last Modified: Thu, 10 Sep 2020 00:17:29 GMT  
		Size: 45.9 MB (45869299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689ccbaccf1b655191aa8867125206ed64238bf9a9e9839c4b10af714b1226f8`  
		Last Modified: Thu, 10 Sep 2020 02:01:37 GMT  
		Size: 7.1 MB (7097950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadf7011b92214ace9e792fa4ef39707503be7ea5c29200c9e71ac3f6b1afb81`  
		Last Modified: Thu, 10 Sep 2020 02:01:37 GMT  
		Size: 9.3 MB (9343399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa216e44ff17d2fdb02fb4a79ef82fd1042dfaefb74d10c5db403575fbb03fc`  
		Last Modified: Thu, 10 Sep 2020 02:02:02 GMT  
		Size: 47.4 MB (47356064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bbcd8b019bad13f613b7988879fc6dadd23cac2c59e64b74e2decf4d3249eb`  
		Last Modified: Thu, 10 Sep 2020 21:45:04 GMT  
		Size: 53.1 MB (53140962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d721835c0d1029ce8182397244b59714d31aba87d7ab1fb4c368421993ba422`  
		Last Modified: Thu, 10 Sep 2020 21:45:20 GMT  
		Size: 98.0 MB (97985540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e858ae6fd3b1cc5acb726f196b15dd6d2891087ada3d32985be40918c0590799`  
		Last Modified: Thu, 10 Sep 2020 21:44:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7917efe5bfb64dc7025a198eac8574e8e7a09ee25850930a4e122057549d4cca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279276059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeeacca48fc4bc72e213403dc5a7783ee0df2a3b9cf7ce926aa202ab2f3d711`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:21 GMT
ADD file:c8c11e622b1b8a1e31f32e2457ff4d1314d5cd4a7ad22b3991ab9d0542db23fd in / 
# Wed, 09 Sep 2020 23:50:22 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:28:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:28:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:29:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:43:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 19:43:07 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 19:43:08 GMT
ENV GOLANG_VERSION=1.15.2
# Thu, 10 Sep 2020 19:43:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Sep 2020 19:43:43 GMT
ENV GOPATH=/go
# Thu, 10 Sep 2020 19:43:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 19:43:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Sep 2020 19:43:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d3a32671b6316bd11f4bf18cb034394ac94d2bb3bc6d09de388b19b06fb94b91`  
		Last Modified: Wed, 09 Sep 2020 23:58:45 GMT  
		Size: 49.2 MB (49175549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1202c4ddac582c7164a6b65b13a2442759bc04660da9ca7d62fabf75225482`  
		Last Modified: Thu, 10 Sep 2020 00:42:35 GMT  
		Size: 7.7 MB (7681394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f110d64c20212ec5e7a7f0622d610346edbd6e508fde94679db44e0f2827b2f9`  
		Last Modified: Thu, 10 Sep 2020 00:42:34 GMT  
		Size: 10.0 MB (9983858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c41999aa9f871546022553f35d4fbbd39cd2bfe8e1a03cce7b1bd78d2a5b0`  
		Last Modified: Thu, 10 Sep 2020 00:43:02 GMT  
		Size: 52.2 MB (52164372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422b93158f2fdb0f38b0153fb7aaa2fbc32743197a85aaf1e38438c13409497b`  
		Last Modified: Thu, 10 Sep 2020 19:46:48 GMT  
		Size: 62.5 MB (62532110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d50c93f607bbe62f3c1c3310352c31cd21c984e3748d71dc4c8b0ea7133a13`  
		Last Modified: Thu, 10 Sep 2020 19:46:59 GMT  
		Size: 97.7 MB (97738621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd04c7f8ff00ff17374d5457ce112287d7504bcbfe3681ad0c879e2a756db699`  
		Last Modified: Thu, 10 Sep 2020 19:46:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; 386

```console
$ docker pull golang@sha256:1d9e56661ecdb3c8c6501009de05d387196d2619ac227de0fabd03f86ad20381
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (297045280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5bdb06d3fb20213d39b609a0a918c57e5c20da46274592ed81d7c6668613c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:39:58 GMT
ADD file:39c4b1e1e5d34f52ad1f95b26bfbbf45f307b94a52d472a561496c440f96d8a2 in / 
# Wed, 09 Sep 2020 23:39:59 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:49:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:50:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:50:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 16:45:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 16:45:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 16:45:16 GMT
ENV GOLANG_VERSION=1.15.2
# Thu, 10 Sep 2020 16:45:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 10 Sep 2020 16:45:30 GMT
ENV GOPATH=/go
# Thu, 10 Sep 2020 16:45:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 16:45:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 10 Sep 2020 16:45:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c89594b72f230eaccb7faa969906602c0f8e2667b7e30e66fe230243f1b5f1d0`  
		Last Modified: Wed, 09 Sep 2020 23:46:14 GMT  
		Size: 51.2 MB (51158853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b43dae2d508d4201f51ab75f9d5022efec80fbcc75ae14efd5ede61105a473f`  
		Last Modified: Thu, 10 Sep 2020 02:12:26 GMT  
		Size: 8.0 MB (7981208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad363e11f9c57ba13f1890587ea2eca980dd6204b267537d3668aa51dc315834`  
		Last Modified: Thu, 10 Sep 2020 02:12:26 GMT  
		Size: 10.3 MB (10338551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d8672d97325675a30cec8549334e1d5a9cacf2cc89afb39870cec739e2fb80`  
		Last Modified: Thu, 10 Sep 2020 02:12:57 GMT  
		Size: 53.4 MB (53432957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb7d2e866e11cbe8d98f5b7bac5eb4be4b77aacc7aa9a4471e3dc7afbbd936f`  
		Last Modified: Thu, 10 Sep 2020 16:48:05 GMT  
		Size: 73.5 MB (73530817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec4d6b5fbb829cad4f57cc60c8666b00e85453a07d4c04c0f91122363c2af77`  
		Last Modified: Thu, 10 Sep 2020 16:48:12 GMT  
		Size: 100.6 MB (100602768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49779ba68b9e4a2cc1c9b7e0c408c02bab62e51cb8d6236eb951ae78dfd900d1`  
		Last Modified: Thu, 10 Sep 2020 16:47:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; mips64le

```console
$ docker pull golang@sha256:150f9e04d5af01afa5c1e17af92307e0839e2a7ad6e25e30e84cfd2ce7aa6843
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272474443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f85c644fcffc2cc9bd995e9ae92e954ce5e0ed0cd87741395ccac7404778ddd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:09:23 GMT
ADD file:0ad6bbc90b50de1f5a0751fd1da65e211c687820c0339fdd38f12d689638b939 in / 
# Tue, 13 Oct 2020 01:09:24 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:12:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 16:23:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 16:23:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 16:23:21 GMT
ENV GOLANG_VERSION=1.15.2
# Tue, 13 Oct 2020 16:30:58 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 13 Oct 2020 16:30:59 GMT
ENV GOPATH=/go
# Tue, 13 Oct 2020 16:31:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 16:31:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 13 Oct 2020 16:31:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9fd0710976c57d8d2e5a2f13cccd726cca5d8b0f607868465c8cffbdcf2d3940`  
		Last Modified: Tue, 13 Oct 2020 01:15:56 GMT  
		Size: 49.0 MB (49017194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c82d5acaa60d5b36fc634c6b79ed00bee8d08c39b78242c5fe5938754739ab7`  
		Last Modified: Tue, 13 Oct 2020 02:23:13 GMT  
		Size: 7.2 MB (7231586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563cb7b9f3c30fcbb19d79fcfce967a57d35fde75fab6e71be156974ed0c6f5e`  
		Last Modified: Tue, 13 Oct 2020 02:23:14 GMT  
		Size: 10.0 MB (10015783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb7ecbbb9a11d82d8b68ac910eb4d6a536ce23ee4172e81a7166d6b6f22535c`  
		Last Modified: Tue, 13 Oct 2020 02:24:04 GMT  
		Size: 50.8 MB (50842169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d59dde81c0fb34075db3f3333fe270df5548321a70da94193c507ae578bded2`  
		Last Modified: Tue, 13 Oct 2020 16:40:08 GMT  
		Size: 54.6 MB (54603789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cc97eaeecabf92709716f3cdbaf8fe6f54eeba2b21ec82a634b2e5375da8b8`  
		Last Modified: Tue, 13 Oct 2020 16:40:39 GMT  
		Size: 100.8 MB (100763796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903cfc5ea742aa626ab0ee09376958be82e11c27283b48351218198bffda1309`  
		Last Modified: Tue, 13 Oct 2020 16:39:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; ppc64le

```console
$ docker pull golang@sha256:83df6ab8f0d4ced8fe586117eb45b71b2729d514022858d9b4b27a26ed35a079
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300610445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9469b8c934e3f52ee0c41abac60c6a5f13e78eee31a0c99dac52b40d35e15a21`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:04:56 GMT
ADD file:a2329a0372b3b40ca345795d86a78ab4cdaa3a1eeda3a5ece35a83881543db1a in / 
# Thu, 10 Sep 2020 01:05:18 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:56:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 02:58:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 03:04:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Sep 2020 03:44:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Sep 2020 03:44:28 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 03:44:36 GMT
ENV GOLANG_VERSION=1.15.2
# Fri, 11 Sep 2020 03:45:21 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 11 Sep 2020 03:45:37 GMT
ENV GOPATH=/go
# Fri, 11 Sep 2020 03:45:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 03:45:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 11 Sep 2020 03:46:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aff7fe9e9819c2b9d4338fae03bd06eb6784016bcf53b2eeab88c21e47dea428`  
		Last Modified: Thu, 10 Sep 2020 01:26:27 GMT  
		Size: 54.1 MB (54142644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6ac2eaf169d79a8354a5aaf6bab62ffaf296672724b4dd0027129293ddadf9`  
		Last Modified: Thu, 10 Sep 2020 04:10:06 GMT  
		Size: 8.3 MB (8255018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a742b7f13bb5936990b399882cff555713c042bbc82bb798fb24d1910e772a5e`  
		Last Modified: Thu, 10 Sep 2020 04:10:07 GMT  
		Size: 10.7 MB (10727473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8644560ef7f8ccfd3073c9565885e70b26ed53108382c857d5d058bf92136a`  
		Last Modified: Thu, 10 Sep 2020 04:12:27 GMT  
		Size: 57.5 MB (57456465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29bd249b03e8b33f2fa749b7e480f92f3c28e2daa686066c12d39f0ff55c1d1`  
		Last Modified: Fri, 11 Sep 2020 03:49:39 GMT  
		Size: 73.6 MB (73578600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730a93d3528b9607bbde43aa9bef64a84ab0728932fb9c3901c66d7e6b55d902`  
		Last Modified: Fri, 11 Sep 2020 03:49:46 GMT  
		Size: 96.5 MB (96450090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5060c4e9b38dc6338d09b3892a152bceed8d67b0f95179eaa2c35a15c7c62f0b`  
		Last Modified: Fri, 11 Sep 2020 03:49:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; s390x

```console
$ docker pull golang@sha256:723d2ee4e1f1310e4cd815079e05fb76063a4f469a0420937fb475481d6b9c7b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275545947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a8d726490c1627c02b7b993c8fb55eb2233c9cca7fe68fafa4fb9432d0a78c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:06 GMT
ADD file:cc8968c8733f7fb6fb644b948e4a21999440d079560afbb2acb9d666de3886ec in / 
# Tue, 13 Oct 2020 01:42:09 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:06:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:06:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:06:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 11:49:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 11:49:16 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 11:49:16 GMT
ENV GOLANG_VERSION=1.15.2
# Tue, 13 Oct 2020 11:49:32 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			arch='linux-amd64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-amd64.tar.gz'; 			sha256='b49fda1ca29a1946d6bb2a5a6982cf07ccd2aba849289508ee0f9918f6bb4552'; 			;; 		'armhf') 			arch='linux-armv6l'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-armv6l.tar.gz'; 			sha256='c12e2afdcb21e530d332d4994919f856dd2a676e9d67034c7d6fefcb241412d9'; 			;; 		'arm64') 			arch='linux-arm64'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-arm64.tar.gz'; 			sha256='c8ec460cc82d61604b048f9439c06bd591722efce5cd48f49e19b5f6226bd36d'; 			;; 		'i386') 			arch='linux-386'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-386.tar.gz'; 			sha256='5a91080469df6b91f1022bdfb0ca75e01ca50387950b13518def3d0a7f6af9f1'; 			;; 		'ppc64el') 			arch='linux-ppc64le'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-ppc64le.tar.gz'; 			sha256='85fc130046f41105b50a0647d1da395d615eac0aefca8776be148800c872c8db'; 			;; 		's390x') 			arch='linux-s390x'; 			url='https://storage.googleapis.com/golang/go1.15.2.linux-s390x.tar.gz'; 			sha256='30f7856323965c6bf8886f8e5ae19d250cc73a10d382948fa78ecb3ace3980b9'; 			;; 		*) 			arch='src'; 			url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 			sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 			echo >&2; 			echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 			echo >&2; 			;; 	esac; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$arch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 13 Oct 2020 11:49:38 GMT
ENV GOPATH=/go
# Tue, 13 Oct 2020 11:49:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 11:49:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 13 Oct 2020 11:49:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dcbd85f88306d080bce94006a992947eaf462efa80b07c202b0514e6ef412fdf`  
		Last Modified: Tue, 13 Oct 2020 01:45:28 GMT  
		Size: 49.0 MB (48966292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbb6631e0a71a71f08faafe174e0f83ad00c87d97301c2bb19333675f52b630`  
		Last Modified: Tue, 13 Oct 2020 02:11:23 GMT  
		Size: 7.4 MB (7385264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2d271697ef75e40cfaf5639cbd0b5730ebe44e841fa156ed503f5c3395c07`  
		Last Modified: Tue, 13 Oct 2020 02:11:24 GMT  
		Size: 9.9 MB (9882087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee6330fdd3fb2bbdaee3b0cf6e327884e191d85e257c9d94345c55dbf83b5e`  
		Last Modified: Tue, 13 Oct 2020 02:11:38 GMT  
		Size: 51.4 MB (51379788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d95435a5ed135058e1ecb863d16380fbe6fec384761bfc8b95ab54dd59869b`  
		Last Modified: Tue, 13 Oct 2020 11:50:45 GMT  
		Size: 56.8 MB (56751650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed7111894892d2d6f3e25101285e89ddf4c1d5e2bd5fc17b983689521a160c`  
		Last Modified: Tue, 13 Oct 2020 11:50:50 GMT  
		Size: 101.2 MB (101180710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3bed25b34e78fe6363ccd99896b53004c7907c37fd88f695e31622ae913a30`  
		Last Modified: Tue, 13 Oct 2020 11:50:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
