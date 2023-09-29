## `caddy:builder`

```console
$ docker pull caddy@sha256:dd4d148ab0a97ac51d24631b974c65810a0887c8d03ebe6ad5a4c2bf2d1c7fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4851; amd64
	-	windows version 10.0.20348.1970; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:877964af702eae05e189ddb46d29c026375a4b4322cf38c4c39c7d334ac388fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76961566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380672f1b85427de87189636acabd9d26608f4b8ddc863bcf5c75556e0818a38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:36:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 09 Aug 2023 04:41:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:29 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 06 Sep 2023 18:31:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 27 Sep 2023 00:22:36 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 Sep 2023 00:22:36 GMT
ENV GOPATH=/go
# Wed, 27 Sep 2023 00:22:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Sep 2023 00:22:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 27 Sep 2023 00:22:36 GMT
WORKDIR /go
# Wed, 27 Sep 2023 00:48:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 27 Sep 2023 00:48:53 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 27 Sep 2023 00:48:53 GMT
ENV CADDY_VERSION=v2.7.4
# Wed, 27 Sep 2023 00:48:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 27 Sep 2023 00:48:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 27 Sep 2023 00:48:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 27 Sep 2023 00:48:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 27 Sep 2023 00:48:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d48a809fc2256f8aa0aeee47998488d64409855adba00a7cb3007ab9f3286e`  
		Last Modified: Wed, 09 Aug 2023 03:37:02 GMT  
		Size: 284.7 KB (284693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60be0ca469417450769350b29d9d86e57dc60849c11fab3e8d0b556fcc35005`  
		Last Modified: Wed, 06 Sep 2023 18:37:24 GMT  
		Size: 67.0 MB (67002091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e31cf1df85f9b87c84f89cf1697395f6149060a4090b00d92c2aaf987a645`  
		Last Modified: Wed, 27 Sep 2023 00:23:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c245b328c436a749be95559ba5546b5a8e2c9755329cdefe5a294ac31cdf8364`  
		Last Modified: Wed, 27 Sep 2023 00:49:11 GMT  
		Size: 5.0 MB (4970375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6c17994f9fecaca655a34ae94799c446f84a70c868192fbecf087edfe8142f`  
		Last Modified: Wed, 27 Sep 2023 00:49:11 GMT  
		Size: 1.3 MB (1302234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ac2e16bdca23c88b034331a9bcc55fa398ba7682019f3bf3dcda9506f54221`  
		Last Modified: Wed, 27 Sep 2023 00:49:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:de02c3655970e860e68fd2840e08fd9656cebb751cf677a0982e67d8fc5538a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75403016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636f8b72fc8192d5a346042bbf7f4b91636efcd463c388b6789b3d107346d09d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:55:22 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:55:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 21:55:22 GMT
ENV GOLANG_VERSION=1.21.1
# Thu, 28 Sep 2023 21:55:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 28 Sep 2023 21:55:37 GMT
ENV GOTOOLCHAIN=local
# Thu, 28 Sep 2023 21:55:37 GMT
ENV GOPATH=/go
# Thu, 28 Sep 2023 21:55:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 21:55:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 28 Sep 2023 21:55:37 GMT
WORKDIR /go
# Thu, 28 Sep 2023 21:59:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 28 Sep 2023 21:59:22 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 28 Sep 2023 21:59:22 GMT
ENV CADDY_VERSION=v2.7.4
# Thu, 28 Sep 2023 21:59:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 28 Sep 2023 21:59:23 GMT
ENV XCADDY_SETCAP=1
# Thu, 28 Sep 2023 21:59:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 28 Sep 2023 21:59:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 28 Sep 2023 21:59:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3da3b9e7a12f6bb6b7f56e9240c2c92ce8c9f5fd5ef3b3063b9a93d454919e`  
		Last Modified: Thu, 28 Sep 2023 21:58:05 GMT  
		Size: 284.9 KB (284887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db471c20f6642596c4a4eeca4a9348dd5a897aa1c3c2383fdf2fe2c2d6f1628`  
		Last Modified: Thu, 28 Sep 2023 21:58:18 GMT  
		Size: 65.8 MB (65758212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037298c7b9748af97a3a2906d0ebb91f2dd588f633a9e8f94e2e2b2a571ead1f`  
		Last Modified: Thu, 28 Sep 2023 21:58:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc923fd6dd565567ed402508a7420812a84f61bbecfa0e1f988bd9b2d7b772b`  
		Last Modified: Thu, 28 Sep 2023 22:00:17 GMT  
		Size: 5.0 MB (4965415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b055d2dc5239a960f27dc6b7a7dcbe9455defa55bfb2f41d11678f8d56591668`  
		Last Modified: Thu, 28 Sep 2023 22:00:17 GMT  
		Size: 1.2 MB (1248652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513967d31b50a4e0f6dd90e6b95fe92f327bab78e463b9ed3a5ab386b0796a0e`  
		Last Modified: Thu, 28 Sep 2023 22:00:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:53113a1b3df8f79b67b12b1443823c7f44848ad7f6f90606a2b21dbeb6795e86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74701010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d1f08a4cbe40e460c9b137e13a56f0cab791a45dbf98a667027dc7d91f1600`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:39:47 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 01:39:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:45 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 06 Sep 2023 18:31:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 27 Sep 2023 00:59:35 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 Sep 2023 00:59:35 GMT
ENV GOPATH=/go
# Wed, 27 Sep 2023 00:59:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Sep 2023 00:59:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 27 Sep 2023 00:59:36 GMT
WORKDIR /go
# Wed, 27 Sep 2023 01:17:08 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 27 Sep 2023 01:17:08 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 27 Sep 2023 01:17:08 GMT
ENV CADDY_VERSION=v2.7.4
# Wed, 27 Sep 2023 01:17:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 27 Sep 2023 01:17:08 GMT
ENV XCADDY_SETCAP=1
# Wed, 27 Sep 2023 01:17:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 27 Sep 2023 01:17:10 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 27 Sep 2023 01:17:10 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47bd95d78f565e902bafd0264a979eb4f6f71e22c0464011bf9db6feb0579e6`  
		Last Modified: Tue, 08 Aug 2023 01:48:34 GMT  
		Size: 284.1 KB (284073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812db0f4af4ab09f020f5a4b3fb1803a8afdf60db3d0e0c2d451a717141054ca`  
		Last Modified: Wed, 06 Sep 2023 18:40:37 GMT  
		Size: 65.8 MB (65758511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad20248d008ed94885846c60482d8b880b64858c6f69972a17687090972e4f6`  
		Last Modified: Wed, 27 Sep 2023 01:00:35 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342dd437f959b874ae6c31887d74e3b3ae1ed45d09350d20db13054ebede00b3`  
		Last Modified: Wed, 27 Sep 2023 01:17:26 GMT  
		Size: 4.5 MB (4512300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b14d416bffd4e3b80b8c40002fed7030446c9368489cd234b6cbfd632487f84`  
		Last Modified: Wed, 27 Sep 2023 01:17:26 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b580d523204e32d7a167e70eec699a382759ae0ce5891a2f64d2d64ea9684b2`  
		Last Modified: Wed, 27 Sep 2023 01:17:25 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f899df9a809470d0ca93ab1e634180bae86b06143e21e498720df8f3d8011fe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a7c6fc8ff287b1c81a9aaa93ab04499ca204f18c8c3e814b321be9434391`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:10:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:10:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:18 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 06 Sep 2023 18:31:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 27 Sep 2023 00:41:32 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 Sep 2023 00:41:32 GMT
ENV GOPATH=/go
# Wed, 27 Sep 2023 00:41:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Sep 2023 00:41:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 27 Sep 2023 00:41:33 GMT
WORKDIR /go
# Wed, 27 Sep 2023 01:16:04 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 27 Sep 2023 01:16:04 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 27 Sep 2023 01:16:04 GMT
ENV CADDY_VERSION=v2.7.4
# Wed, 27 Sep 2023 01:16:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 27 Sep 2023 01:16:04 GMT
ENV XCADDY_SETCAP=1
# Wed, 27 Sep 2023 01:16:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 27 Sep 2023 01:16:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 27 Sep 2023 01:16:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54e960e981301b0098c80d2e61d694333b5ab480a007a3a8d0fa629662d377`  
		Last Modified: Tue, 08 Aug 2023 23:14:21 GMT  
		Size: 286.3 KB (286298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f000f33a92ab709a2599fbb82fa02eca8bca5b4fda93be45a8d0f1daabb73205`  
		Last Modified: Wed, 06 Sep 2023 18:36:08 GMT  
		Size: 64.1 MB (64108346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696c13a2abb008f6aee1be946c6e2aade955168f8fad682a9bedaf7f3d17e285`  
		Last Modified: Wed, 27 Sep 2023 00:42:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ab6353f271f7f6657f7144b208ccb11d894fb9d51422060d1fc48ba49d53c`  
		Last Modified: Wed, 27 Sep 2023 01:16:22 GMT  
		Size: 5.1 MB (5069068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587a4a8a2c4da991592a6256079154d56b9d53059b1aff2d18af44b6b057b87f`  
		Last Modified: Wed, 27 Sep 2023 01:16:21 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb99b18f8c861faaea0d43cd3b3cfae2fff4e0506f19113cc0c7f08e4b2e563`  
		Last Modified: Wed, 27 Sep 2023 01:16:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:0df84fac6186066c6af17d23cb3e4848343b3abdd88551a2e49512f3bb229977
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74204976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e28f2286878ba69441c126938420e49f768b36ec5d8154313c49a74cbea76fe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:25:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 00:25:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:32:13 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 06 Sep 2023 18:32:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 27 Sep 2023 00:19:48 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 Sep 2023 00:19:49 GMT
ENV GOPATH=/go
# Wed, 27 Sep 2023 00:19:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Sep 2023 00:19:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 27 Sep 2023 00:19:53 GMT
WORKDIR /go
# Wed, 27 Sep 2023 00:44:25 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 27 Sep 2023 00:44:26 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 27 Sep 2023 00:44:26 GMT
ENV CADDY_VERSION=v2.7.4
# Wed, 27 Sep 2023 00:44:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 27 Sep 2023 00:44:28 GMT
ENV XCADDY_SETCAP=1
# Wed, 27 Sep 2023 00:44:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 27 Sep 2023 00:44:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 27 Sep 2023 00:44:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966ad2cdd35689da92e7c8fd39bd37cd6080c484e6ccaf00672c154cd4f6c2a`  
		Last Modified: Tue, 08 Aug 2023 00:39:35 GMT  
		Size: 286.7 KB (286662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679e04809663a2145818569201c1dcf2d46798f2198322a8e7910805a9b7dffd`  
		Last Modified: Wed, 06 Sep 2023 18:43:51 GMT  
		Size: 64.1 MB (64116069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adfc64af8099cd6da947abb99291c27bd3e5cd2a4edaafe01275ae6fba70e86`  
		Last Modified: Wed, 27 Sep 2023 00:21:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36769f3ac59b9d089baf3c77f752460312799be52299082e84e0563f1eb90755`  
		Last Modified: Wed, 27 Sep 2023 00:44:52 GMT  
		Size: 5.3 MB (5269261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea37c34f5aec8f5cfc693e18a4812c455b4ea9adfa588417d8396e84996afdd8`  
		Last Modified: Wed, 27 Sep 2023 00:44:52 GMT  
		Size: 1.2 MB (1186172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cb4674441b7d59392f821fbdd3dbae2e3e9f26dc27970dc92dc54a41d0e5d5`  
		Last Modified: Wed, 27 Sep 2023 00:44:51 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:b438b3cf1ad85b0cc2fe8f5319ac062a52640a6a231f4858917e081b1e773001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1788e10f8a6f8ccdc56c8b2c4b5a6ebc9387eb3b66b2b9d2dd1f18b74223f3c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:38:54 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:38:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 21:38:54 GMT
ENV GOLANG_VERSION=1.21.1
# Thu, 28 Sep 2023 21:39:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 28 Sep 2023 21:39:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 28 Sep 2023 21:39:15 GMT
ENV GOPATH=/go
# Thu, 28 Sep 2023 21:39:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 21:39:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 28 Sep 2023 21:39:15 GMT
WORKDIR /go
# Thu, 28 Sep 2023 22:19:51 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 28 Sep 2023 22:19:51 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 28 Sep 2023 22:19:51 GMT
ENV CADDY_VERSION=v2.7.4
# Thu, 28 Sep 2023 22:19:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 28 Sep 2023 22:19:51 GMT
ENV XCADDY_SETCAP=1
# Thu, 28 Sep 2023 22:19:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 28 Sep 2023 22:19:52 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 28 Sep 2023 22:19:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721f16693d4788a5add1bd0b22764c8887cdc62b24edf388ae895df440f4aa9`  
		Last Modified: Thu, 28 Sep 2023 21:46:22 GMT  
		Size: 285.1 KB (285095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40248878cac53fafdd0778844ffa03633e8f3cd73c5d5136e02da42557cb26f6`  
		Last Modified: Thu, 28 Sep 2023 21:46:16 GMT  
		Size: 66.2 MB (66224373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3d28e3790630932107b3adf42c8b1564c57d0ab97f15a759b1a8f835ee4101`  
		Last Modified: Thu, 28 Sep 2023 21:46:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d382e103bfc732fc0a4c2b972100a5426b9a8e99cd21d22eddb196e5bb029206`  
		Last Modified: Thu, 28 Sep 2023 22:20:30 GMT  
		Size: 5.1 MB (5115228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3232faabff7e982d010fd0c3775d8c4a6b80e55bc3acdb0af1e63077c07656`  
		Last Modified: Thu, 28 Sep 2023 22:20:30 GMT  
		Size: 1.3 MB (1262392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff69fb680d5cc18f0d5150ac6c2922176848b00c8456922df5843f6e1c993cc7`  
		Last Modified: Thu, 28 Sep 2023 22:20:29 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.4851; amd64

```console
$ docker pull caddy@sha256:95c666eeefee6beeed59b530714de1ebdd28f2ba6ad0703b37f26b729f5e3793
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2113168904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bf61498c4479dace7e2fa1c8c4c29a0a0722e06138f3d5fa9226287d83f2d6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 01:39:14 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Sep 2023 01:39:15 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Sep 2023 01:39:16 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Sep 2023 01:39:16 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Sep 2023 01:40:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Sep 2023 01:40:50 GMT
ENV GOPATH=C:\go
# Wed, 13 Sep 2023 01:41:53 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Sep 2023 01:41:54 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 13 Sep 2023 01:45:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '10a4f5b63215d11d1770453733dbcbf024f3f74872f84e28d7ea59f0250316c6'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Sep 2023 01:45:04 GMT
WORKDIR C:\go
# Wed, 13 Sep 2023 05:35:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 05:35:07 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Sep 2023 05:35:07 GMT
ENV CADDY_VERSION=v2.7.4
# Wed, 13 Sep 2023 05:35:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Sep 2023 05:36:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Sep 2023 05:36:25 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdfacf538899a08fcbb1c6b92df02725dbfcc05c593d6f310371baf9cc5c28b`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaa9f7bc4f06074cd41e4c8f38f9019d00b30116cc81e7e57bb201a2cddbe76`  
		Last Modified: Wed, 13 Sep 2023 02:16:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa369f25c61f03e75b9090231c21b059562345a9aa5b4710c1d4bd043232a46`  
		Last Modified: Wed, 13 Sep 2023 02:16:48 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1338c790efe798520cb633291aa3dbf3b37552cfbd91737d2539bad7bcac882c`  
		Last Modified: Wed, 13 Sep 2023 02:16:48 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af230316f5f5bdfd37af05e436ffaadf28ac7a31d97f315dbfb2924c4d1ca3c`  
		Last Modified: Wed, 13 Sep 2023 02:16:54 GMT  
		Size: 25.6 MB (25567707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606d89c5df48922aee4ed7b88afc9f9fc270b462891c28d20b75199f2726201e`  
		Last Modified: Wed, 13 Sep 2023 02:16:46 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f90ec51ca481c33d4e3887adf74f8b37c2f82af9e60290d2755f34c55b70e9c`  
		Last Modified: Wed, 13 Sep 2023 02:16:46 GMT  
		Size: 220.5 KB (220461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9741d5460d3c8c14c62fd6990864968f75fbb895dfd099803a72c140739264b`  
		Last Modified: Wed, 13 Sep 2023 02:16:46 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac37fd27ee4a5046c706042d53bb4a5b5e2e9ac0ec76a27142f42a55f09c31aa`  
		Last Modified: Wed, 13 Sep 2023 02:17:12 GMT  
		Size: 69.3 MB (69345076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4460c6474f9af5dc17adefba85607fa63b6072fc39250bcf433f458742fd0987`  
		Last Modified: Wed, 13 Sep 2023 02:16:46 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8840f55013cb306bc30661534c9618bdfda370c585b638deb791ba84fbceee9c`  
		Last Modified: Wed, 13 Sep 2023 05:38:30 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f45db9ea611a79882cee37d8b10da3ddf761d7f9ae24bf1fe0cfdb58497a6ae`  
		Last Modified: Wed, 13 Sep 2023 05:38:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51195ebf7ad1d0ac3972b387896050e20749e6e0bb65d49a1907f49ab5cec5f2`  
		Last Modified: Wed, 13 Sep 2023 05:38:28 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56989aaa5684bbc2d72ae4bb645d01d4dd0c63d35c8f4515b4c8587d6611d519`  
		Last Modified: Wed, 13 Sep 2023 05:38:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae11f7d16342cb14a92f5b67ee9ce0eeab5805f76829bedd3735c0eec9b1f744`  
		Last Modified: Wed, 13 Sep 2023 05:38:29 GMT  
		Size: 1.7 MB (1687175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f520ac11e32bd8e755e12beaef19d397e709b5d8b007fb948658b974af6c7e2`  
		Last Modified: Wed, 13 Sep 2023 05:38:28 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.1970; amd64

```console
$ docker pull caddy@sha256:0a56e01d98805d99f891740e4644f1afb62f725060c36ad3cdcad27f452c3952
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1934132962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f26855783f570cd07fa203aa143ae0ddab1ef24e3a100e66f3cac124f008c0e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 01 Sep 2023 00:43:48 GMT
RUN Install update 10.0.20348.1970
# Wed, 13 Sep 2023 01:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 01:35:30 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Sep 2023 01:35:31 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Sep 2023 01:35:32 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Sep 2023 01:35:33 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Sep 2023 01:36:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Sep 2023 01:36:16 GMT
ENV GOPATH=C:\go
# Wed, 13 Sep 2023 01:36:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Sep 2023 01:36:39 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 13 Sep 2023 01:38:59 GMT
RUN $url = 'https://dl.google.com/go/go1.21.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '10a4f5b63215d11d1770453733dbcbf024f3f74872f84e28d7ea59f0250316c6'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Sep 2023 01:39:01 GMT
WORKDIR C:\go
# Wed, 13 Sep 2023 05:36:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 05:36:35 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Sep 2023 05:36:35 GMT
ENV CADDY_VERSION=v2.7.4
# Wed, 13 Sep 2023 05:36:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Sep 2023 05:37:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Sep 2023 05:37:05 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feca8e06011ab171ad74cda49c7c305e791965aef283d5b7c2b987dd5388e6c7`  
		Last Modified: Tue, 12 Sep 2023 18:24:42 GMT  
		Size: 448.7 MB (448675362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f40969dbf1e035a6c49e7c40b216960e3ee98ec3b76f76f9fe4498d0110bee`  
		Last Modified: Wed, 13 Sep 2023 02:15:22 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a846e03791bc3a58cfed3f02e65f87e18a5f5f416405456368e8a0ec4f9364`  
		Last Modified: Wed, 13 Sep 2023 02:15:21 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bc2015fc36cda903dca8edfdc1c87b219753af24c4ff5a95db324fb0e1cc0c`  
		Last Modified: Wed, 13 Sep 2023 02:15:20 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d1910b6e6c60b5b71a12c43af94e08cf0ba20718d9a6c16ad07734f4977311`  
		Last Modified: Wed, 13 Sep 2023 02:15:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46353fb4c6176aee49921617b1cd3ac7dcbca49d4d7a734cb5ddef177b8354b2`  
		Last Modified: Wed, 13 Sep 2023 02:15:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f70d11added5b27b9707831ac76b04e95d4fa92b406f09532472fa350df630`  
		Last Modified: Wed, 13 Sep 2023 02:15:25 GMT  
		Size: 25.6 MB (25551011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892bff3fc5428691c1922057d675611c2b50e50cf3c6d22c2054b270861bc53c`  
		Last Modified: Wed, 13 Sep 2023 02:15:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ee07c029ab53a292bbb7320390d24d86b21159530b1b77d968b2b5416e8f67`  
		Last Modified: Wed, 13 Sep 2023 02:15:18 GMT  
		Size: 277.5 KB (277484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fba082f03e26936264b99820372415048914f7ffd7f2469a28d3c0edd9224d`  
		Last Modified: Wed, 13 Sep 2023 02:15:17 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5004044396790144a82fbe98df119c5d7ae1a9abaac51c4cf0813b0d43f3f58`  
		Last Modified: Wed, 13 Sep 2023 02:15:43 GMT  
		Size: 69.3 MB (69336704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d84e4497229ea334095327a0106b2812e1dd5261c636cb1461fd698efffc4b6`  
		Last Modified: Wed, 13 Sep 2023 02:15:17 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bad1e33f8c7089f46cd563d46ed621e589ef95c6dd41ba7569e5649804f136`  
		Last Modified: Wed, 13 Sep 2023 05:38:48 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c872ac2c7792d27826114f417d42ecbf945599d2b446775726d828ee99aab2c0`  
		Last Modified: Wed, 13 Sep 2023 05:38:46 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6aff62b7b35fb324b51b0049e8a19ba51736b4f6ba1bfd92511f117e51e794`  
		Last Modified: Wed, 13 Sep 2023 05:38:46 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77347ece80c37436fa82eb033a03166eb1c797e7341a6b642bf3bb80c12e36d5`  
		Last Modified: Wed, 13 Sep 2023 05:38:46 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d1c7afb782c38442247cae60bbf9b16689939a03c80d4394125a9ff0af783c`  
		Last Modified: Wed, 13 Sep 2023 05:38:47 GMT  
		Size: 1.7 MB (1675830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191cef90893a643b034d031ee3e41cd4daa1b59c1d2d0e2dc1640f7bedb6c55a`  
		Last Modified: Wed, 13 Sep 2023 05:38:46 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
