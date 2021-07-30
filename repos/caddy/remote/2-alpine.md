## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:1311edcc88296b87ab8ac84e5384b9d3414623654d884b9ad73f0f7dbea5b668
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
$ docker pull caddy@sha256:975e2acc21fa69679cd59786b1ecd7cf3d8f4ac40b028d61c219fd4e770d14cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13593466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88d5f2ec732bdfe5c5785fb90e7258f29e158c1857de067fb62436a723ec081`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:15 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Tue, 15 Jun 2021 23:15:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Jun 2021 04:25:54 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Jun 2021 04:25:57 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Fri, 25 Jun 2021 04:25:57 GMT
ENV CADDY_VERSION=v2.4.3
# Fri, 25 Jun 2021 04:26:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Jun 2021 04:26:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Jun 2021 04:26:03 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Jun 2021 04:26:03 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Jun 2021 04:26:04 GMT
VOLUME [/config]
# Fri, 25 Jun 2021 04:26:04 GMT
VOLUME [/data]
# Fri, 25 Jun 2021 04:26:05 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Fri, 25 Jun 2021 04:26:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Jun 2021 04:26:05 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Jun 2021 04:26:06 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Jun 2021 04:26:06 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Jun 2021 04:26:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Jun 2021 04:26:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Jun 2021 04:26:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Jun 2021 04:26:08 GMT
EXPOSE 80
# Fri, 25 Jun 2021 04:26:08 GMT
EXPOSE 443
# Fri, 25 Jun 2021 04:26:09 GMT
EXPOSE 2019
# Fri, 25 Jun 2021 04:26:09 GMT
WORKDIR /srv
# Fri, 25 Jun 2021 04:26:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532875903768e2aaa022f0dcc8d36d882e8a7af7edf14e86e6444c2406af868e`  
		Last Modified: Fri, 25 Jun 2021 04:27:35 GMT  
		Size: 299.7 KB (299661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141d604c45916aa77667e44622bc085ab97eec4f8ba487d6f06aed74e53395a4`  
		Last Modified: Fri, 25 Jun 2021 04:27:35 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e46c35d91cdc127af615f56a9074bd03baf63f40550c10ac1e56edf111fd4e`  
		Last Modified: Fri, 25 Jun 2021 04:27:42 GMT  
		Size: 10.9 MB (10863654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7106f92e86cc0f43d86170e3424675fb1543f58df755ce212946b44d5c96c38`  
		Last Modified: Fri, 25 Jun 2021 04:27:35 GMT  
		Size: 154.0 B  
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
$ docker pull caddy@sha256:31130c0111ca19a1dca906ee7b2cc380f8e67ab892979cf56bb190c094f1522f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13173628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd0ea8d539e938e13773b20a1ea1796adb72671700cb9b65b480a669b6e3f8d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Sun, 27 Jun 2021 16:38:07 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sun, 27 Jun 2021 16:38:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sun, 27 Jun 2021 16:38:15 GMT
ENV CADDY_VERSION=v2.4.3
# Sun, 27 Jun 2021 16:38:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sun, 27 Jun 2021 16:38:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sun, 27 Jun 2021 16:38:32 GMT
ENV XDG_CONFIG_HOME=/config
# Sun, 27 Jun 2021 16:38:34 GMT
ENV XDG_DATA_HOME=/data
# Sun, 27 Jun 2021 16:38:36 GMT
VOLUME [/config]
# Sun, 27 Jun 2021 16:38:40 GMT
VOLUME [/data]
# Sun, 27 Jun 2021 16:38:42 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sun, 27 Jun 2021 16:38:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Sun, 27 Jun 2021 16:38:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sun, 27 Jun 2021 16:38:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sun, 27 Jun 2021 16:38:48 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sun, 27 Jun 2021 16:38:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sun, 27 Jun 2021 16:38:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sun, 27 Jun 2021 16:38:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sun, 27 Jun 2021 16:39:01 GMT
EXPOSE 80
# Sun, 27 Jun 2021 16:39:03 GMT
EXPOSE 443
# Sun, 27 Jun 2021 16:39:07 GMT
EXPOSE 2019
# Sun, 27 Jun 2021 16:39:10 GMT
WORKDIR /srv
# Sun, 27 Jun 2021 16:39:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd997e1dce51da7846f8347657708b8750a0eb8c5e786c5fcef5547e42d3e9c`  
		Last Modified: Sun, 27 Jun 2021 16:40:22 GMT  
		Size: 302.5 KB (302543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd65a4be1a04251210dcf5d4925c25d6f9079b4bf699f80e43a2513e46421a5`  
		Last Modified: Sun, 27 Jun 2021 16:40:22 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f2bf16517247de92fb2f9a568c2775d92d15e09db858d1f639199eb8da303`  
		Last Modified: Sun, 27 Jun 2021 16:40:25 GMT  
		Size: 10.1 MB (10051940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca33938766a68ae61be1de59d35bcd5b4bcc18ae96c77ab8baee9b7e319e6b22`  
		Last Modified: Sun, 27 Jun 2021 16:40:22 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:d4226a6c30e268159cbeb15e993d2320d162574b7dae654c2271619b3549bc04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14005935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f8604d50d95bbca3ab5038252554f7698f3fd2db7fbfeea946eae909416ae3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Jun 2021 04:05:27 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 26 Jun 2021 04:05:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Sat, 26 Jun 2021 04:05:30 GMT
ENV CADDY_VERSION=v2.4.3
# Sat, 26 Jun 2021 04:05:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1b39843c198a56ccaf1af19edfe51ff2556d6c9081cbf52bbf8d697777af936b24e872561ca0b35aafa0c84b05c86faa4c2ccf463ffef31bb7140fd09211595c' ;; 		armhf)   binArch='armv6'; checksum='9a1e606bbb6d965ab92b7bcae6a5b58fbffa7f9bec77be3321509e3175e18c8f9db785af40e91bc570f799ea9c44756ff0694439a0b4d30574ea50eee7854693' ;; 		armv7)   binArch='armv7'; checksum='67c1af278bfb79daaf7a2717206b94e09ebfac433c5ce8ef2bad1e1233d626c5b57e822a0c29205b7c62561a06772f116d7dcf072ebea4b3148f0bbaa2f61f6c' ;; 		aarch64) binArch='arm64'; checksum='fa105a900a21f02175a1ab1ff2d0db4f171832183f231d59f265d3f728ac9ec7ff4f2b2a951dccf8f6d7a7057fc69e5670db18bd150ff5bd63df3f72c81cff39' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='71399082625f3059208e590b5d13c700757bcb077063115f26f257ab83b3c51d35eabcf70f0cfb426cb5cb59193ee15301dc2f35b22d2d23f6cf8678c84462a6' ;; 		s390x)   binArch='s390x'; checksum='96c9bcb89fb1083c3a293ccc3568b58fc64cfcfda4983fd244a20be07b1b5e26b54bf155d0e472f035d584f1484bd17073c27a75b72adac7d3a820a616015887' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 26 Jun 2021 04:05:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 26 Jun 2021 04:05:36 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 26 Jun 2021 04:05:36 GMT
ENV XDG_DATA_HOME=/data
# Sat, 26 Jun 2021 04:05:37 GMT
VOLUME [/config]
# Sat, 26 Jun 2021 04:05:37 GMT
VOLUME [/data]
# Sat, 26 Jun 2021 04:05:38 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Sat, 26 Jun 2021 04:05:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 26 Jun 2021 04:05:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 26 Jun 2021 04:05:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 26 Jun 2021 04:05:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 26 Jun 2021 04:05:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 26 Jun 2021 04:05:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 26 Jun 2021 04:05:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 26 Jun 2021 04:05:41 GMT
EXPOSE 80
# Sat, 26 Jun 2021 04:05:41 GMT
EXPOSE 443
# Sat, 26 Jun 2021 04:05:42 GMT
EXPOSE 2019
# Sat, 26 Jun 2021 04:05:43 GMT
WORKDIR /srv
# Sat, 26 Jun 2021 04:05:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ffceb760cf41b73b97483b655680373ee04134e25bd41117589abadd6e8a82`  
		Last Modified: Sat, 26 Jun 2021 04:06:34 GMT  
		Size: 300.8 KB (300839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e000d9bc18af630be9c570949ab0cddf3abec807b8ece78ce1d04846f41d296`  
		Last Modified: Sat, 26 Jun 2021 04:06:34 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6100af0b373c529e22557cf3884882d8e6893ed368d5db1cbd63bf8529c98f6`  
		Last Modified: Sat, 26 Jun 2021 04:06:37 GMT  
		Size: 11.1 MB (11096440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bce8db7df9776b5a33fa86bfa4ee4aa4f5167c8c0f5fd89be151b169616edd8`  
		Last Modified: Sat, 26 Jun 2021 04:06:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
