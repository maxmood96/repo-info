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
$ docker pull kong@sha256:e301cfd327ebc504e1e98f57d4b4bd88d77cc3b1d8b237f2775c018dc1ba9c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c95119594c1fa2794efb7f2ee17327b26228d87eb2b8f68825bd86e2348235a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121296390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bd7caeb7876255f1e8fa2aaad6a4719f82fea7c763527015bb23ee1f8bbf61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:14:37 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 20:14:38 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 20:16:43 GMT
ARG KONG_VERSION=2.5.2
# Tue, 02 Aug 2022 20:16:43 GMT
ENV KONG_VERSION=2.5.2
# Tue, 02 Aug 2022 20:16:43 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 02 Aug 2022 20:16:43 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 02 Aug 2022 20:17:03 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 20:17:04 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 20:17:04 GMT
USER kong
# Tue, 02 Aug 2022 20:17:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:17:05 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 20:17:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 20:17:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 20:17:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854dea64f4525bca9f7eb55f2e5efa5d22b4e423df94a80efd33d829ea77e080`  
		Last Modified: Tue, 02 Aug 2022 20:17:38 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bbe83f6088b06b73555031562502b10ff870d14fdb837f1395113c0707269d`  
		Last Modified: Tue, 02 Aug 2022 20:19:02 GMT  
		Size: 67.6 MB (67640950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e81aeb6041ba0439769070b8356128298d48f16bc9d509341bcdf197fce13b4`  
		Last Modified: Tue, 02 Aug 2022 20:18:51 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b00e73dbca1374dddd9df5f9bf0d0258e1c4f31b31df21053ea2899b4dea7585
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118335097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822080bf7da9d2bce940660752289714f9f23610f91a67f6773536c93b33fbd4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:22:28 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 18:22:29 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 18:22:30 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 18:22:32 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 18:27:15 GMT
ARG KONG_VERSION=2.5.2
# Tue, 02 Aug 2022 18:27:15 GMT
ENV KONG_VERSION=2.5.2
# Tue, 02 Aug 2022 18:27:16 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 02 Aug 2022 18:27:17 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 02 Aug 2022 18:28:49 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 18:28:50 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 18:28:50 GMT
USER kong
# Tue, 02 Aug 2022 18:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:28:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 18:28:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 18:28:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 18:28:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a20134f336ffe1be0b39dfe9f881b4683b6b17815677168c9aa88ce24c0e21`  
		Last Modified: Tue, 02 Aug 2022 18:30:00 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab50134d0d2d51134f9db539176c79ca3c5344bca084ce30c61ce6fcea9b99f`  
		Last Modified: Tue, 02 Aug 2022 18:31:27 GMT  
		Size: 66.1 MB (66060459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad9ca506ed58090e3956a5742d447125524c35538b7c794ba748c09fde3c91d`  
		Last Modified: Tue, 02 Aug 2022 18:31:16 GMT  
		Size: 880.0 B  
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
$ docker pull kong@sha256:e301cfd327ebc504e1e98f57d4b4bd88d77cc3b1d8b237f2775c018dc1ba9c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c95119594c1fa2794efb7f2ee17327b26228d87eb2b8f68825bd86e2348235a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121296390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bd7caeb7876255f1e8fa2aaad6a4719f82fea7c763527015bb23ee1f8bbf61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:14:37 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 20:14:38 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 20:16:43 GMT
ARG KONG_VERSION=2.5.2
# Tue, 02 Aug 2022 20:16:43 GMT
ENV KONG_VERSION=2.5.2
# Tue, 02 Aug 2022 20:16:43 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 02 Aug 2022 20:16:43 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 02 Aug 2022 20:17:03 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 20:17:04 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 20:17:04 GMT
USER kong
# Tue, 02 Aug 2022 20:17:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:17:05 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 20:17:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 20:17:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 20:17:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854dea64f4525bca9f7eb55f2e5efa5d22b4e423df94a80efd33d829ea77e080`  
		Last Modified: Tue, 02 Aug 2022 20:17:38 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bbe83f6088b06b73555031562502b10ff870d14fdb837f1395113c0707269d`  
		Last Modified: Tue, 02 Aug 2022 20:19:02 GMT  
		Size: 67.6 MB (67640950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e81aeb6041ba0439769070b8356128298d48f16bc9d509341bcdf197fce13b4`  
		Last Modified: Tue, 02 Aug 2022 20:18:51 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b00e73dbca1374dddd9df5f9bf0d0258e1c4f31b31df21053ea2899b4dea7585
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118335097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822080bf7da9d2bce940660752289714f9f23610f91a67f6773536c93b33fbd4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:22:28 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 18:22:29 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 18:22:30 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 18:22:32 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 18:27:15 GMT
ARG KONG_VERSION=2.5.2
# Tue, 02 Aug 2022 18:27:15 GMT
ENV KONG_VERSION=2.5.2
# Tue, 02 Aug 2022 18:27:16 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 02 Aug 2022 18:27:17 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 02 Aug 2022 18:28:49 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 18:28:50 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 18:28:50 GMT
USER kong
# Tue, 02 Aug 2022 18:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:28:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 18:28:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 18:28:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 18:28:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a20134f336ffe1be0b39dfe9f881b4683b6b17815677168c9aa88ce24c0e21`  
		Last Modified: Tue, 02 Aug 2022 18:30:00 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab50134d0d2d51134f9db539176c79ca3c5344bca084ce30c61ce6fcea9b99f`  
		Last Modified: Tue, 02 Aug 2022 18:31:27 GMT  
		Size: 66.1 MB (66060459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad9ca506ed58090e3956a5742d447125524c35538b7c794ba748c09fde3c91d`  
		Last Modified: Tue, 02 Aug 2022 18:31:16 GMT  
		Size: 880.0 B  
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
$ docker pull kong@sha256:b023a5e4931ad3325c69d5cba46872b5b51bef4f097768311f70a16ed7f77684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7f69e59136a0b8b6cf6635857305cf79ea5893b8236c7e271c2eb3e63805568b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128180582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27ef990b94043149a2a542765094ee090b5d1a6c5c0bebcb57bc47ad5a15fdc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:14:37 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 20:14:38 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 20:16:13 GMT
ARG KONG_VERSION=2.6.1
# Tue, 02 Aug 2022 20:16:13 GMT
ENV KONG_VERSION=2.6.1
# Tue, 02 Aug 2022 20:16:13 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 02 Aug 2022 20:16:13 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 02 Aug 2022 20:16:33 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 20:16:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 20:16:34 GMT
USER kong
# Tue, 02 Aug 2022 20:16:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:16:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 20:16:35 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 20:16:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 20:16:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854dea64f4525bca9f7eb55f2e5efa5d22b4e423df94a80efd33d829ea77e080`  
		Last Modified: Tue, 02 Aug 2022 20:17:38 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988b36b13333c70c6f2c566ff28758505797ea022b4ade9afe86973d30b66e35`  
		Last Modified: Tue, 02 Aug 2022 20:18:40 GMT  
		Size: 74.5 MB (74525145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d680afd35f508cb92ff76c3dca8415ebb807322372aee2b4c24480e1b4d6a6`  
		Last Modified: Tue, 02 Aug 2022 20:18:25 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d748c7c6975b06ac2bbc2ae31bbbe34508017b1f55565afc5da8d9310ff28e53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125234034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0331d84466d90ebd47ab67542441e7810e15a43b3d6b434c8c2b1f02a9bb62`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:22:28 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 18:22:29 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 18:22:30 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 18:22:32 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 18:25:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 02 Aug 2022 18:25:45 GMT
ENV KONG_VERSION=2.6.1
# Tue, 02 Aug 2022 18:25:46 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 02 Aug 2022 18:25:47 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 02 Aug 2022 18:26:57 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 18:26:58 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 18:26:58 GMT
USER kong
# Tue, 02 Aug 2022 18:26:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:27:00 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 18:27:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 18:27:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 18:27:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a20134f336ffe1be0b39dfe9f881b4683b6b17815677168c9aa88ce24c0e21`  
		Last Modified: Tue, 02 Aug 2022 18:30:00 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295c68f28e2da2dc84828df89f9f2e2ed102d6cc47b3ded4d579d1a8ad53ee2f`  
		Last Modified: Tue, 02 Aug 2022 18:31:02 GMT  
		Size: 73.0 MB (72959394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724a12b1a15d38bb4aeb452357e4e00a1aa09684818705ade03cdc3faa34794e`  
		Last Modified: Tue, 02 Aug 2022 18:30:51 GMT  
		Size: 882.0 B  
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
$ docker pull kong@sha256:b023a5e4931ad3325c69d5cba46872b5b51bef4f097768311f70a16ed7f77684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7f69e59136a0b8b6cf6635857305cf79ea5893b8236c7e271c2eb3e63805568b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128180582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27ef990b94043149a2a542765094ee090b5d1a6c5c0bebcb57bc47ad5a15fdc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:14:37 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 20:14:38 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 20:16:13 GMT
ARG KONG_VERSION=2.6.1
# Tue, 02 Aug 2022 20:16:13 GMT
ENV KONG_VERSION=2.6.1
# Tue, 02 Aug 2022 20:16:13 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 02 Aug 2022 20:16:13 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 02 Aug 2022 20:16:33 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 20:16:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 20:16:34 GMT
USER kong
# Tue, 02 Aug 2022 20:16:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:16:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 20:16:35 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 20:16:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 20:16:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854dea64f4525bca9f7eb55f2e5efa5d22b4e423df94a80efd33d829ea77e080`  
		Last Modified: Tue, 02 Aug 2022 20:17:38 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988b36b13333c70c6f2c566ff28758505797ea022b4ade9afe86973d30b66e35`  
		Last Modified: Tue, 02 Aug 2022 20:18:40 GMT  
		Size: 74.5 MB (74525145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d680afd35f508cb92ff76c3dca8415ebb807322372aee2b4c24480e1b4d6a6`  
		Last Modified: Tue, 02 Aug 2022 20:18:25 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d748c7c6975b06ac2bbc2ae31bbbe34508017b1f55565afc5da8d9310ff28e53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125234034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0331d84466d90ebd47ab67542441e7810e15a43b3d6b434c8c2b1f02a9bb62`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:22:28 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 18:22:29 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 18:22:30 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 18:22:32 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 18:25:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 02 Aug 2022 18:25:45 GMT
ENV KONG_VERSION=2.6.1
# Tue, 02 Aug 2022 18:25:46 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 02 Aug 2022 18:25:47 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 02 Aug 2022 18:26:57 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 18:26:58 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 18:26:58 GMT
USER kong
# Tue, 02 Aug 2022 18:26:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:27:00 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 18:27:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 18:27:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 18:27:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a20134f336ffe1be0b39dfe9f881b4683b6b17815677168c9aa88ce24c0e21`  
		Last Modified: Tue, 02 Aug 2022 18:30:00 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295c68f28e2da2dc84828df89f9f2e2ed102d6cc47b3ded4d579d1a8ad53ee2f`  
		Last Modified: Tue, 02 Aug 2022 18:31:02 GMT  
		Size: 73.0 MB (72959394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724a12b1a15d38bb4aeb452357e4e00a1aa09684818705ade03cdc3faa34794e`  
		Last Modified: Tue, 02 Aug 2022 18:30:51 GMT  
		Size: 882.0 B  
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
$ docker pull kong@sha256:ef129115a0828878e9aaf400f415a02e3229cce371e6c9f5ed07fb285c9a888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d0a060245580a92ef4ebc2e9a3d75ff2d7173fc8a1360245d0b96be9daa1ac0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128094152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3250322b975a69861b7038367d54560d167045308c796fca83fe2828f62fe4a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:14:37 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 20:14:38 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 20:15:37 GMT
ARG KONG_VERSION=2.7.2
# Tue, 02 Aug 2022 20:15:37 GMT
ENV KONG_VERSION=2.7.2
# Tue, 02 Aug 2022 20:15:37 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 02 Aug 2022 20:15:37 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 02 Aug 2022 20:16:05 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 20:16:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 20:16:06 GMT
USER kong
# Tue, 02 Aug 2022 20:16:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:16:06 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 20:16:07 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 20:16:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 20:16:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854dea64f4525bca9f7eb55f2e5efa5d22b4e423df94a80efd33d829ea77e080`  
		Last Modified: Tue, 02 Aug 2022 20:17:38 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a8a18fdffc941532100ad1bbbc342ebcca23960197d227ddd1f8091d4253bc`  
		Last Modified: Tue, 02 Aug 2022 20:18:14 GMT  
		Size: 74.4 MB (74438714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e169b354aa97e3fecc77cf1bea15830d880e16b3534cae8c98b26875119bce`  
		Last Modified: Tue, 02 Aug 2022 20:18:01 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f119be7cc1e78fbbc12cb3021202bb14ac81637586a0e60639a88bc68319f95b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125141734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1213baedb89be3aea612cb20097232ca5db5a6012d384bdb36a5d49764207530`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:22:28 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 18:22:29 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 18:22:30 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 18:22:32 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 18:24:14 GMT
ARG KONG_VERSION=2.7.2
# Tue, 02 Aug 2022 18:24:14 GMT
ENV KONG_VERSION=2.7.2
# Tue, 02 Aug 2022 18:24:15 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 02 Aug 2022 18:24:16 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 02 Aug 2022 18:25:22 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 18:25:23 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 18:25:23 GMT
USER kong
# Tue, 02 Aug 2022 18:25:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:25:25 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 18:25:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 18:25:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 18:25:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a20134f336ffe1be0b39dfe9f881b4683b6b17815677168c9aa88ce24c0e21`  
		Last Modified: Tue, 02 Aug 2022 18:30:00 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7da216270cc8f6f53e42a2940f5cdbea7eb1a6e2bf9d260cd18627840b1965`  
		Last Modified: Tue, 02 Aug 2022 18:30:38 GMT  
		Size: 72.9 MB (72867095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624f56ae7c3c190418ea649134e91b401125a190b56a10533d4a6fde15747c96`  
		Last Modified: Tue, 02 Aug 2022 18:30:26 GMT  
		Size: 881.0 B  
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
$ docker pull kong@sha256:ef129115a0828878e9aaf400f415a02e3229cce371e6c9f5ed07fb285c9a888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d0a060245580a92ef4ebc2e9a3d75ff2d7173fc8a1360245d0b96be9daa1ac0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128094152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3250322b975a69861b7038367d54560d167045308c796fca83fe2828f62fe4a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:14:37 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 20:14:38 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 20:15:37 GMT
ARG KONG_VERSION=2.7.2
# Tue, 02 Aug 2022 20:15:37 GMT
ENV KONG_VERSION=2.7.2
# Tue, 02 Aug 2022 20:15:37 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 02 Aug 2022 20:15:37 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 02 Aug 2022 20:16:05 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 20:16:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 20:16:06 GMT
USER kong
# Tue, 02 Aug 2022 20:16:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:16:06 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 20:16:07 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 20:16:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 20:16:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854dea64f4525bca9f7eb55f2e5efa5d22b4e423df94a80efd33d829ea77e080`  
		Last Modified: Tue, 02 Aug 2022 20:17:38 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a8a18fdffc941532100ad1bbbc342ebcca23960197d227ddd1f8091d4253bc`  
		Last Modified: Tue, 02 Aug 2022 20:18:14 GMT  
		Size: 74.4 MB (74438714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e169b354aa97e3fecc77cf1bea15830d880e16b3534cae8c98b26875119bce`  
		Last Modified: Tue, 02 Aug 2022 20:18:01 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f119be7cc1e78fbbc12cb3021202bb14ac81637586a0e60639a88bc68319f95b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125141734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1213baedb89be3aea612cb20097232ca5db5a6012d384bdb36a5d49764207530`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:22:28 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 18:22:29 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 18:22:30 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 18:22:32 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 18:24:14 GMT
ARG KONG_VERSION=2.7.2
# Tue, 02 Aug 2022 18:24:14 GMT
ENV KONG_VERSION=2.7.2
# Tue, 02 Aug 2022 18:24:15 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 02 Aug 2022 18:24:16 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 02 Aug 2022 18:25:22 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 18:25:23 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 18:25:23 GMT
USER kong
# Tue, 02 Aug 2022 18:25:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:25:25 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 18:25:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 18:25:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 18:25:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a20134f336ffe1be0b39dfe9f881b4683b6b17815677168c9aa88ce24c0e21`  
		Last Modified: Tue, 02 Aug 2022 18:30:00 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7da216270cc8f6f53e42a2940f5cdbea7eb1a6e2bf9d260cd18627840b1965`  
		Last Modified: Tue, 02 Aug 2022 18:30:38 GMT  
		Size: 72.9 MB (72867095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624f56ae7c3c190418ea649134e91b401125a190b56a10533d4a6fde15747c96`  
		Last Modified: Tue, 02 Aug 2022 18:30:26 GMT  
		Size: 881.0 B  
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
$ docker pull kong@sha256:71caba649c5b03500e54b9ef2ca0bbfeed089f91658b52fc1dfa11705b7cde8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e1b1acc841d2534d6f0e2e4633831aba8d072f2f1d697e8812b49a9ed0c8484a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121218256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ca4a8b9412ef4a23651bafcfb89e78bba2f64d17809a787fa3d9f0d6890dd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:14:37 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 20:14:38 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 20:14:38 GMT
ARG KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 20:14:38 GMT
ENV KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 20:14:38 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 02 Aug 2022 20:14:38 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 02 Aug 2022 20:15:24 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 20:15:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 20:15:25 GMT
USER kong
# Tue, 02 Aug 2022 20:15:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:15:25 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 20:15:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 20:15:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 20:15:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854dea64f4525bca9f7eb55f2e5efa5d22b4e423df94a80efd33d829ea77e080`  
		Last Modified: Tue, 02 Aug 2022 20:17:38 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e24c4b15808b8f1d25ce96dc579fd911346c704c0397dffad4260576f8853a`  
		Last Modified: Tue, 02 Aug 2022 20:17:48 GMT  
		Size: 67.6 MB (67562816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f435cfaf25b88220250cbe77bf45fe13378cf2312c2c8c25076e9f7a7cbb77ae`  
		Last Modified: Tue, 02 Aug 2022 20:17:36 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c851e0f1ea8edf17d0f5716f00ec80df53fdfd5fc499ea2ffd059c5b32079231
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121719836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013903134f69f9b05fcf835e4dd034f014d00525765a77bd540d32d91e329664`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:22:28 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 18:22:29 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 18:22:30 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 18:22:32 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 18:22:32 GMT
ARG KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 18:22:33 GMT
ENV KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 18:22:34 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 02 Aug 2022 18:22:35 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 02 Aug 2022 18:23:49 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 18:23:50 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 18:23:50 GMT
USER kong
# Tue, 02 Aug 2022 18:23:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:23:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 18:23:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 18:23:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 18:23:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a20134f336ffe1be0b39dfe9f881b4683b6b17815677168c9aa88ce24c0e21`  
		Last Modified: Tue, 02 Aug 2022 18:30:00 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6825ebf20e3660ab016cc28bf97c0361540bd69c94ed14ad0310693ff42ca370`  
		Last Modified: Tue, 02 Aug 2022 18:30:09 GMT  
		Size: 69.4 MB (69445197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d5e7198cee26634852b73e68d863129627e454ad8aecfaf8f958c9af42f85b`  
		Last Modified: Tue, 02 Aug 2022 18:29:57 GMT  
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
$ docker pull kong@sha256:71caba649c5b03500e54b9ef2ca0bbfeed089f91658b52fc1dfa11705b7cde8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e1b1acc841d2534d6f0e2e4633831aba8d072f2f1d697e8812b49a9ed0c8484a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121218256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ca4a8b9412ef4a23651bafcfb89e78bba2f64d17809a787fa3d9f0d6890dd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:14:37 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 20:14:38 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 20:14:38 GMT
ARG KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 20:14:38 GMT
ENV KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 20:14:38 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 02 Aug 2022 20:14:38 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 02 Aug 2022 20:15:24 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 20:15:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 20:15:25 GMT
USER kong
# Tue, 02 Aug 2022 20:15:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:15:25 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 20:15:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 20:15:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 20:15:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854dea64f4525bca9f7eb55f2e5efa5d22b4e423df94a80efd33d829ea77e080`  
		Last Modified: Tue, 02 Aug 2022 20:17:38 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e24c4b15808b8f1d25ce96dc579fd911346c704c0397dffad4260576f8853a`  
		Last Modified: Tue, 02 Aug 2022 20:17:48 GMT  
		Size: 67.6 MB (67562816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f435cfaf25b88220250cbe77bf45fe13378cf2312c2c8c25076e9f7a7cbb77ae`  
		Last Modified: Tue, 02 Aug 2022 20:17:36 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c851e0f1ea8edf17d0f5716f00ec80df53fdfd5fc499ea2ffd059c5b32079231
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121719836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013903134f69f9b05fcf835e4dd034f014d00525765a77bd540d32d91e329664`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:22:28 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 18:22:29 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 18:22:30 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 18:22:32 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 18:22:32 GMT
ARG KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 18:22:33 GMT
ENV KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 18:22:34 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 02 Aug 2022 18:22:35 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 02 Aug 2022 18:23:49 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 18:23:50 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 18:23:50 GMT
USER kong
# Tue, 02 Aug 2022 18:23:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:23:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 18:23:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 18:23:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 18:23:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a20134f336ffe1be0b39dfe9f881b4683b6b17815677168c9aa88ce24c0e21`  
		Last Modified: Tue, 02 Aug 2022 18:30:00 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6825ebf20e3660ab016cc28bf97c0361540bd69c94ed14ad0310693ff42ca370`  
		Last Modified: Tue, 02 Aug 2022 18:30:09 GMT  
		Size: 69.4 MB (69445197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d5e7198cee26634852b73e68d863129627e454ad8aecfaf8f958c9af42f85b`  
		Last Modified: Tue, 02 Aug 2022 18:29:57 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:4dc4da99f8da9e4d7ab01da7feb3062ba12be1324fa8359f2396bbb7ac07bb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

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

### `kong:alpine` - linux; arm64 variant v8

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

## `kong:latest`

```console
$ docker pull kong@sha256:4dc4da99f8da9e4d7ab01da7feb3062ba12be1324fa8359f2396bbb7ac07bb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

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

### `kong:latest` - linux; arm64 variant v8

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

## `kong:ubuntu`

```console
$ docker pull kong@sha256:71caba649c5b03500e54b9ef2ca0bbfeed089f91658b52fc1dfa11705b7cde8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e1b1acc841d2534d6f0e2e4633831aba8d072f2f1d697e8812b49a9ed0c8484a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121218256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ca4a8b9412ef4a23651bafcfb89e78bba2f64d17809a787fa3d9f0d6890dd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:14:37 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 20:14:38 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 20:14:38 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 20:14:38 GMT
ARG KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 20:14:38 GMT
ENV KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 20:14:38 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 02 Aug 2022 20:14:38 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 02 Aug 2022 20:15:24 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 20:15:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 20:15:25 GMT
USER kong
# Tue, 02 Aug 2022 20:15:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:15:25 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 20:15:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 20:15:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 20:15:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854dea64f4525bca9f7eb55f2e5efa5d22b4e423df94a80efd33d829ea77e080`  
		Last Modified: Tue, 02 Aug 2022 20:17:38 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e24c4b15808b8f1d25ce96dc579fd911346c704c0397dffad4260576f8853a`  
		Last Modified: Tue, 02 Aug 2022 20:17:48 GMT  
		Size: 67.6 MB (67562816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f435cfaf25b88220250cbe77bf45fe13378cf2312c2c8c25076e9f7a7cbb77ae`  
		Last Modified: Tue, 02 Aug 2022 20:17:36 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c851e0f1ea8edf17d0f5716f00ec80df53fdfd5fc499ea2ffd059c5b32079231
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121719836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013903134f69f9b05fcf835e4dd034f014d00525765a77bd540d32d91e329664`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:22:28 GMT
ARG ASSET=ce
# Tue, 02 Aug 2022 18:22:29 GMT
ENV ASSET=ce
# Tue, 02 Aug 2022 18:22:30 GMT
ARG EE_PORTS
# Tue, 02 Aug 2022 18:22:32 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Aug 2022 18:22:32 GMT
ARG KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 18:22:33 GMT
ENV KONG_VERSION=2.8.1
# Tue, 02 Aug 2022 18:22:34 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 02 Aug 2022 18:22:35 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 02 Aug 2022 18:23:49 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 02 Aug 2022 18:23:50 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 02 Aug 2022 18:23:50 GMT
USER kong
# Tue, 02 Aug 2022 18:23:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:23:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Aug 2022 18:23:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Aug 2022 18:23:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 02 Aug 2022 18:23:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a20134f336ffe1be0b39dfe9f881b4683b6b17815677168c9aa88ce24c0e21`  
		Last Modified: Tue, 02 Aug 2022 18:30:00 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6825ebf20e3660ab016cc28bf97c0361540bd69c94ed14ad0310693ff42ca370`  
		Last Modified: Tue, 02 Aug 2022 18:30:09 GMT  
		Size: 69.4 MB (69445197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d5e7198cee26634852b73e68d863129627e454ad8aecfaf8f958c9af42f85b`  
		Last Modified: Tue, 02 Aug 2022 18:29:57 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
