## `caddy:2-builder`

```console
$ docker pull caddy@sha256:16450c5118cda1aa2b8934afd0c9fc93864413ae49c461127f512fe9826d68c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:c6a42d4224bcbc1aa0d2671eb97d2f06a439c36386eedc5d280f8d8cac870ac2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (306011968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eae05b9c152023f118a7b41498c3413fc036dd459dd8cb0b6d3f901e3ddad7b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:40:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:22:58 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:25:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:25:12 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:25:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:25:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:25:13 GMT
WORKDIR /go
# Wed, 09 Sep 2020 22:46:24 GMT
WORKDIR /src
# Wed, 09 Sep 2020 22:46:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 09 Sep 2020 22:46:26 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 09 Sep 2020 22:46:28 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 09 Sep 2020 22:46:28 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 09 Sep 2020 22:46:55 GMT
RUN go get -d ./...
# Wed, 09 Sep 2020 22:46:57 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 09 Sep 2020 22:46:57 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0547b08c8963faeee9d579d8351699f769179aa7a58ada0290e6ab8f5a676c`  
		Last Modified: Wed, 09 Sep 2020 22:30:12 GMT  
		Size: 107.4 MB (107371657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b6f0657434294654385190364b1a7c9af2a6f7b7ef0e821b8d51e20cdd8da5`  
		Last Modified: Wed, 09 Sep 2020 22:29:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f980c0941f345f6e2bea099934d861e844bc878396f9e95b425cdacf969a2815`  
		Last Modified: Wed, 09 Sep 2020 22:47:13 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e601915031b79952a33dafb7515134d728a30295c6f0c269bd6ed347753d6e`  
		Last Modified: Wed, 09 Sep 2020 22:47:14 GMT  
		Size: 8.3 MB (8310036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55de90b62b6b63d79c1b0449a3b5b3ae59fe19f70cce318a51ddb32bcecb8305`  
		Last Modified: Wed, 09 Sep 2020 22:47:12 GMT  
		Size: 3.0 MB (3018197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d779c3f8e871ce33b2daa7edc47e877d7eb18207a9707540088c581e49e764c`  
		Last Modified: Wed, 09 Sep 2020 22:47:46 GMT  
		Size: 184.2 MB (184230897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7817237c1f4eeca376d869f4f339d9631fea2a626190b431ddd23fa7135b54e`  
		Last Modified: Wed, 09 Sep 2020 22:47:12 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff33af75dd2537d1113713133abb0aa2309dd380964987be7e08bda4f2d8475`  
		Last Modified: Wed, 09 Sep 2020 22:47:12 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:90e5ec60900a30c987c06bd8351a60c3831e1f6174caa8acad53eaba9c1c058e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301787869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff83d67e33fd4e4345a625cbcaf782fb6631bb7e3acdde4c1b78e1ed7a39c39`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:51:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:54:15 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:57:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:57:19 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:57:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:57:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:57:23 GMT
WORKDIR /go
# Wed, 09 Sep 2020 23:18:57 GMT
WORKDIR /src
# Wed, 09 Sep 2020 23:19:00 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 09 Sep 2020 23:19:01 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 09 Sep 2020 23:19:03 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 09 Sep 2020 23:19:04 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 09 Sep 2020 23:19:48 GMT
RUN go get -d ./...
# Wed, 09 Sep 2020 23:19:56 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 09 Sep 2020 23:19:57 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6fe6c5f0fa89cff72714190eb250d37035e32c7216624ea20cfcdfc88d8932`  
		Last Modified: Wed, 09 Sep 2020 23:02:32 GMT  
		Size: 103.7 MB (103712873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186bd058112580f710efc27a0aae302bc22b6933011ca92545db5a513ddde4c0`  
		Last Modified: Wed, 09 Sep 2020 23:02:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd397f94f141bae6ded3b8214f6110d80dc00d0ecf9ddef507d79894a47919f`  
		Last Modified: Wed, 09 Sep 2020 23:20:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d09780d3f5ad562a835d8bb15c67e4bd59406c7425f41b7f98a790d082039f`  
		Last Modified: Wed, 09 Sep 2020 23:20:16 GMT  
		Size: 7.9 MB (7928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60355ccb513fab7d8bb83c8cc017903818b391069f816e3a0279b299a3972f22`  
		Last Modified: Wed, 09 Sep 2020 23:20:13 GMT  
		Size: 3.0 MB (3022076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab0b979ca808d239596bf34c983260643fbd5374e4fa9ad61679fb632cbea1c`  
		Last Modified: Wed, 09 Sep 2020 23:20:57 GMT  
		Size: 184.2 MB (184236874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40612d06549d6b11fd1d0cf5cd146540e6ab04bb059e4c0a341163e29bbd386d`  
		Last Modified: Wed, 09 Sep 2020 23:20:12 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ffbb030b4179d885102c4a784086e9546524fd618a5f8f098175cabdec5bbd`  
		Last Modified: Wed, 09 Sep 2020 23:20:12 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7eefa86defbd314e38f66a52e2088430aa9849c52321c5de4031b8b525af3aab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300559812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acb6f0c9bdc5fcee0387fbb1476e819c3b669cc1bd96063104004575f95bc2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:46:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:05:40 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:07:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:07:51 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:07:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:07:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:07:54 GMT
WORKDIR /go
# Wed, 09 Sep 2020 22:30:49 GMT
WORKDIR /src
# Wed, 09 Sep 2020 22:30:52 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 09 Sep 2020 22:30:52 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 09 Sep 2020 22:30:55 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 09 Sep 2020 22:30:56 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 09 Sep 2020 22:31:44 GMT
RUN go get -d ./...
# Wed, 09 Sep 2020 22:31:52 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 09 Sep 2020 22:31:52 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189358c25ed3947ca4fd93936880bae2e9a32a62f75d865d03db0ce536130f63`  
		Last Modified: Wed, 09 Sep 2020 22:14:22 GMT  
		Size: 103.5 MB (103462777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a5f301bfa0a4263c5e4fd043d781161d2579b6d5ac42d3a18287f1452e4194`  
		Last Modified: Wed, 09 Sep 2020 22:13:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627fae0811bf183e71d577ae5c25b7231850907cf5657027a2276754993ad359`  
		Last Modified: Wed, 09 Sep 2020 22:32:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f15eb32ecbdabe764b8485a4a137b40d9bb510b36fb58b19c4860b1aa3b66e`  
		Last Modified: Wed, 09 Sep 2020 22:32:17 GMT  
		Size: 7.1 MB (7144998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9ac55041b3869f979a1080d8e43f8d238ba533c561e1003b54aacd2bce0b10`  
		Last Modified: Wed, 09 Sep 2020 22:32:16 GMT  
		Size: 3.0 MB (3022109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990eaa3e8964d6482ef1e27a21997a4edc1a01d94e1a9b4c0a4dc1fbe3a9dc84`  
		Last Modified: Wed, 09 Sep 2020 22:33:01 GMT  
		Size: 184.2 MB (184240143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dc787416c2c469678e1e5f622edf0b61d332cc35e224d63e818d50a488b6a2`  
		Last Modified: Wed, 09 Sep 2020 22:32:15 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b8026d3dfebac1b5186b3c3a99b251d0905e643e9d1f1606f4ee5e8dcad2f2`  
		Last Modified: Wed, 09 Sep 2020 22:32:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:717015810b86bf461e53dc244b53947fbc7a1f71b64732f8a718a822e6b5187d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301563276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376db6534da4c0bfb8aad0f04b914f4758108b57b1ddec92d0f75b3fdf7b2c20`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:22 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:45:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:45:10 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:45:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:45:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:45:14 GMT
WORKDIR /go
# Wed, 09 Sep 2020 23:07:23 GMT
WORKDIR /src
# Wed, 09 Sep 2020 23:07:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 09 Sep 2020 23:07:26 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 09 Sep 2020 23:07:29 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 09 Sep 2020 23:07:30 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 09 Sep 2020 23:08:15 GMT
RUN go get -d ./...
# Wed, 09 Sep 2020 23:08:22 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 09 Sep 2020 23:08:23 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aee363a75d12710f67004978ba4509d1ddb769cc47ba518bc277ecd103a6b8d`  
		Last Modified: Wed, 09 Sep 2020 22:51:01 GMT  
		Size: 102.8 MB (102811724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab2d6f42095309ce47a6ec4edd38bd86aabe0fb28a18cb007652d42e0f19e0`  
		Last Modified: Wed, 09 Sep 2020 22:50:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5489d969be50d3033392e45f0052fb16b683933184e54bd6dc90a7836630f9bd`  
		Last Modified: Wed, 09 Sep 2020 23:08:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2605dc1c7f70c44d1833597873e877f6c60ee04cba8abf125bf40e6c7d473dbd`  
		Last Modified: Wed, 09 Sep 2020 23:08:40 GMT  
		Size: 8.5 MB (8499918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d068ddd7d6434e06055a366bc9e5252ebe01b49bf8b2d9877f9906db1294a`  
		Last Modified: Wed, 09 Sep 2020 23:08:39 GMT  
		Size: 3.0 MB (3018223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcaf2776515e62eb5a9cf01d1c1631d613fb1080c601baa44c29770df447c04`  
		Last Modified: Wed, 09 Sep 2020 23:09:16 GMT  
		Size: 184.2 MB (184241320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430830f0fb8086c376793d765be00c6a226da704f9630a333e1a3018e9c5efbd`  
		Last Modified: Wed, 09 Sep 2020 23:08:39 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a903bbf5561bf05e968292470a38298e42f48afbef9b0203954316e7fe6d8e8`  
		Last Modified: Wed, 09 Sep 2020 23:08:39 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3f4cb30c6502ec2ff6ec3fa211bb84c01b260969e892a3f8599edf31c5977cea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300951497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4440d71ff6b1d6f7f0ab958da228bc2d958e1ee40c863c011d7196d72c0a44`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 01:38:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:26:40 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:29:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:29:52 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:29:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:30:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:30:39 GMT
WORKDIR /go
# Wed, 09 Sep 2020 23:01:13 GMT
WORKDIR /src
# Wed, 09 Sep 2020 23:01:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 09 Sep 2020 23:01:31 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 09 Sep 2020 23:01:45 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 09 Sep 2020 23:01:53 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 09 Sep 2020 23:08:24 GMT
RUN go get -d ./...
# Wed, 09 Sep 2020 23:08:34 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 09 Sep 2020 23:08:43 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba569e5c85b1b70b3985f097dd79fee89c81c111899c623098e368323e560524`  
		Last Modified: Wed, 09 Sep 2020 22:44:05 GMT  
		Size: 101.7 MB (101676592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826cb177af69484b6f3437a2174165ac7a6c677d76f72e742f049397fb1fe2df`  
		Last Modified: Wed, 09 Sep 2020 22:43:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18250f29498ec73e2ddfef536b10a494834e99da6b938037fecd9f94e386105`  
		Last Modified: Wed, 09 Sep 2020 23:09:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ed76b1419d6b1a5c79669d485991765fb3e2e85ff1646a9a9881738e6f9e2d`  
		Last Modified: Wed, 09 Sep 2020 23:09:13 GMT  
		Size: 8.9 MB (8920013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f641502fd10f29dac58992a2d912c15543f52beed8a2e94c366f048d75f82412`  
		Last Modified: Wed, 09 Sep 2020 23:09:13 GMT  
		Size: 3.0 MB (3018870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428661f93ba3d47996eff0cfadaad0939e596d8c80418ed72c11118bef48b542`  
		Last Modified: Wed, 09 Sep 2020 23:09:39 GMT  
		Size: 184.2 MB (184244659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c8eddd4fb8576ce08a8d2c4d19ca69af18125ab0aea66e5ea209e9686f11ff`  
		Last Modified: Wed, 09 Sep 2020 23:09:12 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7c2fd8cee6e0b035ef2d5f127b71624a0047bd309476b3761549dbbc091bdc`  
		Last Modified: Wed, 09 Sep 2020 23:09:10 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:1c4c9e94d1f1fa36400a42c26efa6b0bb06b60072f31e2011c7ed1d6899e67fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305706045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d86f5ded96bbb8bedc72304d2f4ce10bb466e18c23f60926b7f81ad8bdd61ce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:53:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:55 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:45:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:45:07 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:45:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:45:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:45:08 GMT
WORKDIR /go
# Wed, 09 Sep 2020 23:04:23 GMT
WORKDIR /src
# Wed, 09 Sep 2020 23:04:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 09 Sep 2020 23:04:25 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 09 Sep 2020 23:04:28 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 09 Sep 2020 23:04:28 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 09 Sep 2020 23:04:43 GMT
RUN go get -d ./...
# Wed, 09 Sep 2020 23:04:51 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 09 Sep 2020 23:04:51 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e7f0b644229c4d22243efaf9cde7728d52c4624e9d48ab2d5174ec187de5f9`  
		Last Modified: Wed, 09 Sep 2020 22:48:16 GMT  
		Size: 107.3 MB (107254107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b1ab98332292b26f0fee8484fc91221c2e937011cbcd0fa39c2b7f8b32252e`  
		Last Modified: Wed, 09 Sep 2020 22:48:03 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532f23f71a0518243acc85fd6f986818a0731f1234eb2e447d27cbe9f0ad9cdf`  
		Last Modified: Wed, 09 Sep 2020 23:05:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbc25f41a54e52aa69fcedd6a1d68a07d7c2357cf2d3325a93729306cad2a44`  
		Last Modified: Wed, 09 Sep 2020 23:05:07 GMT  
		Size: 8.4 MB (8352244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dc2c684cdfce8879b83944ce50659293c1672ef6f2289aeae6d5e26105ed53`  
		Last Modified: Wed, 09 Sep 2020 23:05:06 GMT  
		Size: 3.0 MB (3018172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ccaf1327d9e8c98f2135737060be2354164f2df682f4859dded7b22eb77fa6`  
		Last Modified: Wed, 09 Sep 2020 23:05:22 GMT  
		Size: 184.2 MB (184231058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89169387514d2f97acab2cb25524f5527d305110cd42e754b3c8a8c476b99962`  
		Last Modified: Wed, 09 Sep 2020 23:05:06 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014ad4ec30dc130d7bf579221c2331ee49316addfd281e3d3dc1c38c9a1b5bee`  
		Last Modified: Wed, 09 Sep 2020 23:05:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
