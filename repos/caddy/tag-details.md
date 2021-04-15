<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-1809`](#caddy2-builder-windowsservercore-1809)
-	[`caddy:2-builder-windowsservercore-ltsc2016`](#caddy2-builder-windowsservercore-ltsc2016)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2-windowsservercore-ltsc2016`](#caddy2-windowsservercore-ltsc2016)
-	[`caddy:2.3.0`](#caddy230)
-	[`caddy:2.3.0-alpine`](#caddy230-alpine)
-	[`caddy:2.3.0-builder`](#caddy230-builder)
-	[`caddy:2.3.0-builder-alpine`](#caddy230-builder-alpine)
-	[`caddy:2.3.0-builder-windowsservercore-1809`](#caddy230-builder-windowsservercore-1809)
-	[`caddy:2.3.0-builder-windowsservercore-ltsc2016`](#caddy230-builder-windowsservercore-ltsc2016)
-	[`caddy:2.3.0-windowsservercore`](#caddy230-windowsservercore)
-	[`caddy:2.3.0-windowsservercore-1809`](#caddy230-windowsservercore-1809)
-	[`caddy:2.3.0-windowsservercore-ltsc2016`](#caddy230-windowsservercore-ltsc2016)
-	[`caddy:2.4.0-beta.2`](#caddy240-beta2)
-	[`caddy:2.4.0-beta.2-alpine`](#caddy240-beta2-alpine)
-	[`caddy:2.4.0-beta.2-builder`](#caddy240-beta2-builder)
-	[`caddy:2.4.0-beta.2-builder-alpine`](#caddy240-beta2-builder-alpine)
-	[`caddy:2.4.0-beta.2-builder-windowsservercore-1809`](#caddy240-beta2-builder-windowsservercore-1809)
-	[`caddy:2.4.0-beta.2-builder-windowsservercore-ltsc2016`](#caddy240-beta2-builder-windowsservercore-ltsc2016)
-	[`caddy:2.4.0-beta.2-windowsservercore`](#caddy240-beta2-windowsservercore)
-	[`caddy:2.4.0-beta.2-windowsservercore-1809`](#caddy240-beta2-windowsservercore-1809)
-	[`caddy:2.4.0-beta.2-windowsservercore-ltsc2016`](#caddy240-beta2-windowsservercore-ltsc2016)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-1809`](#caddybuilder-windowsservercore-1809)
-	[`caddy:builder-windowsservercore-ltsc2016`](#caddybuilder-windowsservercore-ltsc2016)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-1809`](#caddywindowsservercore-1809)
-	[`caddy:windowsservercore-ltsc2016`](#caddywindowsservercore-ltsc2016)

## `caddy:2`

```console
$ docker pull caddy@sha256:88fc125055b8c4dafe67a48219fd3a89c0a472aa254d2835b2e298b93493b28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:6fbf52298c46c55c572670b5395ecaee5d399338003c9bb4e4abed875c542f4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395cc3713b2ca5574a9b4aafc468a1533d16582efe47dcab74ed547540d698a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:10:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:10:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:10:49 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:10:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:10:53 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:10:54 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:10:55 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:56 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:10:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a0cd9cca5be9b30bbc70611052d1456502e1f338ce4b14946233b21cd6a9a`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 300.0 KB (300016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5666523658a43fbbdff6b8fca498a988f4dcecc3ce027f1701414658c21d4ea`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097228407f13a161f68b188b0a4f255855b64d84e7b076745a744d5aa7ed8cf`  
		Last Modified: Wed, 14 Apr 2021 20:11:49 GMT  
		Size: 11.6 MB (11622383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40682d93cc09b4592a1b9c08d48d0a956b5eef4f123d80d1a12942482edb6aab`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0df9df9725cab39fe073887c98b54bf7bf1c96b3ed0e23916737c7c4877576c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13856181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce1c33ce4509195edc1c67d2dcd15c6c5fc0b35cec2e90714ec3007739600eb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:45:19 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:45:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:45:36 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:45:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:46:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:46:04 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:46:05 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:46:07 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:46:08 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:46:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:46:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:46:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:46:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:46:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:46:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:46:22 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:46:23 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:46:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b83e8a6ea044be2a9e3c87c5fdc047ce9a52d1a64e48f8330d9a19002ecffe1`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 300.1 KB (300117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9949bdfbb1d296dd158f8c2bb959f96c8da162a0d579f68fa3f5a4af58bed5b`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c5cc316af29a89f9a1d4e279b5d1bb964095a15795647d013f40921bc808c3`  
		Last Modified: Wed, 14 Apr 2021 19:47:54 GMT  
		Size: 10.9 MB (10944831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6670cc680ce5e5d9a0adfc380fe4a89ac2a2dcef5a7adeb874967a356e6742`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a41623f53d582c8b503ae859f6ae98c7c0695eddb11bdbf8514b9b914955c3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13639723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b837694902a1a259a4915444feda59d895ed37ffbef66b8518b9a884f029c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:39:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:39:34 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:39:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:39:43 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:39:45 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:39:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:39:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:39:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:39:56 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:39:57 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:39:58 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:39:59 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239ad5e698454501b0de011bffea35a660806a0b85a6141776581e3a98bc467`  
		Last Modified: Wed, 14 Apr 2021 19:41:24 GMT  
		Size: 299.2 KB (299210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0460b038be93717158ad9cdb6f83768b7129eaf4fcaef8620adc7509d0e5fe`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0905d1ca8c4f74966ae8a7b5ebe8fdb33854c4a759d543d767dd9a0add81f155`  
		Last Modified: Wed, 14 Apr 2021 19:41:29 GMT  
		Size: 10.9 MB (10925348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02da274f552e184a7fa5527990e666d77c70e3715a0d96b7588e7433b3022a`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:789a609d1ac52d0bed8718bab07beff0633df8333c8f88a4a54ccc6fa14bfb1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13616003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fab65bcfd86f1922cd2ec38aa336d5c219f99ed0d0878dede9732c770b2113`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:59:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 18:59:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 18:59:56 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:00:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:00:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:00:06 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:00:07 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:00:08 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:00:09 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:00:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:00:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:00:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:00:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:00:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:00:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:00:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:00:22 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:00:23 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:00:25 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:00:26 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:00:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96638d6a34d0588d1723cae433a6176b83e4bec10cb3a37ffac1891313dd144`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 300.4 KB (300352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e448c61e8710f135f93f0f19db0e1e20005299e4e28dfcbba2fc048075b11`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955bb49759c02742bb3fe501b864201c3b2a349f8253b73d7114ba39a816ac02`  
		Last Modified: Wed, 14 Apr 2021 19:01:54 GMT  
		Size: 10.6 MB (10598977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639f923159f69301bb290369ef4804ec8ef52d3d159d531976474f8d34d3dc54`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:f551e1db7910e2d5235d303760aff5b514fc6e8b49d8d67d434bb23c40ac25db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13356454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bd235f46e537404cdab42c3dfb3d0058f97ed5d7984f2e71ad8734adcc6a8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:09:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:09:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 22:09:24 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 22:09:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:09:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:09:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:10:01 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:10:06 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:10:15 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:10:22 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 22:10:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:10:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:10:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:10:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:11:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:11:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:11:20 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:11:27 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:11:35 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:11:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93dd31358a6e859a05bb506b946720f02c7ec7969776d811b20eaaa84508cd7`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 302.3 KB (302339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8077b8c9cca163d9a34281a866cf5fe991ff8c160ebd1ab1b617c6b722ec690`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55884816b8eca8150db9473989410e372c69c5431deb51a6cacd029895cf3dd6`  
		Last Modified: Wed, 14 Apr 2021 22:15:43 GMT  
		Size: 10.2 MB (10241380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efee06e0a650ff5f146fc54a695d4bf2b44e19da18120fdc494982d52cdd62`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:68aaf625a22bff4e71edf895129baa2d562765c24ac81a5c68aff2995ebf89c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14146947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd454f0dfa64ee1a952f9ed74a3f3bda3688a9565f062c3ea37e48b54eb210`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:21 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:07:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:07:22 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:07:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:07:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:07:27 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:07:27 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:07:30 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:07:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dab58470b754d248933aa56b48394e3ee4db4561d430d23ea378f0371ca59cb`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 300.5 KB (300471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd514b608428ea44dae7dc67e641a276593e7715178d86d7702153521de849d7`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a437814dab55b178c71f55598a70d0b532b3f645bdeb43e89244a6ebcde01446`  
		Last Modified: Wed, 14 Apr 2021 20:08:18 GMT  
		Size: 11.3 MB (11272061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412be9af105c69ee35fec76e8c0dbde8c8ba61c774b7d354e9c9fc8f538e8155`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:fa1ae85dc9b12ee47e98d7ef21db409eada3ed48f1865e4b1f1dd78f417132fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:6fbf52298c46c55c572670b5395ecaee5d399338003c9bb4e4abed875c542f4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395cc3713b2ca5574a9b4aafc468a1533d16582efe47dcab74ed547540d698a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:10:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:10:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:10:49 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:10:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:10:53 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:10:54 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:10:55 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:56 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:10:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a0cd9cca5be9b30bbc70611052d1456502e1f338ce4b14946233b21cd6a9a`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 300.0 KB (300016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5666523658a43fbbdff6b8fca498a988f4dcecc3ce027f1701414658c21d4ea`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097228407f13a161f68b188b0a4f255855b64d84e7b076745a744d5aa7ed8cf`  
		Last Modified: Wed, 14 Apr 2021 20:11:49 GMT  
		Size: 11.6 MB (11622383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40682d93cc09b4592a1b9c08d48d0a956b5eef4f123d80d1a12942482edb6aab`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0df9df9725cab39fe073887c98b54bf7bf1c96b3ed0e23916737c7c4877576c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13856181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce1c33ce4509195edc1c67d2dcd15c6c5fc0b35cec2e90714ec3007739600eb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:45:19 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:45:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:45:36 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:45:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:46:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:46:04 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:46:05 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:46:07 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:46:08 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:46:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:46:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:46:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:46:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:46:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:46:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:46:22 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:46:23 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:46:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b83e8a6ea044be2a9e3c87c5fdc047ce9a52d1a64e48f8330d9a19002ecffe1`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 300.1 KB (300117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9949bdfbb1d296dd158f8c2bb959f96c8da162a0d579f68fa3f5a4af58bed5b`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c5cc316af29a89f9a1d4e279b5d1bb964095a15795647d013f40921bc808c3`  
		Last Modified: Wed, 14 Apr 2021 19:47:54 GMT  
		Size: 10.9 MB (10944831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6670cc680ce5e5d9a0adfc380fe4a89ac2a2dcef5a7adeb874967a356e6742`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a41623f53d582c8b503ae859f6ae98c7c0695eddb11bdbf8514b9b914955c3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13639723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b837694902a1a259a4915444feda59d895ed37ffbef66b8518b9a884f029c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:39:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:39:34 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:39:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:39:43 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:39:45 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:39:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:39:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:39:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:39:56 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:39:57 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:39:58 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:39:59 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239ad5e698454501b0de011bffea35a660806a0b85a6141776581e3a98bc467`  
		Last Modified: Wed, 14 Apr 2021 19:41:24 GMT  
		Size: 299.2 KB (299210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0460b038be93717158ad9cdb6f83768b7129eaf4fcaef8620adc7509d0e5fe`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0905d1ca8c4f74966ae8a7b5ebe8fdb33854c4a759d543d767dd9a0add81f155`  
		Last Modified: Wed, 14 Apr 2021 19:41:29 GMT  
		Size: 10.9 MB (10925348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02da274f552e184a7fa5527990e666d77c70e3715a0d96b7588e7433b3022a`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:789a609d1ac52d0bed8718bab07beff0633df8333c8f88a4a54ccc6fa14bfb1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13616003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fab65bcfd86f1922cd2ec38aa336d5c219f99ed0d0878dede9732c770b2113`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:59:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 18:59:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 18:59:56 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:00:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:00:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:00:06 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:00:07 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:00:08 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:00:09 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:00:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:00:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:00:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:00:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:00:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:00:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:00:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:00:22 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:00:23 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:00:25 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:00:26 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:00:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96638d6a34d0588d1723cae433a6176b83e4bec10cb3a37ffac1891313dd144`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 300.4 KB (300352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e448c61e8710f135f93f0f19db0e1e20005299e4e28dfcbba2fc048075b11`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955bb49759c02742bb3fe501b864201c3b2a349f8253b73d7114ba39a816ac02`  
		Last Modified: Wed, 14 Apr 2021 19:01:54 GMT  
		Size: 10.6 MB (10598977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639f923159f69301bb290369ef4804ec8ef52d3d159d531976474f8d34d3dc54`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:f551e1db7910e2d5235d303760aff5b514fc6e8b49d8d67d434bb23c40ac25db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13356454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bd235f46e537404cdab42c3dfb3d0058f97ed5d7984f2e71ad8734adcc6a8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:09:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:09:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 22:09:24 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 22:09:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:09:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:09:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:10:01 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:10:06 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:10:15 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:10:22 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 22:10:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:10:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:10:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:10:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:11:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:11:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:11:20 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:11:27 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:11:35 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:11:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93dd31358a6e859a05bb506b946720f02c7ec7969776d811b20eaaa84508cd7`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 302.3 KB (302339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8077b8c9cca163d9a34281a866cf5fe991ff8c160ebd1ab1b617c6b722ec690`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55884816b8eca8150db9473989410e372c69c5431deb51a6cacd029895cf3dd6`  
		Last Modified: Wed, 14 Apr 2021 22:15:43 GMT  
		Size: 10.2 MB (10241380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efee06e0a650ff5f146fc54a695d4bf2b44e19da18120fdc494982d52cdd62`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:68aaf625a22bff4e71edf895129baa2d562765c24ac81a5c68aff2995ebf89c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14146947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd454f0dfa64ee1a952f9ed74a3f3bda3688a9565f062c3ea37e48b54eb210`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:21 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:07:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:07:22 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:07:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:07:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:07:27 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:07:27 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:07:30 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:07:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dab58470b754d248933aa56b48394e3ee4db4561d430d23ea378f0371ca59cb`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 300.5 KB (300471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd514b608428ea44dae7dc67e641a276593e7715178d86d7702153521de849d7`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a437814dab55b178c71f55598a70d0b532b3f645bdeb43e89244a6ebcde01446`  
		Last Modified: Wed, 14 Apr 2021 20:08:18 GMT  
		Size: 11.3 MB (11272061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412be9af105c69ee35fec76e8c0dbde8c8ba61c774b7d354e9c9fc8f538e8155`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:ee7737d128957678b88f6321b5107ec6e23963fa2012cf2188efc72722ad6f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:3eb8fd03c47af4395bea3f6bcb98e8385f4634c7f513e7746421ae828d62c66f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119544759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dab7b132f437ff0879dfdef9940c90324e4d6a4c5af7de0c2b7b256d5ebf21b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:29:08 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:29:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:29:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:32:48 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:34:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:34:19 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:34:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:34:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:34:20 GMT
WORKDIR /go
# Thu, 15 Apr 2021 09:28:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 09:28:59 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 09:29:00 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 09:29:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 09:29:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 09:29:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 09:29:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b54d2d4342f88201f48db57cae1f7edbacae870ee13d7962f999edd7529a9`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5898d3d0f1f95fd666f764bf918c1656be6169868335cb63bc428a5ef47cf32`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2292415af71b71f5b5eae8c7426f41afef6af628b410acf0b9d036240addeeb`  
		Last Modified: Wed, 14 Apr 2021 21:37:07 GMT  
		Size: 106.8 MB (106825070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483424ea5e047556d6172c0273d0671d368d0e42448ee6eee213adf6f0f0e218`  
		Last Modified: Wed, 14 Apr 2021 21:36:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936094b3e444e93dce0400536b066def6153e8795892e63e44042e3507f71fa7`  
		Last Modified: Thu, 15 Apr 2021 09:29:37 GMT  
		Size: 8.3 MB (8326458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41aa4f492f90b4b9472fbfce9bf1b1f4f9dc08fb9d9ec92fb040160716042e0`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 1.3 MB (1311071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9495ef365ef431007d48d2a011656481c0dcfe85888f9dc8d8780a41db96f26`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ca579a39dbe79f52268fdb5230c9a5ad7cfc115e540b515ecce7a557714b1711
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114723671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf78bfe4d146d0c0b28698b45888f4e663125f52bfb222cd1e7bf6e85248038`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:19:47 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:19:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:19:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:24 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:11:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:12:16 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:12:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:13:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:13:32 GMT
WORKDIR /go
# Thu, 15 Apr 2021 06:25:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 06:25:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 06:25:12 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 06:25:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 06:25:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 06:25:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 06:25:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c231c184d802a569805e44837dd1ea2cb0522bb03ca5763ef5ed9fae5896c`  
		Last Modified: Wed, 14 Apr 2021 21:15:05 GMT  
		Size: 281.0 KB (280982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8ca9e585b85be2e7ddaaf213e22bdb986eba4da2a8cc4d8b45f762752e17df`  
		Last Modified: Wed, 14 Apr 2021 21:15:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa237e1852b6dc6312c54835af4eedd49fc347da91eee2bd9a5cbdf3e4a09a74`  
		Last Modified: Wed, 14 Apr 2021 21:17:14 GMT  
		Size: 102.7 MB (102671404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfaf15ab73c5bd3fd51cf3ad7a986d94a84a0de33b0e2b421df3ece40813b6f`  
		Last Modified: Wed, 14 Apr 2021 21:16:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bceb981e039ba8e3426115768baf63e8372fc75250fbb6d6df522d9558b8abb8`  
		Last Modified: Thu, 15 Apr 2021 06:26:15 GMT  
		Size: 7.9 MB (7943726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec602f7edc3131a49dd0ab8bd4e7b207009dc592d13555e12296c433ef56919`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 1.2 MB (1221591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57d036d826077e94afba969b41b7bdc9d1ae0f266d04bc343350ff391e2fd75`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:28ae48497c0b64592d20b21b122fe14268d4ce85a5e9ea9b5b583d5a58726cfb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113527342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15cf44fde7fa3b279efe2039c6fb0882edb4c49fdc0076fc26c90bdcec1b365`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:28:16 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:28:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:28:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:19:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 22:43:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 22:43:26 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 22:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:43:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 22:43:36 GMT
WORKDIR /go
# Thu, 15 Apr 2021 07:39:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 07:39:41 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 07:39:43 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 07:39:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 07:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 07:39:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 07:39:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a884c3a8500725e0f08f924091ec61ae3e3acee3b0ffe5839b06f874ee63dc08`  
		Last Modified: Wed, 14 Apr 2021 22:45:08 GMT  
		Size: 280.1 KB (280078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f87f08a98de1e7cb636267b626d4e644775ff7962ea1ff9b4813f740b89e67`  
		Last Modified: Wed, 14 Apr 2021 22:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c59f8b5aa025c1cb85f375b22cbc86c2892e311a5aad724e9af892abbefca31`  
		Last Modified: Wed, 14 Apr 2021 22:47:06 GMT  
		Size: 102.5 MB (102463090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146d2365c5f44423fcd2cd482e0d74d784c72e892e81c7d26dd1aa1a8bd3ab43`  
		Last Modified: Wed, 14 Apr 2021 22:46:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689b9c2e77675507509d87b28e5aa533b980296e5ffa8999fa8268863b5691b5`  
		Last Modified: Thu, 15 Apr 2021 07:40:47 GMT  
		Size: 7.2 MB (7154833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c64d502102e5ce2b6b103a14d9af56e06fa146e4eb76cf6423e58e5407b6475`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 1.2 MB (1219446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a490f0c5cdae283a0f25e3bc46079442ea559abaa3cf16c64a5a0cef30befc45`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b89b93e92ffd9427041b5ed8850cc44f292b611e7dee55242ea02c6c3ccf2a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8d157b29403fa75da94e9701e2c3e3d065de48b910f8045b32619bdc25f1e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:09 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:46:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:46:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:54:59 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:58:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:58:21 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:58:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:58:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:58:41 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:44:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:44:05 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:44:06 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:44:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:44:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:44:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:44:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2150ab4b89a5dc832780f442998074db1582348dca0eb60d6b79b59df025f25f`  
		Last Modified: Wed, 14 Apr 2021 21:00:21 GMT  
		Size: 281.2 KB (281220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9d22c0ca7447b1a1b25889675e84f2ed68ecd519fdc513796712138820633b`  
		Last Modified: Wed, 14 Apr 2021 21:00:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cfb7326a4720568ee9867ad9f6dd4b796bcd9e899c6a27a3891589eae5cc06`  
		Last Modified: Wed, 14 Apr 2021 21:02:14 GMT  
		Size: 102.1 MB (102136232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a0cdf5ccbda3f4358749dfd4a03c520b2ca135a303988e74a5796796ccc30d`  
		Last Modified: Wed, 14 Apr 2021 21:01:48 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad8e65604482fa70f402e9fde824dec1ff3f257637f247fe6279c69757b9de6`  
		Last Modified: Thu, 15 Apr 2021 08:45:09 GMT  
		Size: 8.5 MB (8518404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1496bb71598cd42c2f92595b24f0aa7a34914fb6048c11499146f728964ddb`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 1.2 MB (1201555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1678712b911f6bb0ed8a67b615034fcec04e64bca853d43c39e3659d54e649`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4d7764de3f8d29cbb22b2b973802bbf36aa89b6c1e6a11cf6934b2273b80e59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113988669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c777710e48b168e93b792b4171e667a5c16209c668b09dd54d442ad4ef1c55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 31 Mar 2021 18:56:11 GMT
ADD file:d51af61c5955c980d18387ab532110c3874f95a87768be84dfd1eeb3e701d3a4 in / 
# Wed, 31 Mar 2021 18:56:16 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 04:33:46 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 01 Apr 2021 04:33:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 04:33:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:18:36 GMT
ENV GOLANG_VERSION=1.15.11
# Fri, 02 Apr 2021 03:20:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 02 Apr 2021 03:20:38 GMT
ENV GOPATH=/go
# Fri, 02 Apr 2021 03:20:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:20:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 02 Apr 2021 03:21:02 GMT
WORKDIR /go
# Fri, 02 Apr 2021 05:03:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 02 Apr 2021 05:03:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Fri, 02 Apr 2021 05:03:15 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 02 Apr 2021 05:03:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 02 Apr 2021 05:03:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 02 Apr 2021 05:03:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 02 Apr 2021 05:03:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6d4557865d9cec3513c1a5e744cb1073a563d464b8d546911289b9df9998f1b`  
		Last Modified: Wed, 31 Mar 2021 18:57:36 GMT  
		Size: 2.8 MB (2806070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128ce9f93b1dd5f42d7663646400f1307cddfad6a5361031e3a1ca8c46d90d2e`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 283.2 KB (283224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb52babc5b3ae7ccfca63bfc4092e7d57cbd51bc203af266e4fcb0169a6107`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91ebeddf57ad09e8e1b3eb1e312be6a4484d88f8f970a7b241d759abe98e5f`  
		Last Modified: Fri, 02 Apr 2021 03:25:31 GMT  
		Size: 100.8 MB (100806744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac05f37b09f2517038025dd2d905a5d3ecbd9af697023fe05bc857ed48b8f455`  
		Last Modified: Fri, 02 Apr 2021 03:25:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e2e6a908474ce0f09d3cc2e30293784024f2a821c330690e753b01155c5346`  
		Last Modified: Fri, 02 Apr 2021 05:04:26 GMT  
		Size: 8.9 MB (8921423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b888e7962a16510b476660b91df0be664af7f16e7eb94288112b51bfd206995`  
		Last Modified: Fri, 02 Apr 2021 05:04:25 GMT  
		Size: 1.2 MB (1170492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ce4e5965570ab285f5e3be6ab2ca4cd6b618b344303a3e09cbb4c46fb2393f`  
		Last Modified: Fri, 02 Apr 2021 05:04:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:75a9876d6656c0b08c814240a013160e20a41c6a4bfe5939f9befb45ab7e277c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118429233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3dc1b085458cb773f526584cf4e59ebff486ad9b1f684021e37907fd83cb1d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:59 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:47:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:47:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:51:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:51:52 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:51:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:51:53 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:47:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:47:02 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:47:03 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:47:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:47:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:47:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:47:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c45d0e43ef7a36e47dfc16916a076f7ba26b656842380c26207ad30f5c8b`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 281.3 KB (281343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f1645d6cbfccd2924337f37dc819e7edc27989ead8bc679441954a0e483c24`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3233df950b4b58e213bfc323437185867d0d54de06ac41e9e5c408ca83ecd5ca`  
		Last Modified: Wed, 14 Apr 2021 20:53:56 GMT  
		Size: 105.9 MB (105944122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3995327d2f868035d65ecb6b315f8595f43db3da3e10b19dbe964a66b6cfd746`  
		Last Modified: Wed, 14 Apr 2021 20:53:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04afa35fe1fde3bf4e11163aeea0b3f7c6084de121d5f071291ee325ac535f06`  
		Last Modified: Thu, 15 Apr 2021 08:47:53 GMT  
		Size: 8.4 MB (8370192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81b8ec43677381485cbedd3fa6dc24863c5d8f04d8700720662cc1293d70ef`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 1.3 MB (1264434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf872018e54c322f4f460c7e7816a9ae61c2a3c07f73d7f4324c18a21f6ccdfb`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:5d074fc96daecf65b6ea7aaaf9d2217f2c8f4e27a44e13800ee34ce2110620a1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2636098719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e88c818aa8954ae57e277c9730cdfa1dceee6b1cc34304b32f23f94a4ee916`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:47:04 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:50:03 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:50:05 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:10:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:10:40 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:10:41 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:11:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:11:16 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a6b8d8a4b8aea18e07888051dac03e88f4132fba08dca72e5795d9533dd3d`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67fec1bfee8619d88a924c4f9b9f4a04d2a0a1d199406157bb073b9f48d588`  
		Last Modified: Wed, 14 Apr 2021 13:07:33 GMT  
		Size: 134.1 MB (134133939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fe57ae793e79818d065737c8e995bb1b73296275794af222be695733711652`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.6 KB (1562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5134c3d8291dc3a52f7fad327cccf50377f2f362488fbcb8405addc74c0eedcf`  
		Last Modified: Wed, 14 Apr 2021 20:25:05 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d60772069c77cb2a80fec9f6e4d18084a4a919d4f776079dfee7903331331e7`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4716fdd15cdffc3b1aa557c81d58c2d0c343f9bfbfb501325b4cdc3bfeb426d9`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc11d2d339a72dd92f86f4fcc8e6fc299da2b6b381147f41dbd8d789e0c944e`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2909c1d8e32571506ce36cda43c7b113b299e280d6d7dfffafe5cd6284595348`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.7 MB (1712288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e56de156a63d8492bf70144c9e28ae975db36a6a57c54e734c96e20fb8bb13`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:436f2a16a677c719d951ddd10a1f475e81cc61b0726c7a4d5f76bdea16e3d215
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5982128974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1658b3cebc6cc5691856945858057a4e3925a991ead9db618b5058d55e445e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:50:19 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:54:08 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:54:10 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:11:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:11:24 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:11:25 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:11:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:12:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:13:01 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1388c10d71d4f1005ced63001aeb1392f019139011ddf961220ee27a412cbadb`  
		Last Modified: Wed, 14 Apr 2021 13:07:44 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913a59644a65d5f7183aa7bebce08c8b09d1f627c257105a7db7514919858b6e`  
		Last Modified: Wed, 14 Apr 2021 13:08:21 GMT  
		Size: 143.9 MB (143889855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b095a33aa8cc59c703b0a8f3b0bb53508123d89c531d6369de947b72b26f5`  
		Last Modified: Wed, 14 Apr 2021 13:07:46 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c7a21f93788806d3510b3cc8f7692b086c096861b42c218993697d04a890de`  
		Last Modified: Wed, 14 Apr 2021 20:25:25 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fbdf3acf4f09ad44474940358b0b044863361fee2bb201478a8b4b40cced75`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600e2fd01e09ce5bb623f7dbf3080c7127a8c2dc0b54422dee1525e75e6ae6de`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d594e3e36caa66775e5660018a80c02ef6bf4b16e626bdbca53a885634db4a29`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f5b24d29c79d20732eaf23dc495c89959ba869fbcb3bb88d35b42f38616a1`  
		Last Modified: Wed, 14 Apr 2021 20:25:24 GMT  
		Size: 7.0 MB (6976405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11b840b2827a9bb3da231a34e716b4fbd570dffa0b711f9fcbb7ff630c90052`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:388a8615423ce9d162146c4b22c552424c9ef7a58a27c091ae1cb3b3e85e3f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:3eb8fd03c47af4395bea3f6bcb98e8385f4634c7f513e7746421ae828d62c66f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119544759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dab7b132f437ff0879dfdef9940c90324e4d6a4c5af7de0c2b7b256d5ebf21b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:29:08 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:29:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:29:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:32:48 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:34:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:34:19 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:34:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:34:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:34:20 GMT
WORKDIR /go
# Thu, 15 Apr 2021 09:28:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 09:28:59 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 09:29:00 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 09:29:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 09:29:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 09:29:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 09:29:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b54d2d4342f88201f48db57cae1f7edbacae870ee13d7962f999edd7529a9`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5898d3d0f1f95fd666f764bf918c1656be6169868335cb63bc428a5ef47cf32`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2292415af71b71f5b5eae8c7426f41afef6af628b410acf0b9d036240addeeb`  
		Last Modified: Wed, 14 Apr 2021 21:37:07 GMT  
		Size: 106.8 MB (106825070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483424ea5e047556d6172c0273d0671d368d0e42448ee6eee213adf6f0f0e218`  
		Last Modified: Wed, 14 Apr 2021 21:36:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936094b3e444e93dce0400536b066def6153e8795892e63e44042e3507f71fa7`  
		Last Modified: Thu, 15 Apr 2021 09:29:37 GMT  
		Size: 8.3 MB (8326458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41aa4f492f90b4b9472fbfce9bf1b1f4f9dc08fb9d9ec92fb040160716042e0`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 1.3 MB (1311071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9495ef365ef431007d48d2a011656481c0dcfe85888f9dc8d8780a41db96f26`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ca579a39dbe79f52268fdb5230c9a5ad7cfc115e540b515ecce7a557714b1711
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114723671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf78bfe4d146d0c0b28698b45888f4e663125f52bfb222cd1e7bf6e85248038`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:19:47 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:19:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:19:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:24 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:11:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:12:16 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:12:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:13:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:13:32 GMT
WORKDIR /go
# Thu, 15 Apr 2021 06:25:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 06:25:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 06:25:12 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 06:25:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 06:25:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 06:25:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 06:25:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c231c184d802a569805e44837dd1ea2cb0522bb03ca5763ef5ed9fae5896c`  
		Last Modified: Wed, 14 Apr 2021 21:15:05 GMT  
		Size: 281.0 KB (280982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8ca9e585b85be2e7ddaaf213e22bdb986eba4da2a8cc4d8b45f762752e17df`  
		Last Modified: Wed, 14 Apr 2021 21:15:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa237e1852b6dc6312c54835af4eedd49fc347da91eee2bd9a5cbdf3e4a09a74`  
		Last Modified: Wed, 14 Apr 2021 21:17:14 GMT  
		Size: 102.7 MB (102671404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfaf15ab73c5bd3fd51cf3ad7a986d94a84a0de33b0e2b421df3ece40813b6f`  
		Last Modified: Wed, 14 Apr 2021 21:16:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bceb981e039ba8e3426115768baf63e8372fc75250fbb6d6df522d9558b8abb8`  
		Last Modified: Thu, 15 Apr 2021 06:26:15 GMT  
		Size: 7.9 MB (7943726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec602f7edc3131a49dd0ab8bd4e7b207009dc592d13555e12296c433ef56919`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 1.2 MB (1221591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57d036d826077e94afba969b41b7bdc9d1ae0f266d04bc343350ff391e2fd75`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:28ae48497c0b64592d20b21b122fe14268d4ce85a5e9ea9b5b583d5a58726cfb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113527342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15cf44fde7fa3b279efe2039c6fb0882edb4c49fdc0076fc26c90bdcec1b365`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:28:16 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:28:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:28:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:19:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 22:43:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 22:43:26 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 22:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:43:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 22:43:36 GMT
WORKDIR /go
# Thu, 15 Apr 2021 07:39:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 07:39:41 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 07:39:43 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 07:39:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 07:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 07:39:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 07:39:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a884c3a8500725e0f08f924091ec61ae3e3acee3b0ffe5839b06f874ee63dc08`  
		Last Modified: Wed, 14 Apr 2021 22:45:08 GMT  
		Size: 280.1 KB (280078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f87f08a98de1e7cb636267b626d4e644775ff7962ea1ff9b4813f740b89e67`  
		Last Modified: Wed, 14 Apr 2021 22:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c59f8b5aa025c1cb85f375b22cbc86c2892e311a5aad724e9af892abbefca31`  
		Last Modified: Wed, 14 Apr 2021 22:47:06 GMT  
		Size: 102.5 MB (102463090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146d2365c5f44423fcd2cd482e0d74d784c72e892e81c7d26dd1aa1a8bd3ab43`  
		Last Modified: Wed, 14 Apr 2021 22:46:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689b9c2e77675507509d87b28e5aa533b980296e5ffa8999fa8268863b5691b5`  
		Last Modified: Thu, 15 Apr 2021 07:40:47 GMT  
		Size: 7.2 MB (7154833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c64d502102e5ce2b6b103a14d9af56e06fa146e4eb76cf6423e58e5407b6475`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 1.2 MB (1219446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a490f0c5cdae283a0f25e3bc46079442ea559abaa3cf16c64a5a0cef30befc45`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b89b93e92ffd9427041b5ed8850cc44f292b611e7dee55242ea02c6c3ccf2a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8d157b29403fa75da94e9701e2c3e3d065de48b910f8045b32619bdc25f1e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:09 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:46:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:46:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:54:59 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:58:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:58:21 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:58:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:58:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:58:41 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:44:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:44:05 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:44:06 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:44:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:44:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:44:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:44:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2150ab4b89a5dc832780f442998074db1582348dca0eb60d6b79b59df025f25f`  
		Last Modified: Wed, 14 Apr 2021 21:00:21 GMT  
		Size: 281.2 KB (281220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9d22c0ca7447b1a1b25889675e84f2ed68ecd519fdc513796712138820633b`  
		Last Modified: Wed, 14 Apr 2021 21:00:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cfb7326a4720568ee9867ad9f6dd4b796bcd9e899c6a27a3891589eae5cc06`  
		Last Modified: Wed, 14 Apr 2021 21:02:14 GMT  
		Size: 102.1 MB (102136232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a0cdf5ccbda3f4358749dfd4a03c520b2ca135a303988e74a5796796ccc30d`  
		Last Modified: Wed, 14 Apr 2021 21:01:48 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad8e65604482fa70f402e9fde824dec1ff3f257637f247fe6279c69757b9de6`  
		Last Modified: Thu, 15 Apr 2021 08:45:09 GMT  
		Size: 8.5 MB (8518404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1496bb71598cd42c2f92595b24f0aa7a34914fb6048c11499146f728964ddb`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 1.2 MB (1201555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1678712b911f6bb0ed8a67b615034fcec04e64bca853d43c39e3659d54e649`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4d7764de3f8d29cbb22b2b973802bbf36aa89b6c1e6a11cf6934b2273b80e59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113988669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c777710e48b168e93b792b4171e667a5c16209c668b09dd54d442ad4ef1c55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 31 Mar 2021 18:56:11 GMT
ADD file:d51af61c5955c980d18387ab532110c3874f95a87768be84dfd1eeb3e701d3a4 in / 
# Wed, 31 Mar 2021 18:56:16 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 04:33:46 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 01 Apr 2021 04:33:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 04:33:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:18:36 GMT
ENV GOLANG_VERSION=1.15.11
# Fri, 02 Apr 2021 03:20:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 02 Apr 2021 03:20:38 GMT
ENV GOPATH=/go
# Fri, 02 Apr 2021 03:20:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:20:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 02 Apr 2021 03:21:02 GMT
WORKDIR /go
# Fri, 02 Apr 2021 05:03:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 02 Apr 2021 05:03:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Fri, 02 Apr 2021 05:03:15 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 02 Apr 2021 05:03:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 02 Apr 2021 05:03:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 02 Apr 2021 05:03:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 02 Apr 2021 05:03:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6d4557865d9cec3513c1a5e744cb1073a563d464b8d546911289b9df9998f1b`  
		Last Modified: Wed, 31 Mar 2021 18:57:36 GMT  
		Size: 2.8 MB (2806070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128ce9f93b1dd5f42d7663646400f1307cddfad6a5361031e3a1ca8c46d90d2e`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 283.2 KB (283224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb52babc5b3ae7ccfca63bfc4092e7d57cbd51bc203af266e4fcb0169a6107`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91ebeddf57ad09e8e1b3eb1e312be6a4484d88f8f970a7b241d759abe98e5f`  
		Last Modified: Fri, 02 Apr 2021 03:25:31 GMT  
		Size: 100.8 MB (100806744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac05f37b09f2517038025dd2d905a5d3ecbd9af697023fe05bc857ed48b8f455`  
		Last Modified: Fri, 02 Apr 2021 03:25:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e2e6a908474ce0f09d3cc2e30293784024f2a821c330690e753b01155c5346`  
		Last Modified: Fri, 02 Apr 2021 05:04:26 GMT  
		Size: 8.9 MB (8921423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b888e7962a16510b476660b91df0be664af7f16e7eb94288112b51bfd206995`  
		Last Modified: Fri, 02 Apr 2021 05:04:25 GMT  
		Size: 1.2 MB (1170492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ce4e5965570ab285f5e3be6ab2ca4cd6b618b344303a3e09cbb4c46fb2393f`  
		Last Modified: Fri, 02 Apr 2021 05:04:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:75a9876d6656c0b08c814240a013160e20a41c6a4bfe5939f9befb45ab7e277c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118429233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3dc1b085458cb773f526584cf4e59ebff486ad9b1f684021e37907fd83cb1d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:59 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:47:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:47:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:51:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:51:52 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:51:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:51:53 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:47:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:47:02 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:47:03 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:47:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:47:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:47:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:47:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c45d0e43ef7a36e47dfc16916a076f7ba26b656842380c26207ad30f5c8b`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 281.3 KB (281343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f1645d6cbfccd2924337f37dc819e7edc27989ead8bc679441954a0e483c24`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3233df950b4b58e213bfc323437185867d0d54de06ac41e9e5c408ca83ecd5ca`  
		Last Modified: Wed, 14 Apr 2021 20:53:56 GMT  
		Size: 105.9 MB (105944122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3995327d2f868035d65ecb6b315f8595f43db3da3e10b19dbe964a66b6cfd746`  
		Last Modified: Wed, 14 Apr 2021 20:53:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04afa35fe1fde3bf4e11163aeea0b3f7c6084de121d5f071291ee325ac535f06`  
		Last Modified: Thu, 15 Apr 2021 08:47:53 GMT  
		Size: 8.4 MB (8370192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81b8ec43677381485cbedd3fa6dc24863c5d8f04d8700720662cc1293d70ef`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 1.3 MB (1264434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf872018e54c322f4f460c7e7816a9ae61c2a3c07f73d7f4324c18a21f6ccdfb`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:0ee0dd2e13c7c2d8b1a3514be4c8a71a5da92f756386f549bdd51c0bd62700c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:5d074fc96daecf65b6ea7aaaf9d2217f2c8f4e27a44e13800ee34ce2110620a1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2636098719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e88c818aa8954ae57e277c9730cdfa1dceee6b1cc34304b32f23f94a4ee916`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:47:04 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:50:03 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:50:05 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:10:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:10:40 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:10:41 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:11:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:11:16 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a6b8d8a4b8aea18e07888051dac03e88f4132fba08dca72e5795d9533dd3d`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67fec1bfee8619d88a924c4f9b9f4a04d2a0a1d199406157bb073b9f48d588`  
		Last Modified: Wed, 14 Apr 2021 13:07:33 GMT  
		Size: 134.1 MB (134133939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fe57ae793e79818d065737c8e995bb1b73296275794af222be695733711652`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.6 KB (1562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5134c3d8291dc3a52f7fad327cccf50377f2f362488fbcb8405addc74c0eedcf`  
		Last Modified: Wed, 14 Apr 2021 20:25:05 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d60772069c77cb2a80fec9f6e4d18084a4a919d4f776079dfee7903331331e7`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4716fdd15cdffc3b1aa557c81d58c2d0c343f9bfbfb501325b4cdc3bfeb426d9`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc11d2d339a72dd92f86f4fcc8e6fc299da2b6b381147f41dbd8d789e0c944e`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2909c1d8e32571506ce36cda43c7b113b299e280d6d7dfffafe5cd6284595348`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.7 MB (1712288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e56de156a63d8492bf70144c9e28ae975db36a6a57c54e734c96e20fb8bb13`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:80d881fa828e30f1c7d44ae2d3bebe98ef9185d4e43e597ac5205ba32ad13c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:436f2a16a677c719d951ddd10a1f475e81cc61b0726c7a4d5f76bdea16e3d215
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5982128974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1658b3cebc6cc5691856945858057a4e3925a991ead9db618b5058d55e445e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:50:19 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:54:08 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:54:10 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:11:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:11:24 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:11:25 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:11:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:12:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:13:01 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1388c10d71d4f1005ced63001aeb1392f019139011ddf961220ee27a412cbadb`  
		Last Modified: Wed, 14 Apr 2021 13:07:44 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913a59644a65d5f7183aa7bebce08c8b09d1f627c257105a7db7514919858b6e`  
		Last Modified: Wed, 14 Apr 2021 13:08:21 GMT  
		Size: 143.9 MB (143889855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b095a33aa8cc59c703b0a8f3b0bb53508123d89c531d6369de947b72b26f5`  
		Last Modified: Wed, 14 Apr 2021 13:07:46 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c7a21f93788806d3510b3cc8f7692b086c096861b42c218993697d04a890de`  
		Last Modified: Wed, 14 Apr 2021 20:25:25 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fbdf3acf4f09ad44474940358b0b044863361fee2bb201478a8b4b40cced75`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600e2fd01e09ce5bb623f7dbf3080c7127a8c2dc0b54422dee1525e75e6ae6de`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d594e3e36caa66775e5660018a80c02ef6bf4b16e626bdbca53a885634db4a29`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f5b24d29c79d20732eaf23dc495c89959ba869fbcb3bb88d35b42f38616a1`  
		Last Modified: Wed, 14 Apr 2021 20:25:24 GMT  
		Size: 7.0 MB (6976405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11b840b2827a9bb3da231a34e716b4fbd570dffa0b711f9fcbb7ff630c90052`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:6a199f80cee0da0b39f4deffc53efac536c60672f4d8d26887f8f8ec194da3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:89f75ffc06d5f7a7cc6d37f38c9198d869993fa7426542d14c1a8bfdbb467694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:a42a67f914fd976a839e8c725f15fec79415b331ffeaa3972e7bff363bec4ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0`

```console
$ docker pull caddy@sha256:88fc125055b8c4dafe67a48219fd3a89c0a472aa254d2835b2e298b93493b28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.3.0` - linux; amd64

```console
$ docker pull caddy@sha256:6fbf52298c46c55c572670b5395ecaee5d399338003c9bb4e4abed875c542f4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395cc3713b2ca5574a9b4aafc468a1533d16582efe47dcab74ed547540d698a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:10:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:10:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:10:49 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:10:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:10:53 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:10:54 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:10:55 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:56 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:10:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a0cd9cca5be9b30bbc70611052d1456502e1f338ce4b14946233b21cd6a9a`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 300.0 KB (300016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5666523658a43fbbdff6b8fca498a988f4dcecc3ce027f1701414658c21d4ea`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097228407f13a161f68b188b0a4f255855b64d84e7b076745a744d5aa7ed8cf`  
		Last Modified: Wed, 14 Apr 2021 20:11:49 GMT  
		Size: 11.6 MB (11622383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40682d93cc09b4592a1b9c08d48d0a956b5eef4f123d80d1a12942482edb6aab`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0df9df9725cab39fe073887c98b54bf7bf1c96b3ed0e23916737c7c4877576c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13856181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce1c33ce4509195edc1c67d2dcd15c6c5fc0b35cec2e90714ec3007739600eb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:45:19 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:45:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:45:36 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:45:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:46:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:46:04 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:46:05 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:46:07 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:46:08 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:46:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:46:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:46:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:46:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:46:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:46:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:46:22 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:46:23 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:46:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b83e8a6ea044be2a9e3c87c5fdc047ce9a52d1a64e48f8330d9a19002ecffe1`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 300.1 KB (300117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9949bdfbb1d296dd158f8c2bb959f96c8da162a0d579f68fa3f5a4af58bed5b`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c5cc316af29a89f9a1d4e279b5d1bb964095a15795647d013f40921bc808c3`  
		Last Modified: Wed, 14 Apr 2021 19:47:54 GMT  
		Size: 10.9 MB (10944831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6670cc680ce5e5d9a0adfc380fe4a89ac2a2dcef5a7adeb874967a356e6742`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a41623f53d582c8b503ae859f6ae98c7c0695eddb11bdbf8514b9b914955c3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13639723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b837694902a1a259a4915444feda59d895ed37ffbef66b8518b9a884f029c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:39:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:39:34 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:39:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:39:43 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:39:45 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:39:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:39:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:39:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:39:56 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:39:57 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:39:58 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:39:59 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239ad5e698454501b0de011bffea35a660806a0b85a6141776581e3a98bc467`  
		Last Modified: Wed, 14 Apr 2021 19:41:24 GMT  
		Size: 299.2 KB (299210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0460b038be93717158ad9cdb6f83768b7129eaf4fcaef8620adc7509d0e5fe`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0905d1ca8c4f74966ae8a7b5ebe8fdb33854c4a759d543d767dd9a0add81f155`  
		Last Modified: Wed, 14 Apr 2021 19:41:29 GMT  
		Size: 10.9 MB (10925348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02da274f552e184a7fa5527990e666d77c70e3715a0d96b7588e7433b3022a`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:789a609d1ac52d0bed8718bab07beff0633df8333c8f88a4a54ccc6fa14bfb1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13616003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fab65bcfd86f1922cd2ec38aa336d5c219f99ed0d0878dede9732c770b2113`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:59:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 18:59:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 18:59:56 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:00:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:00:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:00:06 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:00:07 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:00:08 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:00:09 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:00:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:00:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:00:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:00:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:00:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:00:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:00:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:00:22 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:00:23 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:00:25 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:00:26 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:00:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96638d6a34d0588d1723cae433a6176b83e4bec10cb3a37ffac1891313dd144`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 300.4 KB (300352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e448c61e8710f135f93f0f19db0e1e20005299e4e28dfcbba2fc048075b11`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955bb49759c02742bb3fe501b864201c3b2a349f8253b73d7114ba39a816ac02`  
		Last Modified: Wed, 14 Apr 2021 19:01:54 GMT  
		Size: 10.6 MB (10598977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639f923159f69301bb290369ef4804ec8ef52d3d159d531976474f8d34d3dc54`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - linux; ppc64le

```console
$ docker pull caddy@sha256:f551e1db7910e2d5235d303760aff5b514fc6e8b49d8d67d434bb23c40ac25db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13356454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bd235f46e537404cdab42c3dfb3d0058f97ed5d7984f2e71ad8734adcc6a8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:09:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:09:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 22:09:24 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 22:09:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:09:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:09:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:10:01 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:10:06 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:10:15 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:10:22 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 22:10:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:10:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:10:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:10:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:11:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:11:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:11:20 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:11:27 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:11:35 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:11:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93dd31358a6e859a05bb506b946720f02c7ec7969776d811b20eaaa84508cd7`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 302.3 KB (302339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8077b8c9cca163d9a34281a866cf5fe991ff8c160ebd1ab1b617c6b722ec690`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55884816b8eca8150db9473989410e372c69c5431deb51a6cacd029895cf3dd6`  
		Last Modified: Wed, 14 Apr 2021 22:15:43 GMT  
		Size: 10.2 MB (10241380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efee06e0a650ff5f146fc54a695d4bf2b44e19da18120fdc494982d52cdd62`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - linux; s390x

```console
$ docker pull caddy@sha256:68aaf625a22bff4e71edf895129baa2d562765c24ac81a5c68aff2995ebf89c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14146947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd454f0dfa64ee1a952f9ed74a3f3bda3688a9565f062c3ea37e48b54eb210`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:21 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:07:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:07:22 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:07:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:07:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:07:27 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:07:27 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:07:30 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:07:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dab58470b754d248933aa56b48394e3ee4db4561d430d23ea378f0371ca59cb`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 300.5 KB (300471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd514b608428ea44dae7dc67e641a276593e7715178d86d7702153521de849d7`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a437814dab55b178c71f55598a70d0b532b3f645bdeb43e89244a6ebcde01446`  
		Last Modified: Wed, 14 Apr 2021 20:08:18 GMT  
		Size: 11.3 MB (11272061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412be9af105c69ee35fec76e8c0dbde8c8ba61c774b7d354e9c9fc8f538e8155`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-alpine`

```console
$ docker pull caddy@sha256:fa1ae85dc9b12ee47e98d7ef21db409eada3ed48f1865e4b1f1dd78f417132fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.3.0-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:6fbf52298c46c55c572670b5395ecaee5d399338003c9bb4e4abed875c542f4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395cc3713b2ca5574a9b4aafc468a1533d16582efe47dcab74ed547540d698a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:10:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:10:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:10:49 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:10:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:10:53 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:10:54 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:10:55 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:56 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:10:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a0cd9cca5be9b30bbc70611052d1456502e1f338ce4b14946233b21cd6a9a`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 300.0 KB (300016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5666523658a43fbbdff6b8fca498a988f4dcecc3ce027f1701414658c21d4ea`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097228407f13a161f68b188b0a4f255855b64d84e7b076745a744d5aa7ed8cf`  
		Last Modified: Wed, 14 Apr 2021 20:11:49 GMT  
		Size: 11.6 MB (11622383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40682d93cc09b4592a1b9c08d48d0a956b5eef4f123d80d1a12942482edb6aab`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0df9df9725cab39fe073887c98b54bf7bf1c96b3ed0e23916737c7c4877576c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13856181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce1c33ce4509195edc1c67d2dcd15c6c5fc0b35cec2e90714ec3007739600eb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:45:19 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:45:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:45:36 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:45:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:46:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:46:04 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:46:05 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:46:07 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:46:08 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:46:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:46:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:46:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:46:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:46:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:46:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:46:22 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:46:23 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:46:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b83e8a6ea044be2a9e3c87c5fdc047ce9a52d1a64e48f8330d9a19002ecffe1`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 300.1 KB (300117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9949bdfbb1d296dd158f8c2bb959f96c8da162a0d579f68fa3f5a4af58bed5b`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c5cc316af29a89f9a1d4e279b5d1bb964095a15795647d013f40921bc808c3`  
		Last Modified: Wed, 14 Apr 2021 19:47:54 GMT  
		Size: 10.9 MB (10944831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6670cc680ce5e5d9a0adfc380fe4a89ac2a2dcef5a7adeb874967a356e6742`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a41623f53d582c8b503ae859f6ae98c7c0695eddb11bdbf8514b9b914955c3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13639723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b837694902a1a259a4915444feda59d895ed37ffbef66b8518b9a884f029c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:39:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:39:34 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:39:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:39:43 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:39:45 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:39:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:39:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:39:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:39:56 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:39:57 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:39:58 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:39:59 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239ad5e698454501b0de011bffea35a660806a0b85a6141776581e3a98bc467`  
		Last Modified: Wed, 14 Apr 2021 19:41:24 GMT  
		Size: 299.2 KB (299210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0460b038be93717158ad9cdb6f83768b7129eaf4fcaef8620adc7509d0e5fe`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0905d1ca8c4f74966ae8a7b5ebe8fdb33854c4a759d543d767dd9a0add81f155`  
		Last Modified: Wed, 14 Apr 2021 19:41:29 GMT  
		Size: 10.9 MB (10925348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02da274f552e184a7fa5527990e666d77c70e3715a0d96b7588e7433b3022a`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:789a609d1ac52d0bed8718bab07beff0633df8333c8f88a4a54ccc6fa14bfb1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13616003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fab65bcfd86f1922cd2ec38aa336d5c219f99ed0d0878dede9732c770b2113`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:59:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 18:59:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 18:59:56 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:00:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:00:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:00:06 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:00:07 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:00:08 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:00:09 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:00:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:00:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:00:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:00:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:00:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:00:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:00:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:00:22 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:00:23 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:00:25 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:00:26 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:00:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96638d6a34d0588d1723cae433a6176b83e4bec10cb3a37ffac1891313dd144`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 300.4 KB (300352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e448c61e8710f135f93f0f19db0e1e20005299e4e28dfcbba2fc048075b11`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955bb49759c02742bb3fe501b864201c3b2a349f8253b73d7114ba39a816ac02`  
		Last Modified: Wed, 14 Apr 2021 19:01:54 GMT  
		Size: 10.6 MB (10598977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639f923159f69301bb290369ef4804ec8ef52d3d159d531976474f8d34d3dc54`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:f551e1db7910e2d5235d303760aff5b514fc6e8b49d8d67d434bb23c40ac25db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13356454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bd235f46e537404cdab42c3dfb3d0058f97ed5d7984f2e71ad8734adcc6a8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:09:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:09:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 22:09:24 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 22:09:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:09:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:09:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:10:01 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:10:06 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:10:15 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:10:22 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 22:10:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:10:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:10:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:10:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:11:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:11:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:11:20 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:11:27 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:11:35 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:11:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93dd31358a6e859a05bb506b946720f02c7ec7969776d811b20eaaa84508cd7`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 302.3 KB (302339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8077b8c9cca163d9a34281a866cf5fe991ff8c160ebd1ab1b617c6b722ec690`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55884816b8eca8150db9473989410e372c69c5431deb51a6cacd029895cf3dd6`  
		Last Modified: Wed, 14 Apr 2021 22:15:43 GMT  
		Size: 10.2 MB (10241380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efee06e0a650ff5f146fc54a695d4bf2b44e19da18120fdc494982d52cdd62`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:68aaf625a22bff4e71edf895129baa2d562765c24ac81a5c68aff2995ebf89c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14146947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd454f0dfa64ee1a952f9ed74a3f3bda3688a9565f062c3ea37e48b54eb210`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:21 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:07:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:07:22 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:07:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:07:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:07:27 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:07:27 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:07:30 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:07:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dab58470b754d248933aa56b48394e3ee4db4561d430d23ea378f0371ca59cb`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 300.5 KB (300471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd514b608428ea44dae7dc67e641a276593e7715178d86d7702153521de849d7`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a437814dab55b178c71f55598a70d0b532b3f645bdeb43e89244a6ebcde01446`  
		Last Modified: Wed, 14 Apr 2021 20:08:18 GMT  
		Size: 11.3 MB (11272061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412be9af105c69ee35fec76e8c0dbde8c8ba61c774b7d354e9c9fc8f538e8155`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-builder`

```console
$ docker pull caddy@sha256:ee7737d128957678b88f6321b5107ec6e23963fa2012cf2188efc72722ad6f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.3.0-builder` - linux; amd64

```console
$ docker pull caddy@sha256:3eb8fd03c47af4395bea3f6bcb98e8385f4634c7f513e7746421ae828d62c66f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119544759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dab7b132f437ff0879dfdef9940c90324e4d6a4c5af7de0c2b7b256d5ebf21b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:29:08 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:29:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:29:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:32:48 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:34:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:34:19 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:34:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:34:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:34:20 GMT
WORKDIR /go
# Thu, 15 Apr 2021 09:28:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 09:28:59 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 09:29:00 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 09:29:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 09:29:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 09:29:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 09:29:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b54d2d4342f88201f48db57cae1f7edbacae870ee13d7962f999edd7529a9`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5898d3d0f1f95fd666f764bf918c1656be6169868335cb63bc428a5ef47cf32`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2292415af71b71f5b5eae8c7426f41afef6af628b410acf0b9d036240addeeb`  
		Last Modified: Wed, 14 Apr 2021 21:37:07 GMT  
		Size: 106.8 MB (106825070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483424ea5e047556d6172c0273d0671d368d0e42448ee6eee213adf6f0f0e218`  
		Last Modified: Wed, 14 Apr 2021 21:36:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936094b3e444e93dce0400536b066def6153e8795892e63e44042e3507f71fa7`  
		Last Modified: Thu, 15 Apr 2021 09:29:37 GMT  
		Size: 8.3 MB (8326458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41aa4f492f90b4b9472fbfce9bf1b1f4f9dc08fb9d9ec92fb040160716042e0`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 1.3 MB (1311071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9495ef365ef431007d48d2a011656481c0dcfe85888f9dc8d8780a41db96f26`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ca579a39dbe79f52268fdb5230c9a5ad7cfc115e540b515ecce7a557714b1711
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114723671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf78bfe4d146d0c0b28698b45888f4e663125f52bfb222cd1e7bf6e85248038`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:19:47 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:19:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:19:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:24 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:11:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:12:16 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:12:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:13:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:13:32 GMT
WORKDIR /go
# Thu, 15 Apr 2021 06:25:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 06:25:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 06:25:12 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 06:25:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 06:25:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 06:25:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 06:25:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c231c184d802a569805e44837dd1ea2cb0522bb03ca5763ef5ed9fae5896c`  
		Last Modified: Wed, 14 Apr 2021 21:15:05 GMT  
		Size: 281.0 KB (280982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8ca9e585b85be2e7ddaaf213e22bdb986eba4da2a8cc4d8b45f762752e17df`  
		Last Modified: Wed, 14 Apr 2021 21:15:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa237e1852b6dc6312c54835af4eedd49fc347da91eee2bd9a5cbdf3e4a09a74`  
		Last Modified: Wed, 14 Apr 2021 21:17:14 GMT  
		Size: 102.7 MB (102671404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfaf15ab73c5bd3fd51cf3ad7a986d94a84a0de33b0e2b421df3ece40813b6f`  
		Last Modified: Wed, 14 Apr 2021 21:16:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bceb981e039ba8e3426115768baf63e8372fc75250fbb6d6df522d9558b8abb8`  
		Last Modified: Thu, 15 Apr 2021 06:26:15 GMT  
		Size: 7.9 MB (7943726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec602f7edc3131a49dd0ab8bd4e7b207009dc592d13555e12296c433ef56919`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 1.2 MB (1221591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57d036d826077e94afba969b41b7bdc9d1ae0f266d04bc343350ff391e2fd75`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:28ae48497c0b64592d20b21b122fe14268d4ce85a5e9ea9b5b583d5a58726cfb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113527342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15cf44fde7fa3b279efe2039c6fb0882edb4c49fdc0076fc26c90bdcec1b365`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:28:16 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:28:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:28:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:19:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 22:43:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 22:43:26 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 22:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:43:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 22:43:36 GMT
WORKDIR /go
# Thu, 15 Apr 2021 07:39:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 07:39:41 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 07:39:43 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 07:39:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 07:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 07:39:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 07:39:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a884c3a8500725e0f08f924091ec61ae3e3acee3b0ffe5839b06f874ee63dc08`  
		Last Modified: Wed, 14 Apr 2021 22:45:08 GMT  
		Size: 280.1 KB (280078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f87f08a98de1e7cb636267b626d4e644775ff7962ea1ff9b4813f740b89e67`  
		Last Modified: Wed, 14 Apr 2021 22:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c59f8b5aa025c1cb85f375b22cbc86c2892e311a5aad724e9af892abbefca31`  
		Last Modified: Wed, 14 Apr 2021 22:47:06 GMT  
		Size: 102.5 MB (102463090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146d2365c5f44423fcd2cd482e0d74d784c72e892e81c7d26dd1aa1a8bd3ab43`  
		Last Modified: Wed, 14 Apr 2021 22:46:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689b9c2e77675507509d87b28e5aa533b980296e5ffa8999fa8268863b5691b5`  
		Last Modified: Thu, 15 Apr 2021 07:40:47 GMT  
		Size: 7.2 MB (7154833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c64d502102e5ce2b6b103a14d9af56e06fa146e4eb76cf6423e58e5407b6475`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 1.2 MB (1219446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a490f0c5cdae283a0f25e3bc46079442ea559abaa3cf16c64a5a0cef30befc45`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b89b93e92ffd9427041b5ed8850cc44f292b611e7dee55242ea02c6c3ccf2a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8d157b29403fa75da94e9701e2c3e3d065de48b910f8045b32619bdc25f1e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:09 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:46:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:46:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:54:59 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:58:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:58:21 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:58:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:58:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:58:41 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:44:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:44:05 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:44:06 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:44:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:44:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:44:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:44:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2150ab4b89a5dc832780f442998074db1582348dca0eb60d6b79b59df025f25f`  
		Last Modified: Wed, 14 Apr 2021 21:00:21 GMT  
		Size: 281.2 KB (281220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9d22c0ca7447b1a1b25889675e84f2ed68ecd519fdc513796712138820633b`  
		Last Modified: Wed, 14 Apr 2021 21:00:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cfb7326a4720568ee9867ad9f6dd4b796bcd9e899c6a27a3891589eae5cc06`  
		Last Modified: Wed, 14 Apr 2021 21:02:14 GMT  
		Size: 102.1 MB (102136232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a0cdf5ccbda3f4358749dfd4a03c520b2ca135a303988e74a5796796ccc30d`  
		Last Modified: Wed, 14 Apr 2021 21:01:48 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad8e65604482fa70f402e9fde824dec1ff3f257637f247fe6279c69757b9de6`  
		Last Modified: Thu, 15 Apr 2021 08:45:09 GMT  
		Size: 8.5 MB (8518404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1496bb71598cd42c2f92595b24f0aa7a34914fb6048c11499146f728964ddb`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 1.2 MB (1201555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1678712b911f6bb0ed8a67b615034fcec04e64bca853d43c39e3659d54e649`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4d7764de3f8d29cbb22b2b973802bbf36aa89b6c1e6a11cf6934b2273b80e59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113988669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c777710e48b168e93b792b4171e667a5c16209c668b09dd54d442ad4ef1c55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 31 Mar 2021 18:56:11 GMT
ADD file:d51af61c5955c980d18387ab532110c3874f95a87768be84dfd1eeb3e701d3a4 in / 
# Wed, 31 Mar 2021 18:56:16 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 04:33:46 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 01 Apr 2021 04:33:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 04:33:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:18:36 GMT
ENV GOLANG_VERSION=1.15.11
# Fri, 02 Apr 2021 03:20:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 02 Apr 2021 03:20:38 GMT
ENV GOPATH=/go
# Fri, 02 Apr 2021 03:20:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:20:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 02 Apr 2021 03:21:02 GMT
WORKDIR /go
# Fri, 02 Apr 2021 05:03:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 02 Apr 2021 05:03:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Fri, 02 Apr 2021 05:03:15 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 02 Apr 2021 05:03:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 02 Apr 2021 05:03:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 02 Apr 2021 05:03:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 02 Apr 2021 05:03:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6d4557865d9cec3513c1a5e744cb1073a563d464b8d546911289b9df9998f1b`  
		Last Modified: Wed, 31 Mar 2021 18:57:36 GMT  
		Size: 2.8 MB (2806070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128ce9f93b1dd5f42d7663646400f1307cddfad6a5361031e3a1ca8c46d90d2e`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 283.2 KB (283224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb52babc5b3ae7ccfca63bfc4092e7d57cbd51bc203af266e4fcb0169a6107`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91ebeddf57ad09e8e1b3eb1e312be6a4484d88f8f970a7b241d759abe98e5f`  
		Last Modified: Fri, 02 Apr 2021 03:25:31 GMT  
		Size: 100.8 MB (100806744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac05f37b09f2517038025dd2d905a5d3ecbd9af697023fe05bc857ed48b8f455`  
		Last Modified: Fri, 02 Apr 2021 03:25:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e2e6a908474ce0f09d3cc2e30293784024f2a821c330690e753b01155c5346`  
		Last Modified: Fri, 02 Apr 2021 05:04:26 GMT  
		Size: 8.9 MB (8921423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b888e7962a16510b476660b91df0be664af7f16e7eb94288112b51bfd206995`  
		Last Modified: Fri, 02 Apr 2021 05:04:25 GMT  
		Size: 1.2 MB (1170492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ce4e5965570ab285f5e3be6ab2ca4cd6b618b344303a3e09cbb4c46fb2393f`  
		Last Modified: Fri, 02 Apr 2021 05:04:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - linux; s390x

```console
$ docker pull caddy@sha256:75a9876d6656c0b08c814240a013160e20a41c6a4bfe5939f9befb45ab7e277c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118429233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3dc1b085458cb773f526584cf4e59ebff486ad9b1f684021e37907fd83cb1d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:59 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:47:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:47:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:51:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:51:52 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:51:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:51:53 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:47:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:47:02 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:47:03 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:47:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:47:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:47:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:47:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c45d0e43ef7a36e47dfc16916a076f7ba26b656842380c26207ad30f5c8b`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 281.3 KB (281343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f1645d6cbfccd2924337f37dc819e7edc27989ead8bc679441954a0e483c24`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3233df950b4b58e213bfc323437185867d0d54de06ac41e9e5c408ca83ecd5ca`  
		Last Modified: Wed, 14 Apr 2021 20:53:56 GMT  
		Size: 105.9 MB (105944122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3995327d2f868035d65ecb6b315f8595f43db3da3e10b19dbe964a66b6cfd746`  
		Last Modified: Wed, 14 Apr 2021 20:53:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04afa35fe1fde3bf4e11163aeea0b3f7c6084de121d5f071291ee325ac535f06`  
		Last Modified: Thu, 15 Apr 2021 08:47:53 GMT  
		Size: 8.4 MB (8370192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81b8ec43677381485cbedd3fa6dc24863c5d8f04d8700720662cc1293d70ef`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 1.3 MB (1264434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf872018e54c322f4f460c7e7816a9ae61c2a3c07f73d7f4324c18a21f6ccdfb`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:5d074fc96daecf65b6ea7aaaf9d2217f2c8f4e27a44e13800ee34ce2110620a1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2636098719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e88c818aa8954ae57e277c9730cdfa1dceee6b1cc34304b32f23f94a4ee916`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:47:04 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:50:03 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:50:05 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:10:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:10:40 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:10:41 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:11:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:11:16 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a6b8d8a4b8aea18e07888051dac03e88f4132fba08dca72e5795d9533dd3d`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67fec1bfee8619d88a924c4f9b9f4a04d2a0a1d199406157bb073b9f48d588`  
		Last Modified: Wed, 14 Apr 2021 13:07:33 GMT  
		Size: 134.1 MB (134133939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fe57ae793e79818d065737c8e995bb1b73296275794af222be695733711652`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.6 KB (1562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5134c3d8291dc3a52f7fad327cccf50377f2f362488fbcb8405addc74c0eedcf`  
		Last Modified: Wed, 14 Apr 2021 20:25:05 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d60772069c77cb2a80fec9f6e4d18084a4a919d4f776079dfee7903331331e7`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4716fdd15cdffc3b1aa557c81d58c2d0c343f9bfbfb501325b4cdc3bfeb426d9`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc11d2d339a72dd92f86f4fcc8e6fc299da2b6b381147f41dbd8d789e0c944e`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2909c1d8e32571506ce36cda43c7b113b299e280d6d7dfffafe5cd6284595348`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.7 MB (1712288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e56de156a63d8492bf70144c9e28ae975db36a6a57c54e734c96e20fb8bb13`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:436f2a16a677c719d951ddd10a1f475e81cc61b0726c7a4d5f76bdea16e3d215
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5982128974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1658b3cebc6cc5691856945858057a4e3925a991ead9db618b5058d55e445e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:50:19 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:54:08 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:54:10 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:11:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:11:24 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:11:25 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:11:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:12:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:13:01 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1388c10d71d4f1005ced63001aeb1392f019139011ddf961220ee27a412cbadb`  
		Last Modified: Wed, 14 Apr 2021 13:07:44 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913a59644a65d5f7183aa7bebce08c8b09d1f627c257105a7db7514919858b6e`  
		Last Modified: Wed, 14 Apr 2021 13:08:21 GMT  
		Size: 143.9 MB (143889855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b095a33aa8cc59c703b0a8f3b0bb53508123d89c531d6369de947b72b26f5`  
		Last Modified: Wed, 14 Apr 2021 13:07:46 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c7a21f93788806d3510b3cc8f7692b086c096861b42c218993697d04a890de`  
		Last Modified: Wed, 14 Apr 2021 20:25:25 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fbdf3acf4f09ad44474940358b0b044863361fee2bb201478a8b4b40cced75`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600e2fd01e09ce5bb623f7dbf3080c7127a8c2dc0b54422dee1525e75e6ae6de`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d594e3e36caa66775e5660018a80c02ef6bf4b16e626bdbca53a885634db4a29`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f5b24d29c79d20732eaf23dc495c89959ba869fbcb3bb88d35b42f38616a1`  
		Last Modified: Wed, 14 Apr 2021 20:25:24 GMT  
		Size: 7.0 MB (6976405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11b840b2827a9bb3da231a34e716b4fbd570dffa0b711f9fcbb7ff630c90052`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-builder-alpine`

```console
$ docker pull caddy@sha256:388a8615423ce9d162146c4b22c552424c9ef7a58a27c091ae1cb3b3e85e3f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.3.0-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:3eb8fd03c47af4395bea3f6bcb98e8385f4634c7f513e7746421ae828d62c66f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119544759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dab7b132f437ff0879dfdef9940c90324e4d6a4c5af7de0c2b7b256d5ebf21b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:29:08 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:29:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:29:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:32:48 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:34:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:34:19 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:34:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:34:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:34:20 GMT
WORKDIR /go
# Thu, 15 Apr 2021 09:28:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 09:28:59 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 09:29:00 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 09:29:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 09:29:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 09:29:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 09:29:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b54d2d4342f88201f48db57cae1f7edbacae870ee13d7962f999edd7529a9`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5898d3d0f1f95fd666f764bf918c1656be6169868335cb63bc428a5ef47cf32`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2292415af71b71f5b5eae8c7426f41afef6af628b410acf0b9d036240addeeb`  
		Last Modified: Wed, 14 Apr 2021 21:37:07 GMT  
		Size: 106.8 MB (106825070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483424ea5e047556d6172c0273d0671d368d0e42448ee6eee213adf6f0f0e218`  
		Last Modified: Wed, 14 Apr 2021 21:36:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936094b3e444e93dce0400536b066def6153e8795892e63e44042e3507f71fa7`  
		Last Modified: Thu, 15 Apr 2021 09:29:37 GMT  
		Size: 8.3 MB (8326458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41aa4f492f90b4b9472fbfce9bf1b1f4f9dc08fb9d9ec92fb040160716042e0`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 1.3 MB (1311071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9495ef365ef431007d48d2a011656481c0dcfe85888f9dc8d8780a41db96f26`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ca579a39dbe79f52268fdb5230c9a5ad7cfc115e540b515ecce7a557714b1711
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114723671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf78bfe4d146d0c0b28698b45888f4e663125f52bfb222cd1e7bf6e85248038`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:19:47 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:19:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:19:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:24 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:11:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:12:16 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:12:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:13:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:13:32 GMT
WORKDIR /go
# Thu, 15 Apr 2021 06:25:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 06:25:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 06:25:12 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 06:25:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 06:25:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 06:25:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 06:25:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c231c184d802a569805e44837dd1ea2cb0522bb03ca5763ef5ed9fae5896c`  
		Last Modified: Wed, 14 Apr 2021 21:15:05 GMT  
		Size: 281.0 KB (280982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8ca9e585b85be2e7ddaaf213e22bdb986eba4da2a8cc4d8b45f762752e17df`  
		Last Modified: Wed, 14 Apr 2021 21:15:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa237e1852b6dc6312c54835af4eedd49fc347da91eee2bd9a5cbdf3e4a09a74`  
		Last Modified: Wed, 14 Apr 2021 21:17:14 GMT  
		Size: 102.7 MB (102671404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfaf15ab73c5bd3fd51cf3ad7a986d94a84a0de33b0e2b421df3ece40813b6f`  
		Last Modified: Wed, 14 Apr 2021 21:16:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bceb981e039ba8e3426115768baf63e8372fc75250fbb6d6df522d9558b8abb8`  
		Last Modified: Thu, 15 Apr 2021 06:26:15 GMT  
		Size: 7.9 MB (7943726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec602f7edc3131a49dd0ab8bd4e7b207009dc592d13555e12296c433ef56919`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 1.2 MB (1221591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57d036d826077e94afba969b41b7bdc9d1ae0f266d04bc343350ff391e2fd75`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:28ae48497c0b64592d20b21b122fe14268d4ce85a5e9ea9b5b583d5a58726cfb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113527342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15cf44fde7fa3b279efe2039c6fb0882edb4c49fdc0076fc26c90bdcec1b365`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:28:16 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:28:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:28:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:19:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 22:43:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 22:43:26 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 22:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:43:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 22:43:36 GMT
WORKDIR /go
# Thu, 15 Apr 2021 07:39:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 07:39:41 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 07:39:43 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 07:39:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 07:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 07:39:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 07:39:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a884c3a8500725e0f08f924091ec61ae3e3acee3b0ffe5839b06f874ee63dc08`  
		Last Modified: Wed, 14 Apr 2021 22:45:08 GMT  
		Size: 280.1 KB (280078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f87f08a98de1e7cb636267b626d4e644775ff7962ea1ff9b4813f740b89e67`  
		Last Modified: Wed, 14 Apr 2021 22:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c59f8b5aa025c1cb85f375b22cbc86c2892e311a5aad724e9af892abbefca31`  
		Last Modified: Wed, 14 Apr 2021 22:47:06 GMT  
		Size: 102.5 MB (102463090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146d2365c5f44423fcd2cd482e0d74d784c72e892e81c7d26dd1aa1a8bd3ab43`  
		Last Modified: Wed, 14 Apr 2021 22:46:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689b9c2e77675507509d87b28e5aa533b980296e5ffa8999fa8268863b5691b5`  
		Last Modified: Thu, 15 Apr 2021 07:40:47 GMT  
		Size: 7.2 MB (7154833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c64d502102e5ce2b6b103a14d9af56e06fa146e4eb76cf6423e58e5407b6475`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 1.2 MB (1219446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a490f0c5cdae283a0f25e3bc46079442ea559abaa3cf16c64a5a0cef30befc45`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b89b93e92ffd9427041b5ed8850cc44f292b611e7dee55242ea02c6c3ccf2a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8d157b29403fa75da94e9701e2c3e3d065de48b910f8045b32619bdc25f1e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:09 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:46:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:46:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:54:59 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:58:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:58:21 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:58:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:58:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:58:41 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:44:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:44:05 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:44:06 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:44:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:44:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:44:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:44:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2150ab4b89a5dc832780f442998074db1582348dca0eb60d6b79b59df025f25f`  
		Last Modified: Wed, 14 Apr 2021 21:00:21 GMT  
		Size: 281.2 KB (281220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9d22c0ca7447b1a1b25889675e84f2ed68ecd519fdc513796712138820633b`  
		Last Modified: Wed, 14 Apr 2021 21:00:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cfb7326a4720568ee9867ad9f6dd4b796bcd9e899c6a27a3891589eae5cc06`  
		Last Modified: Wed, 14 Apr 2021 21:02:14 GMT  
		Size: 102.1 MB (102136232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a0cdf5ccbda3f4358749dfd4a03c520b2ca135a303988e74a5796796ccc30d`  
		Last Modified: Wed, 14 Apr 2021 21:01:48 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad8e65604482fa70f402e9fde824dec1ff3f257637f247fe6279c69757b9de6`  
		Last Modified: Thu, 15 Apr 2021 08:45:09 GMT  
		Size: 8.5 MB (8518404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1496bb71598cd42c2f92595b24f0aa7a34914fb6048c11499146f728964ddb`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 1.2 MB (1201555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1678712b911f6bb0ed8a67b615034fcec04e64bca853d43c39e3659d54e649`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4d7764de3f8d29cbb22b2b973802bbf36aa89b6c1e6a11cf6934b2273b80e59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113988669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c777710e48b168e93b792b4171e667a5c16209c668b09dd54d442ad4ef1c55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 31 Mar 2021 18:56:11 GMT
ADD file:d51af61c5955c980d18387ab532110c3874f95a87768be84dfd1eeb3e701d3a4 in / 
# Wed, 31 Mar 2021 18:56:16 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 04:33:46 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 01 Apr 2021 04:33:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 04:33:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:18:36 GMT
ENV GOLANG_VERSION=1.15.11
# Fri, 02 Apr 2021 03:20:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 02 Apr 2021 03:20:38 GMT
ENV GOPATH=/go
# Fri, 02 Apr 2021 03:20:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:20:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 02 Apr 2021 03:21:02 GMT
WORKDIR /go
# Fri, 02 Apr 2021 05:03:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 02 Apr 2021 05:03:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Fri, 02 Apr 2021 05:03:15 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 02 Apr 2021 05:03:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 02 Apr 2021 05:03:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 02 Apr 2021 05:03:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 02 Apr 2021 05:03:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6d4557865d9cec3513c1a5e744cb1073a563d464b8d546911289b9df9998f1b`  
		Last Modified: Wed, 31 Mar 2021 18:57:36 GMT  
		Size: 2.8 MB (2806070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128ce9f93b1dd5f42d7663646400f1307cddfad6a5361031e3a1ca8c46d90d2e`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 283.2 KB (283224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb52babc5b3ae7ccfca63bfc4092e7d57cbd51bc203af266e4fcb0169a6107`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91ebeddf57ad09e8e1b3eb1e312be6a4484d88f8f970a7b241d759abe98e5f`  
		Last Modified: Fri, 02 Apr 2021 03:25:31 GMT  
		Size: 100.8 MB (100806744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac05f37b09f2517038025dd2d905a5d3ecbd9af697023fe05bc857ed48b8f455`  
		Last Modified: Fri, 02 Apr 2021 03:25:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e2e6a908474ce0f09d3cc2e30293784024f2a821c330690e753b01155c5346`  
		Last Modified: Fri, 02 Apr 2021 05:04:26 GMT  
		Size: 8.9 MB (8921423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b888e7962a16510b476660b91df0be664af7f16e7eb94288112b51bfd206995`  
		Last Modified: Fri, 02 Apr 2021 05:04:25 GMT  
		Size: 1.2 MB (1170492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ce4e5965570ab285f5e3be6ab2ca4cd6b618b344303a3e09cbb4c46fb2393f`  
		Last Modified: Fri, 02 Apr 2021 05:04:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:75a9876d6656c0b08c814240a013160e20a41c6a4bfe5939f9befb45ab7e277c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118429233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3dc1b085458cb773f526584cf4e59ebff486ad9b1f684021e37907fd83cb1d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:59 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:47:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:47:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:51:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:51:52 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:51:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:51:53 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:47:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:47:02 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:47:03 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:47:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:47:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:47:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:47:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c45d0e43ef7a36e47dfc16916a076f7ba26b656842380c26207ad30f5c8b`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 281.3 KB (281343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f1645d6cbfccd2924337f37dc819e7edc27989ead8bc679441954a0e483c24`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3233df950b4b58e213bfc323437185867d0d54de06ac41e9e5c408ca83ecd5ca`  
		Last Modified: Wed, 14 Apr 2021 20:53:56 GMT  
		Size: 105.9 MB (105944122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3995327d2f868035d65ecb6b315f8595f43db3da3e10b19dbe964a66b6cfd746`  
		Last Modified: Wed, 14 Apr 2021 20:53:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04afa35fe1fde3bf4e11163aeea0b3f7c6084de121d5f071291ee325ac535f06`  
		Last Modified: Thu, 15 Apr 2021 08:47:53 GMT  
		Size: 8.4 MB (8370192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81b8ec43677381485cbedd3fa6dc24863c5d8f04d8700720662cc1293d70ef`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 1.3 MB (1264434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf872018e54c322f4f460c7e7816a9ae61c2a3c07f73d7f4324c18a21f6ccdfb`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:0ee0dd2e13c7c2d8b1a3514be4c8a71a5da92f756386f549bdd51c0bd62700c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2.3.0-builder-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:5d074fc96daecf65b6ea7aaaf9d2217f2c8f4e27a44e13800ee34ce2110620a1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2636098719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e88c818aa8954ae57e277c9730cdfa1dceee6b1cc34304b32f23f94a4ee916`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:47:04 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:50:03 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:50:05 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:10:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:10:40 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:10:41 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:11:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:11:16 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a6b8d8a4b8aea18e07888051dac03e88f4132fba08dca72e5795d9533dd3d`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67fec1bfee8619d88a924c4f9b9f4a04d2a0a1d199406157bb073b9f48d588`  
		Last Modified: Wed, 14 Apr 2021 13:07:33 GMT  
		Size: 134.1 MB (134133939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fe57ae793e79818d065737c8e995bb1b73296275794af222be695733711652`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.6 KB (1562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5134c3d8291dc3a52f7fad327cccf50377f2f362488fbcb8405addc74c0eedcf`  
		Last Modified: Wed, 14 Apr 2021 20:25:05 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d60772069c77cb2a80fec9f6e4d18084a4a919d4f776079dfee7903331331e7`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4716fdd15cdffc3b1aa557c81d58c2d0c343f9bfbfb501325b4cdc3bfeb426d9`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc11d2d339a72dd92f86f4fcc8e6fc299da2b6b381147f41dbd8d789e0c944e`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2909c1d8e32571506ce36cda43c7b113b299e280d6d7dfffafe5cd6284595348`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.7 MB (1712288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e56de156a63d8492bf70144c9e28ae975db36a6a57c54e734c96e20fb8bb13`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:80d881fa828e30f1c7d44ae2d3bebe98ef9185d4e43e597ac5205ba32ad13c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.3.0-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:436f2a16a677c719d951ddd10a1f475e81cc61b0726c7a4d5f76bdea16e3d215
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5982128974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1658b3cebc6cc5691856945858057a4e3925a991ead9db618b5058d55e445e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:50:19 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:54:08 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:54:10 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:11:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:11:24 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:11:25 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:11:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:12:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:13:01 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1388c10d71d4f1005ced63001aeb1392f019139011ddf961220ee27a412cbadb`  
		Last Modified: Wed, 14 Apr 2021 13:07:44 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913a59644a65d5f7183aa7bebce08c8b09d1f627c257105a7db7514919858b6e`  
		Last Modified: Wed, 14 Apr 2021 13:08:21 GMT  
		Size: 143.9 MB (143889855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b095a33aa8cc59c703b0a8f3b0bb53508123d89c531d6369de947b72b26f5`  
		Last Modified: Wed, 14 Apr 2021 13:07:46 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c7a21f93788806d3510b3cc8f7692b086c096861b42c218993697d04a890de`  
		Last Modified: Wed, 14 Apr 2021 20:25:25 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fbdf3acf4f09ad44474940358b0b044863361fee2bb201478a8b4b40cced75`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600e2fd01e09ce5bb623f7dbf3080c7127a8c2dc0b54422dee1525e75e6ae6de`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d594e3e36caa66775e5660018a80c02ef6bf4b16e626bdbca53a885634db4a29`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f5b24d29c79d20732eaf23dc495c89959ba869fbcb3bb88d35b42f38616a1`  
		Last Modified: Wed, 14 Apr 2021 20:25:24 GMT  
		Size: 7.0 MB (6976405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11b840b2827a9bb3da231a34e716b4fbd570dffa0b711f9fcbb7ff630c90052`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-windowsservercore`

```console
$ docker pull caddy@sha256:6a199f80cee0da0b39f4deffc53efac536c60672f4d8d26887f8f8ec194da3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.3.0-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-windowsservercore-1809`

```console
$ docker pull caddy@sha256:89f75ffc06d5f7a7cc6d37f38c9198d869993fa7426542d14c1a8bfdbb467694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2.3.0-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:a42a67f914fd976a839e8c725f15fec79415b331ffeaa3972e7bff363bec4ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.3.0-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-beta.2`

```console
$ docker pull caddy@sha256:d8fabc6268aa54ca4fcf66c4e08fe092e9f3d7c5b9dafea4dff860d6ccae9d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.4.0-beta.2` - linux; amd64

```console
$ docker pull caddy@sha256:008590d156dcc7a1533fd34be8e2e452454e27e49ffa533e083c2cdc87292137
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14525666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e49e451428790254800f544ebb051811973a83c34de9eaf1147f7df2914119e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:11:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:11:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 20:11:07 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:11:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:11:10 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:11:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:11:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:11:11 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:11:11 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:11:11 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:11:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:11:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:11:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:11:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:11:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:11:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:11:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:11:13 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:11:13 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:11:13 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:11:13 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:11:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8294633c5b5606f8e98aaf81da701b7a7e2018dbf82355d1d73830c677034f19`  
		Last Modified: Wed, 14 Apr 2021 20:12:08 GMT  
		Size: 300.4 KB (300403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f815e2ab15b24629c79357f527072ba057b7da6a993f0c1d5e36ad122667869f`  
		Last Modified: Wed, 14 Apr 2021 20:12:08 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866e77b5ab7364d6fd10d9aac10241c645d81761011f2544041e03e42d694266`  
		Last Modified: Wed, 14 Apr 2021 20:12:11 GMT  
		Size: 11.4 MB (11407308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93ab174db6c235a141fac119c490f18169f74691e5a11eab453949b232584d5`  
		Last Modified: Wed, 14 Apr 2021 20:12:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:97c65847ce7dedfc97f2a8c45a23e4b98500dbaf64ff859470f3dec89051f96d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13740478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86bf0a2b49de4347cab1ee9820ae0679841542148383a0768a5c937063a6acc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:46:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:46:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 19:46:46 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:47:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:47:01 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:47:02 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:47:02 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:47:03 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:47:04 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:47:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:47:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:47:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:47:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:47:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:47:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:47:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:47:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:47:16 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:47:16 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:47:17 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:47:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf1089ae45174c5bef4f470e0e4c2337f99090005f19e104781d0b048ea9c3b`  
		Last Modified: Wed, 14 Apr 2021 19:48:05 GMT  
		Size: 300.5 KB (300511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57bfdaecc4b43b7518a479f577a5afb7ef6539918e03b27d7cb7865dda8ceaa`  
		Last Modified: Wed, 14 Apr 2021 19:48:05 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb354d82c5c45ab0a1d4b541ed0368301bb0aa5d98d569dcca44ba52af1c82ac`  
		Last Modified: Wed, 14 Apr 2021 19:48:11 GMT  
		Size: 10.8 MB (10811849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4825a384a1336a9aa743168ca8598059188ff162e307fd919af7d232553d8d00`  
		Last Modified: Wed, 14 Apr 2021 19:48:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cb08eec441907897f1f1d5b49e9fc1c25520f50e4ea6b102d9cac96611357924
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13522050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdd47f39bf49de697e4c8c9a7e7a120b0e177759e932df849a7f529c8c7c52c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:40:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:40:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 19:40:21 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:40:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:40:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:40:31 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:40:33 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:40:35 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:40:37 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:40:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:40:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:40:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:40:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:40:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:40:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:40:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:40:45 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:40:46 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:40:47 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:40:48 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f77b739097bd5400613d0daa0adde01d99993ce236a374da6748f11f866bf0`  
		Last Modified: Wed, 14 Apr 2021 19:41:38 GMT  
		Size: 299.7 KB (299662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9788d846329505d64f04c5f1dbd3f0d27d905fb498de7c5c456f5823672b6cff`  
		Last Modified: Wed, 14 Apr 2021 19:41:38 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c35ff970ff73407531ea1f8a1f74a02a827115108af34bd60e0be6c45682a`  
		Last Modified: Wed, 14 Apr 2021 19:41:47 GMT  
		Size: 10.8 MB (10792259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f4cac5d7458d5bd60076049902c4aaf4870551a9ba90d095db1e318e8c6de3`  
		Last Modified: Wed, 14 Apr 2021 19:41:38 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2c68dbeaf7a3f456fe421515303f93f454a7820d503b6b82fee461af7b34a021
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13377789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18721977bc17f197109ce747bc0fc1c903a3e89501c6f6688f2f0e431f377f4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:00:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:00:51 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 19:00:52 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:00:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:01:01 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:01:02 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:01:03 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:01:04 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:01:05 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:01:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:01:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:01:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:01:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:01:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:01:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:01:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:01:13 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:01:14 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:01:15 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:01:16 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:01:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0e0200fa31a158cd37e4584ab7ca30d0663376cf38fe7f1b73ff5a9a59fa12`  
		Last Modified: Wed, 14 Apr 2021 19:02:06 GMT  
		Size: 300.6 KB (300628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ccfceaf045f4ee335a1bc18b6d9b5b810f094e112b8fdba1dd77d677a57026`  
		Last Modified: Wed, 14 Apr 2021 19:02:05 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3652a605ae4ee9ac842d52983544d646423afede33486d85a0d108f543ed73eb`  
		Last Modified: Wed, 14 Apr 2021 19:02:10 GMT  
		Size: 10.4 MB (10359155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f12e452573275d900e63abb280e460ed32ebf196b42ece0bbb9b3426866644`  
		Last Modified: Wed, 14 Apr 2021 19:02:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2` - linux; ppc64le

```console
$ docker pull caddy@sha256:3604464281aef38cf182199e6e9d487be73d952aa9293cc27bcd3c47f3a5e08e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13079793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e6e9d8437131af51b8524a58ca3de724aba1064d7220e22fdfb31fba739983`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:12:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 22:12:32 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 22:12:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:13:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:13:08 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:13:12 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:13:34 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:13:49 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:13:57 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 22:14:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:14:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:14:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:14:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:14:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:14:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:14:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:14:49 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:14:55 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:15:00 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:15:06 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:15:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25908330df11bb7bc2ed71aa9b4de279db5492df2b03ced3f6650b25821c4584`  
		Last Modified: Wed, 14 Apr 2021 22:16:00 GMT  
		Size: 302.6 KB (302554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db38e9079ac39fb587a66fb19194d3b826ebb61f448eec8d7d1881c57d743ee`  
		Last Modified: Wed, 14 Apr 2021 22:16:00 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb3d6ca707ceaa50eb1f2531e22cf89a6048b70374e81f0380914881e0fd229`  
		Last Modified: Wed, 14 Apr 2021 22:16:02 GMT  
		Size: 10.0 MB (9958115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d38adbdd5557c52260b3374adc032cf15b098ae41cdb2c58a8ed4afb6cb9da`  
		Last Modified: Wed, 14 Apr 2021 22:15:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2` - linux; s390x

```console
$ docker pull caddy@sha256:7236cb39ac16745ad402c814cc38fe206ee611029901ef34ddf5bbc38cc3b4dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13897385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92516f58ee45d35db423aab69a6495fd9ec244bd0b00af83ca97d262ff6e9892`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:40 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:07:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 20:07:42 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:07:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:07:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:07:46 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:07:46 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:07:46 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:07:46 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:07:46 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:07:47 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:07:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:07:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:07:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:07:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:07:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:07:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:07:48 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:07:48 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:07:49 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:07:49 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:07:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db3c8b812fcb0d1bfd42c16c2e9ac68f4f3006382c5362e969d1c9eb3a9fab5`  
		Last Modified: Wed, 14 Apr 2021 20:08:26 GMT  
		Size: 300.8 KB (300847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89655d5853714574393844228f501cd2caed22a1af84d0b24b3f3614aa4177d5`  
		Last Modified: Wed, 14 Apr 2021 20:08:26 GMT  
		Size: 5.8 KB (5823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d56d7197473fe4c06e215810298ce281307fc5f2bc659b633f400198ada755`  
		Last Modified: Wed, 14 Apr 2021 20:08:28 GMT  
		Size: 11.0 MB (10987911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe6ca41447c64f973dcf67a370126053ec58952f1e3381e3e97b642a320270b`  
		Last Modified: Wed, 14 Apr 2021 20:08:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:57007a2384bbff9e730072565519dbdb596e6eb66e59969ba33cc31b8a5cea77
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487035062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21166c4140d929d0caccfb9e9ff5b3af4641c7594112345c1d3d87a5bf7f52ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:13:54 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:13:55 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:14:32 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9f41c88fc8c2c28230c5eb67fb7d9ef23477a351fb716a44486b3d1a37569fb141112cd3582adcd44424b2819c22723fb49023a6d371e1bf8d92eefe4e7e9ed4')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:14:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:14:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:14:35 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:14:36 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:14:37 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:14:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:14:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:14:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:14:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:14:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:14:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:14:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:14:45 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:14:46 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:14:47 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:15:12 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:15:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de472ba1df2f836f9b4125180bedb0ca0f6c425460dd8535a92764dff8169f8`  
		Last Modified: Wed, 14 Apr 2021 20:25:56 GMT  
		Size: 5.1 MB (5080859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55627e36839779d3cfb370ec41774f50d7db4ff914a3077c70b75f96287e5af0`  
		Last Modified: Wed, 14 Apr 2021 20:25:52 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f2e16d47aeed21efafcfe34553edd6166984a4ae765a5420a50d46f1d204b6`  
		Last Modified: Wed, 14 Apr 2021 20:25:56 GMT  
		Size: 11.9 MB (11867562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c501d3d5d88099b96f7b95b3f58cdc7baea8006662464c5677f3d8abbad2`  
		Last Modified: Wed, 14 Apr 2021 20:25:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee81a85c97e2bebd04246c72c2e9093a2fc92d5b3a1c61092a47ca2dbca3195`  
		Last Modified: Wed, 14 Apr 2021 20:25:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c473eb70ede949ae95779d72ada5e737f68bee537a5892368b21c219b7ae8f2`  
		Last Modified: Wed, 14 Apr 2021 20:25:51 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962e4b4d5583a800a5fa99d1c9f8344405685fc162718cfab1c851df0b149bf4`  
		Last Modified: Wed, 14 Apr 2021 20:25:50 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4277207668aa329a0fcf285a3e8044549f14fcdc258b54941786b2dbac2b738f`  
		Last Modified: Wed, 14 Apr 2021 20:25:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8932075115714c24da0e0b15ca784e45621efdac23f763feac93a8d63e51dc18`  
		Last Modified: Wed, 14 Apr 2021 20:25:49 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ec24942a02e14cc4f3627742e1a9ba37a831854d99e25e35ab78c7603f4cbd`  
		Last Modified: Wed, 14 Apr 2021 20:25:49 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554d5e240ec502a081852a31141622d738e021388206ba4f43cb159c7c7d7a5`  
		Last Modified: Wed, 14 Apr 2021 20:25:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6d8e32fb60c802dc23aa51a0c38e0588aebbf5461bd4d3b66de34e80d2eb6`  
		Last Modified: Wed, 14 Apr 2021 20:25:47 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339de9553d5fd226cedff68f9c92d817957f2f7809f9d64da67f12fb23bed32`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51272577d8785b827aa7bb896767009a940ee9343189459c6e3c675e566f9f0d`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde8de3cc19d01e8b1d8624b50438d1fa257a16237f41b1d73cff4fa65768a4d`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455f5cdc11de43d196e81d074362a41abcaed1366315581b689ba2a88d3f4857`  
		Last Modified: Wed, 14 Apr 2021 20:25:44 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d7b5d207b9968f7f40e32437e99ef85d2dde4afba849a8825896ee82ed5f50`  
		Last Modified: Wed, 14 Apr 2021 20:25:43 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9dc90818d729c2fd0cb0bac96912bd2969512c4a029b3a3b21b3764b004500`  
		Last Modified: Wed, 14 Apr 2021 20:25:44 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d304d34d98bbc8fed2a3f472757c6377c204ec57a87fd6a3823cf4236f26e877`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 308.5 KB (308506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701310ad80f85832364aa3313c02e66c8a9e60cd165a937c96075db0496b486c`  
		Last Modified: Wed, 14 Apr 2021 20:25:43 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:fa30c18bcdf91806b54ea7ed3a348627df09108ceebc6d0d5550fb0ad3455cde
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5817979261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421de0d93291fba46ed24305b5fe5fe3f674bd381400d00c5bf45a608e170018`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:16:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:16:51 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:18:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9f41c88fc8c2c28230c5eb67fb7d9ef23477a351fb716a44486b3d1a37569fb141112cd3582adcd44424b2819c22723fb49023a6d371e1bf8d92eefe4e7e9ed4')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:18:40 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:18:41 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:18:42 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:18:43 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:18:45 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:18:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:18:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:18:48 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:18:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:18:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:18:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:18:53 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:18:54 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:18:55 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:20:11 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:20:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b068c1eb113cc4e93590b9ea7cd57796316b3b21ba390abfe889d79e702cec3c`  
		Last Modified: Wed, 14 Apr 2021 20:26:14 GMT  
		Size: 5.7 MB (5660433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d97864bd63ccf6806c9e9849c61e19f7a4b476e59b63ac9d243241fdd271e3d`  
		Last Modified: Wed, 14 Apr 2021 20:26:12 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab97c72d1ce9fea13fa1e516f83d28adc8a155bfa23822ce7752d2da4f74c5b`  
		Last Modified: Wed, 14 Apr 2021 20:26:17 GMT  
		Size: 17.2 MB (17151549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8acb6e1c103fe19721c692609bc6eb55acdd0326bb9d027768a6ba92e7e0202`  
		Last Modified: Wed, 14 Apr 2021 20:26:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cdd68811b5c180d1153a0f2b6d8edceb94aad8069b64040d2d8db829dd448e`  
		Last Modified: Wed, 14 Apr 2021 20:26:11 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab6a4bef16e77771e00038b7a77d618e3fc0da8ef554e67d5a8c4e0400f1809`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558d80b23de2d6fb99e705591d268689266afd67afef1012302baf76d43c6a0c`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6382ddb421f9b6ed0c2a785186cf291be684523ec1ddc96d4cfe2963b4f37b79`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991b64532293d0a7f622cce85a5709f33577f5803fda5d8838a8cc850532054c`  
		Last Modified: Wed, 14 Apr 2021 20:26:08 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bf3364ee0158cad4826de8a57245fcb5a54a4f33f0d07fa1867d70b482812d`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4572b72928444624d70624bd4188a957e1cbcdc364bacd3026fc6e46d2154e72`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fae1b86448ffecd80365e375393080c5484925ed877f02fcc8f9bd3389c725c`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae7cbf677188f13aae6856b110af11696cac21e78313f3d225815d7fb16b55b`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e925b48c88da00efc465f3291af0f81734fa9088838bf99e2b21c9763c76aa80`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325a0551f6981da1e92d3974f95db9dbc5553b1acd629302ab8f2ed5aaf64a41`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fbbe5b0ac1c5adbe504a0bded280a2ebc8133939e17035cdf61e5f811a9d79`  
		Last Modified: Wed, 14 Apr 2021 20:26:03 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7999335cd30f75fd39b8d9ebfaac1dfad63e643813eeabfd572210dc15f442`  
		Last Modified: Wed, 14 Apr 2021 20:26:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f9edc21a0f3503cc8695bfb1f0f2bf825fe586c31c14112ebaffc2cccb32be`  
		Last Modified: Wed, 14 Apr 2021 20:26:04 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654c270965f7a90556b3aa0fa48d1fea0ff65f6918708e24ebd83c36be1e0ae9`  
		Last Modified: Wed, 14 Apr 2021 20:26:04 GMT  
		Size: 258.0 KB (257960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893d5403793a417c0e1beac002e47a4e1d311d6aca319395cd9422949b7d393c`  
		Last Modified: Wed, 14 Apr 2021 20:26:03 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-beta.2-alpine`

```console
$ docker pull caddy@sha256:0455b5b7afa12030489e596f302430886c669d365ab904971421f74b8a5eba92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.4.0-beta.2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:008590d156dcc7a1533fd34be8e2e452454e27e49ffa533e083c2cdc87292137
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14525666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e49e451428790254800f544ebb051811973a83c34de9eaf1147f7df2914119e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:11:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:11:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 20:11:07 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:11:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:11:10 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:11:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:11:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:11:11 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:11:11 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:11:11 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:11:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:11:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:11:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:11:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:11:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:11:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:11:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:11:13 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:11:13 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:11:13 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:11:13 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:11:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8294633c5b5606f8e98aaf81da701b7a7e2018dbf82355d1d73830c677034f19`  
		Last Modified: Wed, 14 Apr 2021 20:12:08 GMT  
		Size: 300.4 KB (300403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f815e2ab15b24629c79357f527072ba057b7da6a993f0c1d5e36ad122667869f`  
		Last Modified: Wed, 14 Apr 2021 20:12:08 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866e77b5ab7364d6fd10d9aac10241c645d81761011f2544041e03e42d694266`  
		Last Modified: Wed, 14 Apr 2021 20:12:11 GMT  
		Size: 11.4 MB (11407308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93ab174db6c235a141fac119c490f18169f74691e5a11eab453949b232584d5`  
		Last Modified: Wed, 14 Apr 2021 20:12:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:97c65847ce7dedfc97f2a8c45a23e4b98500dbaf64ff859470f3dec89051f96d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13740478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86bf0a2b49de4347cab1ee9820ae0679841542148383a0768a5c937063a6acc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:46:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:46:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 19:46:46 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:47:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:47:01 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:47:02 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:47:02 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:47:03 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:47:04 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:47:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:47:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:47:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:47:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:47:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:47:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:47:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:47:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:47:16 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:47:16 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:47:17 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:47:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf1089ae45174c5bef4f470e0e4c2337f99090005f19e104781d0b048ea9c3b`  
		Last Modified: Wed, 14 Apr 2021 19:48:05 GMT  
		Size: 300.5 KB (300511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57bfdaecc4b43b7518a479f577a5afb7ef6539918e03b27d7cb7865dda8ceaa`  
		Last Modified: Wed, 14 Apr 2021 19:48:05 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb354d82c5c45ab0a1d4b541ed0368301bb0aa5d98d569dcca44ba52af1c82ac`  
		Last Modified: Wed, 14 Apr 2021 19:48:11 GMT  
		Size: 10.8 MB (10811849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4825a384a1336a9aa743168ca8598059188ff162e307fd919af7d232553d8d00`  
		Last Modified: Wed, 14 Apr 2021 19:48:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cb08eec441907897f1f1d5b49e9fc1c25520f50e4ea6b102d9cac96611357924
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13522050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdd47f39bf49de697e4c8c9a7e7a120b0e177759e932df849a7f529c8c7c52c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:40:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:40:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 19:40:21 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:40:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:40:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:40:31 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:40:33 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:40:35 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:40:37 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:40:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:40:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:40:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:40:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:40:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:40:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:40:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:40:45 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:40:46 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:40:47 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:40:48 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f77b739097bd5400613d0daa0adde01d99993ce236a374da6748f11f866bf0`  
		Last Modified: Wed, 14 Apr 2021 19:41:38 GMT  
		Size: 299.7 KB (299662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9788d846329505d64f04c5f1dbd3f0d27d905fb498de7c5c456f5823672b6cff`  
		Last Modified: Wed, 14 Apr 2021 19:41:38 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c35ff970ff73407531ea1f8a1f74a02a827115108af34bd60e0be6c45682a`  
		Last Modified: Wed, 14 Apr 2021 19:41:47 GMT  
		Size: 10.8 MB (10792259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f4cac5d7458d5bd60076049902c4aaf4870551a9ba90d095db1e318e8c6de3`  
		Last Modified: Wed, 14 Apr 2021 19:41:38 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2c68dbeaf7a3f456fe421515303f93f454a7820d503b6b82fee461af7b34a021
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13377789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18721977bc17f197109ce747bc0fc1c903a3e89501c6f6688f2f0e431f377f4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:00:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:00:51 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 19:00:52 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:00:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:01:01 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:01:02 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:01:03 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:01:04 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:01:05 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 19:01:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:01:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:01:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:01:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:01:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:01:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:01:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:01:13 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:01:14 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:01:15 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:01:16 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:01:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0e0200fa31a158cd37e4584ab7ca30d0663376cf38fe7f1b73ff5a9a59fa12`  
		Last Modified: Wed, 14 Apr 2021 19:02:06 GMT  
		Size: 300.6 KB (300628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ccfceaf045f4ee335a1bc18b6d9b5b810f094e112b8fdba1dd77d677a57026`  
		Last Modified: Wed, 14 Apr 2021 19:02:05 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3652a605ae4ee9ac842d52983544d646423afede33486d85a0d108f543ed73eb`  
		Last Modified: Wed, 14 Apr 2021 19:02:10 GMT  
		Size: 10.4 MB (10359155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f12e452573275d900e63abb280e460ed32ebf196b42ece0bbb9b3426866644`  
		Last Modified: Wed, 14 Apr 2021 19:02:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3604464281aef38cf182199e6e9d487be73d952aa9293cc27bcd3c47f3a5e08e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13079793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e6e9d8437131af51b8524a58ca3de724aba1064d7220e22fdfb31fba739983`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:12:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 22:12:32 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 22:12:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:13:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:13:08 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:13:12 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:13:34 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:13:49 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:13:57 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 22:14:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:14:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:14:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:14:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:14:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:14:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:14:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:14:49 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:14:55 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:15:00 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:15:06 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:15:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25908330df11bb7bc2ed71aa9b4de279db5492df2b03ced3f6650b25821c4584`  
		Last Modified: Wed, 14 Apr 2021 22:16:00 GMT  
		Size: 302.6 KB (302554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db38e9079ac39fb587a66fb19194d3b826ebb61f448eec8d7d1881c57d743ee`  
		Last Modified: Wed, 14 Apr 2021 22:16:00 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb3d6ca707ceaa50eb1f2531e22cf89a6048b70374e81f0380914881e0fd229`  
		Last Modified: Wed, 14 Apr 2021 22:16:02 GMT  
		Size: 10.0 MB (9958115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d38adbdd5557c52260b3374adc032cf15b098ae41cdb2c58a8ed4afb6cb9da`  
		Last Modified: Wed, 14 Apr 2021 22:15:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7236cb39ac16745ad402c814cc38fe206ee611029901ef34ddf5bbc38cc3b4dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13897385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92516f58ee45d35db423aab69a6495fd9ec244bd0b00af83ca97d262ff6e9892`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:40 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:07:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"
# Wed, 14 Apr 2021 20:07:42 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:07:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41daeac683d503264496689c6271645293c95518c5b97870c3f3a17127ae35b820622720315901c0c5856b42e0201b7eaad153dfa4a1045502a99f41d0b9785d' ;; 		armhf)   binArch='armv6'; checksum='51e4d7220064e1948232c8c54996b012d01fe0e2caa71200e34f0da59bd6267cdc318124e1a7a44e83ce54b7276f6d0fb32381d3080e05902d3c3528ff423dd7' ;; 		armv7)   binArch='armv7'; checksum='9c3b4eea4840a1fe633d45d436789edf6839e96527783d2eac309d24e5085c0cdee8beffd7e5ad2f1d7d31e16004e916aa29456d8ac52007e9d904e644d6db40' ;; 		aarch64) binArch='arm64'; checksum='86cf83d11aee266d32c262982df3e286aa0a4b391fc4fbded0e299ace043c753e9a1f53bef1f95a292a71107e1f9578a8615b038871eedb171437eebe7db47d2' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='81b050dae2892feb517db6c782acc506dfe21399b0a79073e5191656f57c6d0a5a511caf1086ffc671712ab198715cca6a2a120812a4df8d774ba17d6242aa39' ;; 		s390x)   binArch='s390x'; checksum='763256d267ad8832c37fa1a902fc06dfb6b9871b75e38545cbc199b50251f78b0cc2400104d31fc18d2c98408f02a74e581a7f7746974837dcdef51a4a259bf2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:07:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:07:46 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:07:46 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:07:46 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:07:46 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:07:46 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:07:47 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:07:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:07:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:07:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:07:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:07:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:07:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:07:48 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:07:48 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:07:49 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:07:49 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:07:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db3c8b812fcb0d1bfd42c16c2e9ac68f4f3006382c5362e969d1c9eb3a9fab5`  
		Last Modified: Wed, 14 Apr 2021 20:08:26 GMT  
		Size: 300.8 KB (300847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89655d5853714574393844228f501cd2caed22a1af84d0b24b3f3614aa4177d5`  
		Last Modified: Wed, 14 Apr 2021 20:08:26 GMT  
		Size: 5.8 KB (5823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d56d7197473fe4c06e215810298ce281307fc5f2bc659b633f400198ada755`  
		Last Modified: Wed, 14 Apr 2021 20:08:28 GMT  
		Size: 11.0 MB (10987911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe6ca41447c64f973dcf67a370126053ec58952f1e3381e3e97b642a320270b`  
		Last Modified: Wed, 14 Apr 2021 20:08:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-beta.2-builder`

```console
$ docker pull caddy@sha256:5c4e73181b18428f694cbb5a01974ec92ec456b7f3bcf8b66d92ab1fdab33318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.4.0-beta.2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:95cacd60ef1d3a7e72d1e72264e6cb97bc62c9020e8134e1906e00e4b52f3dbd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116498360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6a619fa9afac38b043bea122011879afe8113808b2dbf088bd347f4a70a5df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:27:12 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:27:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:27:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:27:13 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 21:28:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:28:50 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:28:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:28:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:28:51 GMT
WORKDIR /go
# Thu, 15 Apr 2021 09:29:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 09:29:10 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 09:29:10 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Thu, 15 Apr 2021 09:29:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 09:29:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 09:29:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 09:29:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc1eea9eeabb6de296adb3e0c1b0722cf13251ff3e4e2d0a5f7ed8e3d48342`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 281.3 KB (281269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab2625f07be8d5c6e48046a05ff3ecc7f374b794a926fb62247b66b511909`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806e9ddb8669cc175ec3d2a0f2ef238a60ce94d8ee931391a7856ae28c94017b`  
		Last Modified: Wed, 14 Apr 2021 21:35:21 GMT  
		Size: 105.7 MB (105703214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d283cc3a6658a3bc5ec5e9c071a04c600dc1730f2fd3190001fee106ed15af2`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66591912ff169e623ab2b1358830d6ca6d624845994a84ae3caf0f36e8fd4902`  
		Last Modified: Thu, 15 Apr 2021 09:29:52 GMT  
		Size: 6.4 MB (6390120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b30f615ae26f9d56f067032a7037a8bab1201b9d9b16e97fbf64ea64b2206fe`  
		Last Modified: Thu, 15 Apr 2021 09:29:51 GMT  
		Size: 1.3 MB (1311072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa76a5a6fe63413a584a9d507fdc39fe3ba32acdf2defc129af433ea061ff0d0`  
		Last Modified: Thu, 15 Apr 2021 09:29:50 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:10928415ac6a350e06a4b0e93ea0bd1df54f485264c3ba201be74f4e2ca6e65e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112263115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2372ee6f6b44b2a8af4f5c7d268fc532981fb94fb6261c1a3865fe43bca297e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:00:55 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:01:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:01:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:01:04 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 20:19:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:19:18 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:19:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:19:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:19:23 GMT
WORKDIR /go
# Thu, 15 Apr 2021 06:25:36 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 06:25:37 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 06:25:38 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Thu, 15 Apr 2021 06:25:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 06:25:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 06:25:42 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 06:25:43 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4dea9fd179326b36ea137aad07e06571ffe7ad849e2a13a32354dcfd5d858d`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 281.4 KB (281379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abeb04d84d23abf8470fc95982483a9117a87e55b13c591f5332a460a5233bb`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d67b51072030b3e320ebdb2cc102328ef570ff5a62537944c7bdd8b6d3c2a96`  
		Last Modified: Wed, 14 Apr 2021 21:14:35 GMT  
		Size: 101.9 MB (101910198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409bbf6fb471be4da4cdfe2943b556f85e813650ad15f40b8c067c720e22badd`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74f944345999429d1a154f38ad122a03544c5cd40567a2cfbff28652ebc59dd`  
		Last Modified: Thu, 15 Apr 2021 06:26:27 GMT  
		Size: 6.2 MB (6227102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09671a010e6fda4ee85fb08a03ecfb84013592b931fe5ab275405d4ebd95f393`  
		Last Modified: Thu, 15 Apr 2021 06:26:26 GMT  
		Size: 1.2 MB (1221592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b8e5a4a4b1e3d1c32cffc15d5f6499a098a63053e9f7d64e3d8c459bd8d32f`  
		Last Modified: Thu, 15 Apr 2021 06:26:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:6b88898e865a42b26b5b5728dd37c11d0d50cdba55afa983e8f73bb1b298e7f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111182679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59d1e2a1e9cc7a69192500f409aaec60926c7aebbd9d5fbe826a19da43f7406`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:00:38 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:01:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:01:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:01:49 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 21:27:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:27:51 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:27:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:27:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:27:58 GMT
WORKDIR /go
# Thu, 15 Apr 2021 07:40:08 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 07:40:09 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 07:40:10 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Thu, 15 Apr 2021 07:40:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 07:40:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 07:40:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 07:40:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6bd423db0b63fdc83c72eae7ef401cb2fb9eaa63961c71a867ff26bfe422f`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 280.5 KB (280532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b667ae68ff940439602ffbabae6e923c687cb56c62a793f23ddca67584049`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29816c0ab9327d02e86175d139a7769a542b54862fe51ff1e45b08213460d43`  
		Last Modified: Wed, 14 Apr 2021 22:44:51 GMT  
		Size: 101.7 MB (101699182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdca1c667e6fb49e4504c506c2d12514dcc000d827567620c331188ea1a3442`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e06e5067d7f69516cbaae00c27cf922293bd52b72d8619b2b81cf598a2f94ef`  
		Last Modified: Thu, 15 Apr 2021 07:40:57 GMT  
		Size: 5.6 MB (5558657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf96d55774eead09223dff076f67cb6a63cfc9d2c58c84585391615629bb51f`  
		Last Modified: Thu, 15 Apr 2021 07:40:56 GMT  
		Size: 1.2 MB (1219448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4d3e271d30cc64a89fed416d34dcabf285cca1d36c68eb05af89b3a25d93ee`  
		Last Modified: Thu, 15 Apr 2021 07:40:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:8550b8bbdc96d888e40c715200c102afd81370dd44daa7f73f635b76497bb860
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111714646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d143f6cec2dab36e63d7c580d595824e658340e005b0009350b99aa199e43158`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:40:18 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:40:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:40:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:41:02 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 20:44:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:44:45 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:44:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:45:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:45:28 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:44:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:44:33 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:44:34 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Thu, 15 Apr 2021 08:44:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:44:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:44:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:44:40 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186ed65a4f7bb0e9cd4b00f43359b47a4f19749dbd48e704fc578a4f43d7c96`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 281.5 KB (281488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316046926c0ae5f42710c1197ed3de9fc374986179c18611f523cf4521adeef1`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b72cf97c3e228e93e48dd9de3c1cbfed84c233199445d18ececf423af07bad4`  
		Last Modified: Wed, 14 Apr 2021 21:00:00 GMT  
		Size: 101.0 MB (101042165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bec215c8f00cdfe7327f71bc5494b3992972876f6dcf8cfb8ac6879df705ce`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91d9159703be9807d98616f6cf6d76bdb69852bb62a3efdd7579d7430860c38`  
		Last Modified: Thu, 15 Apr 2021 08:45:23 GMT  
		Size: 6.5 MB (6476693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a53b4d1c7e8e316e7c346ebf744b34dfc24ed09204d42f4e0e59bfc6d6547b`  
		Last Modified: Thu, 15 Apr 2021 08:45:22 GMT  
		Size: 1.2 MB (1201559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fe80667f0f12fcab9831b162cd18e30ff6a6d8d9f3fa03608b630420fed42c`  
		Last Modified: Thu, 15 Apr 2021 08:45:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:beafcff354118be6cd1946efd9ca2028d36de418a510abc6c65321c08f116a63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110604319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40416b4b95b5338e9d6917f544078a6208c1f7fb7e2620b32fb40c053a634b1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 31 Mar 2021 18:55:41 GMT
ADD file:1dd3315eb685a1b6729efb6f5b634e414f3da0f065078952bc6c0339dc09512d in / 
# Wed, 31 Mar 2021 18:55:49 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 04:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 01 Apr 2021 04:30:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 04:30:38 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:09:14 GMT
ENV GOLANG_VERSION=1.16.3
# Fri, 02 Apr 2021 03:11:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 02 Apr 2021 03:11:20 GMT
ENV GOPATH=/go
# Fri, 02 Apr 2021 03:11:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:11:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 02 Apr 2021 03:11:51 GMT
WORKDIR /go
# Fri, 02 Apr 2021 05:03:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 02 Apr 2021 05:03:46 GMT
ENV XCADDY_VERSION=v0.1.8
# Fri, 02 Apr 2021 18:24:35 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Fri, 02 Apr 2021 18:24:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 02 Apr 2021 18:24:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 02 Apr 2021 18:24:53 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 02 Apr 2021 18:24:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dc4792b25345295bf964e1db1bceedb2338bfad8f0fb64f0cc07b152df9aef84`  
		Last Modified: Wed, 31 Mar 2021 18:57:19 GMT  
		Size: 2.8 MB (2813219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc638e60e2f17921f3b4535edbf7095cc97278ba8d1410fd7e018101a1242be3`  
		Last Modified: Thu, 01 Apr 2021 04:44:03 GMT  
		Size: 283.4 KB (283416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b706ed0ac7a9324a306982c3913517f4f044be650413df529bf27a05c288d1b9`  
		Last Modified: Thu, 01 Apr 2021 04:44:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b169d190e0156b6deab2ff0e58a47150fc50f2868a89d84eb61c9570305e930`  
		Last Modified: Fri, 02 Apr 2021 03:23:03 GMT  
		Size: 99.5 MB (99513251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83adeb4b646f1b8b0b72cac1632f1bddf6a8b5499291eb0fec11957739b98ec1`  
		Last Modified: Fri, 02 Apr 2021 03:22:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604836dc523b402ec6de96489b450d95b267f41ae391d700d4d21b759ffde953`  
		Last Modified: Fri, 02 Apr 2021 05:04:42 GMT  
		Size: 6.8 MB (6823220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317a229e7753654e9d8b6b11dae3b5cb7be5941f353851b897405e9846c4d56`  
		Last Modified: Fri, 02 Apr 2021 18:25:36 GMT  
		Size: 1.2 MB (1170495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44a0398c5bef844d519cc025aa24a3ebf5343578a6bb8b3632cad3f0842284e`  
		Last Modified: Fri, 02 Apr 2021 18:25:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:ba89792f9bc0207e3dbc00c6b3a3a1f424e0154840a59b1ff91c17ede3ae5fa3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115434985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467ed344c1456acf0c0961ca5d0b95c075a6aa71394c97e999ab210f28c44a5c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:45:11 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:45:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:45:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:45:12 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 20:46:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:46:41 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:46:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:46:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:46:42 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:47:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:47:20 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:47:20 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Thu, 15 Apr 2021 08:47:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:47:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:47:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:47:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc746875ae346ee6ec3c9080f8a7a50bef3899ea9d5ae9dac45a81bfe861c9d`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 281.7 KB (281708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0242688236000dd8f33d16f89f36da3ef1bb2a7a32bb59a7eb97a18ed3d5158`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802ffa3a0fccf1874f89c99392b3576703f8080dd83a9d11c3abf30f9a1055f9`  
		Last Modified: Wed, 14 Apr 2021 20:52:37 GMT  
		Size: 104.8 MB (104810039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2fddec9074dc23a3b85bed21c3faca06652fbffc728c690c22aa1680ec2456`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33664dfa444fff209c035cde3fa93b7ac915a71de7753622d6c27dc0dd5bc9fa`  
		Last Modified: Thu, 15 Apr 2021 08:48:02 GMT  
		Size: 6.5 MB (6475440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2a15499d247b78ebff0035e861b3f8937d8ab01f518957a548c49d19f6eeb8`  
		Last Modified: Thu, 15 Apr 2021 08:48:01 GMT  
		Size: 1.3 MB (1264433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ade5f29297943caca06063f9acdfc1da30914a0b11a59ab490ced655d1789e7`  
		Last Modified: Thu, 15 Apr 2021 08:48:01 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:462cb3e87c34b510101ec4d6e1c3f41c249e50c11fc07a67a4c2f7d87c1e7785
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2641308715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a58bba31f403a9518e0b663472ff04a42fa6589bae4318605fb61cfc569d61`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:32:39 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 12:35:13 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.16.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'a4400345135b36cb7942e52bbaf978b66814738b855eeff8de879a09fd99de7f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:35:15 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:20:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:20:23 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:20:24 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:20:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:21:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:21:01 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770bd74ed4014a95375721a1bce0f4632edee8ed42f7f260a48718ee6f732697`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58502c76356a17ed82e8b59c7fe44ef794e3264a08a438016d76ad963ca5981`  
		Last Modified: Wed, 14 Apr 2021 12:58:39 GMT  
		Size: 139.3 MB (139343790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c463edf641e483a77edf915765e64f79175e8153cefcd88cd604e041ce7acb4`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dd5b186731eb0c9c02f4d26a06edc29940d8da335802291ec84b521c3b1be0`  
		Last Modified: Wed, 14 Apr 2021 20:26:32 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7a65e280ed60592afe5b646957a2b20de28f8c3a15588fbcdc3acee2afa400`  
		Last Modified: Wed, 14 Apr 2021 20:26:30 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd7049cb89a87a22b23b0324d7e9852cda6879a91d0544cba6d9fff99bd6917`  
		Last Modified: Wed, 14 Apr 2021 20:26:32 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db63e753a266be0f2b5e0ce8a2a0f3dffddc2e4878e33b607f261f889144e297`  
		Last Modified: Wed, 14 Apr 2021 20:26:29 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38640a1c07ea171864b89df9344108633f93264f53c4dfff35687df1c4bbdde9`  
		Last Modified: Wed, 14 Apr 2021 20:26:30 GMT  
		Size: 1.7 MB (1712234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3d577f5cd66e2d0b0789d4494605c15f2f8ab159e01e3424f87369b77d45e1`  
		Last Modified: Wed, 14 Apr 2021 20:26:30 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:bac307c1e128c3d09f03453016a4566d0184a69a4aec7fdcc557c5cadb453ed1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5987337668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b03d0cdba17b89503ca45d143a167abb87f93b49036f70ee3c0b58031b0b469`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:39:35 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 12:43:21 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.16.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'a4400345135b36cb7942e52bbaf978b66814738b855eeff8de879a09fd99de7f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:43:24 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:21:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:21:08 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:21:09 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:21:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:22:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:22:51 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a6a8e2ceb8224d343a9fc230793caeca50276050099c458dfdefc5aefe2e3e`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bc9fe33dd2652413cbaa5c8b9fc73f4b06b66dba8e87bfd17ea2b7e4263308`  
		Last Modified: Wed, 14 Apr 2021 13:01:47 GMT  
		Size: 149.1 MB (149098429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696c3886196f27d66c781b177bc4321100d92045fccae4986c33b6e2de256243`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad5bdae0dba2b5f4cc89c5942fb0d5d4a806b899832ff95bd449b5f0fc9c9cb`  
		Last Modified: Wed, 14 Apr 2021 20:26:44 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b4b163cb6fdb7544e01b1f7d90edfa10ac6cc481d9b57db46ccf7534532207`  
		Last Modified: Wed, 14 Apr 2021 20:26:41 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877c3eb7550533526d7621a2e42b1846c54be1126384ce86992e67e00dc467d2`  
		Last Modified: Wed, 14 Apr 2021 20:26:41 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73d3b8d11f7a8b62d2e8fbd42eabfa48c76d61d6843779b683cf982b7ea1c5e`  
		Last Modified: Wed, 14 Apr 2021 20:26:41 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b56149f1fc75ce46bdf8fe96da4d6d5bf47f88e9e965f9b1649a6bc4e71ae4`  
		Last Modified: Wed, 14 Apr 2021 20:26:43 GMT  
		Size: 7.0 MB (6976280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6124a00cb79bac42b744dd2831c86d6a5b51c9d2f8553c0647369f704a2efb32`  
		Last Modified: Wed, 14 Apr 2021 20:26:41 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-beta.2-builder-alpine`

```console
$ docker pull caddy@sha256:f10c2e4e8d7868b3d0164177f391569c1ceddc5605e502647695a6d3c924ec5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.4.0-beta.2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:95cacd60ef1d3a7e72d1e72264e6cb97bc62c9020e8134e1906e00e4b52f3dbd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116498360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6a619fa9afac38b043bea122011879afe8113808b2dbf088bd347f4a70a5df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:27:12 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:27:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:27:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:27:13 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 21:28:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:28:50 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:28:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:28:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:28:51 GMT
WORKDIR /go
# Thu, 15 Apr 2021 09:29:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 09:29:10 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 09:29:10 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Thu, 15 Apr 2021 09:29:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 09:29:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 09:29:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 09:29:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc1eea9eeabb6de296adb3e0c1b0722cf13251ff3e4e2d0a5f7ed8e3d48342`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 281.3 KB (281269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab2625f07be8d5c6e48046a05ff3ecc7f374b794a926fb62247b66b511909`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806e9ddb8669cc175ec3d2a0f2ef238a60ce94d8ee931391a7856ae28c94017b`  
		Last Modified: Wed, 14 Apr 2021 21:35:21 GMT  
		Size: 105.7 MB (105703214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d283cc3a6658a3bc5ec5e9c071a04c600dc1730f2fd3190001fee106ed15af2`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66591912ff169e623ab2b1358830d6ca6d624845994a84ae3caf0f36e8fd4902`  
		Last Modified: Thu, 15 Apr 2021 09:29:52 GMT  
		Size: 6.4 MB (6390120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b30f615ae26f9d56f067032a7037a8bab1201b9d9b16e97fbf64ea64b2206fe`  
		Last Modified: Thu, 15 Apr 2021 09:29:51 GMT  
		Size: 1.3 MB (1311072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa76a5a6fe63413a584a9d507fdc39fe3ba32acdf2defc129af433ea061ff0d0`  
		Last Modified: Thu, 15 Apr 2021 09:29:50 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:10928415ac6a350e06a4b0e93ea0bd1df54f485264c3ba201be74f4e2ca6e65e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112263115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2372ee6f6b44b2a8af4f5c7d268fc532981fb94fb6261c1a3865fe43bca297e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:00:55 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:01:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:01:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:01:04 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 20:19:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:19:18 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:19:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:19:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:19:23 GMT
WORKDIR /go
# Thu, 15 Apr 2021 06:25:36 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 06:25:37 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 06:25:38 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Thu, 15 Apr 2021 06:25:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 06:25:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 06:25:42 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 06:25:43 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4dea9fd179326b36ea137aad07e06571ffe7ad849e2a13a32354dcfd5d858d`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 281.4 KB (281379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abeb04d84d23abf8470fc95982483a9117a87e55b13c591f5332a460a5233bb`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d67b51072030b3e320ebdb2cc102328ef570ff5a62537944c7bdd8b6d3c2a96`  
		Last Modified: Wed, 14 Apr 2021 21:14:35 GMT  
		Size: 101.9 MB (101910198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409bbf6fb471be4da4cdfe2943b556f85e813650ad15f40b8c067c720e22badd`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74f944345999429d1a154f38ad122a03544c5cd40567a2cfbff28652ebc59dd`  
		Last Modified: Thu, 15 Apr 2021 06:26:27 GMT  
		Size: 6.2 MB (6227102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09671a010e6fda4ee85fb08a03ecfb84013592b931fe5ab275405d4ebd95f393`  
		Last Modified: Thu, 15 Apr 2021 06:26:26 GMT  
		Size: 1.2 MB (1221592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b8e5a4a4b1e3d1c32cffc15d5f6499a098a63053e9f7d64e3d8c459bd8d32f`  
		Last Modified: Thu, 15 Apr 2021 06:26:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:6b88898e865a42b26b5b5728dd37c11d0d50cdba55afa983e8f73bb1b298e7f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111182679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59d1e2a1e9cc7a69192500f409aaec60926c7aebbd9d5fbe826a19da43f7406`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:00:38 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:01:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:01:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:01:49 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 21:27:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:27:51 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:27:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:27:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:27:58 GMT
WORKDIR /go
# Thu, 15 Apr 2021 07:40:08 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 07:40:09 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 07:40:10 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Thu, 15 Apr 2021 07:40:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 07:40:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 07:40:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 07:40:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6bd423db0b63fdc83c72eae7ef401cb2fb9eaa63961c71a867ff26bfe422f`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 280.5 KB (280532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b667ae68ff940439602ffbabae6e923c687cb56c62a793f23ddca67584049`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29816c0ab9327d02e86175d139a7769a542b54862fe51ff1e45b08213460d43`  
		Last Modified: Wed, 14 Apr 2021 22:44:51 GMT  
		Size: 101.7 MB (101699182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdca1c667e6fb49e4504c506c2d12514dcc000d827567620c331188ea1a3442`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e06e5067d7f69516cbaae00c27cf922293bd52b72d8619b2b81cf598a2f94ef`  
		Last Modified: Thu, 15 Apr 2021 07:40:57 GMT  
		Size: 5.6 MB (5558657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf96d55774eead09223dff076f67cb6a63cfc9d2c58c84585391615629bb51f`  
		Last Modified: Thu, 15 Apr 2021 07:40:56 GMT  
		Size: 1.2 MB (1219448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4d3e271d30cc64a89fed416d34dcabf285cca1d36c68eb05af89b3a25d93ee`  
		Last Modified: Thu, 15 Apr 2021 07:40:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:8550b8bbdc96d888e40c715200c102afd81370dd44daa7f73f635b76497bb860
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111714646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d143f6cec2dab36e63d7c580d595824e658340e005b0009350b99aa199e43158`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:40:18 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:40:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:40:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:41:02 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 20:44:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:44:45 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:44:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:45:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:45:28 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:44:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:44:33 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:44:34 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Thu, 15 Apr 2021 08:44:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:44:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:44:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:44:40 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186ed65a4f7bb0e9cd4b00f43359b47a4f19749dbd48e704fc578a4f43d7c96`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 281.5 KB (281488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316046926c0ae5f42710c1197ed3de9fc374986179c18611f523cf4521adeef1`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b72cf97c3e228e93e48dd9de3c1cbfed84c233199445d18ececf423af07bad4`  
		Last Modified: Wed, 14 Apr 2021 21:00:00 GMT  
		Size: 101.0 MB (101042165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bec215c8f00cdfe7327f71bc5494b3992972876f6dcf8cfb8ac6879df705ce`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91d9159703be9807d98616f6cf6d76bdb69852bb62a3efdd7579d7430860c38`  
		Last Modified: Thu, 15 Apr 2021 08:45:23 GMT  
		Size: 6.5 MB (6476693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a53b4d1c7e8e316e7c346ebf744b34dfc24ed09204d42f4e0e59bfc6d6547b`  
		Last Modified: Thu, 15 Apr 2021 08:45:22 GMT  
		Size: 1.2 MB (1201559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fe80667f0f12fcab9831b162cd18e30ff6a6d8d9f3fa03608b630420fed42c`  
		Last Modified: Thu, 15 Apr 2021 08:45:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:beafcff354118be6cd1946efd9ca2028d36de418a510abc6c65321c08f116a63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110604319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40416b4b95b5338e9d6917f544078a6208c1f7fb7e2620b32fb40c053a634b1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 31 Mar 2021 18:55:41 GMT
ADD file:1dd3315eb685a1b6729efb6f5b634e414f3da0f065078952bc6c0339dc09512d in / 
# Wed, 31 Mar 2021 18:55:49 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 04:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 01 Apr 2021 04:30:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 04:30:38 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:09:14 GMT
ENV GOLANG_VERSION=1.16.3
# Fri, 02 Apr 2021 03:11:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 02 Apr 2021 03:11:20 GMT
ENV GOPATH=/go
# Fri, 02 Apr 2021 03:11:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:11:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 02 Apr 2021 03:11:51 GMT
WORKDIR /go
# Fri, 02 Apr 2021 05:03:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 02 Apr 2021 05:03:46 GMT
ENV XCADDY_VERSION=v0.1.8
# Fri, 02 Apr 2021 18:24:35 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Fri, 02 Apr 2021 18:24:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 02 Apr 2021 18:24:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 02 Apr 2021 18:24:53 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 02 Apr 2021 18:24:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dc4792b25345295bf964e1db1bceedb2338bfad8f0fb64f0cc07b152df9aef84`  
		Last Modified: Wed, 31 Mar 2021 18:57:19 GMT  
		Size: 2.8 MB (2813219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc638e60e2f17921f3b4535edbf7095cc97278ba8d1410fd7e018101a1242be3`  
		Last Modified: Thu, 01 Apr 2021 04:44:03 GMT  
		Size: 283.4 KB (283416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b706ed0ac7a9324a306982c3913517f4f044be650413df529bf27a05c288d1b9`  
		Last Modified: Thu, 01 Apr 2021 04:44:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b169d190e0156b6deab2ff0e58a47150fc50f2868a89d84eb61c9570305e930`  
		Last Modified: Fri, 02 Apr 2021 03:23:03 GMT  
		Size: 99.5 MB (99513251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83adeb4b646f1b8b0b72cac1632f1bddf6a8b5499291eb0fec11957739b98ec1`  
		Last Modified: Fri, 02 Apr 2021 03:22:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604836dc523b402ec6de96489b450d95b267f41ae391d700d4d21b759ffde953`  
		Last Modified: Fri, 02 Apr 2021 05:04:42 GMT  
		Size: 6.8 MB (6823220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317a229e7753654e9d8b6b11dae3b5cb7be5941f353851b897405e9846c4d56`  
		Last Modified: Fri, 02 Apr 2021 18:25:36 GMT  
		Size: 1.2 MB (1170495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44a0398c5bef844d519cc025aa24a3ebf5343578a6bb8b3632cad3f0842284e`  
		Last Modified: Fri, 02 Apr 2021 18:25:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:ba89792f9bc0207e3dbc00c6b3a3a1f424e0154840a59b1ff91c17ede3ae5fa3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115434985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467ed344c1456acf0c0961ca5d0b95c075a6aa71394c97e999ab210f28c44a5c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:45:11 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:45:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:45:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:45:12 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 20:46:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.16.3.src.tar.gz'; 	sha256='b298d29de9236ca47a023e382313bcc2d2eed31dfa706b60a04103ce83a71a25'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:46:41 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:46:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:46:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:46:42 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:47:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:47:20 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:47:20 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Thu, 15 Apr 2021 08:47:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:47:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:47:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:47:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc746875ae346ee6ec3c9080f8a7a50bef3899ea9d5ae9dac45a81bfe861c9d`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 281.7 KB (281708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0242688236000dd8f33d16f89f36da3ef1bb2a7a32bb59a7eb97a18ed3d5158`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802ffa3a0fccf1874f89c99392b3576703f8080dd83a9d11c3abf30f9a1055f9`  
		Last Modified: Wed, 14 Apr 2021 20:52:37 GMT  
		Size: 104.8 MB (104810039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2fddec9074dc23a3b85bed21c3faca06652fbffc728c690c22aa1680ec2456`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33664dfa444fff209c035cde3fa93b7ac915a71de7753622d6c27dc0dd5bc9fa`  
		Last Modified: Thu, 15 Apr 2021 08:48:02 GMT  
		Size: 6.5 MB (6475440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2a15499d247b78ebff0035e861b3f8937d8ab01f518957a548c49d19f6eeb8`  
		Last Modified: Thu, 15 Apr 2021 08:48:01 GMT  
		Size: 1.3 MB (1264433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ade5f29297943caca06063f9acdfc1da30914a0b11a59ab490ced655d1789e7`  
		Last Modified: Thu, 15 Apr 2021 08:48:01 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-beta.2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e00a5d56dd2df7e3710bd950089f5387899a4dd83a12cff0d0953273987af6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2.4.0-beta.2-builder-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:462cb3e87c34b510101ec4d6e1c3f41c249e50c11fc07a67a4c2f7d87c1e7785
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2641308715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a58bba31f403a9518e0b663472ff04a42fa6589bae4318605fb61cfc569d61`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:32:39 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 12:35:13 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.16.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'a4400345135b36cb7942e52bbaf978b66814738b855eeff8de879a09fd99de7f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:35:15 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:20:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:20:23 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:20:24 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:20:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:21:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:21:01 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770bd74ed4014a95375721a1bce0f4632edee8ed42f7f260a48718ee6f732697`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58502c76356a17ed82e8b59c7fe44ef794e3264a08a438016d76ad963ca5981`  
		Last Modified: Wed, 14 Apr 2021 12:58:39 GMT  
		Size: 139.3 MB (139343790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c463edf641e483a77edf915765e64f79175e8153cefcd88cd604e041ce7acb4`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dd5b186731eb0c9c02f4d26a06edc29940d8da335802291ec84b521c3b1be0`  
		Last Modified: Wed, 14 Apr 2021 20:26:32 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7a65e280ed60592afe5b646957a2b20de28f8c3a15588fbcdc3acee2afa400`  
		Last Modified: Wed, 14 Apr 2021 20:26:30 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd7049cb89a87a22b23b0324d7e9852cda6879a91d0544cba6d9fff99bd6917`  
		Last Modified: Wed, 14 Apr 2021 20:26:32 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db63e753a266be0f2b5e0ce8a2a0f3dffddc2e4878e33b607f261f889144e297`  
		Last Modified: Wed, 14 Apr 2021 20:26:29 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38640a1c07ea171864b89df9344108633f93264f53c4dfff35687df1c4bbdde9`  
		Last Modified: Wed, 14 Apr 2021 20:26:30 GMT  
		Size: 1.7 MB (1712234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3d577f5cd66e2d0b0789d4494605c15f2f8ab159e01e3424f87369b77d45e1`  
		Last Modified: Wed, 14 Apr 2021 20:26:30 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-beta.2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:b13c553a0955492ca7e5e96a9bdcad292aabe138d1edd6e6337e3e19be7b48a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.4.0-beta.2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:bac307c1e128c3d09f03453016a4566d0184a69a4aec7fdcc557c5cadb453ed1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5987337668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b03d0cdba17b89503ca45d143a167abb87f93b49036f70ee3c0b58031b0b469`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:39:35 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 12:43:21 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.16.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'a4400345135b36cb7942e52bbaf978b66814738b855eeff8de879a09fd99de7f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:43:24 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:21:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:21:08 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:21:09 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:21:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:22:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:22:51 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a6a8e2ceb8224d343a9fc230793caeca50276050099c458dfdefc5aefe2e3e`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bc9fe33dd2652413cbaa5c8b9fc73f4b06b66dba8e87bfd17ea2b7e4263308`  
		Last Modified: Wed, 14 Apr 2021 13:01:47 GMT  
		Size: 149.1 MB (149098429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696c3886196f27d66c781b177bc4321100d92045fccae4986c33b6e2de256243`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad5bdae0dba2b5f4cc89c5942fb0d5d4a806b899832ff95bd449b5f0fc9c9cb`  
		Last Modified: Wed, 14 Apr 2021 20:26:44 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b4b163cb6fdb7544e01b1f7d90edfa10ac6cc481d9b57db46ccf7534532207`  
		Last Modified: Wed, 14 Apr 2021 20:26:41 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877c3eb7550533526d7621a2e42b1846c54be1126384ce86992e67e00dc467d2`  
		Last Modified: Wed, 14 Apr 2021 20:26:41 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73d3b8d11f7a8b62d2e8fbd42eabfa48c76d61d6843779b683cf982b7ea1c5e`  
		Last Modified: Wed, 14 Apr 2021 20:26:41 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b56149f1fc75ce46bdf8fe96da4d6d5bf47f88e9e965f9b1649a6bc4e71ae4`  
		Last Modified: Wed, 14 Apr 2021 20:26:43 GMT  
		Size: 7.0 MB (6976280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6124a00cb79bac42b744dd2831c86d6a5b51c9d2f8553c0647369f704a2efb32`  
		Last Modified: Wed, 14 Apr 2021 20:26:41 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-beta.2-windowsservercore`

```console
$ docker pull caddy@sha256:4a9eaf08d3964f22fc0bda6ec4e692cd90829921f2239c380ba4e5d691dbce33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.4.0-beta.2-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:57007a2384bbff9e730072565519dbdb596e6eb66e59969ba33cc31b8a5cea77
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487035062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21166c4140d929d0caccfb9e9ff5b3af4641c7594112345c1d3d87a5bf7f52ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:13:54 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:13:55 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:14:32 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9f41c88fc8c2c28230c5eb67fb7d9ef23477a351fb716a44486b3d1a37569fb141112cd3582adcd44424b2819c22723fb49023a6d371e1bf8d92eefe4e7e9ed4')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:14:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:14:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:14:35 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:14:36 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:14:37 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:14:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:14:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:14:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:14:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:14:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:14:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:14:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:14:45 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:14:46 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:14:47 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:15:12 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:15:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de472ba1df2f836f9b4125180bedb0ca0f6c425460dd8535a92764dff8169f8`  
		Last Modified: Wed, 14 Apr 2021 20:25:56 GMT  
		Size: 5.1 MB (5080859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55627e36839779d3cfb370ec41774f50d7db4ff914a3077c70b75f96287e5af0`  
		Last Modified: Wed, 14 Apr 2021 20:25:52 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f2e16d47aeed21efafcfe34553edd6166984a4ae765a5420a50d46f1d204b6`  
		Last Modified: Wed, 14 Apr 2021 20:25:56 GMT  
		Size: 11.9 MB (11867562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c501d3d5d88099b96f7b95b3f58cdc7baea8006662464c5677f3d8abbad2`  
		Last Modified: Wed, 14 Apr 2021 20:25:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee81a85c97e2bebd04246c72c2e9093a2fc92d5b3a1c61092a47ca2dbca3195`  
		Last Modified: Wed, 14 Apr 2021 20:25:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c473eb70ede949ae95779d72ada5e737f68bee537a5892368b21c219b7ae8f2`  
		Last Modified: Wed, 14 Apr 2021 20:25:51 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962e4b4d5583a800a5fa99d1c9f8344405685fc162718cfab1c851df0b149bf4`  
		Last Modified: Wed, 14 Apr 2021 20:25:50 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4277207668aa329a0fcf285a3e8044549f14fcdc258b54941786b2dbac2b738f`  
		Last Modified: Wed, 14 Apr 2021 20:25:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8932075115714c24da0e0b15ca784e45621efdac23f763feac93a8d63e51dc18`  
		Last Modified: Wed, 14 Apr 2021 20:25:49 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ec24942a02e14cc4f3627742e1a9ba37a831854d99e25e35ab78c7603f4cbd`  
		Last Modified: Wed, 14 Apr 2021 20:25:49 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554d5e240ec502a081852a31141622d738e021388206ba4f43cb159c7c7d7a5`  
		Last Modified: Wed, 14 Apr 2021 20:25:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6d8e32fb60c802dc23aa51a0c38e0588aebbf5461bd4d3b66de34e80d2eb6`  
		Last Modified: Wed, 14 Apr 2021 20:25:47 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339de9553d5fd226cedff68f9c92d817957f2f7809f9d64da67f12fb23bed32`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51272577d8785b827aa7bb896767009a940ee9343189459c6e3c675e566f9f0d`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde8de3cc19d01e8b1d8624b50438d1fa257a16237f41b1d73cff4fa65768a4d`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455f5cdc11de43d196e81d074362a41abcaed1366315581b689ba2a88d3f4857`  
		Last Modified: Wed, 14 Apr 2021 20:25:44 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d7b5d207b9968f7f40e32437e99ef85d2dde4afba849a8825896ee82ed5f50`  
		Last Modified: Wed, 14 Apr 2021 20:25:43 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9dc90818d729c2fd0cb0bac96912bd2969512c4a029b3a3b21b3764b004500`  
		Last Modified: Wed, 14 Apr 2021 20:25:44 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d304d34d98bbc8fed2a3f472757c6377c204ec57a87fd6a3823cf4236f26e877`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 308.5 KB (308506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701310ad80f85832364aa3313c02e66c8a9e60cd165a937c96075db0496b486c`  
		Last Modified: Wed, 14 Apr 2021 20:25:43 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-beta.2-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:fa30c18bcdf91806b54ea7ed3a348627df09108ceebc6d0d5550fb0ad3455cde
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5817979261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421de0d93291fba46ed24305b5fe5fe3f674bd381400d00c5bf45a608e170018`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:16:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:16:51 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:18:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9f41c88fc8c2c28230c5eb67fb7d9ef23477a351fb716a44486b3d1a37569fb141112cd3582adcd44424b2819c22723fb49023a6d371e1bf8d92eefe4e7e9ed4')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:18:40 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:18:41 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:18:42 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:18:43 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:18:45 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:18:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:18:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:18:48 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:18:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:18:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:18:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:18:53 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:18:54 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:18:55 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:20:11 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:20:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b068c1eb113cc4e93590b9ea7cd57796316b3b21ba390abfe889d79e702cec3c`  
		Last Modified: Wed, 14 Apr 2021 20:26:14 GMT  
		Size: 5.7 MB (5660433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d97864bd63ccf6806c9e9849c61e19f7a4b476e59b63ac9d243241fdd271e3d`  
		Last Modified: Wed, 14 Apr 2021 20:26:12 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab97c72d1ce9fea13fa1e516f83d28adc8a155bfa23822ce7752d2da4f74c5b`  
		Last Modified: Wed, 14 Apr 2021 20:26:17 GMT  
		Size: 17.2 MB (17151549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8acb6e1c103fe19721c692609bc6eb55acdd0326bb9d027768a6ba92e7e0202`  
		Last Modified: Wed, 14 Apr 2021 20:26:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cdd68811b5c180d1153a0f2b6d8edceb94aad8069b64040d2d8db829dd448e`  
		Last Modified: Wed, 14 Apr 2021 20:26:11 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab6a4bef16e77771e00038b7a77d618e3fc0da8ef554e67d5a8c4e0400f1809`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558d80b23de2d6fb99e705591d268689266afd67afef1012302baf76d43c6a0c`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6382ddb421f9b6ed0c2a785186cf291be684523ec1ddc96d4cfe2963b4f37b79`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991b64532293d0a7f622cce85a5709f33577f5803fda5d8838a8cc850532054c`  
		Last Modified: Wed, 14 Apr 2021 20:26:08 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bf3364ee0158cad4826de8a57245fcb5a54a4f33f0d07fa1867d70b482812d`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4572b72928444624d70624bd4188a957e1cbcdc364bacd3026fc6e46d2154e72`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fae1b86448ffecd80365e375393080c5484925ed877f02fcc8f9bd3389c725c`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae7cbf677188f13aae6856b110af11696cac21e78313f3d225815d7fb16b55b`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e925b48c88da00efc465f3291af0f81734fa9088838bf99e2b21c9763c76aa80`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325a0551f6981da1e92d3974f95db9dbc5553b1acd629302ab8f2ed5aaf64a41`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fbbe5b0ac1c5adbe504a0bded280a2ebc8133939e17035cdf61e5f811a9d79`  
		Last Modified: Wed, 14 Apr 2021 20:26:03 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7999335cd30f75fd39b8d9ebfaac1dfad63e643813eeabfd572210dc15f442`  
		Last Modified: Wed, 14 Apr 2021 20:26:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f9edc21a0f3503cc8695bfb1f0f2bf825fe586c31c14112ebaffc2cccb32be`  
		Last Modified: Wed, 14 Apr 2021 20:26:04 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654c270965f7a90556b3aa0fa48d1fea0ff65f6918708e24ebd83c36be1e0ae9`  
		Last Modified: Wed, 14 Apr 2021 20:26:04 GMT  
		Size: 258.0 KB (257960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893d5403793a417c0e1beac002e47a4e1d311d6aca319395cd9422949b7d393c`  
		Last Modified: Wed, 14 Apr 2021 20:26:03 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-beta.2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:3113033bee6cc942c3e7296b8272fb71bc1394e921982ce6690ecfdff5eeedbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2.4.0-beta.2-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:57007a2384bbff9e730072565519dbdb596e6eb66e59969ba33cc31b8a5cea77
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487035062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21166c4140d929d0caccfb9e9ff5b3af4641c7594112345c1d3d87a5bf7f52ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:13:54 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:13:55 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:14:32 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9f41c88fc8c2c28230c5eb67fb7d9ef23477a351fb716a44486b3d1a37569fb141112cd3582adcd44424b2819c22723fb49023a6d371e1bf8d92eefe4e7e9ed4')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:14:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:14:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:14:35 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:14:36 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:14:37 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:14:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:14:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:14:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:14:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:14:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:14:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:14:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:14:45 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:14:46 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:14:47 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:15:12 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:15:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de472ba1df2f836f9b4125180bedb0ca0f6c425460dd8535a92764dff8169f8`  
		Last Modified: Wed, 14 Apr 2021 20:25:56 GMT  
		Size: 5.1 MB (5080859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55627e36839779d3cfb370ec41774f50d7db4ff914a3077c70b75f96287e5af0`  
		Last Modified: Wed, 14 Apr 2021 20:25:52 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f2e16d47aeed21efafcfe34553edd6166984a4ae765a5420a50d46f1d204b6`  
		Last Modified: Wed, 14 Apr 2021 20:25:56 GMT  
		Size: 11.9 MB (11867562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c501d3d5d88099b96f7b95b3f58cdc7baea8006662464c5677f3d8abbad2`  
		Last Modified: Wed, 14 Apr 2021 20:25:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee81a85c97e2bebd04246c72c2e9093a2fc92d5b3a1c61092a47ca2dbca3195`  
		Last Modified: Wed, 14 Apr 2021 20:25:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c473eb70ede949ae95779d72ada5e737f68bee537a5892368b21c219b7ae8f2`  
		Last Modified: Wed, 14 Apr 2021 20:25:51 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962e4b4d5583a800a5fa99d1c9f8344405685fc162718cfab1c851df0b149bf4`  
		Last Modified: Wed, 14 Apr 2021 20:25:50 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4277207668aa329a0fcf285a3e8044549f14fcdc258b54941786b2dbac2b738f`  
		Last Modified: Wed, 14 Apr 2021 20:25:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8932075115714c24da0e0b15ca784e45621efdac23f763feac93a8d63e51dc18`  
		Last Modified: Wed, 14 Apr 2021 20:25:49 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ec24942a02e14cc4f3627742e1a9ba37a831854d99e25e35ab78c7603f4cbd`  
		Last Modified: Wed, 14 Apr 2021 20:25:49 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554d5e240ec502a081852a31141622d738e021388206ba4f43cb159c7c7d7a5`  
		Last Modified: Wed, 14 Apr 2021 20:25:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6d8e32fb60c802dc23aa51a0c38e0588aebbf5461bd4d3b66de34e80d2eb6`  
		Last Modified: Wed, 14 Apr 2021 20:25:47 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339de9553d5fd226cedff68f9c92d817957f2f7809f9d64da67f12fb23bed32`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51272577d8785b827aa7bb896767009a940ee9343189459c6e3c675e566f9f0d`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde8de3cc19d01e8b1d8624b50438d1fa257a16237f41b1d73cff4fa65768a4d`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455f5cdc11de43d196e81d074362a41abcaed1366315581b689ba2a88d3f4857`  
		Last Modified: Wed, 14 Apr 2021 20:25:44 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d7b5d207b9968f7f40e32437e99ef85d2dde4afba849a8825896ee82ed5f50`  
		Last Modified: Wed, 14 Apr 2021 20:25:43 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9dc90818d729c2fd0cb0bac96912bd2969512c4a029b3a3b21b3764b004500`  
		Last Modified: Wed, 14 Apr 2021 20:25:44 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d304d34d98bbc8fed2a3f472757c6377c204ec57a87fd6a3823cf4236f26e877`  
		Last Modified: Wed, 14 Apr 2021 20:25:46 GMT  
		Size: 308.5 KB (308506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701310ad80f85832364aa3313c02e66c8a9e60cd165a937c96075db0496b486c`  
		Last Modified: Wed, 14 Apr 2021 20:25:43 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-beta.2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:1fb2c0b974c7bfb254e570702f7d13dcfa8c39e44a21311cb6b7a831ac6a0638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.4.0-beta.2-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:fa30c18bcdf91806b54ea7ed3a348627df09108ceebc6d0d5550fb0ad3455cde
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5817979261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421de0d93291fba46ed24305b5fe5fe3f674bd381400d00c5bf45a608e170018`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:16:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/e784a6dd41d1cd4f72de2a427961bfb097b72cf9/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:16:51 GMT
ENV CADDY_VERSION=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:18:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0-beta.2/caddy_2.4.0-beta.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9f41c88fc8c2c28230c5eb67fb7d9ef23477a351fb716a44486b3d1a37569fb141112cd3582adcd44424b2819c22723fb49023a6d371e1bf8d92eefe4e7e9ed4')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:18:40 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:18:41 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:18:42 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:18:43 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:18:45 GMT
LABEL org.opencontainers.image.version=v2.4.0-beta.2
# Wed, 14 Apr 2021 20:18:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:18:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:18:48 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:18:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:18:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:18:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:18:53 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:18:54 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:18:55 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:20:11 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:20:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b068c1eb113cc4e93590b9ea7cd57796316b3b21ba390abfe889d79e702cec3c`  
		Last Modified: Wed, 14 Apr 2021 20:26:14 GMT  
		Size: 5.7 MB (5660433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d97864bd63ccf6806c9e9849c61e19f7a4b476e59b63ac9d243241fdd271e3d`  
		Last Modified: Wed, 14 Apr 2021 20:26:12 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab97c72d1ce9fea13fa1e516f83d28adc8a155bfa23822ce7752d2da4f74c5b`  
		Last Modified: Wed, 14 Apr 2021 20:26:17 GMT  
		Size: 17.2 MB (17151549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8acb6e1c103fe19721c692609bc6eb55acdd0326bb9d027768a6ba92e7e0202`  
		Last Modified: Wed, 14 Apr 2021 20:26:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cdd68811b5c180d1153a0f2b6d8edceb94aad8069b64040d2d8db829dd448e`  
		Last Modified: Wed, 14 Apr 2021 20:26:11 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab6a4bef16e77771e00038b7a77d618e3fc0da8ef554e67d5a8c4e0400f1809`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558d80b23de2d6fb99e705591d268689266afd67afef1012302baf76d43c6a0c`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6382ddb421f9b6ed0c2a785186cf291be684523ec1ddc96d4cfe2963b4f37b79`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991b64532293d0a7f622cce85a5709f33577f5803fda5d8838a8cc850532054c`  
		Last Modified: Wed, 14 Apr 2021 20:26:08 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bf3364ee0158cad4826de8a57245fcb5a54a4f33f0d07fa1867d70b482812d`  
		Last Modified: Wed, 14 Apr 2021 20:26:09 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4572b72928444624d70624bd4188a957e1cbcdc364bacd3026fc6e46d2154e72`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fae1b86448ffecd80365e375393080c5484925ed877f02fcc8f9bd3389c725c`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae7cbf677188f13aae6856b110af11696cac21e78313f3d225815d7fb16b55b`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e925b48c88da00efc465f3291af0f81734fa9088838bf99e2b21c9763c76aa80`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325a0551f6981da1e92d3974f95db9dbc5553b1acd629302ab8f2ed5aaf64a41`  
		Last Modified: Wed, 14 Apr 2021 20:26:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fbbe5b0ac1c5adbe504a0bded280a2ebc8133939e17035cdf61e5f811a9d79`  
		Last Modified: Wed, 14 Apr 2021 20:26:03 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7999335cd30f75fd39b8d9ebfaac1dfad63e643813eeabfd572210dc15f442`  
		Last Modified: Wed, 14 Apr 2021 20:26:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f9edc21a0f3503cc8695bfb1f0f2bf825fe586c31c14112ebaffc2cccb32be`  
		Last Modified: Wed, 14 Apr 2021 20:26:04 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654c270965f7a90556b3aa0fa48d1fea0ff65f6918708e24ebd83c36be1e0ae9`  
		Last Modified: Wed, 14 Apr 2021 20:26:04 GMT  
		Size: 258.0 KB (257960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893d5403793a417c0e1beac002e47a4e1d311d6aca319395cd9422949b7d393c`  
		Last Modified: Wed, 14 Apr 2021 20:26:03 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:fa1ae85dc9b12ee47e98d7ef21db409eada3ed48f1865e4b1f1dd78f417132fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:6fbf52298c46c55c572670b5395ecaee5d399338003c9bb4e4abed875c542f4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395cc3713b2ca5574a9b4aafc468a1533d16582efe47dcab74ed547540d698a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:10:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:10:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:10:49 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:10:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:10:53 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:10:54 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:10:55 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:56 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:10:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a0cd9cca5be9b30bbc70611052d1456502e1f338ce4b14946233b21cd6a9a`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 300.0 KB (300016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5666523658a43fbbdff6b8fca498a988f4dcecc3ce027f1701414658c21d4ea`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097228407f13a161f68b188b0a4f255855b64d84e7b076745a744d5aa7ed8cf`  
		Last Modified: Wed, 14 Apr 2021 20:11:49 GMT  
		Size: 11.6 MB (11622383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40682d93cc09b4592a1b9c08d48d0a956b5eef4f123d80d1a12942482edb6aab`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0df9df9725cab39fe073887c98b54bf7bf1c96b3ed0e23916737c7c4877576c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13856181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce1c33ce4509195edc1c67d2dcd15c6c5fc0b35cec2e90714ec3007739600eb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:45:19 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:45:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:45:36 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:45:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:46:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:46:04 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:46:05 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:46:07 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:46:08 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:46:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:46:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:46:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:46:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:46:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:46:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:46:22 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:46:23 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:46:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b83e8a6ea044be2a9e3c87c5fdc047ce9a52d1a64e48f8330d9a19002ecffe1`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 300.1 KB (300117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9949bdfbb1d296dd158f8c2bb959f96c8da162a0d579f68fa3f5a4af58bed5b`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c5cc316af29a89f9a1d4e279b5d1bb964095a15795647d013f40921bc808c3`  
		Last Modified: Wed, 14 Apr 2021 19:47:54 GMT  
		Size: 10.9 MB (10944831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6670cc680ce5e5d9a0adfc380fe4a89ac2a2dcef5a7adeb874967a356e6742`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a41623f53d582c8b503ae859f6ae98c7c0695eddb11bdbf8514b9b914955c3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13639723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b837694902a1a259a4915444feda59d895ed37ffbef66b8518b9a884f029c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:39:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:39:34 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:39:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:39:43 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:39:45 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:39:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:39:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:39:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:39:56 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:39:57 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:39:58 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:39:59 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239ad5e698454501b0de011bffea35a660806a0b85a6141776581e3a98bc467`  
		Last Modified: Wed, 14 Apr 2021 19:41:24 GMT  
		Size: 299.2 KB (299210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0460b038be93717158ad9cdb6f83768b7129eaf4fcaef8620adc7509d0e5fe`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0905d1ca8c4f74966ae8a7b5ebe8fdb33854c4a759d543d767dd9a0add81f155`  
		Last Modified: Wed, 14 Apr 2021 19:41:29 GMT  
		Size: 10.9 MB (10925348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02da274f552e184a7fa5527990e666d77c70e3715a0d96b7588e7433b3022a`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:789a609d1ac52d0bed8718bab07beff0633df8333c8f88a4a54ccc6fa14bfb1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13616003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fab65bcfd86f1922cd2ec38aa336d5c219f99ed0d0878dede9732c770b2113`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:59:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 18:59:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 18:59:56 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:00:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:00:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:00:06 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:00:07 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:00:08 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:00:09 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:00:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:00:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:00:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:00:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:00:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:00:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:00:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:00:22 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:00:23 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:00:25 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:00:26 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:00:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96638d6a34d0588d1723cae433a6176b83e4bec10cb3a37ffac1891313dd144`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 300.4 KB (300352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e448c61e8710f135f93f0f19db0e1e20005299e4e28dfcbba2fc048075b11`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955bb49759c02742bb3fe501b864201c3b2a349f8253b73d7114ba39a816ac02`  
		Last Modified: Wed, 14 Apr 2021 19:01:54 GMT  
		Size: 10.6 MB (10598977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639f923159f69301bb290369ef4804ec8ef52d3d159d531976474f8d34d3dc54`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:f551e1db7910e2d5235d303760aff5b514fc6e8b49d8d67d434bb23c40ac25db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13356454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bd235f46e537404cdab42c3dfb3d0058f97ed5d7984f2e71ad8734adcc6a8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:09:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:09:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 22:09:24 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 22:09:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:09:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:09:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:10:01 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:10:06 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:10:15 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:10:22 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 22:10:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:10:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:10:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:10:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:11:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:11:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:11:20 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:11:27 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:11:35 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:11:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93dd31358a6e859a05bb506b946720f02c7ec7969776d811b20eaaa84508cd7`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 302.3 KB (302339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8077b8c9cca163d9a34281a866cf5fe991ff8c160ebd1ab1b617c6b722ec690`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55884816b8eca8150db9473989410e372c69c5431deb51a6cacd029895cf3dd6`  
		Last Modified: Wed, 14 Apr 2021 22:15:43 GMT  
		Size: 10.2 MB (10241380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efee06e0a650ff5f146fc54a695d4bf2b44e19da18120fdc494982d52cdd62`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:68aaf625a22bff4e71edf895129baa2d562765c24ac81a5c68aff2995ebf89c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14146947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd454f0dfa64ee1a952f9ed74a3f3bda3688a9565f062c3ea37e48b54eb210`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:21 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:07:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:07:22 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:07:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:07:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:07:27 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:07:27 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:07:30 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:07:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dab58470b754d248933aa56b48394e3ee4db4561d430d23ea378f0371ca59cb`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 300.5 KB (300471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd514b608428ea44dae7dc67e641a276593e7715178d86d7702153521de849d7`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a437814dab55b178c71f55598a70d0b532b3f645bdeb43e89244a6ebcde01446`  
		Last Modified: Wed, 14 Apr 2021 20:08:18 GMT  
		Size: 11.3 MB (11272061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412be9af105c69ee35fec76e8c0dbde8c8ba61c774b7d354e9c9fc8f538e8155`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:ee7737d128957678b88f6321b5107ec6e23963fa2012cf2188efc72722ad6f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:3eb8fd03c47af4395bea3f6bcb98e8385f4634c7f513e7746421ae828d62c66f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119544759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dab7b132f437ff0879dfdef9940c90324e4d6a4c5af7de0c2b7b256d5ebf21b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:29:08 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:29:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:29:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:32:48 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:34:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:34:19 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:34:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:34:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:34:20 GMT
WORKDIR /go
# Thu, 15 Apr 2021 09:28:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 09:28:59 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 09:29:00 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 09:29:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 09:29:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 09:29:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 09:29:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b54d2d4342f88201f48db57cae1f7edbacae870ee13d7962f999edd7529a9`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5898d3d0f1f95fd666f764bf918c1656be6169868335cb63bc428a5ef47cf32`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2292415af71b71f5b5eae8c7426f41afef6af628b410acf0b9d036240addeeb`  
		Last Modified: Wed, 14 Apr 2021 21:37:07 GMT  
		Size: 106.8 MB (106825070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483424ea5e047556d6172c0273d0671d368d0e42448ee6eee213adf6f0f0e218`  
		Last Modified: Wed, 14 Apr 2021 21:36:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936094b3e444e93dce0400536b066def6153e8795892e63e44042e3507f71fa7`  
		Last Modified: Thu, 15 Apr 2021 09:29:37 GMT  
		Size: 8.3 MB (8326458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41aa4f492f90b4b9472fbfce9bf1b1f4f9dc08fb9d9ec92fb040160716042e0`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 1.3 MB (1311071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9495ef365ef431007d48d2a011656481c0dcfe85888f9dc8d8780a41db96f26`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ca579a39dbe79f52268fdb5230c9a5ad7cfc115e540b515ecce7a557714b1711
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114723671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf78bfe4d146d0c0b28698b45888f4e663125f52bfb222cd1e7bf6e85248038`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:19:47 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:19:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:19:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:24 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:11:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:12:16 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:12:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:13:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:13:32 GMT
WORKDIR /go
# Thu, 15 Apr 2021 06:25:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 06:25:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 06:25:12 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 06:25:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 06:25:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 06:25:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 06:25:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c231c184d802a569805e44837dd1ea2cb0522bb03ca5763ef5ed9fae5896c`  
		Last Modified: Wed, 14 Apr 2021 21:15:05 GMT  
		Size: 281.0 KB (280982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8ca9e585b85be2e7ddaaf213e22bdb986eba4da2a8cc4d8b45f762752e17df`  
		Last Modified: Wed, 14 Apr 2021 21:15:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa237e1852b6dc6312c54835af4eedd49fc347da91eee2bd9a5cbdf3e4a09a74`  
		Last Modified: Wed, 14 Apr 2021 21:17:14 GMT  
		Size: 102.7 MB (102671404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfaf15ab73c5bd3fd51cf3ad7a986d94a84a0de33b0e2b421df3ece40813b6f`  
		Last Modified: Wed, 14 Apr 2021 21:16:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bceb981e039ba8e3426115768baf63e8372fc75250fbb6d6df522d9558b8abb8`  
		Last Modified: Thu, 15 Apr 2021 06:26:15 GMT  
		Size: 7.9 MB (7943726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec602f7edc3131a49dd0ab8bd4e7b207009dc592d13555e12296c433ef56919`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 1.2 MB (1221591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57d036d826077e94afba969b41b7bdc9d1ae0f266d04bc343350ff391e2fd75`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:28ae48497c0b64592d20b21b122fe14268d4ce85a5e9ea9b5b583d5a58726cfb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113527342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15cf44fde7fa3b279efe2039c6fb0882edb4c49fdc0076fc26c90bdcec1b365`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:28:16 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:28:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:28:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:19:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 22:43:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 22:43:26 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 22:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:43:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 22:43:36 GMT
WORKDIR /go
# Thu, 15 Apr 2021 07:39:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 07:39:41 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 07:39:43 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 07:39:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 07:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 07:39:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 07:39:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a884c3a8500725e0f08f924091ec61ae3e3acee3b0ffe5839b06f874ee63dc08`  
		Last Modified: Wed, 14 Apr 2021 22:45:08 GMT  
		Size: 280.1 KB (280078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f87f08a98de1e7cb636267b626d4e644775ff7962ea1ff9b4813f740b89e67`  
		Last Modified: Wed, 14 Apr 2021 22:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c59f8b5aa025c1cb85f375b22cbc86c2892e311a5aad724e9af892abbefca31`  
		Last Modified: Wed, 14 Apr 2021 22:47:06 GMT  
		Size: 102.5 MB (102463090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146d2365c5f44423fcd2cd482e0d74d784c72e892e81c7d26dd1aa1a8bd3ab43`  
		Last Modified: Wed, 14 Apr 2021 22:46:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689b9c2e77675507509d87b28e5aa533b980296e5ffa8999fa8268863b5691b5`  
		Last Modified: Thu, 15 Apr 2021 07:40:47 GMT  
		Size: 7.2 MB (7154833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c64d502102e5ce2b6b103a14d9af56e06fa146e4eb76cf6423e58e5407b6475`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 1.2 MB (1219446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a490f0c5cdae283a0f25e3bc46079442ea559abaa3cf16c64a5a0cef30befc45`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b89b93e92ffd9427041b5ed8850cc44f292b611e7dee55242ea02c6c3ccf2a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8d157b29403fa75da94e9701e2c3e3d065de48b910f8045b32619bdc25f1e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:09 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:46:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:46:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:54:59 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:58:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:58:21 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:58:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:58:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:58:41 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:44:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:44:05 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:44:06 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:44:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:44:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:44:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:44:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2150ab4b89a5dc832780f442998074db1582348dca0eb60d6b79b59df025f25f`  
		Last Modified: Wed, 14 Apr 2021 21:00:21 GMT  
		Size: 281.2 KB (281220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9d22c0ca7447b1a1b25889675e84f2ed68ecd519fdc513796712138820633b`  
		Last Modified: Wed, 14 Apr 2021 21:00:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cfb7326a4720568ee9867ad9f6dd4b796bcd9e899c6a27a3891589eae5cc06`  
		Last Modified: Wed, 14 Apr 2021 21:02:14 GMT  
		Size: 102.1 MB (102136232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a0cdf5ccbda3f4358749dfd4a03c520b2ca135a303988e74a5796796ccc30d`  
		Last Modified: Wed, 14 Apr 2021 21:01:48 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad8e65604482fa70f402e9fde824dec1ff3f257637f247fe6279c69757b9de6`  
		Last Modified: Thu, 15 Apr 2021 08:45:09 GMT  
		Size: 8.5 MB (8518404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1496bb71598cd42c2f92595b24f0aa7a34914fb6048c11499146f728964ddb`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 1.2 MB (1201555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1678712b911f6bb0ed8a67b615034fcec04e64bca853d43c39e3659d54e649`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4d7764de3f8d29cbb22b2b973802bbf36aa89b6c1e6a11cf6934b2273b80e59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113988669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c777710e48b168e93b792b4171e667a5c16209c668b09dd54d442ad4ef1c55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 31 Mar 2021 18:56:11 GMT
ADD file:d51af61c5955c980d18387ab532110c3874f95a87768be84dfd1eeb3e701d3a4 in / 
# Wed, 31 Mar 2021 18:56:16 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 04:33:46 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 01 Apr 2021 04:33:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 04:33:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:18:36 GMT
ENV GOLANG_VERSION=1.15.11
# Fri, 02 Apr 2021 03:20:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 02 Apr 2021 03:20:38 GMT
ENV GOPATH=/go
# Fri, 02 Apr 2021 03:20:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:20:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 02 Apr 2021 03:21:02 GMT
WORKDIR /go
# Fri, 02 Apr 2021 05:03:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 02 Apr 2021 05:03:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Fri, 02 Apr 2021 05:03:15 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 02 Apr 2021 05:03:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 02 Apr 2021 05:03:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 02 Apr 2021 05:03:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 02 Apr 2021 05:03:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6d4557865d9cec3513c1a5e744cb1073a563d464b8d546911289b9df9998f1b`  
		Last Modified: Wed, 31 Mar 2021 18:57:36 GMT  
		Size: 2.8 MB (2806070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128ce9f93b1dd5f42d7663646400f1307cddfad6a5361031e3a1ca8c46d90d2e`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 283.2 KB (283224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb52babc5b3ae7ccfca63bfc4092e7d57cbd51bc203af266e4fcb0169a6107`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91ebeddf57ad09e8e1b3eb1e312be6a4484d88f8f970a7b241d759abe98e5f`  
		Last Modified: Fri, 02 Apr 2021 03:25:31 GMT  
		Size: 100.8 MB (100806744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac05f37b09f2517038025dd2d905a5d3ecbd9af697023fe05bc857ed48b8f455`  
		Last Modified: Fri, 02 Apr 2021 03:25:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e2e6a908474ce0f09d3cc2e30293784024f2a821c330690e753b01155c5346`  
		Last Modified: Fri, 02 Apr 2021 05:04:26 GMT  
		Size: 8.9 MB (8921423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b888e7962a16510b476660b91df0be664af7f16e7eb94288112b51bfd206995`  
		Last Modified: Fri, 02 Apr 2021 05:04:25 GMT  
		Size: 1.2 MB (1170492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ce4e5965570ab285f5e3be6ab2ca4cd6b618b344303a3e09cbb4c46fb2393f`  
		Last Modified: Fri, 02 Apr 2021 05:04:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:75a9876d6656c0b08c814240a013160e20a41c6a4bfe5939f9befb45ab7e277c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118429233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3dc1b085458cb773f526584cf4e59ebff486ad9b1f684021e37907fd83cb1d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:59 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:47:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:47:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:51:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:51:52 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:51:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:51:53 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:47:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:47:02 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:47:03 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:47:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:47:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:47:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:47:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c45d0e43ef7a36e47dfc16916a076f7ba26b656842380c26207ad30f5c8b`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 281.3 KB (281343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f1645d6cbfccd2924337f37dc819e7edc27989ead8bc679441954a0e483c24`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3233df950b4b58e213bfc323437185867d0d54de06ac41e9e5c408ca83ecd5ca`  
		Last Modified: Wed, 14 Apr 2021 20:53:56 GMT  
		Size: 105.9 MB (105944122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3995327d2f868035d65ecb6b315f8595f43db3da3e10b19dbe964a66b6cfd746`  
		Last Modified: Wed, 14 Apr 2021 20:53:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04afa35fe1fde3bf4e11163aeea0b3f7c6084de121d5f071291ee325ac535f06`  
		Last Modified: Thu, 15 Apr 2021 08:47:53 GMT  
		Size: 8.4 MB (8370192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81b8ec43677381485cbedd3fa6dc24863c5d8f04d8700720662cc1293d70ef`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 1.3 MB (1264434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf872018e54c322f4f460c7e7816a9ae61c2a3c07f73d7f4324c18a21f6ccdfb`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:5d074fc96daecf65b6ea7aaaf9d2217f2c8f4e27a44e13800ee34ce2110620a1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2636098719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e88c818aa8954ae57e277c9730cdfa1dceee6b1cc34304b32f23f94a4ee916`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:47:04 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:50:03 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:50:05 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:10:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:10:40 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:10:41 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:11:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:11:16 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a6b8d8a4b8aea18e07888051dac03e88f4132fba08dca72e5795d9533dd3d`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67fec1bfee8619d88a924c4f9b9f4a04d2a0a1d199406157bb073b9f48d588`  
		Last Modified: Wed, 14 Apr 2021 13:07:33 GMT  
		Size: 134.1 MB (134133939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fe57ae793e79818d065737c8e995bb1b73296275794af222be695733711652`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.6 KB (1562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5134c3d8291dc3a52f7fad327cccf50377f2f362488fbcb8405addc74c0eedcf`  
		Last Modified: Wed, 14 Apr 2021 20:25:05 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d60772069c77cb2a80fec9f6e4d18084a4a919d4f776079dfee7903331331e7`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4716fdd15cdffc3b1aa557c81d58c2d0c343f9bfbfb501325b4cdc3bfeb426d9`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc11d2d339a72dd92f86f4fcc8e6fc299da2b6b381147f41dbd8d789e0c944e`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2909c1d8e32571506ce36cda43c7b113b299e280d6d7dfffafe5cd6284595348`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.7 MB (1712288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e56de156a63d8492bf70144c9e28ae975db36a6a57c54e734c96e20fb8bb13`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:436f2a16a677c719d951ddd10a1f475e81cc61b0726c7a4d5f76bdea16e3d215
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5982128974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1658b3cebc6cc5691856945858057a4e3925a991ead9db618b5058d55e445e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:50:19 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:54:08 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:54:10 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:11:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:11:24 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:11:25 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:11:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:12:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:13:01 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1388c10d71d4f1005ced63001aeb1392f019139011ddf961220ee27a412cbadb`  
		Last Modified: Wed, 14 Apr 2021 13:07:44 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913a59644a65d5f7183aa7bebce08c8b09d1f627c257105a7db7514919858b6e`  
		Last Modified: Wed, 14 Apr 2021 13:08:21 GMT  
		Size: 143.9 MB (143889855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b095a33aa8cc59c703b0a8f3b0bb53508123d89c531d6369de947b72b26f5`  
		Last Modified: Wed, 14 Apr 2021 13:07:46 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c7a21f93788806d3510b3cc8f7692b086c096861b42c218993697d04a890de`  
		Last Modified: Wed, 14 Apr 2021 20:25:25 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fbdf3acf4f09ad44474940358b0b044863361fee2bb201478a8b4b40cced75`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600e2fd01e09ce5bb623f7dbf3080c7127a8c2dc0b54422dee1525e75e6ae6de`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d594e3e36caa66775e5660018a80c02ef6bf4b16e626bdbca53a885634db4a29`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f5b24d29c79d20732eaf23dc495c89959ba869fbcb3bb88d35b42f38616a1`  
		Last Modified: Wed, 14 Apr 2021 20:25:24 GMT  
		Size: 7.0 MB (6976405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11b840b2827a9bb3da231a34e716b4fbd570dffa0b711f9fcbb7ff630c90052`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:388a8615423ce9d162146c4b22c552424c9ef7a58a27c091ae1cb3b3e85e3f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:3eb8fd03c47af4395bea3f6bcb98e8385f4634c7f513e7746421ae828d62c66f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119544759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dab7b132f437ff0879dfdef9940c90324e4d6a4c5af7de0c2b7b256d5ebf21b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:29:08 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:29:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:29:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:32:48 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:34:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:34:19 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:34:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:34:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:34:20 GMT
WORKDIR /go
# Thu, 15 Apr 2021 09:28:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 09:28:59 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 09:29:00 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 09:29:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 09:29:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 09:29:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 09:29:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b54d2d4342f88201f48db57cae1f7edbacae870ee13d7962f999edd7529a9`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5898d3d0f1f95fd666f764bf918c1656be6169868335cb63bc428a5ef47cf32`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2292415af71b71f5b5eae8c7426f41afef6af628b410acf0b9d036240addeeb`  
		Last Modified: Wed, 14 Apr 2021 21:37:07 GMT  
		Size: 106.8 MB (106825070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483424ea5e047556d6172c0273d0671d368d0e42448ee6eee213adf6f0f0e218`  
		Last Modified: Wed, 14 Apr 2021 21:36:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936094b3e444e93dce0400536b066def6153e8795892e63e44042e3507f71fa7`  
		Last Modified: Thu, 15 Apr 2021 09:29:37 GMT  
		Size: 8.3 MB (8326458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41aa4f492f90b4b9472fbfce9bf1b1f4f9dc08fb9d9ec92fb040160716042e0`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 1.3 MB (1311071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9495ef365ef431007d48d2a011656481c0dcfe85888f9dc8d8780a41db96f26`  
		Last Modified: Thu, 15 Apr 2021 09:29:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ca579a39dbe79f52268fdb5230c9a5ad7cfc115e540b515ecce7a557714b1711
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114723671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf78bfe4d146d0c0b28698b45888f4e663125f52bfb222cd1e7bf6e85248038`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:19:47 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:19:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:19:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:24 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 21:11:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 21:12:16 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 21:12:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 21:13:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 21:13:32 GMT
WORKDIR /go
# Thu, 15 Apr 2021 06:25:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 06:25:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 06:25:12 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 06:25:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 06:25:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 06:25:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 06:25:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c231c184d802a569805e44837dd1ea2cb0522bb03ca5763ef5ed9fae5896c`  
		Last Modified: Wed, 14 Apr 2021 21:15:05 GMT  
		Size: 281.0 KB (280982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8ca9e585b85be2e7ddaaf213e22bdb986eba4da2a8cc4d8b45f762752e17df`  
		Last Modified: Wed, 14 Apr 2021 21:15:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa237e1852b6dc6312c54835af4eedd49fc347da91eee2bd9a5cbdf3e4a09a74`  
		Last Modified: Wed, 14 Apr 2021 21:17:14 GMT  
		Size: 102.7 MB (102671404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfaf15ab73c5bd3fd51cf3ad7a986d94a84a0de33b0e2b421df3ece40813b6f`  
		Last Modified: Wed, 14 Apr 2021 21:16:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bceb981e039ba8e3426115768baf63e8372fc75250fbb6d6df522d9558b8abb8`  
		Last Modified: Thu, 15 Apr 2021 06:26:15 GMT  
		Size: 7.9 MB (7943726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec602f7edc3131a49dd0ab8bd4e7b207009dc592d13555e12296c433ef56919`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 1.2 MB (1221591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57d036d826077e94afba969b41b7bdc9d1ae0f266d04bc343350ff391e2fd75`  
		Last Modified: Thu, 15 Apr 2021 06:26:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:28ae48497c0b64592d20b21b122fe14268d4ce85a5e9ea9b5b583d5a58726cfb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113527342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15cf44fde7fa3b279efe2039c6fb0882edb4c49fdc0076fc26c90bdcec1b365`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:28:16 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:28:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:28:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:19:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 22:43:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 22:43:26 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 22:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 22:43:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 22:43:36 GMT
WORKDIR /go
# Thu, 15 Apr 2021 07:39:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 07:39:41 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 07:39:43 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 07:39:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 07:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 07:39:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 07:39:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a884c3a8500725e0f08f924091ec61ae3e3acee3b0ffe5839b06f874ee63dc08`  
		Last Modified: Wed, 14 Apr 2021 22:45:08 GMT  
		Size: 280.1 KB (280078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f87f08a98de1e7cb636267b626d4e644775ff7962ea1ff9b4813f740b89e67`  
		Last Modified: Wed, 14 Apr 2021 22:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c59f8b5aa025c1cb85f375b22cbc86c2892e311a5aad724e9af892abbefca31`  
		Last Modified: Wed, 14 Apr 2021 22:47:06 GMT  
		Size: 102.5 MB (102463090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146d2365c5f44423fcd2cd482e0d74d784c72e892e81c7d26dd1aa1a8bd3ab43`  
		Last Modified: Wed, 14 Apr 2021 22:46:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689b9c2e77675507509d87b28e5aa533b980296e5ffa8999fa8268863b5691b5`  
		Last Modified: Thu, 15 Apr 2021 07:40:47 GMT  
		Size: 7.2 MB (7154833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c64d502102e5ce2b6b103a14d9af56e06fa146e4eb76cf6423e58e5407b6475`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 1.2 MB (1219446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a490f0c5cdae283a0f25e3bc46079442ea559abaa3cf16c64a5a0cef30befc45`  
		Last Modified: Thu, 15 Apr 2021 07:40:46 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b89b93e92ffd9427041b5ed8850cc44f292b611e7dee55242ea02c6c3ccf2a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8d157b29403fa75da94e9701e2c3e3d065de48b910f8045b32619bdc25f1e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:09 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:46:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:46:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:54:59 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:58:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:58:21 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:58:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:58:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:58:41 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:44:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:44:05 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:44:06 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:44:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:44:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:44:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:44:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2150ab4b89a5dc832780f442998074db1582348dca0eb60d6b79b59df025f25f`  
		Last Modified: Wed, 14 Apr 2021 21:00:21 GMT  
		Size: 281.2 KB (281220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9d22c0ca7447b1a1b25889675e84f2ed68ecd519fdc513796712138820633b`  
		Last Modified: Wed, 14 Apr 2021 21:00:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cfb7326a4720568ee9867ad9f6dd4b796bcd9e899c6a27a3891589eae5cc06`  
		Last Modified: Wed, 14 Apr 2021 21:02:14 GMT  
		Size: 102.1 MB (102136232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a0cdf5ccbda3f4358749dfd4a03c520b2ca135a303988e74a5796796ccc30d`  
		Last Modified: Wed, 14 Apr 2021 21:01:48 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad8e65604482fa70f402e9fde824dec1ff3f257637f247fe6279c69757b9de6`  
		Last Modified: Thu, 15 Apr 2021 08:45:09 GMT  
		Size: 8.5 MB (8518404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1496bb71598cd42c2f92595b24f0aa7a34914fb6048c11499146f728964ddb`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 1.2 MB (1201555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1678712b911f6bb0ed8a67b615034fcec04e64bca853d43c39e3659d54e649`  
		Last Modified: Thu, 15 Apr 2021 08:45:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4d7764de3f8d29cbb22b2b973802bbf36aa89b6c1e6a11cf6934b2273b80e59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113988669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c777710e48b168e93b792b4171e667a5c16209c668b09dd54d442ad4ef1c55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 31 Mar 2021 18:56:11 GMT
ADD file:d51af61c5955c980d18387ab532110c3874f95a87768be84dfd1eeb3e701d3a4 in / 
# Wed, 31 Mar 2021 18:56:16 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 04:33:46 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 01 Apr 2021 04:33:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 04:33:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:18:36 GMT
ENV GOLANG_VERSION=1.15.11
# Fri, 02 Apr 2021 03:20:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 02 Apr 2021 03:20:38 GMT
ENV GOPATH=/go
# Fri, 02 Apr 2021 03:20:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Apr 2021 03:20:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 02 Apr 2021 03:21:02 GMT
WORKDIR /go
# Fri, 02 Apr 2021 05:03:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 02 Apr 2021 05:03:11 GMT
ENV XCADDY_VERSION=v0.1.8
# Fri, 02 Apr 2021 05:03:15 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 02 Apr 2021 05:03:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 02 Apr 2021 05:03:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 02 Apr 2021 05:03:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 02 Apr 2021 05:03:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6d4557865d9cec3513c1a5e744cb1073a563d464b8d546911289b9df9998f1b`  
		Last Modified: Wed, 31 Mar 2021 18:57:36 GMT  
		Size: 2.8 MB (2806070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128ce9f93b1dd5f42d7663646400f1307cddfad6a5361031e3a1ca8c46d90d2e`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 283.2 KB (283224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb52babc5b3ae7ccfca63bfc4092e7d57cbd51bc203af266e4fcb0169a6107`  
		Last Modified: Thu, 01 Apr 2021 04:44:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91ebeddf57ad09e8e1b3eb1e312be6a4484d88f8f970a7b241d759abe98e5f`  
		Last Modified: Fri, 02 Apr 2021 03:25:31 GMT  
		Size: 100.8 MB (100806744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac05f37b09f2517038025dd2d905a5d3ecbd9af697023fe05bc857ed48b8f455`  
		Last Modified: Fri, 02 Apr 2021 03:25:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e2e6a908474ce0f09d3cc2e30293784024f2a821c330690e753b01155c5346`  
		Last Modified: Fri, 02 Apr 2021 05:04:26 GMT  
		Size: 8.9 MB (8921423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b888e7962a16510b476660b91df0be664af7f16e7eb94288112b51bfd206995`  
		Last Modified: Fri, 02 Apr 2021 05:04:25 GMT  
		Size: 1.2 MB (1170492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ce4e5965570ab285f5e3be6ab2ca4cd6b618b344303a3e09cbb4c46fb2393f`  
		Last Modified: Fri, 02 Apr 2021 05:04:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:75a9876d6656c0b08c814240a013160e20a41c6a4bfe5939f9befb45ab7e277c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118429233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3dc1b085458cb773f526584cf4e59ebff486ad9b1f684021e37907fd83cb1d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:59 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:47:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:47:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:50:25 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 20:51:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.11.src.tar.gz'; 	sha256='f25b2441d4c76cf63cde94d59bab237cc33e8a2a139040d904c8630f46d061e5'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 14 Apr 2021 20:51:52 GMT
ENV GOPATH=/go
# Wed, 14 Apr 2021 20:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 20:51:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 14 Apr 2021 20:51:53 GMT
WORKDIR /go
# Thu, 15 Apr 2021 08:47:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 15 Apr 2021 08:47:02 GMT
ENV XCADDY_VERSION=v0.1.8
# Thu, 15 Apr 2021 08:47:03 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 15 Apr 2021 08:47:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Apr 2021 08:47:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='6760a7816d01da49cc6f0e8a476c3e7bd7d3778628b4ddd7edbb69b83fd1d9c086fa51e4195d928526d323f37a52b46a02a62f1ad63fdb511aeec41b83eff7a9' ;; 		armhf)   binArch='armv6'; checksum='9825e195c1abdca6f143d99feb667f8c15181b8dc67e18156c253708e47882cdc4cfffc32b3667f6bfdb2556410136ee11b3df7edca2a7de503f5a4871b0305e' ;; 		armv7)   binArch='armv7'; checksum='9d80d4d1e21135c55ab22a73ee8b45b94aa128c9ef2a95646fff76159ef0087be91641b805f5ea6aea6e949bb197cb051642c3cbf39431f080d70aec55c68854' ;; 		aarch64) binArch='arm64'; checksum='2de63a8305ef485d7cdf5f28f1ca2b68a1f16f051c53035466666d930074aa3be5d32fa69668435cd9dbc9dc84f6fd78307f92caeb4aa544d0032a66bd71514a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='a70446270c35da12ea214072b4f7f9a9d4b59c7ef391e6b2e72cf7a9dab5df1e9eb8d81abed066c5d5036d0a7f5730118ad3b4428df1e0d001b8faf228d368ed' ;; 		s390x)   binArch='s390x'; checksum='b1c72f77caa5bba89b30ef752dc88bd7796975a0a17298fbcc22ddd61ca9d7b1c7aca6b8b9aa231091aea122f9931022552ffe16fc84ebfb9ba936bf53d32367' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 15 Apr 2021 08:47:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 15 Apr 2021 08:47:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c45d0e43ef7a36e47dfc16916a076f7ba26b656842380c26207ad30f5c8b`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 281.3 KB (281343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f1645d6cbfccd2924337f37dc819e7edc27989ead8bc679441954a0e483c24`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3233df950b4b58e213bfc323437185867d0d54de06ac41e9e5c408ca83ecd5ca`  
		Last Modified: Wed, 14 Apr 2021 20:53:56 GMT  
		Size: 105.9 MB (105944122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3995327d2f868035d65ecb6b315f8595f43db3da3e10b19dbe964a66b6cfd746`  
		Last Modified: Wed, 14 Apr 2021 20:53:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04afa35fe1fde3bf4e11163aeea0b3f7c6084de121d5f071291ee325ac535f06`  
		Last Modified: Thu, 15 Apr 2021 08:47:53 GMT  
		Size: 8.4 MB (8370192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81b8ec43677381485cbedd3fa6dc24863c5d8f04d8700720662cc1293d70ef`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 1.3 MB (1264434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf872018e54c322f4f460c7e7816a9ae61c2a3c07f73d7f4324c18a21f6ccdfb`  
		Last Modified: Thu, 15 Apr 2021 08:47:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:0ee0dd2e13c7c2d8b1a3514be4c8a71a5da92f756386f549bdd51c0bd62700c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:5d074fc96daecf65b6ea7aaaf9d2217f2c8f4e27a44e13800ee34ce2110620a1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2636098719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e88c818aa8954ae57e277c9730cdfa1dceee6b1cc34304b32f23f94a4ee916`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:47:04 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:50:03 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:50:05 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:10:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:10:40 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:10:41 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:11:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:11:16 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a6b8d8a4b8aea18e07888051dac03e88f4132fba08dca72e5795d9533dd3d`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67fec1bfee8619d88a924c4f9b9f4a04d2a0a1d199406157bb073b9f48d588`  
		Last Modified: Wed, 14 Apr 2021 13:07:33 GMT  
		Size: 134.1 MB (134133939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fe57ae793e79818d065737c8e995bb1b73296275794af222be695733711652`  
		Last Modified: Wed, 14 Apr 2021 13:04:59 GMT  
		Size: 1.6 KB (1562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5134c3d8291dc3a52f7fad327cccf50377f2f362488fbcb8405addc74c0eedcf`  
		Last Modified: Wed, 14 Apr 2021 20:25:05 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d60772069c77cb2a80fec9f6e4d18084a4a919d4f776079dfee7903331331e7`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4716fdd15cdffc3b1aa557c81d58c2d0c343f9bfbfb501325b4cdc3bfeb426d9`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc11d2d339a72dd92f86f4fcc8e6fc299da2b6b381147f41dbd8d789e0c944e`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2909c1d8e32571506ce36cda43c7b113b299e280d6d7dfffafe5cd6284595348`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.7 MB (1712288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e56de156a63d8492bf70144c9e28ae975db36a6a57c54e734c96e20fb8bb13`  
		Last Modified: Wed, 14 Apr 2021 20:25:02 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:80d881fa828e30f1c7d44ae2d3bebe98ef9185d4e43e597ac5205ba32ad13c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:436f2a16a677c719d951ddd10a1f475e81cc61b0726c7a4d5f76bdea16e3d215
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5982128974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1658b3cebc6cc5691856945858057a4e3925a991ead9db618b5058d55e445e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 12:50:19 GMT
ENV GOLANG_VERSION=1.15.11
# Wed, 14 Apr 2021 12:54:08 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56f63de17cd739287de6d9f3cfdad3b781ad3e4a18aae20ece994ee97c1819fd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:54:10 GMT
WORKDIR C:\gopath
# Wed, 14 Apr 2021 20:11:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:11:24 GMT
ENV XCADDY_VERSION=v0.1.8
# Wed, 14 Apr 2021 20:11:25 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:11:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Apr 2021 20:12:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.8/xcaddy_0.1.8_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('ccbc594da07adff41098959a78efaaee42fca4e5feb7806661d00841229b20ff1c47fed024c7a84e8554d3e8be3f162d3750e5e8347d6a230c496d4b133213e8')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Apr 2021 20:13:01 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1388c10d71d4f1005ced63001aeb1392f019139011ddf961220ee27a412cbadb`  
		Last Modified: Wed, 14 Apr 2021 13:07:44 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913a59644a65d5f7183aa7bebce08c8b09d1f627c257105a7db7514919858b6e`  
		Last Modified: Wed, 14 Apr 2021 13:08:21 GMT  
		Size: 143.9 MB (143889855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b095a33aa8cc59c703b0a8f3b0bb53508123d89c531d6369de947b72b26f5`  
		Last Modified: Wed, 14 Apr 2021 13:07:46 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c7a21f93788806d3510b3cc8f7692b086c096861b42c218993697d04a890de`  
		Last Modified: Wed, 14 Apr 2021 20:25:25 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fbdf3acf4f09ad44474940358b0b044863361fee2bb201478a8b4b40cced75`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600e2fd01e09ce5bb623f7dbf3080c7127a8c2dc0b54422dee1525e75e6ae6de`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d594e3e36caa66775e5660018a80c02ef6bf4b16e626bdbca53a885634db4a29`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f5b24d29c79d20732eaf23dc495c89959ba869fbcb3bb88d35b42f38616a1`  
		Last Modified: Wed, 14 Apr 2021 20:25:24 GMT  
		Size: 7.0 MB (6976405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11b840b2827a9bb3da231a34e716b4fbd570dffa0b711f9fcbb7ff630c90052`  
		Last Modified: Wed, 14 Apr 2021 20:25:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:88fc125055b8c4dafe67a48219fd3a89c0a472aa254d2835b2e298b93493b28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:6fbf52298c46c55c572670b5395ecaee5d399338003c9bb4e4abed875c542f4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395cc3713b2ca5574a9b4aafc468a1533d16582efe47dcab74ed547540d698a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:10:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:10:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:10:49 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:10:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:10:53 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:10:54 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:10:55 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:56 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:10:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a0cd9cca5be9b30bbc70611052d1456502e1f338ce4b14946233b21cd6a9a`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 300.0 KB (300016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5666523658a43fbbdff6b8fca498a988f4dcecc3ce027f1701414658c21d4ea`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097228407f13a161f68b188b0a4f255855b64d84e7b076745a744d5aa7ed8cf`  
		Last Modified: Wed, 14 Apr 2021 20:11:49 GMT  
		Size: 11.6 MB (11622383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40682d93cc09b4592a1b9c08d48d0a956b5eef4f123d80d1a12942482edb6aab`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0df9df9725cab39fe073887c98b54bf7bf1c96b3ed0e23916737c7c4877576c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13856181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce1c33ce4509195edc1c67d2dcd15c6c5fc0b35cec2e90714ec3007739600eb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:45:19 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:45:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:45:36 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:45:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:46:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:46:04 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:46:05 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:46:07 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:46:08 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:46:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:46:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:46:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:46:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:46:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:46:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:46:22 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:46:23 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:46:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b83e8a6ea044be2a9e3c87c5fdc047ce9a52d1a64e48f8330d9a19002ecffe1`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 300.1 KB (300117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9949bdfbb1d296dd158f8c2bb959f96c8da162a0d579f68fa3f5a4af58bed5b`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c5cc316af29a89f9a1d4e279b5d1bb964095a15795647d013f40921bc808c3`  
		Last Modified: Wed, 14 Apr 2021 19:47:54 GMT  
		Size: 10.9 MB (10944831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6670cc680ce5e5d9a0adfc380fe4a89ac2a2dcef5a7adeb874967a356e6742`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a41623f53d582c8b503ae859f6ae98c7c0695eddb11bdbf8514b9b914955c3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13639723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b837694902a1a259a4915444feda59d895ed37ffbef66b8518b9a884f029c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:39:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:39:34 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:39:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:39:43 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:39:45 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:39:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:39:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:39:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:39:56 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:39:57 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:39:58 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:39:59 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239ad5e698454501b0de011bffea35a660806a0b85a6141776581e3a98bc467`  
		Last Modified: Wed, 14 Apr 2021 19:41:24 GMT  
		Size: 299.2 KB (299210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0460b038be93717158ad9cdb6f83768b7129eaf4fcaef8620adc7509d0e5fe`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0905d1ca8c4f74966ae8a7b5ebe8fdb33854c4a759d543d767dd9a0add81f155`  
		Last Modified: Wed, 14 Apr 2021 19:41:29 GMT  
		Size: 10.9 MB (10925348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02da274f552e184a7fa5527990e666d77c70e3715a0d96b7588e7433b3022a`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:789a609d1ac52d0bed8718bab07beff0633df8333c8f88a4a54ccc6fa14bfb1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13616003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fab65bcfd86f1922cd2ec38aa336d5c219f99ed0d0878dede9732c770b2113`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:59:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 18:59:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 18:59:56 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:00:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:00:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:00:06 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:00:07 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:00:08 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:00:09 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:00:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:00:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:00:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:00:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:00:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:00:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:00:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:00:22 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:00:23 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:00:25 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:00:26 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:00:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96638d6a34d0588d1723cae433a6176b83e4bec10cb3a37ffac1891313dd144`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 300.4 KB (300352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e448c61e8710f135f93f0f19db0e1e20005299e4e28dfcbba2fc048075b11`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955bb49759c02742bb3fe501b864201c3b2a349f8253b73d7114ba39a816ac02`  
		Last Modified: Wed, 14 Apr 2021 19:01:54 GMT  
		Size: 10.6 MB (10598977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639f923159f69301bb290369ef4804ec8ef52d3d159d531976474f8d34d3dc54`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:f551e1db7910e2d5235d303760aff5b514fc6e8b49d8d67d434bb23c40ac25db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13356454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bd235f46e537404cdab42c3dfb3d0058f97ed5d7984f2e71ad8734adcc6a8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:09:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:09:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 22:09:24 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 22:09:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:09:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:09:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:10:01 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:10:06 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:10:15 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:10:22 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 22:10:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:10:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:10:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:10:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:11:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:11:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:11:20 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:11:27 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:11:35 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:11:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93dd31358a6e859a05bb506b946720f02c7ec7969776d811b20eaaa84508cd7`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 302.3 KB (302339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8077b8c9cca163d9a34281a866cf5fe991ff8c160ebd1ab1b617c6b722ec690`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55884816b8eca8150db9473989410e372c69c5431deb51a6cacd029895cf3dd6`  
		Last Modified: Wed, 14 Apr 2021 22:15:43 GMT  
		Size: 10.2 MB (10241380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efee06e0a650ff5f146fc54a695d4bf2b44e19da18120fdc494982d52cdd62`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:68aaf625a22bff4e71edf895129baa2d562765c24ac81a5c68aff2995ebf89c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14146947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd454f0dfa64ee1a952f9ed74a3f3bda3688a9565f062c3ea37e48b54eb210`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:21 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:07:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:07:22 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:07:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:07:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:07:27 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:07:27 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:07:30 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:07:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dab58470b754d248933aa56b48394e3ee4db4561d430d23ea378f0371ca59cb`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 300.5 KB (300471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd514b608428ea44dae7dc67e641a276593e7715178d86d7702153521de849d7`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a437814dab55b178c71f55598a70d0b532b3f645bdeb43e89244a6ebcde01446`  
		Last Modified: Wed, 14 Apr 2021 20:08:18 GMT  
		Size: 11.3 MB (11272061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412be9af105c69ee35fec76e8c0dbde8c8ba61c774b7d354e9c9fc8f538e8155`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:6a199f80cee0da0b39f4deffc53efac536c60672f4d8d26887f8f8ec194da3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:89f75ffc06d5f7a7cc6d37f38c9198d869993fa7426542d14c1a8bfdbb467694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:a42a67f914fd976a839e8c725f15fec79415b331ffeaa3972e7bff363bec4ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
