## `golang:1-alpine3.14`

```console
$ docker pull golang@sha256:c2bdb276b6bc67bb46bcca5f4dd6d1c9f004945af49a1111a504b0c11dee734b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `golang:1-alpine3.14` - linux; amd64

```console
$ docker pull golang@sha256:b23ea285284ad120e7803ec27473eaf0558719721f935a5246b1dda28041a051
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108895395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ee2d6efe01c99f6945d62bfd3db2777a3426513ad7a804f76f6c53006bc914`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 23:20:03 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 16 Jun 2021 23:20:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 16 Jun 2021 23:20:04 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:20:46 GMT
ENV GOLANG_VERSION=1.16.7
# Thu, 05 Aug 2021 21:22:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 05 Aug 2021 21:22:25 GMT
ENV GOPATH=/go
# Thu, 05 Aug 2021 21:22:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:22:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Aug 2021 21:22:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8dd7cab73593e079aa6f5b2fe6c2adfe09761320c162696f8fbdc9d81c99e6`  
		Last Modified: Fri, 25 Jun 2021 23:16:30 GMT  
		Size: 281.5 KB (281504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cac70760d29a8ed86a3f007ed2410ef62cc877ddd2ceaa3e10806664fb3d1d1`  
		Last Modified: Fri, 25 Jun 2021 23:16:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bed4a2fc62b9bba0049707854f81b64139584635da1b224c1194ce6a1c77161`  
		Last Modified: Thu, 05 Aug 2021 21:30:54 GMT  
		Size: 105.8 MB (105802101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df72cc8d455ddaa511a7c4a07619dccca830375848f7ec5e43a85e227d56938d`  
		Last Modified: Thu, 05 Aug 2021 21:30:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.14` - linux; arm variant v6

```console
$ docker pull golang@sha256:4be3306149cfe83dc3646b6148dd321a89689d4ccb23d5a8e1e0cdf1b042ed29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104910380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ace6cf801f0e992ef12c1cc5ca8d497e021acdeee11cd8ab955e45ec135168`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 23:25:26 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 30 Jul 2021 23:25:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 23:25:28 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:52:08 GMT
ENV GOLANG_VERSION=1.16.7
# Thu, 05 Aug 2021 21:54:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 05 Aug 2021 21:54:51 GMT
ENV GOPATH=/go
# Thu, 05 Aug 2021 21:54:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:54:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Aug 2021 21:54:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee4cd6a3575f62b66b55378e8df90b574acef888f014ed6645fb7e65ab96305`  
		Last Modified: Fri, 30 Jul 2021 23:49:38 GMT  
		Size: 281.7 KB (281685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fb9aa0b9a1892ff11e3a1a6dc8aa4bbb98d0f6f7ab33ad1cfea51e62e2fdf1`  
		Last Modified: Fri, 30 Jul 2021 23:49:38 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b61fea7971882665351d032a1f0450b025ac44b3b35bb6b68b403f9109cb4ce`  
		Last Modified: Thu, 05 Aug 2021 22:06:51 GMT  
		Size: 102.0 MB (102004007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fc743dfc4d5087c220784c7ce7c2722b9c7e9752ffe6ed40caeedf1848d492`  
		Last Modified: Thu, 05 Aug 2021 22:05:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.14` - linux; arm variant v7

```console
$ docker pull golang@sha256:a9831c2374046b9f6936fa81bf7ca5c3ac9535b830d973b714d184c1df4509ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104527996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d152db7d3c4489653c9086fd5198e3ef46fd3aae292e1e11111cd1856d0d4c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:16:42 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 31 Jul 2021 02:16:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 02:16:44 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jul 2021 02:24:14 GMT
ENV GOLANG_VERSION=1.16.6
# Sat, 31 Jul 2021 02:26:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.6.src.tar.gz'; 	sha256='a3a5d4bc401b51db065e4f93b523347a4d343ae0c0b08a65c3423b05a138037d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Sat, 31 Jul 2021 02:26:46 GMT
ENV GOPATH=/go
# Sat, 31 Jul 2021 02:26:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jul 2021 02:26:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 31 Jul 2021 02:26:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2293fcf302bd1c93bbefaa98b7b505b77efbeb6a1f9b2370158ff8c94f91f7ba`  
		Last Modified: Sat, 31 Jul 2021 02:39:30 GMT  
		Size: 280.8 KB (280833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cf85907084277f615f76a3d1b97d81a0639c29366880610eae30cf45bfc7d5`  
		Last Modified: Sat, 31 Jul 2021 02:39:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f82974acb5bea8902333c360c81acceb501f0fd275a1c91a612316978940c15`  
		Last Modified: Sat, 31 Jul 2021 02:43:56 GMT  
		Size: 101.8 MB (101818937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd152bafb12a2f0143078f0621ffc060b9fb3f5bb07855951b7afa26d1604d1`  
		Last Modified: Sat, 31 Jul 2021 02:42:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b4e29177e535c8a91afb1a04522f340dc4964bcb6e4cd6ea999a8e2c9ba3a4aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104115311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0da18e32313375f81481308ac0275e2a357c8c6df9b870a9e92027d0abfe176`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 23:52:32 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 16 Jun 2021 23:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 16 Jun 2021 23:52:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:40:54 GMT
ENV GOLANG_VERSION=1.16.7
# Thu, 05 Aug 2021 21:42:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 05 Aug 2021 21:42:16 GMT
ENV GOPATH=/go
# Thu, 05 Aug 2021 21:42:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:42:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Aug 2021 21:42:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ad96702509b3443881ad70a623b6184f9936c6b4cd986694020c95f3a4441c`  
		Last Modified: Fri, 25 Jun 2021 22:11:26 GMT  
		Size: 281.7 KB (281671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705bf5f5ed4dc23e2dc33456ba3ccbef3ecabf22614e760a8f4c1e3a93a6c59b`  
		Last Modified: Fri, 25 Jun 2021 22:11:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4445395e5c9e4ed8441e50aae9ef07ddf209fcdb1b44ca00a6c000bd8890af0d`  
		Last Modified: Thu, 05 Aug 2021 21:51:16 GMT  
		Size: 101.1 MB (101123705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6fa344bb6127326aaca0ed73edf8e362f96abeb7481fc8fd3e1661edead6a`  
		Last Modified: Thu, 05 Aug 2021 21:51:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.14` - linux; 386

```console
$ docker pull golang@sha256:7812e21cb8e182d35eeaf3e616c2f1487818f6101c2bc6d4fa3d2590b819fcf1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114048463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3ba5bb1b3c3841c9a2473e631641e8f2907207cb8d9b0cde29c442e067f72e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jun 2021 21:38:30 GMT
ADD file:3b0fe1454491bb05e218b090fd461f2fd39546aa4a53eb3f953ee8eae149ac57 in / 
# Tue, 15 Jun 2021 21:38:30 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 23:38:52 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 16 Jun 2021 23:38:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 16 Jun 2021 23:38:53 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:41:08 GMT
ENV GOLANG_VERSION=1.16.7
# Thu, 05 Aug 2021 21:43:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 05 Aug 2021 21:43:53 GMT
ENV GOPATH=/go
# Thu, 05 Aug 2021 21:43:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:43:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Aug 2021 21:43:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:be21df321efb39c5daf3151073ebff7688e15ea6cd5158878bc9559a5db76ac6`  
		Last Modified: Tue, 15 Jun 2021 21:39:16 GMT  
		Size: 2.8 MB (2820718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697021a242206f31b97863404cd60a096d9ce085a503c527b73071f3b0ed0114`  
		Last Modified: Fri, 25 Jun 2021 18:50:28 GMT  
		Size: 282.1 KB (282050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b62be503967949940d0d99d3e7690039c54be136ff7ac898f44908401328bd0`  
		Last Modified: Fri, 25 Jun 2021 18:50:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d70cf5af442887d9897e5b577a48170ce4e2df5d04562570fbd6500477105de`  
		Last Modified: Thu, 05 Aug 2021 22:06:49 GMT  
		Size: 110.9 MB (110945386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c633792707db8b95d8ac1dc5b60504309973562ac1dea9dd9fbe81f8e99e39`  
		Last Modified: Thu, 05 Aug 2021 22:06:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine3.14` - linux; ppc64le

```console
$ docker pull golang@sha256:73fc27553eb31e9995d39889cbf419b495b0cec898a5c1236edd4222859e4175
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102684959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f33134d7bed4bf359bae727b9513de836c38c7419a8d1976daf3d4a38cee60d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 Jul 2021 17:24:32 GMT
ADD file:0075aad7a94f0496483442bb2d9fdaa13e9c23087b90638d014b4bc263aa3861 in / 
# Fri, 30 Jul 2021 17:24:37 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 01:16:34 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 31 Jul 2021 01:16:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 01:16:51 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jul 2021 01:24:44 GMT
ENV GOLANG_VERSION=1.16.6
# Sat, 31 Jul 2021 01:26:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.6.src.tar.gz'; 	sha256='a3a5d4bc401b51db065e4f93b523347a4d343ae0c0b08a65c3423b05a138037d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Sat, 31 Jul 2021 01:26:49 GMT
ENV GOPATH=/go
# Sat, 31 Jul 2021 01:26:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jul 2021 01:27:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 31 Jul 2021 01:27:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:baf144cfb66ebe9df1969f3b90f1c448beff98edc84de1ccb5d6346195a070d4`  
		Last Modified: Tue, 15 Jun 2021 22:27:38 GMT  
		Size: 2.8 MB (2810478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eadb6e3bae87450b70c1b4112cefea93f12177ad5236832e0d2445acfa20c0`  
		Last Modified: Sat, 31 Jul 2021 01:36:11 GMT  
		Size: 283.6 KB (283642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae8be7dbe7108ce370cc1a1009f59d387bcc9efba97aa7b5a41b6b9834bee54`  
		Last Modified: Sat, 31 Jul 2021 01:36:11 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e033b571854f677774dbe66bbc759fcd32b92b8c08ae957c1df3d50ed974b8ea`  
		Last Modified: Sat, 31 Jul 2021 01:37:45 GMT  
		Size: 99.6 MB (99590530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20c767004436d15bb347d522b2469009eac3312615cae0982bbf1aee03684c3`  
		Last Modified: Sat, 31 Jul 2021 01:37:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
