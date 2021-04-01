## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:bcd45eecf34549d43c888d6b813fb96dfc9ca6e20bf79b79aec50c76a158d2a9
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
$ docker pull caddy@sha256:c0cb0c7ff63937fc641664895e1844666baf2f00eed688237f2e093a9a04a6a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a399f1211b45b8dbf10005ab3deec678552c502ac66a63ea3027a2ac30051414`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:38:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 26 Mar 2021 02:38:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Fri, 26 Mar 2021 02:38:22 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 26 Mar 2021 02:38:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 26 Mar 2021 02:38:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:38:29 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 26 Mar 2021 02:38:30 GMT
ENV XDG_DATA_HOME=/data
# Fri, 26 Mar 2021 02:38:30 GMT
VOLUME [/config]
# Fri, 26 Mar 2021 02:38:30 GMT
VOLUME [/data]
# Fri, 26 Mar 2021 02:38:31 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Fri, 26 Mar 2021 02:38:31 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 26 Mar 2021 02:38:32 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 26 Mar 2021 02:38:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 26 Mar 2021 02:38:32 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 26 Mar 2021 02:38:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 26 Mar 2021 02:38:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 26 Mar 2021 02:38:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 26 Mar 2021 02:38:34 GMT
EXPOSE 80
# Fri, 26 Mar 2021 02:38:34 GMT
EXPOSE 443
# Fri, 26 Mar 2021 02:38:35 GMT
EXPOSE 2019
# Fri, 26 Mar 2021 02:38:35 GMT
WORKDIR /srv
# Fri, 26 Mar 2021 02:38:36 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86cfaea3777414001ca8c36d3fb1c35e31ab133ef9edc3c047ae288ef70eb04`  
		Last Modified: Fri, 26 Mar 2021 02:39:44 GMT  
		Size: 300.0 KB (300017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b3ec4462bfd2b0286ff34909a730ba5f0ac56724d79f281d8837cb9a21492`  
		Last Modified: Fri, 26 Mar 2021 02:39:44 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0074ab5b262dbef2b99e9b03ce56382bb7b5c994d4015b1d035f954f05249a26`  
		Last Modified: Fri, 26 Mar 2021 02:39:47 GMT  
		Size: 11.6 MB (11622386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3482ef241eb9ce7284f69e549fc2ae9718230317834f0476186ef15f535af35a`  
		Last Modified: Fri, 26 Mar 2021 02:39:44 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:b57cdc61b54865a7ff2ea4ef9d16458537d40e0dc25559d6540111874abbe4ce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88293e19906b6b2275ff6e127e29960b1fdf0cf0c4baa4bbce4ea297e90db731`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 17:36:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 31 Mar 2021 17:36:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 31 Mar 2021 17:36:38 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 31 Mar 2021 17:36:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 31 Mar 2021 17:36:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 17:36:52 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 31 Mar 2021 17:36:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 31 Mar 2021 17:36:55 GMT
VOLUME [/config]
# Wed, 31 Mar 2021 17:36:55 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 17:36:56 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 31 Mar 2021 17:36:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 31 Mar 2021 17:36:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 31 Mar 2021 17:37:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 31 Mar 2021 17:37:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 31 Mar 2021 17:37:03 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 31 Mar 2021 17:37:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 31 Mar 2021 17:37:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 31 Mar 2021 17:37:07 GMT
EXPOSE 80
# Wed, 31 Mar 2021 17:37:08 GMT
EXPOSE 443
# Wed, 31 Mar 2021 17:37:10 GMT
EXPOSE 2019
# Wed, 31 Mar 2021 17:37:11 GMT
WORKDIR /srv
# Wed, 31 Mar 2021 17:37:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1532456df32c320ccd3c9ff5433c9e44d873ef87a0dc9fc29f9cf256b517eb4`  
		Last Modified: Wed, 31 Mar 2021 17:38:50 GMT  
		Size: 300.1 KB (300103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7263f61714ef61a0c59bef8e70bc49a741a357b0a0fc556b44f8344df37ea0f8`  
		Last Modified: Wed, 31 Mar 2021 17:38:52 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818002dab28746359de43d5a88d06c77cc3a353c838e15c6b6a67d48352cc5c0`  
		Last Modified: Wed, 31 Mar 2021 17:38:54 GMT  
		Size: 10.9 MB (10944835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7979a3c808bf5c07c668f5966a15458dbfe9aba5aa7d761e690dd3a5cadf45eb`  
		Last Modified: Wed, 31 Mar 2021 17:38:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:6d510324512c20fc0d40aeb8b6e5b98255c857ad2dee894b6cb6e66f0231cf9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13638799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42db38da968682707e6cf0fabb16f93770388907d8a208fca0db74cae3183ba2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 31 Mar 2021 18:13:45 GMT
ADD file:1270a9135e4e3d6bcd51f9c8bb7a5129c493366412591f1a6885db98056a572e in / 
# Wed, 31 Mar 2021 18:13:47 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 08:11:44 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 01 Apr 2021 08:11:47 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 01 Apr 2021 08:11:48 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 01 Apr 2021 08:11:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 01 Apr 2021 08:11:55 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 08:11:56 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 01 Apr 2021 08:11:57 GMT
ENV XDG_DATA_HOME=/data
# Thu, 01 Apr 2021 08:11:58 GMT
VOLUME [/config]
# Thu, 01 Apr 2021 08:11:59 GMT
VOLUME [/data]
# Thu, 01 Apr 2021 08:12:00 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Thu, 01 Apr 2021 08:12:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 01 Apr 2021 08:12:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 01 Apr 2021 08:12:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 01 Apr 2021 08:12:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 01 Apr 2021 08:12:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 01 Apr 2021 08:12:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 01 Apr 2021 08:12:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 01 Apr 2021 08:12:09 GMT
EXPOSE 80
# Thu, 01 Apr 2021 08:12:11 GMT
EXPOSE 443
# Thu, 01 Apr 2021 08:12:13 GMT
EXPOSE 2019
# Thu, 01 Apr 2021 08:12:15 GMT
WORKDIR /srv
# Thu, 01 Apr 2021 08:12:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b04429a2165487924dcbfedfff74fa262e6828327d04bb4b1c6a477096f5010e`  
		Last Modified: Wed, 31 Mar 2021 18:15:12 GMT  
		Size: 2.4 MB (2408269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547b5d01ba24abc02b4f05f8134bfb156ce1840f496ed03a1316c882625bd41f`  
		Last Modified: Thu, 01 Apr 2021 08:13:34 GMT  
		Size: 299.2 KB (299199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a883a914d37801ae97b0fac82c62e4f70ef4c92fc53417a91a23b2e69d36d9bb`  
		Last Modified: Thu, 01 Apr 2021 08:13:34 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475143e7b89d1a36700916ec3c8f0caae9b57d5cd9ba187b9f3fd5d9a71eddcf`  
		Last Modified: Thu, 01 Apr 2021 08:13:38 GMT  
		Size: 10.9 MB (10925346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e79cdab22a3397c4a98f63a7e96c51881033744b1f198c4984072e7303e9f73`  
		Last Modified: Thu, 01 Apr 2021 08:13:34 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2760e78ed4694a84bd2d6c9f8757e0f2eef516d52254f98277005e3332940156
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13614976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb1c06d0b71ebdf93ccd671ded898dbc05fb92605aaa2e613a00c690c63f307`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:31:31 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 25 Mar 2021 23:31:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 25 Mar 2021 23:32:08 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 25 Mar 2021 23:32:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 25 Mar 2021 23:32:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:33:02 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 25 Mar 2021 23:33:13 GMT
ENV XDG_DATA_HOME=/data
# Thu, 25 Mar 2021 23:33:20 GMT
VOLUME [/config]
# Thu, 25 Mar 2021 23:33:35 GMT
VOLUME [/data]
# Thu, 25 Mar 2021 23:33:41 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Thu, 25 Mar 2021 23:33:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 25 Mar 2021 23:33:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 25 Mar 2021 23:33:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 25 Mar 2021 23:33:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 25 Mar 2021 23:33:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 25 Mar 2021 23:34:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 25 Mar 2021 23:34:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 25 Mar 2021 23:34:38 GMT
EXPOSE 80
# Thu, 25 Mar 2021 23:35:00 GMT
EXPOSE 443
# Thu, 25 Mar 2021 23:35:06 GMT
EXPOSE 2019
# Thu, 25 Mar 2021 23:35:19 GMT
WORKDIR /srv
# Thu, 25 Mar 2021 23:35:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18097d4c9638c3cd9be2c7e06cf74879d0c24caa73501e2adfa40b02ec79e261`  
		Last Modified: Thu, 25 Mar 2021 23:42:19 GMT  
		Size: 300.3 KB (300322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8feda3f9171d8b727a6d38d73439a098d5e367e1e7346b0d346e7c09e26cec`  
		Last Modified: Thu, 25 Mar 2021 23:42:19 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60fde45401cbb316e0c5b208967fc883da8992e8b892a574bcb4e69ba7d7e6e`  
		Last Modified: Thu, 25 Mar 2021 23:42:26 GMT  
		Size: 10.6 MB (10598976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f235d25412984912e2016f077ff2c324bbfec9fcfc7051d30f549c5187904f32`  
		Last Modified: Thu, 25 Mar 2021 23:42:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d8ff14acdf013e9a2df27d95f3326bf7175307a04e9e6f7a40b840bf813898ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13355680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63b8a5e4185f59e46edc1e47b15d592327b0c3b8867d3edd3be3a9b3dea5522`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 25 Mar 2021 22:22:44 GMT
ADD file:fa3152db8e0ad493ea5fe137f9b6210cabbda6e880fc18f1935b8ef1dae5e5b7 in / 
# Thu, 25 Mar 2021 22:22:50 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:49:30 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 26 Mar 2021 05:49:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Fri, 26 Mar 2021 05:49:51 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 26 Mar 2021 05:50:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 26 Mar 2021 05:50:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 05:50:10 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 26 Mar 2021 05:50:14 GMT
ENV XDG_DATA_HOME=/data
# Fri, 26 Mar 2021 05:50:24 GMT
VOLUME [/config]
# Fri, 26 Mar 2021 05:50:30 GMT
VOLUME [/data]
# Fri, 26 Mar 2021 05:50:36 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Fri, 26 Mar 2021 05:50:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 26 Mar 2021 05:50:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 26 Mar 2021 05:50:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 26 Mar 2021 05:50:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 26 Mar 2021 05:50:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 26 Mar 2021 05:51:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 26 Mar 2021 05:51:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 26 Mar 2021 05:51:24 GMT
EXPOSE 80
# Fri, 26 Mar 2021 05:51:30 GMT
EXPOSE 443
# Fri, 26 Mar 2021 05:51:35 GMT
EXPOSE 2019
# Fri, 26 Mar 2021 05:51:40 GMT
WORKDIR /srv
# Fri, 26 Mar 2021 05:51:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d9d64eb18374b2d527a335e2362041eba1adef6c7376c1347f45cbd1df5239c1`  
		Last Modified: Thu, 25 Mar 2021 22:24:26 GMT  
		Size: 2.8 MB (2805974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f69ab62cc22d6fb5ba7a45731c0b8f378026c7c711d7d48946bfe7c69eae199`  
		Last Modified: Fri, 26 Mar 2021 05:58:00 GMT  
		Size: 302.3 KB (302337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9767f7d2aec64fa7c89aa12c9b2b14b03dbe10e20cf53279a88f5009dd2c7841`  
		Last Modified: Fri, 26 Mar 2021 05:58:00 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502018de7a2dcf0f08830ebcce7c073c9a9db95ecf366d96d44c7a76ba032edc`  
		Last Modified: Fri, 26 Mar 2021 05:58:02 GMT  
		Size: 10.2 MB (10241383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61815e7304b64383c90b6c68c7220f40b74c932f3dd3cfd44b04fed05920aec`  
		Last Modified: Fri, 26 Mar 2021 05:58:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9d992badb7530225182676af12ae945f5f2de2f5ad7d3946b397892a6de4c123
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14145974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c8a68869d0806c29e6c2c9c655d3e9085af285c6c24ea651ad3bdffd714e38`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 31 Mar 2021 17:15:04 GMT
ADD file:1f37b92ea1f573c4810b1d056dc4880cf4035e143451d9b2b76fac1e3b462248 in / 
# Wed, 31 Mar 2021 17:15:04 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:55:58 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 31 Mar 2021 18:56:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 31 Mar 2021 18:56:00 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 31 Mar 2021 18:56:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 31 Mar 2021 18:56:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:56:05 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 31 Mar 2021 18:56:05 GMT
ENV XDG_DATA_HOME=/data
# Wed, 31 Mar 2021 18:56:05 GMT
VOLUME [/config]
# Wed, 31 Mar 2021 18:56:06 GMT
VOLUME [/data]
# Wed, 31 Mar 2021 18:56:06 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 31 Mar 2021 18:56:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 31 Mar 2021 18:56:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 31 Mar 2021 18:56:06 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 31 Mar 2021 18:56:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 31 Mar 2021 18:56:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 31 Mar 2021 18:56:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 31 Mar 2021 18:56:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 31 Mar 2021 18:56:08 GMT
EXPOSE 80
# Wed, 31 Mar 2021 18:56:08 GMT
EXPOSE 443
# Wed, 31 Mar 2021 18:56:08 GMT
EXPOSE 2019
# Wed, 31 Mar 2021 18:56:08 GMT
WORKDIR /srv
# Wed, 31 Mar 2021 18:56:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:38ca5430c9af12b6b6dee7c10eb6b1eb0e4eb4f5f02a97890579c4b049d00233`  
		Last Modified: Wed, 31 Mar 2021 17:15:46 GMT  
		Size: 2.6 MB (2567453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8eb19b6319d0b09121581759094c3eb58e5574e2063affb6c42c0e1a1937a0`  
		Last Modified: Wed, 31 Mar 2021 18:57:00 GMT  
		Size: 300.5 KB (300471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd6e269a873b8a21e2787b0ea05662c0f2676aa9043f52b8884081965be7112`  
		Last Modified: Wed, 31 Mar 2021 18:57:00 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f6a8a7e19cb11edbda771ce361181202915f4760cdaef5e290b1758cc7b88c`  
		Last Modified: Wed, 31 Mar 2021 18:57:02 GMT  
		Size: 11.3 MB (11272066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec92d2dcab4ee41e4e626d8b360a6feff3822db894894865a36bbe9cfc759df0`  
		Last Modified: Wed, 31 Mar 2021 18:57:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
