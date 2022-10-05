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
-	[`kong:3.0`](#kong30)
-	[`kong:3.0-ubuntu`](#kong30-ubuntu)
-	[`kong:3.0.0`](#kong300)
-	[`kong:3.0.0-alpine`](#kong300-alpine)
-	[`kong:3.0.0-ubuntu`](#kong300-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.5`

```console
$ docker pull kong@sha256:df40856b3bb7775b655016e432f4ab0eb0119dd7e194fda94cf268c159b45d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5` - linux; amd64

```console
$ docker pull kong@sha256:3d935fb8d979d10395b5712b3643c489d6085e85b04196f087b0bc4a57655ef1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49219622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746e0ab1c399ba04ad448f99cba09ef46362b814962136724bbd16a0ff896cc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:59 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:59 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:59 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:51:00 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:51:00 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:51:26 GMT
ARG KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:51:26 GMT
ENV KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:51:26 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 09 Aug 2022 20:51:26 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 09 Aug 2022 20:51:33 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:51:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:51:34 GMT
USER kong
# Tue, 09 Aug 2022 20:51:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:51:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:51:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:51:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:51:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb31d71e8b572b72e18738ce5a5ce873f6bdbd4dfe392710abfaa0b239f5e9e`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe5a5d273313cadd6692e26c961154c8b932e85b748175c31cf56d87115e6f8`  
		Last Modified: Tue, 09 Aug 2022 20:53:19 GMT  
		Size: 46.4 MB (46395098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7318b6ebdf194ef2f4893426d03f77cfe5f9c10b99e54bdfc17aabd811165963`  
		Last Modified: Tue, 09 Aug 2022 20:53:11 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:def066852f719d3e64920b7701673370a967d25714d5d84625b4817b1efc5287
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48424283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d9df74b229506dd2ac6abf64b84819420d931766015b2cf9b0cd31b0107ad2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:43:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:43:12 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:43:13 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:43:14 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:43:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:44:33 GMT
ARG KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:44:34 GMT
ENV KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:44:35 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 09 Aug 2022 20:44:36 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 09 Aug 2022 20:44:55 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:44:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:44:56 GMT
USER kong
# Tue, 09 Aug 2022 20:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:44:58 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:44:59 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:45:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:45:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf24c8e5476c8b7b4206bb7d73b6e374dd6f847c367e880a7e72e96aa1dfd355`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b772d249cbb4432f47594d8c8ae02be54a589b7a07a632fee725bd5519bd1db`  
		Last Modified: Tue, 09 Aug 2022 20:47:28 GMT  
		Size: 45.7 MB (45704832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bc7a05e46049b909f0b4306fe1ca5056b6545e7f9d7a5649eb5474a5b21c59`  
		Last Modified: Tue, 09 Aug 2022 20:47:20 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-ubuntu`

```console
$ docker pull kong@sha256:7e94157233cb982e62211e4fd8b53994057d8dcfcc7dc27ad9b0f1a27b3f363a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e632ff086a0398c2e689ad15179a4c1a21a52bf97eae02e9cbe9bcbc8bc41453
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121373747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bc344365a9680adcc5a9b5f47c0fa586d0277ce2dcf80b2c63ee0c015530c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 18:05:56 GMT
ENV KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Wed, 05 Oct 2022 18:06:17 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:06:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:06:18 GMT
USER kong
# Wed, 05 Oct 2022 18:06:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:06:19 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:06:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:06:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:06:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feafaa2914aeeed8aa4de482bc243e365ed0f4ed3e2fbae0768c8a361cb9754c`  
		Last Modified: Wed, 05 Oct 2022 18:08:48 GMT  
		Size: 67.7 MB (67716453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a07f475cc0994afcdbe19a018a9413c11861f5a8e22c3cb7d88a87b158083ef`  
		Last Modified: Wed, 05 Oct 2022 18:08:36 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e28154aea3d28adb56e330635c326316b54b2f2ac5e22d110b1172949b711196
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118404412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412dd6500807518ad61eb53f7f67b3438a9986e525b6e88d8e817438e8aae3d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:00:20 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 16:00:20 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 16:00:21 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 16:00:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 16:03:17 GMT
ARG KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 16:03:18 GMT
ENV KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 16:03:19 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Wed, 05 Oct 2022 16:03:20 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Wed, 05 Oct 2022 16:03:48 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:03:50 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:03:50 GMT
USER kong
# Wed, 05 Oct 2022 16:03:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:03:52 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:03:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:03:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:03:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f20e2ab08e0103d6be14c1b3d377ca9e5f15a0a1256d9621c287546c1b9f4de`  
		Last Modified: Wed, 05 Oct 2022 16:05:25 GMT  
		Size: 25.1 MB (25081964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4103eb0376b976fac8b1121dc604af20917888625ae4e224e466f81fa68336`  
		Last Modified: Wed, 05 Oct 2022 16:06:49 GMT  
		Size: 66.1 MB (66129945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6b39b4604dfdcc6c6ceb5bc14d7771450cf8cf6e23a18fcb97c51ab33ce1af`  
		Last Modified: Wed, 05 Oct 2022 16:06:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2`

```console
$ docker pull kong@sha256:df40856b3bb7775b655016e432f4ab0eb0119dd7e194fda94cf268c159b45d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2` - linux; amd64

```console
$ docker pull kong@sha256:3d935fb8d979d10395b5712b3643c489d6085e85b04196f087b0bc4a57655ef1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49219622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746e0ab1c399ba04ad448f99cba09ef46362b814962136724bbd16a0ff896cc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:59 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:59 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:59 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:51:00 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:51:00 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:51:26 GMT
ARG KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:51:26 GMT
ENV KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:51:26 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 09 Aug 2022 20:51:26 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 09 Aug 2022 20:51:33 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:51:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:51:34 GMT
USER kong
# Tue, 09 Aug 2022 20:51:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:51:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:51:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:51:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:51:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb31d71e8b572b72e18738ce5a5ce873f6bdbd4dfe392710abfaa0b239f5e9e`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe5a5d273313cadd6692e26c961154c8b932e85b748175c31cf56d87115e6f8`  
		Last Modified: Tue, 09 Aug 2022 20:53:19 GMT  
		Size: 46.4 MB (46395098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7318b6ebdf194ef2f4893426d03f77cfe5f9c10b99e54bdfc17aabd811165963`  
		Last Modified: Tue, 09 Aug 2022 20:53:11 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:def066852f719d3e64920b7701673370a967d25714d5d84625b4817b1efc5287
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48424283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d9df74b229506dd2ac6abf64b84819420d931766015b2cf9b0cd31b0107ad2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:43:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:43:12 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:43:13 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:43:14 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:43:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:44:33 GMT
ARG KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:44:34 GMT
ENV KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:44:35 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 09 Aug 2022 20:44:36 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 09 Aug 2022 20:44:55 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:44:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:44:56 GMT
USER kong
# Tue, 09 Aug 2022 20:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:44:58 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:44:59 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:45:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:45:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf24c8e5476c8b7b4206bb7d73b6e374dd6f847c367e880a7e72e96aa1dfd355`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b772d249cbb4432f47594d8c8ae02be54a589b7a07a632fee725bd5519bd1db`  
		Last Modified: Tue, 09 Aug 2022 20:47:28 GMT  
		Size: 45.7 MB (45704832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bc7a05e46049b909f0b4306fe1ca5056b6545e7f9d7a5649eb5474a5b21c59`  
		Last Modified: Tue, 09 Aug 2022 20:47:20 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2-alpine`

```console
$ docker pull kong@sha256:df40856b3bb7775b655016e432f4ab0eb0119dd7e194fda94cf268c159b45d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:3d935fb8d979d10395b5712b3643c489d6085e85b04196f087b0bc4a57655ef1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49219622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746e0ab1c399ba04ad448f99cba09ef46362b814962136724bbd16a0ff896cc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:59 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:59 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:59 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:51:00 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:51:00 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:51:26 GMT
ARG KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:51:26 GMT
ENV KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:51:26 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 09 Aug 2022 20:51:26 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 09 Aug 2022 20:51:33 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:51:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:51:34 GMT
USER kong
# Tue, 09 Aug 2022 20:51:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:51:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:51:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:51:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:51:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb31d71e8b572b72e18738ce5a5ce873f6bdbd4dfe392710abfaa0b239f5e9e`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe5a5d273313cadd6692e26c961154c8b932e85b748175c31cf56d87115e6f8`  
		Last Modified: Tue, 09 Aug 2022 20:53:19 GMT  
		Size: 46.4 MB (46395098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7318b6ebdf194ef2f4893426d03f77cfe5f9c10b99e54bdfc17aabd811165963`  
		Last Modified: Tue, 09 Aug 2022 20:53:11 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:def066852f719d3e64920b7701673370a967d25714d5d84625b4817b1efc5287
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48424283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d9df74b229506dd2ac6abf64b84819420d931766015b2cf9b0cd31b0107ad2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:43:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:43:12 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:43:13 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:43:14 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:43:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:44:33 GMT
ARG KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:44:34 GMT
ENV KONG_VERSION=2.5.2
# Tue, 09 Aug 2022 20:44:35 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 09 Aug 2022 20:44:36 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 09 Aug 2022 20:44:55 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:44:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:44:56 GMT
USER kong
# Tue, 09 Aug 2022 20:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:44:58 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:44:59 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:45:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:45:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf24c8e5476c8b7b4206bb7d73b6e374dd6f847c367e880a7e72e96aa1dfd355`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b772d249cbb4432f47594d8c8ae02be54a589b7a07a632fee725bd5519bd1db`  
		Last Modified: Tue, 09 Aug 2022 20:47:28 GMT  
		Size: 45.7 MB (45704832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bc7a05e46049b909f0b4306fe1ca5056b6545e7f9d7a5649eb5474a5b21c59`  
		Last Modified: Tue, 09 Aug 2022 20:47:20 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2-ubuntu`

```console
$ docker pull kong@sha256:7e94157233cb982e62211e4fd8b53994057d8dcfcc7dc27ad9b0f1a27b3f363a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e632ff086a0398c2e689ad15179a4c1a21a52bf97eae02e9cbe9bcbc8bc41453
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121373747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bc344365a9680adcc5a9b5f47c0fa586d0277ce2dcf80b2c63ee0c015530c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 18:05:56 GMT
ENV KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Wed, 05 Oct 2022 18:06:17 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:06:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:06:18 GMT
USER kong
# Wed, 05 Oct 2022 18:06:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:06:19 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:06:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:06:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:06:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feafaa2914aeeed8aa4de482bc243e365ed0f4ed3e2fbae0768c8a361cb9754c`  
		Last Modified: Wed, 05 Oct 2022 18:08:48 GMT  
		Size: 67.7 MB (67716453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a07f475cc0994afcdbe19a018a9413c11861f5a8e22c3cb7d88a87b158083ef`  
		Last Modified: Wed, 05 Oct 2022 18:08:36 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e28154aea3d28adb56e330635c326316b54b2f2ac5e22d110b1172949b711196
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118404412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412dd6500807518ad61eb53f7f67b3438a9986e525b6e88d8e817438e8aae3d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:00:20 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 16:00:20 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 16:00:21 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 16:00:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 16:03:17 GMT
ARG KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 16:03:18 GMT
ENV KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 16:03:19 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Wed, 05 Oct 2022 16:03:20 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Wed, 05 Oct 2022 16:03:48 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:03:50 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:03:50 GMT
USER kong
# Wed, 05 Oct 2022 16:03:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:03:52 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:03:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:03:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:03:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f20e2ab08e0103d6be14c1b3d377ca9e5f15a0a1256d9621c287546c1b9f4de`  
		Last Modified: Wed, 05 Oct 2022 16:05:25 GMT  
		Size: 25.1 MB (25081964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4103eb0376b976fac8b1121dc604af20917888625ae4e224e466f81fa68336`  
		Last Modified: Wed, 05 Oct 2022 16:06:49 GMT  
		Size: 66.1 MB (66129945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6b39b4604dfdcc6c6ceb5bc14d7771450cf8cf6e23a18fcb97c51ab33ce1af`  
		Last Modified: Wed, 05 Oct 2022 16:06:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6`

```console
$ docker pull kong@sha256:46225823d1a96d0a3a99d1342b8b2f7b09b8c86357d0d4ba78b6359994f7a11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6` - linux; amd64

```console
$ docker pull kong@sha256:65fc054f1e133a27e059f36e46ab834ca9d8cc96dc9411ee2a6baea87edd4878
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50240678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829954c99f0b57a55aa6e7fb54f705d4825b9c86bc923a36a6b8f042112addfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:59 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:59 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:59 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:51:00 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:51:00 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:51:13 GMT
ARG KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:51:13 GMT
ENV KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:51:13 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 09 Aug 2022 20:51:13 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 09 Aug 2022 20:51:20 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:51:20 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:51:21 GMT
USER kong
# Tue, 09 Aug 2022 20:51:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:51:21 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:51:21 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:51:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:51:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb31d71e8b572b72e18738ce5a5ce873f6bdbd4dfe392710abfaa0b239f5e9e`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1143996ec4f5e396697ffc70d6e2d841941f1cb444050571fc9256fea564403d`  
		Last Modified: Tue, 09 Aug 2022 20:52:59 GMT  
		Size: 47.4 MB (47416156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb252670b28cd4ac88ae7c652f83f084aec63230dcf3decf1991f3db8a5ce5f`  
		Last Modified: Tue, 09 Aug 2022 20:52:51 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3145b8288dcb870adcd915c96f9b4c96dd9583e4069f6f65026a7fcf62a28502
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49654939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3347c8c9f5cc1b42f01a55c503944a1ae2e9b94e715a74856a92c66ad524f30a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:43:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:43:12 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:43:13 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:43:14 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:43:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:43:53 GMT
ARG KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:43:54 GMT
ENV KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:43:55 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 09 Aug 2022 20:43:56 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 09 Aug 2022 20:44:16 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:44:17 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:44:17 GMT
USER kong
# Tue, 09 Aug 2022 20:44:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:44:19 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:44:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:44:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:44:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf24c8e5476c8b7b4206bb7d73b6e374dd6f847c367e880a7e72e96aa1dfd355`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f92c8c87de2bd53ee08911b493553b45eecc09b0940d3958141d2feb9ca3aca`  
		Last Modified: Tue, 09 Aug 2022 20:47:05 GMT  
		Size: 46.9 MB (46935488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85baf7f0279b614b72664a07828f1e5782e57b6510472232213c12692b2f09`  
		Last Modified: Tue, 09 Aug 2022 20:46:57 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-ubuntu`

```console
$ docker pull kong@sha256:80764058c7bfed69eace499cb52ccf6efecfc54585835e2a3a88a02cde257df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:62f0eb7ee8aecf4d9ae88517c0b54e9401f2a992719e7f38d592650d443e4370
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128258108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8466c81f7e147ef5ef114b87cf3a53fe0bf59eaa7df8336d594fadf88cf56e83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 18:05:26 GMT
ENV KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Wed, 05 Oct 2022 18:05:48 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:05:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:05:49 GMT
USER kong
# Wed, 05 Oct 2022 18:05:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:05:49 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:05:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:05:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:05:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e993696815ce3a452cb95ab776e9c62ff68517f43710256e73e840cffb96e`  
		Last Modified: Wed, 05 Oct 2022 18:08:25 GMT  
		Size: 74.6 MB (74600814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb74a132762f4f4e3c5e5039de49d10ffd3c81369242eb4030c36ad9517bfa`  
		Last Modified: Wed, 05 Oct 2022 18:08:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7959dfdbadbe22048a6bfe42c860367e3ee46e87f0355482761ebb2bd6344249
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125291886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e14163bb9b74116b6a4088c99cc27460c5472c05ccce60f9e27cbdad999033`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:00:20 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 16:00:20 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 16:00:21 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 16:00:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 16:02:12 GMT
ARG KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 16:02:13 GMT
ENV KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 16:02:14 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Wed, 05 Oct 2022 16:02:15 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Wed, 05 Oct 2022 16:02:54 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:02:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:02:56 GMT
USER kong
# Wed, 05 Oct 2022 16:02:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:02:58 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:02:59 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:03:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:03:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f20e2ab08e0103d6be14c1b3d377ca9e5f15a0a1256d9621c287546c1b9f4de`  
		Last Modified: Wed, 05 Oct 2022 16:05:25 GMT  
		Size: 25.1 MB (25081964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cec1feb82f9fb166e93c65b4850f9091ddc92322466174a41619467d0f4e3`  
		Last Modified: Wed, 05 Oct 2022 16:06:25 GMT  
		Size: 73.0 MB (73017419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381756fc3ea950cdfe10255dc06998b14a9e521385d86d838bf0fc9fdbb2b163`  
		Last Modified: Wed, 05 Oct 2022 16:06:13 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1`

```console
$ docker pull kong@sha256:46225823d1a96d0a3a99d1342b8b2f7b09b8c86357d0d4ba78b6359994f7a11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1` - linux; amd64

```console
$ docker pull kong@sha256:65fc054f1e133a27e059f36e46ab834ca9d8cc96dc9411ee2a6baea87edd4878
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50240678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829954c99f0b57a55aa6e7fb54f705d4825b9c86bc923a36a6b8f042112addfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:59 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:59 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:59 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:51:00 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:51:00 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:51:13 GMT
ARG KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:51:13 GMT
ENV KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:51:13 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 09 Aug 2022 20:51:13 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 09 Aug 2022 20:51:20 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:51:20 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:51:21 GMT
USER kong
# Tue, 09 Aug 2022 20:51:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:51:21 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:51:21 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:51:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:51:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb31d71e8b572b72e18738ce5a5ce873f6bdbd4dfe392710abfaa0b239f5e9e`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1143996ec4f5e396697ffc70d6e2d841941f1cb444050571fc9256fea564403d`  
		Last Modified: Tue, 09 Aug 2022 20:52:59 GMT  
		Size: 47.4 MB (47416156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb252670b28cd4ac88ae7c652f83f084aec63230dcf3decf1991f3db8a5ce5f`  
		Last Modified: Tue, 09 Aug 2022 20:52:51 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3145b8288dcb870adcd915c96f9b4c96dd9583e4069f6f65026a7fcf62a28502
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49654939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3347c8c9f5cc1b42f01a55c503944a1ae2e9b94e715a74856a92c66ad524f30a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:43:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:43:12 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:43:13 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:43:14 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:43:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:43:53 GMT
ARG KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:43:54 GMT
ENV KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:43:55 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 09 Aug 2022 20:43:56 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 09 Aug 2022 20:44:16 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:44:17 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:44:17 GMT
USER kong
# Tue, 09 Aug 2022 20:44:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:44:19 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:44:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:44:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:44:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf24c8e5476c8b7b4206bb7d73b6e374dd6f847c367e880a7e72e96aa1dfd355`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f92c8c87de2bd53ee08911b493553b45eecc09b0940d3958141d2feb9ca3aca`  
		Last Modified: Tue, 09 Aug 2022 20:47:05 GMT  
		Size: 46.9 MB (46935488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85baf7f0279b614b72664a07828f1e5782e57b6510472232213c12692b2f09`  
		Last Modified: Tue, 09 Aug 2022 20:46:57 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-alpine`

```console
$ docker pull kong@sha256:46225823d1a96d0a3a99d1342b8b2f7b09b8c86357d0d4ba78b6359994f7a11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:65fc054f1e133a27e059f36e46ab834ca9d8cc96dc9411ee2a6baea87edd4878
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50240678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829954c99f0b57a55aa6e7fb54f705d4825b9c86bc923a36a6b8f042112addfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:59 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:59 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:59 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:51:00 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:51:00 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:51:13 GMT
ARG KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:51:13 GMT
ENV KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:51:13 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 09 Aug 2022 20:51:13 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 09 Aug 2022 20:51:20 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:51:20 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:51:21 GMT
USER kong
# Tue, 09 Aug 2022 20:51:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:51:21 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:51:21 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:51:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:51:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb31d71e8b572b72e18738ce5a5ce873f6bdbd4dfe392710abfaa0b239f5e9e`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1143996ec4f5e396697ffc70d6e2d841941f1cb444050571fc9256fea564403d`  
		Last Modified: Tue, 09 Aug 2022 20:52:59 GMT  
		Size: 47.4 MB (47416156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb252670b28cd4ac88ae7c652f83f084aec63230dcf3decf1991f3db8a5ce5f`  
		Last Modified: Tue, 09 Aug 2022 20:52:51 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3145b8288dcb870adcd915c96f9b4c96dd9583e4069f6f65026a7fcf62a28502
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49654939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3347c8c9f5cc1b42f01a55c503944a1ae2e9b94e715a74856a92c66ad524f30a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:43:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:43:12 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:43:13 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:43:14 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:43:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:43:53 GMT
ARG KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:43:54 GMT
ENV KONG_VERSION=2.6.1
# Tue, 09 Aug 2022 20:43:55 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 09 Aug 2022 20:43:56 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 09 Aug 2022 20:44:16 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:44:17 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:44:17 GMT
USER kong
# Tue, 09 Aug 2022 20:44:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:44:19 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:44:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:44:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:44:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf24c8e5476c8b7b4206bb7d73b6e374dd6f847c367e880a7e72e96aa1dfd355`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f92c8c87de2bd53ee08911b493553b45eecc09b0940d3958141d2feb9ca3aca`  
		Last Modified: Tue, 09 Aug 2022 20:47:05 GMT  
		Size: 46.9 MB (46935488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85baf7f0279b614b72664a07828f1e5782e57b6510472232213c12692b2f09`  
		Last Modified: Tue, 09 Aug 2022 20:46:57 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-ubuntu`

```console
$ docker pull kong@sha256:80764058c7bfed69eace499cb52ccf6efecfc54585835e2a3a88a02cde257df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:62f0eb7ee8aecf4d9ae88517c0b54e9401f2a992719e7f38d592650d443e4370
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128258108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8466c81f7e147ef5ef114b87cf3a53fe0bf59eaa7df8336d594fadf88cf56e83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 18:05:26 GMT
ENV KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Wed, 05 Oct 2022 18:05:48 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:05:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:05:49 GMT
USER kong
# Wed, 05 Oct 2022 18:05:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:05:49 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:05:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:05:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:05:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e993696815ce3a452cb95ab776e9c62ff68517f43710256e73e840cffb96e`  
		Last Modified: Wed, 05 Oct 2022 18:08:25 GMT  
		Size: 74.6 MB (74600814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb74a132762f4f4e3c5e5039de49d10ffd3c81369242eb4030c36ad9517bfa`  
		Last Modified: Wed, 05 Oct 2022 18:08:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7959dfdbadbe22048a6bfe42c860367e3ee46e87f0355482761ebb2bd6344249
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125291886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e14163bb9b74116b6a4088c99cc27460c5472c05ccce60f9e27cbdad999033`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:00:20 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 16:00:20 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 16:00:21 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 16:00:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 16:02:12 GMT
ARG KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 16:02:13 GMT
ENV KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 16:02:14 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Wed, 05 Oct 2022 16:02:15 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Wed, 05 Oct 2022 16:02:54 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:02:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:02:56 GMT
USER kong
# Wed, 05 Oct 2022 16:02:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:02:58 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:02:59 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:03:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:03:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f20e2ab08e0103d6be14c1b3d377ca9e5f15a0a1256d9621c287546c1b9f4de`  
		Last Modified: Wed, 05 Oct 2022 16:05:25 GMT  
		Size: 25.1 MB (25081964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334cec1feb82f9fb166e93c65b4850f9091ddc92322466174a41619467d0f4e3`  
		Last Modified: Wed, 05 Oct 2022 16:06:25 GMT  
		Size: 73.0 MB (73017419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381756fc3ea950cdfe10255dc06998b14a9e521385d86d838bf0fc9fdbb2b163`  
		Last Modified: Wed, 05 Oct 2022 16:06:13 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7`

```console
$ docker pull kong@sha256:c60af2f8633d4719bd6c8989de3a9e7c88cc500a17f1e371ec1f0dc51b6182bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7` - linux; amd64

```console
$ docker pull kong@sha256:9c21d4bc5aae773be7872c2edd2e0d0fa365352984311e234d39e4a9708fb74c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50148848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dade8e963fd6f83ecc1ae7b3e50718539c7b263ff1fea242893d39800014e0d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:59 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:59 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:59 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:51:00 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:51:00 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:51:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:51:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:51:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 09 Aug 2022 20:51:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 09 Aug 2022 20:51:07 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:51:08 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:51:08 GMT
USER kong
# Tue, 09 Aug 2022 20:51:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:51:08 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:51:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:51:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:51:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb31d71e8b572b72e18738ce5a5ce873f6bdbd4dfe392710abfaa0b239f5e9e`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcaa0cf883df54fdb29ac9dbf919864e35c4557da6490c9fc6d6a0e58172aa8`  
		Last Modified: Tue, 09 Aug 2022 20:52:37 GMT  
		Size: 47.3 MB (47324324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb36999ccc7dbbae9dc7ae7adff69f22b48a3d2b6a56cab3458f90a1c2ef9f89`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:39ba2815ffe5f5c822fb1a66c61abea4cc4ecc83eb3086cc04cbc9c82d23b040
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49578744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8860d91130909d7b20b4ca98a3d0402047cf8f45b60ffdd15418f8c258718f5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:43:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:43:12 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:43:13 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:43:14 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:43:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:43:16 GMT
ARG KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:43:17 GMT
ENV KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:43:18 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 09 Aug 2022 20:43:19 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 09 Aug 2022 20:43:37 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:43:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:43:38 GMT
USER kong
# Tue, 09 Aug 2022 20:43:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:43:40 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:43:41 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:43:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:43:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf24c8e5476c8b7b4206bb7d73b6e374dd6f847c367e880a7e72e96aa1dfd355`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c33ef81acec69a7618df2a3ff9095806decd55b4e1fe788bd6bd678ee4d8bb`  
		Last Modified: Tue, 09 Aug 2022 20:46:42 GMT  
		Size: 46.9 MB (46859292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72441bb69318c800b3f9710d8aee21166344bb91a8a3274d9f3ab1b08db01f`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7-ubuntu`

```console
$ docker pull kong@sha256:e62e53ba5181f05c27d18d2edbb97272510d4565c2725a63c735c0289c7b3b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1b3b987b13fc81da2bc6d633049a829a93edc97c864045ef7face0cf839ef55b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128168397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71cac7eed8a53d0cc9fbe23a14c1512174123d29c4c74b29476d5576424a20e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 18:04:56 GMT
ENV KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Wed, 05 Oct 2022 18:05:18 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:05:19 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:05:19 GMT
USER kong
# Wed, 05 Oct 2022 18:05:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:05:19 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:05:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:05:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:05:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073853ff82a5607beb1a0cc44c91ba59a4d1122dcb52322cc1a5531bd62a43a2`  
		Last Modified: Wed, 05 Oct 2022 18:07:57 GMT  
		Size: 74.5 MB (74511102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2450b04737255f8e696efca60087f8daa06ac4202cd42d03d8fb4990a420f22`  
		Last Modified: Wed, 05 Oct 2022 18:07:45 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:eb157fb45b7513a34ee7346bcf101f51a723878f681d734da59af1209f779749
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125203448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71a2b9ea24ebf4b91396b4c41fa8f777f1d33e9bdd1af1500f355864b060b2f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:00:20 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 16:00:20 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 16:00:21 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 16:00:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 16:01:16 GMT
ARG KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 16:01:16 GMT
ENV KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 16:01:17 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Wed, 05 Oct 2022 16:01:18 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Wed, 05 Oct 2022 16:01:56 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:01:57 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:01:57 GMT
USER kong
# Wed, 05 Oct 2022 16:01:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:01:59 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:02:00 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:02:01 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:02:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f20e2ab08e0103d6be14c1b3d377ca9e5f15a0a1256d9621c287546c1b9f4de`  
		Last Modified: Wed, 05 Oct 2022 16:05:25 GMT  
		Size: 25.1 MB (25081964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d123530c8c055d40c36f39c6cb0709ac2140afc0abe75c3da0a05f7ed45d24`  
		Last Modified: Wed, 05 Oct 2022 16:05:59 GMT  
		Size: 72.9 MB (72928980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c5796061e5648ed60d7642e8c3816d5bf4e148e98f1002f28297ebac309241`  
		Last Modified: Wed, 05 Oct 2022 16:05:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2`

```console
$ docker pull kong@sha256:c60af2f8633d4719bd6c8989de3a9e7c88cc500a17f1e371ec1f0dc51b6182bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2` - linux; amd64

```console
$ docker pull kong@sha256:9c21d4bc5aae773be7872c2edd2e0d0fa365352984311e234d39e4a9708fb74c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50148848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dade8e963fd6f83ecc1ae7b3e50718539c7b263ff1fea242893d39800014e0d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:59 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:59 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:59 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:51:00 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:51:00 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:51:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:51:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:51:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 09 Aug 2022 20:51:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 09 Aug 2022 20:51:07 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:51:08 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:51:08 GMT
USER kong
# Tue, 09 Aug 2022 20:51:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:51:08 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:51:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:51:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:51:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb31d71e8b572b72e18738ce5a5ce873f6bdbd4dfe392710abfaa0b239f5e9e`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcaa0cf883df54fdb29ac9dbf919864e35c4557da6490c9fc6d6a0e58172aa8`  
		Last Modified: Tue, 09 Aug 2022 20:52:37 GMT  
		Size: 47.3 MB (47324324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb36999ccc7dbbae9dc7ae7adff69f22b48a3d2b6a56cab3458f90a1c2ef9f89`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:39ba2815ffe5f5c822fb1a66c61abea4cc4ecc83eb3086cc04cbc9c82d23b040
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49578744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8860d91130909d7b20b4ca98a3d0402047cf8f45b60ffdd15418f8c258718f5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:43:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:43:12 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:43:13 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:43:14 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:43:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:43:16 GMT
ARG KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:43:17 GMT
ENV KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:43:18 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 09 Aug 2022 20:43:19 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 09 Aug 2022 20:43:37 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:43:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:43:38 GMT
USER kong
# Tue, 09 Aug 2022 20:43:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:43:40 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:43:41 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:43:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:43:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf24c8e5476c8b7b4206bb7d73b6e374dd6f847c367e880a7e72e96aa1dfd355`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c33ef81acec69a7618df2a3ff9095806decd55b4e1fe788bd6bd678ee4d8bb`  
		Last Modified: Tue, 09 Aug 2022 20:46:42 GMT  
		Size: 46.9 MB (46859292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72441bb69318c800b3f9710d8aee21166344bb91a8a3274d9f3ab1b08db01f`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-alpine`

```console
$ docker pull kong@sha256:c60af2f8633d4719bd6c8989de3a9e7c88cc500a17f1e371ec1f0dc51b6182bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:9c21d4bc5aae773be7872c2edd2e0d0fa365352984311e234d39e4a9708fb74c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50148848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dade8e963fd6f83ecc1ae7b3e50718539c7b263ff1fea242893d39800014e0d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:59 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:59 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:59 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:51:00 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:51:00 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:51:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:51:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:51:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 09 Aug 2022 20:51:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 09 Aug 2022 20:51:07 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:51:08 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:51:08 GMT
USER kong
# Tue, 09 Aug 2022 20:51:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:51:08 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:51:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:51:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:51:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb31d71e8b572b72e18738ce5a5ce873f6bdbd4dfe392710abfaa0b239f5e9e`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcaa0cf883df54fdb29ac9dbf919864e35c4557da6490c9fc6d6a0e58172aa8`  
		Last Modified: Tue, 09 Aug 2022 20:52:37 GMT  
		Size: 47.3 MB (47324324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb36999ccc7dbbae9dc7ae7adff69f22b48a3d2b6a56cab3458f90a1c2ef9f89`  
		Last Modified: Tue, 09 Aug 2022 20:52:29 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:39ba2815ffe5f5c822fb1a66c61abea4cc4ecc83eb3086cc04cbc9c82d23b040
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49578744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8860d91130909d7b20b4ca98a3d0402047cf8f45b60ffdd15418f8c258718f5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:43:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:43:12 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:43:13 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:43:14 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:43:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:43:16 GMT
ARG KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:43:17 GMT
ENV KONG_VERSION=2.7.2
# Tue, 09 Aug 2022 20:43:18 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 09 Aug 2022 20:43:19 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 09 Aug 2022 20:43:37 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:43:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:43:38 GMT
USER kong
# Tue, 09 Aug 2022 20:43:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:43:40 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:43:41 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:43:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:43:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf24c8e5476c8b7b4206bb7d73b6e374dd6f847c367e880a7e72e96aa1dfd355`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c33ef81acec69a7618df2a3ff9095806decd55b4e1fe788bd6bd678ee4d8bb`  
		Last Modified: Tue, 09 Aug 2022 20:46:42 GMT  
		Size: 46.9 MB (46859292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72441bb69318c800b3f9710d8aee21166344bb91a8a3274d9f3ab1b08db01f`  
		Last Modified: Tue, 09 Aug 2022 20:46:28 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-ubuntu`

```console
$ docker pull kong@sha256:e62e53ba5181f05c27d18d2edbb97272510d4565c2725a63c735c0289c7b3b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1b3b987b13fc81da2bc6d633049a829a93edc97c864045ef7face0cf839ef55b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128168397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71cac7eed8a53d0cc9fbe23a14c1512174123d29c4c74b29476d5576424a20e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 18:04:56 GMT
ENV KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Wed, 05 Oct 2022 18:05:18 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:05:19 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:05:19 GMT
USER kong
# Wed, 05 Oct 2022 18:05:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:05:19 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:05:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:05:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:05:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073853ff82a5607beb1a0cc44c91ba59a4d1122dcb52322cc1a5531bd62a43a2`  
		Last Modified: Wed, 05 Oct 2022 18:07:57 GMT  
		Size: 74.5 MB (74511102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2450b04737255f8e696efca60087f8daa06ac4202cd42d03d8fb4990a420f22`  
		Last Modified: Wed, 05 Oct 2022 18:07:45 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:eb157fb45b7513a34ee7346bcf101f51a723878f681d734da59af1209f779749
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125203448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71a2b9ea24ebf4b91396b4c41fa8f777f1d33e9bdd1af1500f355864b060b2f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:00:20 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 16:00:20 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 16:00:21 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 16:00:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 16:01:16 GMT
ARG KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 16:01:16 GMT
ENV KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 16:01:17 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Wed, 05 Oct 2022 16:01:18 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Wed, 05 Oct 2022 16:01:56 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:01:57 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:01:57 GMT
USER kong
# Wed, 05 Oct 2022 16:01:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:01:59 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:02:00 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:02:01 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:02:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f20e2ab08e0103d6be14c1b3d377ca9e5f15a0a1256d9621c287546c1b9f4de`  
		Last Modified: Wed, 05 Oct 2022 16:05:25 GMT  
		Size: 25.1 MB (25081964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d123530c8c055d40c36f39c6cb0709ac2140afc0abe75c3da0a05f7ed45d24`  
		Last Modified: Wed, 05 Oct 2022 16:05:59 GMT  
		Size: 72.9 MB (72928980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c5796061e5648ed60d7642e8c3816d5bf4e148e98f1002f28297ebac309241`  
		Last Modified: Wed, 05 Oct 2022 16:05:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8`

```console
$ docker pull kong@sha256:4dc4da99f8da9e4d7ab01da7feb3062ba12be1324fa8359f2396bbb7ac07bb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:7853bcf8b77f2d47fbda34b9ccba8d108c8145622905f5f66c2bc124435d4c88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49349895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf394ffed022e33afd4c01e0f69d77671361bb35c0e0d391a7bf102860dafbfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:46 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:46 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:50:46 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:50:46 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:50:46 GMT
ARG KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:50:46 GMT
ENV KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:50:46 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 09 Aug 2022 20:50:46 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 09 Aug 2022 20:50:53 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:50:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:50:54 GMT
USER kong
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:54 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:50:54 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:50:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:50:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df79bc1e6d9219ba18210a0d465d9d48e3dd749d1fea9c0a50f0e8bb7c57453b`  
		Last Modified: Tue, 09 Aug 2022 20:52:03 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17afdc22f8ede5802cf3c22afe83fdce0451a7282f0d466737dd68f897abb103`  
		Last Modified: Tue, 09 Aug 2022 20:52:11 GMT  
		Size: 46.5 MB (46542829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4782db41dff7a89a4b61290bdcdef60323b2f97dac63b587f51b5f8990443ed8`  
		Last Modified: Tue, 09 Aug 2022 20:52:04 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2e4a51fba3b574ee35f990aef3bfd1120ad2e2704f3bc618697382a9f13eaa5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48542736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef17c5908a084b9879dac56870037eccf0c01f792d09fde4b1509019edcc6834`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:36 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:42:37 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:42:38 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:42:39 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:42:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:42:41 GMT
ARG KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:42:42 GMT
ENV KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:42:43 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 09 Aug 2022 20:42:44 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 09 Aug 2022 20:42:53 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:42:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:42:54 GMT
USER kong
# Tue, 09 Aug 2022 20:42:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:42:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:42:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:42:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:42:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70974eef12350195e179ac6f7e3f7ece7a292a31c6a4f5e19006b7df7f02df11`  
		Last Modified: Tue, 09 Aug 2022 20:45:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8314b864c236792b78293d546cc56ce12740413e395c5cc628457e893f46c905`  
		Last Modified: Tue, 09 Aug 2022 20:46:06 GMT  
		Size: 45.8 MB (45834060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422419cd811d0936d352e9b792f92bcf50bdc9af873da1eb9c5f91f48f0570ca`  
		Last Modified: Tue, 09 Aug 2022 20:45:58 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:35bf8c7bbacaa4f390833471d329c7be06fee5ddd5bfd9d6d776495adfee756f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:cedff6e436f88215dadcd6bf2d25062b9b5d3170ff6c9947b02c1319876e5fdb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121292578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142c60b0bbecd85bac643266c0995c1b42083af9b5c4da4d1ba31592bb7c7f8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 18:04:27 GMT
ENV KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Wed, 05 Oct 2022 18:04:48 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:04:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:04:49 GMT
USER kong
# Wed, 05 Oct 2022 18:04:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:04:50 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:04:50 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:04:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:04:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc176a053adb32647c56614ff026d0deba20cb6efd6372197e024bf7c5693e`  
		Last Modified: Wed, 05 Oct 2022 18:07:33 GMT  
		Size: 67.6 MB (67635284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69d17ca86369a39c8f6a302ebfa154002b3b253738effeb247bfa53ec0330cb`  
		Last Modified: Wed, 05 Oct 2022 18:07:21 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4ace2178b0cbab1f0bfff08ccb4027a2b2c55f3d7a2f799c84b5a3e88b6f02df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121785614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf83f8cd6bb6857178d8573b0a890e9a1ce3f3b92611defef27eb0f010b29f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:00:20 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 16:00:20 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 16:00:21 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 16:00:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 16:00:23 GMT
ARG KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 16:00:24 GMT
ENV KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 16:00:25 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Wed, 05 Oct 2022 16:00:26 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Wed, 05 Oct 2022 16:00:54 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:00:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:00:56 GMT
USER kong
# Wed, 05 Oct 2022 16:00:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:00:58 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:00:59 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:01:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:01:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f20e2ab08e0103d6be14c1b3d377ca9e5f15a0a1256d9621c287546c1b9f4de`  
		Last Modified: Wed, 05 Oct 2022 16:05:25 GMT  
		Size: 25.1 MB (25081964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b815f040535344818d17e5bc9921438e91fbdb7337887300b631c65b9ca2a71`  
		Last Modified: Wed, 05 Oct 2022 16:05:34 GMT  
		Size: 69.5 MB (69511147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9441e13ebe80993a48c4c1856e99266741e08b1aa47010addabad717a2202046`  
		Last Modified: Wed, 05 Oct 2022 16:05:23 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1`

```console
$ docker pull kong@sha256:4dc4da99f8da9e4d7ab01da7feb3062ba12be1324fa8359f2396bbb7ac07bb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1` - linux; amd64

```console
$ docker pull kong@sha256:7853bcf8b77f2d47fbda34b9ccba8d108c8145622905f5f66c2bc124435d4c88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49349895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf394ffed022e33afd4c01e0f69d77671361bb35c0e0d391a7bf102860dafbfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:46 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:46 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:50:46 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:50:46 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:50:46 GMT
ARG KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:50:46 GMT
ENV KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:50:46 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 09 Aug 2022 20:50:46 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 09 Aug 2022 20:50:53 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:50:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:50:54 GMT
USER kong
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:54 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:50:54 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:50:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:50:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df79bc1e6d9219ba18210a0d465d9d48e3dd749d1fea9c0a50f0e8bb7c57453b`  
		Last Modified: Tue, 09 Aug 2022 20:52:03 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17afdc22f8ede5802cf3c22afe83fdce0451a7282f0d466737dd68f897abb103`  
		Last Modified: Tue, 09 Aug 2022 20:52:11 GMT  
		Size: 46.5 MB (46542829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4782db41dff7a89a4b61290bdcdef60323b2f97dac63b587f51b5f8990443ed8`  
		Last Modified: Tue, 09 Aug 2022 20:52:04 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2e4a51fba3b574ee35f990aef3bfd1120ad2e2704f3bc618697382a9f13eaa5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48542736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef17c5908a084b9879dac56870037eccf0c01f792d09fde4b1509019edcc6834`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:36 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:42:37 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:42:38 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:42:39 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:42:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:42:41 GMT
ARG KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:42:42 GMT
ENV KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:42:43 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 09 Aug 2022 20:42:44 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 09 Aug 2022 20:42:53 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:42:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:42:54 GMT
USER kong
# Tue, 09 Aug 2022 20:42:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:42:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:42:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:42:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:42:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70974eef12350195e179ac6f7e3f7ece7a292a31c6a4f5e19006b7df7f02df11`  
		Last Modified: Tue, 09 Aug 2022 20:45:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8314b864c236792b78293d546cc56ce12740413e395c5cc628457e893f46c905`  
		Last Modified: Tue, 09 Aug 2022 20:46:06 GMT  
		Size: 45.8 MB (45834060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422419cd811d0936d352e9b792f92bcf50bdc9af873da1eb9c5f91f48f0570ca`  
		Last Modified: Tue, 09 Aug 2022 20:45:58 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1-alpine`

```console
$ docker pull kong@sha256:4dc4da99f8da9e4d7ab01da7feb3062ba12be1324fa8359f2396bbb7ac07bb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:7853bcf8b77f2d47fbda34b9ccba8d108c8145622905f5f66c2bc124435d4c88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49349895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf394ffed022e33afd4c01e0f69d77671361bb35c0e0d391a7bf102860dafbfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:50:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:50:46 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:50:46 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:50:46 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:50:46 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:50:46 GMT
ARG KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:50:46 GMT
ENV KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:50:46 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 09 Aug 2022 20:50:46 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 09 Aug 2022 20:50:53 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:50:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:50:54 GMT
USER kong
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:54 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:50:54 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:50:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:50:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df79bc1e6d9219ba18210a0d465d9d48e3dd749d1fea9c0a50f0e8bb7c57453b`  
		Last Modified: Tue, 09 Aug 2022 20:52:03 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17afdc22f8ede5802cf3c22afe83fdce0451a7282f0d466737dd68f897abb103`  
		Last Modified: Tue, 09 Aug 2022 20:52:11 GMT  
		Size: 46.5 MB (46542829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4782db41dff7a89a4b61290bdcdef60323b2f97dac63b587f51b5f8990443ed8`  
		Last Modified: Tue, 09 Aug 2022 20:52:04 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2e4a51fba3b574ee35f990aef3bfd1120ad2e2704f3bc618697382a9f13eaa5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48542736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef17c5908a084b9879dac56870037eccf0c01f792d09fde4b1509019edcc6834`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:36 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 09 Aug 2022 20:42:37 GMT
ARG ASSET=ce
# Tue, 09 Aug 2022 20:42:38 GMT
ENV ASSET=ce
# Tue, 09 Aug 2022 20:42:39 GMT
ARG EE_PORTS
# Tue, 09 Aug 2022 20:42:41 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 09 Aug 2022 20:42:41 GMT
ARG KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:42:42 GMT
ENV KONG_VERSION=2.8.1
# Tue, 09 Aug 2022 20:42:43 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 09 Aug 2022 20:42:44 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 09 Aug 2022 20:42:53 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 09 Aug 2022 20:42:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 09 Aug 2022 20:42:54 GMT
USER kong
# Tue, 09 Aug 2022 20:42:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:42:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 09 Aug 2022 20:42:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 20:42:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 09 Aug 2022 20:42:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70974eef12350195e179ac6f7e3f7ece7a292a31c6a4f5e19006b7df7f02df11`  
		Last Modified: Tue, 09 Aug 2022 20:45:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8314b864c236792b78293d546cc56ce12740413e395c5cc628457e893f46c905`  
		Last Modified: Tue, 09 Aug 2022 20:46:06 GMT  
		Size: 45.8 MB (45834060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422419cd811d0936d352e9b792f92bcf50bdc9af873da1eb9c5f91f48f0570ca`  
		Last Modified: Tue, 09 Aug 2022 20:45:58 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1-ubuntu`

```console
$ docker pull kong@sha256:35bf8c7bbacaa4f390833471d329c7be06fee5ddd5bfd9d6d776495adfee756f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:cedff6e436f88215dadcd6bf2d25062b9b5d3170ff6c9947b02c1319876e5fdb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121292578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142c60b0bbecd85bac643266c0995c1b42083af9b5c4da4d1ba31592bb7c7f8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 18:04:27 GMT
ENV KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Wed, 05 Oct 2022 18:04:48 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:04:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:04:49 GMT
USER kong
# Wed, 05 Oct 2022 18:04:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:04:50 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:04:50 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:04:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:04:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc176a053adb32647c56614ff026d0deba20cb6efd6372197e024bf7c5693e`  
		Last Modified: Wed, 05 Oct 2022 18:07:33 GMT  
		Size: 67.6 MB (67635284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69d17ca86369a39c8f6a302ebfa154002b3b253738effeb247bfa53ec0330cb`  
		Last Modified: Wed, 05 Oct 2022 18:07:21 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4ace2178b0cbab1f0bfff08ccb4027a2b2c55f3d7a2f799c84b5a3e88b6f02df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121785614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf83f8cd6bb6857178d8573b0a890e9a1ce3f3b92611defef27eb0f010b29f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:00:20 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 16:00:20 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 16:00:21 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 16:00:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 16:00:23 GMT
ARG KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 16:00:24 GMT
ENV KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 16:00:25 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Wed, 05 Oct 2022 16:00:26 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Wed, 05 Oct 2022 16:00:54 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:00:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:00:56 GMT
USER kong
# Wed, 05 Oct 2022 16:00:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:00:58 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:00:59 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:01:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:01:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f20e2ab08e0103d6be14c1b3d377ca9e5f15a0a1256d9621c287546c1b9f4de`  
		Last Modified: Wed, 05 Oct 2022 16:05:25 GMT  
		Size: 25.1 MB (25081964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b815f040535344818d17e5bc9921438e91fbdb7337887300b631c65b9ca2a71`  
		Last Modified: Wed, 05 Oct 2022 16:05:34 GMT  
		Size: 69.5 MB (69511147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9441e13ebe80993a48c4c1856e99266741e08b1aa47010addabad717a2202046`  
		Last Modified: Wed, 05 Oct 2022 16:05:23 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0`

```console
$ docker pull kong@sha256:5a9796196a6f21216497e2e1a9a606dbe6cd1a2405d4f99ea9d97aef13d3c071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0` - linux; amd64

```console
$ docker pull kong@sha256:8a54bbf5026200150c46a182e0d56d74ba7572d6cfe98e863fb20cdafce1d95e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51522357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bce760c29ce855d5935d777f2ec45b3a9ca895a09334825360cebd26a222e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 14 Sep 2022 00:07:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 14 Sep 2022 00:07:19 GMT
ARG ASSET=ce
# Wed, 14 Sep 2022 00:07:19 GMT
ENV ASSET=ce
# Wed, 14 Sep 2022 00:07:19 GMT
ARG EE_PORTS
# Wed, 14 Sep 2022 00:07:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Sep 2022 00:07:19 GMT
ARG KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 00:07:19 GMT
ENV KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 00:07:20 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 14 Sep 2022 00:07:20 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 14 Sep 2022 00:07:28 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 14 Sep 2022 00:07:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 14 Sep 2022 00:07:28 GMT
USER kong
# Wed, 14 Sep 2022 00:07:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Sep 2022 00:07:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Sep 2022 00:07:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Sep 2022 00:07:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 14 Sep 2022 00:07:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f8c583856d7a692eae94f47792d4cc4a214e2b9d36d1b6dd5eaded569804f`  
		Last Modified: Wed, 14 Sep 2022 00:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd3d1d803c378e5eb206c29367530e2f8a92578534afdf16cd4ff0da3e687f5`  
		Last Modified: Wed, 14 Sep 2022 00:09:33 GMT  
		Size: 48.7 MB (48715295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7a99de7f80d542680872b47fc5405bf068af5fa56916f994a15149ce05e441`  
		Last Modified: Wed, 14 Sep 2022 00:09:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:027a647f0c26cf6b7a763a87d0556f13f998bad6e894b8442442fcff3bb89744
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50657688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523519a6e5d6879a4227e5b1c165a53d9611b923a8202ae1f04050caef825747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Sep 2022 01:59:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 14 Sep 2022 01:59:10 GMT
ARG ASSET=ce
# Wed, 14 Sep 2022 01:59:11 GMT
ENV ASSET=ce
# Wed, 14 Sep 2022 01:59:12 GMT
ARG EE_PORTS
# Wed, 14 Sep 2022 01:59:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Sep 2022 01:59:14 GMT
ARG KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 01:59:15 GMT
ENV KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 01:59:16 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 14 Sep 2022 01:59:17 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 14 Sep 2022 01:59:26 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 14 Sep 2022 01:59:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 14 Sep 2022 01:59:27 GMT
USER kong
# Wed, 14 Sep 2022 01:59:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Sep 2022 01:59:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Sep 2022 01:59:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Sep 2022 01:59:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 14 Sep 2022 01:59:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033ed50262ad7d5f4f3be38481e74d6f1de3313623a89ec7a316233c87cb9f39`  
		Last Modified: Wed, 14 Sep 2022 02:02:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3318efbcbee2b6ebe247f02e9f3c2bdba1cad9ab96167a928e679b33cbe1bb41`  
		Last Modified: Wed, 14 Sep 2022 02:02:15 GMT  
		Size: 47.9 MB (47949011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fa05900110c4740c2e5720297d782338ded9ec460bf8d181fa6905ee5de189`  
		Last Modified: Wed, 14 Sep 2022 02:02:06 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0-ubuntu`

```console
$ docker pull kong@sha256:8a6061f898745d8d1ae6b9b2cc702d422e354844eefbfcd529353297e65ff47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b94b30d589c2d304b5c32ab10ce3c5b16f58b77c2aa363583da387c335c0fb48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126751347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a998d5233b41e636a9afe797738f040dfb82731ce74c88c9208bceae5ff1c5a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:03:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Oct 2022 18:03:44 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:03:44 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:03:44 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:03:44 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 18:03:45 GMT
ENV KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 05 Oct 2022 18:04:17 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:04:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:04:18 GMT
USER kong
# Wed, 05 Oct 2022 18:04:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:04:18 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:04:18 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:04:18 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:04:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a405c4afb98d18d76913bfe72f63dbd4a4d8c04256b6a7dfcbf44e6afba6f4`  
		Last Modified: Wed, 05 Oct 2022 18:06:58 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c61366193417348ac92ea7a0b85d3a941dd84e99ddce0ccf874f9e2dd064a6`  
		Last Modified: Wed, 05 Oct 2022 18:07:08 GMT  
		Size: 73.1 MB (73094048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff353d4dd575bdf6ca92775c17a2634b394fc8f507c04bbaedcdeee8e3eb48e`  
		Last Modified: Wed, 05 Oct 2022 18:06:56 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fdb693a2f651e8ea7fb72a3fbf27e948512f177e59bf67df495ace7bea594054
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123985385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5108a12659480aceff1ac2460acb6b4634ddee97df269cb93243ad915c17149e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 15:59:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Oct 2022 15:59:25 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 15:59:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 15:59:27 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 15:59:29 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 15:59:29 GMT
ARG KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 15:59:30 GMT
ENV KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 15:59:31 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 05 Oct 2022 15:59:32 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 05 Oct 2022 16:00:03 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:00:04 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:00:04 GMT
USER kong
# Wed, 05 Oct 2022 16:00:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:00:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:00:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:00:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:00:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27ee648e3be2639065d71cfba87c6c9d9d97d20920837e201328261d5786d66`  
		Last Modified: Wed, 05 Oct 2022 16:04:57 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee063d7cb8f1088bc6868dfa03aa1ff3523850ba73fdfb7da30a73defb968a0b`  
		Last Modified: Wed, 05 Oct 2022 16:05:07 GMT  
		Size: 71.7 MB (71710928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd23356d620515a3c2a3d982ed3c2ae1f2950af4cb40f5f356f64f5e0ba84e0`  
		Last Modified: Wed, 05 Oct 2022 16:04:55 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.0`

```console
$ docker pull kong@sha256:5a9796196a6f21216497e2e1a9a606dbe6cd1a2405d4f99ea9d97aef13d3c071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.0` - linux; amd64

```console
$ docker pull kong@sha256:8a54bbf5026200150c46a182e0d56d74ba7572d6cfe98e863fb20cdafce1d95e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51522357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bce760c29ce855d5935d777f2ec45b3a9ca895a09334825360cebd26a222e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 14 Sep 2022 00:07:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 14 Sep 2022 00:07:19 GMT
ARG ASSET=ce
# Wed, 14 Sep 2022 00:07:19 GMT
ENV ASSET=ce
# Wed, 14 Sep 2022 00:07:19 GMT
ARG EE_PORTS
# Wed, 14 Sep 2022 00:07:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Sep 2022 00:07:19 GMT
ARG KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 00:07:19 GMT
ENV KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 00:07:20 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 14 Sep 2022 00:07:20 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 14 Sep 2022 00:07:28 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 14 Sep 2022 00:07:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 14 Sep 2022 00:07:28 GMT
USER kong
# Wed, 14 Sep 2022 00:07:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Sep 2022 00:07:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Sep 2022 00:07:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Sep 2022 00:07:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 14 Sep 2022 00:07:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f8c583856d7a692eae94f47792d4cc4a214e2b9d36d1b6dd5eaded569804f`  
		Last Modified: Wed, 14 Sep 2022 00:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd3d1d803c378e5eb206c29367530e2f8a92578534afdf16cd4ff0da3e687f5`  
		Last Modified: Wed, 14 Sep 2022 00:09:33 GMT  
		Size: 48.7 MB (48715295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7a99de7f80d542680872b47fc5405bf068af5fa56916f994a15149ce05e441`  
		Last Modified: Wed, 14 Sep 2022 00:09:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:027a647f0c26cf6b7a763a87d0556f13f998bad6e894b8442442fcff3bb89744
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50657688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523519a6e5d6879a4227e5b1c165a53d9611b923a8202ae1f04050caef825747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Sep 2022 01:59:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 14 Sep 2022 01:59:10 GMT
ARG ASSET=ce
# Wed, 14 Sep 2022 01:59:11 GMT
ENV ASSET=ce
# Wed, 14 Sep 2022 01:59:12 GMT
ARG EE_PORTS
# Wed, 14 Sep 2022 01:59:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Sep 2022 01:59:14 GMT
ARG KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 01:59:15 GMT
ENV KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 01:59:16 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 14 Sep 2022 01:59:17 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 14 Sep 2022 01:59:26 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 14 Sep 2022 01:59:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 14 Sep 2022 01:59:27 GMT
USER kong
# Wed, 14 Sep 2022 01:59:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Sep 2022 01:59:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Sep 2022 01:59:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Sep 2022 01:59:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 14 Sep 2022 01:59:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033ed50262ad7d5f4f3be38481e74d6f1de3313623a89ec7a316233c87cb9f39`  
		Last Modified: Wed, 14 Sep 2022 02:02:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3318efbcbee2b6ebe247f02e9f3c2bdba1cad9ab96167a928e679b33cbe1bb41`  
		Last Modified: Wed, 14 Sep 2022 02:02:15 GMT  
		Size: 47.9 MB (47949011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fa05900110c4740c2e5720297d782338ded9ec460bf8d181fa6905ee5de189`  
		Last Modified: Wed, 14 Sep 2022 02:02:06 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.0-alpine`

```console
$ docker pull kong@sha256:5a9796196a6f21216497e2e1a9a606dbe6cd1a2405d4f99ea9d97aef13d3c071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:8a54bbf5026200150c46a182e0d56d74ba7572d6cfe98e863fb20cdafce1d95e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51522357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bce760c29ce855d5935d777f2ec45b3a9ca895a09334825360cebd26a222e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 14 Sep 2022 00:07:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 14 Sep 2022 00:07:19 GMT
ARG ASSET=ce
# Wed, 14 Sep 2022 00:07:19 GMT
ENV ASSET=ce
# Wed, 14 Sep 2022 00:07:19 GMT
ARG EE_PORTS
# Wed, 14 Sep 2022 00:07:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Sep 2022 00:07:19 GMT
ARG KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 00:07:19 GMT
ENV KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 00:07:20 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 14 Sep 2022 00:07:20 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 14 Sep 2022 00:07:28 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 14 Sep 2022 00:07:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 14 Sep 2022 00:07:28 GMT
USER kong
# Wed, 14 Sep 2022 00:07:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Sep 2022 00:07:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Sep 2022 00:07:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Sep 2022 00:07:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 14 Sep 2022 00:07:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f8c583856d7a692eae94f47792d4cc4a214e2b9d36d1b6dd5eaded569804f`  
		Last Modified: Wed, 14 Sep 2022 00:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd3d1d803c378e5eb206c29367530e2f8a92578534afdf16cd4ff0da3e687f5`  
		Last Modified: Wed, 14 Sep 2022 00:09:33 GMT  
		Size: 48.7 MB (48715295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7a99de7f80d542680872b47fc5405bf068af5fa56916f994a15149ce05e441`  
		Last Modified: Wed, 14 Sep 2022 00:09:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:027a647f0c26cf6b7a763a87d0556f13f998bad6e894b8442442fcff3bb89744
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50657688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523519a6e5d6879a4227e5b1c165a53d9611b923a8202ae1f04050caef825747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Sep 2022 01:59:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 14 Sep 2022 01:59:10 GMT
ARG ASSET=ce
# Wed, 14 Sep 2022 01:59:11 GMT
ENV ASSET=ce
# Wed, 14 Sep 2022 01:59:12 GMT
ARG EE_PORTS
# Wed, 14 Sep 2022 01:59:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Sep 2022 01:59:14 GMT
ARG KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 01:59:15 GMT
ENV KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 01:59:16 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 14 Sep 2022 01:59:17 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 14 Sep 2022 01:59:26 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 14 Sep 2022 01:59:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 14 Sep 2022 01:59:27 GMT
USER kong
# Wed, 14 Sep 2022 01:59:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Sep 2022 01:59:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Sep 2022 01:59:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Sep 2022 01:59:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 14 Sep 2022 01:59:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033ed50262ad7d5f4f3be38481e74d6f1de3313623a89ec7a316233c87cb9f39`  
		Last Modified: Wed, 14 Sep 2022 02:02:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3318efbcbee2b6ebe247f02e9f3c2bdba1cad9ab96167a928e679b33cbe1bb41`  
		Last Modified: Wed, 14 Sep 2022 02:02:15 GMT  
		Size: 47.9 MB (47949011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fa05900110c4740c2e5720297d782338ded9ec460bf8d181fa6905ee5de189`  
		Last Modified: Wed, 14 Sep 2022 02:02:06 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.0-ubuntu`

```console
$ docker pull kong@sha256:8a6061f898745d8d1ae6b9b2cc702d422e354844eefbfcd529353297e65ff47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b94b30d589c2d304b5c32ab10ce3c5b16f58b77c2aa363583da387c335c0fb48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126751347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a998d5233b41e636a9afe797738f040dfb82731ce74c88c9208bceae5ff1c5a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:03:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Oct 2022 18:03:44 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:03:44 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:03:44 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:03:44 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 18:03:45 GMT
ENV KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 05 Oct 2022 18:04:17 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:04:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:04:18 GMT
USER kong
# Wed, 05 Oct 2022 18:04:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:04:18 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:04:18 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:04:18 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:04:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a405c4afb98d18d76913bfe72f63dbd4a4d8c04256b6a7dfcbf44e6afba6f4`  
		Last Modified: Wed, 05 Oct 2022 18:06:58 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c61366193417348ac92ea7a0b85d3a941dd84e99ddce0ccf874f9e2dd064a6`  
		Last Modified: Wed, 05 Oct 2022 18:07:08 GMT  
		Size: 73.1 MB (73094048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff353d4dd575bdf6ca92775c17a2634b394fc8f507c04bbaedcdeee8e3eb48e`  
		Last Modified: Wed, 05 Oct 2022 18:06:56 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fdb693a2f651e8ea7fb72a3fbf27e948512f177e59bf67df495ace7bea594054
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123985385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5108a12659480aceff1ac2460acb6b4634ddee97df269cb93243ad915c17149e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 15:59:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Oct 2022 15:59:25 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 15:59:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 15:59:27 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 15:59:29 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 15:59:29 GMT
ARG KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 15:59:30 GMT
ENV KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 15:59:31 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 05 Oct 2022 15:59:32 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 05 Oct 2022 16:00:03 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:00:04 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:00:04 GMT
USER kong
# Wed, 05 Oct 2022 16:00:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:00:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:00:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:00:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:00:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27ee648e3be2639065d71cfba87c6c9d9d97d20920837e201328261d5786d66`  
		Last Modified: Wed, 05 Oct 2022 16:04:57 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee063d7cb8f1088bc6868dfa03aa1ff3523850ba73fdfb7da30a73defb968a0b`  
		Last Modified: Wed, 05 Oct 2022 16:05:07 GMT  
		Size: 71.7 MB (71710928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd23356d620515a3c2a3d982ed3c2ae1f2950af4cb40f5f356f64f5e0ba84e0`  
		Last Modified: Wed, 05 Oct 2022 16:04:55 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:5a9796196a6f21216497e2e1a9a606dbe6cd1a2405d4f99ea9d97aef13d3c071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:8a54bbf5026200150c46a182e0d56d74ba7572d6cfe98e863fb20cdafce1d95e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51522357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bce760c29ce855d5935d777f2ec45b3a9ca895a09334825360cebd26a222e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 14 Sep 2022 00:07:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 14 Sep 2022 00:07:19 GMT
ARG ASSET=ce
# Wed, 14 Sep 2022 00:07:19 GMT
ENV ASSET=ce
# Wed, 14 Sep 2022 00:07:19 GMT
ARG EE_PORTS
# Wed, 14 Sep 2022 00:07:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Sep 2022 00:07:19 GMT
ARG KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 00:07:19 GMT
ENV KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 00:07:20 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 14 Sep 2022 00:07:20 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 14 Sep 2022 00:07:28 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 14 Sep 2022 00:07:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 14 Sep 2022 00:07:28 GMT
USER kong
# Wed, 14 Sep 2022 00:07:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Sep 2022 00:07:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Sep 2022 00:07:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Sep 2022 00:07:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 14 Sep 2022 00:07:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f8c583856d7a692eae94f47792d4cc4a214e2b9d36d1b6dd5eaded569804f`  
		Last Modified: Wed, 14 Sep 2022 00:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd3d1d803c378e5eb206c29367530e2f8a92578534afdf16cd4ff0da3e687f5`  
		Last Modified: Wed, 14 Sep 2022 00:09:33 GMT  
		Size: 48.7 MB (48715295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7a99de7f80d542680872b47fc5405bf068af5fa56916f994a15149ce05e441`  
		Last Modified: Wed, 14 Sep 2022 00:09:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:027a647f0c26cf6b7a763a87d0556f13f998bad6e894b8442442fcff3bb89744
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50657688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523519a6e5d6879a4227e5b1c165a53d9611b923a8202ae1f04050caef825747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Sep 2022 01:59:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 14 Sep 2022 01:59:10 GMT
ARG ASSET=ce
# Wed, 14 Sep 2022 01:59:11 GMT
ENV ASSET=ce
# Wed, 14 Sep 2022 01:59:12 GMT
ARG EE_PORTS
# Wed, 14 Sep 2022 01:59:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Sep 2022 01:59:14 GMT
ARG KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 01:59:15 GMT
ENV KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 01:59:16 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 14 Sep 2022 01:59:17 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 14 Sep 2022 01:59:26 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 14 Sep 2022 01:59:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 14 Sep 2022 01:59:27 GMT
USER kong
# Wed, 14 Sep 2022 01:59:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Sep 2022 01:59:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Sep 2022 01:59:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Sep 2022 01:59:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 14 Sep 2022 01:59:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033ed50262ad7d5f4f3be38481e74d6f1de3313623a89ec7a316233c87cb9f39`  
		Last Modified: Wed, 14 Sep 2022 02:02:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3318efbcbee2b6ebe247f02e9f3c2bdba1cad9ab96167a928e679b33cbe1bb41`  
		Last Modified: Wed, 14 Sep 2022 02:02:15 GMT  
		Size: 47.9 MB (47949011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fa05900110c4740c2e5720297d782338ded9ec460bf8d181fa6905ee5de189`  
		Last Modified: Wed, 14 Sep 2022 02:02:06 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:5a9796196a6f21216497e2e1a9a606dbe6cd1a2405d4f99ea9d97aef13d3c071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:8a54bbf5026200150c46a182e0d56d74ba7572d6cfe98e863fb20cdafce1d95e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51522357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bce760c29ce855d5935d777f2ec45b3a9ca895a09334825360cebd26a222e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 14 Sep 2022 00:07:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 14 Sep 2022 00:07:19 GMT
ARG ASSET=ce
# Wed, 14 Sep 2022 00:07:19 GMT
ENV ASSET=ce
# Wed, 14 Sep 2022 00:07:19 GMT
ARG EE_PORTS
# Wed, 14 Sep 2022 00:07:19 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Sep 2022 00:07:19 GMT
ARG KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 00:07:19 GMT
ENV KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 00:07:20 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 14 Sep 2022 00:07:20 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 14 Sep 2022 00:07:28 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 14 Sep 2022 00:07:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 14 Sep 2022 00:07:28 GMT
USER kong
# Wed, 14 Sep 2022 00:07:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Sep 2022 00:07:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Sep 2022 00:07:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Sep 2022 00:07:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 14 Sep 2022 00:07:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f8c583856d7a692eae94f47792d4cc4a214e2b9d36d1b6dd5eaded569804f`  
		Last Modified: Wed, 14 Sep 2022 00:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd3d1d803c378e5eb206c29367530e2f8a92578534afdf16cd4ff0da3e687f5`  
		Last Modified: Wed, 14 Sep 2022 00:09:33 GMT  
		Size: 48.7 MB (48715295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7a99de7f80d542680872b47fc5405bf068af5fa56916f994a15149ce05e441`  
		Last Modified: Wed, 14 Sep 2022 00:09:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:027a647f0c26cf6b7a763a87d0556f13f998bad6e894b8442442fcff3bb89744
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50657688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523519a6e5d6879a4227e5b1c165a53d9611b923a8202ae1f04050caef825747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Sep 2022 01:59:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 14 Sep 2022 01:59:10 GMT
ARG ASSET=ce
# Wed, 14 Sep 2022 01:59:11 GMT
ENV ASSET=ce
# Wed, 14 Sep 2022 01:59:12 GMT
ARG EE_PORTS
# Wed, 14 Sep 2022 01:59:14 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Sep 2022 01:59:14 GMT
ARG KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 01:59:15 GMT
ENV KONG_VERSION=3.0.0
# Wed, 14 Sep 2022 01:59:16 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 14 Sep 2022 01:59:17 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 14 Sep 2022 01:59:26 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 14 Sep 2022 01:59:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 14 Sep 2022 01:59:27 GMT
USER kong
# Wed, 14 Sep 2022 01:59:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Sep 2022 01:59:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Sep 2022 01:59:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Sep 2022 01:59:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 14 Sep 2022 01:59:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033ed50262ad7d5f4f3be38481e74d6f1de3313623a89ec7a316233c87cb9f39`  
		Last Modified: Wed, 14 Sep 2022 02:02:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3318efbcbee2b6ebe247f02e9f3c2bdba1cad9ab96167a928e679b33cbe1bb41`  
		Last Modified: Wed, 14 Sep 2022 02:02:15 GMT  
		Size: 47.9 MB (47949011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fa05900110c4740c2e5720297d782338ded9ec460bf8d181fa6905ee5de189`  
		Last Modified: Wed, 14 Sep 2022 02:02:06 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:8a6061f898745d8d1ae6b9b2cc702d422e354844eefbfcd529353297e65ff47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b94b30d589c2d304b5c32ab10ce3c5b16f58b77c2aa363583da387c335c0fb48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126751347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a998d5233b41e636a9afe797738f040dfb82731ce74c88c9208bceae5ff1c5a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:03:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Oct 2022 18:03:44 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:03:44 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:03:44 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:03:44 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 18:03:45 GMT
ENV KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 05 Oct 2022 18:04:17 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:04:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:04:18 GMT
USER kong
# Wed, 05 Oct 2022 18:04:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:04:18 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:04:18 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:04:18 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:04:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a405c4afb98d18d76913bfe72f63dbd4a4d8c04256b6a7dfcbf44e6afba6f4`  
		Last Modified: Wed, 05 Oct 2022 18:06:58 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c61366193417348ac92ea7a0b85d3a941dd84e99ddce0ccf874f9e2dd064a6`  
		Last Modified: Wed, 05 Oct 2022 18:07:08 GMT  
		Size: 73.1 MB (73094048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff353d4dd575bdf6ca92775c17a2634b394fc8f507c04bbaedcdeee8e3eb48e`  
		Last Modified: Wed, 05 Oct 2022 18:06:56 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fdb693a2f651e8ea7fb72a3fbf27e948512f177e59bf67df495ace7bea594054
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123985385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5108a12659480aceff1ac2460acb6b4634ddee97df269cb93243ad915c17149e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 15:59:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Oct 2022 15:59:25 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 15:59:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 15:59:27 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 15:59:29 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 15:59:29 GMT
ARG KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 15:59:30 GMT
ENV KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 15:59:31 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 05 Oct 2022 15:59:32 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 05 Oct 2022 16:00:03 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 16:00:04 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 16:00:04 GMT
USER kong
# Wed, 05 Oct 2022 16:00:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:00:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 16:00:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 16:00:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 16:00:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27ee648e3be2639065d71cfba87c6c9d9d97d20920837e201328261d5786d66`  
		Last Modified: Wed, 05 Oct 2022 16:04:57 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee063d7cb8f1088bc6868dfa03aa1ff3523850ba73fdfb7da30a73defb968a0b`  
		Last Modified: Wed, 05 Oct 2022 16:05:07 GMT  
		Size: 71.7 MB (71710928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd23356d620515a3c2a3d982ed3c2ae1f2950af4cb40f5f356f64f5e0ba84e0`  
		Last Modified: Wed, 05 Oct 2022 16:04:55 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
