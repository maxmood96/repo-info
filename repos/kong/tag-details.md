<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.5`](#kong25)
-	[`kong:2.5-ubuntu`](#kong25-ubuntu)
-	[`kong:2.5.2`](#kong252)
-	[`kong:2.5.2-alpine`](#kong252-alpine)
-	[`kong:2.5.2-ubuntu`](#kong252-ubuntu)
-	[`kong:2.6`](#kong26)
-	[`kong:2.6-ubuntu`](#kong26-ubuntu)
-	[`kong:2.6.1`](#kong261)
-	[`kong:2.6.1-alpine`](#kong261-alpine)
-	[`kong:2.6.1-ubuntu`](#kong261-ubuntu)
-	[`kong:2.7`](#kong27)
-	[`kong:2.7-ubuntu`](#kong27-ubuntu)
-	[`kong:2.7.2`](#kong272)
-	[`kong:2.7.2-alpine`](#kong272-alpine)
-	[`kong:2.7.2-ubuntu`](#kong272-ubuntu)
-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.1`](#kong281)
-	[`kong:2.8.1-alpine`](#kong281-alpine)
-	[`kong:2.8.1-ubuntu`](#kong281-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.5`

```console
$ docker pull kong@sha256:8a3cb53bc3c03c7e988da69458109c15cb1e039344115814808a7d09eb16009c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5` - linux; amd64

```console
$ docker pull kong@sha256:2c9bfd99355de6fc349ea16c4ec6cca757e61b5f954cc664d4ca988088962bc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49204524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80db16570107e0d69667a819857577db271ebda4fa8ae814561a65617088f6dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:37:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 03:37:40 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 03:37:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 03:38:07 GMT
ARG KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 03:38:07 GMT
ENV KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 03:38:07 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Wed, 20 Jul 2022 03:38:07 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Wed, 20 Jul 2022 03:38:14 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 03:38:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 03:38:15 GMT
USER kong
# Wed, 20 Jul 2022 03:38:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:38:15 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 03:38:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 03:38:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 03:38:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd4002abb7a91836fd1374060b160933d644168ad5e9bb241fa36026f4fa5fe`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029b50250cdf5a69a8a3803d0a66c94494d656aebab9712e766692653e724aa7`  
		Last Modified: Wed, 20 Jul 2022 03:39:35 GMT  
		Size: 46.4 MB (46388866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4401765b595e27580475e85f3d1fad61371849b91670faa94f52e01e1db91d0`  
		Last Modified: Wed, 20 Jul 2022 03:39:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf0750cdaed9b42a24bcd0e6ccd9c024b893bc2866585fab312f0d49ec21432c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48396488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e349f530f7fe73e5a2bdb65e04bf24a5b5304f4449ee24a2ec15e6d677d631`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:47:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 00:47:10 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 00:47:11 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 00:47:12 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 00:47:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 00:48:18 GMT
ARG KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 00:48:19 GMT
ENV KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 00:48:20 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Wed, 20 Jul 2022 00:48:21 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Wed, 20 Jul 2022 00:48:36 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 00:48:37 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 00:48:37 GMT
USER kong
# Wed, 20 Jul 2022 00:48:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:48:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 00:48:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 00:48:41 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 00:48:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e78dff165fcb648f5ef225b6518f18aa324f88f81876c0c67bc8b0eb08227e4`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3abee9de2db482f38f16e840df20381d19d17cd249add8436f9d3d6a95238`  
		Last Modified: Wed, 20 Jul 2022 00:50:37 GMT  
		Size: 45.7 MB (45678587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610235864b0b5a7f697620446a4105a3e7bc471794576a36f9d1799fdd1b914b`  
		Last Modified: Wed, 20 Jul 2022 00:50:29 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-ubuntu`

```console
$ docker pull kong@sha256:447357d50ad6393cd4b7baa045c1b9ce43294d15cfee531f710e97c31ba4d815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7b779407b10ad5645905dcb962fbcba0e3d8006eac268bae762bd6e101c402b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121305426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf802a8434b5f2f26de4feddb6b6f63bbbf9f8654966734060d49e41cdaac930`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:13 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 14 Jun 2022 23:22:33 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:22:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:22:34 GMT
USER kong
# Tue, 14 Jun 2022 23:22:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:22:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:22:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:22:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:22:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1dfb679acc17d7d224b74832d6650b64e4e2a73df45a29b9712b90ae1444b2`  
		Last Modified: Tue, 14 Jun 2022 23:25:05 GMT  
		Size: 67.6 MB (67649951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de9cf24cfa64449f509d580c84c4c141998711caf4c75b40416710725aff28c`  
		Last Modified: Tue, 14 Jun 2022 23:24:53 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4d78b67ffc52535176510c5f1ba119df523b6122270603661c6e02f2a50dde06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118343120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9913ca4999397f03acef93722d99d461566c64071b34e043bf756b67e16eb6e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:44:17 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:44:18 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:44:19 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 14 Jun 2022 23:44:20 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 14 Jun 2022 23:44:53 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:44:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:44:54 GMT
USER kong
# Tue, 14 Jun 2022 23:44:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:44:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:44:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:44:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:44:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be098501d93df45466127ba9fd7f67f42d591984b2102a7b118c00422cacfcae`  
		Last Modified: Tue, 14 Jun 2022 23:48:03 GMT  
		Size: 66.1 MB (66069066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8d2a3d441f6730eaa0a2f4e65d4b036ae32f8e13e6078011dbd7c273199a27`  
		Last Modified: Tue, 14 Jun 2022 23:47:52 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2`

```console
$ docker pull kong@sha256:8a3cb53bc3c03c7e988da69458109c15cb1e039344115814808a7d09eb16009c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2` - linux; amd64

```console
$ docker pull kong@sha256:2c9bfd99355de6fc349ea16c4ec6cca757e61b5f954cc664d4ca988088962bc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49204524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80db16570107e0d69667a819857577db271ebda4fa8ae814561a65617088f6dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:37:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 03:37:40 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 03:37:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 03:38:07 GMT
ARG KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 03:38:07 GMT
ENV KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 03:38:07 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Wed, 20 Jul 2022 03:38:07 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Wed, 20 Jul 2022 03:38:14 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 03:38:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 03:38:15 GMT
USER kong
# Wed, 20 Jul 2022 03:38:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:38:15 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 03:38:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 03:38:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 03:38:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd4002abb7a91836fd1374060b160933d644168ad5e9bb241fa36026f4fa5fe`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029b50250cdf5a69a8a3803d0a66c94494d656aebab9712e766692653e724aa7`  
		Last Modified: Wed, 20 Jul 2022 03:39:35 GMT  
		Size: 46.4 MB (46388866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4401765b595e27580475e85f3d1fad61371849b91670faa94f52e01e1db91d0`  
		Last Modified: Wed, 20 Jul 2022 03:39:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf0750cdaed9b42a24bcd0e6ccd9c024b893bc2866585fab312f0d49ec21432c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48396488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e349f530f7fe73e5a2bdb65e04bf24a5b5304f4449ee24a2ec15e6d677d631`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:47:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 00:47:10 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 00:47:11 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 00:47:12 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 00:47:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 00:48:18 GMT
ARG KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 00:48:19 GMT
ENV KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 00:48:20 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Wed, 20 Jul 2022 00:48:21 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Wed, 20 Jul 2022 00:48:36 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 00:48:37 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 00:48:37 GMT
USER kong
# Wed, 20 Jul 2022 00:48:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:48:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 00:48:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 00:48:41 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 00:48:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e78dff165fcb648f5ef225b6518f18aa324f88f81876c0c67bc8b0eb08227e4`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3abee9de2db482f38f16e840df20381d19d17cd249add8436f9d3d6a95238`  
		Last Modified: Wed, 20 Jul 2022 00:50:37 GMT  
		Size: 45.7 MB (45678587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610235864b0b5a7f697620446a4105a3e7bc471794576a36f9d1799fdd1b914b`  
		Last Modified: Wed, 20 Jul 2022 00:50:29 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2-alpine`

```console
$ docker pull kong@sha256:8a3cb53bc3c03c7e988da69458109c15cb1e039344115814808a7d09eb16009c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:2c9bfd99355de6fc349ea16c4ec6cca757e61b5f954cc664d4ca988088962bc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49204524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80db16570107e0d69667a819857577db271ebda4fa8ae814561a65617088f6dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:37:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 03:37:40 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 03:37:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 03:38:07 GMT
ARG KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 03:38:07 GMT
ENV KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 03:38:07 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Wed, 20 Jul 2022 03:38:07 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Wed, 20 Jul 2022 03:38:14 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 03:38:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 03:38:15 GMT
USER kong
# Wed, 20 Jul 2022 03:38:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:38:15 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 03:38:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 03:38:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 03:38:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd4002abb7a91836fd1374060b160933d644168ad5e9bb241fa36026f4fa5fe`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029b50250cdf5a69a8a3803d0a66c94494d656aebab9712e766692653e724aa7`  
		Last Modified: Wed, 20 Jul 2022 03:39:35 GMT  
		Size: 46.4 MB (46388866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4401765b595e27580475e85f3d1fad61371849b91670faa94f52e01e1db91d0`  
		Last Modified: Wed, 20 Jul 2022 03:39:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf0750cdaed9b42a24bcd0e6ccd9c024b893bc2866585fab312f0d49ec21432c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48396488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e349f530f7fe73e5a2bdb65e04bf24a5b5304f4449ee24a2ec15e6d677d631`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:47:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 00:47:10 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 00:47:11 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 00:47:12 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 00:47:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 00:48:18 GMT
ARG KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 00:48:19 GMT
ENV KONG_VERSION=2.5.2
# Wed, 20 Jul 2022 00:48:20 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Wed, 20 Jul 2022 00:48:21 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Wed, 20 Jul 2022 00:48:36 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 00:48:37 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 00:48:37 GMT
USER kong
# Wed, 20 Jul 2022 00:48:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:48:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 00:48:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 00:48:41 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 00:48:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e78dff165fcb648f5ef225b6518f18aa324f88f81876c0c67bc8b0eb08227e4`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3abee9de2db482f38f16e840df20381d19d17cd249add8436f9d3d6a95238`  
		Last Modified: Wed, 20 Jul 2022 00:50:37 GMT  
		Size: 45.7 MB (45678587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610235864b0b5a7f697620446a4105a3e7bc471794576a36f9d1799fdd1b914b`  
		Last Modified: Wed, 20 Jul 2022 00:50:29 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2-ubuntu`

```console
$ docker pull kong@sha256:447357d50ad6393cd4b7baa045c1b9ce43294d15cfee531f710e97c31ba4d815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7b779407b10ad5645905dcb962fbcba0e3d8006eac268bae762bd6e101c402b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121305426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf802a8434b5f2f26de4feddb6b6f63bbbf9f8654966734060d49e41cdaac930`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:13 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 14 Jun 2022 23:22:33 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:22:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:22:34 GMT
USER kong
# Tue, 14 Jun 2022 23:22:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:22:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:22:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:22:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:22:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1dfb679acc17d7d224b74832d6650b64e4e2a73df45a29b9712b90ae1444b2`  
		Last Modified: Tue, 14 Jun 2022 23:25:05 GMT  
		Size: 67.6 MB (67649951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de9cf24cfa64449f509d580c84c4c141998711caf4c75b40416710725aff28c`  
		Last Modified: Tue, 14 Jun 2022 23:24:53 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4d78b67ffc52535176510c5f1ba119df523b6122270603661c6e02f2a50dde06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118343120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9913ca4999397f03acef93722d99d461566c64071b34e043bf756b67e16eb6e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:44:17 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:44:18 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:44:19 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 14 Jun 2022 23:44:20 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 14 Jun 2022 23:44:53 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:44:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:44:54 GMT
USER kong
# Tue, 14 Jun 2022 23:44:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:44:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:44:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:44:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:44:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be098501d93df45466127ba9fd7f67f42d591984b2102a7b118c00422cacfcae`  
		Last Modified: Tue, 14 Jun 2022 23:48:03 GMT  
		Size: 66.1 MB (66069066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8d2a3d441f6730eaa0a2f4e65d4b036ae32f8e13e6078011dbd7c273199a27`  
		Last Modified: Tue, 14 Jun 2022 23:47:52 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6`

```console
$ docker pull kong@sha256:532bd8a7ed4b47b5c37c36fc47cb233760be98218723cf2b1085b97ba92639da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6` - linux; amd64

```console
$ docker pull kong@sha256:f4e231a4cb1d0fde660ce1af53170350f568caf6813573f83a859348c223035e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50220155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036add2cbc3e1e96f65d27e7c93e2815c06b38abab019c64ccc087027d4c59e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:37:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 03:37:40 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 03:37:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 03:37:54 GMT
ARG KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 03:37:54 GMT
ENV KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 03:37:54 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Wed, 20 Jul 2022 03:37:54 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Wed, 20 Jul 2022 03:38:01 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 03:38:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 03:38:01 GMT
USER kong
# Wed, 20 Jul 2022 03:38:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:38:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 03:38:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 03:38:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 03:38:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd4002abb7a91836fd1374060b160933d644168ad5e9bb241fa36026f4fa5fe`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127d00474957afb6ae77ce5d752a46474ecea41329b4abe290c219c6752daa1a`  
		Last Modified: Wed, 20 Jul 2022 03:39:15 GMT  
		Size: 47.4 MB (47404496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7296067d4228b674122479f21b2a833a98d59c54c90647effa719de4dee94a14`  
		Last Modified: Wed, 20 Jul 2022 03:39:07 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:980c314f6436184a28db716fd2958ca105fc60b91e3ccdad202ebfa9ebe383de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49635860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bdadc7cf9acd0f549b75861af9274849e83d5ed97279fa9d65329bab9457af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:47:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 00:47:10 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 00:47:11 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 00:47:12 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 00:47:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 00:47:50 GMT
ARG KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 00:47:51 GMT
ENV KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 00:47:52 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Wed, 20 Jul 2022 00:47:53 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Wed, 20 Jul 2022 00:48:02 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 00:48:03 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 00:48:03 GMT
USER kong
# Wed, 20 Jul 2022 00:48:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:48:05 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 00:48:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 00:48:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 00:48:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e78dff165fcb648f5ef225b6518f18aa324f88f81876c0c67bc8b0eb08227e4`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ee357c14479a2ddaa3bb8de0adb2577b22ddf75f505b732969675d99e0323`  
		Last Modified: Wed, 20 Jul 2022 00:50:13 GMT  
		Size: 46.9 MB (46917959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7115610935b2ce1e7a974313d7672d8258f2660491b95647392d93ef5a2aac`  
		Last Modified: Wed, 20 Jul 2022 00:50:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-ubuntu`

```console
$ docker pull kong@sha256:3eb2f5af81b5573f6bd260eee2c4dab0323bf784233a1d34bda6aa140b647eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:6c732184cbecaf07004a58f98a9caa08eafa9a69bd39a9adfdbcf3e4e489ff08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128178153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c45108fd2c98886ff41659d5b9f9fdf029902a28ec6d17ed46182e387f474e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:27:51 GMT
ARG KONG_VERSION=2.6.1
# Tue, 07 Jun 2022 00:27:51 GMT
ENV KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:21:31 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 14 Jun 2022 23:21:31 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 14 Jun 2022 23:21:52 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:21:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:21:53 GMT
USER kong
# Tue, 14 Jun 2022 23:21:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:21:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:21:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:21:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:21:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a6ad0ac64b328847492648b99c0589ac8f8e6b5b6be0bac479fed0b97074c`  
		Last Modified: Tue, 14 Jun 2022 23:24:24 GMT  
		Size: 74.5 MB (74522678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acebe9b9e2a441ecdfeb94361c4990beb6565b5de4f647440284b1238eb5cab`  
		Last Modified: Tue, 14 Jun 2022 23:24:12 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9edbb82a5cab25824f6a9a5b5fa74099b44dac3ec28a916e8ae1f1007b08f48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125230801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b89305f90c32f975ddc48dc705ba3866dd39e5418bf61a7414eba6061c9ada4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:43:01 GMT
ARG KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:43:02 GMT
ENV KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:43:03 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 14 Jun 2022 23:43:04 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 14 Jun 2022 23:43:32 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:43:33 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:43:33 GMT
USER kong
# Tue, 14 Jun 2022 23:43:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:43:35 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:43:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:43:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:43:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051bb9dc9743d6e00ab1a027ec2e3207ac5a7456b5d4116cd1ea944ee768fe3`  
		Last Modified: Tue, 14 Jun 2022 23:47:20 GMT  
		Size: 73.0 MB (72956746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dd3c509211b3538841a5134650c43551da0e3d7817006fca2cb5ae9b9b5185`  
		Last Modified: Tue, 14 Jun 2022 23:47:08 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1`

```console
$ docker pull kong@sha256:532bd8a7ed4b47b5c37c36fc47cb233760be98218723cf2b1085b97ba92639da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1` - linux; amd64

```console
$ docker pull kong@sha256:f4e231a4cb1d0fde660ce1af53170350f568caf6813573f83a859348c223035e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50220155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036add2cbc3e1e96f65d27e7c93e2815c06b38abab019c64ccc087027d4c59e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:37:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 03:37:40 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 03:37:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 03:37:54 GMT
ARG KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 03:37:54 GMT
ENV KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 03:37:54 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Wed, 20 Jul 2022 03:37:54 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Wed, 20 Jul 2022 03:38:01 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 03:38:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 03:38:01 GMT
USER kong
# Wed, 20 Jul 2022 03:38:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:38:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 03:38:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 03:38:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 03:38:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd4002abb7a91836fd1374060b160933d644168ad5e9bb241fa36026f4fa5fe`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127d00474957afb6ae77ce5d752a46474ecea41329b4abe290c219c6752daa1a`  
		Last Modified: Wed, 20 Jul 2022 03:39:15 GMT  
		Size: 47.4 MB (47404496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7296067d4228b674122479f21b2a833a98d59c54c90647effa719de4dee94a14`  
		Last Modified: Wed, 20 Jul 2022 03:39:07 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:980c314f6436184a28db716fd2958ca105fc60b91e3ccdad202ebfa9ebe383de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49635860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bdadc7cf9acd0f549b75861af9274849e83d5ed97279fa9d65329bab9457af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:47:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 00:47:10 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 00:47:11 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 00:47:12 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 00:47:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 00:47:50 GMT
ARG KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 00:47:51 GMT
ENV KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 00:47:52 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Wed, 20 Jul 2022 00:47:53 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Wed, 20 Jul 2022 00:48:02 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 00:48:03 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 00:48:03 GMT
USER kong
# Wed, 20 Jul 2022 00:48:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:48:05 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 00:48:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 00:48:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 00:48:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e78dff165fcb648f5ef225b6518f18aa324f88f81876c0c67bc8b0eb08227e4`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ee357c14479a2ddaa3bb8de0adb2577b22ddf75f505b732969675d99e0323`  
		Last Modified: Wed, 20 Jul 2022 00:50:13 GMT  
		Size: 46.9 MB (46917959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7115610935b2ce1e7a974313d7672d8258f2660491b95647392d93ef5a2aac`  
		Last Modified: Wed, 20 Jul 2022 00:50:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-alpine`

```console
$ docker pull kong@sha256:532bd8a7ed4b47b5c37c36fc47cb233760be98218723cf2b1085b97ba92639da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:f4e231a4cb1d0fde660ce1af53170350f568caf6813573f83a859348c223035e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50220155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036add2cbc3e1e96f65d27e7c93e2815c06b38abab019c64ccc087027d4c59e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:37:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 03:37:40 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 03:37:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 03:37:54 GMT
ARG KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 03:37:54 GMT
ENV KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 03:37:54 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Wed, 20 Jul 2022 03:37:54 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Wed, 20 Jul 2022 03:38:01 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 03:38:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 03:38:01 GMT
USER kong
# Wed, 20 Jul 2022 03:38:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:38:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 03:38:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 03:38:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 03:38:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd4002abb7a91836fd1374060b160933d644168ad5e9bb241fa36026f4fa5fe`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127d00474957afb6ae77ce5d752a46474ecea41329b4abe290c219c6752daa1a`  
		Last Modified: Wed, 20 Jul 2022 03:39:15 GMT  
		Size: 47.4 MB (47404496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7296067d4228b674122479f21b2a833a98d59c54c90647effa719de4dee94a14`  
		Last Modified: Wed, 20 Jul 2022 03:39:07 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:980c314f6436184a28db716fd2958ca105fc60b91e3ccdad202ebfa9ebe383de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49635860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bdadc7cf9acd0f549b75861af9274849e83d5ed97279fa9d65329bab9457af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:47:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 00:47:10 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 00:47:11 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 00:47:12 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 00:47:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 00:47:50 GMT
ARG KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 00:47:51 GMT
ENV KONG_VERSION=2.6.1
# Wed, 20 Jul 2022 00:47:52 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Wed, 20 Jul 2022 00:47:53 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Wed, 20 Jul 2022 00:48:02 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 00:48:03 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 00:48:03 GMT
USER kong
# Wed, 20 Jul 2022 00:48:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:48:05 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 00:48:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 00:48:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 00:48:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e78dff165fcb648f5ef225b6518f18aa324f88f81876c0c67bc8b0eb08227e4`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ee357c14479a2ddaa3bb8de0adb2577b22ddf75f505b732969675d99e0323`  
		Last Modified: Wed, 20 Jul 2022 00:50:13 GMT  
		Size: 46.9 MB (46917959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7115610935b2ce1e7a974313d7672d8258f2660491b95647392d93ef5a2aac`  
		Last Modified: Wed, 20 Jul 2022 00:50:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-ubuntu`

```console
$ docker pull kong@sha256:3eb2f5af81b5573f6bd260eee2c4dab0323bf784233a1d34bda6aa140b647eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:6c732184cbecaf07004a58f98a9caa08eafa9a69bd39a9adfdbcf3e4e489ff08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128178153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c45108fd2c98886ff41659d5b9f9fdf029902a28ec6d17ed46182e387f474e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:27:51 GMT
ARG KONG_VERSION=2.6.1
# Tue, 07 Jun 2022 00:27:51 GMT
ENV KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:21:31 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 14 Jun 2022 23:21:31 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 14 Jun 2022 23:21:52 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:21:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:21:53 GMT
USER kong
# Tue, 14 Jun 2022 23:21:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:21:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:21:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:21:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:21:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a6ad0ac64b328847492648b99c0589ac8f8e6b5b6be0bac479fed0b97074c`  
		Last Modified: Tue, 14 Jun 2022 23:24:24 GMT  
		Size: 74.5 MB (74522678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acebe9b9e2a441ecdfeb94361c4990beb6565b5de4f647440284b1238eb5cab`  
		Last Modified: Tue, 14 Jun 2022 23:24:12 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9edbb82a5cab25824f6a9a5b5fa74099b44dac3ec28a916e8ae1f1007b08f48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125230801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b89305f90c32f975ddc48dc705ba3866dd39e5418bf61a7414eba6061c9ada4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:43:01 GMT
ARG KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:43:02 GMT
ENV KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:43:03 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 14 Jun 2022 23:43:04 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 14 Jun 2022 23:43:32 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:43:33 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:43:33 GMT
USER kong
# Tue, 14 Jun 2022 23:43:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:43:35 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:43:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:43:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:43:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051bb9dc9743d6e00ab1a027ec2e3207ac5a7456b5d4116cd1ea944ee768fe3`  
		Last Modified: Tue, 14 Jun 2022 23:47:20 GMT  
		Size: 73.0 MB (72956746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dd3c509211b3538841a5134650c43551da0e3d7817006fca2cb5ae9b9b5185`  
		Last Modified: Tue, 14 Jun 2022 23:47:08 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7`

```console
$ docker pull kong@sha256:f6350844d4bf9d3a57a9efc6b80337b528447813286023bbe4350cc82e855530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7` - linux; amd64

```console
$ docker pull kong@sha256:879c18ec2aecea5f766e389fc6fb777fd40b41a95190bf7d6b57208892ebc280
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50140032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5603d5e5040ade333191225532aa20e116bb071245076761193f2d37baccfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:37:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 03:37:40 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 03:37:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 03:37:41 GMT
ARG KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 03:37:41 GMT
ENV KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 03:37:41 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Wed, 20 Jul 2022 03:37:41 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Wed, 20 Jul 2022 03:37:48 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 03:37:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 03:37:49 GMT
USER kong
# Wed, 20 Jul 2022 03:37:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:37:49 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 03:37:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 03:37:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 03:37:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd4002abb7a91836fd1374060b160933d644168ad5e9bb241fa36026f4fa5fe`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af9da6b6f25dd4e4a8698f1b06d1f835f99e081d65a885b5e93f05e8295edd`  
		Last Modified: Wed, 20 Jul 2022 03:38:55 GMT  
		Size: 47.3 MB (47324373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b1a0670c69cc48760c15ab66b985dad2a9ec6d84cfbe009da82fb8f69731dd`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6657a9ee4723f782d1ffeacb6c2f16d5a737262f4c209381baf21b9ebcece6cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49543551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285b20d47b8b7ff5902ac1322e566f51975dd749e96e64fb3cd634c399c359d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:47:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 00:47:10 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 00:47:11 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 00:47:12 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 00:47:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 00:47:14 GMT
ARG KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 00:47:15 GMT
ENV KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 00:47:16 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Wed, 20 Jul 2022 00:47:17 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Wed, 20 Jul 2022 00:47:33 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 00:47:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 00:47:34 GMT
USER kong
# Wed, 20 Jul 2022 00:47:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:47:36 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 00:47:37 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 00:47:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 00:47:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e78dff165fcb648f5ef225b6518f18aa324f88f81876c0c67bc8b0eb08227e4`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3797f9e31013aed880563ed36cbd67ff2d2a48064b2c782c1a19f2fc893bcf`  
		Last Modified: Wed, 20 Jul 2022 00:49:49 GMT  
		Size: 46.8 MB (46825649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c353c62de2bf51e73f8665d6ae8454aa7086cdea2dee82fdf95300dd63ceaa`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7-ubuntu`

```console
$ docker pull kong@sha256:9547499e0db869d571fb76c9e65186a2209bdc2f4022a19d97ac129b9f5cef52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d50ccbfbbf0058ab4e4dbc26727ee1f051fd850a73c0389ccd89d85d055bde13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128089282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b25366321406d551fe15b9c128d8d93ae121d70743a0ca0c9bea69db7b63ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:26:55 GMT
ARG KONG_VERSION=2.7.2
# Tue, 07 Jun 2022 00:26:55 GMT
ENV KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:21:01 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 14 Jun 2022 23:21:01 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 14 Jun 2022 23:21:23 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:21:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:21:24 GMT
USER kong
# Tue, 14 Jun 2022 23:21:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:21:24 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:21:24 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:21:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:21:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f40ef21bcbfbfddd22aaa8c284036f53c749c2ce6aaaf483b2984b15140ee08`  
		Last Modified: Tue, 14 Jun 2022 23:24:01 GMT  
		Size: 74.4 MB (74433808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13147babdcbaf37d0add6eed3e252f5726db6a53fb32a7544f92ae934097ef1f`  
		Last Modified: Tue, 14 Jun 2022 23:23:49 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:288e255e36500d19d5e2c8638533629382eb9246b298ebfb8d57bec058d167bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125134863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08324449eb0cd5ffa32fbb4d8036a3fba00eeabf8da9699c2307bc667975278`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:41:54 GMT
ARG KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:41:55 GMT
ENV KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:41:56 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 14 Jun 2022 23:41:57 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 14 Jun 2022 23:42:37 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:42:39 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:42:39 GMT
USER kong
# Tue, 14 Jun 2022 23:42:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:42:41 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:42:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:42:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:42:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e210ba2a0418dcc22653325535fe628a771663eb3d502d910071f83bba73914d`  
		Last Modified: Tue, 14 Jun 2022 23:46:56 GMT  
		Size: 72.9 MB (72860810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db5446eb906fe4ad4cc3845b976b3f163473fb069894b88e61b3417c1f624e3`  
		Last Modified: Tue, 14 Jun 2022 23:46:44 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2`

```console
$ docker pull kong@sha256:f6350844d4bf9d3a57a9efc6b80337b528447813286023bbe4350cc82e855530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2` - linux; amd64

```console
$ docker pull kong@sha256:879c18ec2aecea5f766e389fc6fb777fd40b41a95190bf7d6b57208892ebc280
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50140032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5603d5e5040ade333191225532aa20e116bb071245076761193f2d37baccfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:37:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 03:37:40 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 03:37:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 03:37:41 GMT
ARG KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 03:37:41 GMT
ENV KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 03:37:41 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Wed, 20 Jul 2022 03:37:41 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Wed, 20 Jul 2022 03:37:48 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 03:37:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 03:37:49 GMT
USER kong
# Wed, 20 Jul 2022 03:37:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:37:49 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 03:37:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 03:37:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 03:37:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd4002abb7a91836fd1374060b160933d644168ad5e9bb241fa36026f4fa5fe`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af9da6b6f25dd4e4a8698f1b06d1f835f99e081d65a885b5e93f05e8295edd`  
		Last Modified: Wed, 20 Jul 2022 03:38:55 GMT  
		Size: 47.3 MB (47324373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b1a0670c69cc48760c15ab66b985dad2a9ec6d84cfbe009da82fb8f69731dd`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6657a9ee4723f782d1ffeacb6c2f16d5a737262f4c209381baf21b9ebcece6cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49543551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285b20d47b8b7ff5902ac1322e566f51975dd749e96e64fb3cd634c399c359d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:47:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 00:47:10 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 00:47:11 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 00:47:12 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 00:47:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 00:47:14 GMT
ARG KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 00:47:15 GMT
ENV KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 00:47:16 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Wed, 20 Jul 2022 00:47:17 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Wed, 20 Jul 2022 00:47:33 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 00:47:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 00:47:34 GMT
USER kong
# Wed, 20 Jul 2022 00:47:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:47:36 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 00:47:37 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 00:47:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 00:47:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e78dff165fcb648f5ef225b6518f18aa324f88f81876c0c67bc8b0eb08227e4`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3797f9e31013aed880563ed36cbd67ff2d2a48064b2c782c1a19f2fc893bcf`  
		Last Modified: Wed, 20 Jul 2022 00:49:49 GMT  
		Size: 46.8 MB (46825649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c353c62de2bf51e73f8665d6ae8454aa7086cdea2dee82fdf95300dd63ceaa`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-alpine`

```console
$ docker pull kong@sha256:f6350844d4bf9d3a57a9efc6b80337b528447813286023bbe4350cc82e855530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:879c18ec2aecea5f766e389fc6fb777fd40b41a95190bf7d6b57208892ebc280
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50140032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5603d5e5040ade333191225532aa20e116bb071245076761193f2d37baccfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:37:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 03:37:40 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 03:37:40 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 03:37:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 03:37:41 GMT
ARG KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 03:37:41 GMT
ENV KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 03:37:41 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Wed, 20 Jul 2022 03:37:41 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Wed, 20 Jul 2022 03:37:48 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 03:37:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 03:37:49 GMT
USER kong
# Wed, 20 Jul 2022 03:37:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:37:49 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 03:37:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 03:37:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 03:37:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd4002abb7a91836fd1374060b160933d644168ad5e9bb241fa36026f4fa5fe`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af9da6b6f25dd4e4a8698f1b06d1f835f99e081d65a885b5e93f05e8295edd`  
		Last Modified: Wed, 20 Jul 2022 03:38:55 GMT  
		Size: 47.3 MB (47324373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b1a0670c69cc48760c15ab66b985dad2a9ec6d84cfbe009da82fb8f69731dd`  
		Last Modified: Wed, 20 Jul 2022 03:38:47 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6657a9ee4723f782d1ffeacb6c2f16d5a737262f4c209381baf21b9ebcece6cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49543551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285b20d47b8b7ff5902ac1322e566f51975dd749e96e64fb3cd634c399c359d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:47:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 20 Jul 2022 00:47:10 GMT
ARG ASSET=ce
# Wed, 20 Jul 2022 00:47:11 GMT
ENV ASSET=ce
# Wed, 20 Jul 2022 00:47:12 GMT
ARG EE_PORTS
# Wed, 20 Jul 2022 00:47:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 20 Jul 2022 00:47:14 GMT
ARG KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 00:47:15 GMT
ENV KONG_VERSION=2.7.2
# Wed, 20 Jul 2022 00:47:16 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Wed, 20 Jul 2022 00:47:17 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Wed, 20 Jul 2022 00:47:33 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 20 Jul 2022 00:47:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 20 Jul 2022 00:47:34 GMT
USER kong
# Wed, 20 Jul 2022 00:47:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:47:36 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 20 Jul 2022 00:47:37 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Jul 2022 00:47:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 20 Jul 2022 00:47:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e78dff165fcb648f5ef225b6518f18aa324f88f81876c0c67bc8b0eb08227e4`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3797f9e31013aed880563ed36cbd67ff2d2a48064b2c782c1a19f2fc893bcf`  
		Last Modified: Wed, 20 Jul 2022 00:49:49 GMT  
		Size: 46.8 MB (46825649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c353c62de2bf51e73f8665d6ae8454aa7086cdea2dee82fdf95300dd63ceaa`  
		Last Modified: Wed, 20 Jul 2022 00:49:41 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-ubuntu`

```console
$ docker pull kong@sha256:9547499e0db869d571fb76c9e65186a2209bdc2f4022a19d97ac129b9f5cef52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d50ccbfbbf0058ab4e4dbc26727ee1f051fd850a73c0389ccd89d85d055bde13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128089282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b25366321406d551fe15b9c128d8d93ae121d70743a0ca0c9bea69db7b63ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:26:55 GMT
ARG KONG_VERSION=2.7.2
# Tue, 07 Jun 2022 00:26:55 GMT
ENV KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:21:01 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 14 Jun 2022 23:21:01 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 14 Jun 2022 23:21:23 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:21:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:21:24 GMT
USER kong
# Tue, 14 Jun 2022 23:21:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:21:24 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:21:24 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:21:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:21:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f40ef21bcbfbfddd22aaa8c284036f53c749c2ce6aaaf483b2984b15140ee08`  
		Last Modified: Tue, 14 Jun 2022 23:24:01 GMT  
		Size: 74.4 MB (74433808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13147babdcbaf37d0add6eed3e252f5726db6a53fb32a7544f92ae934097ef1f`  
		Last Modified: Tue, 14 Jun 2022 23:23:49 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:288e255e36500d19d5e2c8638533629382eb9246b298ebfb8d57bec058d167bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125134863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08324449eb0cd5ffa32fbb4d8036a3fba00eeabf8da9699c2307bc667975278`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:41:54 GMT
ARG KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:41:55 GMT
ENV KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:41:56 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 14 Jun 2022 23:41:57 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 14 Jun 2022 23:42:37 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:42:39 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:42:39 GMT
USER kong
# Tue, 14 Jun 2022 23:42:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:42:41 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:42:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:42:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:42:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e210ba2a0418dcc22653325535fe628a771663eb3d502d910071f83bba73914d`  
		Last Modified: Tue, 14 Jun 2022 23:46:56 GMT  
		Size: 72.9 MB (72860810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db5446eb906fe4ad4cc3845b976b3f163473fb069894b88e61b3417c1f624e3`  
		Last Modified: Tue, 14 Jun 2022 23:46:44 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8`

```console
$ docker pull kong@sha256:7da24d355f2396c38cff56625b6ae5134dc28efca75c8d43562384a30c9f4925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:76e2511d4844e42a1118c561be6c2f797de4319d3359ba141bee3dd307c9846f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49326697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac914d61e19c72a49fd1d32d6e2a58367034c48af55fe776c1ae56ab2271228b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:24:37 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 19 Jul 2022 00:24:37 GMT
ARG ASSET=ce
# Tue, 19 Jul 2022 00:24:37 GMT
ENV ASSET=ce
# Tue, 19 Jul 2022 00:24:37 GMT
ARG EE_PORTS
# Tue, 19 Jul 2022 00:24:37 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_VERSION=2.8.1
# Tue, 19 Jul 2022 00:24:37 GMT
ENV KONG_VERSION=2.8.1
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 19 Jul 2022 00:24:45 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 19 Jul 2022 00:24:46 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 19 Jul 2022 00:24:46 GMT
USER kong
# Tue, 19 Jul 2022 00:24:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Jul 2022 00:24:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 19 Jul 2022 00:24:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Jul 2022 00:24:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 19 Jul 2022 00:24:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a452a510cfd6ecd10d271f128ecb0eff4928164bd7aa989464a7ab8bd4a9f370`  
		Last Modified: Tue, 19 Jul 2022 00:25:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01021de023377a2ff9c3c5ac1e6e059ac3bd004e123c9f09c514fc618b344582`  
		Last Modified: Tue, 19 Jul 2022 00:25:33 GMT  
		Size: 46.5 MB (46526880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd69f5117b2d5591e8da6d2d6c8517b4dd714db165c0ba782885d36ac03b4fb`  
		Last Modified: Tue, 19 Jul 2022 00:25:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:165a85a4bce35a4d1966589fb9721567019aa25ec97828d57f59e630d035c737
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48507749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a03239cfc5173edd64ec1584d4976624a6d27e3155f3bc28303cfb844797fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:38:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Mon, 18 Jul 2022 23:38:09 GMT
ARG ASSET=ce
# Mon, 18 Jul 2022 23:38:10 GMT
ENV ASSET=ce
# Mon, 18 Jul 2022 23:38:11 GMT
ARG EE_PORTS
# Mon, 18 Jul 2022 23:38:13 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Mon, 18 Jul 2022 23:38:13 GMT
ARG KONG_VERSION=2.8.1
# Mon, 18 Jul 2022 23:38:14 GMT
ENV KONG_VERSION=2.8.1
# Mon, 18 Jul 2022 23:38:15 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Mon, 18 Jul 2022 23:38:16 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Mon, 18 Jul 2022 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Mon, 18 Jul 2022 23:38:25 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Mon, 18 Jul 2022 23:38:25 GMT
USER kong
# Mon, 18 Jul 2022 23:38:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Jul 2022 23:38:27 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 18 Jul 2022 23:38:28 GMT
STOPSIGNAL SIGQUIT
# Mon, 18 Jul 2022 23:38:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Mon, 18 Jul 2022 23:38:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1302724bde7bafd2ba09b81d64c1fea90938cc5dd1cf54dd731be936c347aaa`  
		Last Modified: Mon, 18 Jul 2022 23:39:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51072c79d716ea1d1997805681b49c9df516af94b307573653daad345405b107`  
		Last Modified: Mon, 18 Jul 2022 23:39:59 GMT  
		Size: 45.8 MB (45812015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b5ae76cfb4f221d5b49ef4f884ffde2058c0bf17bc53678aa6fe68552ba54d`  
		Last Modified: Mon, 18 Jul 2022 23:39:51 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:27ba987186ac8913235d0bea44433e295511b776e37cc24cad69be56659b44c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5d2559d9967e39a7c0285643a484dc59a434a3dcc73b66183b4d9811ba81bb95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121229036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9348939116e58d77efb379d00687a58a85516ea07a901e5ce6f610ae2ce4ce68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:20:55 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:20:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:55 GMT
USER kong
# Tue, 14 Jun 2022 23:20:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4724d8b04ccf412df4c2eab1db30e216e64b5c7753529b193353c2ba6c8a0b0`  
		Last Modified: Tue, 14 Jun 2022 23:23:36 GMT  
		Size: 67.6 MB (67573561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28de5e8494dca4441e0ee102c3ef5807cd89429f162901e8e26c43625fab30f8`  
		Last Modified: Tue, 14 Jun 2022 23:23:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d35bf65fd2f20eac2327eedb0ad547d92ff8dc60ef0fbd382a72b2e90ee872ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121726118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26405f0174d52a4756cb1ca6e56ab10d1323b68a9697f02b56213d57c47e5f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:40:46 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:47 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:48 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:40:49 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:41:31 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:41:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:41:32 GMT
USER kong
# Tue, 14 Jun 2022 23:41:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:41:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:41:35 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:41:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:41:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66957df71376f98a0e8eb085ef05d9bd8e0647ee35f7576de662cfeed4227cdd`  
		Last Modified: Tue, 14 Jun 2022 23:46:28 GMT  
		Size: 69.5 MB (69452065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b313f50a105849eb0f70997fd0b89b8499f1d2ad74d56b0d467902d67f1bd1`  
		Last Modified: Tue, 14 Jun 2022 23:46:16 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1`

```console
$ docker pull kong@sha256:7da24d355f2396c38cff56625b6ae5134dc28efca75c8d43562384a30c9f4925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1` - linux; amd64

```console
$ docker pull kong@sha256:76e2511d4844e42a1118c561be6c2f797de4319d3359ba141bee3dd307c9846f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49326697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac914d61e19c72a49fd1d32d6e2a58367034c48af55fe776c1ae56ab2271228b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:24:37 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 19 Jul 2022 00:24:37 GMT
ARG ASSET=ce
# Tue, 19 Jul 2022 00:24:37 GMT
ENV ASSET=ce
# Tue, 19 Jul 2022 00:24:37 GMT
ARG EE_PORTS
# Tue, 19 Jul 2022 00:24:37 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_VERSION=2.8.1
# Tue, 19 Jul 2022 00:24:37 GMT
ENV KONG_VERSION=2.8.1
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 19 Jul 2022 00:24:45 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 19 Jul 2022 00:24:46 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 19 Jul 2022 00:24:46 GMT
USER kong
# Tue, 19 Jul 2022 00:24:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Jul 2022 00:24:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 19 Jul 2022 00:24:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Jul 2022 00:24:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 19 Jul 2022 00:24:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a452a510cfd6ecd10d271f128ecb0eff4928164bd7aa989464a7ab8bd4a9f370`  
		Last Modified: Tue, 19 Jul 2022 00:25:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01021de023377a2ff9c3c5ac1e6e059ac3bd004e123c9f09c514fc618b344582`  
		Last Modified: Tue, 19 Jul 2022 00:25:33 GMT  
		Size: 46.5 MB (46526880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd69f5117b2d5591e8da6d2d6c8517b4dd714db165c0ba782885d36ac03b4fb`  
		Last Modified: Tue, 19 Jul 2022 00:25:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:165a85a4bce35a4d1966589fb9721567019aa25ec97828d57f59e630d035c737
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48507749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a03239cfc5173edd64ec1584d4976624a6d27e3155f3bc28303cfb844797fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:38:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Mon, 18 Jul 2022 23:38:09 GMT
ARG ASSET=ce
# Mon, 18 Jul 2022 23:38:10 GMT
ENV ASSET=ce
# Mon, 18 Jul 2022 23:38:11 GMT
ARG EE_PORTS
# Mon, 18 Jul 2022 23:38:13 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Mon, 18 Jul 2022 23:38:13 GMT
ARG KONG_VERSION=2.8.1
# Mon, 18 Jul 2022 23:38:14 GMT
ENV KONG_VERSION=2.8.1
# Mon, 18 Jul 2022 23:38:15 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Mon, 18 Jul 2022 23:38:16 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Mon, 18 Jul 2022 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Mon, 18 Jul 2022 23:38:25 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Mon, 18 Jul 2022 23:38:25 GMT
USER kong
# Mon, 18 Jul 2022 23:38:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Jul 2022 23:38:27 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 18 Jul 2022 23:38:28 GMT
STOPSIGNAL SIGQUIT
# Mon, 18 Jul 2022 23:38:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Mon, 18 Jul 2022 23:38:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1302724bde7bafd2ba09b81d64c1fea90938cc5dd1cf54dd731be936c347aaa`  
		Last Modified: Mon, 18 Jul 2022 23:39:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51072c79d716ea1d1997805681b49c9df516af94b307573653daad345405b107`  
		Last Modified: Mon, 18 Jul 2022 23:39:59 GMT  
		Size: 45.8 MB (45812015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b5ae76cfb4f221d5b49ef4f884ffde2058c0bf17bc53678aa6fe68552ba54d`  
		Last Modified: Mon, 18 Jul 2022 23:39:51 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1-alpine`

```console
$ docker pull kong@sha256:7da24d355f2396c38cff56625b6ae5134dc28efca75c8d43562384a30c9f4925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:76e2511d4844e42a1118c561be6c2f797de4319d3359ba141bee3dd307c9846f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49326697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac914d61e19c72a49fd1d32d6e2a58367034c48af55fe776c1ae56ab2271228b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:24:37 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 19 Jul 2022 00:24:37 GMT
ARG ASSET=ce
# Tue, 19 Jul 2022 00:24:37 GMT
ENV ASSET=ce
# Tue, 19 Jul 2022 00:24:37 GMT
ARG EE_PORTS
# Tue, 19 Jul 2022 00:24:37 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_VERSION=2.8.1
# Tue, 19 Jul 2022 00:24:37 GMT
ENV KONG_VERSION=2.8.1
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 19 Jul 2022 00:24:45 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 19 Jul 2022 00:24:46 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 19 Jul 2022 00:24:46 GMT
USER kong
# Tue, 19 Jul 2022 00:24:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Jul 2022 00:24:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 19 Jul 2022 00:24:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Jul 2022 00:24:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 19 Jul 2022 00:24:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a452a510cfd6ecd10d271f128ecb0eff4928164bd7aa989464a7ab8bd4a9f370`  
		Last Modified: Tue, 19 Jul 2022 00:25:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01021de023377a2ff9c3c5ac1e6e059ac3bd004e123c9f09c514fc618b344582`  
		Last Modified: Tue, 19 Jul 2022 00:25:33 GMT  
		Size: 46.5 MB (46526880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd69f5117b2d5591e8da6d2d6c8517b4dd714db165c0ba782885d36ac03b4fb`  
		Last Modified: Tue, 19 Jul 2022 00:25:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:165a85a4bce35a4d1966589fb9721567019aa25ec97828d57f59e630d035c737
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48507749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a03239cfc5173edd64ec1584d4976624a6d27e3155f3bc28303cfb844797fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:38:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Mon, 18 Jul 2022 23:38:09 GMT
ARG ASSET=ce
# Mon, 18 Jul 2022 23:38:10 GMT
ENV ASSET=ce
# Mon, 18 Jul 2022 23:38:11 GMT
ARG EE_PORTS
# Mon, 18 Jul 2022 23:38:13 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Mon, 18 Jul 2022 23:38:13 GMT
ARG KONG_VERSION=2.8.1
# Mon, 18 Jul 2022 23:38:14 GMT
ENV KONG_VERSION=2.8.1
# Mon, 18 Jul 2022 23:38:15 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Mon, 18 Jul 2022 23:38:16 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Mon, 18 Jul 2022 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Mon, 18 Jul 2022 23:38:25 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Mon, 18 Jul 2022 23:38:25 GMT
USER kong
# Mon, 18 Jul 2022 23:38:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Jul 2022 23:38:27 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 18 Jul 2022 23:38:28 GMT
STOPSIGNAL SIGQUIT
# Mon, 18 Jul 2022 23:38:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Mon, 18 Jul 2022 23:38:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1302724bde7bafd2ba09b81d64c1fea90938cc5dd1cf54dd731be936c347aaa`  
		Last Modified: Mon, 18 Jul 2022 23:39:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51072c79d716ea1d1997805681b49c9df516af94b307573653daad345405b107`  
		Last Modified: Mon, 18 Jul 2022 23:39:59 GMT  
		Size: 45.8 MB (45812015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b5ae76cfb4f221d5b49ef4f884ffde2058c0bf17bc53678aa6fe68552ba54d`  
		Last Modified: Mon, 18 Jul 2022 23:39:51 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1-ubuntu`

```console
$ docker pull kong@sha256:27ba987186ac8913235d0bea44433e295511b776e37cc24cad69be56659b44c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5d2559d9967e39a7c0285643a484dc59a434a3dcc73b66183b4d9811ba81bb95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121229036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9348939116e58d77efb379d00687a58a85516ea07a901e5ce6f610ae2ce4ce68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:20:55 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:20:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:55 GMT
USER kong
# Tue, 14 Jun 2022 23:20:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4724d8b04ccf412df4c2eab1db30e216e64b5c7753529b193353c2ba6c8a0b0`  
		Last Modified: Tue, 14 Jun 2022 23:23:36 GMT  
		Size: 67.6 MB (67573561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28de5e8494dca4441e0ee102c3ef5807cd89429f162901e8e26c43625fab30f8`  
		Last Modified: Tue, 14 Jun 2022 23:23:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d35bf65fd2f20eac2327eedb0ad547d92ff8dc60ef0fbd382a72b2e90ee872ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121726118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26405f0174d52a4756cb1ca6e56ab10d1323b68a9697f02b56213d57c47e5f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:40:46 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:47 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:48 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:40:49 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:41:31 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:41:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:41:32 GMT
USER kong
# Tue, 14 Jun 2022 23:41:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:41:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:41:35 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:41:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:41:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66957df71376f98a0e8eb085ef05d9bd8e0647ee35f7576de662cfeed4227cdd`  
		Last Modified: Tue, 14 Jun 2022 23:46:28 GMT  
		Size: 69.5 MB (69452065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b313f50a105849eb0f70997fd0b89b8499f1d2ad74d56b0d467902d67f1bd1`  
		Last Modified: Tue, 14 Jun 2022 23:46:16 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:7da24d355f2396c38cff56625b6ae5134dc28efca75c8d43562384a30c9f4925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:76e2511d4844e42a1118c561be6c2f797de4319d3359ba141bee3dd307c9846f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49326697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac914d61e19c72a49fd1d32d6e2a58367034c48af55fe776c1ae56ab2271228b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:24:37 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 19 Jul 2022 00:24:37 GMT
ARG ASSET=ce
# Tue, 19 Jul 2022 00:24:37 GMT
ENV ASSET=ce
# Tue, 19 Jul 2022 00:24:37 GMT
ARG EE_PORTS
# Tue, 19 Jul 2022 00:24:37 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_VERSION=2.8.1
# Tue, 19 Jul 2022 00:24:37 GMT
ENV KONG_VERSION=2.8.1
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 19 Jul 2022 00:24:45 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 19 Jul 2022 00:24:46 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 19 Jul 2022 00:24:46 GMT
USER kong
# Tue, 19 Jul 2022 00:24:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Jul 2022 00:24:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 19 Jul 2022 00:24:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Jul 2022 00:24:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 19 Jul 2022 00:24:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a452a510cfd6ecd10d271f128ecb0eff4928164bd7aa989464a7ab8bd4a9f370`  
		Last Modified: Tue, 19 Jul 2022 00:25:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01021de023377a2ff9c3c5ac1e6e059ac3bd004e123c9f09c514fc618b344582`  
		Last Modified: Tue, 19 Jul 2022 00:25:33 GMT  
		Size: 46.5 MB (46526880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd69f5117b2d5591e8da6d2d6c8517b4dd714db165c0ba782885d36ac03b4fb`  
		Last Modified: Tue, 19 Jul 2022 00:25:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:165a85a4bce35a4d1966589fb9721567019aa25ec97828d57f59e630d035c737
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48507749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a03239cfc5173edd64ec1584d4976624a6d27e3155f3bc28303cfb844797fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:38:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Mon, 18 Jul 2022 23:38:09 GMT
ARG ASSET=ce
# Mon, 18 Jul 2022 23:38:10 GMT
ENV ASSET=ce
# Mon, 18 Jul 2022 23:38:11 GMT
ARG EE_PORTS
# Mon, 18 Jul 2022 23:38:13 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Mon, 18 Jul 2022 23:38:13 GMT
ARG KONG_VERSION=2.8.1
# Mon, 18 Jul 2022 23:38:14 GMT
ENV KONG_VERSION=2.8.1
# Mon, 18 Jul 2022 23:38:15 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Mon, 18 Jul 2022 23:38:16 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Mon, 18 Jul 2022 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Mon, 18 Jul 2022 23:38:25 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Mon, 18 Jul 2022 23:38:25 GMT
USER kong
# Mon, 18 Jul 2022 23:38:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Jul 2022 23:38:27 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 18 Jul 2022 23:38:28 GMT
STOPSIGNAL SIGQUIT
# Mon, 18 Jul 2022 23:38:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Mon, 18 Jul 2022 23:38:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1302724bde7bafd2ba09b81d64c1fea90938cc5dd1cf54dd731be936c347aaa`  
		Last Modified: Mon, 18 Jul 2022 23:39:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51072c79d716ea1d1997805681b49c9df516af94b307573653daad345405b107`  
		Last Modified: Mon, 18 Jul 2022 23:39:59 GMT  
		Size: 45.8 MB (45812015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b5ae76cfb4f221d5b49ef4f884ffde2058c0bf17bc53678aa6fe68552ba54d`  
		Last Modified: Mon, 18 Jul 2022 23:39:51 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:7da24d355f2396c38cff56625b6ae5134dc28efca75c8d43562384a30c9f4925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:76e2511d4844e42a1118c561be6c2f797de4319d3359ba141bee3dd307c9846f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49326697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac914d61e19c72a49fd1d32d6e2a58367034c48af55fe776c1ae56ab2271228b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:24:37 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 19 Jul 2022 00:24:37 GMT
ARG ASSET=ce
# Tue, 19 Jul 2022 00:24:37 GMT
ENV ASSET=ce
# Tue, 19 Jul 2022 00:24:37 GMT
ARG EE_PORTS
# Tue, 19 Jul 2022 00:24:37 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_VERSION=2.8.1
# Tue, 19 Jul 2022 00:24:37 GMT
ENV KONG_VERSION=2.8.1
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 19 Jul 2022 00:24:37 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 19 Jul 2022 00:24:45 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 19 Jul 2022 00:24:46 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 19 Jul 2022 00:24:46 GMT
USER kong
# Tue, 19 Jul 2022 00:24:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Jul 2022 00:24:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 19 Jul 2022 00:24:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Jul 2022 00:24:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 19 Jul 2022 00:24:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a452a510cfd6ecd10d271f128ecb0eff4928164bd7aa989464a7ab8bd4a9f370`  
		Last Modified: Tue, 19 Jul 2022 00:25:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01021de023377a2ff9c3c5ac1e6e059ac3bd004e123c9f09c514fc618b344582`  
		Last Modified: Tue, 19 Jul 2022 00:25:33 GMT  
		Size: 46.5 MB (46526880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd69f5117b2d5591e8da6d2d6c8517b4dd714db165c0ba782885d36ac03b4fb`  
		Last Modified: Tue, 19 Jul 2022 00:25:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:165a85a4bce35a4d1966589fb9721567019aa25ec97828d57f59e630d035c737
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48507749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a03239cfc5173edd64ec1584d4976624a6d27e3155f3bc28303cfb844797fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:38:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Mon, 18 Jul 2022 23:38:09 GMT
ARG ASSET=ce
# Mon, 18 Jul 2022 23:38:10 GMT
ENV ASSET=ce
# Mon, 18 Jul 2022 23:38:11 GMT
ARG EE_PORTS
# Mon, 18 Jul 2022 23:38:13 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Mon, 18 Jul 2022 23:38:13 GMT
ARG KONG_VERSION=2.8.1
# Mon, 18 Jul 2022 23:38:14 GMT
ENV KONG_VERSION=2.8.1
# Mon, 18 Jul 2022 23:38:15 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Mon, 18 Jul 2022 23:38:16 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Mon, 18 Jul 2022 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Mon, 18 Jul 2022 23:38:25 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Mon, 18 Jul 2022 23:38:25 GMT
USER kong
# Mon, 18 Jul 2022 23:38:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Jul 2022 23:38:27 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 18 Jul 2022 23:38:28 GMT
STOPSIGNAL SIGQUIT
# Mon, 18 Jul 2022 23:38:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Mon, 18 Jul 2022 23:38:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1302724bde7bafd2ba09b81d64c1fea90938cc5dd1cf54dd731be936c347aaa`  
		Last Modified: Mon, 18 Jul 2022 23:39:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51072c79d716ea1d1997805681b49c9df516af94b307573653daad345405b107`  
		Last Modified: Mon, 18 Jul 2022 23:39:59 GMT  
		Size: 45.8 MB (45812015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b5ae76cfb4f221d5b49ef4f884ffde2058c0bf17bc53678aa6fe68552ba54d`  
		Last Modified: Mon, 18 Jul 2022 23:39:51 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:27ba987186ac8913235d0bea44433e295511b776e37cc24cad69be56659b44c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5d2559d9967e39a7c0285643a484dc59a434a3dcc73b66183b4d9811ba81bb95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121229036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9348939116e58d77efb379d00687a58a85516ea07a901e5ce6f610ae2ce4ce68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:20:55 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:20:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:55 GMT
USER kong
# Tue, 14 Jun 2022 23:20:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4724d8b04ccf412df4c2eab1db30e216e64b5c7753529b193353c2ba6c8a0b0`  
		Last Modified: Tue, 14 Jun 2022 23:23:36 GMT  
		Size: 67.6 MB (67573561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28de5e8494dca4441e0ee102c3ef5807cd89429f162901e8e26c43625fab30f8`  
		Last Modified: Tue, 14 Jun 2022 23:23:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d35bf65fd2f20eac2327eedb0ad547d92ff8dc60ef0fbd382a72b2e90ee872ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121726118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26405f0174d52a4756cb1ca6e56ab10d1323b68a9697f02b56213d57c47e5f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:40:46 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:47 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:48 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:40:49 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:41:31 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:41:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:41:32 GMT
USER kong
# Tue, 14 Jun 2022 23:41:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:41:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:41:35 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:41:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:41:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66957df71376f98a0e8eb085ef05d9bd8e0647ee35f7576de662cfeed4227cdd`  
		Last Modified: Tue, 14 Jun 2022 23:46:28 GMT  
		Size: 69.5 MB (69452065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b313f50a105849eb0f70997fd0b89b8499f1d2ad74d56b0d467902d67f1bd1`  
		Last Modified: Tue, 14 Jun 2022 23:46:16 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
