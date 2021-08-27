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
-	[`caddy:2.4.3`](#caddy243)
-	[`caddy:2.4.3-alpine`](#caddy243-alpine)
-	[`caddy:2.4.3-builder`](#caddy243-builder)
-	[`caddy:2.4.3-builder-alpine`](#caddy243-builder-alpine)
-	[`caddy:2.4.3-builder-windowsservercore-1809`](#caddy243-builder-windowsservercore-1809)
-	[`caddy:2.4.3-builder-windowsservercore-ltsc2016`](#caddy243-builder-windowsservercore-ltsc2016)
-	[`caddy:2.4.3-windowsservercore`](#caddy243-windowsservercore)
-	[`caddy:2.4.3-windowsservercore-1809`](#caddy243-windowsservercore-1809)
-	[`caddy:2.4.3-windowsservercore-ltsc2016`](#caddy243-windowsservercore-ltsc2016)
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
$ docker pull caddy@sha256:d235036337fad2117f058e44b0ce4813f974924e03ff629da08dbee7c6be5e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:77f27025e0e1e0ab97bc931db61d24f9ac41591e17576ab46c4b508afbccacd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14648199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8a741f4852592d8634aa37c7f351ae4f4e7b4a9a2594df54603ac48cbdad74`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:11:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 11 May 2021 01:04:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 19:19:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 19:19:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 19:19:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 19:19:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 19:19:32 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 19:19:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 443
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 19:19:34 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 19:19:34 GMT
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
	-	`sha256:16798e0582fce7af9c2ba2c8ee4990d0fd1e58384e170ee9937486253d67bbf1`  
		Last Modified: Tue, 11 May 2021 01:05:00 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d589bc046eca71df600301462981053bf178fcd31d4b2c882ca05aec70bacd`  
		Last Modified: Thu, 24 Jun 2021 19:19:59 GMT  
		Size: 11.5 MB (11529821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8ce9421f330c9a085ac8f059d2dd53feabf795c461d4f43b596d0302b1cf9`  
		Last Modified: Thu, 24 Jun 2021 19:19:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:615389b06a74c80f0494cdc47da7b9f565cadd8cd715e39d7b65aaaf2937b6cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13816604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac08c3d5e13d15da24bbe2b6e7bd0fe9a42212188c3f33467bb1f38dfdb0b51`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 22:32:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 22:32:24 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 22:32:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 22:32:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 22:32:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 22:32:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 22:32:36 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 22:32:37 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 22:32:37 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 22:32:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 22:32:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 22:32:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 22:32:44 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:32:45 GMT
EXPOSE 443
# Fri, 30 Jul 2021 22:32:46 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 22:32:46 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 22:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18943f91e0b98a5ee778a791cc00f627dfc62e6163be04be39d8dfca48ca309`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 300.5 KB (300515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6779ad883f93abbe8842bc2dd07f67be174891b4b835e18a7eccb5a738ee0eb9`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6cb30c4e53dad6055df249f24807530e7530d534f18b81671b80de7b8b0ad2`  
		Last Modified: Fri, 30 Jul 2021 22:34:16 GMT  
		Size: 10.9 MB (10887954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a803ba6ef03f0246aec715857792f54efc64816b24b563beee84263dd1ad439`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c382c62559cf6348cccc2048f7f6e3234ad6c3322fa778f0d7ab3fbe27cd44e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13593493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c6676bf8617209d68af4cbdd3c3edb6084cbd01e6c7f00b706fab8934f311a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Fri, 30 Jul 2021 18:36:39 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:13:40 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 02:13:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 02:13:44 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 02:13:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 02:13:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 02:13:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 02:13:56 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 443
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 02:13:58 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 02:13:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf509b321d9275e96242772f4cd73ad8da2970e30e18c0f2326ed91777442e`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 299.7 KB (299672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16416239cfcd26ea4cc02aaf7ac5511b6ea5d6cc672046b6e61d90f9c59ffaac`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de14f3facde68cf2e2470839f96bb111537c6b40d15a1b28c47c6568261ee15`  
		Last Modified: Sat, 31 Jul 2021 02:15:20 GMT  
		Size: 10.9 MB (10863669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6b241bda44fe422ccd7c0c967fb01d2d7a191df7b0628d9c44df2d18dd5445`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ee1b9ce06277bd5c34b2d9a6908cdb3028aa838fa75e5c6e1e32d2cabb417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13464756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a697a3b5305c041fd956ba80c8845676041e98bce128a69e70074e5abe9653dd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 15 Jun 2021 22:32:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 18:39:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 18:39:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 18:39:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 443
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 18:39:33 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 18:39:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d0b72044755ebd2b829600b94a69aa9096bbb4bf9a01c1795b5b245261b99a`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 300.6 KB (300631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abde659ccf1d73128ef1e71a9701b014e0f27d4abf15b3d410d0474cdd0adb95`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75403ccf5c23126b5dca334871ec0096a90d0fb85f47be1ecba3904921529c0`  
		Last Modified: Thu, 24 Jun 2021 18:40:18 GMT  
		Size: 10.4 MB (10446098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a85edeaa46fe5e0185f11a1a1801c0d0458e59897d3c04e97136df1c496663`  
		Last Modified: Thu, 24 Jun 2021 18:40:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:fff2119338c215eceae68398483da801f5daf8bb5405c7ed8db5769aeb367cd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13173634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced11b632073f0e249ba02b8326f0c1ccf6c154d4340342b38c8b3f830c37e70`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:24:49 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Fri, 30 Jul 2021 17:24:54 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:36:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 00:36:51 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 00:36:54 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 00:37:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 00:37:10 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 00:37:12 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 00:37:14 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 00:37:17 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 00:37:23 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 00:37:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 00:37:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 00:37:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 00:37:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 00:37:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 00:37:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 00:37:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 00:38:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 00:38:06 GMT
EXPOSE 80
# Sat, 31 Jul 2021 00:38:09 GMT
EXPOSE 443
# Sat, 31 Jul 2021 00:38:16 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 00:38:25 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 00:38:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396ee5e0a948db1cebd77a9b357abbc39c60dc4caf97f87f759a1f232a291da5`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 302.5 KB (302545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c405a506bbc65ab625ac9298a31abc4a1871eef7b93ff4fbc6a25fb9db591a4`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ac195b709078a7d439cd22a970947cb2ed3f9cd136a8d51324ab3d3c746625`  
		Last Modified: Sat, 31 Jul 2021 00:39:16 GMT  
		Size: 10.1 MB (10051943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2c9f1da5ba05b5656393520168363c5d8a223167645bc0a4451fcd4c2f5447`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:576d8d6d9dead63f0cc0db39ad0fb1e9e9539bf5b23a8b70623b7e8f40d916a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14005959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6114aef9a435617ae101cc26569f3f2103cd2c999ef3e41df780270222452a1f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:41:41 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Fri, 30 Jul 2021 17:41:42 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 23:50:44 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 23:50:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 23:50:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 23:50:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 23:50:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 23:50:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 80
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 443
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 23:50:52 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 23:50:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de364003ff53d3ed839a7d8fd8cc6c59936d04b22886595d954e5c9929cfe0e1`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 300.9 KB (300858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d9b83bb28f1c9bc97f9a4907425be62b28dd687b54e3b8d461b2e40203110d`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076584d90c472ad966977bc9f55f53439edb7b5169fa684c1a70a1ea682037ca`  
		Last Modified: Fri, 30 Jul 2021 23:51:34 GMT  
		Size: 11.1 MB (11096451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f126f1c964e9405478f4683dd4b8e93297166d84566a652fe658f36bad6390c`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:277245d2976e25118dde31aa817da26aab9a54b716478e335e7e47a655680fdf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdb54faaf1277fc5d472259e6d51ac14101b59691359db53c189a9f55df03c8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:21:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:21:12 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:22:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:22:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:22:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:22:18 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:22:19 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:22:20 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:22:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:22:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:22:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:22:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:22:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:22:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:22:28 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:22:29 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:22:30 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:23:15 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:23:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc78244c47d63e7118efa5a81aeac258859631816cf0d2e335045eddd6d4562c`  
		Last Modified: Wed, 25 Aug 2021 19:29:08 GMT  
		Size: 390.1 KB (390074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e85659c5ef3d6f1826cce92e5c35cbda668ec96e58661902ea89472385a68`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad534458f62e8592943908290a647cce35c3f5ed0761b80f7d17f55393900e`  
		Last Modified: Wed, 25 Aug 2021 19:29:10 GMT  
		Size: 12.0 MB (12023423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e1aa1a15f7618a90c91ce39aeb28f0b14d0fb039a0a5c387e2d7a4460443aa`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a259cd0cf699d1891ff65f72aaf75b8b53d32409fdbab40fa8aa3594f4edb`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb72b357bee0361ca5587e675d3a832276f086a2d6535147bfe92a000cf044f`  
		Last Modified: Wed, 25 Aug 2021 19:29:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbe28f726b8cddbd0398281cfc45f2dc82f378bef80fa1dfe4dec201451721`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a73648024b9f42aeeda4c4309ba545e089e6943b686c93ea09cec6ac83373`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ad45ece5f60db2673be4be17ca0ac1ff391d32d88f7a84e2e671fca6744e0`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424371920e55efd886bea3b4671eca80436677674986f299b919e72c49d4289`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2b299f27503c9be94a9a16c137b08ba7e2b84cc07b96a281d4b2886b231f0`  
		Last Modified: Wed, 25 Aug 2021 19:29:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c231726719db989f9746b39a4b4b9b54646376e1dc36c124a1401fc15132`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ae0be18044dcf67b8832f125744410261cc8601712176399a3cd632b8843`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b94a88e7f4db3aa538dad13b42b51168525142c8268098dbe8a7175decee6`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0f35247abb67063d217ea9963f29270e1716b21409196f0e935710342a9dd9`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fa12b6daf14192bb460b568c8c3f65625b384fbcfa33e4b227d39de751374d`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43dbbbd0c30fabb616088a2f902ad0177c216707c4e134d10b9a1cd4fde8cb`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee931681f757a39ac6ce152aa1d64f251a68f63dca6dbe3459c2cec9bed0d90e`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deb6e04a956a5c619ff2eb344a4e5fcf8384d890b8120ce2ffd91cf20e0b5f`  
		Last Modified: Wed, 25 Aug 2021 19:29:00 GMT  
		Size: 320.7 KB (320709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b510aa21fdb81bb0a2156b0a977a69ea8187f959ceb05869b1450d9359814`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:bd0551e2eeef6d131272af5e4214599dfc85e2a18d421264005a4f8dc3025a02
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283675023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96c9f880047fab4000d8bad0dceb15c3e478898181805e15b864f3ae980f11`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:24:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:24:21 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:25:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:25:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:25:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:25:25 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:25:26 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:25:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:25:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:25:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:25:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:25:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:25:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:25:35 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:25:36 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:25:37 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:26:16 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:26:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9dee8014da227cc8c6b8d14f6464fefc307c265b07a34d6e2ccc5de24a92a`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 352.7 KB (352700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d26c5819d131639ab53b8e099ab2ed93c63f759072d3a5ce4b9f69f13b8a66`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb3ea0fdbcaf7cab1dbac86676ab00ca78ebf68e3b5c476c5984201c357976`  
		Last Modified: Wed, 25 Aug 2021 19:29:35 GMT  
		Size: 12.0 MB (12025369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a331953cb55eb8482f8b09c1ccb30b06198b0da91f196aa230d56d4f626c3`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c66a58bae64f63c34265474f15131687cba250a5cbeb2166a25d383630b68`  
		Last Modified: Wed, 25 Aug 2021 19:29:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b60346916eaf0cd70873400273d0f0de4f72aa7ee5a5bd6a8cfbe446d62499`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74af1f53b1dc6d2f58a23760f463877d707150f1cae25c0ca6a727c64cd7e9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4467e0d432e5bba7c8e197c057837e438ae63c8748b9765a8d7591c0ea12c0`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c92db8b514f6d653c3d0ba5a7e695e808f5880504124fb94648c10590f7f3c9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63a5575b8310dcb9cbe40352e7753a4bb8f66f1c3fbea055abda03136638d6`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415f534f6818ea980cf13f9a08c0efb9d60c9f86760129563e203ba93e399c8`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be354de1af39afc991030861814f135bfde0267a02f004fd4caf9ccc31d0bfd`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a0ebb3c5c8d126c85ccbad571fef0051ac62cfec3fe5885c82110381049ed9`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893f40ed74354bd380ee49a7141c654ea10f5a43f1e050539bde502c7214c9f`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd03947508d81a8a5c939b4a1697e4cf18bc8722cc1650732f8df2c6924941`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c43d724632362e78f09ee6bf53a8359cdd6db65300cb3687f2ad3a59e1a5d`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaec774cf06dd02e7ebdf8d5e9aa9b8d4578a60c7a54ce84421910922396b7`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb3d76a117ff8038563015df19972676ff4aea085431ef698f57799559b334`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341d5f41a06e42738b97ffd6ca2835680879ba4113b882c5cd8accd857c0551`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 305.6 KB (305571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd0dece66bb4a5f39d723d7d27311fa04d1de60c084735f41cb588c7b4d5701`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:f00d2e7e82418a30135cbe5c1455df6c617ee651d6f430183a8e49e3b2608359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:77f27025e0e1e0ab97bc931db61d24f9ac41591e17576ab46c4b508afbccacd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14648199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8a741f4852592d8634aa37c7f351ae4f4e7b4a9a2594df54603ac48cbdad74`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:11:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 11 May 2021 01:04:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 19:19:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 19:19:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 19:19:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 19:19:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 19:19:32 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 19:19:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 443
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 19:19:34 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 19:19:34 GMT
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
	-	`sha256:16798e0582fce7af9c2ba2c8ee4990d0fd1e58384e170ee9937486253d67bbf1`  
		Last Modified: Tue, 11 May 2021 01:05:00 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d589bc046eca71df600301462981053bf178fcd31d4b2c882ca05aec70bacd`  
		Last Modified: Thu, 24 Jun 2021 19:19:59 GMT  
		Size: 11.5 MB (11529821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8ce9421f330c9a085ac8f059d2dd53feabf795c461d4f43b596d0302b1cf9`  
		Last Modified: Thu, 24 Jun 2021 19:19:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:615389b06a74c80f0494cdc47da7b9f565cadd8cd715e39d7b65aaaf2937b6cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13816604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac08c3d5e13d15da24bbe2b6e7bd0fe9a42212188c3f33467bb1f38dfdb0b51`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 22:32:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 22:32:24 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 22:32:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 22:32:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 22:32:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 22:32:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 22:32:36 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 22:32:37 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 22:32:37 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 22:32:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 22:32:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 22:32:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 22:32:44 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:32:45 GMT
EXPOSE 443
# Fri, 30 Jul 2021 22:32:46 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 22:32:46 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 22:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18943f91e0b98a5ee778a791cc00f627dfc62e6163be04be39d8dfca48ca309`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 300.5 KB (300515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6779ad883f93abbe8842bc2dd07f67be174891b4b835e18a7eccb5a738ee0eb9`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6cb30c4e53dad6055df249f24807530e7530d534f18b81671b80de7b8b0ad2`  
		Last Modified: Fri, 30 Jul 2021 22:34:16 GMT  
		Size: 10.9 MB (10887954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a803ba6ef03f0246aec715857792f54efc64816b24b563beee84263dd1ad439`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c382c62559cf6348cccc2048f7f6e3234ad6c3322fa778f0d7ab3fbe27cd44e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13593493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c6676bf8617209d68af4cbdd3c3edb6084cbd01e6c7f00b706fab8934f311a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Fri, 30 Jul 2021 18:36:39 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:13:40 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 02:13:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 02:13:44 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 02:13:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 02:13:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 02:13:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 02:13:56 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 443
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 02:13:58 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 02:13:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf509b321d9275e96242772f4cd73ad8da2970e30e18c0f2326ed91777442e`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 299.7 KB (299672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16416239cfcd26ea4cc02aaf7ac5511b6ea5d6cc672046b6e61d90f9c59ffaac`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de14f3facde68cf2e2470839f96bb111537c6b40d15a1b28c47c6568261ee15`  
		Last Modified: Sat, 31 Jul 2021 02:15:20 GMT  
		Size: 10.9 MB (10863669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6b241bda44fe422ccd7c0c967fb01d2d7a191df7b0628d9c44df2d18dd5445`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ee1b9ce06277bd5c34b2d9a6908cdb3028aa838fa75e5c6e1e32d2cabb417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13464756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a697a3b5305c041fd956ba80c8845676041e98bce128a69e70074e5abe9653dd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 15 Jun 2021 22:32:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 18:39:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 18:39:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 18:39:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 443
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 18:39:33 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 18:39:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d0b72044755ebd2b829600b94a69aa9096bbb4bf9a01c1795b5b245261b99a`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 300.6 KB (300631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abde659ccf1d73128ef1e71a9701b014e0f27d4abf15b3d410d0474cdd0adb95`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75403ccf5c23126b5dca334871ec0096a90d0fb85f47be1ecba3904921529c0`  
		Last Modified: Thu, 24 Jun 2021 18:40:18 GMT  
		Size: 10.4 MB (10446098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a85edeaa46fe5e0185f11a1a1801c0d0458e59897d3c04e97136df1c496663`  
		Last Modified: Thu, 24 Jun 2021 18:40:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:fff2119338c215eceae68398483da801f5daf8bb5405c7ed8db5769aeb367cd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13173634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced11b632073f0e249ba02b8326f0c1ccf6c154d4340342b38c8b3f830c37e70`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:24:49 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Fri, 30 Jul 2021 17:24:54 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:36:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 00:36:51 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 00:36:54 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 00:37:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 00:37:10 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 00:37:12 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 00:37:14 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 00:37:17 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 00:37:23 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 00:37:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 00:37:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 00:37:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 00:37:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 00:37:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 00:37:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 00:37:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 00:38:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 00:38:06 GMT
EXPOSE 80
# Sat, 31 Jul 2021 00:38:09 GMT
EXPOSE 443
# Sat, 31 Jul 2021 00:38:16 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 00:38:25 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 00:38:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396ee5e0a948db1cebd77a9b357abbc39c60dc4caf97f87f759a1f232a291da5`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 302.5 KB (302545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c405a506bbc65ab625ac9298a31abc4a1871eef7b93ff4fbc6a25fb9db591a4`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ac195b709078a7d439cd22a970947cb2ed3f9cd136a8d51324ab3d3c746625`  
		Last Modified: Sat, 31 Jul 2021 00:39:16 GMT  
		Size: 10.1 MB (10051943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2c9f1da5ba05b5656393520168363c5d8a223167645bc0a4451fcd4c2f5447`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:576d8d6d9dead63f0cc0db39ad0fb1e9e9539bf5b23a8b70623b7e8f40d916a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14005959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6114aef9a435617ae101cc26569f3f2103cd2c999ef3e41df780270222452a1f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:41:41 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Fri, 30 Jul 2021 17:41:42 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 23:50:44 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 23:50:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 23:50:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 23:50:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 23:50:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 23:50:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 80
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 443
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 23:50:52 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 23:50:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de364003ff53d3ed839a7d8fd8cc6c59936d04b22886595d954e5c9929cfe0e1`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 300.9 KB (300858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d9b83bb28f1c9bc97f9a4907425be62b28dd687b54e3b8d461b2e40203110d`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076584d90c472ad966977bc9f55f53439edb7b5169fa684c1a70a1ea682037ca`  
		Last Modified: Fri, 30 Jul 2021 23:51:34 GMT  
		Size: 11.1 MB (11096451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f126f1c964e9405478f4683dd4b8e93297166d84566a652fe658f36bad6390c`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:6d4327fca22a56f18bcb561bbf5be757c05758d8bfcab7b115d6481996285052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:024148c65604529e01fe96436356aef6adc9737caf5784ee97639dc0178c0e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116836974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67f775001477b06c70ee78b6bf98a0ff2eb5c9a458dc030e5c730526e487f8e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:20:55 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:20:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:20:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:23:31 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:25:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:25:15 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:25:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:25:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:25:17 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:15:27 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:15:27 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:15:27 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:15:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:15:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:15:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:15:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e108acfc2dec423245b992f059c15efa90d3da68d666891f88e21cf9ed3044`  
		Last Modified: Fri, 27 Aug 2021 17:26:14 GMT  
		Size: 281.5 KB (281498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d12eec82106ee897382a4e0f5f4012bb993a2abb41ea43f6055affa263792`  
		Last Modified: Fri, 27 Aug 2021 17:26:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba5eda52a4c5e66ad77248b778eeaabf785c0ef090e85270075e82189ccdfc4`  
		Last Modified: Fri, 27 Aug 2021 17:27:13 GMT  
		Size: 105.8 MB (105802322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb85018fe45e8393802b1c7b0b50c6e376a6ca1e8e95626bde089498a365f36`  
		Last Modified: Fri, 27 Aug 2021 17:26:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90db72e3ed64553e72bfe368d98a62d9a915cccbf3fa0c25590581cd4a3cfb5`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 6.6 MB (6626826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2349f3cb068e4777bdf9bcdd5798e514be84f8a1b7c4f6c2cfbfe2ee83c11dcd`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 1.3 MB (1311166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b310272a238f2d14deb416889fbea68278aa777bf5de85c3c294752976cd54`  
		Last Modified: Fri, 27 Aug 2021 18:15:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a2633b70d3d99f56930313cbc6c8e60f9cb84d8a247952f70ecde4b3d287a61f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112621949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995bf035b94c22d1dfae95d63886ec0360983d1862a4f0b9934cfad4c223eecf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:51:48 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:51:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:51:50 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:56:06 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:58:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:58:48 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:58:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:58:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:58:51 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:58:16 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:58:16 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:58:17 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:58:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:58:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:58:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:58:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def35433210b819c72fc8c3f4cefb914a4d2072a396498b271719a29363f24a2`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 281.7 KB (281662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fbd33b2207f0f6c992e5356a6285f8362b9ddf3f61650c7493aa2568c9fa1`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8584a59dc2c89569cc10317112977b3957c6ab4369fad184c5d8f616e7bf78ba`  
		Last Modified: Fri, 27 Aug 2021 18:03:31 GMT  
		Size: 102.0 MB (102005169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28236e9ee5408a1ebfbc1993365e25c57923224e6608703e02685d3aada63456`  
		Last Modified: Fri, 27 Aug 2021 18:02:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bde7b63fd968f5c9eceab8094063f4937b1da8306aa777963db7cbb714883f`  
		Last Modified: Fri, 27 Aug 2021 18:59:31 GMT  
		Size: 6.5 MB (6485279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8f7ef25d584b1a6933ca79bb2c78a3fc206f53a38ab1ddd7060ecbe2a933dd`  
		Last Modified: Fri, 27 Aug 2021 18:59:28 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bf61c4b3d04e6edd3304db5bd03a3241100e4d350312263ff17271a6dc69a6`  
		Last Modified: Fri, 27 Aug 2021 18:59:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:34333a1acab5cdd87309f11e0d23c3d4c6b8685b0160f307ba7206972d37853e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111501647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231aa2a8195b5e48739d3233aacb263ab4462039e3fdd181e304186924795270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:27:52 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 19:27:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 19:27:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:33:26 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 19:36:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 19:36:54 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 19:36:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:36:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 19:37:01 GMT
WORKDIR /go
# Sat, 07 Aug 2021 03:50:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 03:51:00 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 03:51:00 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 03:51:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 03:51:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 03:51:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 03:51:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc7b26480300ed9c6eddb3c4eb897051a740425806a7edff4973e09fae2bb8f`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 280.8 KB (280814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba13042e2b42dba9e7f0e57a60855dff15f2890b8d942f61fbdc4852a43854`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a06372885d9e72431bcb74f5cbb21c55f0607374a0dc1a7261e0fdffe19a389`  
		Last Modified: Fri, 06 Aug 2021 19:47:59 GMT  
		Size: 101.8 MB (101786462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeda0e3490d50d1412a7145a405521667a31542915116d5bca87d1f262a3ba6`  
		Last Modified: Fri, 06 Aug 2021 19:47:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c45b3f2b54d4bc0ce5312c296a0f2073fa104179f9935212b88b9e9e4981251`  
		Last Modified: Sat, 07 Aug 2021 03:52:09 GMT  
		Size: 5.8 MB (5784805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e389ea9eac74a8896f796d9c785720d528a709e5ec82bf35fa05f7d36e8c2d`  
		Last Modified: Sat, 07 Aug 2021 03:52:07 GMT  
		Size: 1.2 MB (1219493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1adc87d17fa7707fc23fe9ed965dd55d2704211e52c5a765628d42ba2439dab`  
		Last Modified: Sat, 07 Aug 2021 03:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6f976dea79506be1124a40be07324506d379f104afb6b4eb7d7ac3ebd1f81143
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112055672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b827a8f7150bc8bc38ad14e96bb8ec14de011b8352d944d532735984a1f6f119`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:41:17 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:41:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:41:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:43:33 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:45:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:45:02 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:45:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:45:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:45:03 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:35:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:35:10 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:35:10 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:35:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:35:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:35:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:35:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e34390c2b14c7d6b4929bed3213d6d86bb9aa93c4ec135494e476afbb7c8ff`  
		Last Modified: Fri, 27 Aug 2021 17:46:50 GMT  
		Size: 281.7 KB (281688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f557407009b175f4d46f52d9e57a4123bc5118b57e0a250e983230d791682`  
		Last Modified: Fri, 27 Aug 2021 17:46:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b522346004414564cf2d79fa6ca0b9efd60f64f3cb1cfc754f94dea608d2a9`  
		Last Modified: Fri, 27 Aug 2021 17:48:05 GMT  
		Size: 101.1 MB (101121978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e36f943c088c76ce04cebeee6e3b83058ecf72465cbb1807ce21d94b09b892`  
		Last Modified: Fri, 27 Aug 2021 17:47:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f7d54a0c7c055c4b4d79ed1dee9267b227d3fe5987a13e382a3a92c14f30fa`  
		Last Modified: Fri, 27 Aug 2021 18:35:48 GMT  
		Size: 6.7 MB (6737926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1225f39dda93839c2256ed41c7299db86680c6c805344be7c064a34211daa`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 1.2 MB (1201538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87cf0ee91a4aba520fb94188e3d73181288f133c2b42cc0add124bc59519f0`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4cb744a2c30bef1fce63b25f25090e9a6fba23d518fbfb8a67f2de5437567654
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110962703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc63a956570ca25fb6e8cda280b13ba663c3f8268fcfd235e0f50e7efe03073`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:02:31 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 21:02:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 21:02:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:06:00 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 21:07:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 21:08:01 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 21:08:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:08:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 21:08:22 GMT
WORKDIR /go
# Sat, 07 Aug 2021 04:22:15 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 04:22:17 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 04:22:21 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 04:22:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 04:22:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 04:22:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 04:22:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f69fce9d10f5a5c047377039cda1fd5125aae4ec022be3dd7aede58be5a483`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 283.6 KB (283642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fdcb934d4034adf5e88a3b7bff7a633580eb8c0f18480df4123a14c499558b`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c6309d0f42f3d590978baeb06a18f86672f414b4fd6b6c0167fbaf5bc68502`  
		Last Modified: Fri, 06 Aug 2021 21:13:47 GMT  
		Size: 99.6 MB (99599293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6b0f08798744f7a5f5fbd19a9db24d1ce885fdb4cf4cc03cb9016e172748d1`  
		Last Modified: Fri, 06 Aug 2021 21:13:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86fe8978f31161530210163b69b5fc67ce11e38c091caab64bb0e3734496a18`  
		Last Modified: Sat, 07 Aug 2021 04:23:35 GMT  
		Size: 7.1 MB (7097385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356115fa932b78fceaeae3fba2bd7a0ff5efa89ebf9e8b5c824b679a666489c9`  
		Last Modified: Sat, 07 Aug 2021 04:23:34 GMT  
		Size: 1.2 MB (1170513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dc07db71f320869edaa3ef484018fc6b46b8bc0671ef668991e69bbda13f51`  
		Last Modified: Sat, 07 Aug 2021 04:23:33 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:bb67f227515b2c32c0cfb3be1c48ff701cc4c525a59532d36b7166fc7aa27a21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115812998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6d4ca5bd25723d47c42919ec6d0b4bf7dd34a67583e8f3f2c95098e2142131`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:43:22 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:43:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:43:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:46:35 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:48:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:48:50 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:48:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:48:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:48:53 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:49:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:49:45 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:49:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:49:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:49:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:49:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccc77cb0a413e660cd5721d395bcec1266cde4d0528e29f1a042fabaa43ff5`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 281.9 KB (281940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d321b5acef374adaa49f78ae74b037995382f01d1353f489b334a6fc4cce81`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3f97bf1abc32dcb5c030e0f8d3abc990e9506ad219ab5cfb5827d15eaa02a`  
		Last Modified: Fri, 27 Aug 2021 17:51:47 GMT  
		Size: 104.9 MB (104940257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441e24829e5d83d1fd83b07e02e0a42bb1d31648314f63b39d44649802a9ee4a`  
		Last Modified: Fri, 27 Aug 2021 17:51:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf03157bc49c8e5393f28b8d4b4a6be766de31b9fc52348246bbe4ff2e7f7c7`  
		Last Modified: Fri, 27 Aug 2021 18:50:30 GMT  
		Size: 6.7 MB (6722103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f71cb40139c0ff03eef852eeea459437e95ca53c5ce0b8b7e1c1d49bab7a4`  
		Last Modified: Fri, 27 Aug 2021 18:50:29 GMT  
		Size: 1.3 MB (1264520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30ad513b9c90196100f4853c9b4d82e758c4acf048b7934bfa29a0fc2b27bd`  
		Last Modified: Fri, 27 Aug 2021 18:50:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:94548298bfccdd350db6f2fa27451effe035e5a1ed853df975c01413c49e19d8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2852923514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60de2cad586e35e33930f37908e1952dee5a28c8f9e23cf4c92f0c39732dfb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:09:49 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:09:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:11:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:26:22 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:27:40 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:27:40 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:30:27 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:29 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:26:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:26:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:26:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:26:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:27:28 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:27:29 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07d2bb4c99ec6467c6c9f474360867d31d27d22bc5be8432059a33a7c602a8`  
		Last Modified: Wed, 25 Aug 2021 13:38:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c31ebb0e52f79c34d0f70b88124ab4959963315dd2da2ec7117063a82d1392`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1935f777314159e43ee24dde17dba33b985a315578d33ec24796ba0ad27f679c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae930e0413fc2f7343e0b46be3ab58503ac4c137e8e6f83c7341838a22c88f3c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6bfd344bdb877d2969098eeb083c114ac4a7ef914d7dcf8eaef4d16e1e248c`  
		Last Modified: Wed, 25 Aug 2021 13:39:17 GMT  
		Size: 25.5 MB (25479918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffc00e2e1aed22bd02a7ac4e30d76d19f6caf0f9897e84d157e7af3c568f644`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f60594f1e4d8c227175212ac0226bec052e45a6f2ac058aa4845f0adc2c70a`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 341.3 KB (341318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67dd63dbd9960fb77efe3da2635624315e5b230e9d0136ff6a61c7667e1e25b`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6af958e54fca1b743938132e070c93737a923c10c0d37af843b754221072e`  
		Last Modified: Wed, 25 Aug 2021 13:41:52 GMT  
		Size: 139.4 MB (139357921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954ad9cafb5aec23d9fb11abca774323d6a853aa361ffcedad5613494b23c93`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98dafaec861f86e2303a05ac82fb338249638e4d85085798cdc5e9fc5b76f27`  
		Last Modified: Wed, 25 Aug 2021 19:29:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc818de352f19f2004712cdda39706ad5004b4c1271cc42d8a60233611cf64`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821ec8a9a1e85d66580448a6b4f6618fe1332d02415302a648a0ec0fb4f074db`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8471a6951d101eba4be159c56c730b5092e3dc7186f71902b34a8c2fd450fa97`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b1f0605dc501c2eb14f989b6a14b369106a5e41c5a9716ebc06c6afbbc0d81`  
		Last Modified: Wed, 25 Aug 2021 19:29:51 GMT  
		Size: 1.7 MB (1728504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c8468929fba91c5ee2288a255b1e7619f9c09a434d631fd20768cfcbd17d14`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:94c1c66eeae5feaeaca8684ac69bab2e5615335d9b8e1c4c27ab2743c0e1de8b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6442269359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b446fe4bd1058c21b63219634d88a9d9df5a9f31133e2434851d9e95305923`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:16:30 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:16:31 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:16:32 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:16:33 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:18:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:48 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:31:48 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:31:49 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:34:39 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:34:41 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:27:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:27:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:27:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:27:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:28:29 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:28:30 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f574487f5e33222a294b80d8246d04988a26a38908346c254fa2647c5a7e028d`  
		Last Modified: Wed, 25 Aug 2021 13:39:45 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e1bdad4b79465c250e34a289c1b634c4874290ec1fa9da12f91124ba323cb8`  
		Last Modified: Wed, 25 Aug 2021 13:39:44 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ca6c7d62e34b14c38c401eb0e5cd89bf7ec9b271c80606691b154e354576ef`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b8e5d43bb747a0877294acd5f9e1e22f072cc43f97874b9ecb708b70e7d96`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c80e7cfb2acdd3bfa5d45d3d78106e313290ca31797c9e09c7a33d383b758e`  
		Last Modified: Wed, 25 Aug 2021 13:40:10 GMT  
		Size: 25.4 MB (25442011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf57eb8b3d45fecbf8fca6bdbb800cf361cce365cd094eb059a82bcb44c0087`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd29eb1ef50bd4fe724ece3a9561ae93cea7d7509126824fded0df0cc4ecdec6`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 344.7 KB (344707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6512f7ffc77c76242888df38f980f80b78fb3a8230566c403838cebeb4bae3`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b245d14d9e193cc5f9cf2a6bd0a099a540ab40c551d463cf481046f9e6dd49ac`  
		Last Modified: Wed, 25 Aug 2021 13:42:48 GMT  
		Size: 143.8 MB (143814166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2271ca3757592eb20dd26ef0b75f72a643a18726ee620f0fda7fc8ab71cc298`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11ee28031df8b44b2509e14bc335b9f37b5f48c3f5bf4e87320948b77e105a`  
		Last Modified: Wed, 25 Aug 2021 19:30:11 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7174be725fdce80ce4b63ab3473b11cb9648e547860d9b802c707bde14e7d9`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8260167642582440a4feef71fce5ddd65334d08b35273698016831c005702fb`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782a41a0abba09324b19eca4010a0c1f4a008f0499b619f1c4acf139b4c67b36`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd614c1c73b684c14eaf7326f746b956f12566201e4ecfe8b836bd436a81f8`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.7 MB (1684554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccc99ea70e3e635c9add2b09e371e07e5ab90668b19b7837f02ed91f8d20c85`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:b4ab80f23735ff30454053be49cfe2e59002772535099b99393a029444628b53
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
$ docker pull caddy@sha256:024148c65604529e01fe96436356aef6adc9737caf5784ee97639dc0178c0e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116836974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67f775001477b06c70ee78b6bf98a0ff2eb5c9a458dc030e5c730526e487f8e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:20:55 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:20:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:20:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:23:31 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:25:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:25:15 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:25:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:25:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:25:17 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:15:27 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:15:27 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:15:27 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:15:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:15:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:15:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:15:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e108acfc2dec423245b992f059c15efa90d3da68d666891f88e21cf9ed3044`  
		Last Modified: Fri, 27 Aug 2021 17:26:14 GMT  
		Size: 281.5 KB (281498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d12eec82106ee897382a4e0f5f4012bb993a2abb41ea43f6055affa263792`  
		Last Modified: Fri, 27 Aug 2021 17:26:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba5eda52a4c5e66ad77248b778eeaabf785c0ef090e85270075e82189ccdfc4`  
		Last Modified: Fri, 27 Aug 2021 17:27:13 GMT  
		Size: 105.8 MB (105802322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb85018fe45e8393802b1c7b0b50c6e376a6ca1e8e95626bde089498a365f36`  
		Last Modified: Fri, 27 Aug 2021 17:26:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90db72e3ed64553e72bfe368d98a62d9a915cccbf3fa0c25590581cd4a3cfb5`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 6.6 MB (6626826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2349f3cb068e4777bdf9bcdd5798e514be84f8a1b7c4f6c2cfbfe2ee83c11dcd`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 1.3 MB (1311166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b310272a238f2d14deb416889fbea68278aa777bf5de85c3c294752976cd54`  
		Last Modified: Fri, 27 Aug 2021 18:15:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a2633b70d3d99f56930313cbc6c8e60f9cb84d8a247952f70ecde4b3d287a61f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112621949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995bf035b94c22d1dfae95d63886ec0360983d1862a4f0b9934cfad4c223eecf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:51:48 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:51:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:51:50 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:56:06 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:58:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:58:48 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:58:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:58:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:58:51 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:58:16 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:58:16 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:58:17 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:58:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:58:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:58:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:58:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def35433210b819c72fc8c3f4cefb914a4d2072a396498b271719a29363f24a2`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 281.7 KB (281662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fbd33b2207f0f6c992e5356a6285f8362b9ddf3f61650c7493aa2568c9fa1`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8584a59dc2c89569cc10317112977b3957c6ab4369fad184c5d8f616e7bf78ba`  
		Last Modified: Fri, 27 Aug 2021 18:03:31 GMT  
		Size: 102.0 MB (102005169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28236e9ee5408a1ebfbc1993365e25c57923224e6608703e02685d3aada63456`  
		Last Modified: Fri, 27 Aug 2021 18:02:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bde7b63fd968f5c9eceab8094063f4937b1da8306aa777963db7cbb714883f`  
		Last Modified: Fri, 27 Aug 2021 18:59:31 GMT  
		Size: 6.5 MB (6485279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8f7ef25d584b1a6933ca79bb2c78a3fc206f53a38ab1ddd7060ecbe2a933dd`  
		Last Modified: Fri, 27 Aug 2021 18:59:28 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bf61c4b3d04e6edd3304db5bd03a3241100e4d350312263ff17271a6dc69a6`  
		Last Modified: Fri, 27 Aug 2021 18:59:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:34333a1acab5cdd87309f11e0d23c3d4c6b8685b0160f307ba7206972d37853e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111501647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231aa2a8195b5e48739d3233aacb263ab4462039e3fdd181e304186924795270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:27:52 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 19:27:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 19:27:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:33:26 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 19:36:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 19:36:54 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 19:36:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:36:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 19:37:01 GMT
WORKDIR /go
# Sat, 07 Aug 2021 03:50:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 03:51:00 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 03:51:00 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 03:51:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 03:51:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 03:51:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 03:51:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc7b26480300ed9c6eddb3c4eb897051a740425806a7edff4973e09fae2bb8f`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 280.8 KB (280814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba13042e2b42dba9e7f0e57a60855dff15f2890b8d942f61fbdc4852a43854`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a06372885d9e72431bcb74f5cbb21c55f0607374a0dc1a7261e0fdffe19a389`  
		Last Modified: Fri, 06 Aug 2021 19:47:59 GMT  
		Size: 101.8 MB (101786462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeda0e3490d50d1412a7145a405521667a31542915116d5bca87d1f262a3ba6`  
		Last Modified: Fri, 06 Aug 2021 19:47:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c45b3f2b54d4bc0ce5312c296a0f2073fa104179f9935212b88b9e9e4981251`  
		Last Modified: Sat, 07 Aug 2021 03:52:09 GMT  
		Size: 5.8 MB (5784805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e389ea9eac74a8896f796d9c785720d528a709e5ec82bf35fa05f7d36e8c2d`  
		Last Modified: Sat, 07 Aug 2021 03:52:07 GMT  
		Size: 1.2 MB (1219493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1adc87d17fa7707fc23fe9ed965dd55d2704211e52c5a765628d42ba2439dab`  
		Last Modified: Sat, 07 Aug 2021 03:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6f976dea79506be1124a40be07324506d379f104afb6b4eb7d7ac3ebd1f81143
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112055672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b827a8f7150bc8bc38ad14e96bb8ec14de011b8352d944d532735984a1f6f119`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:41:17 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:41:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:41:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:43:33 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:45:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:45:02 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:45:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:45:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:45:03 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:35:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:35:10 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:35:10 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:35:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:35:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:35:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:35:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e34390c2b14c7d6b4929bed3213d6d86bb9aa93c4ec135494e476afbb7c8ff`  
		Last Modified: Fri, 27 Aug 2021 17:46:50 GMT  
		Size: 281.7 KB (281688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f557407009b175f4d46f52d9e57a4123bc5118b57e0a250e983230d791682`  
		Last Modified: Fri, 27 Aug 2021 17:46:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b522346004414564cf2d79fa6ca0b9efd60f64f3cb1cfc754f94dea608d2a9`  
		Last Modified: Fri, 27 Aug 2021 17:48:05 GMT  
		Size: 101.1 MB (101121978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e36f943c088c76ce04cebeee6e3b83058ecf72465cbb1807ce21d94b09b892`  
		Last Modified: Fri, 27 Aug 2021 17:47:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f7d54a0c7c055c4b4d79ed1dee9267b227d3fe5987a13e382a3a92c14f30fa`  
		Last Modified: Fri, 27 Aug 2021 18:35:48 GMT  
		Size: 6.7 MB (6737926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1225f39dda93839c2256ed41c7299db86680c6c805344be7c064a34211daa`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 1.2 MB (1201538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87cf0ee91a4aba520fb94188e3d73181288f133c2b42cc0add124bc59519f0`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4cb744a2c30bef1fce63b25f25090e9a6fba23d518fbfb8a67f2de5437567654
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110962703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc63a956570ca25fb6e8cda280b13ba663c3f8268fcfd235e0f50e7efe03073`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:02:31 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 21:02:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 21:02:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:06:00 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 21:07:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 21:08:01 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 21:08:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:08:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 21:08:22 GMT
WORKDIR /go
# Sat, 07 Aug 2021 04:22:15 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 04:22:17 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 04:22:21 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 04:22:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 04:22:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 04:22:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 04:22:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f69fce9d10f5a5c047377039cda1fd5125aae4ec022be3dd7aede58be5a483`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 283.6 KB (283642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fdcb934d4034adf5e88a3b7bff7a633580eb8c0f18480df4123a14c499558b`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c6309d0f42f3d590978baeb06a18f86672f414b4fd6b6c0167fbaf5bc68502`  
		Last Modified: Fri, 06 Aug 2021 21:13:47 GMT  
		Size: 99.6 MB (99599293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6b0f08798744f7a5f5fbd19a9db24d1ce885fdb4cf4cc03cb9016e172748d1`  
		Last Modified: Fri, 06 Aug 2021 21:13:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86fe8978f31161530210163b69b5fc67ce11e38c091caab64bb0e3734496a18`  
		Last Modified: Sat, 07 Aug 2021 04:23:35 GMT  
		Size: 7.1 MB (7097385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356115fa932b78fceaeae3fba2bd7a0ff5efa89ebf9e8b5c824b679a666489c9`  
		Last Modified: Sat, 07 Aug 2021 04:23:34 GMT  
		Size: 1.2 MB (1170513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dc07db71f320869edaa3ef484018fc6b46b8bc0671ef668991e69bbda13f51`  
		Last Modified: Sat, 07 Aug 2021 04:23:33 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bb67f227515b2c32c0cfb3be1c48ff701cc4c525a59532d36b7166fc7aa27a21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115812998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6d4ca5bd25723d47c42919ec6d0b4bf7dd34a67583e8f3f2c95098e2142131`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:43:22 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:43:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:43:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:46:35 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:48:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:48:50 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:48:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:48:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:48:53 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:49:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:49:45 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:49:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:49:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:49:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:49:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccc77cb0a413e660cd5721d395bcec1266cde4d0528e29f1a042fabaa43ff5`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 281.9 KB (281940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d321b5acef374adaa49f78ae74b037995382f01d1353f489b334a6fc4cce81`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3f97bf1abc32dcb5c030e0f8d3abc990e9506ad219ab5cfb5827d15eaa02a`  
		Last Modified: Fri, 27 Aug 2021 17:51:47 GMT  
		Size: 104.9 MB (104940257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441e24829e5d83d1fd83b07e02e0a42bb1d31648314f63b39d44649802a9ee4a`  
		Last Modified: Fri, 27 Aug 2021 17:51:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf03157bc49c8e5393f28b8d4b4a6be766de31b9fc52348246bbe4ff2e7f7c7`  
		Last Modified: Fri, 27 Aug 2021 18:50:30 GMT  
		Size: 6.7 MB (6722103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f71cb40139c0ff03eef852eeea459437e95ca53c5ce0b8b7e1c1d49bab7a4`  
		Last Modified: Fri, 27 Aug 2021 18:50:29 GMT  
		Size: 1.3 MB (1264520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30ad513b9c90196100f4853c9b4d82e758c4acf048b7934bfa29a0fc2b27bd`  
		Last Modified: Fri, 27 Aug 2021 18:50:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a650332bf33eaced67086712173ed2278573f04f8fe94b11682e52eb1222d4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:94548298bfccdd350db6f2fa27451effe035e5a1ed853df975c01413c49e19d8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2852923514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60de2cad586e35e33930f37908e1952dee5a28c8f9e23cf4c92f0c39732dfb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:09:49 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:09:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:11:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:26:22 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:27:40 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:27:40 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:30:27 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:29 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:26:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:26:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:26:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:26:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:27:28 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:27:29 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07d2bb4c99ec6467c6c9f474360867d31d27d22bc5be8432059a33a7c602a8`  
		Last Modified: Wed, 25 Aug 2021 13:38:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c31ebb0e52f79c34d0f70b88124ab4959963315dd2da2ec7117063a82d1392`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1935f777314159e43ee24dde17dba33b985a315578d33ec24796ba0ad27f679c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae930e0413fc2f7343e0b46be3ab58503ac4c137e8e6f83c7341838a22c88f3c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6bfd344bdb877d2969098eeb083c114ac4a7ef914d7dcf8eaef4d16e1e248c`  
		Last Modified: Wed, 25 Aug 2021 13:39:17 GMT  
		Size: 25.5 MB (25479918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffc00e2e1aed22bd02a7ac4e30d76d19f6caf0f9897e84d157e7af3c568f644`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f60594f1e4d8c227175212ac0226bec052e45a6f2ac058aa4845f0adc2c70a`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 341.3 KB (341318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67dd63dbd9960fb77efe3da2635624315e5b230e9d0136ff6a61c7667e1e25b`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6af958e54fca1b743938132e070c93737a923c10c0d37af843b754221072e`  
		Last Modified: Wed, 25 Aug 2021 13:41:52 GMT  
		Size: 139.4 MB (139357921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954ad9cafb5aec23d9fb11abca774323d6a853aa361ffcedad5613494b23c93`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98dafaec861f86e2303a05ac82fb338249638e4d85085798cdc5e9fc5b76f27`  
		Last Modified: Wed, 25 Aug 2021 19:29:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc818de352f19f2004712cdda39706ad5004b4c1271cc42d8a60233611cf64`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821ec8a9a1e85d66580448a6b4f6618fe1332d02415302a648a0ec0fb4f074db`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8471a6951d101eba4be159c56c730b5092e3dc7186f71902b34a8c2fd450fa97`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b1f0605dc501c2eb14f989b6a14b369106a5e41c5a9716ebc06c6afbbc0d81`  
		Last Modified: Wed, 25 Aug 2021 19:29:51 GMT  
		Size: 1.7 MB (1728504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c8468929fba91c5ee2288a255b1e7619f9c09a434d631fd20768cfcbd17d14`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:7ebaf26507754bcf51a3c839f0a4cdec367302d2c4f69b1f816c2f1f8fd2697c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4583; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:94c1c66eeae5feaeaca8684ac69bab2e5615335d9b8e1c4c27ab2743c0e1de8b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6442269359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b446fe4bd1058c21b63219634d88a9d9df5a9f31133e2434851d9e95305923`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:16:30 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:16:31 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:16:32 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:16:33 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:18:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:48 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:31:48 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:31:49 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:34:39 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:34:41 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:27:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:27:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:27:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:27:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:28:29 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:28:30 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f574487f5e33222a294b80d8246d04988a26a38908346c254fa2647c5a7e028d`  
		Last Modified: Wed, 25 Aug 2021 13:39:45 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e1bdad4b79465c250e34a289c1b634c4874290ec1fa9da12f91124ba323cb8`  
		Last Modified: Wed, 25 Aug 2021 13:39:44 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ca6c7d62e34b14c38c401eb0e5cd89bf7ec9b271c80606691b154e354576ef`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b8e5d43bb747a0877294acd5f9e1e22f072cc43f97874b9ecb708b70e7d96`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c80e7cfb2acdd3bfa5d45d3d78106e313290ca31797c9e09c7a33d383b758e`  
		Last Modified: Wed, 25 Aug 2021 13:40:10 GMT  
		Size: 25.4 MB (25442011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf57eb8b3d45fecbf8fca6bdbb800cf361cce365cd094eb059a82bcb44c0087`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd29eb1ef50bd4fe724ece3a9561ae93cea7d7509126824fded0df0cc4ecdec6`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 344.7 KB (344707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6512f7ffc77c76242888df38f980f80b78fb3a8230566c403838cebeb4bae3`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b245d14d9e193cc5f9cf2a6bd0a099a540ab40c551d463cf481046f9e6dd49ac`  
		Last Modified: Wed, 25 Aug 2021 13:42:48 GMT  
		Size: 143.8 MB (143814166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2271ca3757592eb20dd26ef0b75f72a643a18726ee620f0fda7fc8ab71cc298`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11ee28031df8b44b2509e14bc335b9f37b5f48c3f5bf4e87320948b77e105a`  
		Last Modified: Wed, 25 Aug 2021 19:30:11 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7174be725fdce80ce4b63ab3473b11cb9648e547860d9b802c707bde14e7d9`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8260167642582440a4feef71fce5ddd65334d08b35273698016831c005702fb`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782a41a0abba09324b19eca4010a0c1f4a008f0499b619f1c4acf139b4c67b36`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd614c1c73b684c14eaf7326f746b956f12566201e4ecfe8b836bd436a81f8`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.7 MB (1684554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccc99ea70e3e635c9add2b09e371e07e5ab90668b19b7837f02ed91f8d20c85`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:e5e5fb2f39e631146f8c890d36e0a2e6e150c66d5ee959a580002e4032761392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:277245d2976e25118dde31aa817da26aab9a54b716478e335e7e47a655680fdf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdb54faaf1277fc5d472259e6d51ac14101b59691359db53c189a9f55df03c8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:21:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:21:12 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:22:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:22:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:22:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:22:18 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:22:19 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:22:20 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:22:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:22:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:22:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:22:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:22:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:22:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:22:28 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:22:29 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:22:30 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:23:15 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:23:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc78244c47d63e7118efa5a81aeac258859631816cf0d2e335045eddd6d4562c`  
		Last Modified: Wed, 25 Aug 2021 19:29:08 GMT  
		Size: 390.1 KB (390074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e85659c5ef3d6f1826cce92e5c35cbda668ec96e58661902ea89472385a68`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad534458f62e8592943908290a647cce35c3f5ed0761b80f7d17f55393900e`  
		Last Modified: Wed, 25 Aug 2021 19:29:10 GMT  
		Size: 12.0 MB (12023423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e1aa1a15f7618a90c91ce39aeb28f0b14d0fb039a0a5c387e2d7a4460443aa`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a259cd0cf699d1891ff65f72aaf75b8b53d32409fdbab40fa8aa3594f4edb`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb72b357bee0361ca5587e675d3a832276f086a2d6535147bfe92a000cf044f`  
		Last Modified: Wed, 25 Aug 2021 19:29:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbe28f726b8cddbd0398281cfc45f2dc82f378bef80fa1dfe4dec201451721`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a73648024b9f42aeeda4c4309ba545e089e6943b686c93ea09cec6ac83373`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ad45ece5f60db2673be4be17ca0ac1ff391d32d88f7a84e2e671fca6744e0`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424371920e55efd886bea3b4671eca80436677674986f299b919e72c49d4289`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2b299f27503c9be94a9a16c137b08ba7e2b84cc07b96a281d4b2886b231f0`  
		Last Modified: Wed, 25 Aug 2021 19:29:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c231726719db989f9746b39a4b4b9b54646376e1dc36c124a1401fc15132`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ae0be18044dcf67b8832f125744410261cc8601712176399a3cd632b8843`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b94a88e7f4db3aa538dad13b42b51168525142c8268098dbe8a7175decee6`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0f35247abb67063d217ea9963f29270e1716b21409196f0e935710342a9dd9`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fa12b6daf14192bb460b568c8c3f65625b384fbcfa33e4b227d39de751374d`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43dbbbd0c30fabb616088a2f902ad0177c216707c4e134d10b9a1cd4fde8cb`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee931681f757a39ac6ce152aa1d64f251a68f63dca6dbe3459c2cec9bed0d90e`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deb6e04a956a5c619ff2eb344a4e5fcf8384d890b8120ce2ffd91cf20e0b5f`  
		Last Modified: Wed, 25 Aug 2021 19:29:00 GMT  
		Size: 320.7 KB (320709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b510aa21fdb81bb0a2156b0a977a69ea8187f959ceb05869b1450d9359814`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:bd0551e2eeef6d131272af5e4214599dfc85e2a18d421264005a4f8dc3025a02
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283675023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96c9f880047fab4000d8bad0dceb15c3e478898181805e15b864f3ae980f11`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:24:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:24:21 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:25:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:25:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:25:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:25:25 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:25:26 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:25:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:25:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:25:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:25:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:25:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:25:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:25:35 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:25:36 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:25:37 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:26:16 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:26:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9dee8014da227cc8c6b8d14f6464fefc307c265b07a34d6e2ccc5de24a92a`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 352.7 KB (352700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d26c5819d131639ab53b8e099ab2ed93c63f759072d3a5ce4b9f69f13b8a66`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb3ea0fdbcaf7cab1dbac86676ab00ca78ebf68e3b5c476c5984201c357976`  
		Last Modified: Wed, 25 Aug 2021 19:29:35 GMT  
		Size: 12.0 MB (12025369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a331953cb55eb8482f8b09c1ccb30b06198b0da91f196aa230d56d4f626c3`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c66a58bae64f63c34265474f15131687cba250a5cbeb2166a25d383630b68`  
		Last Modified: Wed, 25 Aug 2021 19:29:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b60346916eaf0cd70873400273d0f0de4f72aa7ee5a5bd6a8cfbe446d62499`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74af1f53b1dc6d2f58a23760f463877d707150f1cae25c0ca6a727c64cd7e9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4467e0d432e5bba7c8e197c057837e438ae63c8748b9765a8d7591c0ea12c0`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c92db8b514f6d653c3d0ba5a7e695e808f5880504124fb94648c10590f7f3c9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63a5575b8310dcb9cbe40352e7753a4bb8f66f1c3fbea055abda03136638d6`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415f534f6818ea980cf13f9a08c0efb9d60c9f86760129563e203ba93e399c8`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be354de1af39afc991030861814f135bfde0267a02f004fd4caf9ccc31d0bfd`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a0ebb3c5c8d126c85ccbad571fef0051ac62cfec3fe5885c82110381049ed9`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893f40ed74354bd380ee49a7141c654ea10f5a43f1e050539bde502c7214c9f`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd03947508d81a8a5c939b4a1697e4cf18bc8722cc1650732f8df2c6924941`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c43d724632362e78f09ee6bf53a8359cdd6db65300cb3687f2ad3a59e1a5d`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaec774cf06dd02e7ebdf8d5e9aa9b8d4578a60c7a54ce84421910922396b7`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb3d76a117ff8038563015df19972676ff4aea085431ef698f57799559b334`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341d5f41a06e42738b97ffd6ca2835680879ba4113b882c5cd8accd857c0551`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 305.6 KB (305571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd0dece66bb4a5f39d723d7d27311fa04d1de60c084735f41cb588c7b4d5701`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:50783893bffe979472583ab27a4a4346cdeb5895077ff67af22283b65699eda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:277245d2976e25118dde31aa817da26aab9a54b716478e335e7e47a655680fdf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdb54faaf1277fc5d472259e6d51ac14101b59691359db53c189a9f55df03c8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:21:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:21:12 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:22:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:22:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:22:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:22:18 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:22:19 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:22:20 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:22:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:22:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:22:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:22:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:22:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:22:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:22:28 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:22:29 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:22:30 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:23:15 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:23:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc78244c47d63e7118efa5a81aeac258859631816cf0d2e335045eddd6d4562c`  
		Last Modified: Wed, 25 Aug 2021 19:29:08 GMT  
		Size: 390.1 KB (390074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e85659c5ef3d6f1826cce92e5c35cbda668ec96e58661902ea89472385a68`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad534458f62e8592943908290a647cce35c3f5ed0761b80f7d17f55393900e`  
		Last Modified: Wed, 25 Aug 2021 19:29:10 GMT  
		Size: 12.0 MB (12023423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e1aa1a15f7618a90c91ce39aeb28f0b14d0fb039a0a5c387e2d7a4460443aa`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a259cd0cf699d1891ff65f72aaf75b8b53d32409fdbab40fa8aa3594f4edb`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb72b357bee0361ca5587e675d3a832276f086a2d6535147bfe92a000cf044f`  
		Last Modified: Wed, 25 Aug 2021 19:29:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbe28f726b8cddbd0398281cfc45f2dc82f378bef80fa1dfe4dec201451721`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a73648024b9f42aeeda4c4309ba545e089e6943b686c93ea09cec6ac83373`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ad45ece5f60db2673be4be17ca0ac1ff391d32d88f7a84e2e671fca6744e0`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424371920e55efd886bea3b4671eca80436677674986f299b919e72c49d4289`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2b299f27503c9be94a9a16c137b08ba7e2b84cc07b96a281d4b2886b231f0`  
		Last Modified: Wed, 25 Aug 2021 19:29:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c231726719db989f9746b39a4b4b9b54646376e1dc36c124a1401fc15132`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ae0be18044dcf67b8832f125744410261cc8601712176399a3cd632b8843`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b94a88e7f4db3aa538dad13b42b51168525142c8268098dbe8a7175decee6`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0f35247abb67063d217ea9963f29270e1716b21409196f0e935710342a9dd9`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fa12b6daf14192bb460b568c8c3f65625b384fbcfa33e4b227d39de751374d`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43dbbbd0c30fabb616088a2f902ad0177c216707c4e134d10b9a1cd4fde8cb`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee931681f757a39ac6ce152aa1d64f251a68f63dca6dbe3459c2cec9bed0d90e`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deb6e04a956a5c619ff2eb344a4e5fcf8384d890b8120ce2ffd91cf20e0b5f`  
		Last Modified: Wed, 25 Aug 2021 19:29:00 GMT  
		Size: 320.7 KB (320709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b510aa21fdb81bb0a2156b0a977a69ea8187f959ceb05869b1450d9359814`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:e8353d4e8df77074d824ddc338a6a8784add4f27abe1cda1b230b6a27533edd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4583; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:bd0551e2eeef6d131272af5e4214599dfc85e2a18d421264005a4f8dc3025a02
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283675023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96c9f880047fab4000d8bad0dceb15c3e478898181805e15b864f3ae980f11`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:24:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:24:21 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:25:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:25:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:25:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:25:25 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:25:26 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:25:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:25:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:25:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:25:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:25:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:25:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:25:35 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:25:36 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:25:37 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:26:16 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:26:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9dee8014da227cc8c6b8d14f6464fefc307c265b07a34d6e2ccc5de24a92a`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 352.7 KB (352700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d26c5819d131639ab53b8e099ab2ed93c63f759072d3a5ce4b9f69f13b8a66`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb3ea0fdbcaf7cab1dbac86676ab00ca78ebf68e3b5c476c5984201c357976`  
		Last Modified: Wed, 25 Aug 2021 19:29:35 GMT  
		Size: 12.0 MB (12025369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a331953cb55eb8482f8b09c1ccb30b06198b0da91f196aa230d56d4f626c3`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c66a58bae64f63c34265474f15131687cba250a5cbeb2166a25d383630b68`  
		Last Modified: Wed, 25 Aug 2021 19:29:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b60346916eaf0cd70873400273d0f0de4f72aa7ee5a5bd6a8cfbe446d62499`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74af1f53b1dc6d2f58a23760f463877d707150f1cae25c0ca6a727c64cd7e9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4467e0d432e5bba7c8e197c057837e438ae63c8748b9765a8d7591c0ea12c0`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c92db8b514f6d653c3d0ba5a7e695e808f5880504124fb94648c10590f7f3c9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63a5575b8310dcb9cbe40352e7753a4bb8f66f1c3fbea055abda03136638d6`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415f534f6818ea980cf13f9a08c0efb9d60c9f86760129563e203ba93e399c8`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be354de1af39afc991030861814f135bfde0267a02f004fd4caf9ccc31d0bfd`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a0ebb3c5c8d126c85ccbad571fef0051ac62cfec3fe5885c82110381049ed9`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893f40ed74354bd380ee49a7141c654ea10f5a43f1e050539bde502c7214c9f`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd03947508d81a8a5c939b4a1697e4cf18bc8722cc1650732f8df2c6924941`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c43d724632362e78f09ee6bf53a8359cdd6db65300cb3687f2ad3a59e1a5d`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaec774cf06dd02e7ebdf8d5e9aa9b8d4578a60c7a54ce84421910922396b7`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb3d76a117ff8038563015df19972676ff4aea085431ef698f57799559b334`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341d5f41a06e42738b97ffd6ca2835680879ba4113b882c5cd8accd857c0551`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 305.6 KB (305571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd0dece66bb4a5f39d723d7d27311fa04d1de60c084735f41cb588c7b4d5701`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.3`

```console
$ docker pull caddy@sha256:d235036337fad2117f058e44b0ce4813f974924e03ff629da08dbee7c6be5e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `caddy:2.4.3` - linux; amd64

```console
$ docker pull caddy@sha256:77f27025e0e1e0ab97bc931db61d24f9ac41591e17576ab46c4b508afbccacd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14648199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8a741f4852592d8634aa37c7f351ae4f4e7b4a9a2594df54603ac48cbdad74`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:11:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 11 May 2021 01:04:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 19:19:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 19:19:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 19:19:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 19:19:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 19:19:32 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 19:19:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 443
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 19:19:34 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 19:19:34 GMT
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
	-	`sha256:16798e0582fce7af9c2ba2c8ee4990d0fd1e58384e170ee9937486253d67bbf1`  
		Last Modified: Tue, 11 May 2021 01:05:00 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d589bc046eca71df600301462981053bf178fcd31d4b2c882ca05aec70bacd`  
		Last Modified: Thu, 24 Jun 2021 19:19:59 GMT  
		Size: 11.5 MB (11529821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8ce9421f330c9a085ac8f059d2dd53feabf795c461d4f43b596d0302b1cf9`  
		Last Modified: Thu, 24 Jun 2021 19:19:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3` - linux; arm variant v6

```console
$ docker pull caddy@sha256:615389b06a74c80f0494cdc47da7b9f565cadd8cd715e39d7b65aaaf2937b6cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13816604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac08c3d5e13d15da24bbe2b6e7bd0fe9a42212188c3f33467bb1f38dfdb0b51`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 22:32:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 22:32:24 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 22:32:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 22:32:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 22:32:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 22:32:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 22:32:36 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 22:32:37 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 22:32:37 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 22:32:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 22:32:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 22:32:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 22:32:44 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:32:45 GMT
EXPOSE 443
# Fri, 30 Jul 2021 22:32:46 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 22:32:46 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 22:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18943f91e0b98a5ee778a791cc00f627dfc62e6163be04be39d8dfca48ca309`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 300.5 KB (300515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6779ad883f93abbe8842bc2dd07f67be174891b4b835e18a7eccb5a738ee0eb9`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6cb30c4e53dad6055df249f24807530e7530d534f18b81671b80de7b8b0ad2`  
		Last Modified: Fri, 30 Jul 2021 22:34:16 GMT  
		Size: 10.9 MB (10887954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a803ba6ef03f0246aec715857792f54efc64816b24b563beee84263dd1ad439`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c382c62559cf6348cccc2048f7f6e3234ad6c3322fa778f0d7ab3fbe27cd44e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13593493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c6676bf8617209d68af4cbdd3c3edb6084cbd01e6c7f00b706fab8934f311a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Fri, 30 Jul 2021 18:36:39 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:13:40 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 02:13:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 02:13:44 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 02:13:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 02:13:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 02:13:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 02:13:56 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 443
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 02:13:58 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 02:13:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf509b321d9275e96242772f4cd73ad8da2970e30e18c0f2326ed91777442e`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 299.7 KB (299672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16416239cfcd26ea4cc02aaf7ac5511b6ea5d6cc672046b6e61d90f9c59ffaac`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de14f3facde68cf2e2470839f96bb111537c6b40d15a1b28c47c6568261ee15`  
		Last Modified: Sat, 31 Jul 2021 02:15:20 GMT  
		Size: 10.9 MB (10863669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6b241bda44fe422ccd7c0c967fb01d2d7a191df7b0628d9c44df2d18dd5445`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ee1b9ce06277bd5c34b2d9a6908cdb3028aa838fa75e5c6e1e32d2cabb417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13464756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a697a3b5305c041fd956ba80c8845676041e98bce128a69e70074e5abe9653dd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 15 Jun 2021 22:32:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 18:39:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 18:39:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 18:39:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 443
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 18:39:33 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 18:39:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d0b72044755ebd2b829600b94a69aa9096bbb4bf9a01c1795b5b245261b99a`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 300.6 KB (300631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abde659ccf1d73128ef1e71a9701b014e0f27d4abf15b3d410d0474cdd0adb95`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75403ccf5c23126b5dca334871ec0096a90d0fb85f47be1ecba3904921529c0`  
		Last Modified: Thu, 24 Jun 2021 18:40:18 GMT  
		Size: 10.4 MB (10446098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a85edeaa46fe5e0185f11a1a1801c0d0458e59897d3c04e97136df1c496663`  
		Last Modified: Thu, 24 Jun 2021 18:40:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3` - linux; ppc64le

```console
$ docker pull caddy@sha256:fff2119338c215eceae68398483da801f5daf8bb5405c7ed8db5769aeb367cd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13173634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced11b632073f0e249ba02b8326f0c1ccf6c154d4340342b38c8b3f830c37e70`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:24:49 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Fri, 30 Jul 2021 17:24:54 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:36:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 00:36:51 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 00:36:54 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 00:37:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 00:37:10 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 00:37:12 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 00:37:14 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 00:37:17 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 00:37:23 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 00:37:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 00:37:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 00:37:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 00:37:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 00:37:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 00:37:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 00:37:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 00:38:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 00:38:06 GMT
EXPOSE 80
# Sat, 31 Jul 2021 00:38:09 GMT
EXPOSE 443
# Sat, 31 Jul 2021 00:38:16 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 00:38:25 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 00:38:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396ee5e0a948db1cebd77a9b357abbc39c60dc4caf97f87f759a1f232a291da5`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 302.5 KB (302545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c405a506bbc65ab625ac9298a31abc4a1871eef7b93ff4fbc6a25fb9db591a4`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ac195b709078a7d439cd22a970947cb2ed3f9cd136a8d51324ab3d3c746625`  
		Last Modified: Sat, 31 Jul 2021 00:39:16 GMT  
		Size: 10.1 MB (10051943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2c9f1da5ba05b5656393520168363c5d8a223167645bc0a4451fcd4c2f5447`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3` - linux; s390x

```console
$ docker pull caddy@sha256:576d8d6d9dead63f0cc0db39ad0fb1e9e9539bf5b23a8b70623b7e8f40d916a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14005959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6114aef9a435617ae101cc26569f3f2103cd2c999ef3e41df780270222452a1f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:41:41 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Fri, 30 Jul 2021 17:41:42 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 23:50:44 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 23:50:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 23:50:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 23:50:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 23:50:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 23:50:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 80
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 443
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 23:50:52 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 23:50:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de364003ff53d3ed839a7d8fd8cc6c59936d04b22886595d954e5c9929cfe0e1`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 300.9 KB (300858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d9b83bb28f1c9bc97f9a4907425be62b28dd687b54e3b8d461b2e40203110d`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076584d90c472ad966977bc9f55f53439edb7b5169fa684c1a70a1ea682037ca`  
		Last Modified: Fri, 30 Jul 2021 23:51:34 GMT  
		Size: 11.1 MB (11096451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f126f1c964e9405478f4683dd4b8e93297166d84566a652fe658f36bad6390c`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:277245d2976e25118dde31aa817da26aab9a54b716478e335e7e47a655680fdf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdb54faaf1277fc5d472259e6d51ac14101b59691359db53c189a9f55df03c8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:21:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:21:12 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:22:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:22:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:22:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:22:18 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:22:19 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:22:20 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:22:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:22:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:22:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:22:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:22:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:22:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:22:28 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:22:29 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:22:30 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:23:15 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:23:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc78244c47d63e7118efa5a81aeac258859631816cf0d2e335045eddd6d4562c`  
		Last Modified: Wed, 25 Aug 2021 19:29:08 GMT  
		Size: 390.1 KB (390074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e85659c5ef3d6f1826cce92e5c35cbda668ec96e58661902ea89472385a68`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad534458f62e8592943908290a647cce35c3f5ed0761b80f7d17f55393900e`  
		Last Modified: Wed, 25 Aug 2021 19:29:10 GMT  
		Size: 12.0 MB (12023423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e1aa1a15f7618a90c91ce39aeb28f0b14d0fb039a0a5c387e2d7a4460443aa`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a259cd0cf699d1891ff65f72aaf75b8b53d32409fdbab40fa8aa3594f4edb`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb72b357bee0361ca5587e675d3a832276f086a2d6535147bfe92a000cf044f`  
		Last Modified: Wed, 25 Aug 2021 19:29:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbe28f726b8cddbd0398281cfc45f2dc82f378bef80fa1dfe4dec201451721`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a73648024b9f42aeeda4c4309ba545e089e6943b686c93ea09cec6ac83373`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ad45ece5f60db2673be4be17ca0ac1ff391d32d88f7a84e2e671fca6744e0`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424371920e55efd886bea3b4671eca80436677674986f299b919e72c49d4289`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2b299f27503c9be94a9a16c137b08ba7e2b84cc07b96a281d4b2886b231f0`  
		Last Modified: Wed, 25 Aug 2021 19:29:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c231726719db989f9746b39a4b4b9b54646376e1dc36c124a1401fc15132`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ae0be18044dcf67b8832f125744410261cc8601712176399a3cd632b8843`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b94a88e7f4db3aa538dad13b42b51168525142c8268098dbe8a7175decee6`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0f35247abb67063d217ea9963f29270e1716b21409196f0e935710342a9dd9`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fa12b6daf14192bb460b568c8c3f65625b384fbcfa33e4b227d39de751374d`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43dbbbd0c30fabb616088a2f902ad0177c216707c4e134d10b9a1cd4fde8cb`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee931681f757a39ac6ce152aa1d64f251a68f63dca6dbe3459c2cec9bed0d90e`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deb6e04a956a5c619ff2eb344a4e5fcf8384d890b8120ce2ffd91cf20e0b5f`  
		Last Modified: Wed, 25 Aug 2021 19:29:00 GMT  
		Size: 320.7 KB (320709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b510aa21fdb81bb0a2156b0a977a69ea8187f959ceb05869b1450d9359814`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:bd0551e2eeef6d131272af5e4214599dfc85e2a18d421264005a4f8dc3025a02
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283675023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96c9f880047fab4000d8bad0dceb15c3e478898181805e15b864f3ae980f11`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:24:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:24:21 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:25:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:25:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:25:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:25:25 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:25:26 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:25:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:25:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:25:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:25:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:25:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:25:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:25:35 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:25:36 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:25:37 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:26:16 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:26:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9dee8014da227cc8c6b8d14f6464fefc307c265b07a34d6e2ccc5de24a92a`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 352.7 KB (352700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d26c5819d131639ab53b8e099ab2ed93c63f759072d3a5ce4b9f69f13b8a66`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb3ea0fdbcaf7cab1dbac86676ab00ca78ebf68e3b5c476c5984201c357976`  
		Last Modified: Wed, 25 Aug 2021 19:29:35 GMT  
		Size: 12.0 MB (12025369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a331953cb55eb8482f8b09c1ccb30b06198b0da91f196aa230d56d4f626c3`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c66a58bae64f63c34265474f15131687cba250a5cbeb2166a25d383630b68`  
		Last Modified: Wed, 25 Aug 2021 19:29:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b60346916eaf0cd70873400273d0f0de4f72aa7ee5a5bd6a8cfbe446d62499`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74af1f53b1dc6d2f58a23760f463877d707150f1cae25c0ca6a727c64cd7e9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4467e0d432e5bba7c8e197c057837e438ae63c8748b9765a8d7591c0ea12c0`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c92db8b514f6d653c3d0ba5a7e695e808f5880504124fb94648c10590f7f3c9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63a5575b8310dcb9cbe40352e7753a4bb8f66f1c3fbea055abda03136638d6`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415f534f6818ea980cf13f9a08c0efb9d60c9f86760129563e203ba93e399c8`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be354de1af39afc991030861814f135bfde0267a02f004fd4caf9ccc31d0bfd`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a0ebb3c5c8d126c85ccbad571fef0051ac62cfec3fe5885c82110381049ed9`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893f40ed74354bd380ee49a7141c654ea10f5a43f1e050539bde502c7214c9f`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd03947508d81a8a5c939b4a1697e4cf18bc8722cc1650732f8df2c6924941`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c43d724632362e78f09ee6bf53a8359cdd6db65300cb3687f2ad3a59e1a5d`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaec774cf06dd02e7ebdf8d5e9aa9b8d4578a60c7a54ce84421910922396b7`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb3d76a117ff8038563015df19972676ff4aea085431ef698f57799559b334`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341d5f41a06e42738b97ffd6ca2835680879ba4113b882c5cd8accd857c0551`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 305.6 KB (305571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd0dece66bb4a5f39d723d7d27311fa04d1de60c084735f41cb588c7b4d5701`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.3-alpine`

```console
$ docker pull caddy@sha256:f00d2e7e82418a30135cbe5c1455df6c617ee651d6f430183a8e49e3b2608359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.4.3-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:77f27025e0e1e0ab97bc931db61d24f9ac41591e17576ab46c4b508afbccacd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14648199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8a741f4852592d8634aa37c7f351ae4f4e7b4a9a2594df54603ac48cbdad74`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:11:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 11 May 2021 01:04:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 19:19:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 19:19:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 19:19:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 19:19:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 19:19:32 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 19:19:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 443
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 19:19:34 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 19:19:34 GMT
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
	-	`sha256:16798e0582fce7af9c2ba2c8ee4990d0fd1e58384e170ee9937486253d67bbf1`  
		Last Modified: Tue, 11 May 2021 01:05:00 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d589bc046eca71df600301462981053bf178fcd31d4b2c882ca05aec70bacd`  
		Last Modified: Thu, 24 Jun 2021 19:19:59 GMT  
		Size: 11.5 MB (11529821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8ce9421f330c9a085ac8f059d2dd53feabf795c461d4f43b596d0302b1cf9`  
		Last Modified: Thu, 24 Jun 2021 19:19:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:615389b06a74c80f0494cdc47da7b9f565cadd8cd715e39d7b65aaaf2937b6cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13816604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac08c3d5e13d15da24bbe2b6e7bd0fe9a42212188c3f33467bb1f38dfdb0b51`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 22:32:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 22:32:24 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 22:32:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 22:32:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 22:32:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 22:32:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 22:32:36 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 22:32:37 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 22:32:37 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 22:32:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 22:32:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 22:32:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 22:32:44 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:32:45 GMT
EXPOSE 443
# Fri, 30 Jul 2021 22:32:46 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 22:32:46 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 22:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18943f91e0b98a5ee778a791cc00f627dfc62e6163be04be39d8dfca48ca309`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 300.5 KB (300515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6779ad883f93abbe8842bc2dd07f67be174891b4b835e18a7eccb5a738ee0eb9`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6cb30c4e53dad6055df249f24807530e7530d534f18b81671b80de7b8b0ad2`  
		Last Modified: Fri, 30 Jul 2021 22:34:16 GMT  
		Size: 10.9 MB (10887954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a803ba6ef03f0246aec715857792f54efc64816b24b563beee84263dd1ad439`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c382c62559cf6348cccc2048f7f6e3234ad6c3322fa778f0d7ab3fbe27cd44e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13593493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c6676bf8617209d68af4cbdd3c3edb6084cbd01e6c7f00b706fab8934f311a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Fri, 30 Jul 2021 18:36:39 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:13:40 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 02:13:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 02:13:44 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 02:13:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 02:13:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 02:13:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 02:13:56 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 443
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 02:13:58 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 02:13:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf509b321d9275e96242772f4cd73ad8da2970e30e18c0f2326ed91777442e`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 299.7 KB (299672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16416239cfcd26ea4cc02aaf7ac5511b6ea5d6cc672046b6e61d90f9c59ffaac`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de14f3facde68cf2e2470839f96bb111537c6b40d15a1b28c47c6568261ee15`  
		Last Modified: Sat, 31 Jul 2021 02:15:20 GMT  
		Size: 10.9 MB (10863669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6b241bda44fe422ccd7c0c967fb01d2d7a191df7b0628d9c44df2d18dd5445`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ee1b9ce06277bd5c34b2d9a6908cdb3028aa838fa75e5c6e1e32d2cabb417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13464756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a697a3b5305c041fd956ba80c8845676041e98bce128a69e70074e5abe9653dd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 15 Jun 2021 22:32:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 18:39:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 18:39:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 18:39:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 443
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 18:39:33 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 18:39:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d0b72044755ebd2b829600b94a69aa9096bbb4bf9a01c1795b5b245261b99a`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 300.6 KB (300631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abde659ccf1d73128ef1e71a9701b014e0f27d4abf15b3d410d0474cdd0adb95`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75403ccf5c23126b5dca334871ec0096a90d0fb85f47be1ecba3904921529c0`  
		Last Modified: Thu, 24 Jun 2021 18:40:18 GMT  
		Size: 10.4 MB (10446098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a85edeaa46fe5e0185f11a1a1801c0d0458e59897d3c04e97136df1c496663`  
		Last Modified: Thu, 24 Jun 2021 18:40:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:fff2119338c215eceae68398483da801f5daf8bb5405c7ed8db5769aeb367cd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13173634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced11b632073f0e249ba02b8326f0c1ccf6c154d4340342b38c8b3f830c37e70`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:24:49 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Fri, 30 Jul 2021 17:24:54 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:36:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 00:36:51 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 00:36:54 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 00:37:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 00:37:10 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 00:37:12 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 00:37:14 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 00:37:17 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 00:37:23 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 00:37:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 00:37:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 00:37:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 00:37:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 00:37:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 00:37:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 00:37:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 00:38:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 00:38:06 GMT
EXPOSE 80
# Sat, 31 Jul 2021 00:38:09 GMT
EXPOSE 443
# Sat, 31 Jul 2021 00:38:16 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 00:38:25 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 00:38:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396ee5e0a948db1cebd77a9b357abbc39c60dc4caf97f87f759a1f232a291da5`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 302.5 KB (302545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c405a506bbc65ab625ac9298a31abc4a1871eef7b93ff4fbc6a25fb9db591a4`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ac195b709078a7d439cd22a970947cb2ed3f9cd136a8d51324ab3d3c746625`  
		Last Modified: Sat, 31 Jul 2021 00:39:16 GMT  
		Size: 10.1 MB (10051943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2c9f1da5ba05b5656393520168363c5d8a223167645bc0a4451fcd4c2f5447`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:576d8d6d9dead63f0cc0db39ad0fb1e9e9539bf5b23a8b70623b7e8f40d916a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14005959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6114aef9a435617ae101cc26569f3f2103cd2c999ef3e41df780270222452a1f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:41:41 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Fri, 30 Jul 2021 17:41:42 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 23:50:44 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 23:50:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 23:50:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 23:50:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 23:50:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 23:50:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 80
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 443
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 23:50:52 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 23:50:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de364003ff53d3ed839a7d8fd8cc6c59936d04b22886595d954e5c9929cfe0e1`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 300.9 KB (300858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d9b83bb28f1c9bc97f9a4907425be62b28dd687b54e3b8d461b2e40203110d`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076584d90c472ad966977bc9f55f53439edb7b5169fa684c1a70a1ea682037ca`  
		Last Modified: Fri, 30 Jul 2021 23:51:34 GMT  
		Size: 11.1 MB (11096451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f126f1c964e9405478f4683dd4b8e93297166d84566a652fe658f36bad6390c`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.3-builder`

```console
$ docker pull caddy@sha256:6d4327fca22a56f18bcb561bbf5be757c05758d8bfcab7b115d6481996285052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `caddy:2.4.3-builder` - linux; amd64

```console
$ docker pull caddy@sha256:024148c65604529e01fe96436356aef6adc9737caf5784ee97639dc0178c0e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116836974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67f775001477b06c70ee78b6bf98a0ff2eb5c9a458dc030e5c730526e487f8e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:20:55 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:20:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:20:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:23:31 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:25:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:25:15 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:25:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:25:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:25:17 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:15:27 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:15:27 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:15:27 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:15:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:15:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:15:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:15:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e108acfc2dec423245b992f059c15efa90d3da68d666891f88e21cf9ed3044`  
		Last Modified: Fri, 27 Aug 2021 17:26:14 GMT  
		Size: 281.5 KB (281498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d12eec82106ee897382a4e0f5f4012bb993a2abb41ea43f6055affa263792`  
		Last Modified: Fri, 27 Aug 2021 17:26:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba5eda52a4c5e66ad77248b778eeaabf785c0ef090e85270075e82189ccdfc4`  
		Last Modified: Fri, 27 Aug 2021 17:27:13 GMT  
		Size: 105.8 MB (105802322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb85018fe45e8393802b1c7b0b50c6e376a6ca1e8e95626bde089498a365f36`  
		Last Modified: Fri, 27 Aug 2021 17:26:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90db72e3ed64553e72bfe368d98a62d9a915cccbf3fa0c25590581cd4a3cfb5`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 6.6 MB (6626826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2349f3cb068e4777bdf9bcdd5798e514be84f8a1b7c4f6c2cfbfe2ee83c11dcd`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 1.3 MB (1311166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b310272a238f2d14deb416889fbea68278aa777bf5de85c3c294752976cd54`  
		Last Modified: Fri, 27 Aug 2021 18:15:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a2633b70d3d99f56930313cbc6c8e60f9cb84d8a247952f70ecde4b3d287a61f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112621949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995bf035b94c22d1dfae95d63886ec0360983d1862a4f0b9934cfad4c223eecf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:51:48 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:51:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:51:50 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:56:06 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:58:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:58:48 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:58:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:58:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:58:51 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:58:16 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:58:16 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:58:17 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:58:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:58:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:58:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:58:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def35433210b819c72fc8c3f4cefb914a4d2072a396498b271719a29363f24a2`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 281.7 KB (281662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fbd33b2207f0f6c992e5356a6285f8362b9ddf3f61650c7493aa2568c9fa1`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8584a59dc2c89569cc10317112977b3957c6ab4369fad184c5d8f616e7bf78ba`  
		Last Modified: Fri, 27 Aug 2021 18:03:31 GMT  
		Size: 102.0 MB (102005169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28236e9ee5408a1ebfbc1993365e25c57923224e6608703e02685d3aada63456`  
		Last Modified: Fri, 27 Aug 2021 18:02:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bde7b63fd968f5c9eceab8094063f4937b1da8306aa777963db7cbb714883f`  
		Last Modified: Fri, 27 Aug 2021 18:59:31 GMT  
		Size: 6.5 MB (6485279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8f7ef25d584b1a6933ca79bb2c78a3fc206f53a38ab1ddd7060ecbe2a933dd`  
		Last Modified: Fri, 27 Aug 2021 18:59:28 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bf61c4b3d04e6edd3304db5bd03a3241100e4d350312263ff17271a6dc69a6`  
		Last Modified: Fri, 27 Aug 2021 18:59:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:34333a1acab5cdd87309f11e0d23c3d4c6b8685b0160f307ba7206972d37853e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111501647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231aa2a8195b5e48739d3233aacb263ab4462039e3fdd181e304186924795270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:27:52 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 19:27:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 19:27:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:33:26 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 19:36:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 19:36:54 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 19:36:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:36:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 19:37:01 GMT
WORKDIR /go
# Sat, 07 Aug 2021 03:50:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 03:51:00 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 03:51:00 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 03:51:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 03:51:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 03:51:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 03:51:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc7b26480300ed9c6eddb3c4eb897051a740425806a7edff4973e09fae2bb8f`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 280.8 KB (280814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba13042e2b42dba9e7f0e57a60855dff15f2890b8d942f61fbdc4852a43854`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a06372885d9e72431bcb74f5cbb21c55f0607374a0dc1a7261e0fdffe19a389`  
		Last Modified: Fri, 06 Aug 2021 19:47:59 GMT  
		Size: 101.8 MB (101786462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeda0e3490d50d1412a7145a405521667a31542915116d5bca87d1f262a3ba6`  
		Last Modified: Fri, 06 Aug 2021 19:47:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c45b3f2b54d4bc0ce5312c296a0f2073fa104179f9935212b88b9e9e4981251`  
		Last Modified: Sat, 07 Aug 2021 03:52:09 GMT  
		Size: 5.8 MB (5784805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e389ea9eac74a8896f796d9c785720d528a709e5ec82bf35fa05f7d36e8c2d`  
		Last Modified: Sat, 07 Aug 2021 03:52:07 GMT  
		Size: 1.2 MB (1219493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1adc87d17fa7707fc23fe9ed965dd55d2704211e52c5a765628d42ba2439dab`  
		Last Modified: Sat, 07 Aug 2021 03:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6f976dea79506be1124a40be07324506d379f104afb6b4eb7d7ac3ebd1f81143
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112055672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b827a8f7150bc8bc38ad14e96bb8ec14de011b8352d944d532735984a1f6f119`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:41:17 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:41:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:41:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:43:33 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:45:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:45:02 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:45:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:45:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:45:03 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:35:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:35:10 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:35:10 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:35:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:35:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:35:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:35:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e34390c2b14c7d6b4929bed3213d6d86bb9aa93c4ec135494e476afbb7c8ff`  
		Last Modified: Fri, 27 Aug 2021 17:46:50 GMT  
		Size: 281.7 KB (281688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f557407009b175f4d46f52d9e57a4123bc5118b57e0a250e983230d791682`  
		Last Modified: Fri, 27 Aug 2021 17:46:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b522346004414564cf2d79fa6ca0b9efd60f64f3cb1cfc754f94dea608d2a9`  
		Last Modified: Fri, 27 Aug 2021 17:48:05 GMT  
		Size: 101.1 MB (101121978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e36f943c088c76ce04cebeee6e3b83058ecf72465cbb1807ce21d94b09b892`  
		Last Modified: Fri, 27 Aug 2021 17:47:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f7d54a0c7c055c4b4d79ed1dee9267b227d3fe5987a13e382a3a92c14f30fa`  
		Last Modified: Fri, 27 Aug 2021 18:35:48 GMT  
		Size: 6.7 MB (6737926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1225f39dda93839c2256ed41c7299db86680c6c805344be7c064a34211daa`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 1.2 MB (1201538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87cf0ee91a4aba520fb94188e3d73181288f133c2b42cc0add124bc59519f0`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4cb744a2c30bef1fce63b25f25090e9a6fba23d518fbfb8a67f2de5437567654
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110962703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc63a956570ca25fb6e8cda280b13ba663c3f8268fcfd235e0f50e7efe03073`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:02:31 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 21:02:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 21:02:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:06:00 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 21:07:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 21:08:01 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 21:08:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:08:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 21:08:22 GMT
WORKDIR /go
# Sat, 07 Aug 2021 04:22:15 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 04:22:17 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 04:22:21 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 04:22:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 04:22:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 04:22:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 04:22:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f69fce9d10f5a5c047377039cda1fd5125aae4ec022be3dd7aede58be5a483`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 283.6 KB (283642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fdcb934d4034adf5e88a3b7bff7a633580eb8c0f18480df4123a14c499558b`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c6309d0f42f3d590978baeb06a18f86672f414b4fd6b6c0167fbaf5bc68502`  
		Last Modified: Fri, 06 Aug 2021 21:13:47 GMT  
		Size: 99.6 MB (99599293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6b0f08798744f7a5f5fbd19a9db24d1ce885fdb4cf4cc03cb9016e172748d1`  
		Last Modified: Fri, 06 Aug 2021 21:13:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86fe8978f31161530210163b69b5fc67ce11e38c091caab64bb0e3734496a18`  
		Last Modified: Sat, 07 Aug 2021 04:23:35 GMT  
		Size: 7.1 MB (7097385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356115fa932b78fceaeae3fba2bd7a0ff5efa89ebf9e8b5c824b679a666489c9`  
		Last Modified: Sat, 07 Aug 2021 04:23:34 GMT  
		Size: 1.2 MB (1170513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dc07db71f320869edaa3ef484018fc6b46b8bc0671ef668991e69bbda13f51`  
		Last Modified: Sat, 07 Aug 2021 04:23:33 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder` - linux; s390x

```console
$ docker pull caddy@sha256:bb67f227515b2c32c0cfb3be1c48ff701cc4c525a59532d36b7166fc7aa27a21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115812998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6d4ca5bd25723d47c42919ec6d0b4bf7dd34a67583e8f3f2c95098e2142131`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:43:22 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:43:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:43:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:46:35 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:48:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:48:50 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:48:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:48:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:48:53 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:49:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:49:45 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:49:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:49:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:49:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:49:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccc77cb0a413e660cd5721d395bcec1266cde4d0528e29f1a042fabaa43ff5`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 281.9 KB (281940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d321b5acef374adaa49f78ae74b037995382f01d1353f489b334a6fc4cce81`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3f97bf1abc32dcb5c030e0f8d3abc990e9506ad219ab5cfb5827d15eaa02a`  
		Last Modified: Fri, 27 Aug 2021 17:51:47 GMT  
		Size: 104.9 MB (104940257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441e24829e5d83d1fd83b07e02e0a42bb1d31648314f63b39d44649802a9ee4a`  
		Last Modified: Fri, 27 Aug 2021 17:51:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf03157bc49c8e5393f28b8d4b4a6be766de31b9fc52348246bbe4ff2e7f7c7`  
		Last Modified: Fri, 27 Aug 2021 18:50:30 GMT  
		Size: 6.7 MB (6722103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f71cb40139c0ff03eef852eeea459437e95ca53c5ce0b8b7e1c1d49bab7a4`  
		Last Modified: Fri, 27 Aug 2021 18:50:29 GMT  
		Size: 1.3 MB (1264520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30ad513b9c90196100f4853c9b4d82e758c4acf048b7934bfa29a0fc2b27bd`  
		Last Modified: Fri, 27 Aug 2021 18:50:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:94548298bfccdd350db6f2fa27451effe035e5a1ed853df975c01413c49e19d8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2852923514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60de2cad586e35e33930f37908e1952dee5a28c8f9e23cf4c92f0c39732dfb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:09:49 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:09:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:11:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:26:22 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:27:40 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:27:40 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:30:27 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:29 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:26:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:26:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:26:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:26:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:27:28 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:27:29 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07d2bb4c99ec6467c6c9f474360867d31d27d22bc5be8432059a33a7c602a8`  
		Last Modified: Wed, 25 Aug 2021 13:38:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c31ebb0e52f79c34d0f70b88124ab4959963315dd2da2ec7117063a82d1392`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1935f777314159e43ee24dde17dba33b985a315578d33ec24796ba0ad27f679c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae930e0413fc2f7343e0b46be3ab58503ac4c137e8e6f83c7341838a22c88f3c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6bfd344bdb877d2969098eeb083c114ac4a7ef914d7dcf8eaef4d16e1e248c`  
		Last Modified: Wed, 25 Aug 2021 13:39:17 GMT  
		Size: 25.5 MB (25479918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffc00e2e1aed22bd02a7ac4e30d76d19f6caf0f9897e84d157e7af3c568f644`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f60594f1e4d8c227175212ac0226bec052e45a6f2ac058aa4845f0adc2c70a`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 341.3 KB (341318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67dd63dbd9960fb77efe3da2635624315e5b230e9d0136ff6a61c7667e1e25b`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6af958e54fca1b743938132e070c93737a923c10c0d37af843b754221072e`  
		Last Modified: Wed, 25 Aug 2021 13:41:52 GMT  
		Size: 139.4 MB (139357921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954ad9cafb5aec23d9fb11abca774323d6a853aa361ffcedad5613494b23c93`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98dafaec861f86e2303a05ac82fb338249638e4d85085798cdc5e9fc5b76f27`  
		Last Modified: Wed, 25 Aug 2021 19:29:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc818de352f19f2004712cdda39706ad5004b4c1271cc42d8a60233611cf64`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821ec8a9a1e85d66580448a6b4f6618fe1332d02415302a648a0ec0fb4f074db`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8471a6951d101eba4be159c56c730b5092e3dc7186f71902b34a8c2fd450fa97`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b1f0605dc501c2eb14f989b6a14b369106a5e41c5a9716ebc06c6afbbc0d81`  
		Last Modified: Wed, 25 Aug 2021 19:29:51 GMT  
		Size: 1.7 MB (1728504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c8468929fba91c5ee2288a255b1e7619f9c09a434d631fd20768cfcbd17d14`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:94c1c66eeae5feaeaca8684ac69bab2e5615335d9b8e1c4c27ab2743c0e1de8b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6442269359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b446fe4bd1058c21b63219634d88a9d9df5a9f31133e2434851d9e95305923`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:16:30 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:16:31 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:16:32 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:16:33 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:18:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:48 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:31:48 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:31:49 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:34:39 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:34:41 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:27:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:27:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:27:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:27:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:28:29 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:28:30 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f574487f5e33222a294b80d8246d04988a26a38908346c254fa2647c5a7e028d`  
		Last Modified: Wed, 25 Aug 2021 13:39:45 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e1bdad4b79465c250e34a289c1b634c4874290ec1fa9da12f91124ba323cb8`  
		Last Modified: Wed, 25 Aug 2021 13:39:44 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ca6c7d62e34b14c38c401eb0e5cd89bf7ec9b271c80606691b154e354576ef`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b8e5d43bb747a0877294acd5f9e1e22f072cc43f97874b9ecb708b70e7d96`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c80e7cfb2acdd3bfa5d45d3d78106e313290ca31797c9e09c7a33d383b758e`  
		Last Modified: Wed, 25 Aug 2021 13:40:10 GMT  
		Size: 25.4 MB (25442011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf57eb8b3d45fecbf8fca6bdbb800cf361cce365cd094eb059a82bcb44c0087`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd29eb1ef50bd4fe724ece3a9561ae93cea7d7509126824fded0df0cc4ecdec6`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 344.7 KB (344707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6512f7ffc77c76242888df38f980f80b78fb3a8230566c403838cebeb4bae3`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b245d14d9e193cc5f9cf2a6bd0a099a540ab40c551d463cf481046f9e6dd49ac`  
		Last Modified: Wed, 25 Aug 2021 13:42:48 GMT  
		Size: 143.8 MB (143814166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2271ca3757592eb20dd26ef0b75f72a643a18726ee620f0fda7fc8ab71cc298`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11ee28031df8b44b2509e14bc335b9f37b5f48c3f5bf4e87320948b77e105a`  
		Last Modified: Wed, 25 Aug 2021 19:30:11 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7174be725fdce80ce4b63ab3473b11cb9648e547860d9b802c707bde14e7d9`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8260167642582440a4feef71fce5ddd65334d08b35273698016831c005702fb`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782a41a0abba09324b19eca4010a0c1f4a008f0499b619f1c4acf139b4c67b36`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd614c1c73b684c14eaf7326f746b956f12566201e4ecfe8b836bd436a81f8`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.7 MB (1684554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccc99ea70e3e635c9add2b09e371e07e5ab90668b19b7837f02ed91f8d20c85`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.3-builder-alpine`

```console
$ docker pull caddy@sha256:b4ab80f23735ff30454053be49cfe2e59002772535099b99393a029444628b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.4.3-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:024148c65604529e01fe96436356aef6adc9737caf5784ee97639dc0178c0e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116836974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67f775001477b06c70ee78b6bf98a0ff2eb5c9a458dc030e5c730526e487f8e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:20:55 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:20:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:20:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:23:31 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:25:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:25:15 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:25:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:25:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:25:17 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:15:27 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:15:27 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:15:27 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:15:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:15:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:15:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:15:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e108acfc2dec423245b992f059c15efa90d3da68d666891f88e21cf9ed3044`  
		Last Modified: Fri, 27 Aug 2021 17:26:14 GMT  
		Size: 281.5 KB (281498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d12eec82106ee897382a4e0f5f4012bb993a2abb41ea43f6055affa263792`  
		Last Modified: Fri, 27 Aug 2021 17:26:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba5eda52a4c5e66ad77248b778eeaabf785c0ef090e85270075e82189ccdfc4`  
		Last Modified: Fri, 27 Aug 2021 17:27:13 GMT  
		Size: 105.8 MB (105802322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb85018fe45e8393802b1c7b0b50c6e376a6ca1e8e95626bde089498a365f36`  
		Last Modified: Fri, 27 Aug 2021 17:26:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90db72e3ed64553e72bfe368d98a62d9a915cccbf3fa0c25590581cd4a3cfb5`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 6.6 MB (6626826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2349f3cb068e4777bdf9bcdd5798e514be84f8a1b7c4f6c2cfbfe2ee83c11dcd`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 1.3 MB (1311166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b310272a238f2d14deb416889fbea68278aa777bf5de85c3c294752976cd54`  
		Last Modified: Fri, 27 Aug 2021 18:15:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a2633b70d3d99f56930313cbc6c8e60f9cb84d8a247952f70ecde4b3d287a61f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112621949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995bf035b94c22d1dfae95d63886ec0360983d1862a4f0b9934cfad4c223eecf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:51:48 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:51:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:51:50 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:56:06 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:58:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:58:48 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:58:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:58:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:58:51 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:58:16 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:58:16 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:58:17 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:58:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:58:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:58:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:58:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def35433210b819c72fc8c3f4cefb914a4d2072a396498b271719a29363f24a2`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 281.7 KB (281662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fbd33b2207f0f6c992e5356a6285f8362b9ddf3f61650c7493aa2568c9fa1`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8584a59dc2c89569cc10317112977b3957c6ab4369fad184c5d8f616e7bf78ba`  
		Last Modified: Fri, 27 Aug 2021 18:03:31 GMT  
		Size: 102.0 MB (102005169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28236e9ee5408a1ebfbc1993365e25c57923224e6608703e02685d3aada63456`  
		Last Modified: Fri, 27 Aug 2021 18:02:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bde7b63fd968f5c9eceab8094063f4937b1da8306aa777963db7cbb714883f`  
		Last Modified: Fri, 27 Aug 2021 18:59:31 GMT  
		Size: 6.5 MB (6485279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8f7ef25d584b1a6933ca79bb2c78a3fc206f53a38ab1ddd7060ecbe2a933dd`  
		Last Modified: Fri, 27 Aug 2021 18:59:28 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bf61c4b3d04e6edd3304db5bd03a3241100e4d350312263ff17271a6dc69a6`  
		Last Modified: Fri, 27 Aug 2021 18:59:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:34333a1acab5cdd87309f11e0d23c3d4c6b8685b0160f307ba7206972d37853e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111501647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231aa2a8195b5e48739d3233aacb263ab4462039e3fdd181e304186924795270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:27:52 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 19:27:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 19:27:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:33:26 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 19:36:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 19:36:54 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 19:36:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:36:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 19:37:01 GMT
WORKDIR /go
# Sat, 07 Aug 2021 03:50:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 03:51:00 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 03:51:00 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 03:51:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 03:51:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 03:51:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 03:51:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc7b26480300ed9c6eddb3c4eb897051a740425806a7edff4973e09fae2bb8f`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 280.8 KB (280814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba13042e2b42dba9e7f0e57a60855dff15f2890b8d942f61fbdc4852a43854`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a06372885d9e72431bcb74f5cbb21c55f0607374a0dc1a7261e0fdffe19a389`  
		Last Modified: Fri, 06 Aug 2021 19:47:59 GMT  
		Size: 101.8 MB (101786462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeda0e3490d50d1412a7145a405521667a31542915116d5bca87d1f262a3ba6`  
		Last Modified: Fri, 06 Aug 2021 19:47:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c45b3f2b54d4bc0ce5312c296a0f2073fa104179f9935212b88b9e9e4981251`  
		Last Modified: Sat, 07 Aug 2021 03:52:09 GMT  
		Size: 5.8 MB (5784805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e389ea9eac74a8896f796d9c785720d528a709e5ec82bf35fa05f7d36e8c2d`  
		Last Modified: Sat, 07 Aug 2021 03:52:07 GMT  
		Size: 1.2 MB (1219493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1adc87d17fa7707fc23fe9ed965dd55d2704211e52c5a765628d42ba2439dab`  
		Last Modified: Sat, 07 Aug 2021 03:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6f976dea79506be1124a40be07324506d379f104afb6b4eb7d7ac3ebd1f81143
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112055672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b827a8f7150bc8bc38ad14e96bb8ec14de011b8352d944d532735984a1f6f119`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:41:17 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:41:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:41:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:43:33 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:45:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:45:02 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:45:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:45:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:45:03 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:35:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:35:10 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:35:10 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:35:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:35:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:35:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:35:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e34390c2b14c7d6b4929bed3213d6d86bb9aa93c4ec135494e476afbb7c8ff`  
		Last Modified: Fri, 27 Aug 2021 17:46:50 GMT  
		Size: 281.7 KB (281688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f557407009b175f4d46f52d9e57a4123bc5118b57e0a250e983230d791682`  
		Last Modified: Fri, 27 Aug 2021 17:46:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b522346004414564cf2d79fa6ca0b9efd60f64f3cb1cfc754f94dea608d2a9`  
		Last Modified: Fri, 27 Aug 2021 17:48:05 GMT  
		Size: 101.1 MB (101121978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e36f943c088c76ce04cebeee6e3b83058ecf72465cbb1807ce21d94b09b892`  
		Last Modified: Fri, 27 Aug 2021 17:47:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f7d54a0c7c055c4b4d79ed1dee9267b227d3fe5987a13e382a3a92c14f30fa`  
		Last Modified: Fri, 27 Aug 2021 18:35:48 GMT  
		Size: 6.7 MB (6737926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1225f39dda93839c2256ed41c7299db86680c6c805344be7c064a34211daa`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 1.2 MB (1201538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87cf0ee91a4aba520fb94188e3d73181288f133c2b42cc0add124bc59519f0`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4cb744a2c30bef1fce63b25f25090e9a6fba23d518fbfb8a67f2de5437567654
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110962703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc63a956570ca25fb6e8cda280b13ba663c3f8268fcfd235e0f50e7efe03073`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:02:31 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 21:02:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 21:02:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:06:00 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 21:07:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 21:08:01 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 21:08:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:08:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 21:08:22 GMT
WORKDIR /go
# Sat, 07 Aug 2021 04:22:15 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 04:22:17 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 04:22:21 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 04:22:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 04:22:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 04:22:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 04:22:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f69fce9d10f5a5c047377039cda1fd5125aae4ec022be3dd7aede58be5a483`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 283.6 KB (283642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fdcb934d4034adf5e88a3b7bff7a633580eb8c0f18480df4123a14c499558b`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c6309d0f42f3d590978baeb06a18f86672f414b4fd6b6c0167fbaf5bc68502`  
		Last Modified: Fri, 06 Aug 2021 21:13:47 GMT  
		Size: 99.6 MB (99599293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6b0f08798744f7a5f5fbd19a9db24d1ce885fdb4cf4cc03cb9016e172748d1`  
		Last Modified: Fri, 06 Aug 2021 21:13:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86fe8978f31161530210163b69b5fc67ce11e38c091caab64bb0e3734496a18`  
		Last Modified: Sat, 07 Aug 2021 04:23:35 GMT  
		Size: 7.1 MB (7097385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356115fa932b78fceaeae3fba2bd7a0ff5efa89ebf9e8b5c824b679a666489c9`  
		Last Modified: Sat, 07 Aug 2021 04:23:34 GMT  
		Size: 1.2 MB (1170513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dc07db71f320869edaa3ef484018fc6b46b8bc0671ef668991e69bbda13f51`  
		Last Modified: Sat, 07 Aug 2021 04:23:33 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bb67f227515b2c32c0cfb3be1c48ff701cc4c525a59532d36b7166fc7aa27a21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115812998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6d4ca5bd25723d47c42919ec6d0b4bf7dd34a67583e8f3f2c95098e2142131`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:43:22 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:43:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:43:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:46:35 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:48:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:48:50 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:48:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:48:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:48:53 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:49:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:49:45 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:49:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:49:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:49:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:49:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccc77cb0a413e660cd5721d395bcec1266cde4d0528e29f1a042fabaa43ff5`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 281.9 KB (281940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d321b5acef374adaa49f78ae74b037995382f01d1353f489b334a6fc4cce81`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3f97bf1abc32dcb5c030e0f8d3abc990e9506ad219ab5cfb5827d15eaa02a`  
		Last Modified: Fri, 27 Aug 2021 17:51:47 GMT  
		Size: 104.9 MB (104940257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441e24829e5d83d1fd83b07e02e0a42bb1d31648314f63b39d44649802a9ee4a`  
		Last Modified: Fri, 27 Aug 2021 17:51:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf03157bc49c8e5393f28b8d4b4a6be766de31b9fc52348246bbe4ff2e7f7c7`  
		Last Modified: Fri, 27 Aug 2021 18:50:30 GMT  
		Size: 6.7 MB (6722103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f71cb40139c0ff03eef852eeea459437e95ca53c5ce0b8b7e1c1d49bab7a4`  
		Last Modified: Fri, 27 Aug 2021 18:50:29 GMT  
		Size: 1.3 MB (1264520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30ad513b9c90196100f4853c9b4d82e758c4acf048b7934bfa29a0fc2b27bd`  
		Last Modified: Fri, 27 Aug 2021 18:50:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.3-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a650332bf33eaced67086712173ed2278573f04f8fe94b11682e52eb1222d4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `caddy:2.4.3-builder-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:94548298bfccdd350db6f2fa27451effe035e5a1ed853df975c01413c49e19d8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2852923514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60de2cad586e35e33930f37908e1952dee5a28c8f9e23cf4c92f0c39732dfb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:09:49 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:09:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:11:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:26:22 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:27:40 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:27:40 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:30:27 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:29 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:26:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:26:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:26:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:26:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:27:28 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:27:29 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07d2bb4c99ec6467c6c9f474360867d31d27d22bc5be8432059a33a7c602a8`  
		Last Modified: Wed, 25 Aug 2021 13:38:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c31ebb0e52f79c34d0f70b88124ab4959963315dd2da2ec7117063a82d1392`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1935f777314159e43ee24dde17dba33b985a315578d33ec24796ba0ad27f679c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae930e0413fc2f7343e0b46be3ab58503ac4c137e8e6f83c7341838a22c88f3c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6bfd344bdb877d2969098eeb083c114ac4a7ef914d7dcf8eaef4d16e1e248c`  
		Last Modified: Wed, 25 Aug 2021 13:39:17 GMT  
		Size: 25.5 MB (25479918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffc00e2e1aed22bd02a7ac4e30d76d19f6caf0f9897e84d157e7af3c568f644`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f60594f1e4d8c227175212ac0226bec052e45a6f2ac058aa4845f0adc2c70a`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 341.3 KB (341318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67dd63dbd9960fb77efe3da2635624315e5b230e9d0136ff6a61c7667e1e25b`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6af958e54fca1b743938132e070c93737a923c10c0d37af843b754221072e`  
		Last Modified: Wed, 25 Aug 2021 13:41:52 GMT  
		Size: 139.4 MB (139357921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954ad9cafb5aec23d9fb11abca774323d6a853aa361ffcedad5613494b23c93`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98dafaec861f86e2303a05ac82fb338249638e4d85085798cdc5e9fc5b76f27`  
		Last Modified: Wed, 25 Aug 2021 19:29:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc818de352f19f2004712cdda39706ad5004b4c1271cc42d8a60233611cf64`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821ec8a9a1e85d66580448a6b4f6618fe1332d02415302a648a0ec0fb4f074db`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8471a6951d101eba4be159c56c730b5092e3dc7186f71902b34a8c2fd450fa97`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b1f0605dc501c2eb14f989b6a14b369106a5e41c5a9716ebc06c6afbbc0d81`  
		Last Modified: Wed, 25 Aug 2021 19:29:51 GMT  
		Size: 1.7 MB (1728504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c8468929fba91c5ee2288a255b1e7619f9c09a434d631fd20768cfcbd17d14`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.3-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:7ebaf26507754bcf51a3c839f0a4cdec367302d2c4f69b1f816c2f1f8fd2697c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4583; amd64

### `caddy:2.4.3-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:94c1c66eeae5feaeaca8684ac69bab2e5615335d9b8e1c4c27ab2743c0e1de8b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6442269359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b446fe4bd1058c21b63219634d88a9d9df5a9f31133e2434851d9e95305923`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:16:30 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:16:31 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:16:32 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:16:33 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:18:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:48 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:31:48 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:31:49 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:34:39 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:34:41 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:27:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:27:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:27:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:27:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:28:29 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:28:30 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f574487f5e33222a294b80d8246d04988a26a38908346c254fa2647c5a7e028d`  
		Last Modified: Wed, 25 Aug 2021 13:39:45 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e1bdad4b79465c250e34a289c1b634c4874290ec1fa9da12f91124ba323cb8`  
		Last Modified: Wed, 25 Aug 2021 13:39:44 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ca6c7d62e34b14c38c401eb0e5cd89bf7ec9b271c80606691b154e354576ef`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b8e5d43bb747a0877294acd5f9e1e22f072cc43f97874b9ecb708b70e7d96`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c80e7cfb2acdd3bfa5d45d3d78106e313290ca31797c9e09c7a33d383b758e`  
		Last Modified: Wed, 25 Aug 2021 13:40:10 GMT  
		Size: 25.4 MB (25442011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf57eb8b3d45fecbf8fca6bdbb800cf361cce365cd094eb059a82bcb44c0087`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd29eb1ef50bd4fe724ece3a9561ae93cea7d7509126824fded0df0cc4ecdec6`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 344.7 KB (344707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6512f7ffc77c76242888df38f980f80b78fb3a8230566c403838cebeb4bae3`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b245d14d9e193cc5f9cf2a6bd0a099a540ab40c551d463cf481046f9e6dd49ac`  
		Last Modified: Wed, 25 Aug 2021 13:42:48 GMT  
		Size: 143.8 MB (143814166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2271ca3757592eb20dd26ef0b75f72a643a18726ee620f0fda7fc8ab71cc298`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11ee28031df8b44b2509e14bc335b9f37b5f48c3f5bf4e87320948b77e105a`  
		Last Modified: Wed, 25 Aug 2021 19:30:11 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7174be725fdce80ce4b63ab3473b11cb9648e547860d9b802c707bde14e7d9`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8260167642582440a4feef71fce5ddd65334d08b35273698016831c005702fb`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782a41a0abba09324b19eca4010a0c1f4a008f0499b619f1c4acf139b4c67b36`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd614c1c73b684c14eaf7326f746b956f12566201e4ecfe8b836bd436a81f8`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.7 MB (1684554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccc99ea70e3e635c9add2b09e371e07e5ab90668b19b7837f02ed91f8d20c85`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.3-windowsservercore`

```console
$ docker pull caddy@sha256:e5e5fb2f39e631146f8c890d36e0a2e6e150c66d5ee959a580002e4032761392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `caddy:2.4.3-windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:277245d2976e25118dde31aa817da26aab9a54b716478e335e7e47a655680fdf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdb54faaf1277fc5d472259e6d51ac14101b59691359db53c189a9f55df03c8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:21:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:21:12 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:22:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:22:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:22:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:22:18 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:22:19 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:22:20 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:22:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:22:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:22:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:22:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:22:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:22:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:22:28 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:22:29 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:22:30 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:23:15 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:23:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc78244c47d63e7118efa5a81aeac258859631816cf0d2e335045eddd6d4562c`  
		Last Modified: Wed, 25 Aug 2021 19:29:08 GMT  
		Size: 390.1 KB (390074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e85659c5ef3d6f1826cce92e5c35cbda668ec96e58661902ea89472385a68`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad534458f62e8592943908290a647cce35c3f5ed0761b80f7d17f55393900e`  
		Last Modified: Wed, 25 Aug 2021 19:29:10 GMT  
		Size: 12.0 MB (12023423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e1aa1a15f7618a90c91ce39aeb28f0b14d0fb039a0a5c387e2d7a4460443aa`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a259cd0cf699d1891ff65f72aaf75b8b53d32409fdbab40fa8aa3594f4edb`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb72b357bee0361ca5587e675d3a832276f086a2d6535147bfe92a000cf044f`  
		Last Modified: Wed, 25 Aug 2021 19:29:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbe28f726b8cddbd0398281cfc45f2dc82f378bef80fa1dfe4dec201451721`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a73648024b9f42aeeda4c4309ba545e089e6943b686c93ea09cec6ac83373`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ad45ece5f60db2673be4be17ca0ac1ff391d32d88f7a84e2e671fca6744e0`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424371920e55efd886bea3b4671eca80436677674986f299b919e72c49d4289`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2b299f27503c9be94a9a16c137b08ba7e2b84cc07b96a281d4b2886b231f0`  
		Last Modified: Wed, 25 Aug 2021 19:29:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c231726719db989f9746b39a4b4b9b54646376e1dc36c124a1401fc15132`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ae0be18044dcf67b8832f125744410261cc8601712176399a3cd632b8843`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b94a88e7f4db3aa538dad13b42b51168525142c8268098dbe8a7175decee6`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0f35247abb67063d217ea9963f29270e1716b21409196f0e935710342a9dd9`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fa12b6daf14192bb460b568c8c3f65625b384fbcfa33e4b227d39de751374d`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43dbbbd0c30fabb616088a2f902ad0177c216707c4e134d10b9a1cd4fde8cb`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee931681f757a39ac6ce152aa1d64f251a68f63dca6dbe3459c2cec9bed0d90e`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deb6e04a956a5c619ff2eb344a4e5fcf8384d890b8120ce2ffd91cf20e0b5f`  
		Last Modified: Wed, 25 Aug 2021 19:29:00 GMT  
		Size: 320.7 KB (320709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b510aa21fdb81bb0a2156b0a977a69ea8187f959ceb05869b1450d9359814`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.3-windowsservercore` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:bd0551e2eeef6d131272af5e4214599dfc85e2a18d421264005a4f8dc3025a02
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283675023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96c9f880047fab4000d8bad0dceb15c3e478898181805e15b864f3ae980f11`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:24:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:24:21 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:25:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:25:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:25:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:25:25 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:25:26 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:25:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:25:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:25:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:25:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:25:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:25:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:25:35 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:25:36 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:25:37 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:26:16 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:26:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9dee8014da227cc8c6b8d14f6464fefc307c265b07a34d6e2ccc5de24a92a`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 352.7 KB (352700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d26c5819d131639ab53b8e099ab2ed93c63f759072d3a5ce4b9f69f13b8a66`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb3ea0fdbcaf7cab1dbac86676ab00ca78ebf68e3b5c476c5984201c357976`  
		Last Modified: Wed, 25 Aug 2021 19:29:35 GMT  
		Size: 12.0 MB (12025369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a331953cb55eb8482f8b09c1ccb30b06198b0da91f196aa230d56d4f626c3`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c66a58bae64f63c34265474f15131687cba250a5cbeb2166a25d383630b68`  
		Last Modified: Wed, 25 Aug 2021 19:29:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b60346916eaf0cd70873400273d0f0de4f72aa7ee5a5bd6a8cfbe446d62499`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74af1f53b1dc6d2f58a23760f463877d707150f1cae25c0ca6a727c64cd7e9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4467e0d432e5bba7c8e197c057837e438ae63c8748b9765a8d7591c0ea12c0`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c92db8b514f6d653c3d0ba5a7e695e808f5880504124fb94648c10590f7f3c9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63a5575b8310dcb9cbe40352e7753a4bb8f66f1c3fbea055abda03136638d6`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415f534f6818ea980cf13f9a08c0efb9d60c9f86760129563e203ba93e399c8`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be354de1af39afc991030861814f135bfde0267a02f004fd4caf9ccc31d0bfd`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a0ebb3c5c8d126c85ccbad571fef0051ac62cfec3fe5885c82110381049ed9`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893f40ed74354bd380ee49a7141c654ea10f5a43f1e050539bde502c7214c9f`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd03947508d81a8a5c939b4a1697e4cf18bc8722cc1650732f8df2c6924941`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c43d724632362e78f09ee6bf53a8359cdd6db65300cb3687f2ad3a59e1a5d`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaec774cf06dd02e7ebdf8d5e9aa9b8d4578a60c7a54ce84421910922396b7`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb3d76a117ff8038563015df19972676ff4aea085431ef698f57799559b334`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341d5f41a06e42738b97ffd6ca2835680879ba4113b882c5cd8accd857c0551`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 305.6 KB (305571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd0dece66bb4a5f39d723d7d27311fa04d1de60c084735f41cb588c7b4d5701`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.3-windowsservercore-1809`

```console
$ docker pull caddy@sha256:50783893bffe979472583ab27a4a4346cdeb5895077ff67af22283b65699eda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `caddy:2.4.3-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:277245d2976e25118dde31aa817da26aab9a54b716478e335e7e47a655680fdf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdb54faaf1277fc5d472259e6d51ac14101b59691359db53c189a9f55df03c8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:21:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:21:12 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:22:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:22:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:22:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:22:18 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:22:19 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:22:20 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:22:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:22:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:22:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:22:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:22:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:22:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:22:28 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:22:29 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:22:30 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:23:15 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:23:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc78244c47d63e7118efa5a81aeac258859631816cf0d2e335045eddd6d4562c`  
		Last Modified: Wed, 25 Aug 2021 19:29:08 GMT  
		Size: 390.1 KB (390074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e85659c5ef3d6f1826cce92e5c35cbda668ec96e58661902ea89472385a68`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad534458f62e8592943908290a647cce35c3f5ed0761b80f7d17f55393900e`  
		Last Modified: Wed, 25 Aug 2021 19:29:10 GMT  
		Size: 12.0 MB (12023423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e1aa1a15f7618a90c91ce39aeb28f0b14d0fb039a0a5c387e2d7a4460443aa`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a259cd0cf699d1891ff65f72aaf75b8b53d32409fdbab40fa8aa3594f4edb`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb72b357bee0361ca5587e675d3a832276f086a2d6535147bfe92a000cf044f`  
		Last Modified: Wed, 25 Aug 2021 19:29:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbe28f726b8cddbd0398281cfc45f2dc82f378bef80fa1dfe4dec201451721`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a73648024b9f42aeeda4c4309ba545e089e6943b686c93ea09cec6ac83373`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ad45ece5f60db2673be4be17ca0ac1ff391d32d88f7a84e2e671fca6744e0`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424371920e55efd886bea3b4671eca80436677674986f299b919e72c49d4289`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2b299f27503c9be94a9a16c137b08ba7e2b84cc07b96a281d4b2886b231f0`  
		Last Modified: Wed, 25 Aug 2021 19:29:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c231726719db989f9746b39a4b4b9b54646376e1dc36c124a1401fc15132`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ae0be18044dcf67b8832f125744410261cc8601712176399a3cd632b8843`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b94a88e7f4db3aa538dad13b42b51168525142c8268098dbe8a7175decee6`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0f35247abb67063d217ea9963f29270e1716b21409196f0e935710342a9dd9`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fa12b6daf14192bb460b568c8c3f65625b384fbcfa33e4b227d39de751374d`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43dbbbd0c30fabb616088a2f902ad0177c216707c4e134d10b9a1cd4fde8cb`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee931681f757a39ac6ce152aa1d64f251a68f63dca6dbe3459c2cec9bed0d90e`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deb6e04a956a5c619ff2eb344a4e5fcf8384d890b8120ce2ffd91cf20e0b5f`  
		Last Modified: Wed, 25 Aug 2021 19:29:00 GMT  
		Size: 320.7 KB (320709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b510aa21fdb81bb0a2156b0a977a69ea8187f959ceb05869b1450d9359814`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.3-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:e8353d4e8df77074d824ddc338a6a8784add4f27abe1cda1b230b6a27533edd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4583; amd64

### `caddy:2.4.3-windowsservercore-ltsc2016` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:bd0551e2eeef6d131272af5e4214599dfc85e2a18d421264005a4f8dc3025a02
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283675023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96c9f880047fab4000d8bad0dceb15c3e478898181805e15b864f3ae980f11`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:24:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:24:21 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:25:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:25:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:25:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:25:25 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:25:26 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:25:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:25:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:25:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:25:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:25:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:25:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:25:35 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:25:36 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:25:37 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:26:16 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:26:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9dee8014da227cc8c6b8d14f6464fefc307c265b07a34d6e2ccc5de24a92a`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 352.7 KB (352700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d26c5819d131639ab53b8e099ab2ed93c63f759072d3a5ce4b9f69f13b8a66`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb3ea0fdbcaf7cab1dbac86676ab00ca78ebf68e3b5c476c5984201c357976`  
		Last Modified: Wed, 25 Aug 2021 19:29:35 GMT  
		Size: 12.0 MB (12025369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a331953cb55eb8482f8b09c1ccb30b06198b0da91f196aa230d56d4f626c3`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c66a58bae64f63c34265474f15131687cba250a5cbeb2166a25d383630b68`  
		Last Modified: Wed, 25 Aug 2021 19:29:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b60346916eaf0cd70873400273d0f0de4f72aa7ee5a5bd6a8cfbe446d62499`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74af1f53b1dc6d2f58a23760f463877d707150f1cae25c0ca6a727c64cd7e9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4467e0d432e5bba7c8e197c057837e438ae63c8748b9765a8d7591c0ea12c0`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c92db8b514f6d653c3d0ba5a7e695e808f5880504124fb94648c10590f7f3c9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63a5575b8310dcb9cbe40352e7753a4bb8f66f1c3fbea055abda03136638d6`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415f534f6818ea980cf13f9a08c0efb9d60c9f86760129563e203ba93e399c8`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be354de1af39afc991030861814f135bfde0267a02f004fd4caf9ccc31d0bfd`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a0ebb3c5c8d126c85ccbad571fef0051ac62cfec3fe5885c82110381049ed9`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893f40ed74354bd380ee49a7141c654ea10f5a43f1e050539bde502c7214c9f`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd03947508d81a8a5c939b4a1697e4cf18bc8722cc1650732f8df2c6924941`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c43d724632362e78f09ee6bf53a8359cdd6db65300cb3687f2ad3a59e1a5d`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaec774cf06dd02e7ebdf8d5e9aa9b8d4578a60c7a54ce84421910922396b7`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb3d76a117ff8038563015df19972676ff4aea085431ef698f57799559b334`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341d5f41a06e42738b97ffd6ca2835680879ba4113b882c5cd8accd857c0551`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 305.6 KB (305571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd0dece66bb4a5f39d723d7d27311fa04d1de60c084735f41cb588c7b4d5701`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:f00d2e7e82418a30135cbe5c1455df6c617ee651d6f430183a8e49e3b2608359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:77f27025e0e1e0ab97bc931db61d24f9ac41591e17576ab46c4b508afbccacd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14648199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8a741f4852592d8634aa37c7f351ae4f4e7b4a9a2594df54603ac48cbdad74`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:11:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 11 May 2021 01:04:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 19:19:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 19:19:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 19:19:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 19:19:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 19:19:32 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 19:19:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 443
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 19:19:34 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 19:19:34 GMT
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
	-	`sha256:16798e0582fce7af9c2ba2c8ee4990d0fd1e58384e170ee9937486253d67bbf1`  
		Last Modified: Tue, 11 May 2021 01:05:00 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d589bc046eca71df600301462981053bf178fcd31d4b2c882ca05aec70bacd`  
		Last Modified: Thu, 24 Jun 2021 19:19:59 GMT  
		Size: 11.5 MB (11529821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8ce9421f330c9a085ac8f059d2dd53feabf795c461d4f43b596d0302b1cf9`  
		Last Modified: Thu, 24 Jun 2021 19:19:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:615389b06a74c80f0494cdc47da7b9f565cadd8cd715e39d7b65aaaf2937b6cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13816604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac08c3d5e13d15da24bbe2b6e7bd0fe9a42212188c3f33467bb1f38dfdb0b51`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 22:32:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 22:32:24 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 22:32:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 22:32:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 22:32:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 22:32:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 22:32:36 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 22:32:37 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 22:32:37 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 22:32:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 22:32:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 22:32:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 22:32:44 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:32:45 GMT
EXPOSE 443
# Fri, 30 Jul 2021 22:32:46 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 22:32:46 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 22:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18943f91e0b98a5ee778a791cc00f627dfc62e6163be04be39d8dfca48ca309`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 300.5 KB (300515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6779ad883f93abbe8842bc2dd07f67be174891b4b835e18a7eccb5a738ee0eb9`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6cb30c4e53dad6055df249f24807530e7530d534f18b81671b80de7b8b0ad2`  
		Last Modified: Fri, 30 Jul 2021 22:34:16 GMT  
		Size: 10.9 MB (10887954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a803ba6ef03f0246aec715857792f54efc64816b24b563beee84263dd1ad439`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c382c62559cf6348cccc2048f7f6e3234ad6c3322fa778f0d7ab3fbe27cd44e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13593493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c6676bf8617209d68af4cbdd3c3edb6084cbd01e6c7f00b706fab8934f311a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Fri, 30 Jul 2021 18:36:39 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:13:40 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 02:13:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 02:13:44 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 02:13:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 02:13:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 02:13:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 02:13:56 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 443
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 02:13:58 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 02:13:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf509b321d9275e96242772f4cd73ad8da2970e30e18c0f2326ed91777442e`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 299.7 KB (299672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16416239cfcd26ea4cc02aaf7ac5511b6ea5d6cc672046b6e61d90f9c59ffaac`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de14f3facde68cf2e2470839f96bb111537c6b40d15a1b28c47c6568261ee15`  
		Last Modified: Sat, 31 Jul 2021 02:15:20 GMT  
		Size: 10.9 MB (10863669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6b241bda44fe422ccd7c0c967fb01d2d7a191df7b0628d9c44df2d18dd5445`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ee1b9ce06277bd5c34b2d9a6908cdb3028aa838fa75e5c6e1e32d2cabb417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13464756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a697a3b5305c041fd956ba80c8845676041e98bce128a69e70074e5abe9653dd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 15 Jun 2021 22:32:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 18:39:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 18:39:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 18:39:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 443
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 18:39:33 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 18:39:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d0b72044755ebd2b829600b94a69aa9096bbb4bf9a01c1795b5b245261b99a`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 300.6 KB (300631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abde659ccf1d73128ef1e71a9701b014e0f27d4abf15b3d410d0474cdd0adb95`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75403ccf5c23126b5dca334871ec0096a90d0fb85f47be1ecba3904921529c0`  
		Last Modified: Thu, 24 Jun 2021 18:40:18 GMT  
		Size: 10.4 MB (10446098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a85edeaa46fe5e0185f11a1a1801c0d0458e59897d3c04e97136df1c496663`  
		Last Modified: Thu, 24 Jun 2021 18:40:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:fff2119338c215eceae68398483da801f5daf8bb5405c7ed8db5769aeb367cd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13173634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced11b632073f0e249ba02b8326f0c1ccf6c154d4340342b38c8b3f830c37e70`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:24:49 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Fri, 30 Jul 2021 17:24:54 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:36:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 00:36:51 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 00:36:54 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 00:37:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 00:37:10 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 00:37:12 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 00:37:14 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 00:37:17 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 00:37:23 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 00:37:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 00:37:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 00:37:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 00:37:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 00:37:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 00:37:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 00:37:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 00:38:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 00:38:06 GMT
EXPOSE 80
# Sat, 31 Jul 2021 00:38:09 GMT
EXPOSE 443
# Sat, 31 Jul 2021 00:38:16 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 00:38:25 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 00:38:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396ee5e0a948db1cebd77a9b357abbc39c60dc4caf97f87f759a1f232a291da5`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 302.5 KB (302545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c405a506bbc65ab625ac9298a31abc4a1871eef7b93ff4fbc6a25fb9db591a4`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ac195b709078a7d439cd22a970947cb2ed3f9cd136a8d51324ab3d3c746625`  
		Last Modified: Sat, 31 Jul 2021 00:39:16 GMT  
		Size: 10.1 MB (10051943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2c9f1da5ba05b5656393520168363c5d8a223167645bc0a4451fcd4c2f5447`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:576d8d6d9dead63f0cc0db39ad0fb1e9e9539bf5b23a8b70623b7e8f40d916a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14005959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6114aef9a435617ae101cc26569f3f2103cd2c999ef3e41df780270222452a1f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:41:41 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Fri, 30 Jul 2021 17:41:42 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 23:50:44 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 23:50:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 23:50:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 23:50:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 23:50:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 23:50:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 80
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 443
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 23:50:52 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 23:50:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de364003ff53d3ed839a7d8fd8cc6c59936d04b22886595d954e5c9929cfe0e1`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 300.9 KB (300858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d9b83bb28f1c9bc97f9a4907425be62b28dd687b54e3b8d461b2e40203110d`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076584d90c472ad966977bc9f55f53439edb7b5169fa684c1a70a1ea682037ca`  
		Last Modified: Fri, 30 Jul 2021 23:51:34 GMT  
		Size: 11.1 MB (11096451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f126f1c964e9405478f4683dd4b8e93297166d84566a652fe658f36bad6390c`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:6d4327fca22a56f18bcb561bbf5be757c05758d8bfcab7b115d6481996285052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:024148c65604529e01fe96436356aef6adc9737caf5784ee97639dc0178c0e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116836974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67f775001477b06c70ee78b6bf98a0ff2eb5c9a458dc030e5c730526e487f8e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:20:55 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:20:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:20:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:23:31 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:25:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:25:15 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:25:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:25:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:25:17 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:15:27 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:15:27 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:15:27 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:15:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:15:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:15:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:15:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e108acfc2dec423245b992f059c15efa90d3da68d666891f88e21cf9ed3044`  
		Last Modified: Fri, 27 Aug 2021 17:26:14 GMT  
		Size: 281.5 KB (281498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d12eec82106ee897382a4e0f5f4012bb993a2abb41ea43f6055affa263792`  
		Last Modified: Fri, 27 Aug 2021 17:26:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba5eda52a4c5e66ad77248b778eeaabf785c0ef090e85270075e82189ccdfc4`  
		Last Modified: Fri, 27 Aug 2021 17:27:13 GMT  
		Size: 105.8 MB (105802322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb85018fe45e8393802b1c7b0b50c6e376a6ca1e8e95626bde089498a365f36`  
		Last Modified: Fri, 27 Aug 2021 17:26:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90db72e3ed64553e72bfe368d98a62d9a915cccbf3fa0c25590581cd4a3cfb5`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 6.6 MB (6626826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2349f3cb068e4777bdf9bcdd5798e514be84f8a1b7c4f6c2cfbfe2ee83c11dcd`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 1.3 MB (1311166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b310272a238f2d14deb416889fbea68278aa777bf5de85c3c294752976cd54`  
		Last Modified: Fri, 27 Aug 2021 18:15:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a2633b70d3d99f56930313cbc6c8e60f9cb84d8a247952f70ecde4b3d287a61f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112621949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995bf035b94c22d1dfae95d63886ec0360983d1862a4f0b9934cfad4c223eecf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:51:48 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:51:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:51:50 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:56:06 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:58:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:58:48 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:58:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:58:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:58:51 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:58:16 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:58:16 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:58:17 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:58:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:58:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:58:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:58:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def35433210b819c72fc8c3f4cefb914a4d2072a396498b271719a29363f24a2`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 281.7 KB (281662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fbd33b2207f0f6c992e5356a6285f8362b9ddf3f61650c7493aa2568c9fa1`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8584a59dc2c89569cc10317112977b3957c6ab4369fad184c5d8f616e7bf78ba`  
		Last Modified: Fri, 27 Aug 2021 18:03:31 GMT  
		Size: 102.0 MB (102005169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28236e9ee5408a1ebfbc1993365e25c57923224e6608703e02685d3aada63456`  
		Last Modified: Fri, 27 Aug 2021 18:02:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bde7b63fd968f5c9eceab8094063f4937b1da8306aa777963db7cbb714883f`  
		Last Modified: Fri, 27 Aug 2021 18:59:31 GMT  
		Size: 6.5 MB (6485279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8f7ef25d584b1a6933ca79bb2c78a3fc206f53a38ab1ddd7060ecbe2a933dd`  
		Last Modified: Fri, 27 Aug 2021 18:59:28 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bf61c4b3d04e6edd3304db5bd03a3241100e4d350312263ff17271a6dc69a6`  
		Last Modified: Fri, 27 Aug 2021 18:59:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:34333a1acab5cdd87309f11e0d23c3d4c6b8685b0160f307ba7206972d37853e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111501647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231aa2a8195b5e48739d3233aacb263ab4462039e3fdd181e304186924795270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:27:52 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 19:27:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 19:27:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:33:26 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 19:36:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 19:36:54 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 19:36:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:36:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 19:37:01 GMT
WORKDIR /go
# Sat, 07 Aug 2021 03:50:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 03:51:00 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 03:51:00 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 03:51:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 03:51:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 03:51:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 03:51:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc7b26480300ed9c6eddb3c4eb897051a740425806a7edff4973e09fae2bb8f`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 280.8 KB (280814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba13042e2b42dba9e7f0e57a60855dff15f2890b8d942f61fbdc4852a43854`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a06372885d9e72431bcb74f5cbb21c55f0607374a0dc1a7261e0fdffe19a389`  
		Last Modified: Fri, 06 Aug 2021 19:47:59 GMT  
		Size: 101.8 MB (101786462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeda0e3490d50d1412a7145a405521667a31542915116d5bca87d1f262a3ba6`  
		Last Modified: Fri, 06 Aug 2021 19:47:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c45b3f2b54d4bc0ce5312c296a0f2073fa104179f9935212b88b9e9e4981251`  
		Last Modified: Sat, 07 Aug 2021 03:52:09 GMT  
		Size: 5.8 MB (5784805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e389ea9eac74a8896f796d9c785720d528a709e5ec82bf35fa05f7d36e8c2d`  
		Last Modified: Sat, 07 Aug 2021 03:52:07 GMT  
		Size: 1.2 MB (1219493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1adc87d17fa7707fc23fe9ed965dd55d2704211e52c5a765628d42ba2439dab`  
		Last Modified: Sat, 07 Aug 2021 03:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6f976dea79506be1124a40be07324506d379f104afb6b4eb7d7ac3ebd1f81143
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112055672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b827a8f7150bc8bc38ad14e96bb8ec14de011b8352d944d532735984a1f6f119`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:41:17 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:41:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:41:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:43:33 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:45:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:45:02 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:45:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:45:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:45:03 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:35:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:35:10 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:35:10 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:35:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:35:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:35:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:35:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e34390c2b14c7d6b4929bed3213d6d86bb9aa93c4ec135494e476afbb7c8ff`  
		Last Modified: Fri, 27 Aug 2021 17:46:50 GMT  
		Size: 281.7 KB (281688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f557407009b175f4d46f52d9e57a4123bc5118b57e0a250e983230d791682`  
		Last Modified: Fri, 27 Aug 2021 17:46:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b522346004414564cf2d79fa6ca0b9efd60f64f3cb1cfc754f94dea608d2a9`  
		Last Modified: Fri, 27 Aug 2021 17:48:05 GMT  
		Size: 101.1 MB (101121978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e36f943c088c76ce04cebeee6e3b83058ecf72465cbb1807ce21d94b09b892`  
		Last Modified: Fri, 27 Aug 2021 17:47:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f7d54a0c7c055c4b4d79ed1dee9267b227d3fe5987a13e382a3a92c14f30fa`  
		Last Modified: Fri, 27 Aug 2021 18:35:48 GMT  
		Size: 6.7 MB (6737926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1225f39dda93839c2256ed41c7299db86680c6c805344be7c064a34211daa`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 1.2 MB (1201538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87cf0ee91a4aba520fb94188e3d73181288f133c2b42cc0add124bc59519f0`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4cb744a2c30bef1fce63b25f25090e9a6fba23d518fbfb8a67f2de5437567654
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110962703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc63a956570ca25fb6e8cda280b13ba663c3f8268fcfd235e0f50e7efe03073`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:02:31 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 21:02:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 21:02:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:06:00 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 21:07:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 21:08:01 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 21:08:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:08:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 21:08:22 GMT
WORKDIR /go
# Sat, 07 Aug 2021 04:22:15 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 04:22:17 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 04:22:21 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 04:22:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 04:22:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 04:22:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 04:22:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f69fce9d10f5a5c047377039cda1fd5125aae4ec022be3dd7aede58be5a483`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 283.6 KB (283642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fdcb934d4034adf5e88a3b7bff7a633580eb8c0f18480df4123a14c499558b`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c6309d0f42f3d590978baeb06a18f86672f414b4fd6b6c0167fbaf5bc68502`  
		Last Modified: Fri, 06 Aug 2021 21:13:47 GMT  
		Size: 99.6 MB (99599293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6b0f08798744f7a5f5fbd19a9db24d1ce885fdb4cf4cc03cb9016e172748d1`  
		Last Modified: Fri, 06 Aug 2021 21:13:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86fe8978f31161530210163b69b5fc67ce11e38c091caab64bb0e3734496a18`  
		Last Modified: Sat, 07 Aug 2021 04:23:35 GMT  
		Size: 7.1 MB (7097385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356115fa932b78fceaeae3fba2bd7a0ff5efa89ebf9e8b5c824b679a666489c9`  
		Last Modified: Sat, 07 Aug 2021 04:23:34 GMT  
		Size: 1.2 MB (1170513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dc07db71f320869edaa3ef484018fc6b46b8bc0671ef668991e69bbda13f51`  
		Last Modified: Sat, 07 Aug 2021 04:23:33 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:bb67f227515b2c32c0cfb3be1c48ff701cc4c525a59532d36b7166fc7aa27a21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115812998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6d4ca5bd25723d47c42919ec6d0b4bf7dd34a67583e8f3f2c95098e2142131`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:43:22 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:43:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:43:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:46:35 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:48:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:48:50 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:48:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:48:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:48:53 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:49:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:49:45 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:49:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:49:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:49:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:49:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccc77cb0a413e660cd5721d395bcec1266cde4d0528e29f1a042fabaa43ff5`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 281.9 KB (281940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d321b5acef374adaa49f78ae74b037995382f01d1353f489b334a6fc4cce81`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3f97bf1abc32dcb5c030e0f8d3abc990e9506ad219ab5cfb5827d15eaa02a`  
		Last Modified: Fri, 27 Aug 2021 17:51:47 GMT  
		Size: 104.9 MB (104940257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441e24829e5d83d1fd83b07e02e0a42bb1d31648314f63b39d44649802a9ee4a`  
		Last Modified: Fri, 27 Aug 2021 17:51:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf03157bc49c8e5393f28b8d4b4a6be766de31b9fc52348246bbe4ff2e7f7c7`  
		Last Modified: Fri, 27 Aug 2021 18:50:30 GMT  
		Size: 6.7 MB (6722103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f71cb40139c0ff03eef852eeea459437e95ca53c5ce0b8b7e1c1d49bab7a4`  
		Last Modified: Fri, 27 Aug 2021 18:50:29 GMT  
		Size: 1.3 MB (1264520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30ad513b9c90196100f4853c9b4d82e758c4acf048b7934bfa29a0fc2b27bd`  
		Last Modified: Fri, 27 Aug 2021 18:50:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:94548298bfccdd350db6f2fa27451effe035e5a1ed853df975c01413c49e19d8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2852923514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60de2cad586e35e33930f37908e1952dee5a28c8f9e23cf4c92f0c39732dfb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:09:49 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:09:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:11:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:26:22 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:27:40 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:27:40 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:30:27 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:29 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:26:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:26:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:26:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:26:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:27:28 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:27:29 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07d2bb4c99ec6467c6c9f474360867d31d27d22bc5be8432059a33a7c602a8`  
		Last Modified: Wed, 25 Aug 2021 13:38:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c31ebb0e52f79c34d0f70b88124ab4959963315dd2da2ec7117063a82d1392`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1935f777314159e43ee24dde17dba33b985a315578d33ec24796ba0ad27f679c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae930e0413fc2f7343e0b46be3ab58503ac4c137e8e6f83c7341838a22c88f3c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6bfd344bdb877d2969098eeb083c114ac4a7ef914d7dcf8eaef4d16e1e248c`  
		Last Modified: Wed, 25 Aug 2021 13:39:17 GMT  
		Size: 25.5 MB (25479918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffc00e2e1aed22bd02a7ac4e30d76d19f6caf0f9897e84d157e7af3c568f644`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f60594f1e4d8c227175212ac0226bec052e45a6f2ac058aa4845f0adc2c70a`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 341.3 KB (341318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67dd63dbd9960fb77efe3da2635624315e5b230e9d0136ff6a61c7667e1e25b`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6af958e54fca1b743938132e070c93737a923c10c0d37af843b754221072e`  
		Last Modified: Wed, 25 Aug 2021 13:41:52 GMT  
		Size: 139.4 MB (139357921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954ad9cafb5aec23d9fb11abca774323d6a853aa361ffcedad5613494b23c93`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98dafaec861f86e2303a05ac82fb338249638e4d85085798cdc5e9fc5b76f27`  
		Last Modified: Wed, 25 Aug 2021 19:29:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc818de352f19f2004712cdda39706ad5004b4c1271cc42d8a60233611cf64`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821ec8a9a1e85d66580448a6b4f6618fe1332d02415302a648a0ec0fb4f074db`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8471a6951d101eba4be159c56c730b5092e3dc7186f71902b34a8c2fd450fa97`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b1f0605dc501c2eb14f989b6a14b369106a5e41c5a9716ebc06c6afbbc0d81`  
		Last Modified: Wed, 25 Aug 2021 19:29:51 GMT  
		Size: 1.7 MB (1728504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c8468929fba91c5ee2288a255b1e7619f9c09a434d631fd20768cfcbd17d14`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:94c1c66eeae5feaeaca8684ac69bab2e5615335d9b8e1c4c27ab2743c0e1de8b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6442269359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b446fe4bd1058c21b63219634d88a9d9df5a9f31133e2434851d9e95305923`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:16:30 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:16:31 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:16:32 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:16:33 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:18:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:48 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:31:48 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:31:49 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:34:39 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:34:41 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:27:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:27:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:27:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:27:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:28:29 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:28:30 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f574487f5e33222a294b80d8246d04988a26a38908346c254fa2647c5a7e028d`  
		Last Modified: Wed, 25 Aug 2021 13:39:45 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e1bdad4b79465c250e34a289c1b634c4874290ec1fa9da12f91124ba323cb8`  
		Last Modified: Wed, 25 Aug 2021 13:39:44 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ca6c7d62e34b14c38c401eb0e5cd89bf7ec9b271c80606691b154e354576ef`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b8e5d43bb747a0877294acd5f9e1e22f072cc43f97874b9ecb708b70e7d96`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c80e7cfb2acdd3bfa5d45d3d78106e313290ca31797c9e09c7a33d383b758e`  
		Last Modified: Wed, 25 Aug 2021 13:40:10 GMT  
		Size: 25.4 MB (25442011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf57eb8b3d45fecbf8fca6bdbb800cf361cce365cd094eb059a82bcb44c0087`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd29eb1ef50bd4fe724ece3a9561ae93cea7d7509126824fded0df0cc4ecdec6`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 344.7 KB (344707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6512f7ffc77c76242888df38f980f80b78fb3a8230566c403838cebeb4bae3`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b245d14d9e193cc5f9cf2a6bd0a099a540ab40c551d463cf481046f9e6dd49ac`  
		Last Modified: Wed, 25 Aug 2021 13:42:48 GMT  
		Size: 143.8 MB (143814166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2271ca3757592eb20dd26ef0b75f72a643a18726ee620f0fda7fc8ab71cc298`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11ee28031df8b44b2509e14bc335b9f37b5f48c3f5bf4e87320948b77e105a`  
		Last Modified: Wed, 25 Aug 2021 19:30:11 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7174be725fdce80ce4b63ab3473b11cb9648e547860d9b802c707bde14e7d9`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8260167642582440a4feef71fce5ddd65334d08b35273698016831c005702fb`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782a41a0abba09324b19eca4010a0c1f4a008f0499b619f1c4acf139b4c67b36`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd614c1c73b684c14eaf7326f746b956f12566201e4ecfe8b836bd436a81f8`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.7 MB (1684554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccc99ea70e3e635c9add2b09e371e07e5ab90668b19b7837f02ed91f8d20c85`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:b4ab80f23735ff30454053be49cfe2e59002772535099b99393a029444628b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:024148c65604529e01fe96436356aef6adc9737caf5784ee97639dc0178c0e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116836974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67f775001477b06c70ee78b6bf98a0ff2eb5c9a458dc030e5c730526e487f8e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:20:55 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:20:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:20:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:23:31 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:25:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:25:15 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:25:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:25:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:25:17 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:15:27 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:15:27 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:15:27 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:15:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:15:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:15:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:15:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e108acfc2dec423245b992f059c15efa90d3da68d666891f88e21cf9ed3044`  
		Last Modified: Fri, 27 Aug 2021 17:26:14 GMT  
		Size: 281.5 KB (281498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d12eec82106ee897382a4e0f5f4012bb993a2abb41ea43f6055affa263792`  
		Last Modified: Fri, 27 Aug 2021 17:26:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba5eda52a4c5e66ad77248b778eeaabf785c0ef090e85270075e82189ccdfc4`  
		Last Modified: Fri, 27 Aug 2021 17:27:13 GMT  
		Size: 105.8 MB (105802322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb85018fe45e8393802b1c7b0b50c6e376a6ca1e8e95626bde089498a365f36`  
		Last Modified: Fri, 27 Aug 2021 17:26:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90db72e3ed64553e72bfe368d98a62d9a915cccbf3fa0c25590581cd4a3cfb5`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 6.6 MB (6626826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2349f3cb068e4777bdf9bcdd5798e514be84f8a1b7c4f6c2cfbfe2ee83c11dcd`  
		Last Modified: Fri, 27 Aug 2021 18:15:52 GMT  
		Size: 1.3 MB (1311166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b310272a238f2d14deb416889fbea68278aa777bf5de85c3c294752976cd54`  
		Last Modified: Fri, 27 Aug 2021 18:15:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a2633b70d3d99f56930313cbc6c8e60f9cb84d8a247952f70ecde4b3d287a61f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112621949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995bf035b94c22d1dfae95d63886ec0360983d1862a4f0b9934cfad4c223eecf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:51:48 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:51:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:51:50 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:56:06 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:58:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:58:48 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:58:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:58:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:58:51 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:58:16 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:58:16 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:58:17 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:58:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:58:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:58:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:58:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def35433210b819c72fc8c3f4cefb914a4d2072a396498b271719a29363f24a2`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 281.7 KB (281662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fbd33b2207f0f6c992e5356a6285f8362b9ddf3f61650c7493aa2568c9fa1`  
		Last Modified: Fri, 27 Aug 2021 18:00:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8584a59dc2c89569cc10317112977b3957c6ab4369fad184c5d8f616e7bf78ba`  
		Last Modified: Fri, 27 Aug 2021 18:03:31 GMT  
		Size: 102.0 MB (102005169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28236e9ee5408a1ebfbc1993365e25c57923224e6608703e02685d3aada63456`  
		Last Modified: Fri, 27 Aug 2021 18:02:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bde7b63fd968f5c9eceab8094063f4937b1da8306aa777963db7cbb714883f`  
		Last Modified: Fri, 27 Aug 2021 18:59:31 GMT  
		Size: 6.5 MB (6485279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8f7ef25d584b1a6933ca79bb2c78a3fc206f53a38ab1ddd7060ecbe2a933dd`  
		Last Modified: Fri, 27 Aug 2021 18:59:28 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bf61c4b3d04e6edd3304db5bd03a3241100e4d350312263ff17271a6dc69a6`  
		Last Modified: Fri, 27 Aug 2021 18:59:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:34333a1acab5cdd87309f11e0d23c3d4c6b8685b0160f307ba7206972d37853e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111501647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231aa2a8195b5e48739d3233aacb263ab4462039e3fdd181e304186924795270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:27:52 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 19:27:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 19:27:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:33:26 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 19:36:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 19:36:54 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 19:36:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 19:36:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 19:37:01 GMT
WORKDIR /go
# Sat, 07 Aug 2021 03:50:59 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 03:51:00 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 03:51:00 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 03:51:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 03:51:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 03:51:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 03:51:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc7b26480300ed9c6eddb3c4eb897051a740425806a7edff4973e09fae2bb8f`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 280.8 KB (280814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba13042e2b42dba9e7f0e57a60855dff15f2890b8d942f61fbdc4852a43854`  
		Last Modified: Fri, 06 Aug 2021 19:45:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a06372885d9e72431bcb74f5cbb21c55f0607374a0dc1a7261e0fdffe19a389`  
		Last Modified: Fri, 06 Aug 2021 19:47:59 GMT  
		Size: 101.8 MB (101786462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbeda0e3490d50d1412a7145a405521667a31542915116d5bca87d1f262a3ba6`  
		Last Modified: Fri, 06 Aug 2021 19:47:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c45b3f2b54d4bc0ce5312c296a0f2073fa104179f9935212b88b9e9e4981251`  
		Last Modified: Sat, 07 Aug 2021 03:52:09 GMT  
		Size: 5.8 MB (5784805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e389ea9eac74a8896f796d9c785720d528a709e5ec82bf35fa05f7d36e8c2d`  
		Last Modified: Sat, 07 Aug 2021 03:52:07 GMT  
		Size: 1.2 MB (1219493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1adc87d17fa7707fc23fe9ed965dd55d2704211e52c5a765628d42ba2439dab`  
		Last Modified: Sat, 07 Aug 2021 03:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6f976dea79506be1124a40be07324506d379f104afb6b4eb7d7ac3ebd1f81143
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112055672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b827a8f7150bc8bc38ad14e96bb8ec14de011b8352d944d532735984a1f6f119`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:41:17 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:41:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:41:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:43:33 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:45:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:45:02 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:45:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:45:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:45:03 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:35:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:35:10 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:35:10 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:35:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:35:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:35:12 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:35:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e34390c2b14c7d6b4929bed3213d6d86bb9aa93c4ec135494e476afbb7c8ff`  
		Last Modified: Fri, 27 Aug 2021 17:46:50 GMT  
		Size: 281.7 KB (281688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f557407009b175f4d46f52d9e57a4123bc5118b57e0a250e983230d791682`  
		Last Modified: Fri, 27 Aug 2021 17:46:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b522346004414564cf2d79fa6ca0b9efd60f64f3cb1cfc754f94dea608d2a9`  
		Last Modified: Fri, 27 Aug 2021 17:48:05 GMT  
		Size: 101.1 MB (101121978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e36f943c088c76ce04cebeee6e3b83058ecf72465cbb1807ce21d94b09b892`  
		Last Modified: Fri, 27 Aug 2021 17:47:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f7d54a0c7c055c4b4d79ed1dee9267b227d3fe5987a13e382a3a92c14f30fa`  
		Last Modified: Fri, 27 Aug 2021 18:35:48 GMT  
		Size: 6.7 MB (6737926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1225f39dda93839c2256ed41c7299db86680c6c805344be7c064a34211daa`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 1.2 MB (1201538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87cf0ee91a4aba520fb94188e3d73181288f133c2b42cc0add124bc59519f0`  
		Last Modified: Fri, 27 Aug 2021 18:35:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4cb744a2c30bef1fce63b25f25090e9a6fba23d518fbfb8a67f2de5437567654
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110962703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc63a956570ca25fb6e8cda280b13ba663c3f8268fcfd235e0f50e7efe03073`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:02:31 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 06 Aug 2021 21:02:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 06 Aug 2021 21:02:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:06:00 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 06 Aug 2021 21:07:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Aug 2021 21:08:01 GMT
ENV GOPATH=/go
# Fri, 06 Aug 2021 21:08:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:08:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Aug 2021 21:08:22 GMT
WORKDIR /go
# Sat, 07 Aug 2021 04:22:15 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 07 Aug 2021 04:22:17 GMT
ENV XCADDY_VERSION=v0.1.9
# Sat, 07 Aug 2021 04:22:21 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 07 Aug 2021 04:22:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 07 Aug 2021 04:22:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 07 Aug 2021 04:22:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 07 Aug 2021 04:22:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f69fce9d10f5a5c047377039cda1fd5125aae4ec022be3dd7aede58be5a483`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 283.6 KB (283642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fdcb934d4034adf5e88a3b7bff7a633580eb8c0f18480df4123a14c499558b`  
		Last Modified: Fri, 06 Aug 2021 21:12:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c6309d0f42f3d590978baeb06a18f86672f414b4fd6b6c0167fbaf5bc68502`  
		Last Modified: Fri, 06 Aug 2021 21:13:47 GMT  
		Size: 99.6 MB (99599293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6b0f08798744f7a5f5fbd19a9db24d1ce885fdb4cf4cc03cb9016e172748d1`  
		Last Modified: Fri, 06 Aug 2021 21:13:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86fe8978f31161530210163b69b5fc67ce11e38c091caab64bb0e3734496a18`  
		Last Modified: Sat, 07 Aug 2021 04:23:35 GMT  
		Size: 7.1 MB (7097385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356115fa932b78fceaeae3fba2bd7a0ff5efa89ebf9e8b5c824b679a666489c9`  
		Last Modified: Sat, 07 Aug 2021 04:23:34 GMT  
		Size: 1.2 MB (1170513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dc07db71f320869edaa3ef484018fc6b46b8bc0671ef668991e69bbda13f51`  
		Last Modified: Sat, 07 Aug 2021 04:23:33 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bb67f227515b2c32c0cfb3be1c48ff701cc4c525a59532d36b7166fc7aa27a21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115812998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6d4ca5bd25723d47c42919ec6d0b4bf7dd34a67583e8f3f2c95098e2142131`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:43:22 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 27 Aug 2021 17:43:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Aug 2021 17:43:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:46:35 GMT
ENV GOLANG_VERSION=1.16.7
# Fri, 27 Aug 2021 17:48:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 	sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		./make.bash; 	); 		go install std; 		apk del --no-network .build-deps; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 27 Aug 2021 17:48:50 GMT
ENV GOPATH=/go
# Fri, 27 Aug 2021 17:48:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:48:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 27 Aug 2021 17:48:53 GMT
WORKDIR /go
# Fri, 27 Aug 2021 18:49:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 27 Aug 2021 18:49:45 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 27 Aug 2021 18:49:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 27 Aug 2021 18:49:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 27 Aug 2021 18:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 27 Aug 2021 18:49:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 27 Aug 2021 18:49:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccc77cb0a413e660cd5721d395bcec1266cde4d0528e29f1a042fabaa43ff5`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 281.9 KB (281940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d321b5acef374adaa49f78ae74b037995382f01d1353f489b334a6fc4cce81`  
		Last Modified: Fri, 27 Aug 2021 17:50:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3f97bf1abc32dcb5c030e0f8d3abc990e9506ad219ab5cfb5827d15eaa02a`  
		Last Modified: Fri, 27 Aug 2021 17:51:47 GMT  
		Size: 104.9 MB (104940257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441e24829e5d83d1fd83b07e02e0a42bb1d31648314f63b39d44649802a9ee4a`  
		Last Modified: Fri, 27 Aug 2021 17:51:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf03157bc49c8e5393f28b8d4b4a6be766de31b9fc52348246bbe4ff2e7f7c7`  
		Last Modified: Fri, 27 Aug 2021 18:50:30 GMT  
		Size: 6.7 MB (6722103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f71cb40139c0ff03eef852eeea459437e95ca53c5ce0b8b7e1c1d49bab7a4`  
		Last Modified: Fri, 27 Aug 2021 18:50:29 GMT  
		Size: 1.3 MB (1264520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30ad513b9c90196100f4853c9b4d82e758c4acf048b7934bfa29a0fc2b27bd`  
		Last Modified: Fri, 27 Aug 2021 18:50:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a650332bf33eaced67086712173ed2278573f04f8fe94b11682e52eb1222d4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:94548298bfccdd350db6f2fa27451effe035e5a1ed853df975c01413c49e19d8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2852923514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60de2cad586e35e33930f37908e1952dee5a28c8f9e23cf4c92f0c39732dfb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:09:49 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:09:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:09:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:11:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:26:22 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:27:40 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:27:40 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:30:27 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:29 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:26:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:26:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:26:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:26:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:27:28 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:27:29 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07d2bb4c99ec6467c6c9f474360867d31d27d22bc5be8432059a33a7c602a8`  
		Last Modified: Wed, 25 Aug 2021 13:38:54 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c31ebb0e52f79c34d0f70b88124ab4959963315dd2da2ec7117063a82d1392`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1935f777314159e43ee24dde17dba33b985a315578d33ec24796ba0ad27f679c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae930e0413fc2f7343e0b46be3ab58503ac4c137e8e6f83c7341838a22c88f3c`  
		Last Modified: Wed, 25 Aug 2021 13:38:51 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6bfd344bdb877d2969098eeb083c114ac4a7ef914d7dcf8eaef4d16e1e248c`  
		Last Modified: Wed, 25 Aug 2021 13:39:17 GMT  
		Size: 25.5 MB (25479918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffc00e2e1aed22bd02a7ac4e30d76d19f6caf0f9897e84d157e7af3c568f644`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f60594f1e4d8c227175212ac0226bec052e45a6f2ac058aa4845f0adc2c70a`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 341.3 KB (341318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67dd63dbd9960fb77efe3da2635624315e5b230e9d0136ff6a61c7667e1e25b`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6af958e54fca1b743938132e070c93737a923c10c0d37af843b754221072e`  
		Last Modified: Wed, 25 Aug 2021 13:41:52 GMT  
		Size: 139.4 MB (139357921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954ad9cafb5aec23d9fb11abca774323d6a853aa361ffcedad5613494b23c93`  
		Last Modified: Wed, 25 Aug 2021 13:41:23 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98dafaec861f86e2303a05ac82fb338249638e4d85085798cdc5e9fc5b76f27`  
		Last Modified: Wed, 25 Aug 2021 19:29:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc818de352f19f2004712cdda39706ad5004b4c1271cc42d8a60233611cf64`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821ec8a9a1e85d66580448a6b4f6618fe1332d02415302a648a0ec0fb4f074db`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8471a6951d101eba4be159c56c730b5092e3dc7186f71902b34a8c2fd450fa97`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b1f0605dc501c2eb14f989b6a14b369106a5e41c5a9716ebc06c6afbbc0d81`  
		Last Modified: Wed, 25 Aug 2021 19:29:51 GMT  
		Size: 1.7 MB (1728504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c8468929fba91c5ee2288a255b1e7619f9c09a434d631fd20768cfcbd17d14`  
		Last Modified: Wed, 25 Aug 2021 19:29:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:7ebaf26507754bcf51a3c839f0a4cdec367302d2c4f69b1f816c2f1f8fd2697c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4583; amd64

### `caddy:builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:94c1c66eeae5feaeaca8684ac69bab2e5615335d9b8e1c4c27ab2743c0e1de8b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6442269359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b446fe4bd1058c21b63219634d88a9d9df5a9f31133e2434851d9e95305923`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 13:16:30 GMT
ENV GIT_VERSION=2.23.0
# Wed, 25 Aug 2021 13:16:31 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 25 Aug 2021 13:16:32 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 25 Aug 2021 13:16:33 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 25 Aug 2021 13:18:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:30:48 GMT
ENV GOPATH=C:\gopath
# Wed, 25 Aug 2021 13:31:48 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Aug 2021 13:31:49 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 25 Aug 2021 13:34:39 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 13:34:41 GMT
WORKDIR C:\gopath
# Wed, 25 Aug 2021 19:27:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:27:36 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 25 Aug 2021 19:27:37 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:27:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 25 Aug 2021 19:28:29 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 25 Aug 2021 19:28:30 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f574487f5e33222a294b80d8246d04988a26a38908346c254fa2647c5a7e028d`  
		Last Modified: Wed, 25 Aug 2021 13:39:45 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e1bdad4b79465c250e34a289c1b634c4874290ec1fa9da12f91124ba323cb8`  
		Last Modified: Wed, 25 Aug 2021 13:39:44 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ca6c7d62e34b14c38c401eb0e5cd89bf7ec9b271c80606691b154e354576ef`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b8e5d43bb747a0877294acd5f9e1e22f072cc43f97874b9ecb708b70e7d96`  
		Last Modified: Wed, 25 Aug 2021 13:39:43 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c80e7cfb2acdd3bfa5d45d3d78106e313290ca31797c9e09c7a33d383b758e`  
		Last Modified: Wed, 25 Aug 2021 13:40:10 GMT  
		Size: 25.4 MB (25442011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf57eb8b3d45fecbf8fca6bdbb800cf361cce365cd094eb059a82bcb44c0087`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd29eb1ef50bd4fe724ece3a9561ae93cea7d7509126824fded0df0cc4ecdec6`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 344.7 KB (344707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6512f7ffc77c76242888df38f980f80b78fb3a8230566c403838cebeb4bae3`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b245d14d9e193cc5f9cf2a6bd0a099a540ab40c551d463cf481046f9e6dd49ac`  
		Last Modified: Wed, 25 Aug 2021 13:42:48 GMT  
		Size: 143.8 MB (143814166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2271ca3757592eb20dd26ef0b75f72a643a18726ee620f0fda7fc8ab71cc298`  
		Last Modified: Wed, 25 Aug 2021 13:42:19 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11ee28031df8b44b2509e14bc335b9f37b5f48c3f5bf4e87320948b77e105a`  
		Last Modified: Wed, 25 Aug 2021 19:30:11 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7174be725fdce80ce4b63ab3473b11cb9648e547860d9b802c707bde14e7d9`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8260167642582440a4feef71fce5ddd65334d08b35273698016831c005702fb`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782a41a0abba09324b19eca4010a0c1f4a008f0499b619f1c4acf139b4c67b36`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd614c1c73b684c14eaf7326f746b956f12566201e4ecfe8b836bd436a81f8`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.7 MB (1684554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccc99ea70e3e635c9add2b09e371e07e5ab90668b19b7837f02ed91f8d20c85`  
		Last Modified: Wed, 25 Aug 2021 19:30:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:d235036337fad2117f058e44b0ce4813f974924e03ff629da08dbee7c6be5e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:77f27025e0e1e0ab97bc931db61d24f9ac41591e17576ab46c4b508afbccacd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14648199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8a741f4852592d8634aa37c7f351ae4f4e7b4a9a2594df54603ac48cbdad74`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:11:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 11 May 2021 01:04:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 19:19:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 19:19:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 19:19:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 19:19:31 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 19:19:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 19:19:32 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 19:19:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 19:19:33 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 19:19:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 443
# Thu, 24 Jun 2021 19:19:34 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 19:19:34 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 19:19:34 GMT
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
	-	`sha256:16798e0582fce7af9c2ba2c8ee4990d0fd1e58384e170ee9937486253d67bbf1`  
		Last Modified: Tue, 11 May 2021 01:05:00 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d589bc046eca71df600301462981053bf178fcd31d4b2c882ca05aec70bacd`  
		Last Modified: Thu, 24 Jun 2021 19:19:59 GMT  
		Size: 11.5 MB (11529821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8ce9421f330c9a085ac8f059d2dd53feabf795c461d4f43b596d0302b1cf9`  
		Last Modified: Thu, 24 Jun 2021 19:19:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:615389b06a74c80f0494cdc47da7b9f565cadd8cd715e39d7b65aaaf2937b6cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13816604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac08c3d5e13d15da24bbe2b6e7bd0fe9a42212188c3f33467bb1f38dfdb0b51`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 22:32:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 22:32:24 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 22:32:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 22:32:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 22:32:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 22:32:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 22:32:36 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 22:32:37 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 22:32:37 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 22:32:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 22:32:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 22:32:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 22:32:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 22:32:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 22:32:44 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:32:45 GMT
EXPOSE 443
# Fri, 30 Jul 2021 22:32:46 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 22:32:46 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 22:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18943f91e0b98a5ee778a791cc00f627dfc62e6163be04be39d8dfca48ca309`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 300.5 KB (300515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6779ad883f93abbe8842bc2dd07f67be174891b4b835e18a7eccb5a738ee0eb9`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6cb30c4e53dad6055df249f24807530e7530d534f18b81671b80de7b8b0ad2`  
		Last Modified: Fri, 30 Jul 2021 22:34:16 GMT  
		Size: 10.9 MB (10887954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a803ba6ef03f0246aec715857792f54efc64816b24b563beee84263dd1ad439`  
		Last Modified: Fri, 30 Jul 2021 22:34:11 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c382c62559cf6348cccc2048f7f6e3234ad6c3322fa778f0d7ab3fbe27cd44e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13593493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c6676bf8617209d68af4cbdd3c3edb6084cbd01e6c7f00b706fab8934f311a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Fri, 30 Jul 2021 18:36:39 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:13:40 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 02:13:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 02:13:44 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 02:13:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 02:13:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 02:13:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 02:13:52 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 02:13:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 02:13:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 02:13:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 02:13:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 02:13:56 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 443
# Sat, 31 Jul 2021 02:13:57 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 02:13:58 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 02:13:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf509b321d9275e96242772f4cd73ad8da2970e30e18c0f2326ed91777442e`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 299.7 KB (299672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16416239cfcd26ea4cc02aaf7ac5511b6ea5d6cc672046b6e61d90f9c59ffaac`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 5.9 KB (5854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de14f3facde68cf2e2470839f96bb111537c6b40d15a1b28c47c6568261ee15`  
		Last Modified: Sat, 31 Jul 2021 02:15:20 GMT  
		Size: 10.9 MB (10863669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6b241bda44fe422ccd7c0c967fb01d2d7a191df7b0628d9c44df2d18dd5445`  
		Last Modified: Sat, 31 Jul 2021 02:15:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ee1b9ce06277bd5c34b2d9a6908cdb3028aa838fa75e5c6e1e32d2cabb417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13464756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a697a3b5305c041fd956ba80c8845676041e98bce128a69e70074e5abe9653dd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 22:32:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 15 Jun 2021 22:32:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Thu, 24 Jun 2021 18:39:27 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 18:39:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Jun 2021 18:39:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Jun 2021 18:39:30 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/config]
# Thu, 24 Jun 2021 18:39:31 GMT
VOLUME [/data]
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 18:39:31 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 18:39:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 80
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 443
# Thu, 24 Jun 2021 18:39:33 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 18:39:33 GMT
WORKDIR /srv
# Thu, 24 Jun 2021 18:39:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d0b72044755ebd2b829600b94a69aa9096bbb4bf9a01c1795b5b245261b99a`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 300.6 KB (300631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abde659ccf1d73128ef1e71a9701b014e0f27d4abf15b3d410d0474cdd0adb95`  
		Last Modified: Tue, 15 Jun 2021 22:33:24 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75403ccf5c23126b5dca334871ec0096a90d0fb85f47be1ecba3904921529c0`  
		Last Modified: Thu, 24 Jun 2021 18:40:18 GMT  
		Size: 10.4 MB (10446098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a85edeaa46fe5e0185f11a1a1801c0d0458e59897d3c04e97136df1c496663`  
		Last Modified: Thu, 24 Jun 2021 18:40:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:fff2119338c215eceae68398483da801f5daf8bb5405c7ed8db5769aeb367cd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13173634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced11b632073f0e249ba02b8326f0c1ccf6c154d4340342b38c8b3f830c37e70`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:24:49 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Fri, 30 Jul 2021 17:24:54 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:36:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 31 Jul 2021 00:36:51 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 31 Jul 2021 00:36:54 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 31 Jul 2021 00:37:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 31 Jul 2021 00:37:10 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 31 Jul 2021 00:37:12 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 31 Jul 2021 00:37:14 GMT
ENV XDG_DATA_HOME=/data
# Sat, 31 Jul 2021 00:37:17 GMT
VOLUME [/config]
# Sat, 31 Jul 2021 00:37:23 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 00:37:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 31 Jul 2021 00:37:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 31 Jul 2021 00:37:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 31 Jul 2021 00:37:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 31 Jul 2021 00:37:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 31 Jul 2021 00:37:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 31 Jul 2021 00:37:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 31 Jul 2021 00:38:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 31 Jul 2021 00:38:06 GMT
EXPOSE 80
# Sat, 31 Jul 2021 00:38:09 GMT
EXPOSE 443
# Sat, 31 Jul 2021 00:38:16 GMT
EXPOSE 2019
# Sat, 31 Jul 2021 00:38:25 GMT
WORKDIR /srv
# Sat, 31 Jul 2021 00:38:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396ee5e0a948db1cebd77a9b357abbc39c60dc4caf97f87f759a1f232a291da5`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 302.5 KB (302545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c405a506bbc65ab625ac9298a31abc4a1871eef7b93ff4fbc6a25fb9db591a4`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ac195b709078a7d439cd22a970947cb2ed3f9cd136a8d51324ab3d3c746625`  
		Last Modified: Sat, 31 Jul 2021 00:39:16 GMT  
		Size: 10.1 MB (10051943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2c9f1da5ba05b5656393520168363c5d8a223167645bc0a4451fcd4c2f5447`  
		Last Modified: Sat, 31 Jul 2021 00:39:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:576d8d6d9dead63f0cc0db39ad0fb1e9e9539bf5b23a8b70623b7e8f40d916a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14005959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6114aef9a435617ae101cc26569f3f2103cd2c999ef3e41df780270222452a1f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 30 Jul 2021 17:41:41 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Fri, 30 Jul 2021 17:41:42 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 23:50:44 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 30 Jul 2021 23:50:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 30 Jul 2021 23:50:46 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 30 Jul 2021 23:50:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 30 Jul 2021 23:50:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 30 Jul 2021 23:50:49 GMT
ENV XDG_DATA_HOME=/data
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/config]
# Fri, 30 Jul 2021 23:50:50 GMT
VOLUME [/data]
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 30 Jul 2021 23:50:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 30 Jul 2021 23:50:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 30 Jul 2021 23:50:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 80
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 443
# Fri, 30 Jul 2021 23:50:52 GMT
EXPOSE 2019
# Fri, 30 Jul 2021 23:50:52 GMT
WORKDIR /srv
# Fri, 30 Jul 2021 23:50:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de364003ff53d3ed839a7d8fd8cc6c59936d04b22886595d954e5c9929cfe0e1`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 300.9 KB (300858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d9b83bb28f1c9bc97f9a4907425be62b28dd687b54e3b8d461b2e40203110d`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076584d90c472ad966977bc9f55f53439edb7b5169fa684c1a70a1ea682037ca`  
		Last Modified: Fri, 30 Jul 2021 23:51:34 GMT  
		Size: 11.1 MB (11096451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f126f1c964e9405478f4683dd4b8e93297166d84566a652fe658f36bad6390c`  
		Last Modified: Fri, 30 Jul 2021 23:51:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:277245d2976e25118dde31aa817da26aab9a54b716478e335e7e47a655680fdf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdb54faaf1277fc5d472259e6d51ac14101b59691359db53c189a9f55df03c8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:21:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:21:12 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:22:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:22:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:22:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:22:18 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:22:19 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:22:20 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:22:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:22:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:22:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:22:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:22:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:22:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:22:28 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:22:29 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:22:30 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:23:15 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:23:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc78244c47d63e7118efa5a81aeac258859631816cf0d2e335045eddd6d4562c`  
		Last Modified: Wed, 25 Aug 2021 19:29:08 GMT  
		Size: 390.1 KB (390074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e85659c5ef3d6f1826cce92e5c35cbda668ec96e58661902ea89472385a68`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad534458f62e8592943908290a647cce35c3f5ed0761b80f7d17f55393900e`  
		Last Modified: Wed, 25 Aug 2021 19:29:10 GMT  
		Size: 12.0 MB (12023423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e1aa1a15f7618a90c91ce39aeb28f0b14d0fb039a0a5c387e2d7a4460443aa`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a259cd0cf699d1891ff65f72aaf75b8b53d32409fdbab40fa8aa3594f4edb`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb72b357bee0361ca5587e675d3a832276f086a2d6535147bfe92a000cf044f`  
		Last Modified: Wed, 25 Aug 2021 19:29:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbe28f726b8cddbd0398281cfc45f2dc82f378bef80fa1dfe4dec201451721`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a73648024b9f42aeeda4c4309ba545e089e6943b686c93ea09cec6ac83373`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ad45ece5f60db2673be4be17ca0ac1ff391d32d88f7a84e2e671fca6744e0`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424371920e55efd886bea3b4671eca80436677674986f299b919e72c49d4289`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2b299f27503c9be94a9a16c137b08ba7e2b84cc07b96a281d4b2886b231f0`  
		Last Modified: Wed, 25 Aug 2021 19:29:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c231726719db989f9746b39a4b4b9b54646376e1dc36c124a1401fc15132`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ae0be18044dcf67b8832f125744410261cc8601712176399a3cd632b8843`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b94a88e7f4db3aa538dad13b42b51168525142c8268098dbe8a7175decee6`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0f35247abb67063d217ea9963f29270e1716b21409196f0e935710342a9dd9`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fa12b6daf14192bb460b568c8c3f65625b384fbcfa33e4b227d39de751374d`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43dbbbd0c30fabb616088a2f902ad0177c216707c4e134d10b9a1cd4fde8cb`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee931681f757a39ac6ce152aa1d64f251a68f63dca6dbe3459c2cec9bed0d90e`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deb6e04a956a5c619ff2eb344a4e5fcf8384d890b8120ce2ffd91cf20e0b5f`  
		Last Modified: Wed, 25 Aug 2021 19:29:00 GMT  
		Size: 320.7 KB (320709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b510aa21fdb81bb0a2156b0a977a69ea8187f959ceb05869b1450d9359814`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:bd0551e2eeef6d131272af5e4214599dfc85e2a18d421264005a4f8dc3025a02
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283675023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96c9f880047fab4000d8bad0dceb15c3e478898181805e15b864f3ae980f11`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:24:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:24:21 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:25:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:25:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:25:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:25:25 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:25:26 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:25:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:25:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:25:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:25:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:25:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:25:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:25:35 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:25:36 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:25:37 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:26:16 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:26:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9dee8014da227cc8c6b8d14f6464fefc307c265b07a34d6e2ccc5de24a92a`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 352.7 KB (352700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d26c5819d131639ab53b8e099ab2ed93c63f759072d3a5ce4b9f69f13b8a66`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb3ea0fdbcaf7cab1dbac86676ab00ca78ebf68e3b5c476c5984201c357976`  
		Last Modified: Wed, 25 Aug 2021 19:29:35 GMT  
		Size: 12.0 MB (12025369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a331953cb55eb8482f8b09c1ccb30b06198b0da91f196aa230d56d4f626c3`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c66a58bae64f63c34265474f15131687cba250a5cbeb2166a25d383630b68`  
		Last Modified: Wed, 25 Aug 2021 19:29:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b60346916eaf0cd70873400273d0f0de4f72aa7ee5a5bd6a8cfbe446d62499`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74af1f53b1dc6d2f58a23760f463877d707150f1cae25c0ca6a727c64cd7e9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4467e0d432e5bba7c8e197c057837e438ae63c8748b9765a8d7591c0ea12c0`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c92db8b514f6d653c3d0ba5a7e695e808f5880504124fb94648c10590f7f3c9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63a5575b8310dcb9cbe40352e7753a4bb8f66f1c3fbea055abda03136638d6`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415f534f6818ea980cf13f9a08c0efb9d60c9f86760129563e203ba93e399c8`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be354de1af39afc991030861814f135bfde0267a02f004fd4caf9ccc31d0bfd`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a0ebb3c5c8d126c85ccbad571fef0051ac62cfec3fe5885c82110381049ed9`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893f40ed74354bd380ee49a7141c654ea10f5a43f1e050539bde502c7214c9f`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd03947508d81a8a5c939b4a1697e4cf18bc8722cc1650732f8df2c6924941`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c43d724632362e78f09ee6bf53a8359cdd6db65300cb3687f2ad3a59e1a5d`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaec774cf06dd02e7ebdf8d5e9aa9b8d4578a60c7a54ce84421910922396b7`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb3d76a117ff8038563015df19972676ff4aea085431ef698f57799559b334`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341d5f41a06e42738b97ffd6ca2835680879ba4113b882c5cd8accd857c0551`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 305.6 KB (305571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd0dece66bb4a5f39d723d7d27311fa04d1de60c084735f41cb588c7b4d5701`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:e5e5fb2f39e631146f8c890d36e0a2e6e150c66d5ee959a580002e4032761392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:277245d2976e25118dde31aa817da26aab9a54b716478e335e7e47a655680fdf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdb54faaf1277fc5d472259e6d51ac14101b59691359db53c189a9f55df03c8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:21:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:21:12 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:22:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:22:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:22:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:22:18 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:22:19 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:22:20 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:22:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:22:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:22:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:22:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:22:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:22:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:22:28 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:22:29 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:22:30 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:23:15 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:23:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc78244c47d63e7118efa5a81aeac258859631816cf0d2e335045eddd6d4562c`  
		Last Modified: Wed, 25 Aug 2021 19:29:08 GMT  
		Size: 390.1 KB (390074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e85659c5ef3d6f1826cce92e5c35cbda668ec96e58661902ea89472385a68`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad534458f62e8592943908290a647cce35c3f5ed0761b80f7d17f55393900e`  
		Last Modified: Wed, 25 Aug 2021 19:29:10 GMT  
		Size: 12.0 MB (12023423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e1aa1a15f7618a90c91ce39aeb28f0b14d0fb039a0a5c387e2d7a4460443aa`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a259cd0cf699d1891ff65f72aaf75b8b53d32409fdbab40fa8aa3594f4edb`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb72b357bee0361ca5587e675d3a832276f086a2d6535147bfe92a000cf044f`  
		Last Modified: Wed, 25 Aug 2021 19:29:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbe28f726b8cddbd0398281cfc45f2dc82f378bef80fa1dfe4dec201451721`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a73648024b9f42aeeda4c4309ba545e089e6943b686c93ea09cec6ac83373`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ad45ece5f60db2673be4be17ca0ac1ff391d32d88f7a84e2e671fca6744e0`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424371920e55efd886bea3b4671eca80436677674986f299b919e72c49d4289`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2b299f27503c9be94a9a16c137b08ba7e2b84cc07b96a281d4b2886b231f0`  
		Last Modified: Wed, 25 Aug 2021 19:29:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c231726719db989f9746b39a4b4b9b54646376e1dc36c124a1401fc15132`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ae0be18044dcf67b8832f125744410261cc8601712176399a3cd632b8843`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b94a88e7f4db3aa538dad13b42b51168525142c8268098dbe8a7175decee6`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0f35247abb67063d217ea9963f29270e1716b21409196f0e935710342a9dd9`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fa12b6daf14192bb460b568c8c3f65625b384fbcfa33e4b227d39de751374d`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43dbbbd0c30fabb616088a2f902ad0177c216707c4e134d10b9a1cd4fde8cb`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee931681f757a39ac6ce152aa1d64f251a68f63dca6dbe3459c2cec9bed0d90e`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deb6e04a956a5c619ff2eb344a4e5fcf8384d890b8120ce2ffd91cf20e0b5f`  
		Last Modified: Wed, 25 Aug 2021 19:29:00 GMT  
		Size: 320.7 KB (320709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b510aa21fdb81bb0a2156b0a977a69ea8187f959ceb05869b1450d9359814`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:bd0551e2eeef6d131272af5e4214599dfc85e2a18d421264005a4f8dc3025a02
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283675023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96c9f880047fab4000d8bad0dceb15c3e478898181805e15b864f3ae980f11`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:24:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:24:21 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:25:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:25:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:25:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:25:25 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:25:26 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:25:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:25:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:25:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:25:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:25:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:25:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:25:35 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:25:36 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:25:37 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:26:16 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:26:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9dee8014da227cc8c6b8d14f6464fefc307c265b07a34d6e2ccc5de24a92a`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 352.7 KB (352700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d26c5819d131639ab53b8e099ab2ed93c63f759072d3a5ce4b9f69f13b8a66`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb3ea0fdbcaf7cab1dbac86676ab00ca78ebf68e3b5c476c5984201c357976`  
		Last Modified: Wed, 25 Aug 2021 19:29:35 GMT  
		Size: 12.0 MB (12025369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a331953cb55eb8482f8b09c1ccb30b06198b0da91f196aa230d56d4f626c3`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c66a58bae64f63c34265474f15131687cba250a5cbeb2166a25d383630b68`  
		Last Modified: Wed, 25 Aug 2021 19:29:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b60346916eaf0cd70873400273d0f0de4f72aa7ee5a5bd6a8cfbe446d62499`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74af1f53b1dc6d2f58a23760f463877d707150f1cae25c0ca6a727c64cd7e9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4467e0d432e5bba7c8e197c057837e438ae63c8748b9765a8d7591c0ea12c0`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c92db8b514f6d653c3d0ba5a7e695e808f5880504124fb94648c10590f7f3c9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63a5575b8310dcb9cbe40352e7753a4bb8f66f1c3fbea055abda03136638d6`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415f534f6818ea980cf13f9a08c0efb9d60c9f86760129563e203ba93e399c8`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be354de1af39afc991030861814f135bfde0267a02f004fd4caf9ccc31d0bfd`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a0ebb3c5c8d126c85ccbad571fef0051ac62cfec3fe5885c82110381049ed9`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893f40ed74354bd380ee49a7141c654ea10f5a43f1e050539bde502c7214c9f`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd03947508d81a8a5c939b4a1697e4cf18bc8722cc1650732f8df2c6924941`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c43d724632362e78f09ee6bf53a8359cdd6db65300cb3687f2ad3a59e1a5d`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaec774cf06dd02e7ebdf8d5e9aa9b8d4578a60c7a54ce84421910922396b7`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb3d76a117ff8038563015df19972676ff4aea085431ef698f57799559b334`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341d5f41a06e42738b97ffd6ca2835680879ba4113b882c5cd8accd857c0551`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 305.6 KB (305571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd0dece66bb4a5f39d723d7d27311fa04d1de60c084735f41cb588c7b4d5701`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:50783893bffe979472583ab27a4a4346cdeb5895077ff67af22283b65699eda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull caddy@sha256:277245d2976e25118dde31aa817da26aab9a54b716478e335e7e47a655680fdf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdb54faaf1277fc5d472259e6d51ac14101b59691359db53c189a9f55df03c8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:21:11 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:21:12 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:22:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:22:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:22:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:22:18 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:22:19 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:22:20 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:22:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:22:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:22:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:22:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:22:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:22:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:22:28 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:22:29 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:22:30 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:23:15 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:23:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc78244c47d63e7118efa5a81aeac258859631816cf0d2e335045eddd6d4562c`  
		Last Modified: Wed, 25 Aug 2021 19:29:08 GMT  
		Size: 390.1 KB (390074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e85659c5ef3d6f1826cce92e5c35cbda668ec96e58661902ea89472385a68`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ad534458f62e8592943908290a647cce35c3f5ed0761b80f7d17f55393900e`  
		Last Modified: Wed, 25 Aug 2021 19:29:10 GMT  
		Size: 12.0 MB (12023423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e1aa1a15f7618a90c91ce39aeb28f0b14d0fb039a0a5c387e2d7a4460443aa`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a259cd0cf699d1891ff65f72aaf75b8b53d32409fdbab40fa8aa3594f4edb`  
		Last Modified: Wed, 25 Aug 2021 19:29:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb72b357bee0361ca5587e675d3a832276f086a2d6535147bfe92a000cf044f`  
		Last Modified: Wed, 25 Aug 2021 19:29:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbe28f726b8cddbd0398281cfc45f2dc82f378bef80fa1dfe4dec201451721`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a73648024b9f42aeeda4c4309ba545e089e6943b686c93ea09cec6ac83373`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ad45ece5f60db2673be4be17ca0ac1ff391d32d88f7a84e2e671fca6744e0`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424371920e55efd886bea3b4671eca80436677674986f299b919e72c49d4289`  
		Last Modified: Wed, 25 Aug 2021 19:29:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c2b299f27503c9be94a9a16c137b08ba7e2b84cc07b96a281d4b2886b231f0`  
		Last Modified: Wed, 25 Aug 2021 19:29:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c231726719db989f9746b39a4b4b9b54646376e1dc36c124a1401fc15132`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ae0be18044dcf67b8832f125744410261cc8601712176399a3cd632b8843`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b94a88e7f4db3aa538dad13b42b51168525142c8268098dbe8a7175decee6`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0f35247abb67063d217ea9963f29270e1716b21409196f0e935710342a9dd9`  
		Last Modified: Wed, 25 Aug 2021 19:29:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fa12b6daf14192bb460b568c8c3f65625b384fbcfa33e4b227d39de751374d`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43dbbbd0c30fabb616088a2f902ad0177c216707c4e134d10b9a1cd4fde8cb`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee931681f757a39ac6ce152aa1d64f251a68f63dca6dbe3459c2cec9bed0d90e`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deb6e04a956a5c619ff2eb344a4e5fcf8384d890b8120ce2ffd91cf20e0b5f`  
		Last Modified: Wed, 25 Aug 2021 19:29:00 GMT  
		Size: 320.7 KB (320709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426b510aa21fdb81bb0a2156b0a977a69ea8187f959ceb05869b1450d9359814`  
		Last Modified: Wed, 25 Aug 2021 19:28:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:e8353d4e8df77074d824ddc338a6a8784add4f27abe1cda1b230b6a27533edd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4583; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.4583; amd64

```console
$ docker pull caddy@sha256:bd0551e2eeef6d131272af5e4214599dfc85e2a18d421264005a4f8dc3025a02
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6283675023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96c9f880047fab4000d8bad0dceb15c3e478898181805e15b864f3ae980f11`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:16:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 19:24:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 25 Aug 2021 19:24:21 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 25 Aug 2021 19:25:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 25 Aug 2021 19:25:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 25 Aug 2021 19:25:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 25 Aug 2021 19:25:25 GMT
VOLUME [c:/config]
# Wed, 25 Aug 2021 19:25:26 GMT
VOLUME [c:/data]
# Wed, 25 Aug 2021 19:25:27 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 25 Aug 2021 19:25:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 25 Aug 2021 19:25:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 25 Aug 2021 19:25:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 25 Aug 2021 19:25:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 25 Aug 2021 19:25:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 25 Aug 2021 19:25:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 25 Aug 2021 19:25:35 GMT
EXPOSE 80
# Wed, 25 Aug 2021 19:25:36 GMT
EXPOSE 443
# Wed, 25 Aug 2021 19:25:37 GMT
EXPOSE 2019
# Wed, 25 Aug 2021 19:26:16 GMT
RUN caddy version
# Wed, 25 Aug 2021 19:26:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f888b02e4880b5280aedf776d35ce62a07f97c9f4671b4e167d0fadfbcd663f`  
		Last Modified: Wed, 25 Aug 2021 13:39:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c9dee8014da227cc8c6b8d14f6464fefc307c265b07a34d6e2ccc5de24a92a`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 352.7 KB (352700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d26c5819d131639ab53b8e099ab2ed93c63f759072d3a5ce4b9f69f13b8a66`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb3ea0fdbcaf7cab1dbac86676ab00ca78ebf68e3b5c476c5984201c357976`  
		Last Modified: Wed, 25 Aug 2021 19:29:35 GMT  
		Size: 12.0 MB (12025369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a331953cb55eb8482f8b09c1ccb30b06198b0da91f196aa230d56d4f626c3`  
		Last Modified: Wed, 25 Aug 2021 19:29:32 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c66a58bae64f63c34265474f15131687cba250a5cbeb2166a25d383630b68`  
		Last Modified: Wed, 25 Aug 2021 19:29:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b60346916eaf0cd70873400273d0f0de4f72aa7ee5a5bd6a8cfbe446d62499`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74af1f53b1dc6d2f58a23760f463877d707150f1cae25c0ca6a727c64cd7e9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4467e0d432e5bba7c8e197c057837e438ae63c8748b9765a8d7591c0ea12c0`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c92db8b514f6d653c3d0ba5a7e695e808f5880504124fb94648c10590f7f3c9`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63a5575b8310dcb9cbe40352e7753a4bb8f66f1c3fbea055abda03136638d6`  
		Last Modified: Wed, 25 Aug 2021 19:29:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1415f534f6818ea980cf13f9a08c0efb9d60c9f86760129563e203ba93e399c8`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be354de1af39afc991030861814f135bfde0267a02f004fd4caf9ccc31d0bfd`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a0ebb3c5c8d126c85ccbad571fef0051ac62cfec3fe5885c82110381049ed9`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893f40ed74354bd380ee49a7141c654ea10f5a43f1e050539bde502c7214c9f`  
		Last Modified: Wed, 25 Aug 2021 19:29:27 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffd03947508d81a8a5c939b4a1697e4cf18bc8722cc1650732f8df2c6924941`  
		Last Modified: Wed, 25 Aug 2021 19:29:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c43d724632362e78f09ee6bf53a8359cdd6db65300cb3687f2ad3a59e1a5d`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaec774cf06dd02e7ebdf8d5e9aa9b8d4578a60c7a54ce84421910922396b7`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb3d76a117ff8038563015df19972676ff4aea085431ef698f57799559b334`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341d5f41a06e42738b97ffd6ca2835680879ba4113b882c5cd8accd857c0551`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 305.6 KB (305571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd0dece66bb4a5f39d723d7d27311fa04d1de60c084735f41cb588c7b4d5701`  
		Last Modified: Wed, 25 Aug 2021 19:29:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
