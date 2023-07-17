## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:c3db1fad2e1d04e8898d90ebebea68e75dc0d36f6a6699ddd14dcee761dae99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:045c42bf437d1299a92cb1d236cb7eff143ad57fb0bcbf542918eba7c1231e4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110884721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb47caf0927823b5f2368e4ee45b0f6d72f69e3174d1b96db8a6da722563cbe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:35:02 GMT
RUN apk add --no-cache ca-certificates
# Wed, 14 Jun 2023 22:35:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:20:25 GMT
ENV GOLANG_VERSION=1.20.6
# Thu, 13 Jul 2023 20:30:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.6.src.tar.gz'; 		sha256='62ee5bc6fb55b8bae8f705e0cb8df86d6453626b4ecf93279e2867092e0b7f70'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 20:30:32 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 20:30:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 20:30:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 20:30:32 GMT
WORKDIR /go
# Thu, 13 Jul 2023 22:11:34 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 22:11:34 GMT
ENV XCADDY_VERSION=v0.3.4
# Mon, 17 Jul 2023 21:19:40 GMT
ENV CADDY_VERSION=v2.6.4
# Mon, 17 Jul 2023 21:19:40 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 17 Jul 2023 21:19:40 GMT
ENV XCADDY_SETCAP=1
# Mon, 17 Jul 2023 21:19:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 17 Jul 2023 21:19:42 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 17 Jul 2023 21:19:42 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9bcf943fa5571df036dca6da19434d38edf546ef8bb04ddbc803634cc9a3b8`  
		Last Modified: Wed, 14 Jun 2023 22:42:14 GMT  
		Size: 284.7 KB (284706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd371fdf0be1f3f0149451e08183a8bb178e63b4360e6691f07dccf51f0dc7f`  
		Last Modified: Thu, 13 Jul 2023 20:37:30 GMT  
		Size: 100.9 MB (100942716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add974993529c266bf715fdeb763bf86e7a45dc0405d68fbe483a4428c59b55d`  
		Last Modified: Thu, 13 Jul 2023 20:37:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6789097faeb3a011c86d5ea50cf331495de5a8a0e23e5649ddd53270b553a`  
		Last Modified: Thu, 13 Jul 2023 22:12:14 GMT  
		Size: 5.0 MB (4957629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e9953eea227278c191c50574a1b5977ce95132636f8ff5c2d6b17dc8b5068c`  
		Last Modified: Mon, 17 Jul 2023 21:20:18 GMT  
		Size: 1.3 MB (1301228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc19eb45d37a12edd02f392537a301bdf4c5660784581897c3955276a92a5d5`  
		Last Modified: Mon, 17 Jul 2023 21:20:18 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:3a56d5d605f87ccca6c59254a55feb56e23892a1e9cf9b970ce73cd0966f7dde
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108290917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893721b291337627949a44de0328552034c89dc54f47dc597c0dac6b0e809728`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 19:56:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 14 Jun 2023 19:56:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:03:08 GMT
ENV GOLANG_VERSION=1.20.6
# Thu, 13 Jul 2023 19:52:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.6.src.tar.gz'; 		sha256='62ee5bc6fb55b8bae8f705e0cb8df86d6453626b4ecf93279e2867092e0b7f70'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 19:52:07 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 19:52:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 19:52:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 19:52:07 GMT
WORKDIR /go
# Thu, 13 Jul 2023 20:42:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 20:42:49 GMT
ENV XCADDY_VERSION=v0.3.4
# Mon, 17 Jul 2023 21:49:17 GMT
ENV CADDY_VERSION=v2.6.4
# Mon, 17 Jul 2023 21:49:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 17 Jul 2023 21:49:17 GMT
ENV XCADDY_SETCAP=1
# Mon, 17 Jul 2023 21:49:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 17 Jul 2023 21:49:18 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 17 Jul 2023 21:49:19 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ffe4223b1ef1f186378646830e3b2006e9e2e96241c0b319c50387ac3fa566`  
		Last Modified: Wed, 14 Jun 2023 20:08:03 GMT  
		Size: 284.9 KB (284873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51060beaf6b9ecb3160e6dd2fb57d49e5ee3e71b01507b7d5a176da636ae1ad8`  
		Last Modified: Thu, 13 Jul 2023 20:00:00 GMT  
		Size: 98.7 MB (98664691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef8a0b77b4d5268c5bedf1a7f069d51332b43b410c4441c7702927f0f6ae5b7`  
		Last Modified: Thu, 13 Jul 2023 19:59:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae925e86be480fd548766b52150c1c147247d957c639c80d119edf65aa6301e`  
		Last Modified: Thu, 13 Jul 2023 20:43:25 GMT  
		Size: 5.0 MB (4950276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ca488f4081333700a1f331f89b8cff85f7b77ed8fa2d9c8d6d4b18dd75c9ac`  
		Last Modified: Mon, 17 Jul 2023 21:49:48 GMT  
		Size: 1.2 MB (1247160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0e61d2c8d9803002d0d27b369d6f878b33c51847327e8cb71862403dbb5fc6`  
		Last Modified: Mon, 17 Jul 2023 21:49:48 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:b1a8ac9eb0c3f1ac3633eadca81a0da61621c5c25377109e5f6544d10d34d8ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107368272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889da2e9b68a2efe9d67bd651531ddf01700ab358b2e4d21b952e56461099af3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:14:54 GMT
RUN apk add --no-cache ca-certificates
# Thu, 15 Jun 2023 02:14:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:14:39 GMT
ENV GOLANG_VERSION=1.20.6
# Thu, 13 Jul 2023 20:00:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.6.src.tar.gz'; 		sha256='62ee5bc6fb55b8bae8f705e0cb8df86d6453626b4ecf93279e2867092e0b7f70'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 20:00:23 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 20:00:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 20:00:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 20:00:24 GMT
WORKDIR /go
# Thu, 13 Jul 2023 22:14:27 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 22:14:27 GMT
ENV XCADDY_VERSION=v0.3.4
# Mon, 17 Jul 2023 21:57:17 GMT
ENV CADDY_VERSION=v2.6.4
# Mon, 17 Jul 2023 21:57:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 17 Jul 2023 21:57:17 GMT
ENV XCADDY_SETCAP=1
# Mon, 17 Jul 2023 21:57:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 17 Jul 2023 21:57:18 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 17 Jul 2023 21:57:19 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad2d22fcfeec0ce3f819b7931d5f6b12f8aa5ed452de9e2200f594a3bacfa30`  
		Last Modified: Thu, 15 Jun 2023 02:23:48 GMT  
		Size: 284.1 KB (284075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f189018ebdf2475ad6cb31814d154952383fd7ced0b8ca0f691a18aa95c001ba`  
		Last Modified: Thu, 13 Jul 2023 20:10:16 GMT  
		Size: 98.4 MB (98439759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f61d89748a50c1932931011597967f35b43c564d1217a65aa2a3caf8e539d1`  
		Last Modified: Thu, 13 Jul 2023 20:10:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cc8627e7ea47ac280c7c9f8ccb024c91fcdf51fb953373e82f09ffc601a2ea`  
		Last Modified: Thu, 13 Jul 2023 22:15:07 GMT  
		Size: 4.5 MB (4500113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a0c05af9dd1ede4f08da30e7aafb53341ba5fffbd962360d1b82d3ef9ecd8d`  
		Last Modified: Mon, 17 Jul 2023 21:57:51 GMT  
		Size: 1.2 MB (1245254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a585ca9fb6b7fd0235dc07c0945e147b9c6adae6f6bd7f0228afdb28ff95bd6e`  
		Last Modified: Mon, 17 Jul 2023 21:57:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:47ca5d23444819341d60939a93d0efd4f54020351654355502890268b02f1c67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105967399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a818b761597493d904cef7839c7c3e71999af53fac2227716ed60e8bef4bcb1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 23:22:17 GMT
RUN apk add --no-cache ca-certificates
# Wed, 14 Jun 2023 23:22:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:13:00 GMT
ENV GOLANG_VERSION=1.20.6
# Thu, 13 Jul 2023 20:41:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.6.src.tar.gz'; 		sha256='62ee5bc6fb55b8bae8f705e0cb8df86d6453626b4ecf93279e2867092e0b7f70'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 20:41:26 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 20:41:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 20:41:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 20:41:27 GMT
WORKDIR /go
# Thu, 13 Jul 2023 22:39:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 22:39:12 GMT
ENV XCADDY_VERSION=v0.3.4
# Mon, 17 Jul 2023 21:39:22 GMT
ENV CADDY_VERSION=v2.6.4
# Mon, 17 Jul 2023 21:39:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 17 Jul 2023 21:39:22 GMT
ENV XCADDY_SETCAP=1
# Mon, 17 Jul 2023 21:39:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 17 Jul 2023 21:39:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 17 Jul 2023 21:39:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a768fa670f57b0faf1a0a8cb211432ed97307628729fa53e3ea9981ba7512d4`  
		Last Modified: Wed, 14 Jun 2023 23:27:58 GMT  
		Size: 286.3 KB (286290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853813baecd1ddb90696e6b4a565323335e39f1945532972b66a05165d862eae`  
		Last Modified: Thu, 13 Jul 2023 20:46:45 GMT  
		Size: 96.1 MB (96100116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b4e48867a2ca4441a1f324dd91e8cc4e75d6e9f03d6b34dc85d1ed36306cd7`  
		Last Modified: Thu, 13 Jul 2023 20:46:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa15f217ee350877fa2bb153a136f0d3561f2afa8e07a6466ea495c64a8138e`  
		Last Modified: Thu, 13 Jul 2023 22:39:46 GMT  
		Size: 5.1 MB (5053698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafda9c6952bd9fa6425c617d6062af1cfaa1b9b5ac6b8a6cad0cd9d9e28c467`  
		Last Modified: Mon, 17 Jul 2023 21:39:51 GMT  
		Size: 1.2 MB (1197482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12da8cbf6b0e599e14123b1ea292254f7e89239d99c653ee3ade902778d0041b`  
		Last Modified: Mon, 17 Jul 2023 21:39:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:771796ac64a26efdd5f00b35574c844c94afb8a88ae3f348f4102b24ee5a5937
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106633322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fecb31635e47618377ea56d3058db3902c839209023b93321e3dca4b433a44f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:49 GMT
ADD file:694c636c0dd19fd01accbc189e4c1dc4d063952692c6e7eb26dce02a7adba833 in / 
# Thu, 15 Jun 2023 00:39:49 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:25:57 GMT
RUN apk add --no-cache ca-certificates
# Thu, 15 Jun 2023 01:25:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:04:49 GMT
ENV GOLANG_VERSION=1.20.6
# Thu, 13 Jul 2023 20:20:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.6.src.tar.gz'; 		sha256='62ee5bc6fb55b8bae8f705e0cb8df86d6453626b4ecf93279e2867092e0b7f70'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 20:20:54 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 20:20:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 20:20:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 20:21:01 GMT
WORKDIR /go
# Thu, 13 Jul 2023 23:47:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 23:47:29 GMT
ENV XCADDY_VERSION=v0.3.4
# Mon, 17 Jul 2023 21:16:31 GMT
ENV CADDY_VERSION=v2.6.4
# Mon, 17 Jul 2023 21:16:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 17 Jul 2023 21:16:32 GMT
ENV XCADDY_SETCAP=1
# Mon, 17 Jul 2023 21:16:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 17 Jul 2023 21:16:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 17 Jul 2023 21:16:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ffa4a466dbb8eebd7e7f25590a9df12390de9016abf82279c29c9a64aa76491a`  
		Last Modified: Thu, 15 Jun 2023 00:40:26 GMT  
		Size: 3.3 MB (3344781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1647fd337167bcedcd03fcbbea1cdda0214e39f0c809960a10a1a2e7f5ec905`  
		Last Modified: Thu, 15 Jun 2023 01:37:59 GMT  
		Size: 286.7 KB (286671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc56d2a25a9549c37e2bf8861517bda4252cb591ac93b6f4874f889f22b17bfc`  
		Last Modified: Thu, 13 Jul 2023 20:32:32 GMT  
		Size: 96.6 MB (96566467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5855e125e918cd8e7934334c95e456fcb079c83b5f26be07ee429ca4a361a895`  
		Last Modified: Thu, 13 Jul 2023 20:32:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c1b71f3ca615e42762c551459aa93fdf8d6ab374b7a7f0a1d897f70c49d3b0`  
		Last Modified: Thu, 13 Jul 2023 23:48:36 GMT  
		Size: 5.2 MB (5249642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990451bccc25ade15202f710dc3d603a2e262b6e017a82110c7f9001694b2d74`  
		Last Modified: Mon, 17 Jul 2023 21:18:45 GMT  
		Size: 1.2 MB (1185196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e049478a1caa617cd8a7b3a3a1fe29771b39ffbd87549ac9d0f69faf9326cc`  
		Last Modified: Mon, 17 Jul 2023 21:18:45 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:e78b675aa5637cac94b9d0040ac529d9ff04d72e707b53bd3b3421eb428d2fe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110700542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87028e05ab64c95ca9e9621d78fd0b922456256e0b6cb90fae2d3244c24dbc5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:37:10 GMT
RUN apk add --no-cache ca-certificates
# Thu, 15 Jun 2023 05:37:10 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:43:21 GMT
ENV GOLANG_VERSION=1.20.6
# Thu, 13 Jul 2023 21:18:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.6.src.tar.gz'; 		sha256='62ee5bc6fb55b8bae8f705e0cb8df86d6453626b4ecf93279e2867092e0b7f70'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 21:18:44 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 21:18:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 21:18:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 21:18:44 GMT
WORKDIR /go
# Thu, 13 Jul 2023 21:43:50 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 21:43:50 GMT
ENV XCADDY_VERSION=v0.3.4
# Mon, 17 Jul 2023 21:41:44 GMT
ENV CADDY_VERSION=v2.6.4
# Mon, 17 Jul 2023 21:41:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 17 Jul 2023 21:41:44 GMT
ENV XCADDY_SETCAP=1
# Mon, 17 Jul 2023 21:41:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 17 Jul 2023 21:41:45 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 17 Jul 2023 21:41:45 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175521994a5932158dbd78d2153c38836ab5e1db0ceb4af91113d4c49c5caba2`  
		Last Modified: Thu, 15 Jun 2023 06:04:00 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3d5aab1b722344a2b27dda9306fdd8695280c545304899dacc0c8b485a803d`  
		Last Modified: Thu, 13 Jul 2023 21:26:38 GMT  
		Size: 100.8 MB (100840316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186907ef44e4d85a8da0e537dd36516c0ba205606d1c7a6fd9f4629917bee1bb`  
		Last Modified: Thu, 13 Jul 2023 21:26:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a7f9731da1d937dfee5000e36e3a12144b2cc3be1838d9101fc3e685d197a8`  
		Last Modified: Thu, 13 Jul 2023 21:44:40 GMT  
		Size: 5.1 MB (5099678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0c335632c4f44b83a9f03336bf3e1d61ce49d00b53ec4ff13a629d8b6fd979`  
		Last Modified: Mon, 17 Jul 2023 21:42:34 GMT  
		Size: 1.3 MB (1261396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9064a8ee9d6df192bda3c651e86f446b16864e2e72696bae7e03a0002795a`  
		Last Modified: Mon, 17 Jul 2023 21:42:34 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
