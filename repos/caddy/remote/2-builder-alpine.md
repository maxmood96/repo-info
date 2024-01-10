## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:88ea79d5d4c27d14e88147a8ee7880afdd51b939d2fc2b455146a10fbc326986
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
$ docker pull caddy@sha256:40fb52ba04a15d7b79c65ccf594655c93ef84951d4b5f3636dd741c6f7117c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8a77457f35f87a6c0e163b4b9ca06831e9597838815cdfafd6924007b2053`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:46:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:46:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:46 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:20:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:20:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:20:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:13:01 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:13:01 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:13:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:13:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:13:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501dced60f86be38cc73d3c038f7db4afeee65726f7e422aacf09244539ebf1`  
		Last Modified: Fri, 01 Dec 2023 03:50:39 GMT  
		Size: 284.7 KB (284697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2786abec99e189a4a116c45771654dd1220a5a78deb32430974d369c08fa4bd0`  
		Last Modified: Tue, 09 Jan 2024 22:27:13 GMT  
		Size: 67.1 MB (67086665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ece744550870593fb66b630e5fa62ae11cf9c89547275dd4450952b0fc9460`  
		Last Modified: Tue, 09 Jan 2024 22:27:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a3a5ccc6f4610e4fd60832b6c63eed6366cfe0b0f37e3e6125f54aef9f135`  
		Last Modified: Tue, 09 Jan 2024 23:13:20 GMT  
		Size: 5.0 MB (4972463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d8e469393bc3c86e3dc711c99a557728a8c0e8a67a85f65d7fdc195034cd`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ef04b7c1f8fcec7e6f8b1f4995bdf8f34100b19140a0faef407b758829e8d`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:83a8b023f6fa4c601dca30abe334e1243463e92f8e84e33dac925e8d6f7a601f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0ab3fe89b994d3ff35471a8b1709d10e3ca724eb9a2e14bac7221211877bb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 00:53:48 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:49:18 GMT
ENV GOLANG_VERSION=1.21.5
# Wed, 20 Dec 2023 21:34:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOPATH=/go
# Wed, 20 Dec 2023 21:34:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 21:34:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 20 Dec 2023 21:34:13 GMT
WORKDIR /go
# Wed, 20 Dec 2023 21:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 20 Dec 2023 21:51:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SETCAP=1
# Wed, 20 Dec 2023 21:51:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 20 Dec 2023 21:51:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 20 Dec 2023 21:51:43 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bee9d75e3ae91d44ddf09cf0fa198b556654c8073aa50d8b630e52a5d203be`  
		Last Modified: Wed, 20 Dec 2023 21:36:17 GMT  
		Size: 65.8 MB (65764273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a485eddce12cbac59d4532427a2f3bc7f475a18f1b6ddc05d3631682cde4be3e`  
		Last Modified: Wed, 20 Dec 2023 21:36:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460d4992c24f213c1a4f97d850c33f2a32be4f0763f60ae881dfb36929edbeb8`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 5.0 MB (4966637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf270d0f9df22c9f4d54cc419be9b59b79eec2ef2f2c70fa2545347b5db6a1de`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 1.2 MB (1248658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559d6667b029d9d030a6d020a049a1c7df7a5d84b925b75e0b37d63be04d25`  
		Last Modified: Wed, 20 Dec 2023 21:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:286339d083a589ff4ee17f2a98eabb1011f13f93e40c79bba2af0748f9bf2c8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74795731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08540a67a8309258e1b934ca527574a28d9cd09a153f09e55635d67a11e5572d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:44:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:59:02 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:59:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:59:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:59:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:59:27 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:59:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:59:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:59:30 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:59:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:59:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:59:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f975e362e12b206661ef3e8661f8ddef5b3886db6695858a6ee13107cfb406cd`  
		Last Modified: Tue, 09 Jan 2024 23:10:25 GMT  
		Size: 65.8 MB (65849716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d88a6cd0c6e987e9c7854e8091bc0d3da0f5215dc272d31db2a10463a597eb`  
		Last Modified: Tue, 09 Jan 2024 23:10:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ccd85286302c0f7692dc9bf9e673cc831252fa3892db98d4a388f8e3a40229`  
		Last Modified: Tue, 09 Jan 2024 23:59:54 GMT  
		Size: 4.5 MB (4514276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c77c0eb7e54b1d25489fbedb6607137e9123f25be63514940cec48f5afbcbb`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 1.2 MB (1246091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe6c53215469f1e0efd2612e28e7bc3d644b7460fdac4ed2217adcfcbb01ff`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:29c1d8e221c7025b5fa2bd564d67b2cbe54abf6ed141469ee753714d4b86de8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74062596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a7ab9b4f36aa69472a02e61896bae0e9f5d4d8751e6a7791c550f914532f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:43:53 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:18:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:40:13 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:40:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:40:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:40:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:40:24 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:34:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:34:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:34:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:34:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:34:51 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a63ed24dc22a348b35d99b5ec9dc67ff66563b539875e5c8ab2d870b3991ac`  
		Last Modified: Fri, 01 Dec 2023 02:44:03 GMT  
		Size: 286.3 KB (286307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f784b2816c0487ec6a1efb9635a001a738ce6794c6f60cef8dd8fc658663da9f`  
		Last Modified: Tue, 09 Jan 2024 22:45:17 GMT  
		Size: 64.2 MB (64173642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878d57b8185e91fa6aee756ccda964266f809fac11f9dce2ed4fbfd8912f1a9`  
		Last Modified: Tue, 09 Jan 2024 22:45:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab371eb8298e2716c51ac9c58092131a438b00268b67ae458e1ace0ff2b0b5a`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 5.1 MB (5070606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797b9a67275bffa5caa99271d04d6986b812b4aa84192f9ba3f1ff7b1dfed362`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13428147a58f4a789fd5d1f01d54bef643a726131dd40b35c267f16843158a6c`  
		Last Modified: Tue, 09 Jan 2024 23:35:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:745364722abfeb88309b8c87aaea59721a3b9ce6770ef2ece3727cd89c4ecdb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ca8de75928fb38f0a93327b23d822645315bee4c8d32dbc96b28ffbf4f513b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 06:37:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:18:29 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:18:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:18:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:18:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:31:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:31:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:31:34 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:31:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:31:36 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:31:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:31:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08676902305ce1488e47f2c6cf37c156f8adf34592d23cb6c0adda7f8e20bbec`  
		Last Modified: Tue, 09 Jan 2024 22:27:11 GMT  
		Size: 64.2 MB (64202869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007761f68f098a06788d8a4f5b63c5c25fa52e8f613da754d12a9c8005b2ad44`  
		Last Modified: Tue, 09 Jan 2024 22:26:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28beac3397f3e144b5cbb889b20e5c6450f5a635fd5679a9ddb77b34420a9512`  
		Last Modified: Tue, 09 Jan 2024 23:31:57 GMT  
		Size: 5.3 MB (5270658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee35c838a10edf1f76e27c99108010f65e1cb2d9cbad31ebe0480cdcc17a15d`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2a624f1055a6b34babd0b44d093aa23653397f4289c89018b0396bebcf038`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9eb20c4013227f7a3b0435a6f5346ec30763958b3f54f7ad0e7a02a7dd369f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76184930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c9ebcb7eda5bc7753c6ac25b3a1ea2cbdce628c002973e9ad47ffb0d3ba97e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:14:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:43:43 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:43:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:44:01 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:08:20 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:08:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:08:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:08:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:08:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d670b96a401a5cfb61ad27940492a2027ad1b61a1fa46000d705a1d8d159201`  
		Last Modified: Tue, 09 Jan 2024 22:51:10 GMT  
		Size: 66.3 MB (66302457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da6e3a038c3bd2afee0afab16ad35ea548d1966b1df80e55d9dcee9b280b371`  
		Last Modified: Tue, 09 Jan 2024 22:50:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08206a39be152f3861e70f6c3448542421f3249680b9274fd278f6015cc11aa5`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1075ed747212d8e9506ed70d4cccab2b94dd685aa98e25a32f43575e21839`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b6771ab88a9777236c173bb24bbc313a76da44e25c4c9ce07f8ff003338ee`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
