## `caddy:alpine`

```console
$ docker pull caddy@sha256:99d811b358ec3f3bc45a430c6358fc7af75423cb047012518fdd1708f5b2dc71
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
$ docker pull caddy@sha256:cbb1e84121ca20ac7fbc3cf8a9e04f4ee4979f33352ecfb883b56984fccf2cd7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14727284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c73dc9258a8ebf0244d67701a655c1fc655cbfda642ab615e06b1a6039d5b2e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 12:34:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Dec 2020 12:35:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Mon, 04 Jan 2021 18:19:40 GMT
ENV CADDY_VERSION=v2.3.0
# Mon, 04 Jan 2021 18:19:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 04 Jan 2021 18:19:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Jan 2021 18:19:43 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 04 Jan 2021 18:19:43 GMT
ENV XDG_DATA_HOME=/data
# Mon, 04 Jan 2021 18:19:43 GMT
VOLUME [/config]
# Mon, 04 Jan 2021 18:19:43 GMT
VOLUME [/data]
# Mon, 04 Jan 2021 18:19:43 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Mon, 04 Jan 2021 18:19:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 04 Jan 2021 18:19:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 04 Jan 2021 18:19:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 04 Jan 2021 18:19:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 04 Jan 2021 18:19:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 04 Jan 2021 18:19:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 04 Jan 2021 18:19:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 04 Jan 2021 18:19:45 GMT
EXPOSE 80
# Mon, 04 Jan 2021 18:19:45 GMT
EXPOSE 443
# Mon, 04 Jan 2021 18:19:45 GMT
EXPOSE 2019
# Mon, 04 Jan 2021 18:19:46 GMT
WORKDIR /srv
# Mon, 04 Jan 2021 18:19:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afadb5ee6ea5f6d507d8b77b8ba0ace43c1db0a163815f209e62439af325d6c`  
		Last Modified: Thu, 17 Dec 2020 12:36:36 GMT  
		Size: 300.0 KB (299951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e5593f16cf4f0a44a49cdf9021457e530ba060d4610405b1d37004ab643d79`  
		Last Modified: Thu, 17 Dec 2020 12:36:45 GMT  
		Size: 5.8 KB (5758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fe9aaa681bd550de2455df437d9c9a9e24005e810e7d5a01c35d263fa2aa46`  
		Last Modified: Mon, 04 Jan 2021 18:20:23 GMT  
		Size: 11.6 MB (11622354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f3b11169846dc2fcfacfbcaae13fcc50c8b72dc70b6bc9c4cfd9f156a37c4c`  
		Last Modified: Mon, 04 Jan 2021 18:20:21 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:b11903d75dc786cc7a333dcc8eb86432e12286a27596ba9a13de8ce6a16bbe4e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f2d0ff6672d884939bbd0e7ae29c28c4a54054bfb0132b16a6fd7144ccf4d4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:57:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Dec 2020 00:58:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Mon, 04 Jan 2021 18:49:38 GMT
ENV CADDY_VERSION=v2.3.0
# Mon, 04 Jan 2021 18:49:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 04 Jan 2021 18:49:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Jan 2021 18:49:44 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 04 Jan 2021 18:49:45 GMT
ENV XDG_DATA_HOME=/data
# Mon, 04 Jan 2021 18:49:45 GMT
VOLUME [/config]
# Mon, 04 Jan 2021 18:49:46 GMT
VOLUME [/data]
# Mon, 04 Jan 2021 18:49:47 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Mon, 04 Jan 2021 18:49:47 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 04 Jan 2021 18:49:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 04 Jan 2021 18:49:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 04 Jan 2021 18:49:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 04 Jan 2021 18:49:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 04 Jan 2021 18:49:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 04 Jan 2021 18:49:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 04 Jan 2021 18:49:51 GMT
EXPOSE 80
# Mon, 04 Jan 2021 18:49:52 GMT
EXPOSE 443
# Mon, 04 Jan 2021 18:49:52 GMT
EXPOSE 2019
# Mon, 04 Jan 2021 18:49:53 GMT
WORKDIR /srv
# Mon, 04 Jan 2021 18:49:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab316ae645fb129ec71432847f46832070abbd380444d7a049031cbef03c39`  
		Last Modified: Thu, 17 Dec 2020 00:59:38 GMT  
		Size: 300.1 KB (300099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c408732dcfb31f73b6a82942aa3e9ab50640eaeb49c175dcfddab4b07f0e790`  
		Last Modified: Thu, 17 Dec 2020 00:59:51 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7493ce1c2e0e02619db2817c3da32453658bbca2b087c8d73cf9c8eae72e5926`  
		Last Modified: Mon, 04 Jan 2021 18:50:38 GMT  
		Size: 10.9 MB (10944839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a640f55dfe60d817bb1c48cf163e52c3c42b843b7aa9976d573ac5b4bb322a04`  
		Last Modified: Mon, 04 Jan 2021 18:50:34 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8d7dd8d7f22f669d44669e643d61092c90ec7c1bcd4704e119d72715dc4b7de1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13638064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8ff470d547b26a0bf496261541723024fa700eb9d162dad5eba091a1320ce5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:02:07 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Dec 2020 01:02:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Mon, 04 Jan 2021 18:57:42 GMT
ENV CADDY_VERSION=v2.3.0
# Mon, 04 Jan 2021 18:57:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 04 Jan 2021 18:57:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Jan 2021 18:57:48 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 04 Jan 2021 18:57:49 GMT
ENV XDG_DATA_HOME=/data
# Mon, 04 Jan 2021 18:57:49 GMT
VOLUME [/config]
# Mon, 04 Jan 2021 18:57:50 GMT
VOLUME [/data]
# Mon, 04 Jan 2021 18:57:51 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Mon, 04 Jan 2021 18:57:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 04 Jan 2021 18:57:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 04 Jan 2021 18:57:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 04 Jan 2021 18:57:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 04 Jan 2021 18:57:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 04 Jan 2021 18:57:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 04 Jan 2021 18:57:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 04 Jan 2021 18:57:56 GMT
EXPOSE 80
# Mon, 04 Jan 2021 18:57:56 GMT
EXPOSE 443
# Mon, 04 Jan 2021 18:57:57 GMT
EXPOSE 2019
# Mon, 04 Jan 2021 18:57:58 GMT
WORKDIR /srv
# Mon, 04 Jan 2021 18:57:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e409aee3f1c32dd7aeea094975a27bd66a5c78389115618ff162028b950dd4b2`  
		Last Modified: Thu, 17 Dec 2020 01:04:59 GMT  
		Size: 299.2 KB (299192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1d150f546c9b585983f5e6390aa4e292e940deda5ca6eafab23f7eccd86e1f`  
		Last Modified: Thu, 17 Dec 2020 01:05:12 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d1178be4a6bd4aee0a16e25358732f4deac6a84f6614bd4d5a9d242ac9068d`  
		Last Modified: Mon, 04 Jan 2021 18:58:43 GMT  
		Size: 10.9 MB (10925337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb438ac85eaa28804b9de2f3e230fe52916ba5b81a38b03c514f2dbe9282c679`  
		Last Modified: Mon, 04 Jan 2021 18:58:39 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:93f5ca2902036950ab4ab8a22f4d74f36bce55feee9b7e0e797396e2d07f4df4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13614354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9774262cda02b94b5c9cc6bfc57d947819c3a0f1e85aacb278c6e91ddd7850`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:32:45 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Dec 2020 00:33:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Mon, 04 Jan 2021 18:39:58 GMT
ENV CADDY_VERSION=v2.3.0
# Mon, 04 Jan 2021 18:40:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 04 Jan 2021 18:40:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Jan 2021 18:40:03 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 04 Jan 2021 18:40:04 GMT
ENV XDG_DATA_HOME=/data
# Mon, 04 Jan 2021 18:40:05 GMT
VOLUME [/config]
# Mon, 04 Jan 2021 18:40:05 GMT
VOLUME [/data]
# Mon, 04 Jan 2021 18:40:06 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Mon, 04 Jan 2021 18:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 04 Jan 2021 18:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 04 Jan 2021 18:40:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 04 Jan 2021 18:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 04 Jan 2021 18:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 04 Jan 2021 18:40:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 04 Jan 2021 18:40:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 04 Jan 2021 18:40:17 GMT
EXPOSE 80
# Mon, 04 Jan 2021 18:40:18 GMT
EXPOSE 443
# Mon, 04 Jan 2021 18:40:19 GMT
EXPOSE 2019
# Mon, 04 Jan 2021 18:40:19 GMT
WORKDIR /srv
# Mon, 04 Jan 2021 18:40:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e6b1f8553a8382b04fce0860980a988a45e1e4efa692cd394306560d4d8352`  
		Last Modified: Thu, 17 Dec 2020 00:35:31 GMT  
		Size: 300.3 KB (300344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e695d7a94fe7f9e9c0dd063d219b5498420a85648620408166c2eba6a1fc81f`  
		Last Modified: Thu, 17 Dec 2020 00:35:41 GMT  
		Size: 5.8 KB (5825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48312421be65c130b3524264024f10c7774e9eab1b9cf370a6c7022753927567`  
		Last Modified: Mon, 04 Jan 2021 18:41:12 GMT  
		Size: 10.6 MB (10598984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332c70787e2588f66eeb0b6abd933d1f004e4f0357a5618092fdb36f9e88913f`  
		Last Modified: Mon, 04 Jan 2021 18:41:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:1be56543a90159f9a8bd5a83094c762bda8baef783604503316fcafbc5467c09
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13354933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b014a3125a542b761c87a24c6c1c5f71f964b4414c310af9ce20822717a8e2ba`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Dec 2020 00:20:42 GMT
ADD file:0a38c9b4955f8faa79627c166fca80ef342e443a16ce2925a30eeae317bbd786 in / 
# Thu, 17 Dec 2020 00:20:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 02:26:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Dec 2020 02:29:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Mon, 04 Jan 2021 18:17:34 GMT
ENV CADDY_VERSION=v2.3.0
# Mon, 04 Jan 2021 18:17:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 04 Jan 2021 18:18:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Jan 2021 18:18:12 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 04 Jan 2021 18:18:18 GMT
ENV XDG_DATA_HOME=/data
# Mon, 04 Jan 2021 18:18:23 GMT
VOLUME [/config]
# Mon, 04 Jan 2021 18:18:29 GMT
VOLUME [/data]
# Mon, 04 Jan 2021 18:18:34 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Mon, 04 Jan 2021 18:18:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 04 Jan 2021 18:18:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 04 Jan 2021 18:18:48 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 04 Jan 2021 18:18:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 04 Jan 2021 18:18:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 04 Jan 2021 18:19:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 04 Jan 2021 18:19:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 04 Jan 2021 18:19:27 GMT
EXPOSE 80
# Mon, 04 Jan 2021 18:19:43 GMT
EXPOSE 443
# Mon, 04 Jan 2021 18:19:50 GMT
EXPOSE 2019
# Mon, 04 Jan 2021 18:19:55 GMT
WORKDIR /srv
# Mon, 04 Jan 2021 18:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a9d343b7bcc225fe7ac17d96a81329510ab7f31a50472311cafe7168d3107317`  
		Last Modified: Thu, 17 Dec 2020 00:21:33 GMT  
		Size: 2.8 MB (2805226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5661232cea07dc41ae167e15c374f79251b26170652b994e8844fb55b4a5410`  
		Last Modified: Thu, 17 Dec 2020 02:34:34 GMT  
		Size: 302.3 KB (302338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e6c5134cf53417dab24ffba916fe2c36f64c91f8109cd4035ce97e9d2efa6f`  
		Last Modified: Thu, 17 Dec 2020 02:34:48 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecaad708cba83777a49b8b0153fd11aa1fda8c3de8c2669359510c7fba8e1d4`  
		Last Modified: Mon, 04 Jan 2021 18:21:19 GMT  
		Size: 10.2 MB (10241384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235fec692a51bccc1545ea1f8f892604e9198ae61248e12ddeba4043bea2c1f3`  
		Last Modified: Mon, 04 Jan 2021 18:21:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:1d605f274d1eca015a6899f98aed7e87ddbcf21fee25db45eb3af04b7fa35c7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14145519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499a2f900066e27e26138f6cac769b05f6cd3b0c6859052c1aa39eba8665d1a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 16 Dec 2020 23:41:37 GMT
ADD file:3ad3856d165e8760af85574a8ffa75ca44b7e1b97b64d1d6d4608445efa4b860 in / 
# Wed, 16 Dec 2020 23:41:37 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:48 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Dec 2020 00:26:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Mon, 04 Jan 2021 18:41:41 GMT
ENV CADDY_VERSION=v2.3.0
# Mon, 04 Jan 2021 18:41:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 04 Jan 2021 18:41:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Jan 2021 18:41:45 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 04 Jan 2021 18:41:45 GMT
ENV XDG_DATA_HOME=/data
# Mon, 04 Jan 2021 18:41:45 GMT
VOLUME [/config]
# Mon, 04 Jan 2021 18:41:45 GMT
VOLUME [/data]
# Mon, 04 Jan 2021 18:41:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Mon, 04 Jan 2021 18:41:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 04 Jan 2021 18:41:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 04 Jan 2021 18:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 04 Jan 2021 18:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 04 Jan 2021 18:41:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 04 Jan 2021 18:41:47 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 04 Jan 2021 18:41:47 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 04 Jan 2021 18:41:47 GMT
EXPOSE 80
# Mon, 04 Jan 2021 18:41:48 GMT
EXPOSE 443
# Mon, 04 Jan 2021 18:41:48 GMT
EXPOSE 2019
# Mon, 04 Jan 2021 18:41:48 GMT
WORKDIR /srv
# Mon, 04 Jan 2021 18:41:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ee52640a49e15b8b7c8edb66c2d048b26abdee8d828d6e5ef4e10a28cb15a84f`  
		Last Modified: Wed, 16 Dec 2020 23:42:15 GMT  
		Size: 2.6 MB (2567018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540682837d130d7c39e8c04e25653ea251d395459d10b412bfe6ef4350bf64e4`  
		Last Modified: Thu, 17 Dec 2020 00:28:06 GMT  
		Size: 300.5 KB (300456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cd745d1483c5464a545008c053bd17567c01d9e53779365080e1ac3d4207da`  
		Last Modified: Thu, 17 Dec 2020 00:28:17 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e914cfc82e9092a831f17f5daebbbde8ebe39d7fe50230325ce80f657bfe3f0f`  
		Last Modified: Mon, 04 Jan 2021 18:42:29 GMT  
		Size: 11.3 MB (11272057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d554de8138d32421dfdcb23f0feec824f7106586791ae523f39943c710ad71`  
		Last Modified: Mon, 04 Jan 2021 18:42:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
