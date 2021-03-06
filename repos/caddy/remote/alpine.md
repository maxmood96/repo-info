## `caddy:alpine`

```console
$ docker pull caddy@sha256:30cf6a3da8365c2d9344adfc42b33a5b6e01dc4943c75b0132d556d12bd5f995
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
$ docker pull caddy@sha256:d0b43ebda8fd47409cec98d5f3c3b4c60bfc6bca35338313c002dc64c2283055
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14727887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88588539bb905b66ad7f78f35b915f2daf56ec49fd5f20019793e9dbd9747497`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 08:10:50 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 06 Mar 2021 08:10:52 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Sat, 06 Mar 2021 08:10:52 GMT
ENV CADDY_VERSION=v2.3.0
# Sat, 06 Mar 2021 08:10:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 06 Mar 2021 08:10:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 06 Mar 2021 08:10:56 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 06 Mar 2021 08:10:56 GMT
ENV XDG_DATA_HOME=/data
# Sat, 06 Mar 2021 08:10:57 GMT
VOLUME [/config]
# Sat, 06 Mar 2021 08:10:57 GMT
VOLUME [/data]
# Sat, 06 Mar 2021 08:10:57 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Sat, 06 Mar 2021 08:10:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 06 Mar 2021 08:10:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 06 Mar 2021 08:10:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 06 Mar 2021 08:10:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 06 Mar 2021 08:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 06 Mar 2021 08:10:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 06 Mar 2021 08:10:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 06 Mar 2021 08:10:59 GMT
EXPOSE 80
# Sat, 06 Mar 2021 08:10:59 GMT
EXPOSE 443
# Sat, 06 Mar 2021 08:10:59 GMT
EXPOSE 2019
# Sat, 06 Mar 2021 08:10:59 GMT
WORKDIR /srv
# Sat, 06 Mar 2021 08:10:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6296b24b4efd312d2a5e0a24a29635cf8aa098c9c3e50ca6566741a54b2794b`  
		Last Modified: Sat, 06 Mar 2021 08:11:50 GMT  
		Size: 300.0 KB (300027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd0836949366398b595edf3fde04aff8f2a0c0f4c1ea35372e070f4bf27ce59`  
		Last Modified: Sat, 06 Mar 2021 08:11:50 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7383a05b49b6f752da622ff9a170dccd483a982060cc06a6be10d6312d32a0`  
		Last Modified: Sat, 06 Mar 2021 08:11:52 GMT  
		Size: 11.6 MB (11622385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84701a0726354caf82c1c4be1f558173acf8b6604f7b4118a1097b98424256bd`  
		Last Modified: Sat, 06 Mar 2021 08:11:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:2c03423186b55d3813eb09d04dc53106635be68cfb5969c12109e08cff9aa2cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569b44d4318ddaf5248442e91df11b525d9ccaf230b7efd78c6ce6ef08281ebc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:34 GMT
ADD file:8bbb59eeaad0cbcf11559bc6e2b4492aadf6822d1935ed50c710f8bed858b7b5 in / 
# Wed, 24 Feb 2021 20:50:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:07:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 24 Feb 2021 21:07:11 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 24 Feb 2021 21:07:11 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 24 Feb 2021 21:07:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 24 Feb 2021 21:07:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:07:18 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 24 Feb 2021 21:07:19 GMT
ENV XDG_DATA_HOME=/data
# Wed, 24 Feb 2021 21:07:20 GMT
VOLUME [/config]
# Wed, 24 Feb 2021 21:07:20 GMT
VOLUME [/data]
# Wed, 24 Feb 2021 21:07:21 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 24 Feb 2021 21:07:22 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 24 Feb 2021 21:07:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 24 Feb 2021 21:07:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 24 Feb 2021 21:07:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 24 Feb 2021 21:07:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 24 Feb 2021 21:07:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 24 Feb 2021 21:07:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 24 Feb 2021 21:07:26 GMT
EXPOSE 80
# Wed, 24 Feb 2021 21:07:27 GMT
EXPOSE 443
# Wed, 24 Feb 2021 21:07:28 GMT
EXPOSE 2019
# Wed, 24 Feb 2021 21:07:28 GMT
WORKDIR /srv
# Wed, 24 Feb 2021 21:07:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:55242616b0494f68f44470d864da746cd2a8f8f2d1ffca698114de64032247ef`  
		Last Modified: Wed, 24 Feb 2021 20:51:17 GMT  
		Size: 2.6 MB (2604518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9d7c4e3e67f9f36b119476dce4a4951c76aca8f9848b7cc600797ce9a5dbb5`  
		Last Modified: Wed, 24 Feb 2021 21:08:09 GMT  
		Size: 300.1 KB (300107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0438df6797a38cba7f30dd40d58d68e90cf6f6a4ece0a3352142ef610796d1`  
		Last Modified: Wed, 24 Feb 2021 21:08:09 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa1886901d622dcb0b11ff563e6eca542fec29b60ae60c1bf82c8d7271fbcb8`  
		Last Modified: Wed, 24 Feb 2021 21:08:13 GMT  
		Size: 10.9 MB (10944831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f6d93c8b87b0adc5fdfbfb465ceb4e8c5ccbfe7e75288a0b6247b287bd1d19`  
		Last Modified: Wed, 24 Feb 2021 21:08:09 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:35efa62036c16d5ac4716ce79b11c0505538236542b982ce31e580044712c961
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13638536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e584e1be15b38bc7eddfd01bedf8038c9b6eb1d20a21df121376bc0878fa2b5e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Feb 2021 21:03:35 GMT
ADD file:2632f48dd643f8927da2b1af8365b3edb484bd6b7d9fee4009e69f6cf3310e91 in / 
# Wed, 24 Feb 2021 21:03:36 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:20:21 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 24 Feb 2021 21:20:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 24 Feb 2021 21:20:25 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 24 Feb 2021 21:20:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 24 Feb 2021 21:20:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:20:31 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 24 Feb 2021 21:20:31 GMT
ENV XDG_DATA_HOME=/data
# Wed, 24 Feb 2021 21:20:32 GMT
VOLUME [/config]
# Wed, 24 Feb 2021 21:20:33 GMT
VOLUME [/data]
# Wed, 24 Feb 2021 21:20:34 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 24 Feb 2021 21:20:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 24 Feb 2021 21:20:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 24 Feb 2021 21:20:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 24 Feb 2021 21:20:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 24 Feb 2021 21:20:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 24 Feb 2021 21:20:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 24 Feb 2021 21:20:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 24 Feb 2021 21:20:39 GMT
EXPOSE 80
# Wed, 24 Feb 2021 21:20:40 GMT
EXPOSE 443
# Wed, 24 Feb 2021 21:20:41 GMT
EXPOSE 2019
# Wed, 24 Feb 2021 21:20:41 GMT
WORKDIR /srv
# Wed, 24 Feb 2021 21:20:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8e85c7428c31ea48b47424ca0e4663106c54591c83545d32b66a77093f90ffd0`  
		Last Modified: Wed, 24 Feb 2021 21:04:23 GMT  
		Size: 2.4 MB (2408004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38341eca332cf74b9be3ce81ca1d45dfb58d85d6d26b7e95c316e6c9bb29ee72`  
		Last Modified: Wed, 24 Feb 2021 21:21:20 GMT  
		Size: 299.2 KB (299205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dc65ce8d47b334515d1e1114419a952c7a20fde643e2cb7d7fba90886eb905`  
		Last Modified: Wed, 24 Feb 2021 21:21:20 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dac8b9094b9d9fb88438fba0a9603978bb1779e919ca8adf8673ef932f74e5`  
		Last Modified: Wed, 24 Feb 2021 21:21:23 GMT  
		Size: 10.9 MB (10925347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f114ebf580e52effa6a3b734370fc33000e5a7439f0b0b2b275ffaca7483dd32`  
		Last Modified: Wed, 24 Feb 2021 21:21:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9629cb7ae3d67bb1da05e2a4fa565c7549f1d0df99f27e50987ad0414fa275a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13615189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0888c16cdeddffbcaf6f274289f92000cb7e408a60c2788e1cecce57fb4f54d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:33:39 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 24 Feb 2021 21:33:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 24 Feb 2021 21:33:42 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 24 Feb 2021 21:33:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 24 Feb 2021 21:33:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:33:48 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 24 Feb 2021 21:33:49 GMT
ENV XDG_DATA_HOME=/data
# Wed, 24 Feb 2021 21:33:50 GMT
VOLUME [/config]
# Wed, 24 Feb 2021 21:33:50 GMT
VOLUME [/data]
# Wed, 24 Feb 2021 21:33:51 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 24 Feb 2021 21:33:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 24 Feb 2021 21:33:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 24 Feb 2021 21:33:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 24 Feb 2021 21:33:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 24 Feb 2021 21:33:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 24 Feb 2021 21:33:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 24 Feb 2021 21:33:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 24 Feb 2021 21:33:57 GMT
EXPOSE 80
# Wed, 24 Feb 2021 21:33:57 GMT
EXPOSE 443
# Wed, 24 Feb 2021 21:33:58 GMT
EXPOSE 2019
# Wed, 24 Feb 2021 21:33:59 GMT
WORKDIR /srv
# Wed, 24 Feb 2021 21:34:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e93c560f04d39148af03b91ee7707d8a25136794128fdc0eb1a28ee5a9c7ec5`  
		Last Modified: Wed, 24 Feb 2021 21:34:44 GMT  
		Size: 300.4 KB (300351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bb894d60771907a615f58e2c0b5873da52637bf52500990e34621581a232d7`  
		Last Modified: Wed, 24 Feb 2021 21:34:44 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c61561fb1545eb44bb540b09bf7ce497aa3618f51b8dd8013e161cbe6b595d`  
		Last Modified: Wed, 24 Feb 2021 21:34:44 GMT  
		Size: 10.6 MB (10598977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9572d97783fa5ecc238f39ccba3a47e00bbef6ee3ac8db0ad07989b7f65fac81`  
		Last Modified: Wed, 24 Feb 2021 21:34:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:835954456f4b23bc0438b0423cfb25b19d1f184d85c44e7d50483c98c1bdb237
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13355613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f32f89e24ae18bc58ff2f9474e23a0240dcf374e6f2ff1f6f01dbde7895883b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Feb 2021 20:45:10 GMT
ADD file:90df4b3d767cd67ff62e490ca0a7d69bae532cf3fa6f8971a0d2c1b27fb4bdd1 in / 
# Wed, 24 Feb 2021 20:45:16 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:02:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 24 Feb 2021 21:02:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 24 Feb 2021 21:02:42 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 24 Feb 2021 21:02:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 24 Feb 2021 21:03:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:03:16 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 24 Feb 2021 21:03:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 24 Feb 2021 21:03:28 GMT
VOLUME [/config]
# Wed, 24 Feb 2021 21:03:33 GMT
VOLUME [/data]
# Wed, 24 Feb 2021 21:03:37 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 24 Feb 2021 21:03:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 24 Feb 2021 21:03:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 24 Feb 2021 21:03:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 24 Feb 2021 21:03:57 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 24 Feb 2021 21:04:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 24 Feb 2021 21:04:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 24 Feb 2021 21:04:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 24 Feb 2021 21:04:13 GMT
EXPOSE 80
# Wed, 24 Feb 2021 21:04:17 GMT
EXPOSE 443
# Wed, 24 Feb 2021 21:04:22 GMT
EXPOSE 2019
# Wed, 24 Feb 2021 21:04:28 GMT
WORKDIR /srv
# Wed, 24 Feb 2021 21:04:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f446c8f22d4a7a7520099080f73ffa6f455358a840b542fb2ad15c0032adeca`  
		Last Modified: Wed, 24 Feb 2021 20:46:19 GMT  
		Size: 2.8 MB (2805893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9864d4f9ffa98b896ad863ec705c2a2bce2aa8691403eecce7790d467de7e89`  
		Last Modified: Wed, 24 Feb 2021 21:05:09 GMT  
		Size: 302.3 KB (302341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72b4f216ba67dc77214d3ec8d53e95b9f4a7989eb80b52621fcf35941362dc`  
		Last Modified: Wed, 24 Feb 2021 21:05:08 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798bd52028343039b1f04dfc295f0a8c69da2291e8821a937274bcab1d94e2c5`  
		Last Modified: Wed, 24 Feb 2021 21:05:12 GMT  
		Size: 10.2 MB (10241391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bf4197b2f1cc35b12da368fd4455bab68c9d6034ce3d778ae2d146d0b111ec`  
		Last Modified: Wed, 24 Feb 2021 21:05:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:247ebfeff707410bb47d0a0501aee685d43129a4fab344f361ca1430c28a4058
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14145843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9eef5ad7357ccba137393d95be15feb69c0fb5bf08d5a63bdd1d15f0a957a92`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Feb 2021 20:42:00 GMT
ADD file:ad5b3d24d5412d341e932d4497614d564c9c413984feaf8542113d6674b34b53 in / 
# Wed, 24 Feb 2021 20:42:01 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:19:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 24 Feb 2021 21:19:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 24 Feb 2021 21:19:19 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 24 Feb 2021 21:19:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 24 Feb 2021 21:19:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:19:29 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 24 Feb 2021 21:19:30 GMT
ENV XDG_DATA_HOME=/data
# Wed, 24 Feb 2021 21:19:31 GMT
VOLUME [/config]
# Wed, 24 Feb 2021 21:19:31 GMT
VOLUME [/data]
# Wed, 24 Feb 2021 21:19:32 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 24 Feb 2021 21:19:33 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 24 Feb 2021 21:19:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 24 Feb 2021 21:19:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 24 Feb 2021 21:19:35 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 24 Feb 2021 21:19:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 24 Feb 2021 21:19:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 24 Feb 2021 21:19:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 24 Feb 2021 21:19:37 GMT
EXPOSE 80
# Wed, 24 Feb 2021 21:19:38 GMT
EXPOSE 443
# Wed, 24 Feb 2021 21:19:39 GMT
EXPOSE 2019
# Wed, 24 Feb 2021 21:19:40 GMT
WORKDIR /srv
# Wed, 24 Feb 2021 21:19:40 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:84a604a54099b51a6c81db20dff8dc298ec82555e772be84328b067d3f35a93e`  
		Last Modified: Wed, 24 Feb 2021 20:42:40 GMT  
		Size: 2.6 MB (2567318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866813d62eb8e73b5cfc9e73e48928d678fcad6123ca0697fdc6ff6faf0c91e`  
		Last Modified: Wed, 24 Feb 2021 21:20:15 GMT  
		Size: 300.5 KB (300478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8052626100230d16d27888d060e65aaf770add1ae10f69a8f03a903d274ec2`  
		Last Modified: Wed, 24 Feb 2021 21:20:15 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6a465134a658869ad61a0ea92cf2775ffd82e4cd1d0e2246f24abd0ac95613`  
		Last Modified: Wed, 24 Feb 2021 21:20:17 GMT  
		Size: 11.3 MB (11272060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fffed8a5a7c6c9efd387b3b851eb42ba3b176b5614156a8f2b5ca6dbfe56e7`  
		Last Modified: Wed, 24 Feb 2021 21:20:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
